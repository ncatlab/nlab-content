## Idea

How do you type check [[linear logic|MILL]], but with projections rather than matching to eliminate $\otimes$? This page gives algorithmic rules that are intended to do that. [Mike Shulman](#Shulman) showed a not-especially-algorithmic type system based on [[PROPs]], but it doesn't handle [[linear implication]].

## Judgment form, Notations

$U \subseteq \Gamma \vdash t\,:\,T\,\boxtimes\,U' \subseteq \Gamma'$

$U$, $\Gamma$, and $t$ are inputs; $T$, $U'$, and $\Gamma'$ are outputs.

The observation in [Allais](#Allais) motivating the use of "$\boxtimes$" was that a term is implicitly tensored with the identity on all the unused resources.

$\Gamma$ and $\Gamma'$ are [[contexts]] with some natural number of semicolon "scope" delimiters. $U$ and $U'$ are "usage" sets, which are subsets of the (domains of the) respective contexts. In [Allais](#Allais), the usage sets are represented as bit vectors (which is a fine way to implement them). Unlike [Allais](#Allais), the usage before and after are for *different* contexts, because type checking a term generally adds projections to the context as potentially-consumed resources.

The purpose of delimited scopes in the context is to remember by when we must've consumed tensor projections. Currently, only lambda adds a scope delimiter. The current algorithm puts projections in the outermost scope it can get away with. This approach will not work when adding additive connectives.

In the rules, I implicitly coerce a context to the usage set of its entire domain. The abbreviation $(\Gamma \mapsto \Gamma')U$ "weakens" $U$ to include all entries in $\Gamma'$ but not $\Gamma$. Set theoretically speaking: $(\Gamma \mapsto \Gamma')U \coloneqq U \cup (\Gamma' \setminus \Gamma)$. "$\Delta$" and variants are used as metavariables for contexts *without any delimiters*.

Some important (intended) properties of the judgment form are that if $U \subseteq \Gamma \vdash t\,:\,T\,\boxtimes\,U' \subseteq \Gamma'$, then:

* $U \subseteq \Gamma$ and $U' \subseteq \Gamma'$
* $\Gamma$ and $\Gamma'$ have the same number of delimiters.
* $\Gamma'$ includes all the entries of $\Gamma$, in the same scopes. (So in particular, $\Gamma \subseteq \Gamma'$.)
* $U' \subseteq (\Gamma \mapsto \Gamma')U$

Note that the context grows while the usage shrinks. Erm, I guess these usage sets are the sets of resources *not* used (and thus available). $(\Gamma \mapsto \Gamma')U$ should be understood as the *actual* usage indicated by $U \subseteq \Gamma$, in light of the additional resources in $\Gamma'$. So as the type checker proceeds, more resources are known of, but fewer remain available.

## Generators and Functions

There are generator morphisms, which can be used any number of times. $f \in \mathcal{G}(A;\overrightarrow{B})$ means you can get $f\,:\,A \multimap \overrightarrow{B}$ whenever you want.

Functions take exactly one argument, and have one or more results. Semantically, the results are tensored ($\otimes$) together. Following [Shulman](#Shulman), multiple results are accessed using "generalized Sweedler notation". For example, if $f(a)$ has two results, they are typically written as $f_{(1)}(a)$ and $f_{(2)}(a)$. Using *both* results is a *single* use of linear implication elimination. This is actually the only way to use tensor projections, currently. Combining it with function application was purely a matter of convenience, and is probably a bad idea, for adding more connectives.

## Rules

$$\frac{t:T \in U}{U \subseteq \Gamma \vdash t\,:\,T\,\boxtimes\,U \setminus \{t\} \subseteq \Gamma}$$

Yes, you get *terms* out of the context, not just variables. For now, the only terms that end up in the context are variables and tensor projections. $(t:T) \in U$ really means $(t:T) \in \Gamma$ and $t \in U$, since the type is stored in $\Gamma$.

$$\begin{gathered}
\frac{f \in \mathcal{G}(A;\overrightarrow{B})}
{U \subseteq \Gamma \vdash f\,:\,A \multimap \overrightarrow{B}\,\boxtimes\,U \subseteq \Gamma} \\
\\
\frac{}{U \subseteq \Gamma \vdash ()\,:\,\mathbf{1}\,\boxtimes\,U \subseteq \Gamma} \\
\\
\frac{U \subseteq \Gamma \vdash c\,:\,\mathbf{1}\,\boxtimes\,U_1 \subseteq \Gamma_1 \qquad
U_1 \subseteq \Gamma_1 \vdash t\,:\,T\,\boxtimes\,U_2 \subseteq \Gamma_2}
{U \subseteq \Gamma \vdash c;\,t\,:\,T\,\boxtimes\,U_2 \subseteq \Gamma_2} \\
\\
\frac{U \subseteq \Gamma \vdash a\,:\,A\,\boxtimes\,U_1 \subseteq \Gamma_1 \qquad
U_1 \subseteq \Gamma_1 \vdash b\,:\,B\,\boxtimes\,U_2 \subseteq \Gamma_2}
{U \subseteq \Gamma \vdash (a,b)\,:\,A \otimes B\,\boxtimes\,U_2 \subseteq \Gamma_2} \\
\\
\frac{}{U \subseteq \Gamma \vdash \pi\,:\,(A \otimes B) \multimap (A,B)\,\boxtimes\,U \subseteq \Gamma}
\end{gathered}$$

Yeah, that's tensor elim now. Kind of funky.

$$\frac{U \cup \{x\} \subseteq \Gamma;x:A \vdash b\,:\,B_1 \otimes \dots \otimes B_n\,\boxtimes\,U' \subseteq \Gamma';\Delta \qquad
U' \cap \Delta = \emptyset}
{U \subseteq \Gamma \vdash \lambda x:A.b\,:\,A \multimap (B_1,\dots,B_n)\,\boxtimes\,U' \subseteq \Gamma'}$$

There is a new scope for checking the body, which starts out with just the bound variable. When done checking, there's generally more stuff in it. Currently, that would only be tensor projections. In any case, everything in the new scope must've been consumed.

$$\frac{U \subseteq \Gamma \vdash f\,:\,A \multimap B\,\boxtimes\,U_1 \subseteq \Gamma_1 \qquad
U_1 \subseteq \Gamma_1 \vdash a\,:\,A\,\boxtimes\,U_2 \subseteq \Gamma_2}
{U \subseteq \Gamma \vdash f(a)\,:\,B\,\boxtimes\,U_2 \subseteq \Gamma_2}$$

That's the *nice* application rule, for when there's one result. Now for the *nasty* ones...

$$\frac{\begin{array}{l}f_{(i)}(a) \notin \Gamma \\
U \subseteq \Gamma \vdash f\,:\,A \multimap \overrightarrow{B}\,\boxtimes\,U_1 \subseteq \Gamma_1 \\
U_1 \subseteq \Gamma_1 \vdash a\,:\,A\,\boxtimes\,U_2 \subseteq \Gamma_2 \\
|\overrightarrow{B}| \gt 1 \qquad 0 \lt i \leq |\overrightarrow{B}| \\
U_d = (\Gamma \mapsto \Gamma_2)U \setminus U_2 \\
\Gamma_2 = \Gamma_l;\Delta;\Gamma_r \\
U_d \cap \Gamma_r = \emptyset \qquad U_d \cap \Delta \neq \emptyset \\
\Gamma_3 = \Gamma_l;\Delta,\overrightarrow{f(a):B};\Gamma_r \\
U_3 = (\Gamma_2 \mapsto \Gamma_3)U_2 \setminus \{f_{(i)}(a)\}\end{array}}
{U \subseteq \Gamma \vdash f_{(i)}(a)\,:\,B_i\,\boxtimes\,U_3 \subseteq \Gamma_3}$$

$$\;$$

$$\frac{\begin{array}{l}f^u_{(i)}(a) \notin \Gamma \\
U \subseteq \Gamma \vdash f\,:\,A \multimap \overrightarrow{B}\,\boxtimes\,U_1 \subseteq \Gamma_1 \\
U_1 \subseteq \Gamma_1 \vdash a\,:\,A\,\boxtimes\,U_2 \subseteq \Gamma_2 \\
|\overrightarrow{B}| \gt 1 \qquad 0 \lt i \leq |\overrightarrow{B}| \\
(\Gamma \mapsto \Gamma_2)U \setminus U_2 = \emptyset \\
\Gamma_2 = \Delta_l;\Gamma_r \\
\Gamma_3 = \Delta_l,\overrightarrow{f^u(a):B};\Gamma_r \\
U_3 = (\Gamma_2 \mapsto \Gamma_3)U_2 \setminus \{f^u_{(i)}(a)\}\end{array}}
{U \subseteq \Gamma \vdash f^u_{(i)}(a)\,:\,B_i\,\boxtimes\,U_3 \subseteq \Gamma_3}$$

Whew. These rules add tensor projections of a function application to the context, the first time the application is encountered in a given scope. There are two rules because if the application doesn't consume any resources, there's generally an ambiguity between multiple instances of the application, so we add a "label" to disambiguate. $u$ is the label metavariable. This labeling idea is from [Shulman](#Shulman). See there for a discussion of the problem.

In the rule mentioning $U_d$, $U_d$ is the set of resources consumed by the application. That is, both the function and argument. The premise $U_d \cap \Delta \neq \emptyset$ implies that $U_d$ is nonempty. Meanwhile, the other rule checks that the same computed usage *is* empty.

In both rules, $\Gamma_2$ is split to find the scope to which the projections are added. If the application uses resources, that scope is the innermost scope with resources that were used. Otherwise it's the outermost scope.

The projections cannot go in a scope outside one with resources used, because then there would be no way to get the variables out there in ordinary MILL using a match.

On the other hand, it can be trouble to put the projections in a scope more inside than necessary, since the lambda rule checks that everything in its scope was consumed. The projections only need to be consumed before one of their dependencies goes out of scope. For example, ($\lambda x:A.((\lambda y:B.(y,f_{(1)}(x))),f_{(2)}(x))$) means ($\lambda x:A.let\;(f_1,f_2) = f(x)\;in\;((\lambda y:B.(y,f_1)),f_2)$), but would be rejected if we naively put $f(x)$ into the scope in which it's first encountered.

## References

These algorithmic rules are loosely based on:

* {#Allais} Guillaume Allais, _Typing with Leftovers – A mechanization of Intuitionistic Multiplicative-Additive Linear Logic_, TYPES 2017 ([pdf](http://drops.dagstuhl.de/opus/volltexte/2018/10049/pdf/LIPIcs-TYPES-2017-1.pdf))

The idea to allow tensor projections in some sound way, and a lot of the notation, are from:

* {#Shulman} [[Michael Shulman]], _A practical type theory for symmetric monoidal categories_, 2019 ([arXiv](https://arxiv.org/abs/1911.00818))
## Idea

How do you type check MILL, but with projections rather than matching to eliminate $\otimes$? This page gives algorithmic rules that are intended to do that. [Mike Shulman](#Shulman) showed a not-especially-algorithmic type system based on props, but it doesn't handle linear implication.

## Judgment form

$U \subseteq \Gamma \vdash t\,:\,T\,\Box\,U' \subseteq \Gamma'$

The $\Box$ would ideally be a `\boxtimes`, like in [Allais](#Allais), but that doesn't seem to be available. The observation was that a term is implicitly tensored with the identity on all the unused resources.

$\Gamma$ and $\Gamma'$ are contexts with some natural number of semicolon "scope" delimiters. $U$ and $U'$ are "usage" sets, which are subsets of the (domains of the) respective contexts. In [Allais](#Allais), the usage sets are represented as bit vectors (which is a fine way to implement them). Unlike [Allais](#Allais), the usage before and after are for *different* contexts, because type checking a term generally adds projections to the context as potentially-consumed resources.

The purpose of delimited scopes in the context is to remember by when we must've consumed tensor projections. Currently, only lambda adds a scope delimiter. The current algorithm puts projections in the outermost scope it can get away with. This approach will not work when adding additive connectives.

In the rules, I implicitly coerce a context to the usage set of its entire domain. The abbreviation $(\Gamma \mapsto \Gamma')U$ "weakens" $U$ to include all entries in $\Gamma'$ but not $\Gamma$. Set theoretically speaking: $(\Gamma \mapsto \Gamma')U \coloneqq U \cup (\Gamma' \setminus \Gamma)$.

Some important (intended) properties of the judgment form are that if ($U \subseteq \Gamma \vdash t\,:\,T\,\Box\,U' \subseteq \Gamma'$), then:

* $\Gamma$ and $\Gamma'$ have the same number of delimiters.
* $\Gamma'$ includes all the entries of $\Gamma$, in the same scopes. (So in particular, $\Gamma \subseteq \Gamma'$.)
* $U' \subseteq (\Gamma \mapsto \Gamma')U$

Note that the context grows while the usage shrinks. Erm, I guess these usage sets are the sets of resources *not* used (and thus available). $(\Gamma \mapsto \Gamma')U$ should be understood as the *actual* usage indicated by $U \subseteq \Gamma$, in light of the additional resources in $\Gamma'$. So as the type checker proceeds, more resources are known of, but fewer remain available.

## Generators and Functions

There are generator morphisms, which can be used any number of times. $f \in \mathcal{G}(A;\overrightarrow{B})$ means you can get $f\,:\,A \multimap \overrightarrow{B}$ whenever you want.

Functions take exactly one argument, and have one or more results. Semantically, the results are tensored ($\otimes$) together. Following [Shulman](#Shulman), multiple results are accessed using "generalized Sweedler notation". For example, if $f(a)$ has two results, they are typically written as $f_{(1)}(a)$ and $f_{(2)}(a)$. Using *both* results is a *single* use of linear implication elimination. This is actually the only way to use tensor projections, currently. Combining it with function application was purely a matter of convenience, and is probably a bad idea, for adding more connectives.

## Rules

$$\frac{t:T \in U}{U \subseteq \Gamma \vdash t\,:\,T\,\Box\,U \setminus \{t\} \subseteq \Gamma}$$

Remark: Yes, you get *terms* out of the context, not just variables. For now, the only terms that end up in the context are variables and tensor projections. $(t:T) \in U$ really means $(t:T) \in \Gamma$ and $t \in U$, since the type is stored in $\Gamma$.

$$\begin{gathered}
\frac{f \in \mathcal{G}(A;\overrightarrow{B})}
{U \subseteq \Gamma \vdash f\,:\,A \multimap \overrightarrow{B}\,\Box\,U \subseteq \Gamma} \\
\\
\frac{}{U \subseteq \Gamma \vdash ()\,:\,1\,\Box\,U \subseteq \Gamma} \\
\\
\frac{U \subseteq \Gamma \vdash c\,:\,1\,\Box\,U_1 \subseteq \Gamma_1 \qquad
U_1 \subseteq \Gamma_1 \vdash t\,:\,T\,\Box\,U_2 \subseteq \Gamma_2}
{U \subseteq \Gamma \vdash c;\,t\,:\,T\,\Box\,U_2 \subseteq \Gamma_2}
\end{gathered}$$

## References

These algorithmic rules are loosely based on:

* {#Allais} Guillaume Allais, _Typing with Leftovers – A mechanization of Intuitionistic Multiplicative-Additive Linear Logic_, TYPES 2017 ([pdf](http://drops.dagstuhl.de/opus/volltexte/2018/10049/pdf/LIPIcs-TYPES-2017-1.pdf))

The idea to allow tensor projections in some sound way, and a lot of the notation, are from:

* {#Shulman} Michael Shulman, _A practical type theory for symmetric monoidal categories_, 2019 ([arXiv](https://arxiv.org/abs/1911.00818))
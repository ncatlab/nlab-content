
# Limits of functions
* table of contents
{: toc}

## Idea

Although it has less emphasis in advanced mathematics, and although its definition is more complicated than that of the [[limit of a sequence]], the first concept of limit seen by most students is that of a limit of a [[function]].  This is the idea that
$$ \lim_{x \to c} f(x) = L $$
means that $f(x)$ is close to $L$ if $x$ is sufficiently close to $c$.  Of course, $x$ here is just a dummy variable, so this is really a [[ternary relation]] between $f$, $c$, and $L$.


## Definitions {#definitions}

Limits of functions could be defined for functions between various mathematical structures, such as subsets of the [[real numbers]], [[metric spaces]] and [[topological spaces]]. In all cases, there are two different definitions of limit of a function, depending on whether one uses the definition by [[Nicolas Bourbaki]] or the historical definition, first defined by [[Karl Weierstrass]] in the context of partial functions on the real numbers and later generalized to metric spaces and topological spaces. Bourbaki's definition is commonly used in the French language, while Weierstrass's definition is commonly used in the English language. Weierstrass's definition is also referred to as the *punctured limit* of a function ("limite épointée" in French), because it uses [[accumulation points]] and [[punctured neighborhoods]] instead of [[adherent points]] and [[neighborhoods]]. 

### In metric spaces

Let $(X, d_X)$ and $(Y, d_Y)$ be [[metric spaces]], and let $f$ be a [[function]] from $X$ to $Y$, let $c$ be an [[adherent point]] of $X$, and let $L$ be an element in $Y$. Then

> the **limit of $f$ approaching $c$** is $L$ if for all positive real numbers $\epsilon$ there exists a positive real number $\delta$ such that for all elements $x \in X$, $d_X(x, c) \lt \delta$ implies that $d_Y(f(x), L) \lt \epsilon$. 

Alternatively, let $c$ be an [[accumulation point]] of $X$. Then

> the **(punctured) limit of $f$ approaching $c$** is $L$ if for all positive real numbers $\epsilon$ there exists a positive real number $\delta$ such that for all elements $x \in X$, $0 \lt d_X(x, c)$ and $d_X(x, c) \lt \delta$ implies that $d_Y(f(x), L) \lt \epsilon$. 

In [[dependent type theory]], "there exists" can be represented either by the [[existential quantifier]] or the [[dependent sum type]]. In the latter case, one has an element of the following type for limits as defined by Bourbaki

$$\prod_{\epsilon:\mathbb{R}_+} \sum_{\delta:\mathbb{R}_+} \prod_{x:X} (d_X(x, c) \lt \delta) \to (d_Y(f(x), L) \lt \epsilon)$$

and similarly for punctured limits

$$\prod_{\epsilon:\mathbb{R}_+} \sum_{\delta:\mathbb{R}_+} \prod_{x:X} (0 \lt d_X(x, c)) \times (d_X(x, c) \lt \delta) \to (d_Y(f(x), L) \lt \epsilon)$$

By the [[type theoretic axiom of choice]], which is simply the distributivity of [[dependent function types]] over [[dependent sum types]], this is the same as saying, respectively 

> the **limit (as defined by Bourbaki) of $f$ approaching $c$** is $L$ if there exists as structure a function $\omega:\mathbb{R}_+ \to \mathbb{R}_+$ such that for all positive real numbers $\epsilon$ and for all elements $x \in X$, $d_X(x, c) \lt \omega(\epsilon)$ implies that $d_Y(f(x), L) \lt \epsilon$. 

$$\sum_{\omega:\mathbb{R}_+ \to \mathbb{R}_+}\prod_{\epsilon:\mathbb{R}_+} \prod_{x:X} (d_X(x, c) \lt \omega(\epsilon)) \to (d_Y(f(x), L) \lt \epsilon)$$

> the **(punctured) limit of $f$ approaching $c$** is $L$ if there exists as structure a function $\omega:\mathbb{R}_+ \to \mathbb{R}_+$ such that for all positive real numbers $\epsilon$ and for all elements $x \in X$, $0 \lt d_X(x, c)$ and $d_X(x, c) \lt \omega(\epsilon)$ implies that $d_Y(f(x), L) \lt \epsilon$. 

$$\sum_{\omega:\mathbb{R}_+ \to \mathbb{R}_+}\prod_{\epsilon:\mathbb{R}_+} \prod_{x:X} (0 \lt d_X(x, c)) \times (d_X(x, c) \lt \omega(\epsilon)) \to (d_Y(f(x), L) \lt \epsilon)$$

### In uniform spaces

The definition of a limit of a function as defined by Bourbaki can be generalized from [[metric spaces]] to [[uniform spaces]]:

Let $(X, \mathcal{U}(X), \approx)$ and $(Y, \mathcal{U}(Y), \approx)$ be [[uniform spaces]], and let $f$ be a [[function]] from $X$ to $Y$, let $c$ be an [[adherent point]] of $X$, and let $L$ be an element in $Y$.  Then, 

> the **limit of $f$ approaching $c$** is $L$ if for all [[entourages]] $E \in \mathcal{U}(Y)$ there exists an entourage $D \in \mathcal{U}(X)$ such that for all elements $x \in X$, $x \approx_D c$ implies that $f(x) \approx_E L$. 

And similarly, in [[dependent type theory]], if one were using the [[dependent sum type]] to represent "there exists", one has an element of the following type

$$\prod_{E:\mathcal{U}(Y)} \sum_{D:\mathcal{U}(X)} \prod_{x:X} (x \approx_D c) \to (f(x) \approx_E L)$$

which, by the [[type theoretic axiom of choice]], which is simply the distributivity of [[dependent function types]] over [[dependent sum types]], is the same as saying 

> the **limit of $f$ approaching $c$** is $L$ if there exists as structure a function $\omega:\mathcal{U}(Y) \to \mathcal{U}(X)$ such that for all entourages $E$ and for all elements $x \in X$, $x \approx_{\omega(E)} c$ implies that $f(x) \approx_E L$. 

$$\sum_{\omega:\mathcal{U}(Y) \to \mathcal{U}(X) }\prod_{E:\mathcal{U}(Y)} \prod_{x:X} (x \approx_{\omega(E)} c) \to (f(x) \approx_E L)$$

### In topological spaces

Let $X$ and $Y$ be [[topological spaces]], let $f$ be a [[partial function]] from $X$ to $Y$ (*not* assumed continuous or anything else), let $c$ be a [[limit point]] of the domain $D$ of $f$ in $X$, and let $L$ be a point in $Y$.

There are actually two definitions of 'limit point' in the literature: an [[adherent point]] and an [[accumulation point]].  And there are two definitions of 'limit' in this context: the usual French-language one (following [[Bourbaki]]) and the usual English-language one.  These definitions correspond respectively.  In both cases, the first definition is simpler, while the second is more common.

+-- {: .num_defn #French}
###### Definition
**(French)**

$L$ is a __limit__ of $f$ approaching $c$ (assumed to be an adherent point of the domain $D$) if, for each [[neighbourhood]] $V$ of $L$, for some neighbourhood $U$ of $c$, for each point $x \in U \cap D$, we have $f(x) \in V$.
=--

+-- {: .num_defn #English}
###### Definition
**(English)**

$L$ is a __limit__ of $f$ approaching $c$ (assumed to be an accumulation point of the domain $D$) if, for each [[neighbourhood]] $V$ of $L$, for some [[punctured neighborhood|punctured neighbourhood]] $U$ of $c$, for each point $x \in U \cap D$, we have $f(x) \in V$.  Equivalently, for each neighbourhood $V$ of $L$, for some neighbourhood $U'$ of $c$, for each point $x \in U' \cap D$, if $x \ne c$, then $f(x) \in V$.
=--

Note that in each case, $U \cap D$ is [[inhabited subset|inhabited]] precisely because $c$ is a limit point of $D$.  That is, in the French definition, $U \cap D$ must be inhabited because an adherent point of $D$ is precisely a point $c$ such that each neighbourhood of $c$ meets $D$; while in the English definition, $U \cap D$ must be inhabited because an accumulation point of $D$ is precisely a point $c$ such that each punctured neighbourhood of $c$ meets $D$.  If we did not require $c$ to be such a limit point (in other words, if we allowed $c$ to have a [punctured] neighbourhood $U$ that was disjoint from $D$), then every value $L$ would satisfy the definition vacuously.

The two notions of limit can each be defined in terms of the other:
+-- {: .num_prop #translation}
###### Proposition

$L$ is a limit of $f$ approaching $c$ by the English definition if and only if $L$ is a limit of $f|_{\hat{c}}$ approaching $c$ by the French definition, where $f|_{\hat{c}}$ is the [[restriction]] of $f$ to the [[relative complement]] $D \setminus \{c\}$ of $c$ in the original domain $D$.  Conversely, $L$ is a limit of $f$ approaching $c$ by the French definition if and only if $c$ is an adherent point of the domain $D$ and these two hypothetical conditions are met: if $f$ is defined at $c$ (in other words, if $c$ belongs to $D$), then $f(c)$ belongs to every neighbourhood of $L$; and if $c$ is an accumulation point of $D$, then $L$ is a limit of $f$ approaching $c$ by the English definition.
=--

The basic difference is that the English definition doesn\'t care about $f(c)$ itself, while the French definition does.  For the French, $f$ must be continuous at $c$ if it is defined there, or equivalently (in the Hausdorff case), $f(c)$ must equal the limit $L$ if it exists at all.  This makes the French definition more strict when both make sense, but it also allows the French definition to make sense at isolated points of the domain $D$, since we know what the value must be there.  For $c \notin D$, then the two definitions are equivalent.

These limits can be defined as [[limits of a filter]]:
+-- {: .num_prop #filter}
###### Proposition

Let $\mathcal{N}_c$ be the [[neighbourhood filter]] of $c$, and let $\dot{\mathcal{N}}_c$ be the filter of punctured neighbourhoods of $c$.  Then the filter $f(\mathcal{N}_c)$ is [[proper filter|proper]] iff $c$ is an adherent point of the domain $D$, and $f(\dot{\mathcal{N}}_c)$ is proper iff $c$ is an accumulation point of $D$.  Futhermore, $L$ is a limit of $f$ approaching $c$ by the French definition iff $L$ is a limit of $f(\mathcal{N}_c)$, and $L$ is a limit of $f$ approaching $c$ by the English definition iff $L$ is a limit of $f(\dot{\mathcal{N}}_c)$.
=--

Here, $f(\mathcal{F})$ is the filter generated by the [[filterbase]] of sets $f(A)$ for $A \in \mathcal{F}$, where $f(A)$ is the image $\{ f(x) \;|\; x \in A \}$.  As an immediate corollary, if $Y$ is [[Hausdorff space|Hausdorff]], then $L$ must be the *only* limit of $f$ approaching $c$.

We can generalize from functions to [[multivalued functions]]; since we\'re already using partial functions, this means that we are dealing with an arbitrary [[binary relation]].  That is, let $X$ and $Y$ be topological spaces, let $R$ be a relation from $X$ to $Y$, let $c$ be a limit (adherent or accumulation) point of the domain $D$ of $R$ in $X$, and let $L$ be a point in $Y$.

+-- {: .num_defn #relations}
###### Definition

$L$ is a __limit__ of $R$ approaching $c$ if, for each neighbourhood $V$ of $L$, for some [punctured] neighbourhood $U$ of $c$, for each point $x \in U \cap D$, we have $R(x) \subseteq V$.
=--

Here, $R(x)$ is the set $\{ y \in Y \;|\; (x,y) \in R \}$ of values of $R$ at $x$.  Again, there are both French-style and English-style versions of the definition.  This can also be defined as the limit of a filter $R(\mathcal{N}_c)$ or $R(\dot{\mathcal{N}}_c)$, where $R(\mathcal{F})$ is generated by the sets $R(A) = \bigcup_{x \in A} R(x)$ for $A \in \mathcal{F}$.  In particular, limits of multivalued functions are still unique, so long as the [[target]] $Y$ is Hausdorff.

We may generalize further from relations to [[spans]].  Let $X$ and $Y$ be topological spaces, let $\Gamma$ be any [[set]], let $g\colon \Gamma \to X$ and $f\colon \Gamma \to Y$ be (total) functions, let $c$ be a limit (adherent or accumulation) point of the [[range]] $D$ of $g$ in $X$, and let $L$ be a point in $Y$.

+-- {: .num_defn #spans}
###### Definition

$L$ is a __limit__ of the span $(g,f)$ approaching $c$ if, for each neighbourhood $V$ of $L$, for some [punctured] neighbourhood $U$ of $c$, for each element $\gamma$ of the [[preimage]] $g^*(U \cap D)$, we have $f(\gamma) \in V$.
=--

Once again, there are both French-style and English-style versions of the definition.  And this too can be defined as the limit of a filter $f(g^*(\mathcal{N}_c))$ or $f(g^*(\dot{\mathcal{N}}_c))$, where $g^*(\mathcal{F})$ consists of the [[preimages]] $g^*(A)$ for $A \in \mathcal{F}$.  In particular, limits of spans to a Hausdorff space are unique.

Limits of spans are no more general than limits of relations:
+-- {: .num_prop #spansrelations}
###### Proposition

$L$ is a limit of the span $(g,f)$ approaching $c$ if and only if $L$ is a limit of the [[range]] $\ran(g,f) = \{ g(\gamma), f(\gamma) \;|\; \gamma \in \Gamma \}$ approaching $c$.
=--
(But often the span is more convenient to refer to than its range.)

Finally, we may impose restrictions on the limit:
+-- {: .num_defn #restricted}
###### Definition

Let $C$ be a [[subset]] of $X$, and suppose that $c$ is a limit (adherent or accumulation) point of $C$.  Then $L$ is a __limit__ of the function $f$ (or the relation $R$, or the span $(g,f)$) approaching $c$ in $C$ if $L$ is a limit of the [[restriction]] $f|_C$ of $f$ to $D \cap C$ (or the restriction $R \cap (C \times Y)$ of $R$, or the restriction $(g|_{g^*(C)},f|_{g^*(C)})$ of $(g,f)$).  In the case of the limit of a span, we can also let $C$ be a subset of $\Gamma$; then the limit in question is the limit of $(g|_C,f|_C)$.
=--

Yet again, there are both French-style and English-style versions, although these are equivalent when $c \notin C$.  And once more, this is the limit of a filter, since it reduces to a previous definition.

This concept allows us to define the English version of limit directly as a French limit:
+-- {: .num_prop}
###### Proposition

$L$ is a limit (in the English sense) of $f$ (or $R$, or $(g,f)$) approaching $c$ in $C$ if and only if $L$ is a limit (in the French sense) of $f$ (or $R$, or $(g,f)$) approaching $c$ in $C \setminus \{c\}$.
=--

To go more general than this would seem to require referring directly to a [[net]] $\nu$ or [[filter]] $\mathcal{F}$ on $X$, at which point we may as well just talk about the [[limit of the net]] $f \circ \nu$ or the [[limit of the filter]] $f(\mathcal{F})$ (or of the filter $R(\mathcal{F})$ or of the filter $f(g^*(\mathcal{F}))$).


## Notation

In the Hausdorff case, we usually write
$$ L = \lim_{x \to c} f(x) $$
to say that $L$ is a limit, or rather *the* limit, of $f$ approaching $c$.  Or indeed, just write
$$ \lim_{x \to c} f(x) $$
for the limit, if it exists (so, like $1/x$ when $x$ is an arbitrary real number, this is a symbol for a thing that might not be defined).  Since $x$ is just a dummy variable here, one can try a notation that does not refer to it, such as $ \lim_c f$ or $f(c^\pm)$.

The last notation is not very common, but some variations of it are when $X$ is a topological [[poset]]: $f(c^-)$ is the limit of $f$ approaching $c$ in $C = \{ x \in X \;|\; x \lt c \}$, while $f(c^+)$ is the limit of $f$ approaching $c$ in $C = \{ x \in X \;|\; x \gt c \}$.  Similarly, $f(\infty)$ is the limit of $f$ approaching $\infty$, where the domain $X$ is taken to be the [[disjoint union]] (as a set) of the original topological poset and a point $\infty$ that is greater than every original element and whose neighbourhoods are the [[upper sets]] of $X$; while $f(-\infty)$ is the limit of $f$ approaching $-\infty$, where the domain $X$ is taken to be the disjoint union of the original topological poset and a point $-\infty$ that is less than every original element and whose neighbourhoods are the [[lower sets]] of $X$.  (In all of these, the French and English definitions agree.)

For the general restricted case, write
$$ \lim_{x \to c \atop x \in C} f(x) $$
for the limit of $f$ approaching $c$ in $C$.  The dummy variable is quite useful here, since neither $f$ nor $C$ have to be given names but can be given by formulas instead.  (For example, $f(c^+)$ is $\lim_{x \to c \atop x \gt c} f(x)$.)

In the non-Hausdorff case, we can use the same notation but interpret it as referring to a [[subset]] of $Y$ instead of an element of $Y$.  Then this subset always exists; it just might be [[empty subset|empty]].  Sometimes a capitalized $Lim$ is used to emphasize that this is now a set.  This set can also be taken to be all of $Y$ whenever $c$ is not a limit point of the appropriate kind, but this is likely to lead to confusion if not explicitly warned about.

Another notation, especially useful when $Y$ is non-Hausdorff, but common even in the Hausdorff case, is
$$ f(x) \underset{x \to c}{\to} L $$
to mean that $L$ is a limit of $f$ approaching $c$.  Again, we can add $x \in C$ if we wish to take the limit in $C$.  And again, the dummy variable means that we don\'t need a name for $f$ (or $C$), just a formula.  Often one writes only $f(x) \to L$ and puts $x \to c$ (and $x \in C$ if appropriate) off to the side somewhere:

* $f(x) \to L$ as $x \to c$ while $x \in C$,

or with more words: $f(x)$ approaches $L$ as $x$ approaches $c$ while $x \in C$.

Most of this notation can also be used for limits of spans:
$$ \array { L = \lim_{g(\gamma) \to c \atop \gamma \in C} f(\gamma) ,\\
L \in \underset{g(\gamma) \to c \atop \gamma \in C}{Lim} f(\gamma) ,\\
f(\gamma) \underset{g(\gamma) \to c \atop \gamma \in C}{\to} L } $$
all mean that $L$ is a limit of $(g,f)$ approaching $c$ in $C$.  Thus the most general notion of limit appearing here is to say that $f(\gamma)$ approaches $L$ as $g(\gamma)$ approaches $c$ while $\gamma \in C$.

It would be nice to have notation to distinguish the French and English versions of limit.  One way would be to adopt the French definition by default and add the restriction $x \ne c$ to produce the English version.  Unfortunately, the English definition is the default in most of the world, and then there is no slick way to denote the French version.


## Examples

A function $f$ is [[continuous function|continuous]] at a point $c$ in its domain $D$, if and only if $f(c)$ is a limit of $f$ approaching $c$ by the French definition; $f$ is continuous at $c$ if and only if, if $c$ is an accumulation point of $D$, then $f(c)$ is a limit of $f$ approaching $c$ by the English definition.  (If $c$ is an [[isolated point]] of $D$, then of course $f$ is continuous there.)

Given a [[real number|real]]-valued function $F$ defined on a real [[interval]] $[a,b]$, we can speak of tagged partitions of $[a,b]$ and consider the [[Riemann sum|Riemann sums]] of $F$ on these tagged partitions.  Let $X$ and $Y$ each be the [[real line]], let $\Gamma$ be the set of tagged partitions of $[a,b]$, let $g\colon \Gamma \to X$ map a partition to the maximum length of its parts (often called the norm or mesh of the partition), and let $f\colon \Gamma \to Y$ map a tagged partition to the Riemann sum of $F$ on it.  Then the [[Riemann integral]] of $F$ on $[a,b]$ is defined to be the limit of the span $(f,g)$ approaching $0$.  That is, the Riemann integral of a function on an interval is the limit of the Riemann sum of the function on a tagged partition of the interval as the mesh of the partition approaches zero.

Let $A$ be a [[directed set]] and let $\nu\colon A \to Y$ be a [[net]] in $Y$.  Give $A$ the [[discrete topology]], and let $X$ be the [[disjoint union]] (as a set) of $A$ and $\{\infty\}$, made into a [[proset]] with $x \lt \infty$ for $x \in A$, and made into a topological space with the neighbourhoods of $\infty$ being the [[upper sets]] of $X$.  Interpret $\nu$ as a partial function from $X$ to $Y$.  Then the limits of $\nu$ approaching $\infty$ are precisely the [[limit of a net|limits]] of $\nu$ as a net.  That is, $\lim \nu = \lim_{x \to \infty} \nu_x$.


## Properties

Some basic relationships between the definitions are in the [definitions](#definitions) section.

As stated in the examples, $f$ is [[continuous function|continuous]] at a point $c$ in its domain $D$ if and only if $f(c)$ is a limit of $f$ approaching $c$ by the French definition, while $f$ is continuous at $c$ if and only if, if $c$ is an accumulation point of $D$, then $f(c)$ is a limit of $f$ approaching $c$ by the English definition.  In this way, pointwise continuity may be defined using limits.

Conversely, limits can be defined using pointwise continuity; the basic idea is that $L$ is a limit of $f$ at $c$ if setting $f(c)$ to $L$ makes $f$ continuous.  For once, this is easier to describe using the English definition: $L$ is the limit of $f$ at an accumulation point $c$ of the domain $D$ if and only if $f_{c \mapsto L}$ is continuous at $c$, where
$$ f_{c \mapsto L}(x) \coloneqq \left\{ \array{ f(x) & x \ne c,\; x \in D ,\\ L & x = c .}\right. $$
For the French definition, in addition to allowing $c$ to be any adherent point of $D$, we use
$$ f_{c \mapsto L}(x) \coloneqq \left\{ \array{ f(x) & x \in D ,\\ L & x = c ,}\right. $$
where the definition by cases is interpreted to mean that the value of the function is undefined if the two cases overlap and give different results.  Except that even this is only correct when the target $Y$ of $f$ is Hausdorff (or at least $\mathrm{T}_1$); in general, we have to allow the value to be defined if the two cases overlap and give different results as long as one result is in the closure of the other (and then we use the other).

There is a Chain Rule for limits.  Using the French definition, the limit of a [[composite]] function $f \circ g$ approaching $c$ is equal to the limit of $f$ approaching the limit of $g$ approaching $c$, if the latter exists:
$$ \lim_{x \to c} f(g(x)) \risingdotseq \lim_{u \to \lim_{x \to c} g(x)} f(u) ,$$
or equivalently $(f \circ g)(c^\pm) \risingdotseq f(g(c^\pm)^\pm)$, where $A \risingdotseq B$ means that $A$ and $B$ are equal if $B$ exists (and $A \fallingdotseq B$ means that $A$ and $B$ are equal if $A$ exists).  Using the English definition, this holds if we impose the requirement that if $g$ takes the value $\lim_c g$ arbitrarily close to $c$ (regardless of its value at $c$) and $f$ is defined there, then $f$ is continuous there.  Either way, we can write
$$ \lim_{x \to c} f(g(x)) = f\Big(\lim_{x \to c} g(x)\Big) $$
if $f$ is continuous at $\lim_c g$.

## See also ##

* [[function limit space]]

## References

* Claude Deschamps, François Moulin, André Warusfel et al., Mathématiques tout-en-un MPSI - 4e éd.: conforme au nouveau programme, Concours Ecoles d'ingénieurs, Dunod, 2015. ISBN:9782100730438

* Wikipédia, <a href="https://fr.wikipedia.org/wiki/Limite_(mathématiques)">Limite (mathématiques)</a>

* Wikipedia, [Limit of a function](https://en.wikipedia.org/wiki/Limit_of_a_function)

[[!redirects limit of a function]]
[[!redirects limits of a function]]
[[!redirects limit of functions]]
[[!redirects limits of functions]]
[[!redirects limit of the function]]
[[!redirects limit of the functions]]
[[!redirects limits of the function]]
[[!redirects limits of the functions]]

[[!redirects limit of a relation]]
[[!redirects limits of a relation]]
[[!redirects limit of relations]]
[[!redirects limits of relations]]
[[!redirects limit of the relation]]
[[!redirects limits of the relation]]
[[!redirects limit of the relations]]
[[!redirects limits of the relations]]

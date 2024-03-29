
# Prometric spaces
* table of contents
{: toc}

## Definitions

Let $X$ be an abstract [[set]].  For purposes of this definition, let a _distance function_ on $X$ be a [[positive number|nonnegative]]-[[extended real number|extended]]-[[real number|real]]-valued [[binary function|binary]] [[function]] on $X$; that is, a function $d\colon X \times X \to [0,\infty]$.

(For most purposes, we may assume that these distance functions are _pointwise-bounded_: taking only finite values.  On the other hand, for full generality in [[constructive mathematics]], we must allow the distance functions to take nonnegative extended *[[upper real|upper]]* real values, although again we may assume them to be pointwise-bounded and pointwise-[[located real number|located]] for many purposes.)

Let $G$ be a collection of such distance functions.


### Elementary axioms {#elementary}

Consider the following potential properties of $G$:

1. _Reflexivity_:  For every $d \in G$ and $x \in X$, we have $d(x,x) = 0$.

2. _Transitivity_ (a version of the [[triangle identity]]):  For any $d \in G$ there exists an $e \in G$ with
   $$ d(x,z) \leq e(x,y) + e(y,z) $$
   for all $x,y,z \in X$.

3. _Symmetry_:  For every $d \in G$, there is an $e \in G$ with $d(x,y) \leq e(y,x)$ for all $x,y \in X$.  (In light of Isotony below, we may require $d(x,y) = e(y,x)$.)

4. _Nontriviality_:  There exists a $d \in G$.  (In light of Isotony below, we may require $d(x,y) = 0$ for all $x,y \in X$.)

5. _Filtration_:  For all $d,e \in G$, there is an $f \in G$ with $d(x,y) \leq f(x,y)$ and $e(x,y) \leq f(x,y)$ for all $x,y \in X$.  (In light of Isotony below, we may require $f(x,y) = \max(d(x,y), e(x,y))$ for all $x,y \in X$.)

6. _Isotony_:  If $d \in G$ and $e$ is a distance function with $e(x,y) \leq d(x,y)$ for all $x,y \in X$, then $e \in G$.


### Sophisticated axioms {#sophisticated}

With the aid of [[abstract algebra]] (but nothing too fancy), we may view these same 6 axioms in another light, as follows.

First, the [[function set]] $[0,\infty]^{X \times X}$ of all distance functions $d\colon X \times X \to [0,\infty]$ on $X$ is a [[lattice group|lattice]] $*$-[[star-monoid|monoid]] under these operations:

* The order $\leq$ is given pointwise:
  $$ d \leq e \;\iff\; \forall(x,y\colon X),\; d(x,y) \leq e(x,y) .$$

* The corresponding [[join]] operation $\vee$ is also pointwise:
  $$ (d \vee e)(x,y) \coloneqq \max(d(x,y), e(x,y)) .$$

* The corresponding [[bottom element]] is the [[zero function]] $0$:
  $$ 0(x,y) \coloneqq 0 .$$

* The monoid operation $\circ$ is defined so:
  $$ (d \circ e)(x,z) \coloneqq \inf_{y \in X} (d(x,y) + e(y,z)) .$$

* The corresponding [[identity element]] is the infinite [[Kronecker delta]] $\delta$:
  $$ \delta(x,y) \coloneqq \begin{cases}
                           0      & if\; x = y,\\
                           \infty & if\; x \ne y.
                           \end{cases} $$
  (This works in [[constructive mathematics]] because we are using extended *[[upper real number|upper]]* reals; $\delta(x,y)$ is the [[infimum]] of the set $\{ t\colon \mathbb{R} \;|\; t = 0 \;\wedge\; x = y \}$.)

* The [[involution]] $d \mapsto d^{\op}$ is defined so:
  $$ d^{\op}(x,y) \coloneqq d(y,x) .$$

Then the same 6 axioms may be expressed as follows:

1. Reflexivity:  For every $d \in G$, we have $d \leq \delta$.

2. Transitivity:  For every $d \in G$, there exists $e \in G$ such that $d \leq e \circ e$.

3. Symmetry:  For every $d \in G$, there exists $e \in G$ such that $d \leq e^{\op}$.  (In light of Isotony, we may require $d = e^op$; in other words, $d^op \in G$.)

4. Nontriviality:  There exists a $d \in G$.  (In light of Isotony, we may require $d = 0$.)

5. Filtration:  For all $d,e \in G$, there is an $f \in G$ with $d \leq f$ and $e \leq f$.  (In light of Isotony, we may require $f = d \vee e$.)

6. Isotony:  If $d \in G$ and $e$ is a distance function with $e \leq d$, then $e \in G$.

It is possible to generate these even more systematically by specifying a [[proarrow equipment]] and considering the (possibly symmetric) [[pro-object|pro]]-[[monads]] in it; see the [Categorial interpretation](#proarrows) below.


### Unbiased versions

Reflexivity and Transitivity are a binary--nullary pair whose [[unbiased]] combination is as follows:

* [Elementary](#elementary) version:  For every [[natural number]] $n = 0,1,2,\ldots$ and every $d \in G$, there exists $e \in G$ with
   $$ d(x_0,x_n) \leq \sum_{i \lt n} e(x_i,x_{i+}) $$
   for each [[list]] $x_0,\ldots,x_n \in X$.

* [Sophisticated](#sophisticated) version:  For every [[natural number]] $n = 0,1,2,\ldots$ and every $d \in G$, there exists $e \in G$ such that $d \leq e^{\circ n}$.

We can combine these with Symmetry by generalizing $n$ from a natural number to a [[list]] $\epsilon$ of [[bits]] and replacing $e(x_i,x_{i+})$ with $e(x_{i+},x_i)$ (that is, replacing $e$ with $e^{\op}$ in the $i$th position) when $\epsilon_i = 1$.

Similarly, Nontriviality and Filtration are a binary--nullary pair whose unbiased version states (in light of Isotony) closure under finitary joins; but this is properly discussed at [[ideal]].


### Structures and spaces

A collection $G$ of distance functions that satisfies all of (1--6) is a __prometric__; if we drop (3), then we still have a __quasi-prometric__.  If we are working with quasi-prometrics generally, then one that happens to satisfy (3) is called __symmetric__; in other words, a prometric is precisely a symmetric quasi-prometric.

Finally, a __prometric space__ is a set equipped with a prometric, and likewise a __quasi-prometric space__ is a set equipped with a quasi-prometric.


### Generating (quasi)-prometrics

We sometimes wish to consider collections of distance functions that generate (quasi)-prometrics.  In the following table, a collection $G$ satisfying the conditions listed on the left has the name on the right:

| Conditions | Name |
| - | - |
| 1,2 | __pre-quasi-prometric__ |
| 1,2,3 | __pre-prometric__ |
| &#8199;&#8201;&#8199;&#8201;&#8199;&#8201;4,5 | [[ideal base]] |
| 1,2,&#8199;&#8201;4,5 | quasi-prometric __[[base]]__ |
| 1,2,3,4,5 | prometric __base__ |
| &#8199;&#8201;&#8199;&#8201;&#8199;&#8201;4,5,6 | [[ideal]] |
| 1,2,&#8199;&#8201;4,5,6 | quasi-prometric |
| 1,2,3,4,5,6 | prometric |

Here we always use the original (either [elementary](#elementary) or [sophisticated](#sophisticated)) formulation of (3--5); one might consider what it means if these satisfy the stronger versions rewritten in light of Isotony, but it\'s getting a bit far along into [[centipede mathematics]] to actually give these things names.

A (quasi)-prometric base is precisely an ideal base whose generated ideal is a (quasi)-prometric.  We may also speak of a (quasi)-prometric __subbase__ as an [[ideal subbase]] (that is, an arbitrary collection) whose generated ideal base is a (quasi)-prometric base, or equivalently whose generated ideal is a (quasi)-prometric.  A pre-(quasi)-prometric is always a (quasi)-prometric subbase, but not conversely; but thinking too hard about subbases risks more centipedes.

A pre-quasi-prometric is __symmetric__ if its generated quasi-prometric is symmetric (hence a prometric); a quasi-prometric base is symmetric iff it is a prometric base (and the analogous result holds for subbases), but a symmetric pre-quasi-prometric need not be a pre-prometric.  Some authors may require a strong version of Symmetry in which the distance functions $d$ are all individually required to be [[symmetric binary function|symmetric]]; that is, $d(x,y) = d(y,x)$ (or simply $d = d^{\op}$).  Every prometric has a base with this property; in particular, if $G$ is a prometric, then
$$ \{ d \in G \;|\; d = d^{\op} \} $$
is a prometric base that generates $G$, and it is this base that some authors may refer to as the prometric itself.  (I write 'some authors may', but there are few authors on this subject; still, it\'s the sort of thing that somebody might do.)

A pre-quasi-prometric $G$ is __pointwise-bounded__ if every $d \in G$ is pointwise-bounded; that is, $d(x,y) \lt \infty$ for every $x,y \in X$ (or simply $d \lt \infty$).  If $G$ is a (quasi)-prometric, then
$$ G_b \coloneqq \{ d \in G \;|\; d \lt \infty \} $$
is a (quasi)-prometric that is very similar to $G$ (in particular, they are [[uniformly equivalent]]), and some authors may prefer to work with $G_b$.  Indeed, when pointwise boundedness is *not* required, some authors may call the structure __extended__, as an instance of the [[red herring principle]].  However, requiring pointwise boundedness interferes with the more sophisticated approaches to (quasi)-prometrics; in particular, $\delta$ is not pointwise-bounded.  (It is possible that prometric spaces would work better with a closure condition that would make $G_b$ generate $G$.)

Most definitions are no more complicated when phrased in terms of (quasi)-prometric bases or even pre-(quasi)-prometrics, and some constructions give one of these more naturally than the generated (quasi)-prometric.  When working in [[predicative mathematics]], it is preferable to work exclusively with (quasi)-prometric bases, as the generated (quasi)-prometric will typically be a [[proper class]].  However, it is ultimately the generated (quasi)-prometric (even if referred to only obliquely) that matters.

Any (quasi)-[[gauge space|gauge]] is a (quasi)-prometric base; similarly, given any (quasi)-[[pseudometric]] $d$, the [[singleton subset|singleton]] $\{d\}$ is a (quasi)-prometric base (and its generated (quasi)-gauge in turn generates the same (quasi)-prometric).  One might call a (quasi)-prometric (space) _simple_ if it is generated in this way by a (quasi)-pseudometric; this term is used analogously in the theory of [[syntopogenous spaces]], but the term _(quasi)-pseudometrizable_ is more likely to be understood.  (See [Subcategories](#subcategories) below.)


## Morphisms

A **[[short map]]** between (quasi)-prometric spaces $X$ and $Y$ is a function $f:X\to Y$ such that for every $d\in G_Y$, we have $d\circ (f\times f) \in G_X$.  We write $ProMet$ for the category of prometric spaces and short maps, and similarly $QProMet$ for the category of quasi-prometric spaces and short maps.

If the (quasi)-prometrics of $X$ and $Y$ are presented by bases, then this is equivalent to saying that for any basic distance function $d$ on $Y$, there is a basic $e$ on $X$ such that $d(f(x),f(x'))\le e(x,x')$ for all $x,x'\in X$.  Thus, for (quasi)-pseudometric spaces and (quasi)-gauge spaces considered as (quasi)-prometric spaces, this reduces to the usual notion of short map (i.e., distance-decreasing map).  Hence the category $Gau$ of gauge spaces and short maps is included as a full subcategory of $ProMet$, and similarly with $QGau$ in $QProMet$.


## Subcategories {#subcategories}

Since $Gau$ includes the categories of metric spaces and uniform spaces (disjointly), so does $ProMet$.  Likewise, since $QGau$ includes the category of topological spaces (disjointly from metric and uniform spaces), so does $QProMet$.

There is also another embedding of $Unif$ into $ProMet$, however, which is notably simpler than its embedding into $Gau$ (both easier to state and not using [[dependent choice]]).  Given a [[uniform space]] $X$, we define for each [[entourage]] $U\subseteq X\times X$ a distance function
$$
d_U(x,y) =
\begin{cases}
  0 & (x,y)\in U\\
  \infty & (x,y)\notin U.
\end{cases}
$$
(Again, this may be defined constructively as an infimum.)  The collection of such $d_U$ is a base for a prometric on $X$.  The short maps between such prometric spaces are precisely the uniformly continuous ones, so this defines another embedding of $Unif$ into $ProMet$.  The full image of this embedding consists precisely of those prometric spaces generated by a base of $\{0,\infty\}$-valued functions.  Note that replacing $\infty$ by any positive real number also defines an embedding of $Unif$ into $ProMet$, but a yet different one.

Conversely, every prometric induces a uniformity, where the entourages are the sets
$$ U_{d,\epsilon} = \{ (x,y) \;|\; d(x,y) \lt \epsilon \} .$$
In this way every short map induces a uniformly continuous map as well.  This operation is compatible with the above inclusions of $Unif$, as well as with the inclusion via $Gau$.


## Categorical interpretation {#proarrows}

As observed by Lawvere, an extended quasi-pseudo-metric space is a [[category enriched]] over the [[monoidal category]] $([0,\infty],\geq,+,0)$.  In other words, it is a monoid (or [[monad]]) in the [[bicategory]] $[0,\infty] Mat$ of [[matrices]] with values in this monoidal category.  Analogously, an extended quasi-prometric space is a monad in the bicategory $Pro [0,\infty] Mat$ whose hom-categories are the categories of [[pro-object]]s in the hom-categories of $[0,\infty] Mat$.

Note that if $Rel = \{0,1\} Mat$ denotes the bicategory of [[relation]]s in $Set$, then a monad in $Rel$ is a [[preorder]], while a monad in $Pro Rel$ is a quasi-[[uniform space]].

In all these cases, in order to recover the correct notion of morphism abstractly, we must consider monads in a [[double category]] or [[equipment]] rather than merely a bicategory.

[[!include generalized uniform structures - table]]


## References

* Maria Manuel Clementino, Dirk Hofmann, and Walter Tholen.  "One Setting for All: Metric, Topology, Uniformity, Approach Structure." ([pdf](http://www.math.yorku.ca/~tholen/ProMat_V_.pdf)) 


[[!redirects prometric]]
[[!redirects prometrics]]
[[!redirects prometric space]]
[[!redirects prometric spaces]]

[[!redirects quasiprometric]]
[[!redirects quasiprometrics]]
[[!redirects quasiprometric space]]
[[!redirects quasiprometric spaces]]

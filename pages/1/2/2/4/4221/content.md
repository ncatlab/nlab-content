## Idea

If a [[derivator]] is regarded as a "shadow" of an $(\infty,1)$-category, then an *enriched derivator* is an analogous shadow of an [[enriched category|enriched]] $(\infty,1)$-category.

## Definitions

There are several different things in which one could try to enrich a derivator.  It would be nice to be able to remain completely in the world of derivators by enriching a derivator over a [[monoidal derivator]].  However, it seems unlikely that the naive notion of monoidal derivator (a [[pseudomonoid]] in the 2-category of derivators) contains enough information to make this feasible, so we either have to augment that notion somehow, or enrich over something else.  At present, the latter is easier.

### Enrichment over a monoidal $(\infty,1)$-category

+--{: .standout}
The following is tentative.
=--

Let $V'$ be a bicomplete closed symmetric [[monoidal (∞,1)-category]], and let $V\subset V'$ be a [[reflective sub-(∞,1)-category]] which is a 1-category and which is closed under the monoidal structure and the [[internal-hom]].  For example:

* $V'=\infty Gpd$ with cartesian [[product]], $V=Set$.
* $V'= \infty Gpd_*$ (pointed $\infty$-groupoids) with [[smash product]], $V=Set_*$.

We can therefore talk about $V$-enriched categories.  Moreover, since $V$ is bicomplete and closed, the category $V$-$Cat$ is again closed symmetric monoidal, and hence enriched over itself.

+--{: .un_defn}
###### Definition
A **$(V,V')$-enriched prederivator** is a $V CAT$-enriched functor
$$ D\colon V Cat^{op} \to V CAT. $$
(or replacing $V Cat$ by some subcategory of it.)
=--

For instance, when $(V,V') = (Set, \infty Gpd)$ then this is precisely the ordinary notion of prederivator.  We include the additional data of $V$ in order that the definition of prederivator can remain a purely 1-categorical notion, without referring explicitly to any $(\infty,1)$-category.

We now need to specify the axioms which an enriched prederivator should satisfy to be called an enriched derivator.  Most of them are easy by analogy:

* **(Der1)** $D$ takes [[coproducts]] to [[products]].

* **(Der2)** If $1$ denotes the unit $V$-category, then for any $V$-category $A$ the family of functors $D(A) \to D(1)$ is jointly [[conservative functor|conservative]].

* **(Der3)** For any $V$-functor $u\colon A\to B$, the $V$-functor $u^*\colon D(B) \to D(A)$ has a left and a right adjoint $u_!$ and $u_*$.

* **(Der5)** For any object $x\in V$, let $I[x]$ denote the $x$-fattened [[interval category]], with two objects $0$ and $1$ and $hom(0,1)=x$.  Then for any $V$-category $A$, the induced functor $D(A\times I[x]) \to D(A)^{I[x]}$ is essentially surjective and full.

The last, and most important, axiom, involves a characterization of the appropriate [[homotopy exact squares]] of $V$-categories.  Here is finally where the larger $(\infty,1)$-category $V'$ enters the picture.  If $A$ is a $V$-category and $F\colon A\to V$ and $G\colon A^{op}\to V$ are $V$-functors, then we can take their [[tensor product]] $G\otimes_A F \in V$, but we can also regard them as landing in $V'$ and take their homotopy tensor product $G \otimes^h_A F \in V'$, and these will generally give different results.

* **(Der4)** Given any square
  $$ \array{ A & \overset{f}{\to} & B \\
   ^u\downarrow & & \downarrow ^v \\
   C & \underset{g}{\to} & D} $$
  of $V$-categories such that for any objects $c\in C$ and $b\in B$, the induced map
  $$ C(-,c) \otimes^h_A B(b,-) \to D(v(b),g(c)) $$
  is an equivalence in $V'$, then the induced transformation
  $$ u_! f^* \to g^* v_! $$
  (and hence also its mate $v^* g_* \to f_* u^*$) is an isomorphism.

This should be compared with the characterizations of [[exact squares]] for ordinary (enriched) category theory and of [[homotopy exact squares]].

### Enrichment over a monoidal homotopical category

Note that actually, we didn't really need $V'$ to be monoidal; we just need a place for a well-behaved homotopy tensor product of $V$-profunctors to live.

...

## Examples

* Cisinski's theorem characterizing [[homotopy exact squares]] shows that a $(Set, \infty Gpd)$-enriched derivator is exactly the same as an ordinary [[derivator]].  One has to observe that $C(-,c) \otimes^h_A B(b,-)$ can be constructed as a [[two-sided bar construction]], which in turn can be identified with the nerve of a particular category.

* Conjecturally, $(Set_*, \infty Gpd_*)$-enriched derivators are the same as [[pointed derivators]] in the usual sense.

* Also conjecturally, any $V'$-enriched $(\infty,1)$-category should have an underlying $(V,V')$-enriched derivator.

## Properties

Just as an ordinary derivator encodes a well-behaved notion of [[homotopy limits], an enriched derivator encodes a notion of homotopy [[weighted limit]].  In order to recover this, we need to represent [[profunctors]] by their [[cograph of a profunctor|collages]].

Specifically, let $H\colon A&#8696; B$ be a $V$-profunctor, and $A \overset{u}{\to} \bar{H} \overset{v}{\leftarrow} B$ its collage.  Then homotopy $H$-weighted limits in an enriched derivator are computed by the composite $v^* u_*$.

[[!redirects enriched derivators]]

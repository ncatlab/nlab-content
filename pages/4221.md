## Idea

If a [[derivator]] is regarded as a "shadow" of an $(\infty,1)$-category, then an *enriched derivator* is an analogous shadow of an [[enriched category|enriched]] $(\infty,1)$-category.

+--{: .query}
[[Peter LeFanu Lumsdaine]]: What does "enriched $(\infty,1)$-category" mean here? --- just one of the models for $(\infty,1)$-categories as (Top-, Kan-, SSet-)enriched categories, or actually some further idea of "$(\infty,1)$-category enriched in something"?  (The latter sounds an interesting idea, but I'm not quite sure how to imagine it!)

[[Mike Shulman]]: I had the latter in mind.  Just as a 1-category can be enriched over a monoidal 1-category, an $(\infty,1)$-category should be enrichable over a monoidal $(\infty,1)$-category.  The "default" enrichment will be over $\infty$-groupoids (which one could express in any particular model), just as the "default" enrichment for 1-categories is over sets.
=--

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

For instance, when $(V,V') = (Set, \infty Gpd)$ then this is precisely the ordinary notion of prederivator.  We define this by reference to $V$, rather than $V'$, in order that the definition of prederivator can remain a purely 1-categorical notion, without referring explicitly to any $(\infty,1)$-category.

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

A $(V,V')$-enriched prederivator satisfying (Der1)--(Der5) is called a **$(V,V')$-enriched derivator**.

### Enrichment over a monoidal homotopical category

Note that all we really needed of $V'$ was a place for a well-behaved homotopy tensor product of $V$-profunctors to live.  Thus, we could replace it by anything else sufficiently good, such as a [[monoidal model category]] or a [[closed monoidal homotopical category]].  In this case, the homotopy tensor product can be computed as a "homotopy coend" or more explicitly as a [[two-sided bar construction]].

Moreover, since the only dependence on $V'$ in the definition is via the homotopy tensor product of functors, the particular choice of model we make is essentially irrelevant for the resulting notion of derivator.  In other words, the true input for a notion of enriched derivator is an ordinary monoidal category $V$, together with "a homotopy theory in which $V$ is reflectively embedded."

## Examples

* When $(V,V') = (Set,\infty Gpd)$, all the axioms of an enriched derivator are identical to those of an ordinary [[derivator]], except for (Der4).  The usual axiom (Der4) asserts the conclusion only for [[comma squares]].  However, Cisinski's theorem characterizing [[homotopy exact squares]] shows that this implies the enriched version of (Der4) stated above (which is a priori stronger).  To make this comparison with the way Cisinski's theorem is usually stated, one has to observe that $C(-,c) \otimes^h_A B(b,-)$ can be constructed as a [[two-sided bar construction]], which in turn can (in this case) be identified with the nerve of a particular category.

* Conjecturally, $(Set_*, \infty Gpd_*)$-enriched derivators are the same as [[pointed derivators]] in the usual sense.

* Also conjecturally, any $V'$-enriched $(\infty,1)$-category should have an underlying $(V,V')$-enriched derivator.

## Properties

Just as an ordinary derivator encodes a well-behaved notion of [[homotopy limits]], an enriched derivator encodes a notion of homotopy [[weighted limit]].  In order to recover this, we need to represent [[profunctors]] by their [[cograph of a profunctor|collages]].

Specifically, let $H\colon A&#8696; B$ be a $V$-profunctor, and $A \overset{u}{\to} \bar{H} \overset{v}{\leftarrow} B$ its collage.  Then homotopy $H$-weighted limits in an enriched derivator are computed by the composite $v^* u_*$, and similarly $H$-weighted colimits are computed by $u^* v_!$.

Note that unlike in the ordinary unenriched case, it is not possible to compute all limits by Kan extending along functors to the terminal category.  This is because of the presence and importance of weighted limits.

### Homotopy Kan extensions are pointwise

Part of the intuition behind the usual axiom (Der4) is that it says that the homotopy Kan extensions which make up the structure of a derivator are all [[pointwise Kan extension|pointwise]].  For left Kan extensions along $u\colon A\to B$, pointwiseness means that each object $(Lan_u X)(b)$ is calculated as a suitable colimit, which in the unenriched case can be expressed as an ordinary colimit over the comma category $u/b$ -- hence why we assert that comma squares are exact.

In the enriched situation, the (co)limit involved in the notion of "pointwise Kan extension" is irreducibly a [[weighted limit]], and not constructible as a comma object.  However, the Kan extensions in an enriched derivator are still pointwise in a suitable sense; we can see this as follows.  Let $u\colon A\to B$ be a $V$-functor, let $b\in B$, let $B(u,b)\colon 1 &#8696; A$ denote the representable profunctor, and let $H$ be its collage.  Then the square
$$\array{ A & \to & A \\
\downarrow & & \downarrow^u\\
H & \to & B } $$
satisfies the hypothesis of the enriched (Der4).  (This is just the homotopical version of [[Yoneda reduction]]: $B(u,b) \otimes_A^h A \simeq B(u,b)$.)  Therefore, if we left extend along $u$, then restrict to $H$ and further restrict to $b$, we get the same thing as if we just extended to $H$ and restricted to $b$ --- but the latter is exactly the process of taking the $B(u,b)$-weighted colimit.  Thus, the evaluation of $u_! X$ at $b$ is computed as a weighted colimit, and hence the Kan extension is "pointwise."

[[!redirects enriched derivators]]

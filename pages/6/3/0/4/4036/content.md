
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Topos theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition


+-- {: .num_defn #GoodOpenCover }
###### Definition

A [[cover]] $\{U_i \to X\}$ of a [[topological space]] $X$ is called a **good cover** -- or **good open cover** if it is

1. an [[open cover]];

1. such that all the $U_i$ and all their inhabited finite intersections are [[contractible topological spaces]].

=--

+-- {: .num_remark }
###### Remark


For $X$ a [[topological manifold]] one often requires that the inhabited finite intersections are [[homeomorphism|homeomorphic]] to an [[open ball]]. Similarly, for $X$ a [[smooth manifold]] one often requires that the finite inhabited intersections are [[diffeomorphism|diffeomorphic]] to an [[open ball]].

In the literature this is traditionally glossed over, but this is in fact a subtle point, see the discussion at [[open ball]] and see below at _[Existence on paracompact smooth manifolds](#ExistenceOnParacompactManifolds)_. 

=--

Due to this subtly, it is instructive to make explicit the following definition:

+-- {: .num_defn #DifferentiablyGoodOpenCover}
###### Definition

Given a [[smooth manifold]] $X$ a _differentiably good open cover_ is a good open cover one all whose finite non-empty intersections are in fact [[diffeomorphism|diffeomorphic]] to an [[open ball]], hence to a [[Cartesian space]].

=--


## Properties {#Properties}
 
### Existence on paracompact smooth manifolds
 {#ExistenceOnParacompactManifolds}

+-- {: .num_prop }
###### Proposition

Every [[paracompact manifold|paracompact]] [[smooth manifold]] admits a good open cover, def.&#160;\ref{GoodOpenCover}, in fact
a differentiable good open cover, def.&#160;\ref{DifferentiablyGoodOpenCover}

=--

+-- {: .proof}
###### Proof

Every [[paracompact manifold|paracompact]] [[smooth manifold]] admits a [[Riemannian metric]], and for any point in a [[Riemannian manifold]] there is a [[geodesically convex]] [[neighborhood]] (any two points in the neighborhood are connected by a unique geodesic in the neighborhood, one whose length is the distance between the points; see for example the remark after lemma 10.3 ([Milnor](#Milnor)) page 59, or ([do Carmo](#doCarmo)), Proposition 4.2).
A nonempty intersection of finitely many such geodesically convex neighborhoods is also geodesically convex.
The inverse of the exponential map based at any
interior point of a geodesically convex open subset
gives a diffeomorphism from this subset to a star-shaped
open subset of $\mathbf{R}^n$.
Indeed, the [[Gauss lemma]] shows that the tangent
map of the exponential map is invertible.
By definition of geodesic convexity the exponential
map is injective, hence a diffeomorphism.
As proved in [[ball]], star-shaped open subsets
of $\mathbf{R}^n$ are diffeomorphic to $\mathbf{R}^n$,
which completes the proof.

=--

+-- {: .num_remark }
###### Remark

It is apparently a folk theorem that every [[geodesic convexity|geodesically convex]] [[open neighbourhood]] in a Riemannian manifold is [[diffeomorphic]] to a [[Cartesian space]].
For instance, this is asserted in the proof of Theorem&#160;5.1 of ([BottTu](#BottTu)), which
claims the existence of differentiable good open covers.
But a complete proof in the literature is hard to find.
See also the discussion of the references at [[ball]].
=--

+-- {: .num_prop }
###### Proposition

Every [[smooth manifold|smooth]] [[paracompact manifold]] of [[dimension]] $d$ admits a differentiably good open cover, def. \ref{DifferentiablyGoodOpenCover}, hence an open cover such that every non-empty finite intersection is [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^d$.

=--


+-- {: .proof}
###### Proof

By ([Greene](#Greene)) every paracompact smooth manifold admits a [[Riemannian metric]] with positive [[convexity radius]] $r_{\mathrm{conv}} \in \mathbb{R}$. Choose such a metric and choose an [[open cover]] consisting for each point $p\in X$ of the geodesically convex open subset $U_p := B_p(r_{conv})$ given by the geodesic $r_{conv}$-ball at $p$. Since the [[injectivity radius]] of any metric is at least $2r_{\mathrm{conv}}$ it follows from the minimality of the geodesics in a geodesically convex region that inside every finite nonempty intersection $U_{p_1} \cap \cdots \cap U_{p_n}$ the [[geodesic flow]] around any point $u$ is of radius less than or equal the injectivity radius and is therefore a diffeomorphism onto its image. 

Moreover, the [[preimage]] of the intersection region under the geometric flow is a [[star-shaped]] region in the [[tangent space]] $T_u X$: because the intersection of geodesically convex regions is itself geodesically convex, so that for any $v \in T_u X$ with $\exp(v) \in U_{p_1} \cap \cdots \cap U_{p_n}$ the whole geodesic segment $t \mapsto \exp(t v)$ for $t \in [0,1]$ is also in the region.

So we have that every finite non-empty intersection of the $U_p$ is diffeomorphic to a star-shaped region in a vector space. By the results cited at [[ball]] (e.g. theorem 237 of ([Ferus](#Ferus))) this star-shaped region is diffeomorphic to an $\mathbb{R}^n$.

=--

### Coverages of good open covers

+-- {: .num_cor }
###### Corollary

The [[category]] $ParaSmMfd$ of paracompact smooth manifolds admits a [[coverage]] whose covering families are good open covers.

The same holds true for [[subcategories]] such as

* [[CartSp]] -- [[Cartesian spaces]].


=--

+-- {: .proof}
###### Proof

It is sufficient to check this in $ParaSmMfd$.
We need to check that for $\{U_i \to U\}$ a good open cover and $f : V \to U$ any morphism, we get commuting squares

$$  
  \array{  
     V_j &\to& U_{i(j)}
     \\
     \downarrow && \downarrow
     \\
     V &\stackrel{f}{\to}& U
  }
$$

such that the $\{V_i \to V\}$ form a good open cover of $V$. 

Now, while $ParaSmMfd$ does not have all [[pullbacks]], the pullback  of an [[open cover]] does exist, and since $f$ is necessarily a [[continuous function]] this is an [[open cover]] $\{f^* U_i \to V\}$. The $f^* U_i$ need not be contractible, but being open subsets of a paracompact manifold, they are themselves paracompact manifolds and hence admit themselves good open covers $\{W_{i,j} \to f^* U_i\}$.

Then the family of composites $\{W_{i,j} \to f^* U_i \to V\}$ is clearly a good open cover of $V$.



=--


### Existence on CW complexes 

+-- {: .num_prop }
###### Proposition

Every [[CW complex]] admits a good open cover. 

=--


+-- {: .proof}
###### Proof

It suffices to prove that if $X$ admits a good open cover and $\phi: S^n \to X$ is an attaching map, then the [[pushout]]
 
$$\array{
S^n & \stackrel{\phi}{\to} & X \\
i \downarrow & & \downarrow \\
D^{n+1} & \to & Y
}$$ 

also admits a good open cover. Let $\{U_\alpha\}$ be a good open cover of $X$ closed under nonempty finite intersections, and choose a contracting [[homotopy]] $h_\alpha: I \times U_\alpha \to U_\alpha$ such that $h_\alpha(0, -) = id$ and $h_\alpha(1, -)$ is constant. For any subset $S \subseteq D^{n+1}$, let $Hull(S)$ denote the [[convex hull]] of $S$ in $D^{n+1}$. If $V$ is relatively open in the boundary $S^n$, we can choose for each $x \in V$ a small open neighborhood $V_x \subseteq Hull(V)$ of $x$ such that $y \in V_x$ implies $t y \in V_x$ whenever $1 \leq t \leq 1/{|y|}$; having made such choices, put $H(V) \coloneqq (\bigcup_{x \in V} V_x) \cap \{z \in D^{n+1}: {|z|} \gt 1/2\}$. Now the image in $Y$ of 

$$V_\alpha \coloneqq U_\alpha \cup H(\phi^{-1}(U_\alpha)) \subseteq X \cup D^{n+1}$$ 

is open in $Y$, and it is contractible: define a contracting homotopy 
$$H_\alpha: I \times V_\alpha \to V_\alpha$$ 

by 

$$
H_\alpha(t, v) = \left\{ 

\array{
(1 - 2t)v + 2t \frac{v}{|v|} & 0 \leq t \lt \frac1{2}, v \in int(D^{n+1}) \cap V_\alpha \\

v & 0 \leq t \leq \frac1{2}, v \in U_\alpha \\

h_\alpha(2t - 1, \phi(\frac{v}{|v|})) & \frac1{2} \leq t \leq 1, v \in int(D^{n+1}) \cap V_\alpha \\

h_\alpha(2t - 1, v) & \frac1{2} \leq t \leq 1, v \in U_\alpha
} \right.
$$

These sets $V_\alpha$ together with $int(D^{n+1})$ form a good open cover of $Y$. 

=--

### (Non-)Existence for topological manifolds

For a (paracompact) [[topological manifold]] the construction via [[Riemannian metrics]] or similar smooth constructions in general does not work. 

In ([Osborne-Stern 69](#OsborneStern69)) the following discussion for sufficient conditions getting "close" to good open covers is discussed:

Let $X$ be a [[n-connected space|k-connected]] [[topological manifold]] of [[dimension]] $n$ (without [[boundary]]), and define 

$$
  q \coloneqq
  min(k,n-3)
  \,.
$$ 

For $p \in \mathbb{N}$ such that $p(q+1) \gt n$ then $X$ admits a cover by $p$ open balls and such that all nonempty intersections of the covering cells are [[n-connected space|(q−1)-connected]].


### Refining covers

A cover $\{U_i\to X\}_{i\in I}$ refines another cover $\{V_j\to X\}_{j\in J}$ if each map $V_j\to X$ is some $U_i\to X$.

Each differentially good cover has a unique smallest refinement to a differentially good cover that is closed under intersection.

## $n$POV

The following [[nPOV]] perspective on good open covers gives a useful general "explanation" for their relevance, which also explains the role of good covers in [[Cech cohomology]] generally and [[abelian sheaf cohomology]]  in particular.

+-- {: .num_prop}
###### Proposition

Let $sPSh(CartSp)_{proj}$ be the category of [[simplicial presheaves]] on the category [[CartSp]] equipped with the projective [[model structure on simplicial presheaves]].

Let $X$ be a [[smooth manifold]], regarded as a 0-[[truncated]] object of $sPSh(C)$.

Let $\{U_i \to X\}$ be a good open cover by [[open ball]]s in the strong sense: such that every finite non-empty intersection is diffeomorphic to an $\mathbb{R}^d$.

Then: the [[Cech nerve]] $C(\{U\}) \in sPSh(C)$ is a cofibrant resolution of $X$ in the [[local model structure on simplicial presheaves]].

=--

+-- {: .proof}
###### Proof

By assumption we have that $C(U)$ is degreewise a [[coproduct]] of [[representable functor|representables]]. It is also evidently a [[split hypercover]].

This implies the statement by the [characterization of cofibrant objects in the projective structure](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects).


=--

This has a useful application in the [[nerve theorem]].

Notice that the [[descent]] condition for simplicial presheaves on [[CartSp]] at (good) covers is very weak, since all [[Cartesian space]]s are topologically contractible, so it is easy to find the fibrant objects $A \in sPSh(C)_{proj, loc}$ in the [[topological localization]] of $sPSh(C)_{proj}$ for the canonical [[coverage]] of [[CartSp]]. The above observation says that for computing the $A$-valued [[cohomology]] of a [[diffeological space]] $X$, it is sufficient to evaluate $A$ on (the Cech nerve of) a good cover of $X$.


We can turn this around and speak for any [[site]] $C$ of a covering family $\{U_i \to X\}$ as being _good_ if the corresponding [[Cech nerve]] is degreewise a coproduct of representables. In the projective model structure on simplicial presheaves on $C$ such good covers will enjoy the central properties of good covers of topological spaces.

## Related concepts

* [good covers by Stein manifolds](Stein+manifold#GoodCoversBySteinManifolds) - note that this is a different concept, with vanishing Dolbeault cohomology replacing contractibility.

## References

* {#doCarmo} [[Manfredo do Carmo]], _Riemannian geometry_ (trans. Francis Flaherty), Birkh&#228;user (1992) 

* {#Milnor} [[John Milnor]], _Morse theory_ , Princeton University Press (1963)

* {#Greene} R. Greene, _Complete metrics of bounded curvature on noncompact manifolds_  Archiv der Mathematik Volume 31, Number 1 (1978)


* {#Ferus} [[Dirk Ferus]], _Analysis III_ ([pdf](http://www.math.tu-berlin.de/~ferus/ANA/Ana3.pdf))


* {#BottTu} [[Raoul Bott]],  [[Loring Tu]], _Differential forms in algebraic topology_, Graduate texts in mathematics vol. 82 (1982)  ([pdf](http://www.maths.ed.ac.uk/~aar/papers/botttu.pdf))

* {#OsborneStern69} RP Osborne and JL Stern. _Covering Manifolds with Cells_, Pacific Journal of Mathematics, Vol 30, No. 1, 1969.

* MathOverflow, _[Proving the existence of good covers](http://mathoverflow.net/q/102161/381)_

[[!redirects good cover]]
[[!redirects good covers]]
[[!redirects good open covers]]

[[!redirects good covering]]
[[!redirects good coverings]]

[[!redirects differentiably good open cover]]
[[!redirects differentiably good open covers]]
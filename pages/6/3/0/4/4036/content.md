
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
* automatic table of contents goes here
{:toc}


## Definition

A [[cover]] $\{U_i \to X\}$ of a [[topological space]] or [[smooth manifold]] $X$ is called a **good cover** -- or **good open cover** if it is

1. an [[open cover]]

1. such that all the $U_i$ and all their nonempty finite intersections are [[contractible]].




## Properties {#Properties}
 
+-- {: .un_prop }
###### Proposition

Every [[paracompact manifold]] admits a good open cover.

=--

+-- {: .proof}
###### Proof

Every paracompact manifold admits a [[Riemannian metric]], and for any point in a [[Riemannian manifold]] there is a [[geodesically convex]] [[neighborhood]] (any two points in the neighborhood are connected by a unique geodesic in the neighborhood, one whose length is the distance between the points; see for example the remark after lemma 10.3 ([Milnor](#Milnor)) page 59). It is immediate that a nonempty intersection of finitely many such geodesically convex neighborhoods is also geodesically convex, hence contractible. 

=--

+-- {: .un_remark }
###### Remark

It is apparently a folk theorem that every geodesically convex neighbourhood in a Riemannian manfifold is [[diffeomorphic]] to a [[Cartesian space]] (for instance this is asserted on page 42 of ([BottTu](#BottTu)). This implies the following strengthening of the above result, which appears stated as theorem 5.1  in [BottTu](#BottTu). But a complete proof in the literature is hard to find (see also the discussion of the references at [[ball]]). We give a complete proof below.

=--

+-- {: .un_prop }
###### Proposition

Every [[paracompact manifold]] of [[dimension]] $d$ admits an open cover such that every non-empty finite intersection is [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^d$.

=--


+-- {: .proof}
###### Proof

By ([Greene](#Greene)) every paracompact manifold admits a Riemannian metric with positive [[convexity radius]] $r_{\mathrm{conv}} \in \mathbb{R}$. Choose such a metric and choose an open cover consisting for each point $p\in X$ of the geodesically convex open subset $U_p := B_p(r_{conv})$ given by the geodesic $r_{conv}$-ball at $p$. Since the [[injectivity radius]] of any metric is at least $2r_{\mathrm{conv}}$ it follows from the minimality of the geodesics in a geodesically convex region that inside every finite nonempty intersection $U_{p_1} \cap \cdots \cap U_{p_n}$ the [[geodesic flow]] around any point $u$ is of radius less than or equal the injectivity radius and is therefore a diffeomorphism onto its image. 

Moreover, the preimage of the intersection region under the geometric flow is a [[star-shaped]] region in the tangent space $T_u X$: because the intersection of geodesically convex regions is itself geodesically convex, so that for any $v \in T_u X$ with $\exp(v) \in U_{p_1} \cap \cdots \cap U_{p_n}$ the whole geodesic segment $t \mapsto \exp(t v)$ for $t \in [0,1]$ is also in the region.

So we have that every finite non-empty intersection of the $U_p$ is diffeomorphic to a star-shaped region in a vector space. By the results cited at [[ball]] (e.g. theorem 237 of ([Ferus](#Ferus))) this star-shaped region is diffeomorphic to an $\mathbb{R}^n$.

=--

+-- {: .un_cor }
###### Corollary

The [[category]] $Para$ paracompact manifolds admits a [[coverage]] whose covering families are good open covers.

The same holds true for [[subcategories]] such as

* [[Diff]] -- paracompact [[smooth manifold]]s;

* [[CartSp]] -- [[Cartesian space]]s.


=--

+-- {: .proof}
###### Proof

It is suficcient to check this in $Para$.
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

Now, while $Para$ does not have all [[pullback]]s, the pullback  of an [[open cover]] does exist, and since $f$ is necessarily a [[continuous function]] this is an [[open cover]] $\{f^* U_i \to V\}$. The $f^* U_i$ need not be contractible, but being open subsets of a paracompact manifold, they are themselves paracompact manifolds and hence admit themselves good open covers $\{W_{i,j} \to f^* U_i\}$.

Then the family of composites $\{W_{i,j} \to f^* U_i \to V\}$ is clearly a good open cover of $V$.



=--


+-- {: .un_prop }
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

also admits a good open cover. Let $\{U_\alpha\}$ be a good open cover of $X$ closed under nonempty finite intersections, and choose a contracting [[homotopy]] $h_\alpha: I \times U_\alpha \to U_\alpha$ such that $h_\alpha(0, -) = id$ and $h_\alpha(1, -)$ is constant. For any subset $S \subseteq D^{n+1}$, let $Hull(S)$ denote the [[convex hull]] of $S$. Then, if $V$ is relatively open in the boundary $S^n$, $Hull(V)$ is open in $D^{n+1}$. It follows that the image in $Y$ of 

$$V_\alpha \coloneqq U_\alpha \cup Hull(\phi^{-1}(U_\alpha)) \subseteq X \cup D^{n+1}$$ 

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


## $n$POV

The following [[nPOV]] perspective on good open covers gives a useful general "explanation" for their relevance, which also explains the role of good covers in [[Cech cohomology]] generally and [[abelian sheaf cohomology]]  in particular.

+-- {: .un_prop}
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


## References

* [[John Milnor]], _Morse theory_ , Princeton University Press (1963)
{#Milnor}

* R. Greene, _Complete metrics of bounded curvature on noncompact manifolds_  Archiv der Mathematik Volume 31, Number 1 (1978)
{#Greene}

* [[Dirk Ferus]], _Analysis III_ ([pdf](http://www.math.tu-berlin.de/~ferus/ANA/Ana3.pdf))
{#Ferus}


* [[Raoul Bott]] [[Loring Tu]], _Differential forms in algebraic topology_ 
{#BottTu}

[[!redirects good cover]]
[[!redirects good covers]]
[[!redirects good open covers]]
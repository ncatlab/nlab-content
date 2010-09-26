
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

Every [[paracompact space|paracompact]] [[manifold]] admits a good open cover.

=--

+-- {: .proof}
###### Proof

Every paracompact manifold admits a [[Riemannian metric]], and for any point in a [[Riemannian manifold]] there is a geodesically convex neighborhood (any two points in the neighborhood are connected by a geodesic in the neighborhood; see for example the remark after lemma 10.3 in Milnor's _Morse Theory_ , page 59). Provided that the neighborhoods are chosen small enough to guarantee that any two points within a neighborhood are joined by a
unique geodesic which is also minimal in the manifold, it is immediate that a nonempty intersection of finitely many such geodesically convex neighborhoods is also geodesically convex, hence contractible. 

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

Let $X$ be a [[manifold]], or more generally a [[diffeological space]], regarded as a 0-[[truncated]] object of $sPSh(C)$.

Then: the [[Cech nerve]] $C(\{U_i\}) \in sPSh(C)$ of a good open cover $\{U_i \to X\}$ is cofibrant in $X$.

=--

+-- {: .proof}
###### Proof

This is a special case of the [characterization of cofibrant objects in the projective structure](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects): the point is that the fact that the cover is _good_ means that the Cech nerve $C(\{U_i\})$ is degreewise a [[coproduct]] of [[representable functor|representables]]: every open contractible subset is isomorphic to an open ball, hence to an object in the site [[CartSp]].

=--

This has a useful application in the [[nerve theorem]].

Notice that the [[descent]] condition for simplicial presheaves on [[CartSp]] at (good) covers is very weak, since all [[Cartesian space]]s are topologically contractible, so it is easy to find the fibrant objects $A \in sPSh(C)_{proj, loc}$ in the [[topological localization]] of $sPSh(C)_{proj}$ for the canonical [[coverage]] of [[CartSp]]. The above observation says that for computing the $A$-valued [[cohomology]] of a [[diffeological space]] $X$, it is sufficient to evaluate $A$ on (the Cech nerve of) a good cover of $X$.


We can turn this around and speak for any [[site]] $C$ of a covering family $\{U_i \to X\}$ as being _good_ if the corresponding [[Cech nerve]] is degreewise a coproduct of representables. In the projective model structure on simplicial presheaves on $C$ such good covers will enjoy the central properties of good covers of topological spaces.


[[!redirects good cover]]
[[!redirects good covers]]
[[!redirects good open covers]]

<div class="rightHandSide toc">
[[!include topology - contents]]
***
[[!include topos theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Definition

A [[cover]] $\{U_i \to X\}$ of a [[topological space]] or [[smooth manifold]] $X$ is called a **good cover** -- or **good open cover** if it is

1. an [[open cover]]

1. such that all the $U_i$ and all their nonempty finite intersections are [[contractible]].




## Properties {#Properties}

Every [[paracompact space|paracompact]] [[manifold]] should admit a good open cover.

Because every paracompact manifold admits a [[Riemannian metric]], and for any point in a [[Riemannian manifold]] there is a geodesically convex neighborhood (any two points in the neighborhood are connected by a geodesic in the neighborhood; see for example the remark after lemma 10.3 in Milnor's _Morse Theory_ , page 59). Provided that the neighborhoods are chosen small enough to guarantee uniqueness of the geodesic, it is immediate that a nonempty intersection of finitely many such geodesically convex neighborhoods is also geodesically convex, hence contractible. 


### $n$POV

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
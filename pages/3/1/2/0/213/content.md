
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

+-- {: .num_defn}
###### Definition

Write $CartSp$ for the [[category]] whose 

* [[objects]] are [[Cartesian space]]s $\mathbb{R}^n$ for $n \in \mathbb{N}$;

* [[morphisms]] are suitable structure-preserving [[functions]] between these spaces. 

For definiteness we write

$CartSp_{lin}$ for the category whose objects are [[Cartesian space]]s regarded as [[real number|real]] [[vector spaces]] and whose morphisms are [[linear function]]s between these;

* $CartSp_{top}$ for the category whose objects are Cartesian spaces regarded as [[topological spaces]] equipped with their [[Euclidean topology]] and morphisms are [[continuous maps]] between them.

* $CartSp_{smth}$ for the category whose objects are Cartesian spaces regarded as [[smooth manifolds]] with their standard [[smooth structure]] and morphisms are [[smooth function]]s.

=--


## Properties

### As a small category of objects with a basis

A [[Cartesian space]] carries a lot of structure, for instance [[CartSp]] may be naturally regarded as a [[full subcategory]] of the category $C$, for $C$ (any one of) the category of

*  [[vector spaces]],
*  [[affine spaces]],
*  [[normed vector spaces]],
*  [[inner product spaces]],
*  [[Euclidean spaces]].

In all these cases, the inclusion $CartSp \hookrightarrow C$ is an [[equivalence of categories]]: choosing an [[isomorphism]] from any of these objects to a [[Cartesian space]] amounts to choosing a [[basis]] of a [[vector space]], a [[coordinate system]].

### As a site

+-- {: .num_defn}
###### Definition

Write

* [[CartSp]]${}_{top}$ for the category whose [[object]]s are Cartesian spaces and whose [[morphism]]s are all [[continuous maps]] between these.

* [[CartSp]]${}_{smooth}$ for the category whose [[object]]s are Cartesian spaces and whose [[morphism]]s are all [[smooth f# Refefunctions]] between these.

* [[CartSp]]${}_{synthdiff}$ for the [[full subcategory]] of the category of [[smooth loci]] on those of the form $\mathbb{R}^n \times D$ for $D$ an [[infinitesimal space]] (the formal dual of a Weil algebra).

=--

+-- {: .num_prop}
###### Proposition

In all three cases there is the [[good open cover]] [[coverage]] that makes [[CartSp]] a [[site]].

=--

+-- {: .proof}
###### Proof

For [[CartSp]]${}_{top}$ this is obvious. For [[CartSp]]${}_{smooth}$ this is somewhat more subtle. It is a folk theorem (see the references at [[open ball]]). A detailed proof is at [[good open cover]]. This directly carries over to $CartSp_{synthdiff}$.

=--

+-- {: .num_prop #AsDenseSubsite}
###### Proposition

* The site $CartSp_{top}$ is a [[dense subsite]] of the site of [[paracompact topological space|paracompact]] [[topological manifold]]s with the [[open cover]] [[coverage]].

* The site $CartSp_{smooth}$ is a [[dense subsite]] of the [[site]] [[Diff]] of [[paracompact topological space|paracompact]] [[smooth manifold]]s equipped with the [[open cover]] [[coverage]].

=--

+-- {: .num_prop}
###### Proposition

Equipped with this structure of a site, [[CartSp]] is an 
[[∞-cohesive site]].

=--

The corresponding [[cohesive topos]] [[sheaf topos|of sheaves]] is

* $Sh_{(1,1)}(CartSp_{smooth})$, discussed at [[diffeological space]].

* $Sh_{(1,1)}(CartSp_{synthdiff})$, discussed at [[Cahiers topos]].

The corresponding [[cohesive (∞,1)-topos]] [[(∞,1)-category of (∞,1)-sheaves|of (∞,1)-sheaves]] is

* $Sh_{(\infty,1)}(CartSp_{top}) =$ [[ETop∞Grpd]];

* $Sh_{(\infty,1)}(CartSp_{smooth}) =$ [[Smooth∞Grpd]];

* $Sh_{(\infty,1)}(CartSp_{synthdiff}) =$ [[SynthDiff∞Grpd]];

+-- {: .num_cor}
###### Corollary

We have [[equivalences of categories]]

* $Sh(CartSp_{top}) \simeq Sh(TopMfd)$

* $Sh(CartSp_{smooth}) \simeq Sh(Diff)$

and [[equivalences of (∞,1)-categories]]

* $Sh_{(\infty,1)}(CartSp_{top}) \simeq Sh_{(\infty,1)}(TopMfd)$;

* $Sh_{(\infty,1)}(CartSp_{smooth}) \simeq Sh_{(\infty,1)}(Diff)$.

=--

+-- {: .proof}
###### Proof

The first two statements follow by the [above proposition](#AsDenseSubsite) with the _comparison lemma_ discussed at [[dense sub-site]].

For the second condition notice that since an [[∞-cohesive site]] is in particular an [[∞-local site]] we have that $Sh_{(\infty,1)}(CartSp)$ is a [[local (∞,1)-topos]]. As discussed there, this implies that it is a [[hypercomplete (∞,1)-topos]]. By the discussion at [[model structure on simplicial presheaves]] this means that it is [[presentable (∞,1)-category|presented]] by the Joyal-Jardine-[[model structure on simplicial sheaves]] $Sh(CartSp)^{\Delta^{op}}_{loc}$. The claim then follows with the first two statements.

=--

### As a category with open maps

There is a canonical structure of a category with [[open map]]s on $CartSp$ (...)


### As an algebraic theory

The category $CartSp$ is (the [[syntactic category]] of ) a [[Lawvere theory]]: the theory for [[smooth algebra]]s.


### As a pre-geometry

Equipped with the above [[coverage]]-structure,  [[open map]]-structure and [[Lawvere theory]]-property, $CartSp$ is essentially a [[pregeometry (for structured (∞,1)-toposes)]].

(Except that the pullback stability of the open maps holds only in the weaker sense of [[coverage]]s).

(...)

$\,$

## Related concepts

[[!include geometries of physics -- table]]

$\,$

## References 
 {#References}

$CartSp_{smth}$ as an example of a "cartesian [[differential category]]":

* [[R. Blute]], [[J.R.B. Cockett]], [[Robert Seely]], section 2 of _Cartesian differential categories_, Theory and Applications of Categories **22** 23 (2009) 622-672 &lbrack;[tac:22-23](http://www.tac.mta.ca/tac/volumes/22/23/22-23abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/22/23/22-23.pdf)&rbrack;

{#CartSpAsSiteReference} $CartSp_{smth}$ as a convenient [[site]] for [[diffeological spaces]], [[smooth sets]], [[smooth groupoids]], ... [[smooth infinity-groupoids|smooth $\infty$-groupoids]] (and the term "CartSp", or similar, for it) was first considered in:

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], p. 22 in: *[[schreiber:Twisted Differential String and Fivebrane Structures]]*, Communications in Mathematical Physics **315** 1 (2012) 169-213 &lbrack;[arXiv:0910.4001](http://arxiv.org/abs/0910.4001), [doi:10.1007/s00220-012-1510-3](https://doi.org/10.1007/s00220-012-1510-3)&rbrack;

* [[Urs Schreiber]], [[Zoran Škoda]], [§6.2](https://arxiv.org/pdf/1004.2472.pdf#page=15) of: *Categorified symmetries* &lbrack;[arXiv:1004.2472](https://arxiv.org/abs/1004.2472)&rbrack;


* {#FSS12} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], Appendix of: _[[schreiber:Cech cocycles for differential characteristic classes|Čech cocycles for differential characteristic classes]]_, Advances in Theoretical and Mathematical Physics, **16** 1 (2012) 149-250 &lbrack;[arXiv:1011.4735](https://arxiv.org/abs/1011.4735), [doi:10.1007/BF02104916](https://doi.org/10.1007/BF02104916)&rbrack;

* [[Urs Schreiber]], §3.2.1 & §4.4 in: *[[schreiber:differential cohomology in a cohesive topos]]* &lbrack;[arXiv:1310.7930](https://arxiv.org/abs/1310.7930)&rbrack;


following the [[site]] [[ThCartSp|$CartSp_{synthdiff}$]] of [[formal smooth manifold|infinitesimally thickened]] Cartesian spaces, previously claimed (then without proof, it seems) to be a site for the [[Cahiers topos]] in:

* [[Anders Kock]], Section 5 of: *Convenient vector spaces embed into the Cahiers topos*, Cahiers de Topologie et Géométrie Différentielle Catégoriques **27** 1 (1986) 3-17  &lbrack;[numdam:CTGDC_1986__27_1_3_0](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0)&rbrack;

* {#KockReyes} [[Anders Kock]], [[Gonzalo Reyes]], _Corrigendum and addenda to: Convenient vector spaces embed into the Cahiers topos_, [[Cahiers|Cahiers de Topologie et Géométrie Différentielle Catégoriques]], **28** 2 (1987)  99-110 &lbrack;[numdam:CTGDC_1987__28_2_99_0](http://www.numdam.org/item?id=CTGDC_1987__28_2_99_0)&rbrack;


The idea is also implicit in

* [[Denis-Charles Cisinski]], Exp. 6.1.2 in: *Faisceaux localement asph&eacute;riques* (2003) &lbrack;[pdf](https://cisinski.app.uni-regensburg.de/mtest2.pdf), [[Cisinski-FaisceauxLocAsph.pdf:file]]&rbrack;


With an eye towards [[Frölicher spaces]], $CartSp_{synthdiff}$ also briefly appears in:

* Hirokazu Nishimura, Section 5 of: _Microlinearity in Frölicher -- Beyond the Regnant Philosophy of Manifolds_ &lbrack;[arXiv:0912.0827](http://arxiv.org/abs/0912.0827)&rbrack;


category: category

[[!redirects Cart]]
[[!redirects site of cartesian spaces]]
[[!redirects sites of cartesian spaces]]
[[!redirects site of cartesian manifolds]]
[[!redirects sites of cartesian manifolds]]

[[!redirects CartSp]]
[[!redirects Cart Sp]]

[[!redirects CartesianSpace]]
[[!redirects CartesianSpaces]]



[[!redirects SmoothCartSp]]





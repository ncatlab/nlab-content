
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

* [[object]]s are [[Cartesian space]]s $\mathbb{R}^n$ for $n \in \mathbb{N}$;

* [[morphisms]] are suitable structure-preserving [[function]]s between these spaces. 

For definiteness we write

$CartSp_{lin}$ for the category whose objects are [[Cartesian space]]s regarded as [[real number|real]] [[vector space]]s and whose morphisms are [[linear function]]s between these;

* $CartSp_{top}$ for the category whose objects are Cartesian spaces regarded as [[topological spaces]] equipped with their [[Euclidean topology]] and morphisms are [[continuous maps]] between them.

* $CartSp_{smooth}$ for the category whose objects are Cartesian spaces regarded as [[smooth manifolds]] with their standard [[smooth structure]] and morphisms are [[smooth function]]s.

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

* [[CartSp]]${}_{smooth}$ for the category whose [[object]]s are Cartesian spaces and whose [[morphism]]s are all [[smooth functions]] between these.

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



## Related concepts

A development of [[differential geometry]] as as geometry modeled on $CartSp$ is discussed, with an eye towards applications in [[physics]], in _[[geometry of physics]]_.

The [[sheaf topos]] over $CartSp_{smooth}$ is that of _[[smooth spaces]]_. 

The [[(∞,1)-sheaf (∞,1)-topos]] over $CartSp_{top}$ is discussed at _[[ETop∞Grpd]]_, that over $CartSp_{smooth}$ at _[[Smooth∞Grpd]]_, and that over $CartSp_{synthdiff}$ at _[[SynthDiff∞Grpd]]_.

The generalization of $CartSp$ to [[formal smooth manifolds]] is _[[FormalCartSp]]_.

## References 
 {#References}

In secton 2 of 

* [[R. Blute]], [[J.R.B. Cockett]], [[Robert Seely]], _Cartesian differential categories_, Theory and Applications of Categories, Vol. 22, 2009, No. 23, pp 622-672. ([journal](http://www.tac.mta.ca/tac/volumes/22/23/22-23abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/22/23/22-23.pdf))

$CartSp$ is discussed as an example of a "cartesian differential category".

There are various slight variations of the category $CartSp$ (many of them [[equivalence of categories|equivalent]]) that one can consider without changing its basic properties as a category of test spaces for [[generalized smooth spaces]]. A different choice that enjoys some popularity in the literature is the category of open (contractible) subsets of Euclidean spaces. For more references on this see [[diffeological space]].

The [[site]] $CartSp_{synthdiff}$ of [[formal smooth manifold|infinitesimally thickened]] Cartesian spaces is known as the site for the [[Cahiers topos]]. It is considered in detail in section 5 of

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0))

and briefly mentioned in example 2) on p. 191 of

* [[Anders Kock]], _Synthetic differential geometry_ ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

following the original article

* [[Eduardo Dubuc]], _Sur les modeles de la geometrie differentielle synthetique_ ([numdam](http://www.numdam.org/item?id=CTGDC_1979__20_3_231_0)).

With an eye towards [[Frölicher space]]s the site is also considered in section 5 of 

* Hirokazu Nishimura, _Beyond the Regnant Philosophy of Manifolds_ ([arXiv:0912.0827](http://arxiv.org/abs/0912.0827))


category: category

[[!redirects CartSp]]
[[!redirects Cart Sp]]
[[!redirects CartesianSpace]]
[[!redirects Cartesian Space]]
[[!redirects CartesianSpaces]]
[[!redirects Cartesian Spaces]]

[[!redirects SmoothCartSp]]


[[!redirects smooth Cartesian space]]
[[!redirects smooth Cartesian spaces]]


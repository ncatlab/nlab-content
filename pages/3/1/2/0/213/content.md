
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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


## Idea

The [[category]] $CartSp$ is the category of [[cartesian space]]s $\mathbb{R}^n$ and [[smooth function]]s between them.
This is the basic category of test [[space]]s on which [[differential geometry]] and its generalizations is modeled. 

## Definition

By $CartSp$ we denote the [[category]]

* whose [[object]]s are the [[cartesian spaces]] $\mathbb{R}^n$, $n \in \mathbb{N}$ -- the [[real line]] to its $n$th [[product|cartesian power]] -- equipped with their standard smooth structure;

* whose [[morphism]]s are all [[smooth functions]] between these spaces.

So $CartSp$ may be thought of as the [[full subcategory]] of [[Diff]] on the [[smooth manifold]]s of the form $\mathbb{R}^n$ for $n \in \mathbb{N}$.


Some variants of this are of interest:

* write $ThCartSp$ for the category of [[nLab:infinitesimal object|infinitesimally thickened]] Cartesian spaces: the [[full subcategory]] on the category of [[smooth loci]] on those of the form $\mathbb{R}^n \times d$, where $d$ is an [[infinitesimal space]].

## Geometry induced from $CartSp$.

Along the general lines of [notions of space](http://ncatlab.org/nlab/show/space#NotionsOfSpace) we have the following notions of spaces modeled on $CartSp$.

Consider [[CartSp]] as a [[site]] with the standard notion of [[coverage]] (for instance [[good open cover]]s, using that fact that a [[Cartesian space]] is [[diffeomorphism|diffeomorphic]] to an open ball).

Then 

* the category of very general spaces modeled on $CartSp$ is the [[sheaf topos]] $Sh(CartSp)$;

  Some objects in here are indeed very general spaces. For instance there is the sheaf $\Omega^p : \mathbb{R}^n \mapsto \Omega^p_{closed}(\mathbb{R}^n)$ that assigns sets of closed [[differential form]]s. This is a very non-classical object. For instance in that this space has just a single point, a single curve, a single surface, and so on, up to a single $(p-1)$-dimensional plot, but then has infinitely many $p$-dimensional plots. Despite this non-classicality, this is a very natural and useful object. To some extent it plays the role of an [[Eilenberg-MacLane space]] $K(\mathbb{R},p)$, even though it is far from having an underlying topological space.

* Accordingly, the first major subcategories inside $Sh(Cart)$ of more tame objects are those sheaves that do have underlying [[topological space]]s: these are the [[concrete sheaves]]

  $$
    DiffeologicalSpaces \subset Sh(CartSp)
  $$

  called [[diffeological space]]s. Among them objects like [[Frölicher space]]s play roughly the role of locally [[CartSp]]-ringed spaces, vaguely in the sense of [[structured (∞,1)-topos]]es.

* Refining one step further to even more tame objects inside $Sh(CartSp)$ we arrive at those concrete sheaves that are locally isomorphic to a [[representable functor]]. i.e. to a Cartesian space itsef. These are the [[smooth manifold]]s

  $$
    SmoothManifolds \hookrightarrow DiffeologicalSpaces \hookrightarrow
    Sh(CartSp)
    \,.
  $$

* Finally the Cartesian test spaces themselves sind inside this hierarchy via the [[Yoneda embedding]]  $CartSp \hookrightarrow Sh(CartSp)$ , which we have hence factored as

  $$
    CartSp \hookrightarrow
    SmoothManifolds \hookrightarrow DiffeologicalSpaces \hookrightarrow
    Sh(CartSp)
    \,.
  $$

As already indicated, this story in ordinary [[category theory]] may be lifted to [[higher topos theory]]. The [[(∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$ is a model for generalized [[Lie ∞-groupoid]]s. The fact that a Cartesian space is effectively just a smooth open ball makes this a [[locally contractible (∞,1)-topos]].


Dually, using that $CartSp$ is evidently the syntactic category of a [[Lawvere theory]] (even of a [[Fermat theory]]) there are the generalized [[quantities]] modeled on $CartSp$, algebras over this theory:

* a product-preserving [[functor]] $A \in Func_\times(CartSp,Set)$ is a [[smooth algebra]].

* a product-preserving [[(∞,1)-functor]] $A \in (\infty,1)Func_\times(CartSp, \infty Grpd)$ , i.e. an algebra over $CartSp$ regarded as an [[(∞,1)-algebraic theory]] is a [[smooth (∞,1)-algebra]]. 


Iterating this way of passing from simple test spaces to spaces and quantities modeled on them, we can next consider 

* $C^\infty Alg^{op} := Func_\times(CartSp,Set)^{op}$

and

* $(\infty,1)C^\infty Alg^{op} := Func_\times(CartSp,\infty Grpd)^{op}$

as new categories of test spaces, and pass to generalized spaces modeled on these.

The very general spaces modeled on $C^\infty Alg^{op}$ form the [[smooth topos]]es used in the well-adapted [[Models for Smooth Infinitesimal Analysis]] in the context of [[synthetic differential geometry]].

On the other hand, considering [[locally ringed space]]s with local rings of functions in $(\infty,1)C^\infty Alg^{op}$  leads to the notion of [[derived smooth manifold]]s.


## References {#References}

There are various slight variations of the category $CartSp$ that one can consider without changing its basic properties as a category of test spaces for [[generalized smooth space]]s. A different choice that enjoys some popularity in the literature is the category of open (contractible) subsets of Euclidean spaces. For more references on this see [[diffeological space]].

The [[site]] $ThCartSp$ of infinitesimally thickened Cartesian spaces is known as the site for the [[Cahiers topos]]. It is considered 

in detal in section 5 of

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

[[!redirects ThCartSp]]
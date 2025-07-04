
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

\tableofcontents

## Idea

A **diffeological vector space** is a [[real vector space]] equipped with a [[diffeology]] for which addition and scalar multiplication are [[smooth map|smooth]], similar to how a [[topological vector space]] is a vector space equipped with a [[topological space|topology]] for which addition and scalar multiplication are [[continuous map|continuous]]. In principle one could also define diffeological vector spaces over arbitrary [[diffeological field]]s, but in practice it seems that almost exclusively real and only sometimes complex diffeological vector spaces are considered.

The natural [[morphisms]] between diffeological vector spaces are the [[smooth map|smooth]] [[linear maps]], analogous to how the natural morphisms between topological vector spaces are the [[continuous map|continuous]] linear maps. Together diffeological vector spaces and smooth linear maps form a [[category]] $DiffVect_{\mathbb{R}}$ analogous to [[TopVect]]$_{\mathbb{R}}$.

## Properties

The obvious [[forgetful functor]] $DiffVect_{\mathbb{R}}\to Vect_{\mathbb{R}}$ gives diffeological vector spaces the structure of a [[concrete category]] over the category [[Vect]]$_{\mathbb{R}}$ of real vector spaces. Even more is true: for every family of linear maps $f_i:V\to W_i$ from a real vector space into diffeological vector spaces there is a coarsest diffeology on $V$ turning $V$ into a diffeological vector space and rendering all the maps $f_i$ smooth, and dually there is also a finest such diffeology for every family of linear maps $f_i:W_i\to V$ from diffeological vector spaces into $V$. This gives $DiffVect_{\mathbb{R}}$ like $TopVect_{\mathbb{R}}$ the structure of a [[topological concrete category]] over $Vect_{\mathbb{R}}$. In particular, this means that $DiffVect_{\mathbb{R}}$ is [[complete category|complete]], [[cocomplete category|cocomplete]], [[well-powered category|well-powered]] and [[well-powered category|co-well-powered]], that the forgetful functor $DiffVect_{\mathbb{R}}\to Vect_{\mathbb{R}}$ [[preserved limit|preserves]] all [[limits]] and [[colimits]] and that it thus has both a [[left adjoint]] and a [[right adjoint]].

Intuitively, all of this can be summarised as saying that the category $DiffVect_{\mathbb{R}}$ behaves over $Vect_{\mathbb{R}}$ much like e.g. [[Top]] behaves over [[Set]]: vector diffeologies on any given vector space form a [[complete lattice]], and all constructions like limits/colimits and subspaces/quotients can be carried out by equipping the corresponding vector space with the finest/coarsest vector diffeology that renders all the involved structure maps smooth.

## Relation to topological vector spaces

Since the [[D-topology]] provides a natural way to turn diffeological spaces into topological spaces, it seems only natural to assume that it also turns diffeological vector spaces into topological vector spaces. This however turns out to be false, because the D-topology does not commute with products and so addition $+:V\times V\to V$ can be discontinuous with respect to the product topology on $V\times V$ even though it is continuous with respect to the D-topology of the product diffeology on $V\times V$; an explicit example of this is claimed in ([Wu & Yang 2022, theorem 9.9](#WY2022)). At least scalar multiplication on the other hand does always end up continuous, because the D-topology preserves binary products involving [[locally compact]] spaces like $\mathbb{R}$.

## Fine diffeological vector spaces

The *fine diffeology* on a given real vector space $V$ is the finest diffeology turning it into a diffeological vector space. While the coarsest such diffeology is always just the indiscrete one, the fine diffeology is usually not discrete; instead it is generated by all linear maps $\mathbb{R}^n\to V$, or equivalently given by all maps $\mathbb{R}^n\to V$ that locally look like a smooth map to a finite-dimensional subspace of $V$. A diffeological vector space is called *fine* if it is equipped with the fine diffeology; for example, all finite-dimensional real vector spaces with their standard diffeologies are fine.

All linear maps from a fine diffeological vector space into other diffeological vector spaces are smooth. In particular, the construction of fine diffeological vector spaces is functorial, and in fact it is the aforementioned left adjoint to the forgetful functor $DiffVect_{\mathbb{R}}\to Vect_{\mathbb{R}}$.


## References

See also: 

* {#PIZ} [[Patrick Iglesias-Zemmour]], _Diffeology_, Mathematical Surveys and Monographs, AMS (2013) ([web](http://math.huji.ac.il/~piz/Site/The%20Book.html), [ ISBN:978-0-8218-9131-5](https://bookstore.ams.org/surv-185))
 * {#WY2022} [[Enxin Wu]], Zhongqiang Yang, _Topology on diffeological vector spaces_, preprint &lbrack;[arXiv:2205.09562](https://arxiv.org/abs/2205.09562)&rbrack;

[[!redirects diffeological vector spaces]]

> This entry is about a certain way of formalizing [[higher geometry]]. For variants and more background, see there.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea and motivation

For $T$ a [[nLab:Lawvere theory]], the _geometry_ modeled on $T$ is encoded in the [[nLab:sheaf topos]] on formal duals of $T$-algebras.

This statement generalizes to [[nLab:(∞,1)-category theory]]: for $T$ an [[nLab:(∞,1)-algebraic theory]] and $C \subset T Alg^{op}$ a [[nLab:(∞,1)-site]] of formal duals of $\infty$-algebras over $T$, one says that the [[nLab:(∞,1)-topos]] $\mathbf{H} = \infty Sh(C)$ over $C$ encodes **[[nLab:derived geometry]]** modeled on $T$. The objects of $\mathbf{H}$ also called _[[nLab:derived stack]]s_ on $C$.

The term "derived" here is meant to specifically contrast with [[nLab:∞-stack]]s on just a 1-categorical site. Even if $T$ happens to be just an ordinary Lawvere theory, regarded as a 1-[[nLab:truncated]] $(\infty,1)$-theory, the $\infty$-topos over $T Alg_\infty^{op}$ behaves considerably different from that over just $T Alg^{op}$.

An object $X$ in derived geometry has both, an [[nLab:∞-groupoid]] of internal symmetries as well as an $\infty$-[[nLab:function algebras on ∞-stacks|algebra of functions]]:

1. passing from a  sheaf topos over a site to the $\infty$-stacks over that site makes _[[nLab:colimit]]s_ behave well in [[nLab:cohomology]]. For instance a singular [[nLab:quotient]] becomes an [[nLab:orbifold]]. 

1. passing to derived geometry by making the site a genuine $(\infty,1)$-category makes _[[nLab:limit]]s_ behave well in cohomology. For instance the intersection pairing of non-[[nLab:transversal map|transversal]] [[nLab:smooth manifold]]s comes out correctly when regarding them as [[nLab:derived smooth manifold]]s.

A central class of examples for nontransveral [[nLab:pullback]]s in derived geometry are [[nLab:derived loop space]] objects. For $X \in T Alg^{op}$ an ordinary space, its [[nLab:free loop space object]] computed in the underived $\infty$-topos over $T Alg^{op}$ exists, but simply coincides with $X$, because $X$ is 0-[[nLab:truncated]] in there. But the free loop space object $\mathcal{L}X$ of $X$ computed in the $\infty$-topos over $T Alg_\infty^{op}$ may be very rich: its $\infty$-[[nLab:function algebras on infinity-stacks|function algebra]] is the [[nLab:Hochschild homology]] of $X$. Moreover, the functions on $\mathcal{L}X$ that are invariant under the canonical internal [[nLab:circle]]-[[nLab:action]] are the _closed_ [[nLab:Kähler differential]] forms on $X$.


Examples of derived spaces have appeared long ago as the configuration spaces in [[nLab:gauge theory]]. What is called the [[nLab:BV-BRST complex]] of a gauge theory is the function algebra on the [[nLab:infinitesimal object|infinitesimal]] approximation to a derived orbifold whose internal symmetries are the [[nLab:gauge transformation]]s and whose function complex provides a [[nLab:resolution]] of the locus of solutions to the physical equations of motion.

More recently, much of motivation for derived geometry came from the observation that the [Goerss-Hopkins-Miller theorem](http://arxiv.org/abs/0910.5130) suggests that there is a [[nLab:A Survey of Elliptic Cohomology - the derived moduli stack of derived elliptic curves|derived moduli space of derived elliptic currves]], that it carries a [[nLab:structured (∞,1)-topos|structure ∞-sheaf]] of [[nLab:E-∞-rings]], and the the [[nLab:global section]]s of that yield the [[nLab:ring spectrum]] of the [[nLab:generalized cohomology theory]] called [[nLab:tmf]].


## References

A systematic description of derived geometry using [[nLab:model category]]-theoretic tools was first undertaken in 

* [[nLab:Bertrand Toën]], [[nLab:Gabriele Vezzosi]], 

  * _Homotopical Algebraic Geometry I: Topos theory_ ([arXiv](http://arxiv.org/abs/math/0207028))

  * _Homotopical Algebraic Geometry II: geometric stacks and applications _ ([arXiv](http://arxiv.org/abs/math/0404373))

This generalizes the Brown-Jardine-Joyal-[[nLab:model structure on simplicial presheaves]] to a [[nLab:model structure on sSet-enriched presheaves]] over an [[nLab:sSet-site]].

A proposal for the precise set of the scene of derived geometry in general abstract [[nLab:(∞,1)-category theory]]-terms is

* [[nLab:Jacob Lurie]], _[[nLab:Structured Spaces]]_

The main point of this is an formalization and identification of special tame objects inside the collection of all [[nLab:derived stack]]s, namely the [[nLab:derived scheme]]s and [[nLab:structured (∞,1)-topos]]es.

The relevance of derived loop spaces in derived was notably amplified in a series of articles by [[nLab:David Ben-Zvi]] and [[nLab:David Nadler]],

* [[nLab:David Ben-Zvi]], [[nLab:David Nadler]],

  * _Loop Spaces and Langlands Parameters_ ([arXiv:0706.0322](http://arxiv.org/abs/0706.0322)) 

  * _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry _ ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))

  * _Loop Spaces and Connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))

    This article uses To&#235;n's theory of [[nLab:function algebras on ∞-stacks]] for showing that the function complex on a derived loop space $\mathcal{L}X$ is under mild conditions the [[nLab:Hochschild homology]] complex of $X$ hence by [[nLab:Hochschild-Kostant-Rosenberg theorem]] the collection of [[nLab:Kähler differential]] forms on $X$, and that the functions on $\mathcal{L}X$ that are invariant under the canonical $S^1$-[[nLab:action]] on $\mathcal{L}X$ are the _closed_ forms. This also gives a geometric interpretation of the old observation by [[nLab:Maxim Kontsevich]] and others, that the differential and grading on the de Rham complex may be understood as induced from automorphisms of the [[nLab:odd line]].

  * _Loop Spaces and Representations_ ([arXiv:1004.5120](http://arxiv.org/abs/1004.5120))


The application of derived geometry to the construction of [[nLab:tmf]] is described in

* [[nLab:Jacob Lurie]], _[[nLab:A Survey of Elliptic Cohomology]]_

The article

* [[nLab:David Spivak]], _Derived smooth manifolds_

discussed the $\infty$-version of [[nLab:smooth algebra|C-oo-rings]] -- the algebras over the Lawvere theory [[nLab:CartSp]] -- and the corresponding locally ringed spaces: [[nLab:derived smooth manifold]]s.

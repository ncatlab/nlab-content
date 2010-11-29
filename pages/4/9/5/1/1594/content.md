
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An _orbifold_ is a [[differentiable stack]] which may be presented by a [[proper groupoid|proper]] [[étale groupoid|étale]] [[Lie groupoid]]. [[Morita equivalence|Morita equivalent]] Lie groupoids give rise to the same orbifold. One can consider a [[bicategory]] of proper &#233;tale Lie groupoids and the orbifolds will be the objects of certain bicategorical [[localization]] of this bicategory (a result of Moerdijk and Pronk). 

An orbifold is traditionally defined as a topological space equipped with an _orbifold structure_, which is in turn an equivalence class of _orbifold atlases_. An orbifold is locally a stack quotient of a [[smooth manifold]] by a finite group. Every orbifold is globally a quotient of a smooth manifold by an action of finite-dimensional [[Lie group]] with finite stabilizers in each point (the construction uses the frame bundle). The word orbifold is invented by Thurston, while the original name was V-manifold (Satake), and was taken in a more restrictive sense, assuming that the actions of finite groups on the charts are always effective. Nowdays we call such orbifolds _effective_ and those which are global quotients by a finite group _global quotient orbifolds_.  

## (Co)homology

It has been noticed that the topological invariants of the underlying topological space of an orbifold as a topological space with an orbifold structure are not appropriate, but have to be corrected leading to orbifold Euler characteristics, orbifold cohomology etc. One of the constructions which is useful in this respect is the inertia orbifold (the inertia stack of the original orbifold) which gives rise to "twisted sectors" in Hilbert space of a quantum field theory on the orbifold, and also to twisted sectors in the appropriate cohomology spaces. A further generalization gives multitwisted sectors. 

## Algebraic orbifolds

There is also a notion of finite stabilizers in [[algebraic geometry]]. A singular variety is called an (algebraic) _orbifold_ if it has only so-called _orbifold singularities_.

## References

* [[Ieke Moerdijk]], _Orbifolds as Groupoids: an Introduction_ ([arXiv](http://arxiv.org/abs/math.DG/0203100) [blog](http://golem.ph.utexas.edu/string/archives/000733.html))

* Eugene Lerman, _Orbifolds as stacks?_ ([arXiv](http://arxiv.org/abs/0806.4160))

Orbifolds often appear as moduli spaces in differential geometric setting:

* [[Dietmar Salamon]], [[Joel Robbin|Joel W. Robbin]], A construction of the Deligne--Mumford orbifold, J. Eur. Math. Society, ISSN 1435-9855, Vol. 8, N&#186; 4, 2006, 611-699 ([arXiv](http://arxiv.org/abs/math/0407090))

An interesting generalization of an orbifold is so-called weighted branched manifold; see

* [[Dusa McDuff]], Groupoids, branched manifolds and multisections, J. Symplectic Geom. Volume 4, Number 3 (2006), 259-315 ([project euclid](http://projecteuclid.org/euclid.jsg/1180135649))

Wikipedia [article](http://en.wikipedia.org/wiki/Orbifold) is mainly tailored toward Thurston's approach. 

[[!redirects orbifolds]]
+-- {: .query}
I am confused by this page.  It starts out by boldly declaring that "An orbifold is a differentiable stack which may be presented by a proper &#233;tale Lie groupoid" but then it  goes on to talk about the "traditional" definition.  The traditional definition definitely **does not**  view orbifolds as stacks.   Neither does Moerdijk's paper referenced below --- there orbifolds form a 1-category.

Personally I am not completely convinced that orbifolds are differentiable stacks.  Would it not be better to start out by saying that there is no consensus on what orbifolds "really are" and lay out three points of view: traditional, Moerdijk's "orbifolds as groupoids" (called "modern" by Adem and Ruan in their book) and orbifolds as stacks?

[[Urs Schreiber]]: please, go ahead. It would be appreciated.

=--

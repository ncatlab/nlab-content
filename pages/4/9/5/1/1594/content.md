
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
 {:toc}

## Idea

Where an ordinary [[manifold]] is a [[space]] locally modeled on [[Cartesian spaces]], an _orbifold_ is, more generally, a [[space]] that is locally modeled on [[Lie groupoid|smooth]] [[action groupoids]] (="stack quotients") of a [[finite group]] [[action|acting]] on a [[Cartesian space]].

This turns out to be equivalent ([Moerdijk](#Moerdijk), [Mordijk-Pronk](#MoerdijkPronk)) to saying that an orbifold is a [[proper groupoid|proper]] [[étale groupoid|étale]] [[Lie groupoid]]. ([[Morita equivalence|Morita equivalent]] Lie groupoids correspond to the same orbifolds.)

The word _orbifold_ was invented in ([Thurston 1992](#Thurston)), while the original name was _$V$-manifold_ ([Satake](#Satake)), and was taken in a more restrictive sense, assuming that the actions of finite groups on the charts are always effective. Nowdays we call such orbifolds _effective_ and those which are global quotients by a finite group _global quotient orbifolds_.  

There is also a notion of finite stabilizers in [[algebraic geometry]]. A singular variety is called an (algebraic) _orbifold_ if it has only so-called _orbifold singularities_.

## Definition

An orbifold is a stack presented by an [[orbifold groupoid]].

## Properties

### General

* One can consider a [[bicategory]] of proper &#233;tale Lie groupoids and the orbifolds will be the objects of certain bicategorical [[localization]] of this bicategory (a result of [Moerdijk and Pronk](#MoerdijkPronk)). 


* Equivalently, every orbifold is globally a quotient of a smooth manifold by an [[action]] of finite-dimensional [[Lie group]] with finite [[stabilizer subgroup|stabilizers]] in each point. 



### (Co)homology

It has been noticed that the topological invariants of the underlying topological space of an orbifold as a topological space with an orbifold structure are not appropriate, but have to be corrected leading to orbifold Euler characteristics, orbifold cohomology etc. One of the constructions which is useful in this respect is the inertia orbifold (the inertia stack of the original orbifold) which gives rise to "twisted sectors" in Hilbert space of a quantum field theory on the orbifold, and also to twisted sectors in the appropriate cohomology spaces. A further generalization gives multitwisted sectors. 




## Examples

* [[inertia orbifold]]

## Related concepts

Orbifolds are in [[differential geometry]] what [[Deligne-Mumford stacks]] are in [[algebraic geometry]]. In [[topology]] one also speaks of _[[orbispaces]]_.

Orbifolds may be regarded as a kind of _[[stratified spaces]]_.



## References

Original sources on orbifolds include

* I. Satake, _On a generalisation of the notion of manifold_, Proc. Nat. Acad. Sci. U.S.A. 42 (1956), 359&#8211;363.
 {#Satake}

* I. Satake, _The Gauss&#8211;Bonnet theorem for $V$-manifolds_, J. Math. Soc. Japan 9 (1957), 464&#8211;492.

* [[William Thurston]], _Three-dimensional geometry and topology,_ preliminary draft, University of Minnesota, Minnesota, (1992)
 {#Thurston} which in completed and revised form is available as his book: _The Geometry and Topology of Three-Manifolds;_ in particular the orbifold discussion is in [chapter 13](http://library.msri.org/books/gt3m/PDF/13.pdf).

Discussion of orbifold as [[Lie groupoids]]/[[differentiable stacks]] is in

* [[Ieke Moerdijk]], _Orbifolds as Groupoids: an Introduction_ ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100))
 {#Moerdijk}

* [[Ieke Moerdijk]], [[Dorette Pronk]], _Orbifolds, sheaves and groupoids_, K-theory 12 3-21 (1997) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/pronk.pdf))
  {#MoerdijkPronk}

* [[Eugene Lerman]], _Orbifolds as stacks?_ ([arXiv](http://arxiv.org/abs/0806.4160))

Orbifolds often appear as [[moduli spaces]] in differential geometric setting:

* [[Dietmar Salamon]], [[Joel Robbin|Joel W. Robbin]], A construction of the Deligne--Mumford orbifold, J. Eur. Math. Society, ISSN 1435-9855, Vol. 8, N&#186; 4, 2006, 611-699 ([arXiv](http://arxiv.org/abs/math/0407090))

The generalization of orbifolds to _weighted [[branched manifolds]]_ is discussed in

* [[Dusa McDuff]], _Groupoids, branched manifolds and multisections_, J. Symplectic Geom. Volume 4, Number 3 (2006), 259-315 ([project euclid](http://projecteuclid.org/euclid.jsg/1180135649))

See also

* wikipedia,  [orbifolds](http://en.wikipedia.org/wiki/Orbifold) 

(which is mainly tailored toward Thurston's approach). 

category: Lie theory


[[!redirects orbifolds]]

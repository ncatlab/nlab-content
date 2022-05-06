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

An [[orbifold]] is much like a [[smooth manifold]] but possibly with [[singularities]] of the form of [[fixed points]] of [[group]]-[[actions]].

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/OrbifoldTypes.jpg" width="240">
</div>

Where a [[smooth manifold]] is a [[space]] locally modeled on [[Cartesian spaces]]/[[Euclidean spaces]] $\mathbb{R}^n$, an _orbifold_ is, more generally, a [[space]] that is locally modeled on [[Lie groupoid|smooth]] [[action groupoids]] ([[homotopy quotients]]) $\mathbb{R}^n\sslash G$ of a [[finite group]] $G$ [[action|acting]] on a [[Cartesian space]].

> graphics grabbed from [Hyde-Ramsden-Robins 14](#HydeRamsdenRobins14)

This turns out to be broadly captured([Moerdijk-Pronk 97](#MoerdijkPronk97), [Moerdijk 02](#Moerdijk02)) by saying that an orbifold is a [[proper groupoid|proper]] [[étale groupoid|étale]] [[Lie groupoid]]. ([[Morita equivalence|Morita equivalent]] Lie groupoids correspond to the same orbifolds.)

The word _orbifold_ was invented in ([Thurston 1992](#Thurston)), while the original name was _$V$-manifold_ ([Satake](#Satake)), and was taken in a more restrictive sense, assuming that the actions of finite groups on the charts are always effective. Nowadays we call such orbifolds _effective_ and those which are global quotients by a finite group _global quotient orbifolds_.  

There is also a notion of finite stabilizers in [[algebraic geometry]]. A singular variety is called an (algebraic) _orbifold_ if it has only so-called _orbifold singularities_.

## Definition

An orbifold is a stack presented by an [[orbifold groupoid]].

## Properties

### General

* One can consider a [[bicategory]] of proper &#233;tale Lie groupoids and the orbifolds will be the objects of certain bicategorical [[localization]] of this bicategory (a result of [Moerdijk-Pronk 97](#MoerdijkPronk97)). 


* Equivalently, every orbifold is globally a quotient of a smooth manifold by an [[action]] of finite-dimensional [[Lie group]] with finite [[stabilizer subgroup|stabilizers]] in each point. (eg ([Adem-Leida-Ruan 2007](#ALR07)), Corollary 1.24)


### Global quotient orbifolds
 {#GlobalQuotientOrbifolds}

In ([ALR 07, theorem 1.23](#ALR07)) is asserted that every effective orbifold $X$ (paracompact, Hausdorff) is isomorphic to a global quotient orbifold, specifically to a global quotient of $O(n)$ (where $n$ is the dimension of $X$) acting on the [[frame bundle]] of $X$ (which is a manifold).

### (Co)homology

It has been noticed that the topological invariants of the underlying topological space of an orbifold as a topological space with an orbifold structure are not appropriate, but have to be corrected leading to [[orbifold Euler characteristics]], [[orbifold cohomology]] etc. One of the constructions which is useful in this respect is the [[inertia orbifold]] (the inertia stack of the original orbifold) which gives rise to "twisted sectors" in Hilbert space of a quantum field theory on the orbifold, and also to twisted sectors in the appropriate cohomology spaces. A further generalization gives multitwisted sectors. 




## Examples

* Some basic building blocks of orbifolds:

  The quotient of a  [[ball]] by a [[discrete group|discrete]] [[subgroup]] of the [[special orthogonal group]] of rotations. Is an orbifold, and orbifolds may be obtained by cutting out balls from ordinary [[smooth manifolds]] and gluing in these orbifold quotients.

* The [[moduli stack of elliptic curves]] over the [[complex numbers]] is an orbifold, being the [[homotopy quotient]] of the [[upper half plane]] by the [[special linear group]] acting by [[Möbius transformations]].

* For $\mathcal{G}$ any orbifold, then the [[mapping space]] $\mathcal{G}^{\Pi(S^1)} = \mathcal{G}^{B\mathbb{Z}}$ is again an orbifold, called the [[inertia orbifold]].

* [[G2-orbifolds]]

* [[lens spaces]]

* [[ADE singularities]]

* [[metric cones]]


## Related concepts

* [[Riemannian orbifold]]

  * [[flat orbifold]]

* [[discrete torsion]]

* [[motivation for higher differential geometry]]

* [[orbifold Euler characteristic]]

Orbifolds are in [[differential geometry]] what [[Deligne-Mumford stacks]] are in [[algebraic geometry]]. See also at _[[geometric invariant theory]]_ and _[[GIT-stable point]]_.

If the finiteness condition is dropped one also speaks of _[[orbispaces]] and generally of [[stacks]].

Orbifolds may be regarded as a kind of _[[stratified spaces]]_.

See also 

* [[étale groupoid]]

* [[stable map]]

* [[orbifold cohomology]]

* [[Gromov-Witten theory]]

Orbifolds in [[string theory]]:

* [[fractional D-brane]]

  [[permutation D-brane]]

* [[ADE singularity]]

* [[orientifold]]

## References

### General

The concept originates in

* {#Satake} I. Satake, _On a generalisation of the notion of manifold_, Proc. Nat. Acad. Sci. U.S.A. 42 (1956), 359&#8211;363.
 

* I. Satake, _The Gauss&#8211;Bonnet theorem for $V$-manifolds_, J. Math. Soc. Japan 9 (1957), 464&#8211;492.

* [[William Thurston]], _Three-dimensional geometry and topology,_ preliminary draft, University of Minnesota, Minnesota, (1992)
 {#Thurston} which in completed and revised form is available as his book: _The Geometry and Topology of Three-Manifolds;_ in particular the orbifold discussion is in [chapter 13](http://library.msri.org/books/gt3m/PDF/13.pdf).

Survey of basic orbifold theory:

* Daryl Cooper, Craig Hodgson, Steve Kerckhoff, _Three-dimensional Orbifolds and Cone-Manifolds_,  MSJ Memoirs Volume 5, 2000 ([pdf](https://web.math.ucsb.edu/~cooper/37.pdf), [euclid:1389985812](https://projecteuclid.org/euclid.msjm/1389985812))

* {#Kaye07} Adam Kaye, _Two-Dimensional Orbifolds_, 2007 ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2007/REUPapers/FINALFULL/Kaye.pdf))

* Michael Davis, _Lectures on orbifolds and reflection groups_, 2008 ([pdf](https://math.osu.edu/sites/math.osu.edu/files/08-05-MRI-preprint.pdf))

* {#Porti09} Joan Porti, _An introduction to orbifolds_, 2009 ([pdf](http://mat.uab.es/~porti/orbifoldLeiden.pdf))

Textbook account:

* {#Ratcliffe06} John Ratcliffe, _Geometric Orbifolds_, chapter 13 in _Foundations of Hyperbolic Manifolds_, Springer 2006

On [[Riemannian orbifolds]]:

* Christian Lange, _Orbifolds from a metric viewpoint_ ([arXiv:1801.03472](https://arxiv.org/abs/1801.03472))

* Renato G. Bettiol, Andrzej Derdzinski, Paolo Piccione, _Teichmüller theory and collapse of flat manifolds_, Annali di Matematica (2018) 197: 1247 ([arXiv:1705.08431](https://arxiv.org/abs/1705.08431), [doi:10.1007/s10231-017-0723-7](https://doi.org/10.1007/s10231-017-0723-7))

* {#HydeRamsdenRobins14} S. T. Hyde, S. J. Ramsden and V. Robins, _Unification and classification of two-dimensional crystalline patterns using orbifolds_, Acta Cryst. (2014). A70, 319-337 ([doi:10.1107/S205327331400549X](https://doi.org/10.1107/S205327331400549X))



Discussion of orbifold as [[Lie groupoids]]/[[differentiable stacks]] is in

 

* {#MoerdijkPronk97} [[Ieke Moerdijk]], [[Dorette Pronk]], _Orbifolds, sheaves and groupoids_, K-theory 12 3-21 (1997) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/pronk.pdf))

* {#Moerdijk02} [[Ieke Moerdijk]], _Orbifolds as Groupoids: an Introduction_, [[Alejandro Adem]], [[Jack Morava]], Yongbin Ruan (eds.) _Orbifolds in Mathematics and Physics_, Contemporary Math 310 , AMS (2002), 205–222 ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100))
  

* [[Eugene Lerman]], _Orbifolds as stacks?_ ([arXiv:0806.4160](http://arxiv.org/abs/0806.4160))

The [[mapping stacks]] of orbifolds are discussed in

* W. Chen, _On a notion of maps between orbifolds_, I. Function spaces, Commun. Contemp. Math. 8 (2006), no. 5, 569&#8211;620.

Orbifolds often appear as [[moduli spaces]] in differential geometric setting:

* [[Dietmar Salamon]], [[Joel Robbin|Joel W. Robbin]], A construction of the Deligne--Mumford orbifold, J. Eur. Math. Society, ISSN 1435-9855, Vol. 8, N&#186; 4, 2006, 611-699 ([arXiv](http://arxiv.org/abs/math/0407090))

The generalization of orbifolds to _weighted [[branched manifolds]]_ is discussed in

* [[Dusa McDuff]], _Groupoids, branched manifolds and multisections_, J. Symplectic Geom. Volume 4, Number 3 (2006), 259-315 ([project euclid](http://projecteuclid.org/euclid.jsg/1180135649)).

A reference dealing with the [[string topology]] of orbifolds is

* {#ALR07} A. Adem, J. Leida and Y. Ruan, _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))

The relation of orbifolds to [[global equivariant homotopy theory]] is discussed in

* [[Stefan Schwede]], _Orbispaces, orthogonal spaces, and the universal compact Lie group_ ([arXiv:1711.06019](https://arxiv.org/abs/1711.06019)) (on the relation to [[orbispaces]]/[[topological stacks]])


See also

* Wikipedia,  _[Orbifolds](http://en.wikipedia.org/wiki/Orbifold)_ 

(which is mainly tailored toward Thurston's approach). 

### Orbifold cobordism

Orbifold [[cobordisms]] are discussed in 

* K. S. Druschel, _Oriented Orbifold Cobordism_, Pacific J. Math., 164(2) (1994), 299-319.

* K. S. Druschel, _The Cobordism of Oriented Three Dimensional Orbifolds_, Pacific J. Math., bf 193(1) (2000), 45-55.

* Andres Angel, _Orbifold cobordism_ ([pdf](http://www.math.uni-bonn.de/people/aangel79/Orbifold%20cobordism.pdf)) 

See also at _[[orbifold cobordism]]_.

### In string theory
 {#ReferencesInStringTheory}

In [[perturbative string theory]], orbifolds as [[target spaces]] for a [[string]] [[sigma-model]] were first considered in 

* {#DixonHarveyVafaWitten85} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds_, Nuclear Physics B Volume 261, 1985, Pages 678-686 (<a href="https://doi.org/10.1016/0550-3213(85)90593-0">doi:10.1016/0550-3213(85)90593-0</a>)

* {#DixonHarveyVafaWitten86} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds (II)_, Nuclear Physics B Volume 274, Issue 2, 15 September 1986, Pages 285-314 (<a href="https://doi.org/10.1016/0550-3213(86)90287-7">doi:10.1016/0550-3213(86)90287-7</a>)

and then further developed notably in 

* {#DVVV89} [[Robbert Dijkgraaf]], [[Cumrun Vafa]], [[Erik Verlinde]], [[Herman Verlinde]], _The operator algebra of orbifold models_, Comm. Math. Phys. Volume 123, Number 3 (1989), 485-526.

* [[Eric Zaslow]], _Topological orbifold models and quantum cohomology rings_, Comm. Math. Phys. 156 (1993), no. 2, 301&#8211;331.

See also the references at _[[fractional D-brane]]_.

Review of orbifolds in the context of string compactifications includes

* Susanne Reffert, _The Geometer's Toolkit to String Compactifications_, lectures at _[String and M theory approaches to particle physics and cosmology](https://www.ggi.infn.it/showevent.pl?id=11)_, 2007 ([arXiv:0706.1310](https://arxiv.org/abs/0706.1310))

and for orbifolds of [[G2-manifolds]] for [[M-theory on G2-manifolds]]

* {#Reidegeld15} [[Frank Reidegeld]], _$G_2$-orbifolds from K3 surfaces with ADE-singularities_ ([arXiv:1512.05114](http://arxiv.org/abs/1512.05114))

* [[Frank Reidegeld]], _$G_2$-orbifolds with ADE-singularities_ ([pdf](https://core.ac.uk/download/pdf/159317626.pdf))


For [[topological strings]] the [[path integral as a pull-push transform]] for target orbifolds -- in analogy to what [[Gromov-Witten theory]] is for [[Deligne-Mumford stacks]] -- has first been considered in 

* {#ChenRuan01} Weimin Chen, [[Yongbin Ruan]], _Orbifold Gromov-Witten Theory_, in _Orbifolds in mathematics and physics_ (Madison, WI, 2001), 25&#8211;85, Contemp. Math., 310, Amer. Math. Soc., Providence, RI, 2002 ([arXiv:math/0103156](http://arxiv.org/abs/math/0103156))
 

A review with further pointers is in 

* {#Abramovich05} [[Dan Abramovich]], _Lectures on Gromov-Witten invariants of orbifolds_ ([arXiv:math/0512372](http://arxiv.org/abs/math/0512372))
 

category: Lie theory



[[!redirects orbifolds]]
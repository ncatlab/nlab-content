[[!redirects Poincare duality]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--
 

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Poincar&#233; duality over some [[space]] is an [[equivalence]]  (if it exists) relating [[cohomology]] with [[homology]] on that space.

The canonical example is the Poincar&#233; duality in [[ordinary cohomology]] $H^\bullet(X)$/[[ordinary homology]] $H_\bullet(X)$ which exists over an [[orientation|orientable]] [[closed manifold]] $X$ of [[dimension]] $n$: any choice of [[volume form]] $\omega$ induces by the [[cap product]] an [[isomorphism]]

$$
  (-)\cap \omega \;\colon\; H_\bullet(X) \stackrel{\simeq}{\to} H^{n-\bullet}(X)
  \,.
$$

More generally Poincar&#233; duality is about [[dual objects]] in a [[generalized cohomology theory]]. For instance if $X$ above is furthermore [[K-orientation|K-oriented]], hence [[orientation in generalized cohomology |oriented]] in the [[K-theory]] [[cohomology theory]] (hence if it has [[spin^c structure]]) then there is an isomorphism between its [[K-homology]] and [[K-theory]]. For more on this see at _[[Poincaré duality algebra]]_.

Poincar&#233; duality is the mechanism behind [[Umkehr maps]]/[[push-forward in generalized cohomology]]: given a map of [[spaces]] $f \colon X \to Y$ which enjoy Poincar&#233; duality with respect to some [[generalized cohomology theory]] $R$, one can pass from the canonically given pullback morphism 

$$
  f^\ast \colon R^\bullet(Y) \to R^\bullet(X)
$$

to the [[dual morphism]]

$$
  f_! \colon R^\bullet(X) \simeq R_\bullet(X) \stackrel{f_\ast}{\to} R_\bullet(Y) \simeq R^\bullet(Y)
  \,.
$$

Here the duality is typically exhibited in two steps: 

1. an [[Atiyah duality]] identifies the dual of $R^\bullet(X)$ with the $R$-cohomology of a [[Thom space]] of $X$;

1. a [[Thom isomorphism]] identified the $R$-cohomology of the Thom space back with that of $X$.

More generally, spaces $X$ are not self-dual in this way, but may at least be dual to themselves but equipped with a [[twisted cohomology|twist]]. This yields the _[[twisted Umkehr maps]]_ in [[twisted cohomology]] (see for instance at [[Freed-Witten-Kapustin anomaly cancellation]]).

For more on this see at _[[twisted Umkehr map]]_.

## Properties

### Recognition of manifolds

+-- {: .query}

From [ALGTOP-L], Oct 5, 2010.

* [[Jim Stasheff]]:  

  Any one have a reference for obstructions which detect whether a space whose cohomology has Poincare duality is actually a manifold? thanks

* John Klein: 

  Ranicki's total surgery obstruction does it in the top case, in
surgery dimensions.

  * The total surgery obstruction. Algebraic topology, Aarhus 1978 (Proc. Sympos., Univ. Aarhus, Aarhus, 1978), pp. 275--316, Lecture Notes in Math., 763, Springer, Berlin, 1979. ([pdf](http://www.maths.ed.ac.uk/~aar/papers/total.pdf))


* Nathanien Rounds:

  I believe this question is answered (simply connected case, over Q) in
Dennis Sullivan's paper Infinitesmal Computations in Topology (Theorem 13.2).  The answer, as I understand it, is that outside dimension 4k any graded commutative algebra over Q wtih first betti number 0 satisfying Poincare Duality can be realized as the cohomoloyg ring of a manifold.  In dimension 4k there is an obstruction related to the signature which is given in that paper.  There won't in general be a unique manifold corresponding to the ring; for example one can choose different rational Pontragin classes and change the homemorphism type but not the cohomology. 

  The general answer (not simply connected, over Z) is given by Ranicki's total surgery obstruction, as John Klein has already pointed out. One way to interpret this obstruction geometrically is that the Poincare duality map is always "local" but it need not have a "local" inverse, and the lack of a local inverse is an obstruction to having a anifold structure.  See for example McCrory's paper "A Characterization of Homology Manifolds" and also my thesis, which if you're interested is here:

  www.math.purdue.edu/~nrounds

=--

See also ([Ranicki 96](#Ranicki96)) and see at _[[Poincaré complex]]_.

### Relation to Thom isomorphism

The Poincar&#233; dual of a [[submanifold]] can be identified with the [[Thom class]] on its [[normal bundle]]

(...)

### Generalizations

The [[six operations]] of [[Grothendieck]] and [[Grothendieck duality]] are designed to ensure a generalized and relative versions of Poincar&#233; duality and related phenomena in the setups like sheaf and [[topos theory]], algebraic geometry. See _[[Grothendieck duality]]_ for references. 

Another generalization, for singular spaces, is with help of stratifications and via [[intersection cohomology]]. 

## Variants and generalizations

* in [[noncommutative topology]]: [[Poincaré duality algebra]]

* in [[derived category|derived]] [[abelian sheaf|abelian]] [[sheaf and topos theory]]: [[Verdier duality]]

* in [[nonabelian cohomology]]: [[nonabelian Poincaré duality]]

## Related concepts

* [[Poincaré complex]]

* [[Poincaré duality algebra]]



## References

### General

* [[eom]], _[Poincar&#233; duality](http://www.encyclopediaofmath.org/index.php/Poincar%C3%A9_duality)_

* [[Andrew Ranicki]], _45 slides on chain duality_, September 1996 ([pdf](http://www.math.uiuc.edu/K-theory/0154/45slides.pdf))
 {#Ranicki96}

### For Hochschild cohomology

[[nLab:Poincaré duality]] on [[nLab:Hochschild cohomology|Hochschild (co)homology]]

* M. Van den Bergh, _A relation between Hochschild homology and cohomology for Gorenstein rings_ . Proc. Amer. Math. Soc. 126 (1998), 1345&#8211;1348; ([JSTOR](http://www.jstor.org/stable/118786)) 

  Correction: Proc. Amer. Math. Soc. 130 (2002), 2809&#8211;2810.
{#VanDenBergh}

with more on that in

* U. Kr&#228;hmer, _Poincar&#233; duality in Hochschild cohomology_
  ([pdf](http://www.maths.gla.ac.uk/~ukraehmer/brussels.pdf))

That this Poincare duality takes the [[Connes coboundary operator]] to the [[BV operator]] is shown in 

* [[nLab:Victor Ginzburg]], _Calabi-Yau Algebras_, [arXiv/math.AG/0612139](http://arxiv.org/abs/math.AG/0612139)
{#Ginzburg}

### In higher geometry

Poincar&#233; duality on [[Deligne-Mumford stacks]]/[[orbifolds]] is discussed in 

* Dan Abramovich, Tom Graber, [[Angelo Vistoli]], _Gromov-Witten theory of Deligne-Mumford stacks_ ([arXiv:math/0603151](http://arxiv.org/abs/math/0603151))

* Weimin Chen, Yongbin Ruan, _A New Cohomology Theory for Orbifold_, Commun. Math. Phys. 248 (2004) 1-31 ([arXiv:math/0004129](http://arxiv.org/abs/math/0004129))

For disucssion in [[noncommutative topology]]/[[KK-theory]] see at _[[Poincaré duality algebra]]_.



[[!redirects Poincare duality]]
[[!redirects Poincaré duality]]
[[!redirects Poincar%C3%A9 duality]]

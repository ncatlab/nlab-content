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

More generally, spaces $X$ are not [[self-dual]] in this way, but may at least be dual to themselves but equipped with a [[twisted cohomology|twist]]. This yields the _[[twisted Umkehr maps]]_ in [[twisted cohomology]] (see for instance at [[Freed-Witten-Kapustin anomaly cancellation]]).

For more on this see at _[[twisted Umkehr map]]_.

## Definition and statement
 {#DefinitionAndStatement}

We first state the

* _[Traditional formulation](#TraditionalFormulation)_

and then its 

* _[Refinement in homotopy theory](#RefinementInHomotopyTheory)_.

### Traditional formulation
 {#TraditionalFormulation}

Around 1895 [[Henri Poincaré]] made an observation about [[Betti numbers]] of [[closed manifolds]], which in the 1930s was then formulated by [[Eduard ?ech]] and [[Hassler Whitney]] in the following modern form:

+-- {: .num_theorem #TraditionalPoincareDuality}
###### Theorem

Let $X$ be a [[closed manifold]] of [[dimension]] $n$ that is [[orientation|orientable]]. Then the [[cap product]] with any choice of [[orientation]] -- in the form of a [[fundamental class]] $[X] \in H_n(X)$ -- induces [[isomorphisms]] of the form

$$
  (-)\cap [X] \;\colon\; H^k(X) \stackrel{\simeq}{\to} H_{n-k}(X)
$$

between the [[ordinary cohomology]] and the [[ordinary homology]] groups of $X$.

=--

Later this was turned around and more general [[topological spaces]] satisfying this condition were considered

+-- {: .num_defn #PoincareDualitySpace}
###### Definition

A [[topological space]] for which there is $d \in \mathbb{N}$ and a  class $[X] \in H_d(X)$ such that the [[cap product]] induces [[isomorphisms]]

$$
  (-) \cap [X] \;\colon\; H^\bullet(X) \stackrel{\simeq}{\to} H_{d-\bullet}(X)
$$

is called a **[[Poincaré duality space]]**.
 

=--



### Refinement to homotopy theory 
 {#RefinementInHomotopyTheory}


Traditionally Poincar&#233; duality is stated as a [[dual object|duality]] of [[chain homology|chain]] [[homology groups]]. The passage from [[chain complexes]] to their [[homology groups]], hence the passage from full [[homotopy theory]] to just some invariants, however forgets a lot of information. But it turns out that this can always be lifted:

+-- {: .num_theorem}
###### Theorem

Let $X$ be a [[Poincaré duality space]] of [[dimension]] $n$, def. \ref{PoincareDualitySpace}. Then there is a [[quasi-isomorphism]]

$$
  C^\bullet(X) \stackrel{\simeq}{\to} \Sigma^{-d} C_\bullet(X)
$$

between the [[chain complex]] of [[ordinary cohomology]] of $X$ with that $d$-fold [[suspension|de-suspension]] of the [[chain complex]] of [[ordinary homology]] of $X$.

This is such that its image in [[chain homology]] is (up to sign) the traditional Poincar&#233; duality isomorphism

$$
  H^\bullet(X) \stackrel{\simeq}{\to} H_{\bullet + d}(X)
$$

of theorem \ref{TraditionalPoincareDuality}.

=--

This is ([EM 11, theorem, 2.5.2](#EM11)).

+-- {: .num_remark}
###### Remark

Since $C^\bullet(X) \simeq [C_\bullet(X,), \mathbb{I}] \simeq (C_\bullet(X))^\vee$ is the [[dual object]] to $C_\bullet(X)$ in the [[(∞,1)-category of unbounded chain complexes]], this says that for a [[Poincaré duality space]] $X$ the [[chain complex]] $C_\bullet(X)$ is almost a self-[[dual objects]], except for a degree-shift, hence except for a [[twisted cohomology|twist]] of (itself) degree 0.

=--





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

### Relation to push-forward in cohomology

Given Poincare duality and hence (twisted-)[[self-dual objects]], the [induced dagger-structure](self-dual+object#RelationToDaggerCompactStructure) allows torevert morphisms in [[cohomology]]. These "[[Umkehr maps]]" describe _[[fiber integration in cohomology]]_.

### Generalizations

The [[six operations]] of [[Grothendieck]] and [[Grothendieck duality]] are designed to ensure a generalized and relative versions of Poincar&#233; duality and related phenomena in the setups like sheaf and [[topos theory]], algebraic geometry. See _[[Grothendieck duality]]_ for references. 

Another generalization, for singular spaces, is with help of stratifications and via [[intersection cohomology]]. 

## Variants and generalizations

* in [[topology]]: [[Poincaré duality complex]]

* in [[noncommutative topology]]: [[Poincaré duality algebra]]

* in [[derived category|derived]] [[abelian sheaf|abelian]] [[sheaf and topos theory]] (for [[abelian sheaf cohomology]]): [[Verdier duality]]

* in [[nonabelian cohomology]]: [[nonabelian Poincaré duality]]

## Related concepts

* [[Poincaré complex]]

* [[Poincaré duality algebra]]

* [[KO-dimension]]

* [[Serre duality]]

## References

### General

This historical work of [[Henri Poincaré]] is reviewed around page 28. pf 

* [[Jean Dieudonné]], _A History of Algebraic and Differential Topology, 1900 - 1960_

Summaries of the traditional modern statement of Poincar&#233; duality are for instance in

* [[eom]], _[Poincar&#233; duality](http://www.encyclopediaofmath.org/index.php/Poincar%C3%A9_duality)_

* Manifold Atlas, _[Poincar&#233; Duality Spaces](http://www.map.mpim-bonn.mpg.de/Poincar%C3%A9_Duality_Spaces)_ 

Discussion of generalizations to "chain duality" (see also at _[[Poincare complex]]_) is at

* [[Andrew Ranicki]], _45 slides on chain duality_, September 1996 ([pdf](http://www.math.uiuc.edu/K-theory/0154/45slides.pdf))
 {#Ranicki96}

Discussion in [[etale cohomology]] is in 

* [[James Milne]], sections 14 and 24 of _[[Lectures on Étale Cohomology]]_

With an eye towards generalization in [[spectral geometry]] ([[spectral triples]]):

* {#Connes95} [[Alain Connes]], page 10 of _Noncommutative geometry and reality_, J. Math. Phys. 36 (11), 1995 ([pdf](http://www.alainconnes.org/docs/reality.pdf))


### For equivariant cohomology

In [[equivariant cohomology]]:


For [[finite groups]]

* [[Steven Costenoble]], [[Stefan Waner]], _Equivariant Poincar&#233; duality_, Michigan Math. J. 39 (1992), no. 2, 325&#8211;351

For [[compact Lie groups]]

* [[Michel Brion]], _Poincar&#233; duality and equivariant (co)homology_, Michigan mathematical journal, Volume 48, Issue 1 (2000), 1-624 ([EUCLID](http://projecteuclid.org/euclid.mmj/1030132709))

* [[Steven Costenoble]], [[Stefan Waner]], _Equivariant ordinary homology and cohomology_ ([arXiv:math/0310237](http://arxiv.org/abs/math/0310237))

* Christopher Allday, Matthias Franz, [[Volker Puppe]], _Equivariant Poincar&#233;-Alexander-Lefschetz duality and the Cohen-Macaulay property_ ([arXiv:1303.1146](http://arxiv.org/abs/1303.1146))

In [[equivariant K-theory]]:

* {#Tu06} [[Jean-Louis Tu]], _Twisted K-theory and Poincare duality_ ([arXiv:0609556](http://arxiv.org/abs/math/0609556))

* [[Heath Emerson]], [[Ralf Meyer]], _Dualities in equivariant Kasparov theory_, New York J. Math. 16 (2010), 245-313 ([arXiv:0711.0025](http://arxiv.org/abs/0711.0025))

* [[Heath Emerson]], _Duality, correspondences and the Lefschetz map in equivariant KK-theory: a survey_ ([arXiv:0904.4744](http://arxiv-web3.library.cornell.edu/abs/0904.4744))


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

### For spaces in higher geometry

Poincar&#233; duality on [[Deligne-Mumford stacks]]/[[orbifolds]] is discussed in 

* Dan Abramovich, Tom Graber, [[Angelo Vistoli]], _Gromov-Witten theory of Deligne-Mumford stacks_ ([arXiv:math/0603151](http://arxiv.org/abs/math/0603151))

* Weimin Chen, [[Yongbin Ruan]], _A New Cohomology Theory for Orbifold_, Commun. Math. Phys. 248 (2004) 1-31 ([arXiv:math/0004129](http://arxiv.org/abs/math/0004129))

For disucssion in [[noncommutative topology]]/[[KK-theory]] see at _[[Poincaré duality algebra]]_.

### On the level of chains

Poincar&#233; duality is traditional considered on the level of [[cohomology groups]]. One may asks if it lifts to a duality on the underlying [[chain complexes]]. 

Such "derived" Poincar&#233; duality on the level of chain complexes is claimed in theorem 2.5.2 of 

* Eric J. Malm, _String topology and the based loop space_ ([arXiv:1103.6198](http://arxiv.org/abs/1103.6198))
 {#EM11}

based on -- or at least inspired by -- the discussion in (section 10) of 

* [[William Dwyer]], [[John Greenlees]], S. Iyengar, _Duality in algebra and topology_ ([arXiv:math/0510247](http://arxiv.org/abs/math/0510247))

The article

* [[Thomas Tradler]], [[Mahmoud Zeinalian]], [[Dennis Sullivan]], _Infinity Structure of Poincare Duality Spaces_ ([arXiv:math/0309455](http://arxiv.org/abs/math/0309455))

claims a chain duality (even of $A_\infty$-comodule chains but then possibly only exhibited by a [[bimodule]]) for the [[singular chain complex]] of any Poincar&#233; duality topological space.

A review is in 

* [[Thomas Tradler]], _Infinity inner products on A-infinity algebras_ ([arXiv:0806.0065](http://arxiv.org/abs/0806.0065))




[[!redirects Poincare duality]]
[[!redirects Poincaré duality]]
[[!redirects Poincar%C3%A9 duality]]
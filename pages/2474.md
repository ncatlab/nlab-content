
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Noncommutative geometry
+-- {: .hide}
[[!include noncommutative geometry - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

### Abstract $C^\ast$-algebras

+-- {: .num_defn}
###### Definition

A $C^*$-algebra is a [[Banach algebra]] $(A, {\|-\|})$ over a [[topological field]] $K$ (often the field $K \coloneqq \mathbb{C}$ of [[complex numbers]]) equipped with an [[involution]] $(-)^\ast$ compatible with [[complex conjugation]] if appropriate (that is: a Banach [[star-algebra]]) that satisfies the __$C^*$-identity__
$$ 
  {\|{A^* A}\|} = {\|{A^*}\|} \, {\|{A}\|} 
$$
or equivalently the __$B^*$-identity__
$$ 
  {\|{A^* A}\|} = {\|{A}\|^2} 
  \,.
$$

A [[homomorphism]] of $C^\ast$-algebras is a map that preserves all this structure. For this it is sufficient for it to be a [[star-algebra]] homomorphisms.

$C^\ast$-algebras with these homomorphisms form a [[category]] [[C*Alg]].

=--

+-- {: .num_remark}
###### Remark

Often one sees the definition without the clause (which should be in the definition of Banach $*$-algebra) that the involution is an [[isometry]] (so that ${\|A^*\|} = {\|A\|}$, which is key for the equivalence of the $B^*$ and $C^*$ identities).  This follows easily from the $B^*$-identity, while it follows from the $C^*$-identity after some difficulty.
=--

+-- {: .num_remark}
###### Remark

There are different concepts for the [[tensor product]] of $C^*$-algebras, see for example at _[[spatial tensor product]]_.

=--

+-- {: .num_remark}
###### Remark

$C^*$-algebras equipped with the [[action]] of a [[group]] by [[automorphisms]] of the algebra are called _[[C-star-systems]]_ .

=--
### Concrete $C^\ast$-algebras and $C^\ast$-representations

+-- {: .num_defn}
###### Definition

Given a [[complex numbers|complex]] [[Hilbert space]] $H$, a __[[concrete structure|concrete]] $C^*$-algebra__ on $H$ is a $*$-[[subalgebra]] of the algebra of [[bounded operators]] on $H$ that is [[closed subspace|closed]] in the [[norm topology]].  

=--

+-- {: .num_defn}
###### Definition

A __[[representation of a C-star algebra|representation]]__ of a $C^*$-algebra $A$ on a [[Hilbert space]] $H$ is a $*$-homomorphism from $A$ to the algebra of [[bounded operators]] on $H$.

=--

+-- {: .num_remark}
###### Remark

It is immediate that concrete $C^*$-algebras correspond precisely to [[faithful representations]] of abstract $C^*$-algebras.  It is an important theorem that *every* $C^*$-algebra has a faithful representation; that is, every abstract $C^*$-algebra is [[isomorphism|isomorphic]] to a concrete $C^*$-algebra.

=--

+-- {: .num_remark}
###### Remark

The original definition of the term '$C^*$-algebra' was in fact the concrete notion; the 'C' stood for 'closed'.  Furthermore, the original term for the abstract notion was '$B^*$-algebra' (where the 'B' stood for 'Banach').  However, we now usually interpret '$C^*$-algebra' abstractly.  (Compare '$W^*$-algebra' and '[[von Neumann algebra]]'.)

=--


### In $\dagger$-compact categories {#DaggerFormulation}

The notion of $C^*$-algebra can be abstracted to the general context of [[symmetric monoidal †-categories]], which serves to illuminate their role in _[[quantum mechanics in terms of †-compact categories]]_.

For a discussion of this in the finite-dimensional case see for instance ([Vicary](#Vicary)).


## Properties
 {#Properties}

$C^*$-algebras are [[monadic]] over sets. 
More precisely, the forgetful functor $\mathbf{C^*Alg}\to\mathbf{Set}$ that assigns to each algebra the set of points in its unit ball is monadic. See J Wick Pelletier & J Rosicky, On the equational theory of $C^*$-algebras, Algebra Universalis 30:275-284, 1993.

See also [[operator algebras]].


### Gelfand-Naimark theorem

The _[[Gelfand-Naimark theorem]]_ says that every [[C*-algebra]] is [[isomorphism|isomorphic]] to a $C^\ast$-algebra of [[bounded linear operators]] on a [[Hilbert space]].  In other words, every abstract $C^*$-algebra may be made into a concrete $C^*$-algebra.


### Gelfand-Naimark-Segal construction

The [[Gelfand-Naimark-Segal construction]] ([[GNS construction]]) establishes a correspondence between cyclic $*$-[[representation]]s of $C^*$-[[C*-algebra|algebras]] and certain linear functionals (usually called _[[state on an operator algebra|states]]_) on those same $C^*$-algebras.  The correspondence comes about from an explicit construction of the [[star-representation|*-representation]] from one of the [[linear functionals|linear functionals]] (states).


### Gelfand duality

[[Gelfand duality]] says that every ([[unital algebra|unital]]) _[[commutative C-star-algebra|commutative]]_ $C^*$-algebra over the [[complex numbers]] is that of complex-valued [[continuous functions]] from some [[compactum|compact Hausdorff topological space]]: there is an [[equivalence of categories]] $C^* CAlg \simeq $ [[Top]]${}_{cpt}$.

Accordingly one may think of the study of non-commutative $C^\ast$-algebras as _[[non-commutative topology]]_.


### General
 {#General}

+-- {: .num_prop}
###### Proposition

For $A$ and $B$ two $C^\ast$-algebras and $f : A \to B$
a [[star-algebra]] [[homomorphism]] the set-theoretic [[image]]
$f(A) \subset B$ is a $C^\ast$-subalgebra of $B$, hence is also the 
[[image]] of $f$ in $C^\ast Alg$.

=--

This is ([KadisonRingrose, theorem 4.1.9](#KadisonRingrose)).

+-- {: .num_cor}
###### Corollary

There is a [[functor]]

$$
  \mathcal{C} : C^\ast Alg \to Poset
$$

to the [[category]] [[Poset]] of [[posets]], which sends each $A \in C^\ast Alg$
to its [[poset of commutative subalgebras]] $\mathcal{C}(A)$ 
and sends each morphism $f : A \to B$ to the [[functor]]
$\mathcal{C}(f) : \mathcal{C}(A) \to \mathcal{C}(B)$ which
sends a [[commutative C-star-algebra|commutative]] subalgebra $C \subset A$ to $f(C) \subset B$.

=--


### Construction as groupoid convolution algebras

Many $C^\ast$-algebras arise as [[groupoid algebras]] of [[Lie groupoids]]. See at _[groupoid algebra - References - For smooth geometry](category+algebra#ReferencesForSmoothGeometry)_


### Homotopy theory

There is [[homotopy theory]] of $C^\ast$-algebras, being a non-commutative generalization of that of [[Top]]. 
(e.g. [Uuye 12](#Uuye)). For more see at _[[homotopical structure on C*-algebras]]_.


## Examples

+-- {: .num_example}
###### Example

Any algebra $M_n(A)$ of [[matrices]] with [[coefficients]] in a $C^\ast$-algebra is again a $C^\ast$-algebra. In particular $M_n(\mathbb{C})$ is a $C^\ast$-algebra for all $n \in \mathbb{N}$.

=--

+-- {: .num_example}
###### Example

For $A$ a $C^\ast$-algebra and for $X$ a [[locally compact topological space|locally compact]] [[Hausdorff topological space]], the set of [[continuous functions]] $X \to A$ which [[vanish at infinity]] is again a $C^\ast$-algebra by extending all operations pointwise.
(This algebra is [[unital algebra|unital]] precisely if $A$ is and if $X$ is a [[compact topological space]].)

This algebra is denoted 

$$
  C_0(X,A) \in C^\ast Alg
  \,.
$$ 

If $A = \mathbb{C}$ then one usually just writes 

$$
  C_0(X) \coloneqq C_0(X, \mathbb{C})
  \,.
$$

This are the $C^\ast$-algebras to which the [[Gelfand duality]] theorem applies.

=--

+-- {: .num_example}
###### Example

A [[uniformly hyperfinite algebra]] is in particular a $C^\ast$-algebra, by definition.

=--

+-- {: .num_example}
###### Example

A [[von Neumann algebra]] is in particular a $C^\ast$-algebra, by definition.

=--


## Related concepts

* [[commutative C-star-algebra]], [[Gelfand duality]], [[noncommutative topology]]

* [[separable C*-algebra]], [[homogeneous C*-algebra]]

* [[nuclear C*-algebra]]

* [[unitisation of C*-algebras]]

* [[von Neumann algebra]], [[enveloping von Neumann algebra]]

* [[JB-algebra]], [[JLB-algebra]]

* [[dense subalgebra]], [[F-star-algebra]]

* [[multiplier algebra]]

* [[graded C*-algebra]]

* [[tensor product of C*-algebras]]

* [[crossed product C*-algebra]]

* [[Cuntz algebra]]

* [[Poincaré duality C*-algebra]]

* [[Hilbert C*-module]], [[Hilbert C*-bimodule]], [[amplimorphism]]

* [[C*-category]]

* [[C*-coalgebra]], [[Hopf C*-algebra]]

* [[continuous field of C*-algebras]]

* [[homotopical structure on C*-algebras]]

  * [[asymptotic C*-homomorphism]], [[l.m.c.-C*-algebra]]

  * [[KK-theory]], [[E-theory]]

* [[AQFT]]

  * [[state on an operator algebra]]


## References

Textbook accounts:

* [[Gerard Murphy]], _$C^\ast$-algebras and Operator Theory_, Academic Press 1990 ([doi:10.1016/C2009-0-22289-6](https://doi.org/10.1016/C2009-0-22289-6))


* {#KadisonRingrose} Richard Kadison, John Ringrose, chapter 4 in volume 1 of: _Fundamentals of the theory of operator algebras_ Academic Press, (1983)
 


An exposition that explicitly gives [[Gelfand duality]] as an [[equivalence of categories]] and introduces all the notions of [[category theory]] necessary for this statement is in

* Ivo Dell'Ambrogio, _Categories of $C^\ast$-algebras_ ([pdf](http://www.math.ethz.ch/u/ambrogio/exercise_C_-algebras.pdf))

For [[operator algebra]]-theory see there and see

* [[Stanisław Woronowicz]], _Unbounded elements affiliated with $C^\ast$-algebras and
non-compact quantum groups. Commun. Math. Phys. 136, 399&#8211;432 (1991)

* [[Stanisław Woronowicz]], K. Napi&#243;rkowski, _[[Operator theory in the C*-algebra framework]]_, Reports on Mathematical Physics Volume 31, Issue 3, June 1992, Pages 353&#8211;371 ([publisher](http://www.sciencedirect.com/science/article/pii/003448779290025V), [pdf](http://www.fuw.edu.pl/~slworono/PDF-y/OP.pdf))


A characterizations of injections of commutative sub-$C^*$-algebras -- hence of the [[poset of commutative subalgebras]] of a $C^*$-algebra -- is in

* [[Chris Heunen]], _Characterizations of categories of commutative $C^*$-algebras_ ([arXiv:1106.5942](http://arxiv.org/abs/1106.5942))

General properties of the [[category]] of $C^\ast$-algebras are discussed in 

* [[Ralf Meyer]], _Categorical aspects of bivariant K-theory_, ([arXiv:math/0702145](http://arxiv.org/abs/math/0702145))
 {#Meyer}

Specifically [[pullback]] and [[pushout]] of $C^\ast$-algebras is discussed in 

* Gerd Petersen, _Pullback and pushout constructions in $C^\ast$-algebra theory_ ([pdf](http://www.math.ru.nl/~mueger/ped2.pdf))


The [[homotopy theory]] of $C^\ast$-algebras (a [[category of fibrant objects]]-structure on $C^\ast Alg$) is discussed in

* Otgonbayar Uuye, _Homotopy theory for $C^\ast$-algebras_ ([arXiv:1011.2926](http://arxiv.org/abs/1011.2926))
 {#Uuye}

For more along such lines see the references at _[[KK-theory]]_ and _[[E-theory]]_.


[[!redirects C-star-algebra]]
[[!redirects C-star-algebras]]
[[!redirects C-star algebra]]
[[!redirects C-star algebras]]
[[!redirects C*-algebra]]
[[!redirects C* algebra]]
[[!redirects C*-algebras]]
[[!redirects C* algebras]]
[[!redirects C-*-algebra]]
[[!redirects C-* algebra]]
[[!redirects C-*-algebras]]
[[!redirects C-* algebras]]
[[!redirects B-star-algebra]]
[[!redirects B-star-algebras]]
[[!redirects B-star algebra]]
[[!redirects B-star algebras]]
[[!redirects B*-algebra]]
[[!redirects B* algebra]]
[[!redirects B*-algebras]]
[[!redirects B* algebras]]
[[!redirects B-*-algebra]]
[[!redirects B-* algebra]]
[[!redirects B-*-algebras]]
[[!redirects B-* algebras]]

[[!redirects C*-identity]]
[[!redirects B*-identity]]

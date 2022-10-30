
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
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

### Abstract $C^\ast$-algebras

+-- {: .num_defn}
###### Definition

A $C^*$-algebra is a [[Banach algebra]] $(A, {\|-\|})$ over a [[topological field]] $K$ (often the field $K \coloneqq \mathbb{C}$ of [[complex numbers]]) equipped with an [[involution]] $(-)^\ast$ compatible with [[complex conjugation]] if appropriate (that is: a Banach [[star-algebra]]) that satisfies the _$C^*$-identity_
$$ 
  {\|{A^* A}\|} = {\|{A^*}\|} \, {\|{A}\|} 
$$
or equivalently the _$B^*$-identity_
$$ 
  {\|{A^* A}\|} = {\|{A}\|^2} 
  \,.
$$

A [[homomorphism]] of $C^\ast$-algebras is a map that preserves all this structure. For this it is sufficient for it to be a [[star-algebra]] homomorphisms.

$C^\ast$-algebras with these homomorphisms form a [[category]] [[C*Alg]].

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

The original definition of the term '$C^*$-algebra' was in fact the concrete notion; the 'C' stood for 'closed'.  Furthermore, the original term for the abstract notion was '$B^*$-algebra'.  However, we now usually interpret '$C^*$-algebra' abstractly.  (Compare '$W^*$-algebra' and '[[von Neumann algebra]]'.)

=--


### In $\dagger$-compact categories {#DaggerFormulation}

The notion of $C^*$-algebra can be abstracted to the general context of [[symmetric monoidal †-categories]], which serves to illuminate their role in _[[quantum mechanics in terms of †-compact categories]]_.

For a discussion of this in the finite-dimensional case see for instance ([Vicary](#Vicary)).


## Properties
 {#Properties}

See also [[operator algebras]].


### GNS construction

The [[GNS construction]] shows that every abstract $C^*$-algebra over the [[complex numbers]] as a concrete $C^*$-algebra: a subalgebra of an algebra of [[bounded operator]]s on some [[Hilbert space]].


### Gelfand duality

[[Gelfand duality]] says that every (unital) _[[commutative C-star-algebra|commutative]]_ $C^*$-algebra over the [[complex numbers]] is that of complex-valued [[continuous functions]] from some [[compactum|compact Hausdorff topological space]]: there is an [[equivalence of categories]] $C^* CAlg_{com} \simeq $ [[Top]]${}_{cpt}$.

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

There is [[homotopy theory]] of $C^\ast$-algebras, being a non-commutative generalization of that of [[Top]]. See for instance ([Uuye 12](#Uuye)).


## Examples

* [[matrix]] algebras;

* [[uniformly hyperfinite algebra]]

* [[von Neumann algebra]]


## Related concepts

* [[commutative C-star-algebra]]

* [[C-star-category]]

* [[Hopf C-star-algebra]]

* [[C-star coalgebra]]

* [[nuclear C*-algebra]]

* [[von Neumann algebra]]

* [[Jordan-Lie-Banach algebra]]

* [[dense subalgebra]], [[F-star-algebra]]


* [[Hilbert C-star-module]], [[Hilbert bimodule]], [[KK-theory]]

* [[state on an operator algebra]]

* [[AQFT]]


## References

A standard textbook reference is chapter 4 in volume 1 of 

* Richard Kadison, John Ringrose, _Fundamentals of the theory of operator algebras_ Academic Press, (1983)
 {#KadisonRingrose}

See also the references at _[[operator algebras]]_.

An exposition that explicitly gives [[Gelfand duality]] as an [[equivalence of categories]] and introduces all the notions of [[category theory]] necessary for this statement is in

* Ivo Dell'Ambrogio, _Categories of $C^\ast$-algebras_ ([pdf](http://www.math.ethz.ch/u/ambrogio/exercise_C_-algebras.pdf))

A characterizations of injections of commutative sub-$C^*$-algebras -- hence of the [[poset of commutative subalgebras]] of a $C^*$-algebra -- is in

* [[Chris Heunen]], _Characterizations of categories of commutative $C^*$-algebras_ ([arXiv:1106.5942](http://arxiv.org/abs/1106.5942))

Properties of the [[category]] of $C^\ast$-algebras are discussed in 

* [[Ralf Meyer]], _Categorical aspects of bivariant K-theory_, ([arXiv:math/0702145](http://arxiv.org/abs/math/0702145))
 {#Meyer}


Homotopy theory of $C^\ast$-algebras (a [[category of fibrant objects]]-structure on $C^\ast Alg$) is discussed in

* Otgonbayar Uuye, _Homotopy theory for $C^\ast$-algebras_ ([arXiv:1011.2926](http://arxiv.org/abs/1011.2926))


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

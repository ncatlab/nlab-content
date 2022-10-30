
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

A **Poisson algebra** is

* a [[module]] $A$ over some [[field]] or other [[commutative ring]] $k$,

* equipped with the structure ${\cdot}\colon A \otimes_k A \to A$ of a commutative [[associative algebra]];

* and equipped with the bracket $[-,-]\colon A \otimes_k A \to A$ of a [[Lie algebra]];

* such that for every $a \in A$ we have that $[a,-]\colon A \to A$ is a [[derivation]] of $(A,\cdot)$.

=--

The definition makes sense, but is not standardly used, also for the more general case when the product $\cdot$ is not necessarily commutative (it is often however taken in the sense of commutative internally to a symmetric monoidal category, say of chain complexes, graded vector spaces or supervector spaces). 

+-- {: .num_defn}
###### Definition

The [[opposite category]] of that of (commutative) real Poisson algebras can be identified with the category of **[[classical mechanical systems]]**

$$
  ClassMechSys := CPoiss^{op}
  \,.
$$ 

See there for more details.

=--

+-- {: .num_example}
###### Example

For $(X, \{-,-\})$ a [[Poisson manifold]] or $(X, \omega)$ a [[symplectic manifold]], the algebra of [[smooth function]]s $C^\infty(X, \mathbb{R})$ is naturally a Poisson algebra, thus may be regarded as an object in $ClassMechSys$. For classical mechanical systems of this form, we say that the [[manifold]] $X$ is the [[phase space]] of the system.

Generally, therefore, for $(A, \cdot,[-,-])$ a Poisson algebra, we may regard it as a formal dual to some generalized Phase space.

=--

+-- {: .num_remark}
###### Remark

For $(A, \cdot, \{-,-\})$ a Poisson algebra, $A$ together with its [[module]] $\Omega^1(A)$ of [[Kähler differential]]s naturally form a [[Lie-Rinehart pair]], with bracket given by

$$
  [d a, d b ] := d \{a,b\}
  \,.
$$

If the Poisson algebra comes from a [[Poisson manifold]] $X$, then this Lie-Rinehart pair is the [[Chevalley-Eilenberg algebra]] of the given [[Poisson Lie algebroid]] over $X$. We can therefore identify classical mechanical systems over a phase space manifold also with Poisson Lie algebroids. 

=--

## Examples

### For a symplectic manifold
 {#FromSymplecticManifold}

+-- {: .num_defn}
###### Definition

A [[symplectic manifold]] $(X, \omega)$
canonically is a [[Poisson manifold]] $(X; \{-,-\})$ by 
defining the Poisson bracket as follows.

By the symplectic structure, 
to every [[smooth function]] $f \in C^\infty(X)$
is associated the correspinding [[Hamiltonian vector field]]
$v_f \in \Gamma(T X)$, defined, uniquely, by the equation

$$
  d_{dR} f = \iota_{v_f} \omega
  \,.
$$

In terms of this, the Poisson bracket is given by

$$
  \{f,g\} := \iota_{v_g} \iota_{v_f} \omega
  \,.
$$

=--

## Properties

### For a symplectic manifold

Let $(X, \omega)$ be a [[symplectic manifold]],
and $(X, \{-,-\})$ the corresponding [[Poisson manifold]]
as [above](FromSymplecticManifold). 

Write
$\mathcal{P} := (C^\infty(X), \{-,-\})$ for the [[Lie algebra]]
underlying the Poisson algebra.

+-- {: .num_prop}
###### Proposition

This fits into a [[central extension]] of Lie algebras

$$
  \mathbb{T} \to \mathcal{P} \to Ham(X)
  \,,
$$

where $Ham(X) \subset \Gamma(T X)$ is the sub-Lie algebra of [[vector fields]] on the [[Hamiltonian vector fields]].

=--

+-- {: .proof}
###### Proof

Observe that the [[Hamiltonian]] function associated to a 
[[Hamiltonian vector field]] is well-defined only up to addition of 
a constant function.

=--

This is also called the **Kostant-Souriau central extension** 
(see [Kostant 1970](#Kostant)). 

## Related concepts

*  A __[[Poisson manifold]]__ is a [[smooth manifold]] whose associatve algebra of [[smooth function]]s with values in the [[real line]] $\mathbb{R}$ that is equipped with the structure of a Poisson algebra (over $\mathbb{R}$).

* A [[Poisson n-algebra]] is a Poisson algebra in chain complexes with a bracket of degree $1-n$.

  *  A [[Gerstenhaber algebra]] is a Poisson 2-algebra.

* A [[Coisson algebra]] is essentially a Poisson algebra [[internalization|internal to]] [[D-module]]s.

* A [[Jordan-Lie-Banach algebra]] is a non-associative (quantum) Poisson algebra.

## References

* [[Yvette Kosmann-Schwarzbach]],  _Poisson algebra_, article in _Encyclopedia of mathematics_, ([pdf](http://www.math.polytechnique.fr/~kosmann/palg.pdf))

* [[Klaas Landsman]], _[[Mathematical Topics Between Classical and Quantum Mechanics]]_

* N. Chriss, [[Victor Ginzburg]], _Complex geometry and representation theory_

* [[Peter Olver]], _Equivalence, invariants, and symmetry_, Cambridge Univ. Press 1995

* [[Bertram Kostant]], _Quantization and unitary representations. I. Prequantization_, In Lectures in Modern Analysis and Applications, III, pages 87&#8211;208. Lecture Notes in Math., Vol. 170. Springer, Berlin (1970)
 {#Kostant}

[[!redirects Poisson algebra]]
[[!redirects Poisson algebras]]

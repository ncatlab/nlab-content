
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

+-- {: .un_defn}
###### Definition

A **Poisson algebra** is

* a [[module]] $A$ over some [[field]] or other [[commutative ring]] $k$,

* equipped with the structure ${\cdot}\colon A \otimes_k A \to A$ of an [[associative algebra]];

* and equipped with the structure $[-,-]\colon A \otimes_k A \to A$ of a [[Lie algebra]];

* such that for every $a \in A$ we have that $[a,-]\colon A \to A$ is a [[derivation]] of $(A,\cdot)$.

=--

+-- {: .num_defn}
###### Definition

The [[opposite category]] of that of commutative real Poisson algebras can be identified with the category of **[[classical mechanical systems]]**

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




## Related concepts

*  A __[[Poisson manifold]]__ is a [[smooth manifold]] whose associatve algebra of [[smooth function]]s with values in the [[real line]] $\mathbb{R}$ that is equipped with the structure of a Poisson algebra (over $\mathbb{R}$).

* A [[Poisson n-algebra]] is a Poisson algebra in chain complexes with a bracket of degree $1-n$.

  *  A [[Gerstenhaber algebra]] is a Poisson 2-algebra.


## References

* Encyclopedia of mathematics _Poisson algebra_ ([pdf](http://www.math.polytechnique.fr/~kosmann/palg.pdf))

[[!redirects Poisson algebra]]
[[!redirects Poisson algebras]]

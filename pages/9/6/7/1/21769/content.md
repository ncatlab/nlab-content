
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

$FinRel$ is the [[category]] of [[finite set]]s and all [[relation]]s between them: the [[full subcategory]] of [[Rel]] on finite sets.  

## As a category of matrices

$FinRel$ is isomorphic to $Mat(Bool)$, the category where the objects are natural numbers and a morphism $f : m \to n$ is an $n \times m$ matrix with entries in the [[semiring]] of booleans, $Bool = \{F,T\}$, where addition is the logical operation "or" and multiplication is "and".  For any semiring $R$, the category $Mat(R)$ has [[biproducts]], corresponding to addition of natural numbers, and the initial object $0$ is also terminal.  For any commutative semiring $R$, $Mat(R)$ also has another symmetric monoidal structure, a tensor product with $m \otimes n = m n$, which distributes over biproducts.  Thus FinRel has all these properties.   

## As a PROP

We can define [[bimonoid]] objects in any symmetric monoidal category, and a bimonoid object is said to be **special** if comultiplication followed by multiplication is the identity.   $FinRel$ made symmetric monoidal with biproducts is the free symmetric monoidal category on a special bicommutative bimonoid object.  That is, given a symmetric monoidal category $C$ and a special bicommutative bimonoid object $c \in C$, there is symmetric monoidal functor $F: FinRel \to C$, unique up to monoidal natural isomorphism, mapping $1 \in FinRel$ together with its bimonoid operations to $c$ and its bimonoid operations.

This is conveniently expressed in the language of [[PROP]]s: $Mat(Bool)$ is the PROP for special bicommutative bimonoids.   This is Theorem 7.2 in Coya and Fong.


## References

* Brandon Coya and [[Brendan Fong]], _Corelations are the prop for extraspecial commutative Frobenius monoids_, Theory and Applications of Categories, Vol. 32, 2017, No. 11, pp. 380-395.   ([arxiv](https://arxiv.org/abs/1601.02307))

category: category


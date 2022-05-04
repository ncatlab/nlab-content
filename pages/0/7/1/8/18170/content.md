
#Contents#
* table of contents
{:toc}

## Idea

A __decimal rational number__ or __decimal fraction__ is a [[rational number]] $r \in \mathbb{Q}$ such that the [[binary number|binary]] expansion of $r$ has finitely many digits. 

## Definition

### As a subset of the rational numbers

A __decimal rational number__ or __decimal fraction__ is a [[rational number]] $r \in \mathbb{Q}$ such that there exists $n \in \mathbb{N}$ and $a \in \mathbb{Z}$ such that $r = \frac{a}{2^n}$.

### As the localisation of the integers at 2

The [[commutative ring]] of decimal rational numbers $\mathbb{Z}[1/2]$ is the [[localization of a commutative ring|localization]] of the [[integers]] $\mathbb{Z}$ [[localisation of a commutative ring away from an element|away from]] $2$.

### As an initial object of a category

For lack of a better name, let us define a *dyadic rational number algebra* to be a set $A$ with a function $\iota \in \mathbb{Z} \times \mathbb{N} \to A$ with domain the Cartesian product $\mathbb{Z} \times \mathbb{N}$ and codomain $A$, such that 

$$\forall a \in \mathbb{Z}. \forall b \in \mathbb{N}. \forall c \in \mathbb{Z}. \forall d \in \mathbb{N}. (a \cdot 2^d = c \cdot 2^b) \implies (\iota(a, b) = \iota(c, d))$$

A *dyadic rational number algebra homomorphism* between two dyadic rational number algebras $A$ and $B$ is a function $f \in B^A$ such that 

$$\forall a \in \mathbb{Z}. \forall b \in \mathbb{N}. f(\iota_A(a, b)) = \iota_B(a, b)$$

The *category of dyadic rational number algebras* is the category $DRNA$ whose objects $Ob(DRNA)$ are dyadic rational number algebras and whose morphisms $Mor(DRNA)$ are dyadic rational number algebra homomorphisms. The set of **dyadic rational numbers**, denoted $\mathbb{Z}[1/2]$, is defined as the initial object in the category of dyadic rational number algebras. 

## Related entries

* [[decimal rational number]]

* [[Urysohn's lemma]]

* [[symmetric midpoint algebra]]

* [[dyadic rational module]]

* [[dyadic rational algebra]]

## References

* Wikipedia, _[Dyadic rational](https://en.wikipedia.org/wiki/Dyadic_rational)_

[[!redirects dyadic rational numbers]]

[[!redirects dyadic rational]]
[[!redirects dyadic rationals]]

[[!redirects dyadic number]]
[[!redirects dyadic numbers]]
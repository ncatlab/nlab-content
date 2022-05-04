
#Contents#
* table of contents
{:toc}

## Idea

A __dyadic rational number__ is a [[rational number]] $r \in \mathbb{Q}$ such that the [[binary number|binary]] expansion of $r$ has finitely many digits. 

## Definition

### As a subset of the rational numbers

A __dyadic rational number__ is a [[rational number]] $r \in \mathbb{Q}$ such that there exists $n \in \mathbb{N}$ and $a \in \mathbb{Z}$ such that $r = \frac{a}{2^n}$.

### As the localisation of the integers at 2

The [[commutative ring]] of dyadic rational numbers $\mathbb{Z}[1/2]$ is the [[localization of a commutative ring|localization]] of the [[integers]] $\mathbb{Z}$ [[localisation of a commutative ring away from an element|away from]] $2$.

### As an initial object of a category

For lack of a better name, let us define a *set with dyadic rational numbers* to be a set $A$ with a function $\iota \in \mathbb{Z} \times \mathbb{N} \to A$, such that 

$$\forall a \in \mathbb{Z}. \forall b \in \mathbb{N}. \forall c \in \mathbb{Z}. \forall d \in \mathbb{N}. (a \cdot 2^d = c \cdot 2^b) \implies (\iota(a, b) = \iota(c, d))$$

The integer $a:\mathbb{Z}$ represents the integer if one ignores the separator in the [[binary number|binary numeral representation]] of the dyadic rational number, and the natural number $b:\mathbb{N}$ represents the number of digits to the left of the final digit where the separator ought to be placed after in the binary numeral representation of the dyadic rational number.  The axiom above is used to state that equivalent numeral representations are equal: i.e. 1.00 = 1.000 with binary numeral representations. 

A *homomorphism of sets with dyadic rational numbers* between two sets with dyadic rational numbers $A$ and $B$ is a function $f:A \to B$ such that 

$$\forall a \in \mathbb{Z}. \forall b \in \mathbb{N}. f(\iota_A(a, b)) = \iota_B(a, b)$$

The *category of sets with dyadic rational numbers* is the category $SwDRN$ whose objects $Ob(SwDF)$ are sets with dyadic rational numbers and whose morphisms $Mor(A,B)$ for sets with dyadic rational numbers $A \in Ob(SwDRN)$, $B \in Ob(SwDRN)$ are homomorphisms of sets with dyadic rational numbers. The set of **dyadic rational number**, denoted $\mathbb{Z}[1/2]$, is defined as the initial object in the category of sets with dyadic rational number. 

## Properties 

### Algebraic closure

The [[algebraic closure]] $\overline{\mathbb{Z}[1/2]}$ of the dyadic rational numbers is called the [[field]] of _[[algebraic numbers]]_, and is thus isomorphic to \overline{\mathbb{Q}}, the algebraic closure of the [[rational numbers]]. 

### Topologies

There are several interesting [[topological space|topologies]] on $\mathbb{Z}[1/2]$ that make $\mathbb{Z}[1/2]$ into a [[topological group]] under addition, allowing us to define interesting fields by taking the [[complete space|completion]] with respect to this topology:

1.  The _[[discrete topology]]_ is the most obvious, which is already complete.

2.  The _absolute-value topology_ is defined by the [[metric space|metric]] $d(x,y) \coloneqq {|x - y|}$; the completion is the field of [[real numbers]]. 

    (This topology is [[totally disconnected space|totally disconnected]].)

3.  The _$2$-adic topology_ is defined by the [[ultrametric]] $d(x,y) \coloneqq 1/n$ where $n$ is the highest exponent on $2$ in the [[prime factorization]] of ${|x - y|}$; the completions of each metric are the fields of $2$-[[adic number|adic numbers]].

## Related entries

* [[decimal rational number]]

* [[Urysohn's lemma]]

* [[symmetric midpoint algebra]]

* [[dyadic rational module]]

* [[dyadic rational algebra]]

* [[dyadic interval coalgebra]]

## References

* Wikipedia, _[Dyadic rational](https://en.wikipedia.org/wiki/Dyadic_rational)_

[[!redirects dyadic rational numbers]]

[[!redirects dyadic rational]]
[[!redirects dyadic rationals]]

[[!redirects dyadic number]]
[[!redirects dyadic numbers]]
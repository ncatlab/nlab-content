+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition ##

### In commutative rings ###

#### Elementary defintion ####

For a [[commutative ring]] $R$, a **polynomial function** is a [[function]] $f:R \to R$ with a [[natural number]] $n \in \mathbb{N}$ and a function $a:[0, n] \to R$ from the set of natural numbers less than or equal to $n$ to $R$, such that for all $x \in R$, 

$$f(x) = \sum_{i:[0, n]} a(i) \cdot x^i$$

where $x^i$ is the $i$-th [[power function]] for multiplication. 

#### Structural definition ####

For a [[commutative ring]] $R$, let $R[\mathbb{1}]$ be [[generalized the|the]] [[free commutative algebra|free commutative $R$-algebra]] on the [[singleton]] $\mathbb{1}$ with element $0 \in \mathbb{1}$, with canonical function $x:\mathbb{1} \to R[\mathbb{1}]$, and let $R \to R$ be the [[function algebra]] of $R$, with [[identity function]] $id_R:R \to R$. Since both objects are commutative $R$-algebras there are canonical commutative [[ring homomorphisms]] $\alpha:R \to R[x]$ and $\beta:R \to (R \to R)$, and there exists a commutative ring homomorphism $i:R[\mathbb{1}] \to (R \to R)$ such that $i \circ \alpha = \beta$ and $i(x(0)) = id_R$. A **polynomial function** is a function $f:R \to R$ in the [[image]] of $i:R[\mathbb{1}] \to (R \to R)$. 

### In non-commutative algebras ###

For a [[commutative ring]] $R$ and a $R$-[[associative unital algebra|non-commutative algebra]] $A$, a $R$-**polynomial function** is a [[function]] $f:A \to A$ with a [[natural number]] $n \in \mathbb{N}$ and a function $a:[0, n] \to R$ from the set of natural numbers less than or equal to $n$ to $R$, such that for all $x \in A$, 

$$f(x) = \sum_{i:[0, n]} a(i) x^i$$

where $x^i$ is the $i$-th [[power function]] for the (non-commutative) multiplication. 

## See also 

* [[real polynomial function]]

* [[quadratic function]]

* [[rational zero theorem]]

* [[fundamental theorem of algebra]]

* [[polynomial]]

## References

* Wikipedia, _[Polynomial function](https://en.wikipedia.org/wiki/Polynomial_function)_

[[!redirects polynomial functions]]

[[!redirects polynomial map]]
[[!redirects polynomial maps]]
[[!redirects polynomial mapping]]
[[!redirects polynomial mappings]]
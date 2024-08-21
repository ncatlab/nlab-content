+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition ##

### In commutative rings ###

#### Without scalar coefficients ####

Let $R$ be a [[commutative ring]]. A **polynomial function** is a a [[function]] $f:R \to R$ such that 

* $f$ is in the image of the [[function]] $j:R^* \to (R \to R)$ from the [[free monoid]] $R^*$ on $R$, i.e. the set of lists of elements in $R$, to the [[function algebra]] $R \to R$, such that 

  * $j(\epsilon) = 0$, where $0$ is the zero function. 
  * for all $a \in R^*$ and $b \in R^*$, $j(a b) = j(a) + j(b) \cdot (-)^{\mathrm{len}(a)}$, where $(-)^n$ is the $n$-th power function for $n \in \mathbb{N}$
  * for all $r \in R$, $j(r) = c_r$, where $c_r$ is the constant function whose value is always $r$. 

* $f$ is in the image of the canonical [[ring homomorphism]] $i:R[x] \to (R \to R)$ from the polynomial ring in one indeterminant $R[x]$ to the [[function algebra]] $R \to R$, which takes constant polynomials in $R[x]$ to constant functions in $R \to R$ and the indeterminant $x$ in $R[x]$ to the identity function $\mathrm{id}_R$ in $R \to R$

#### With scalar coefficients ####

For a [[commutative ring]] $R$, a **polynomial function** is a [[function]] $f:R \to R$ with a [[natural number]] $n \in \mathbb{N}$ and a function $a:[0, n] \to R$ from the set of natural numbers less than or equal to $n$ to $R$, such that for all $x \in R$, 

$$f(x) = \sum_{i:[0, n]} a(i) \cdot x^i$$

where $x^i$ is the $i$-th [[power function]] for multiplication. 

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

* [[degree of a polynomial]]

## References

* Wikipedia, _[Polynomial function](https://en.wikipedia.org/wiki/Polynomial_function)_

[[!redirects polynomial functions]]

[[!redirects polynomial map]]
[[!redirects polynomial maps]]
[[!redirects polynomial mapping]]
[[!redirects polynomial mappings]]
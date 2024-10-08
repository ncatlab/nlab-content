
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In a [[category]] $C$ with [[biproducts]], [[morphisms]] between [[finite product|finite]] biproducts are naturally encoded in terms of arrays of morphisms between the [[direct sum|direct summands]] of the [[objects]]. The natural operations on  morphisms (addition, composition) correspond to the usual matrix calculus operations on these arrays. 

For the special case that $C =$ [[Vect]] this reproduces the standard matrix calculus of linear algebra.

## Rules

Let $f : X \to Y$ be a [[morphism]] in a [[category]] with [[biproducts]] where the objects $X$ and $Y$ are given as [[direct sums]]
$$
  X = \oplus_{j = 1}^m X_j
  \,,
  \;\;
  Y = \oplus_{i = 1}^n Y_i
  \,.
$$

Since a [[biproduct]] is both a [[product]] as well as a [[coproduct]], the morphism $f$ is fixed by all its compositions $f^i_j$ with the product projections $\pi^i : Y \to Y_i$ and the coproduct injections $\iota_j : X_j \to X$:

$$
  f^i_j
  :=
  X_j \stackrel{\iota_j}{\to}
  X \stackrel{f}{\to}
  Y \stackrel{\pi^i}{\to}
  Y_i
  \,.
$$

In **matrix calculus** one therefore writes

$$
  f := 
  \left(
    \array{
       f^1_1 & f^1_2 & \cdots & f^1_m
       \\
       \vdots & \vdots & \ddots & \vdots
       \\
       f^n_1 & f^n_2 & \cdots & f^n_m
    }
  \right)
  \,.
$$

With this notation one has the following rules for computation:

* matrix addition, where $f,g : X \to Y$,

  $$
    (f + g)^i_j = f^i_j + g^i_j
  $$


* matrix multiplication, where $f:X \to Y$, $g:Y \to Z$,

  $$
    (g \circ f)^i_j
    =
    \sum_k
     g^i_k \circ f^k_j
    \,,
  $$

where in each case the sum of morphisms is taken using the canonical [[enriched category|enrichment]] of $C$ in abelian [[monoids]] (as described at [[biproduct]]).


As can be seen in the above formulas, particularly for matrix multiplication, this is a context is which the [[Einstein summation convention]] can be used, with a distinction drawn between upper and lower indices.  Then repeated indices (in formulas with general applicability) will always appear once upper and once lower, summed over.  However, this convention can apply only to the morphisms, not to the objects.

## In dagger categories

If the category $C$ is in addition a [[dagger category]] with an obvious compatibility condition between the dagger operation $(-)^\dagger : C \to C$ and the biproduct structure, then the usual rules of computation for matrices over complex numbers have analogs in $C$.

* conjugation

  $$
    (f^\dagger)_{i j} =  (f_{j i})^\dagger
  $$

Here the distinction between upper and lower indices cannot be maintained, although it is still true that repeated indices will be summed in formulas with general applicability.

## Related concepts

* [[matrix analysis]]

* [[integral transform]]

## References

Historical origins:

* [[Arthur Cayley]]: *A Memoir on the Theory of Matrices*, Philosophical Transactions of the Royal Society of London, **148** (1858) 17-37 &lbrack;[jstor:108649](https://www.jstor.org/stable/108649)&rbrack;


Discussion in the generality of [[monoidal category|monoidal]] [[category theory]] is in

* [[John Harding]], section 2  of _[[matrixcalculus.pdf:file]]_


Formalization in terms of [[dependent linear type theory]] is in

* _[[schreiber:Type-semantics for quantization]]_ 

[[!redirects matrix multiplication]]

[[!redirects matrix product]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Gerstenhaber algebra_ is a [[Poisson n-algebra|Poisson 2-algebra]], a [[Poisson algebra]] in graded vector spaces with Poisson bracket of degree -1.

## Definition

+-- {: .un_defn}
###### Definition


A **Gerstenhaber algebra** is a [[chain complex]] $A$ equipped with

* a symmetric product $\cdot : A \otimes A \to A$;

* a skew-symmetric bracket $[-,-] : A \otimes A \to A[1]$;

* such that [[associativity]] of $\cdot$ and the [[Jacobi identity]] for $[-,-]$ holds and such that $[a,-]$ is a [[derivation]] of $\cdot$.

=--

## Properties

+-- {: .un_theorem}
###### Theorem

The [[homology]] of the  [[operad]] for Gerstenhaber algebras in [[chain complexes]] is the operad for Gerstenhaber algebras.

Accordingly the [[homology]] of a [[E2-algebra]] is a Gerstenhaber algebra.

=--

This is due to [Cohen (1976)](#Cohen).

+-- {: .un_remark}
###### Remark

A Gerstenhaber algebra equipped in addition with a certain morphism $\Delta : A \to A$ is a **[[BV-algebra]]**. This is the homology of an algebra over the [[framed little 2-disk operad]].

=--

## References

* Cohen (1976)
{#Cohen}

[[!redirects Gerstenhaber algebras]]

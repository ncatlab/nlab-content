

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

+-- {: .num_defn}
###### Definition


A **Gerstenhaber algebra** is a [[chain complex]] $A$ equipped with

* a symmetric product $\cdot : A \otimes A \to A$;

* a skew-symmetric bracket $[-,-] : A \otimes A \to A[1]$;

* such that [[associativity]] of $\cdot$ and the [[Jacobi identity]] for $[-,-]$ holds and such that $[a,-]$ is a [[derivation]] of $\cdot$.

=--

## Properties

+-- {: .num_theorem}
###### Theorem

The [[homology]] of the  [[operad]] for Gerstenhaber algebras in [[chain complexes]] is the operad for Gerstenhaber algebras.

Accordingly the [[homology]] of an [[E2-algebra]] is a Gerstenhaber algebra.

=--

This is due to [Cohen (1976)](#Cohen).

+-- {: .num_remark}
###### Remark

A Gerstenhaber algebra equipped in addition with a certain morphism $\Delta : A \to A$ is a **[[BV-algebra]]**. This is the homology of an algebra over the [[framed little 2-disk operad]].

=--

## Related concepts

* [[Poisson n-algebra]]

* [[BV-algebra]]

## References

* {#Cohen} Cohen (1976)
 
* [[Murray Gerstenhaber]], _The cohomology structure of an associative ring_, Ann. of Math., 78 (1963), 267-288 [MR28:5102](http://www.ams.org/mathscinet-getitem?mr=28:5102)

* [[Ping Xu]], _Gerstenhaber algebras and BV-algebras in Poisson geometry_, Commun. Math. Phys. 200, No.3, 545-560 (1999).

[[!redirects Gerstenhaber algebras]]
[[!redirects Poisson 2-algebra]]
[[!redirects Poisson 2-algebras]]

[[!redirects Gerstenhaber bracket]]

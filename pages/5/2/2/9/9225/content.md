
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _Beilinson-Drinfeld algebra_ (or _BD-algebra_ for short) is like a [[BV-algebra]] with nilpotent [[BV-operator]], but over [[formal power series]] in one formal parameter $\hbar$, and such that the [[Gerstenhaber algebra|Gerstenhaber bracket]] is proportional to that parameter. 

This means that one may think of a BD-algebra as an $\hbar$-parameterized formal family of algebras which for $\hbar = 0$ are [[Poisson 0-algebras]] and for $\hbar \neq 0$ they look superficially like [[BV-algebras]]. But see remark \ref{RoleOfTheDifferential} below.

Such BD-algbras are used to formalize [[formal deformation quantization]] in the context of the [[BV-BRST formalism]] (in [Costello-Gwilliam](#CostelloGwilliam)).



## Definition

+-- {: .num_defn #BeilinsonDrinfelAlgebra}
###### Definition

A **quantum BV complex** or **Beilinson-Drinfeld algebra** is 

1. a [[differential graded-commutative algebra]] $A$ (whose [[differential]] we denote by $\Delta$) over the ring $\mathbb{R} [ [ \hbar ] ]$ of [[formal power series]] over the [[real numbers]] in a formal constant $\hbar$, 

1. equipped with a [[Poisson 0-algebra|Poisson bracket]] $\{-,-\}$ of the same degree as the differential

such that 

* the following equation holds for all elements $a,b \in A$ of homogeneous degree ${\vert a\vert}, {\vert b\vert} \in \mathbb{Z}$

  $$
    \Delta( a \cdot b) = (\Delta a) \cdot b  + (-1)^{\vert a\vert} a \Delta b + \hbar \{a,b\}$ for all homogenous elements $a, b \in A
    \,.
  $$

=--

(e.g. [Costello-Gwilliam, def. 1.4.0.1](#CostelloGwilliam), [Gwilliam 13, def. 2.2.5](#Gwilliam))

+-- {: .num_remark #RoleOfTheDifferential}
###### Remark

If in the equation in def. \ref{BeilinsonDrinfelAlgebra} one replaces $\hbar$ by 1, then it takes the form characteristic of a [[BV-algebra]]. However the differential $\Delta$ here is the differential in the underlying [[chain complex]] for an [[algebra over an operad]] in chain complexes, while in a BV-algebra $\Delta$ is the unary operation encoded in the [[BV-operad]], hence present already for algebras in plain modules/chain complexes over that operad. Accordingly, in the context of BD-algebra then for $\hbar \neq 0$ the bracket is actually trivial up to homotopy.

=--

## Related concepts

[[!include deformation quantization - table]]

## References

The notion was introduced in

* [[Alexander Beilinson]], [[Vladimir Drinfeld]], _[[Chiral Algebras]]_

A discussion is in section 2.4 of

* {#CostelloGwilliam} [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in quantum field theory Volume 2_ ([pdf](http://people.mpim-bonn.mpg.de/gwilliam/vol2may8.pdf))


See also

* {#Gwilliam13} [[Owen Gwilliam]], _Factorization algebras and free field theories_ PhD thesis (2013) ([[GwilliamThesis.pdf:file]])
 


[[!redirects Beilinson-Drinfeld algebras]]

[[!redirects BD algebra]]
[[!redirects BD algebras]]

[[!redirects BD-algebra]]
[[!redirects BD-algebras]]


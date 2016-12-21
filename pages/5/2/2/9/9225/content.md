
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

A _Beilinson-Drinfeld algebra_ (or _BD-algebra_ for short) is like a [[BV-algebra]], but over [[formal power series]] in one formal parameter $\hbar$, and with the [[Gerstenhaber algebra|Gerstenhaber bracket]] is proportional to that parameter. 

This means that on may think of a BD-algebra as an $\hbar$-parameterized formal family of algebras which for $\hbar = 0$ are [[Poisson 0-algebras]] and for $\hbar \neq 0$ are [[BV-algebras]] (maybe without the condition that the [[BV-operator]] is a derivation for the bracket).

Such BD-algbras are used to formalize [[formal deformation quantization]] in the context of the [[BV-BRST formalism]].



## Definition

+-- {: .num_defn #BeilinsonDrinfelAlgebra}
###### Definition

A **quantum BV complex** or **Beilinson-Drinfeld algebra** is a $\mathbb{Z}$-[[graded algebra|graded]] [[supercommutative superalgebra|graded-commutative algebra]] $A$ over the ring $\mathbb{R} [ [ \hbar ] ]$ of [[formal power series]] in a formal constant $\hbar$, equipped with a [[Poisson 0-algebra|Poisson bracket]] $\{-,-\}$ of degree 1 and with an operator $\Delta \colon A \to A$ of degree 1 which satisfies:

1. $\Delta^2 = 0$

1. $\Delta( a b) = (\Delta a) b  + (-1)^{\vert a\vert} a \Delta b + \hbar \{a,b\}$ for all homogenous elements $a, b \in A$

=--

(e.g. [Costello-Gwilliam, def. 1.4.0.1](#CostelliGwilliam), [Gwilliam 13, def. 2.2.5](#Gwilliam))

This is [[algebra over an operad]] over the [[BD operad]].


## Related concepts

[[!include deformation quantization - table]]

## References

The notion was introduced in

* [[Alexander Beilinson]], [[Vladimir Drinfeld]], _[[Chiral Algebras]]_

A discussion is in section 2.4 of

* {#CostelloGwilliam} [[Kevin Costello]], [[Owen Gwilliam]], ([pdf](http://people.mpim-bonn.mpg.de/gwilliam/vol2may8.pdf))


See also

* {#Gwilliam13} [[Owen Gwilliam]], _Factorization algebras and free field theories_ PhD thesis (2013) ([[GwilliamThesis.pdf:file]])
 


[[!redirects Beilinson-Drinfeld algebras]]

[[!redirects BD algebra]]
[[!redirects BD algebras]]

[[!redirects BD-algebra]]
[[!redirects BD-algebras]]


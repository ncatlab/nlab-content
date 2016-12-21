
#Contents#
* table of contents
{:toc}

## Idea

An [[algebra over an operad]] over the [[BD operad]].

For the moment see at _[[BV-complex]]_

+-- {: .num_remark}
###### Remark

Beware that the definition of BD-algebra is very similar to that of _[[BV-algebra]]_, but there is a crucial difference in sign in the grading of the bracket (e.g. [Gwilliam 13, footnote 7](#Gwilliam13)). Beware that, confusingly, it is the BD-algebras, not the [[BV-algebras]], which control [[BV-formalism]] in [[field theory]].

=--

## Definition

+-- {: .num_defn #BeilinsonDrinfelAlgebra}
###### Definition

A **quantum BV complex** or **Beilinson-Drinfeld algebra** is a $\mathbb{Z}$-[[graded algebra]] $A$ over the ring $\mathbb{R} [ [ \hbar ] ]$ of [[formal power series]] in a formal constant $\hbar$, equipped with a [[Poisson 0-algebra|Poisson bracket]] $\{-,-\}$ of degree 1 and with an operator $\Delta \colon A \to A$ of degree 1 which satisfies:

1. $\Delta^2 = 0$

1. $\Delta( a b) = (\Delta a) b  + (-1)^{\vert a\vert} a \Delta b + \hbar \{a,b\}$ for all homogenous elements $a, b \in A$

=--

In ([Gwilliam 2013](#Gwilliam)) this is def. 2.2.5.

## Related concepts

[[!include deformation quantization - table]]

## References

The notion was introduced in

* [[Alexander Beilinson]], [[Vladimir Drinfeld]], _[[Chiral Algebras]]_

A discussion is in section 2.4 of

* [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in perturbative quantum field theory : $P_0$-operad_ ([wiki](http://math.northwestern.edu/~costello/factorization_public.html#[[P_0%20operad]]), [pdf](http://math.northwestern.edu/~gwilliam/factorization.pdf)) 


See also

* {#Gwilliam13} [[Owen Gwilliam]], _Factorization algebras and free field theories_ PhD thesis (2013) ([[GwilliamThesis.pdf:file]])
 


[[!redirects Beilinson-Drinfeld algebras]]

[[!redirects BD algebra]]
[[!redirects BD algebras]]

[[!redirects BD-algebra]]
[[!redirects BD-algebras]]


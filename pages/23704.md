[[!redirects semiadditive dagger categories]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##
A **semiadditive dagger category** is a [[cocartesian monoidal dagger category]] $(C, \oplus, 0, i_A, i_B, 0_A)$ such that 

* for all objects $A \in Ob(C)$, $i_A^\dagger \circ i_A = id_A$ and $i_A^\dagger \circ i_A = id_A$
* for all objects $A \in Ob(C)$ and $B \in Ob(C)$, $i_B^\dagger \circ i_A = 0_B \circ 0_A^\dagger$

In a semiadditive dagger category, the coproduct is called a **biproduct** and the initial object is called a **zero object**. 

## Examples ##

* The dagger category [[Hilb]] of [[Hilbert spaces]] and [[continuous map|continuous]] [[linear maps]] is a semiadditive dagger category. 

* The dagger category [[Rel]] of [[sets]] and [[relations]] is a semiadditive dagger category. 

## See also ##

* [[dagger category]]
* [[monoidal dagger category]]
* [[cocartesian monoidal dagger category]]
* [[cartesian monoidal dagger category]]
* [[semiadditive dagger 2-poset]]

## References ##


* Martti Karvonen. Biproducts without pointedness ([abs:1801.06488](https://arxiv.org/abs/1801.06488))
* Chris Heunen and Martti Karvonen. Limits in dagger categories. Theory and Applications of Categories, 34(18):468–513, 2019.
* Chris Heunen, Andre Kornell. Axioms for the category of Hilbert spaces ([arXiv:2109.07418](https://arxiv.org/abs/2109.07418))
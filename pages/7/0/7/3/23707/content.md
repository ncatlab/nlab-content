[[!redirects compact closed dagger categories]]

#Contents#
* table of contents
{:toc}

## Definition ##
A **compact closed dagger category** is a [[symmetric monoidal dagger category]] $C$ with 

* an object $A^*$ called the **dual** for every object $A:Ob(C)$

* for every object $A:Ob(C)$, a morphism $\iota^R_A: \Iota \to A \otimes A^*$ called the **right unit**

* for every object $A:Ob(C)$, a morphism $\iota^L_A: \Iota \to A^* \otimes A$ called the **left unit**

* for every object $A:Ob(C)$, a morphism $\eta^L_A: A \otimes A^* \to \Iota$ called the **left counit**

* for every object $A:Ob(C)$, a morphism $\eta^R_A: A^* \otimes A \to \Iota$ called the **right counit**

such that

* for all objects $A:Ob(C)$, ${\iota^R_A}^\dagger = \eta^L_A$ 

* for all objects $A:Ob(C)$, ${\iota^L_A}^\dagger = \eta^R_A$

* for all objects $A:Ob(C)$, $\iota^L_{A}A \circ A\eta^L_{A}$

* for all objects $A:Ob(C)$, $\iota^R_{A^*}A^* \circ A\eta^R_{A^*}$

* for all objects $A:Ob(C)$, $A\iota^R_{A} \circ \eta^R_{A}A$

* for all objects $A:Ob(C)$, $A^*\iota^R_{A^*} \circ \eta^R_{A^*}A^*$

## Examples ##

* The [[dagger category]] [[Hilb]] of [[Hilbert spaces]] and [[continuous map|continuous]] [[linear maps]] is a compact closed dagger category. 

## See also ##

* [[dagger category]]

* [[monoidal dagger category]]

* [[symmetric monoidal dagger category]]

* [[compact closed category]]

## References ##

* [[Chris Heunen]], [[Andre Kornell]], *Axioms for the category of Hilbert spaces* ([arXiv:2109.07418](https://arxiv.org/abs/2109.07418))


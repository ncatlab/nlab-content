[[!redirects monoidal dagger categories]]

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
A **monoidal dagger category** is a [[dagger category]] $C$ with a [[dagger functor]] $(-)\otimes(-): (C \times C) \to C$ from the product dagger category of $C$ to $C$ itself called the **tensor product** and an object $\Iota \in Ob(C)$ called the **tensor unit**, such that

* for all morphisms $f \in Hom_C(D,E)$ and $g \in Hom_C(F,G)$, $(f \otimes g)^\dagger = f^\dagger \otimes g^\dagger$

* for all objects $D \in Ob(C)$, $E \in Ob(C)$, $F\in Ob(C)$, a [[natural unitary isomorphism]] called the **associator** of $D$, $E$, and $F$,

$$alpha_{D, E, F}:(D\otimes E)\otimes F \cong^\dagger D\otimes(E\otimes F)$$

* for objects $A \in Ob(C)$, a natural unitary isomorphism called the **left unitor** of $A$, 

$$\lambda_{A}: \Iota\otimes A \cong^\dagger A$$

* for objects $A \in Ob(C)$, a natural unitary isomorphism called the **right unitor** of $A$

$$\rho_{A}: A\otimes\Iota \cong^\dagger A$$

* all objects $A \in Ob(C)$ and $B \in Ob(C)$ satify the **triangle identity**:

$$\rho_A \otimes \Iota_B = (1_A \otimes \rho_B) \circ \alpha_{A, \Iota, B}$$

* all objects $D \in Ob(C)$, $E \in Ob(C)$, $F \in Ob(C)$, $G \in Ob(C)$ satisfy the **pentagon identity**:

$$\alpha_{D, E, F \otimes G} \circ \alpha_{D \otimes E, F, G} = (id_D \otimes \alpha_{E, F, G}) \circ \alpha_{D, E \otimes F, G} \circ (\alpha_{D, E, F} \otimes id_G)$$

## Examples ##

* [[braided monoidal dagger category]]

* [[symmetric monoidal dagger category]]

* [[cartesian monoidal dagger category]]

* [[cocartesian monoidal dagger category]]

* [[semiadditive dagger category]]

* [[rigid monoidal dagger category]]

* [[compact closed dagger category]]

## See also ##

* [[dagger category]]
* [[dagger functor]]
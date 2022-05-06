
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Overview

DisCoPy is a toolbox for computing with monoidal categories in Python.

It is available at: [https://github.com/oxford-quantum-group/discopy](https://github.com/oxford-quantum-group/discopy)

## String diagrams

The core data structure is [`Diagram`](https://discopy.readthedocs.io/en/main/_autosummary/monoidal/discopy.monoidal.Diagram.html), an implementation of [[string diagram|string diagrams]] in the free [[premonoidal category]]. 

Diagrams in the free [[monoidal category]] can be seen as premonoidal diagrams quotiented by the _interchanger_, i.e. the naturality equation for the monoidal product: $f \otimes 1_c \circ 1_b \otimes g = 1_a \otimes g \circ f \otimes 1_d$ for all $f : a \to b$ and $g : c \to d$. Diagrams in the free [[rigid monoidal category]] can be seen as monoidal diagrams quotiented by the [[triangle identities|snake equations]]. In practice, these quotients are computed by calling `Diagram.normal_form`.

DisCoPy also implements the syntax for diagrams in the free [[cartesian monoidal category]] and [[biclosed monoidal category]], although their normal form is not yet implemented. Furthermore, formal sums of diagrams can also be composed and tensored, making all the diagams [[enriched category|enriched]] in [[monoid|monoids]].

## Monoidal functors

Diagrams can be evaluated in concrete monoidal categories by applying functors to them. DisCoPy implements strong monoidal functors into:

* the category of matrices into arbitrary [[rig|semirings]], including finite dimensional [[vector space|vector spaces]] and finite [[relation|relations]],
* the category of quantum circuits,
* the category of Python functions.

## References

* DisCoPy's documentation: [https://discopy.readthedocs.io/](https://discopy.readthedocs.io/)
* [[Giovanni de Felice]], [[Alexis Toumi]], [[Bob Coecke]]. _DisCoPy: Monoidal Categories in Python_. Applied Category Theory, 2020. ([arXiv:2005.02975l](https://arxiv.org/abs/2005.02975l))
* [[Konstantinos Meichanetzidis]], [[Stefano Gogioso]], [[Giovanni De Felice]], [[Nicolò Chiappori]], [[Alexis Toumi]], [[Bob Coecke]]. _Quantum Natural Language Processing on Near-Term Quantum Computers_. Quantum physics & logic, 2020. ([arXiv:2005.04147](https://arxiv.org/abs/2005.04147 ))
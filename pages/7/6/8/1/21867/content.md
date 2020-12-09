
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

_DisCoPy_ is a toolbox for computing with [[string diagram|string diagrams]], [[monoidal categories]] and [[monoidal functor|strong monoidal functors]] in [[Python]]. It is available on [GitHub](#GitHubDisCoPy).

## String diagrams

The core data structure is [`Diagram`](https://discopy.readthedocs.io/en/main/_autosummary/discopy.monoidal.Diagram.html), an implementation of [[string diagram|string diagrams]] in the [[free construction|free]] [[premonoidal category]].

Fix a monoidal [[signature (in logic) |signature]] $\Sigma = \Sigma_1 \xrightarrow{\text{dom}, \text{cod}} \Sigma_0^\star$ for a set of _boxes_ $\Sigma_1$, a set of objects $\Sigma_0$ and its [[free monoid]] $\Sigma_0^\star$, we write $f \colon s \to t$ for $f \in \Sigma_1$ whenever $\text{dom}(f) = s$ and $\text{cod}(f) = t$.
Let $L(\Sigma) = \Sigma_0^\star \times \Sigma_1 \times \Sigma_0^\star$, a _layer_ is a triple $l = (u, f \colon s \to t, v) \in L(\Sigma)$, where we define $\text{dom}(l) = u s v$ and $\text{cod}(l) = u t v$.
It is depicted, in [[string diagram]]-notation, as:

\begin{tikzpicture}
\node () at (0.25, 1) {$u$};
\node () at (1.25, 1) {$s$};
\node () at (2.25, 1) {$v$};
\node () at (1.25, 0.0) {$t$};
\draw [out=-90, in=90] (0, 1) to (0, 0);
\draw [out=-90, in=90] (1, 1) to (1, 0.75);
\draw [out=-90, in=90] (2, 1) to (2, 0);
\draw [out=-90, in=90] (1.0, 0.25) to (1.0, 0);
\draw (0.75, 0.25) -- (1.25, 0.25) -- (1.25, 0.75) -- (0.75, 0.75) -- (0.75, 0.25);
\node () at (1.0, 0.5) {$f$};
\end{tikzpicture}

The set of _diagrams_ $D(\Sigma)$ is the [[hom-set|set of arrows]] in the [[free category]] [[generators and relations|generated]] by the layers $L(\Sigma)$, considered as a [[directed graph]]. Concretely, $d$ is given by a length $\text{len}(d) = n \in \mathbb{N}$, a domain $\text{dom}(d) \in \Sigma_0^\star$ and a list of layers $\layers(d) = (d_1, \dots, d_n) \in L(\Sigma)^n$ such that $\text{dom}(d) = \text{dom}(d_0)$ and $\text{cod}(d_i) = \text{dom}(d_{i + 1})$ for each $i \leq n$.
The codomain of a diagram is the codomain of its last layer $\cod(d) = \cod(d_n)$.

Note that in order to define a diagram uniquely, its layers have more data than necessary. It is enough to specify a list $\boxes(d) \in \Sigma_1^n$ of generators together with a list $\offsets(d) \in \N^n$: the number of wires on the left of each box.
This is the definition used in [Delpeuch and Vicary (2018)](#DelpeuchVicary18), [[Globular]], [[homotopy.io]] as well as DisCoPy.

Diagrams in the free [[monoidal category]] can be seen as premonoidal diagrams quotiented by the _[[interchanger]]_, i.e. the naturality equation for the [[tensor product|monoidal product]]: $f \otimes 1_c \circ 1_b \otimes g = 1_a \otimes g \circ f \otimes 1_d$ for all $f : a \to b$ and $g : c \to d$. Diagrams in the free [[rigid monoidal category]] can be seen as monoidal diagrams quotiented by the [[triangle identities|snake equations]]. In practice, these quotients are computed by calling `Diagram.normal_form`.

DisCoPy also implements the [[syntax]] for diagrams in the [[free construction|free]] [[cartesian monoidal category]] and [[biclosed monoidal category]], although their normal form is not yet implemented. Furthermore, formal sums of diagrams can also be composed and tensored, making all the diagams [[enriched category|enriched]] in [[monoid|monoids]].

## Monoidal functors

Diagrams can be evaluated in concrete monoidal categories by applying [[functors]] to them. DisCoPy implements [[strong monoidal functors]] into:

* the category of [[matrices]] in arbitrary [[rig|semirings]], including [[finite dimensional vector spaces]] and finite [[relation|relations]],

* the category of [[quantum circuits]],

* the category of [[Python]] functions.

## Related entries

[[!include proof assistants and formalization projects -- list]]

## References

* DisCoPy's documentation: [https://discopy.readthedocs.io/](https://discopy.readthedocs.io/)

* Giovanni de Felice, [[Alexis Toumi]], [[Bob Coecke]]. _DisCoPy: Monoidal Categories in Python_. Applied Category Theory, 2020. ([arXiv:2005.02975l](https://arxiv.org/abs/2005.02975l))

* Konstantinos Meichanetzidis, Stefano Gogioso, Giovanni De Felice, Nicolò Chiappori, [[Alexis Toumi]], [[Bob Coecke]]. _Quantum Natural Language Processing on Near-Term Quantum Computers_. Quantum physics & logic, 2020. ([arXiv:2005.04147](https://arxiv.org/abs/2005.04147 ))

* {#DelpeuchVicary18} Delpeuch, Antonin, and [[Jamie Vicary]], _Normalization for planar string diagrams and a quadratic equivalence algorithm._ arXiv preprint [arXiv:1804.07832](https://arxiv.org/abs/1804.07832) (2018).

* {#GitHubDisCoPy} DisCoPy repository, [github.com/oxford-quantum-group/discopy](https://github.com/oxford-quantum-group/discopy)


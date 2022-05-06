
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###

#### Proof assistants and formalization projects
+--{: .hide}
[[!include proof assistants and formalization projects -- list]]
=--

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

The name stands for _Distributional Compositional Python_, indeed the package was first intended as an implementation of the [[DisCoCat]] models of [[natural language]].

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

We can define identity, composition and tensor of diagrams in terms of this combinatorial encoding:

* The identity diagram $\text{id}(x)$ for $x \in \Sigma_0^\star$ is defined by $\text{len}(\text{id}(x)) = 0$ and $\text{dom}(\text{id}(x)) = x$. It is depicted as vertical wires labeled with $x$.
* Given two diagrams $d_0, d_1 \in D(\Sigma)$ with $\text{cod}(d_0) = \text{dom}(d_1)$, their composition $d_1 \circ d_0 \in D(\Sigma)$ is defined by vertical concatenation, i.e. $\text{layers}(d_1 \circ d_0) = \text{layers}(d_0) \text{layers}(d_1)$. In Python code, this is written `d0 >> d1` or `d1 << d0`.
* Given a diagram $d \in D(\Sigma)$ and a type $x \in \Sigma_0^\star$, the [[whiskering|whiskerings]] $x \otimes d$ and $d \otimes x$ are defined by concatenating $d$ with $x$-labeled wires on its left and right. First, define whiskering for layers $l = (u, f, v) \in L(\Sigma)$ as $x \otimes l = (x u, f, v)$ and $l \otimes x = (u, f, v x)$. Then, define whiskering for diagrams as $\text{layers}(x \otimes d) = (x \otimes d_1, \dots, x \otimes d_n)$ and $\text{layers}(d \otimes x) = (d_1 \otimes x, \dots, d_n \otimes x)$.
* Given two diagrams $d_0, d_1 \in D(\Sigma)$, their tensor is defined as $d_0 \otimes d_1 = \text{cod}(d_0) \otimes d_1 \circ d_0 \otimes \text{dom}(d_1)$. In Python, this is written `d0 @ d1 == d0 @ Id(d1.dom) >> Id(d0.cod) @ d1`.

Diagrams in the free [[monoidal category]] can be seen as premonoidal diagrams quotiented by the _[[interchanger]]_, i.e. the naturality equation for the [[tensor product|monoidal product]]: $f \otimes 1_c \circ 1_b \otimes g = 1_a \otimes g \circ f \otimes 1_d$ for all $f : a \to b$ and $g : c \to d$. Diagrams in the free [[rigid monoidal category]] can be seen as monoidal diagrams quotiented by the [[triangle identities|snake equations]]. In practice, these quotients are computed by calling `Diagram.normal_form`.

Diagrams are equipped with an involution `Diagram.dagger` that implements [[dagger categories]]. Furthermore, formal sums of diagrams can also be composed and tensored, making all the diagams [[enriched category|enriched]] in [[monoid|monoids]].
DisCoPy also implements the [[syntax]] for diagrams in the [[free construction|free]] [[cartesian monoidal category]] and [[biclosed monoidal category]], although their normal form is not yet implemented. 

## Monoidal functors

Diagrams can be evaluated in concrete monoidal categories by applying [`Functor`](https://discopy.readthedocs.io/en/main/_autosummary/discopy.monoidal.Functor.html) instances to them.

Let $\mathcal{F} : \text{MonSig} \to \text{MonCat}$ be the functor that sends a monoidal signature to its free monoidal category, and its right adjoint $\mathcal{U} : \text{MonCat} \to \text{MonSig}$ the [[forgetful functor]]. From the [[free-forgetful adjunction]], we get that monoidal functor $F : \mathcal{F}(\Sigma) \to S$ from a free monoidal category generated by a signature $\Sigma$ into some monoidal category $S$ is uniquely defined by a morphism of signature $F : \Sigma \to \mathcal{U}(S)$. That is, in order to define a functor $F : \mathcal{F}(\Sigma) \to S$, it's enough to define two mappings $F_0 : \Sigma_0 \to \text{Ob}(S)$ and $F_1 : \Sigma_1 \to \text{Ar}(S)$ which commute with $\text{dom}$ and $\text{cod}$.

Concretely, a DisCoPy functor is defined by `F = Functor(ob, ar)` where `ob` and `ar` are mappings from generating object to types and from box to diagram respectively. These mappings can be either given as Python dictionaries if they have finite domains or as Python functions otherwise. Once its image for each generating object and each box is given, `F` can be applied to arbitrary diagrams. Optional arguments `ob_factory` and `ar_factory` can be used to define functors with arbitrary categories as codomain. By default DisCoPy functors are endofunctors from the free category to itself, i.e. they send diagrams to diagrams. 

Currently, DisCoPy implements [[strong monoidal functors]] into:

* the category of [[matrices]] in arbitrary [[rig|semirings]], including [[finite dimensional vector spaces]] and finite [[relation|relations]],

* the category of [[quantum circuits]],

* the category of [[Python]] functions.

## Natural language processing

Diagrams can be used to encode derivations in a [[formal grammar]]. Indeed, the first use case of DisCoPy was to apply monoidal diagrams to these grammar diagrams in order to compute their [[semantics]]. Currently, DisCoPy can handle the following frameworks:

* [[context-free grammar]], where derivations are diagrams in a [[monoidal category]],
* [[combinatory categorial grammar]], where derivations are diagrams in a [[biclosed monoidal category]],
* [[pregroup grammar]], where derivations are diagrams in a [[rigid monoidal category]].

## References

* Giovanni de Felice, [[Alexis Toumi]], [[Bob Coecke]]. _DisCoPy: Monoidal Categories in Python_. Applied Category Theory, 2020. ([arXiv:2005.02975l](https://arxiv.org/abs/2005.02975l))

* Konstantinos Meichanetzidis, Stefano Gogioso, Giovanni De Felice, Nicolò Chiappori, [[Alexis Toumi]], [[Bob Coecke]]. _Quantum Natural Language Processing on Near-Term Quantum Computers_. Quantum physics & logic, 2020. ([arXiv:2005.04147](https://arxiv.org/abs/2005.04147 ))

* {#DelpeuchVicary18} Delpeuch, Antonin, and [[Jamie Vicary]], _Normalization for planar string diagrams and a quadratic equivalence algorithm._ arXiv preprint [arXiv:1804.07832](https://arxiv.org/abs/1804.07832) (2018).

* {#DisCoPyDoc} _DisCoPy's documentation._ [discopy.readthedocs.io](https://discopy.readthedocs.io/)

* {#GitHubDisCoPy} _DisCoPy's repository._ [github.com/oxford-quantum-group/discopy](https://github.com/oxford-quantum-group/discopy)


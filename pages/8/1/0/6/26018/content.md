
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[categorification]] of the notion of *[[fusion categories]]* to [[2-categories]].

## Properties
### Tannaka-Krein reconstruction theorem

The [[Tannaka duality]] establishes a correspondence between (multi-)[[fusion category|fusion categories]] and [[weak Hopf algebra|weak Hopf algebras]]. It is expected that an analogous statement holds for the higher categorification of this setting. The theorem corresponding to the specialization of this setting to fusion 2-categories and [[semisimple category|semisimple]] [[Hopf monoidal category|Hopf categories]] (as opposed to *multi-* fusion 2-categories and *weak* Hopf categories) appears in ([Green (2023)](#Green23)).

+-- {: .num_theorem}
###### Theorem
**(Tannaka-Krein reconstruction theorem for fusion 2-categories)**

There is a symmetric monoidal equivalence, contravariant at the level of 1-morphisms,
between the full subcategory of $3Vec/2Vec$ consisting of locally faithful functors and the 2-category of
2-Hopf Algebras. The natural transformations associated to this equivalence reconstruct a semisimple
Hopf category from its fusion 2-category of representations and fiber functor, and a fusion 2-category
with fiber functor $F$ from the Hopf category $End(F)$.

=--


## References

* [[Christopher L. Douglas]], [[David J. Reutter]], *Fusion 2-categories and a state-sum invariant for 4-manifolds* &lbrack;[arXiv:1812.11933](https://arxiv.org/abs/1812.11933)&rbrack;

* {#DY23} [[Thibault Decoppet]], [[Matthew Yu]]. *Fiber 2-Functors and Tambara-Yamagami Fusion 2-Categories*. (2023) &lbrack;[arXiv:2306.08117](https://arxiv.org/abs/2306.08117)&rbrack;

* {#Green23} David Green. *Tannaka-Krein reconstruction for fusion 2-categories*. (2023). ([arXiv:2309.05591](https://arxiv.org/abs/2309.05591)).

[[!redirects fusion 2-categories]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### (0,1)-categoty theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

A __transitive relation__ is a [[semicategory]] or [[magmoid]] $A$ such that for all objects $a$ and $b$ in $A$, there are no more than one morphism with domain $a$ and codomain $b$. Equivalently, a transitive relation is a semicategory or magmoid [[enriched category|enriched]] on [[truth values]]. 

[[set theory|Set theoretically]], a (binary) [[relation]] $\sim$ on a [[set]] $A$ is __transitive__ if in every chain of $3$ pairwise related elements, the first and last elements are also related:
$$\forall (x, y, z: A),\; x \sim y \;\wedge\; y \sim z \;\Rightarrow\; x \sim z$$
which generalises from $3$ to any finite, positive number of elements.

In the language of the $2$-poset [[Rel]] of sets and relations, a relation $R: A \to A$ is __transitive__ if it contains its composite with itself:
$$R^2 \subseteq R$$
from which it follows that $R^n \subseteq R$ for any positive [[natural number]] $n$.  To include the case where $n = 0$, we must explicitly state that the relation is [[reflexive relation|reflexive]].

Transitive relations are often understood as [[orders]].


[[!redirects transitive relation]]
[[!redirects transitive relations]]

[[!redirects transitivity]]


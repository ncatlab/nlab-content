+-- {: .rightHandSide}
+-- {: .toc .hide                Show TOC}
* [[measure theory]]
* [[outer measure]]
* [[sigma-algebra]]
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The **Carathéodory construction** is a fundamental method in [[measure theory]] used to construct a [[measure space]] from an [[outer measure]]. It provides the standard machinery to extend a pre-measure (defined on a simple structure like a ring of sets) to a complete measure on a [[sigma-algebra]]. It is most famously used to define the [[Lebesgue measure]].


### Carathéodory's Criterion
\begin{definition}
A subset $E \subseteq X$ is said to be **Carathéodory-measurable** (or $\mu^*$-measurable) if for every "test set" $A \subseteq X$, the following equality holds:
$$\mu^*(A) = \mu^*(A \cap E) + \mu^*(A \cap E^c)$$
\end{definition}

In practice, since subadditivity implies $\mu^*(A) \leq \mu^*(A \cap E) + \mu^*(A \cap E^c)$, one only needs to verify:
$$\mu^*(A) \geq \mu^*(A \cap E) + \mu^*(A \cap E^c)$$

## Properties

\begin{theorem}
**(Carathéodory's Theorem)**
Let $\mu^*$ be an outer measure on $X$. The collection $\mathcal{M}$ of all $\mu^*$-measurable sets forms a [[sigma-algebra]] on $X$. Furthermore, the restriction $\mu = \mu^*|_{\mathcal{M}}$ is a complete [[measure]].
\end{theorem}

## Applications

* **Lebesgue Measure**: Starting with the volume of $n$-dimensional intervals as a pre-measure, the Carathéodory construction yields the [[Lebesgue measure]] on $\mathbb{R}^n$.
* **Hausdorff Measure**: Used in [[fractal geometry]] to define measures on metric spaces.
* **Hahn-Kolmogorov Extension**: The construction is the core engine behind extending measures from a [[ring of sets]] to the generated $\sigma$-algebra.

## Related entries

* [[measure]]
* [[outer measure]]
* [[measurable set]]
* [[Hahn-Kolmogorov theorem]]

[[!redirects Caratheodory construction]]
[[!redirects Carathéodory-measurable set]]
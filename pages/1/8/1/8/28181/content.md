+-- {: .rightHandSide}
+-- {: .toc .hide                Show TOC}
* [[measure theory]]
* [[measure space]]
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An **outer measure** is a function that assigns a "size" to every subset of a given set $X$. Unlike a [[measure]], it is not required to be countably additive, but only countably subadditive. It serves as the starting point for the [[Caratheodory construction]].

## Definition

\begin{definition}
An **outer measure** on a set $X$ is a function $\mu^* \colon \mathcal{P}(X) \to [0, \infty]$ satisfying the following axioms:

1. **Null empty set**: $\mu^*(\emptyset) = 0$.
2. **Monotonicity**: If $A \subseteq B \subseteq X$, then $\mu^*(A) \leq \mu^*(B)$.
3. **Countable subadditivity**: For any sequence of subsets $\{A_n\}_{n=1}^\infty$ of $X$, 
   $$\mu^*\left( \bigcup_{n=1}^\infty A_n \right) \leq \sum_{n=1}^\infty \mu^*(A_n)$$
\end{definition}

## Construction from pre-measures

The most common way to produce an outer measure is from a [[pre-measure]] $\mu_0$ defined on a [[ring of sets]] (or semi-ring) $\mathcal{R}$ covering $X$. For any $A \subseteq X$, we define:
$$\mu^*(A) = \inf \left\{ \sum_{n=1}^\infty \mu_0(E_n) : A \subseteq \bigcup_{n=1}^\infty E_n, E_n \in \mathcal{R} \right\}$$

## Related entries

* [[measure]]
* [[Carathéodory construction]]
* [[measurable set]]

[[!redirects outer measures]]
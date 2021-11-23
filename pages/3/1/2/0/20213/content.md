## Idea

The concept of approach space generalized the concept of [[metric space]]. The idea is that the distance describes not only the distance between two points but the distance of a point to a subset. This relatively tangible generalization gives the missing link in the triad of the concepts of [[uniform space|uniformity]], [[topological space|topology]], and [[metric space|metric spaces]].


## Definition

An __approach space__ is a set $X$ together with a __distance__ $d\colon X \times \mathcal{P}(X) \to [0,\infty]$ (where $\mathcal{P}(X)$ denotes the [[power set]]) such that the following axioms hold for all $x \in X$

1. $d(x, \{x\}) = 0$ 

1. $d(x, \emptyset) = \infty$

1. for all $A, B \in \mathcal{P}$: 
   $d(x, A\cup B) = \min\{ d(x, A), d(x, B) \}$

1. for all $A \in \mathcal{P}$ and $\varepsilon \in [0,\infty]$: 
   $d(x, A ) \leq d(x, A^{\varepsilon]} ) + \varepsilon $

where $A^{\varepsilon]} \coloneqq \{x \in X \mid d(x, A) \leq \varepsilon \}$.

## Properties

Every approach space $d$ induces a [[topological space|topology]] on $X$ via the [[closed subspace |closure operator]] $Cl_d(A) = \{x \in X \mid d(x, A) = 0 \}$.

## Examples

* Every [[topological space]] is induced by a canonical approach structure given by $d(x, A) = 0$ if $x \in Cl(A)$ and $d(x, A) = \infty$ otherwise.

* The [[one-point compactification]] of a metric space $d$ can be metrised in a canonical way as an approach space by 

$$
d^*(x, A) = 
\begin{cases} 
d(x, A\setminus\{\infty\})  & x \neq \infty \\
0  & x = \infty\, and\, A\, is\, not\, precompact \\
\infty & x = \infty\, and\, A\, is\, precompact.
\end{cases}
$$

* A [[gauge space|gauge]], or more generally a gauge base, $G$ on $X$ gives a distance on $X$ by $d_G(x, A) = \sup_{d \in G} \inf_{y\in A} d(x,y)$.


## Related concepts

* [[metric space]]

* [[gauge space]]

* [[relational beta-module]]

## References

 * Robert Lowen, _Approach spaces: the missing link in the topology-uniformity-metric triad_, Oxford Mathematical Monographs. 1997. ([publisher link](https://global.oup.com/academic/product/approach-spaces-9780198500308)).
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _bornological set_ is a notion of space, where instead of considering open sets and continuous functions whose inverse images preserve open sets as one does for [[topological space]]s, one considers bounded sets (which constitute a _bornology_) and bounded maps whose direct images preserve bounded sets. Bornological sets are especially important in functional analysis (see [[bornological space]]). 

## Definition 

Let $X$ be a set. A **bornology** on $X$ is a collection $\mathcal{B} \subseteq P X$ of subsets of $X$ such that 

* $\mathcal{B}$ covers $X$: $\bigcup_{B \in \mathcal{B}} B = X$, 

* $\mathcal{B}$ is downward-closed: if $B \in \mathcal{B}$ and $A \subseteq B$, then $A \in \mathcal{B}$, 

* $\mathcal{B}$ is closed under finite unions: if $B_1 \ldots, B_n \in \mathcal{B}$, then $\bigcup_{1 \leq \i \leq n} B_i \in \mathcal{B}$. 

A **bornological set** is a set $X$ equipped with a bornology. The elements of $\mathcal{B}$ are called the **bounded sets** of a bornological set. 

If $X$, $Y$ are bornological sets, a function $f: X \to Y$ is said to be **bounded** if $f(B)$ is bounded in $Y$ for every bounded $B$ in $X$. One obtains a category of bornological sets and bounded maps. 

## Examples

* If $X$ is any topological space, there is a bornology consisting of all _precompact_ sets of $X$ (subsets whose closure is compact). Any continuous map is bounded with respect to this uniform choice of bornology. 

* If $X$ is any metric space, there is a bornology where a set is bounded if it is contained in some open ball. Any Lipschitz continuous map is bounded with respect to this uniform choice of bornology. 

* For linear maps between [[bornological space|bornological spaces]], a map is continuous if and only if it is bounded. 


A **structure** on a [[set]] $X$ consists of a collection 

$$\mathcal{S}_n \subseteq P(X^n)$$ 

for each [[natural number]] $n$ such that 

* $\mathcal{S}_n$ is a [[Boolean algebra|Boolean subalgebra]] of $P(X^n)$, 

* If $A \in \mathcal{S}_n$, then $A \times X$ and $X \times A$ belong to $\mathcal{S}_{n+1}$, 

* The set $\Delta = \{(x_1, \ldots, x_n): \forall_{1 \leq i \leq n} x_i = x_1\}$ belongs to $\mathcal{S}_n$, 

* If $\pi: X^{n+1} \to X^n$ denotes the projection onto the first $n$ coordinates, then the image $\pi(A)$ belongs to $\mathcal{S}_n$ whenever $A \in \mathcal{S}_{n+1}$. 

Morally, a structure on a set is the collection of subsets of a finite power of $X$ which are definable with respect to a [[first-order language]] that has been interpreted in $X$ (such an interpretation being called a structure of the language). Indeed, the definable sets of such a language do form a structure in the present sense. Conversely, to any structure in this sense, we may introduce a relational language whose $n$-ary relation symbols are named by the elements of $\mathcal{S}_n$, and then the tautological structure of this language on $X$, where each relation is interpreted as the set that names it, is a structure of this language. 

Each structure $\mathcal{S}$ on $X$ induces a [[bicategory of relations]]: the objects are natural numbers, and 1-cells $m \to n$ are triples $(m, n, R)$ where $R \in \mathcal{S}_{m+n}$, ordered by inclusion. (It is indeed not difficult to show that 1-cells are closed under set-theoretic relational composition.) 


[[!redirects structure (model theory)]]
[[!redirects structures (model theory)]]
[[!redirects model-theoretic structure]]
[[!redirects model-theoretic structures]]

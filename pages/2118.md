Projection measures are operator-valued [[measures]] of a special type. They appear for example in the theory of reproducing kernel [[Hilbert spaces]], [[coherent states]] and the foundations of [[quantum mechanics]]. A projection measure is used to parametrize a complete family of [[projection operator]]s by subsets of some parameter space.  

Given a [[topological space]] $X$ and the $\sigma$-[[sigma-algebra|algebra]] $\mathcal{B}(X)$ of [[Borel set|Borel subsets]] of $X$, a __projection measure__ $P$ is an assignment $A\mapsto P(A)$ of self-adjoint projection operators on a fixed Hilbert space $H$
to Borel subsets $A\in \mathcal{B}(X)$ such that 
$$
P(A_1\cap A_2) = P(A_1) P(A_2)
$$
for any Borel $A_1,A_2\subset X$, where the product on the right-hand side is the composition of operators,
and if $A_1, A_2$ are disjoint also
$$
P(A_1\cup A_2) = P(A_1)+P(A_2) 
$$
and if $A_n\to A$, in the sense that $A= \cap_n \cup_{k\geq n} A_k = \cup_n \cap_{k\geq n} A_k$, then $P(A_n)\to P(A)$ in the weak operator topology. 

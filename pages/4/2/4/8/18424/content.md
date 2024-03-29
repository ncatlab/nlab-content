
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

## Definition

Let $A$ be a commutative [[topological ring]]. 

A [[formal power series]]
$$
\sum c_{n_1,\ldots,n_p}X_1^{n_1}\cdots X_p^{n_p} \in A[[X_1,\ldots,X_p]]
$$
is called **restricted** if for every neigbourhood $V$ of 0 in $A$, there is only a finite number of coefficients $c_{n_1,\ldots,n_p}$ not belonging to $V$. One can view this as the coefficients "converging to $0\in A$".

If $A$ is linearly topologised (that is, it has a fundamental system of [[neighbourhoods]] of $0$ consisting of [[ideals]]) then restricted formal power series form a _subring_ $A\{X_1,\ldots,X_p\} \subset A[[X_1,\ldots,X_p]]$.

Every derivative (in the formal sense) of a restricted formal power series is also restricted.

If $A$ is discrete, then a $A\{X_1,\ldots,X_p\} = A[X_1,\ldots,A_p]$, the ring of [[polynomials]].
#Definition:#
A simplicial complex $K$ is a set of objects, $V(K)$, called **vertices** and a set, $S(K)$, of finite non-empty subsets of $V(K)$, called **simplices**.  The simplices satisfy the condition that if $\sigma \subset V(K)$ is a simplex and $\tau \subset \sigma$, $\tau \neq \emptyset$, then $\tau$ is also a simplex.  

We say $\tau$ is a **face** of $\sigma$.  If $\sigma \in S(K)$ has $p+1$ elements it is said to be a **$p$-simplex**.  The set of $p$-simplices of $K$ is denoted by $K_p$. The **dimension** of $K$ is the largest $p$ such that $K_p$ is non-empty.

#Remarks#

* Simplicial complexes are, in some sense, special cases of [[simplicial set|simplicial sets]]. To get from a simplicial complex to a simplicial set, you pick a total order on the set of vertices.
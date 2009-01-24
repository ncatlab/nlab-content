#Definition:#
A simplicial complex $K$ is a set of objects, $V(K)$, called **vertices** and a set, $S(K)$, of finite non-empty subsets of $V(K)$, called **simplices**.  The simplices satisfy the condition that if $\sigma \subset V(K)$ is a simplex and $\tau \subset \sigma$, $\tau \neq \emptyset$, then $\tau$ is also a simplex.  

We say $\tau$ is a **face** of $\sigma$.  If $\sigma \in S(K)$ has $p+1$ elements it is said to be a **$p$-simplex**.  The set of $p$-simplices of $K$ is denoted by $K_p$. The **dimension** of $K$ is the largest $p$ such that $K_p$ is non-empty.

#Remarks#

* Simplicial complexes are, in some sense, special cases of [[simplicial set|simplicial sets]]. To get from a simplicial complex to a simplicial set, you pick a total order on the set of vertices. Without an order on the vertices it is not easy to speak of the $k^{th}$ face of a simplex as you do not know which it is! The degeneracies are obtained by repeating an element when listing the vertices of a simplex. If $\sigma = \{v_0,v_1,\ldots, v_n\}$, with $v_0\lt v_1\lt \ldots \lt v_n$ then, for instance, $s_0(\sigma) = \{v_0,v_0, v_1,\ldots, v_n\}$.
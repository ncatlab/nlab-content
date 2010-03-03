#Definition:#
A simplicial complex $K$ is a set of objects, $V(K)$, called **vertices** and a set, $S(K)$, of finite non-empty subsets of $V(K)$, called **simplices**.  The simplices satisfy the condition that if $\sigma \subset V(K)$ is a simplex and $\tau \subset \sigma$, $\tau \ne \emptyset$, then $\tau$ is also a simplex.  

We say $\tau$ is a **face** of $\sigma$.  If $\sigma \in S(K)$ has $p+1$ elements it is said to be a **$p$-simplex**.  The set of $p$-simplices of $K$ is denoted by $K_p$. The **dimension** of $K$ is the largest $p$ such that $K_p$ is non-empty.

##Simplicial complexes v. simplicial sets##

* Simplicial complexes are, in some sense, special cases of [[simplicial set|simplicial sets]],  but only 'in some sense'.  To get from a simplicial complex to a simplicial set, you must pick a total order on the set of vertices. Without an order on the vertices you cannot speak of the $k^{th}$ face of a simplex, which is an essential feature of a simplicial set! The degeneracies are obtained by repeating an element when listing the vertices of a simplex. If $\sigma = \{v_0,v_1,\ldots, v_n\}$, with $v_0\lt v_1\lt \ldots \lt v_n$ then, for instance, $s_0(\sigma) = \{v_0,v_0, v_1,\ldots, v_n\}$.

##Geometric realisations and Polyhedra##
An abstract simplicial complex is a combinatorial gadget that models certain aspects of a spatial configuration.  Sometimes it is useful, perhaps even necessary, to produce a topological space from that data in a simplicial complex. 



###Idea###
 To each simplicial complex $K$, one can associate a topological space called the _polyhedron_ of $K$ often also called or  _geometric realisation_ of $K$ and denoted $|K|$.   


This can be constructed by taking a copy $K(\sigma)$ of a standard topological $p$-simplex for each $p$-simplex of $K$ and then 'gluing' them together according to the face relations encoded in $K$.



####Definition#### 

The _standard (topological) $p$-simplex_ is usually  taken to be the convex hull of the basis vectors $\mathbf{e}_1, \mathbf{e}_2,\ldots, \mathbf{e}_{p+1}$ in $\mathbb{R}^{p+1}$, to represent each abstract $p$-simplex, $\sigma\in S(K)$, and then 'gluing' faces together, so whenever $\tau$ is a face of $\sigma$ we identify $K(\tau)$ with the corresponding face of $K(\sigma)$. This space is usually denoted $\Delta^p$.

####Canonical construction####

There is a canonical way of constructing $|K|$ as follows: 

$|K|$ is the set of all functions from $V(K)$ to  the closed interval $[0,1]$ such that

* if $\alpha \in |K|$, the set
 
$$\{v \in V(K) \mid \alpha(v)  \neq  0\}$$

is a simplex of $K$;

 * for each $v\in V(K)$,  
$$\sum_{\alpha \in V(K)} \alpha (v) = 1.$$

We can put a metric $d$ on $|K|$ by 

$$d(\alpha,\beta) = \Big(\sum_{v\in V(K)} (p_v(\alpha) - p_v(\beta))^2\Big)^\frac{1}{2}.$$

This however gives $|K|$ as a subspace of $\mathbb{R}^{\#(V(K))}$, and so is usually of much higher dimension then might seem geometrically significant in a given context. 



[[!redirects simplicial complexes]]
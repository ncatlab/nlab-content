Given positive integers $v,\beta,r,k,\lambda$, a __block 2-design__ of type $(v,\beta,r,k,\lambda)$ is a combinatorial structure consisting of 

* a finite set $X$ whose elements are declared _points_ 
* set $B$ of $k$-element subsets of $X$, called _blocks_

such that

* (i) for each $x\in X$ the number of $v\in B$ such that $x\in b$ is independent of $x$ and equals $r$ 
* (ii) for each pair of distinct elements $x,y\in X$, the number of $b\in B$ such that $\{x,y\}\subset b$ is independent of $(x,y)$ and equals $\lambda$

__Block $s$-designs__ of type $(v,\beta,r,k,\lambda)$ for $s\gt 2$ have (ii) changed to 

(ii') for each subset $\{x_1,\ldots,x_s\}\subset X$ of cardinality precisely $s$, the number of $b\in B$ such that $\{x_1,\ldots,x_s\}\subset b$ is independent of the choice of such a subset and equals $\lambda$. 

Examples: [[Steiner system]]s, finite projective planes. 

Applications: cryptography, codes, finite geometries, finite group theory.

* Wikipedia [block design](http://en.wikipedia.org/wiki/Block_design)

 
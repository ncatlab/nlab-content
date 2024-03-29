
# Partial sections
* table of contents
{: toc}

## Definition 

Given a [[morphism]] $f: A \to B$ in any [[category]], a __partial section__ of $f$ is a [[partial map]] $s: B \nrightarrow A$ such that $f \circ s$ equals the identity on the [[domain]] of $s$. Explictly, this is a [[subobject]] $i: D \to B$ of $B$ together with a morphism $s: D \to A$ such that $f \circ s = i$.


## Examples 

* A [[local section]] of a continuous map $f: A \to B$ is a partial section of $f$ whose domain is an [[open subset]] of $B$. 

* In [[obstruction theory]], one may be interested in how far one can construct a section of a [[bundle]] (say a [[principal bundle]] with [[group]] $G$), $p: E \to X$, over a [[CW-complex]] $X$. Given a section of the restriction of $E$ over the $(k-1)$-skeleton $X_{k-1}$ (i.e., a partial section of $X$), obstructions to extending to a partial section over $X_k$ are measured by a [[cohomology class|class]] in $H^k(X_k, X_{k-1}; \pi_k(G))$. 


[[!redirects partial section]] 
[[!redirects partial sections]] 

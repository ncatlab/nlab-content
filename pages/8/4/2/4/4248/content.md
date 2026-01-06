
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _Hodge numbers_ $h^{p,q}(X)$ of a [[compact space|compact]] [[complex manifold]] $X$ are the complex [[dimensions]] of the [[Dolbeault cohomology]] groups of $X$; the [[complex geometry]]-analog of the [[Betti numbers]].

## Definition

Via the [[Dolbeault theorem]], the $(p,q)$-Hodge number of a [[compact space|compact]] [[complex manifold]] $X$ is

$$
  h^{p,q}(X) 
    \;\coloneqq\; 
  dim_\mathbb{C}H^q(X;\Omega^p),
$$

where $\Omega^p$ is the [[sheaf]] of [[holomorphic p-forms]] on $X$ and $H^q(X; \Omega^p)$ is the corresponding [[abelian sheaf cohomology]]. 

## Properties

If $dim_\mathbb{C}(X)=n$, then $h^{p,q}(X)=h^{n-p,n-q}(X)$; in particular, $h^{n,n}(X)=1$.

When $X$ is a [[Kähler manifold]], then Hodge numbers have a number of additional nontrivial properties: 

* they are symmetric, i.e., $h^{p,q}(X)=h^{q,p}(X)$;

* $h^{p,p}\geq 1$ for any $p=1,\dots,n$; 

* $b_k(X)=\sum_{p+q=k}h^{p,q}(X)$, where $b_k$ is the $k$-th [[Betti number]] of $X$.

## Related concepts

* [[Betti number]]

[[!redirects Hodge numbers]]
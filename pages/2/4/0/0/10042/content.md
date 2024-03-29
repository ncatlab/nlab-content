
> under construction

#Contents#
* table of contents
{:toc}

## Idea

Let $f:X\to Y$ be a morphism of [[locally compact topological spaces]]. Then there exist a unique [[subfunctor]] $f_!: Sh(X)\to Sh(Y)$ of the [[direct image]] functor $f_*$ such that for any [[abelian sheaf]] $F$ over $X$ the sections of $f_!(F)$ over $U^{open}\subset Y$ are those sections $s\in f_*(U)= \Gamma(f^{-1}(U),F)$ for which the restriction $f|_{supp(s)} : supp(s)\to U$ is a [[proper map]]. 

This is called the **direct image with compact support**.

It follows that $f_!$ is left exact. 

Let $p:X\to {*}$ be the map into the one point space. Then for any $F\in Sh(X)$ the [[abelian sheaf]] $p_!F$ is the [[abelian group]] consisting of sections $s\in \Gamma(X,F)$ such that $supp(s)$ is compact. One writes $\Gamma_c(X,F):= p_! F$ and calls this group a group of sections of $F$ with compact support. If $y\in Y$, then the fiber $(f_! F)_y$ is isomorphic to $\Gamma_c(f^{-1}y,F|_{f^{-1}(y)})$. 



## Related concepts

* [[exceptional inverse image]]

* [[Verdier duality]], [[six operations]]

* [[locally proper map]]


[[!redirects direct image with compact suppports]]
[[!redirects direct images with compact support]]
[[!redirects direct images with compact supports]]


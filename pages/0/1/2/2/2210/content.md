
> needs to be merged with [[infinitesimal path infinity-groupoid in a smooth topos]]

# Idea #

Recall from the discussion at [[path infinity-groupoid]] that to a [[manifold]] $X$ we may naturally associated its smooth path $\infty$-groupoid $\Pi(X)$ [[models for infinity-stack (infinity,1)-toposes|modeled by]] the simplicial [[smooth space]] or smooth singular simplicial complex $X^{\Delta^\bullet_{Diff}}$ which in degree $k$ is the smooth space of maps from the standard smooth $k$-simplex $Delta^k_{Diff} \subset \mathbb{R}^k$ to $X$.

In the context of [[synthetic differential geometry]] where there is a notion of smooth [[infinitesimal space]] there exists concretely a subcomplex of this which contains only the _infinitesimal simplices_ in $X$. This is the infinitesimal singular simplicial complex $X^{\Delta^\bullet_{inf}}$.

In internal [[topos]]-theoretic language the definition of $X^{\Delta^\bullet_{inf}}$ is simple, straightforward and transparent: in degree $k$ the space $X^{\Delta^k_{inf}}$ is  given by the formula

$$
  X^{\Delta^k_{inf}} = \{ (x_0, \cdots, x_k) \in X^k | \forall i,j,\;  x_i \approx x_j\}
  \,,
$$

where $x \approx y$ means that $x$ is an infinitesimal neighbor of $y$.

In this form the infinitesimal singular simplicial complex is discussed in [section 2.8](http://home.imf.au.dk/kock/SGM-final.pdf#page=89) of

* Anders Kock, _Synthetic geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

The details of what $X^{\Delta^k_{inf}}$ is like in terms of the generic concrete model of spaces dual to function algebras are in section 1 of

* Breen, Messing, _Combinatorial differential forms_ ([pdf](http://arxiv.org/abs/math/0005087))

As the title suggests, the infinitesimal singular simplicial complex is tightly related to [[differential forms in synthetic differential geometry]]: the deRham complex is the normalized [[Moore complex|Moore cochain complex]] of the [[cosimplicial algebra]] $C^\infty(X^{\Delta^\bullet_{inf}})$ of functions on the spaces of infinitesimal simplices.

#In nonstandard analysis#

There is also a version of the infinitesimal singular simplicial context in the context of [[nonstandard analysis]]. See

* Zivaljevic, _On a cohomology theory based on hyperfinite sums of microcomplexes_ .
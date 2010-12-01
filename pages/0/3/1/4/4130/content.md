
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

**Subdivision** is a usually functorial process which takes as input some combinatorial notion of space (for example, a [[simplicial complex]] or [[simplicial set]]) and produces as output a more finely meshed space. It is related to the notion of [[classical triangulation|classical subdivision]].



## Definition and Properties

There are several versions of this, some of which we describe by appeal to the diagram 

$$SimpComplex \stackrel{\overset{U}{\to}}{\underset{Flag}{\leftarrow}} Pos \stackrel{\overset{nerve}{\to}}{\underset{Face}{\leftarrow}} Set^{\Delta^{op}}$$

In this diagram, 

* The [[functor]] $U$ sends a simplicial complex $(V, \Sigma)$ to $\Sigma$, regarded as a [[poset]] ordered by inclusion, 

* The functor $Flag$ sends a poset $P$ to the simplicial complex whose vertex set is $P$ and whose [[simplex|simplices]] are the underlying sets $\{x_0, \ldots, x_n\}$ of flags $x_0 \lt \ldots \lt x_n$, 

* The functor $Face$ sends a simplicial set $X$ to the poset whose elements are nondegenerate simplices (elements) of $X$, ordered by $x \leq y$ if there is some monomorphism $i: [m] \to [n]$ such that $X(i)(y) = x$. 

* The functor $nerve$ is the usual [[nerve]] functor restricted to the category of posets [[Pos]] $\hookrightarrow$ [[Cat]] .

+-- {: .un_thm}
###### Theorem 
Let $|(-)|_{sc}: SimpComplex \to Top$ and $|(-)|_{ss}: Set^{\Delta^{op}} \to Top$ denote the usual [[geometric realization]] functors. Then 

1. $|(nerve \circ Face)(X)|_{ss} \cong |X|_{ss}$

1. $|(Flag \circ Face)(X)|_{sc} \cong |X|_{ss}$

1. $|(nerve \circ U)(S)|_{ss} \cong |S|_{sc}$

1. $|(Flag \circ U)(S)|_{sc} \cong |S|_{sc}$
=-- 

Each of the four composite functors displayed on the left sides of these [[isomorphism]]s is called a **subdivision** functor. 


## Applications

The functor $nerve \circ Face$ can be used to construct [[Kan fibrant replacement]]s in the [[model structure on simplicial sets]]. In that context it is usually called "$Ex$".

This functorial subdivision corresponds to the classical [[barycentric subdivision]].  Other [[classical triangulation|classical subdivision]]s that are frequently encountered include the middle edge subdivision.  This latter is closely related to the [[ordinal subdivision]] of simplicial sets.


[[!redirects subdivisions]]
[[!redirects barycentric subdivision]]
[[!redirects barycentric subdivisions]]
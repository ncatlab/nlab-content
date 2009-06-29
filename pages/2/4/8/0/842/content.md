#Idea#

The notion of [[limit]] generalizes to [[quasi-category|quasi-categories]] straightforwardly using the generalization of [[over category]] and [[terminal object]] to [[over quasi-category]] and [[terminal object in a quasi-category]].


#Definition#

For $K$ and $C$ two [[quasi-category|quasi-categories]] and $F : K \to C$ a morphism of [[quasi-category|quasi-categories]], the **limit** over $F$ is, if it exists, the [[terminal object in a quasi-category|quasi-categorical terminal object]] in the [[over quasi-category|over quasi-categories]] $C_{/F}$:

$$
  lim F := TerminalObj(C_{/F})
  \,.
$$

#Examples#

## Homotopy limits in Kan-enriched categories ##

Let $K$ and $C$ be categories [[enriched category|enriched]] in [[Kan complex|Kan complexes]] and $F : K \to C$ a morphism of Kan-enriched categories (i.e. an [[SimpSet]]-functor). Then the [[homotopy limit]] of $F$ (computed for instance as described at [[weighted limit]]) coincides with the quasi-categorical limit of $F$ under the embedding of simplicial categories into quasi-categories.

This is [theorem 4.2.4.1, p. 214](http://www-math.mit.edu/~lurie/topoibook/highertopoi.pdf#page=214) in Lurie's book (see below).


#References#

The definition of limit in quasi-categories is due to

* A. Joyal, _Quasi-categories and Kan complexes_ Journal of Pure and Applied Algebra 175 (2002), 207-222.

It appears as [definition 1.2.13.4, p. 48](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=48) in 

* J. Lurie, _Higher topos theory_ ([pdf](http://arxiv.org/abs/math.CT/0608040))


[[!redirects limits in quasi-categories]]
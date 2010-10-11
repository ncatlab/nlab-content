
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _differential structure_ on a [[topological space]] $X$ is the extra structure of a [[differential manifold]] on $X$. A _smooth structure_ on $X$ is the extra structure of a [[smooth manifold]].


## Definition

For $k \in \mathbb{R}$ a **$C^k$-differential structure** on a [[topological space]] $X$ is a [[manifold]] $\hat X$ whose charts have transition functions that have continuous [[derivative]]s to degree $k$, such that $X$ is the topological space underlying $\hat X$.

A **smooth structure** on $X$ is a [[smooth manifold]] $\hat X$ (transition functios have derivatives to all degrees) with underlying topological space $X$.

## Properties

+-- {: .un_theorem}
###### Theorem

For $n \in \mathbb{N}$ a [[natural number]] with $n \neq 4$, there is a unique (up to [[isomorphism]]) smooth structure on the [[Cartesian space]] $\mathbb{R}^n$. 

=--

This was shown in ([Stallings](#Stallings)).

+-- {: .un_theorem}
###### Theorem

In $d = 4$ the analog of this statement is false. One says that on $\mathb{R}^4$ there exist [[exotic smooth structure]]s.
 
=--

### Exotic smooth structures

Many topological spaces have canonical or "obvious" smooth structures. For instance a [[Cartesian space]] $\mathbb{R}^n$ has the evident smooth structure induced from the fact that it can be covered by a single chart -- itself.

From this example, various topological spaces inherit a canonical smooth structure by embedding. For instance the $n$-[[sphere]] may naturally be thought of as the collection of points

$$
  S^n \hookrightarrow \mathbb{R}^n 
$$

given by $S^n = \{\vec x \in \mathbb{R}^n | \sum_i (x^i)^2 = 1\}$ and this induces a smooth structure of $\mathbb{S}^n$.

But there may be other, non-equivalent smooth structures than these canonical ones. These are called [[exotic smooth structure]]s. See there for more details.

## References

* [[John Stallings]], _The piecewise linear structure of Euclidean space_ , Proc. Cambridge Philos. Soc. 58 (1962), 481-488. ([pdf](http://journals.cambridge.org/production/action/cjoGetFulltext?fulltextid=2118140))
{#Stallings}

[[!redirects differential structure]]
[[!redirects differential structures]]
[[!redirects smooth structures]]

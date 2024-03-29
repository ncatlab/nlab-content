
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
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

+-- {: .num_defn #SmoothStructure}
###### Definition
**(smooth structure)**

Let $X$ be a [[topological manifold]] and let 

$$
  \left(
    \mathbb{R}^n \underoverset{\simeq}{\phi_i}{\longrightarrow} U_i \subset X
  \right)_{i \in I}
  \phantom{AAA}
   \text{and}
  \phantom{AAA}
  \left(
    \mathbb{R}^{n} \underoverset{\simeq}{\psi_j}{\longrightarrow} V_j \subset X
  \right)_{j \in J}
$$

be two [[atlases]], both making $X$ into a [[smooth manifold]] ([this def.](differentiable+manifold#DifferentiableManifold)).

Then there is a [[diffeomorphism]] of the form

$$
  f
  \;\colon\;
  \left(
    X 
      \;,\;
    \left(
      \mathbb{R}^n \underoverset{\simeq}{\phi_i}{\longrightarrow} U_i \subset X
    \right)_{i \in I}    
  \right)
    \overset{\simeq}{\longrightarrow}
  \left(
    X\;,\;
    \left(
      \mathbb{R}^{n} \underoverset{\simeq}{\psi_j}{\longrightarrow} V_j \subset X
    \right)_{j \in J}
  \right)
$$

precisely if the [[identity function]] on the underlying set of $X$ constitutes such a diffeomorphism.
(Because if $f$ is a diffeomorphism, then also $f^{-1}\circ f = id_X$ is a diffeomorphism.)

That the identity function is a diffeomorphism between $X$ equipped with these two atlases means (by [definition](differentiable+manifold#DifferentiableManifold)) that 

$$
  \underset{{i \in I} \atop {j \in J}}{\forall}
  \left(
    \phi_i^{-1}(V_j) \overset{\phi_i}{\longrightarrow} V_j \overset{\psi_j^{-1}}{\longrightarrow} \mathbb{R}^n
    \phantom{AA}
    \text{is smooth}
  \right)
  \,.
$$

Hence diffeomorphsm induces an [[equivalence relation]] on the set of 
smooth atlases that exist on a given [[topological manifold]] $X$. An [[equivalence class]]
with respect to this equivalence relation is called a _smooth structure_ on $X$.

=--

## Properties

+-- {: .num_theorem #UniquenessOfSmoothStructures}
###### Theorem
**(uniqueness of smooth structure on [[Euclidean space]] in $d \neq 4$)

For $n \in \mathbb{N}$ a [[natural number]] with $n \neq 4$, there is a unique (up to [[isomorphism]]) smooth structure on the [[Cartesian space]] $\mathbb{R}^n$. 

=--

This was shown in ([Stallings 62](#Stallings62)).

+-- {: .num_theorem}
###### Theorem

In $d = 4$ the analog of this statement is false. One says that on $\mathbb{R}^4$ there exist [[exotic smooth structure]]s.
 
=--

### Exotic smooth structures

Many topological spaces have canonical or "obvious" smooth structures. For instance a [[Cartesian space]] $\mathbb{R}^n$ has the evident smooth structure induced from the fact that it can be covered by a single chart -- itself.

From this example, various topological spaces inherit a canonical smooth structure by embedding. For instance the $n$-[[sphere]] may naturally be thought of as the collection of points

$$
  S^n \hookrightarrow \mathbb{R}^n 
$$

given by $S^n = \{\vec x \in \mathbb{R}^n | \sum_i (x^i)^2 = 1\}$ and this induces a smooth structure of $\mathbb{S}^n$.

But there may be other, non-equivalent smooth structures than these canonical ones. These are called [[exotic smooth structure]]s. See there for more details.

## Related concepts

* [[smooth structure on a topos]]

## References

* {#Stallings62} [[John Stallings]], _The piecewise linear structure of Euclidean space_ , Proc. Cambridge Philos. Soc. 58 (1962), 481-488. ([pdf](http://journals.cambridge.org/production/action/cjoGetFulltext?fulltextid=2118140))


See also

* Wikipedia, _[Smooth structure](https://en.wikipedia.org/wiki/Smooth_structure)_


[[!redirects differential structure]]
[[!redirects differential structures]]
[[!redirects smooth structures]]

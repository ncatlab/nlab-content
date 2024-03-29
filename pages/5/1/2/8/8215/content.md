
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $S$ a [[simplicial set]] and $A$ an [[abelian group]], the _simplicial [[homology]]_ of $S$ is the [[chain homology]] of the [[chain complex]] corresponding under the [[Dold-Kan correspondence]] to the [[simplicial abelian group]] $S \cdot A$ of $A$-[[chains]] on $S$: [[formal linear combinations]] of [[simplices]] in $S$ with [[coefficients]] in $A$.

## Definition

Let $S$ be a [[simplicial set]] and $A$ an [[abelian group]].

+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$ write 

$$
  S_n \cdot A \coloneqq \mathbb{Z}[S_n] \otimes A
$$

for the [[free abelian group]] on the set $S_n$  of $n$-[[simplices]] [[tensor product of abelian groups|tensored]] with $A$: the group of [[formal linear combinations]] of $n$-simplices with [[coefficients]] in $A$.

These abelian groups arrange to a [[simplicial abelian group]]

$$
  X \cdot A \in Ab^{\Delta^{op}}
  \,.
$$

The [[alternating face map complex]] of these groups is called the **complex of simplicial chains** on $S$

$$
  C_\bullet(S \cdot A) = C_\bullet(S,A)
  \,.
$$

The **simplicial homology** of $S$ is the [[chain homology]] of the complex of simplicial chains:

$$
  H_\bullet(S, A)
  \coloneqq
  H_\bullet(C_\bullet(S,A))
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

This means that the [[differentials]] in $C_\bullet(S,A)$ are given on [[basis]] elements $\sigma \in S_n$ by the [[formal linear combination]]

$$
  \partial \sigma
    = 
  \sum_{k = 0}^{n} (-1)^k d_k \sigma
  \,,
$$

where $d_k : S_n \to S_{n-1}$ are the [[face maps]] of $S$.

=--

## Examples

### Explicit

+-- {: .num_example #OfTetrahedon}
###### Example

Let $S = \partial \Delta^3$ be the [[boundary of a simplex|boundary]] of the simplicial  3-[[simplex]], the (hollow) simplicial [[tetrahedron]].

Since this has 

* 4 non-degenerate vertices

* 6 non-degenerate edges

* 4 non-degenerate faces

the [[normalized chain complex]] of $\mathbb{Z}$ is of the form

$$
  \cdots \to 0 \to 0 \to \mathbb{Z}^4 \to \mathbb{Z}^6 \to \mathbb{Z}^4 \to 0
  \,.
$$

By writing out the two non-trivial differentials, one can deduce explicitly that 

* $H_0(\partial \Delta^3) = \mathbb{Z}$ (reflecting the fact that the tetrahedron is [[connected topological space|connected]]);

* $H_1(\partial \Delta^3) = 0$ (reflecting the fact that it is [[simply-connected topological space|simply-connected]]);

* $H_2(\partial \Delta^3) = \mathbb{Z}$ (reflecting the fact, by the [[Hurewicz theorem]], that the second [[homotopy group]] of the 2-sphere is $\mathbb{Z}$ );


=--


### General

* For $X$ a [[topological space]] and $S = Sing X$ the [[singular simplicial complex]] of $X$, the simplicial homology of $Sing X$ is called the _[[singular homology]]_ of $X$, denoted $H_\bullet(X,A)$.


## Related concepts

* [[cochain on a simplicial set]]

* [[singular homology]]

## Terminology and a bit of history

The term simplicial homology is also used in the literature for the homology of polyhedral spaces, based on the theory of [[simplicial complex]]es.  That homology is defined by first looking at a chain complex of simplicial chains on, say, a triangulation of a space, and then passing to the corresponding homology.  The theory then proceeds by proving that the end result is independent of the triangulation used.  The resulting homology theory is isomorphic to singular homology, but historically was the earlier theory.

## References

A basic discussion is for instance around application 1.1.3 of 

* [[Charles Weibel]]. _[[An Introduction to Homological Algebra]]_

Homology for spaces  is discussed in chapter 2 of 

*  [[Alan Hatcher]], [Algebraic topology](http://www.math.cornell.edu/~hatcher/AT/AT.pdf), Cambridge Univ. Press 2002, starting p. 106

and this includes a discussion of the homology of simplicial complexes.

[[!redirects chain on a simplicial set]]
[[!redirects chains on a simplicial set]]

[[!redirects simplicial chain]]
[[!redirects simplicial chains]]


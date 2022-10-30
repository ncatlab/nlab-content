
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Write
-
$$
  N : Cat \to sSet
$$

for the [[nerve]] functor from [[Cat]] to [[sSet]]. Write 

$$
  {\vert - \vert} : sSet \to Top
$$

for the [[geometric realization]] of [[simplicial sets]].

The _[[geometric realization]]_ of categories is the composite

$$
  {\vert - \vert} := {\vert N(-)\vert} : Cat \to Top
$$

## Properties

### Thomason model structure

There is a [[model category]] structure on [[Cat]] whose weak equivalences are those [[functor]]s which under geometric realization are weak equivalences in the standard [[model structure on topological spaces]]: the [[Thomason model structure]].

### Recognizing weak equivalences: Quillens theorem A and B

Let $F : C \to D$ be a [[functor]].

+-- {: .num_theorem}
###### Theorem
**(Quillen's theorem A)**

If for all [[object]]s $d \in D$ the geometric realization $\vert F/d\vert$ of the [[comma category]] $F/d$ is [[contractible]], then $\vert f \vert : \vert C \vert \to \vert D \vert  $ is a [[weak homotopy equivalence]].

=--

+-- {: .num_theorem}
###### Theorem
**(Quillen's theorem B)**

If for all $d \in D$ we have that $\vert F/d\vert$ is [[weak homotopy equivalence|weakly homotopy equivalent]] to a given [[topological space]] $X$ and all morphism $f : d_1 \to d_2$ induce weak homotopy equivalences between these, then $X$ is the [[homotopy fiber]] of $\vert f \vert$, hence we have a [[fiber sequence]]

$$
  X \to \vert C \vert \stackrel{\vert f \vert }{\to} \vert D \vert
  \,.
$$

=--

## References

* Jonathan Ariel Barmak, _On Quillen's Theorem A for posets_ ([arXiv:1005.0538](http://arxiv.org/abs/1005.0538))

* [[Clark Barwick]], [[Dan Kan]], _A Quillen theorem $B_n$ for homotopy pullbacks_ ([arXiv:1101.4879](http://arxiv.org/abs/1101.4879))

* [[David Roberts]], _[[davidroberts:Theorem A for topological categories]]_

## Related concepts

* [[geometric realization]]

  * **of categories**, [[geometric realization of simplicial topological spaces|of simplicial topological spaces]], [[geometric realization of cohesive ∞-groupoids|of cohesive ∞-groupoids]]



[[!redirects Quillen's theorem A]]
[[!redirects Quillen's theorem A]]
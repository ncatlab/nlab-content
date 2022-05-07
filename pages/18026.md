
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The definition of (the [[syntactic category]] of) a _[[Lawvere theory]]_ as a [[category]] with certain properties has an immediate generalization to [[simplicial categories]]. 

## Details

+-- {: .num_defn #SimplicialLawvereTheory}
###### Definition

Let $\Gamma = (Skel(FinSet^{\ast/}))$ be [[Segal's category]], the [[opposite category]] of a [[skeleton]] of [[finite set|finite]] [[pointed sets]].

A _[[simplicial Lawvere theory]]_ is a a pointed [[simplicial category]] $T$ equipped with a [[functor]] $i \;\colon\;\Gamma \to T$ such that 

1. $T$ has the same [[set]] of [[objects]] as $\Gamma$;

1. $i$ is the identity on objects

1  $i$ preserves [[finite products]]

Given a simplicial theory $T$, then a _simplicial $T$-algebra_ is a product preserving [[simplicial functor]] $X$ to the [[simplicial category]] of [[pointed simplicial sets]]. The simplicial set

$$
  X(1_+) \in sSet
$$

(the value on the pointed 2-element set) is called the _underlying simplicial set_ of the $T$-algebra.

A [[homomorphism]] of $T$-algebras is a simplicial [[natural transformation]] between such functors. Write

$$
  T Alg \in sSet Cat
$$

for the resulting [[simplicial category]].

A homomorphism is called a _weak equivalence_ or a _fibration_ if on underlying simplicial sets it is a weak equivalence or fibration, respectively, in the [[classical model structure on simplicial sets]].
Write

$$
  (T Alg)_{proj}
$$

for the category equipped with these [[classes]] of morphisms.

=--

([Schwede 01, def. 2.1 and def. 2.2 and beginning of section 3](#Schwede01))


+-- {: .num_prop}
###### Proposition

For $T$ a [[simplicial Lawvere theory]] (def. \ref{SimplicialLawvereTheory}) the category $(T Alg)_{poj}$ from def. \ref{SimplicialLawvereTheory} is a [[simplicial model category]].

=--

This is due to ([Reedy 74, theorem I](#Reedy74)), reviewed in ([Schwede 01](#Schwede01)). For more see at _[[model structure on simplicial algebras]]_.

The analogous statement with the [[classical model structure on simplicial sets]] replaced by the [[classical model structure on topological spaces]] is due to ([Schw&#228;nzl-Vogt 91](#Schw&#228;nzlVogt91)9

## Related concepts

* [[(infinity,1)-algebraic theory]]

## References


* {#Reedy74} [[Christopher Reedy]], _Homology of algebraic theories_, Ph.D. Thesis, University of California, San Diego, 1974

* {#Schw&#228;nzlVogt91} [[Roland Schwänzl]], [[Rainer Vogt]], _The categories of $A_\infty$- and $E_\infty$-monoids and ring spaces as closed simplicial and topological model categories_, Archives of Mathematics 56 (1991) 405-411 ([doi:10.1007/BF01198229](https://doi.org/10.1007/BF01198229))

  > (the [[model structure on simplicial algebras]])

* {#Schwede01} [[Stefan Schwede]], _Stable homotopy of algebraic theories_, Topology 40 (2001) 1-41 ([pdf](http://www.math.uni-bonn.de/people/schwede/stable.pdf))

[[!redirects simplicial Lawvere theories]]

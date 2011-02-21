
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
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

A _simplicial topological group_ is a [[simplicial object]] in the [[category]] of [[topological groups]].

## Properties


Recall for a [[discrete group|discrete]] [[simplicial group]] $G$ the notation $\bar W G \to W G$ for the [[Kan complex]] presentation of the [[universal principal infinity-bundle]] $\mathbf{E}G \to \mathbf{B}G$ from [[simplicial group]]. These constructions for discrete simplicial groups have immediate analogs for simplicial topological groups.

+-- {: .un_def}
###### Definition

Let $G$ be a simplicial topological group. Write $\bar W G \in Top^{\Delta^{op}}$ for the [[simplicial topological space]] whose topological space of $n$-[[simplices]] is the [[product]]

$$
  \bar W G_n := G_{n-1} \times G_{n-2} \cdots \times G_{0}
$$

in [[Top]], equipped wwith the evident (...) face and degeneracy maps.

=--

+-- {: .un_def}
###### Definition

We say a morphism $f : X \to Y$ of [[simplicial topological space]]s is a **global Kan fibration** if for all $n \in \mathbb{N}$ and $0 \leq k \leq n$ the canonical morphism

$$
  X_n \to Y_n \times_{sTop(\Lambda^n_k, Y)} sTop(\Lambda^n_k, X)
$$

in [[Top]] has a [[section]], where 

* $\Lambda^n_k \in $ [[sSet]] $\hookrightarrow Top^{\Delta^{op}}$ is the $k$th $n$-[[horn]] regarded as a [[discrete space|discrete]] [[simplicial topological space]]:

* $sTop(-,-) : sTop^{op} \times sTop \to Top$ is the [[Top]]-[[hom object]].

We say a [[simplicial topological space]] $X_\bullet \in Top^{\Delta^{op}}$ is **(global) Kan simplicial space** if the unique morphism $X_\bullet \to *$ is a global Kan fibration, hence if for all $n \in \mathbb{N}$ and all $0 \leq i \leq n$ the canonical [[continuous function]]

$$
  X_n \to [\Lambda^n_k, X]
$$

into the [[topological space]] of $k$th $n$-[[horn]]s admits a [[section]].

=--

This global notion of Kan simplicial spaces is considered for instance in ([BrownSzczarba](#BrownSzczarba)) and ([May](#May)).

+-- {: .un_prop}
###### Proposition

Let $G$ be a simplicial topological group. Then 

1. $G$ is a globally Kan simplicial topological space;

1. $\bar W G$ is a globally Kan simplicial topological space;

1. $W G \to \bar W G$ is a global Kan fibration.

=--

+-- {: .proof}
###### Proof

The first statement appears as ([BrownSzczarba, theorem 3.8](#BrownSzczarba)), the second is noted in ([Stevenson](#Stevenson)), the third as ([BrownSzczarba, lemma 6.7](#BrownSzczarba)).

=--


+-- {: .un_prop}
###### Proposition

If $G$ is a well-pointed simplicial topological group, then

1. $G$ is a [[nice simplicial topological space|good simplicial topological space]];

1. the [[geometric realization of simplicial topological spaces|geometric realizaiton]] $|G|$ is well-pointed;

1. $\bar W G$ is a [[nice simplicial topological space|proper simplicial topological space]].

=--

+-- {: .proof}
###### Proof

The statement about $\bar W G$ is proven in ([Stevenson](#Stevenson)). The other statements are referenced there.

=--

## Related concepts

* [[simplicial topological space]], [[nice simplicial topological space]]

* **simplicial topological group**

* [[geometric realization of simplicial topological spaces]]

## References

* E. H. Brown and R. H. Szczarba, _Continuous cohomology and real homotopy
type_ , Trans. Amer. Math. Soc. 311 (1989), no. 1, 57 ([pdf](http://www.ams.org/journals/tran/1989-311-01/S0002-9947-1989-0929667-6/S0002-9947-1989-0929667-6.pdf))
{#BrownSzczarba}

* [[Peter May]], _Geometry of iterated loop spaces_ , SLNM 271, Springer-Verlag, 1972.
{#May}

* [[David Roberts]], [[Danny Stevenson]], _Simplicial principal bundles in parametrized spaces_
{#Stevenson}

[[!redirects simplicial topological groups]]

[[!redirects topological simplicial group]]
[[!redirects topological simplicial groups]]

[[!redirects well-pointed simplicial topological group]]
[[!redirects well pointed simplicial topological group]]
[[!redirects well-pointed simplicial topological groups]]
[[!redirects well pointed simplicial topological groups]]

[[!redirects well-sectioned simplicial topological group]]
[[!redirects well sectioned simplicial topological group]]
[[!redirects well-sectioned simplicial topological groups]]
[[!redirects well sectioned simplicial topological groups]]
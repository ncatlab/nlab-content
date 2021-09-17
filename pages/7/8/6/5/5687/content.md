
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

+-- {: .num_defn}
###### Definition

A _simplicial topological group_ is a [[simplicial object]] in the [[category]] of [[topological groups]].

=--

For various applications the ambient category [[Top]] of [[topological space]]s is taken specifically to be 

* the [[category]] of [[compactly generated space|compactly generated]] [[weakly Hausdorff space]]s, or

* or the category of [[k-space]]s.

We take [[Top]] to be the category of [[k-space]]s in the following.

+-- {: .num_defn #WellPointedSimplicialTopologicalGroup}
###### Definition

A simplicial topological group $G$ is called **well-pointed** if for $*$ the trivial simplicial topological group and $i : * \to G$ the unique [[homomorphism]], all components $i_n : * \to G_n$ are [[closed cofibrations]].

=--

For $B \in Top$ a fixed base object, it is often desirable to work in "$B$-parameterized families", hence in the [[over-category]] $Top/B$ (see [MaySigurdson](#MaySigurdson)). There is the 
[[Strøm model structure|relative Strøm model structure]] on $Top/B$.

+-- {: .num_defn}
###### Definition

A simplicial group in $G$ in $Top/B$ is called **well-sectioned** if for $B$ the trivial simplicial topological group over $B$ and $i : B \to G$ the unique [[homomorphism]], all components $i_n : B \to G_n$ are $\bar f$-cofibrations.

=--


## Properties


Recall for a [[discrete group|discrete]] [[simplicial group]] $G$ the [[simplicial classifying space]] coprojection  $W G \to \overline{W} G$, being a [[Kan complex]] presentation of the [[universal principal infinity-bundle]] $\mathbf{E}G \to \mathbf{B}G$ from [[simplicial group]]. These constructions for discrete simplicial groups have immediate analogs for simplicial topological groups.

+-- {: .num_defn}
###### Definition

Let $G$ be a simplicial topological group. Write $\bar W G \in Top^{\Delta^{op}}$ for the [[simplicial topological space]] whose topological space of $n$-[[simplices]] is the [[product]]

$$
  \bar W G_n := G_{n-1} \times G_{n-2} \cdots \times G_{0}
$$

in [[Top]], equipped with the evident face and degeneracy maps (see at *[[simplicial classifying space]]*).

=--

+-- {: .num_defn}
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
  X_n \to sTop(\Lambda^n_k, X)
$$

into the [[topological space]] of $k$th $n$-[[horn]]s admits a [[section]].

=--

This global notion of Kan simplicial spaces is considered for instance in ([BrownSzczarba](#BrownSzczarba)) and ([May](#May)).

+-- {: .num_prop}
###### Proposition

Let $G$ be a simplicial topological group. Then 

1. $G$ is a globally Kan simplicial topological space;

1. $\bar W G$ is a globally Kan simplicial topological space;

1. $W G \to \bar W G$ is a global Kan fibration.

=--

+-- {: .proof}
###### Proof

The first statement appears as ([BrownSzczarba, theorem 3.8](#BrownSzczarba)), the second is noted in ([Roberts & Stevenson 2012](#RobertsStevenson12)), the third as ([BrownSzczarba, lemma 6.7](#BrownSzczarba)).

=--



\begin{proposition}\label{RealizationOfWellPointedIsWellPointed}
If $G$ is a [well-pointed](#WellPointedSimplicialTopologicalGroup) simplicial topological group, then

1. $G$ is a [[nice simplicial topological space|good simplicial topological space]];

1. $\overline{W} G$ is a [[nice simplicial topological space|proper simplicial topological space]];

1. the [[geometric realization of simplicial topological spaces|geometric realization]] $|G|$ is well-pointed.

\end{proposition}

([Roberts & Stevenson 2012, Prop. 3](#RobertsStevenson12), for the last item see also [Baez & Stevenson 2008, Lem. 1](#BaezStevenson08))

## Related concepts

* [[simplicial topological space]], [[nice simplicial topological space]]

* [[simplicial group]], [[simplicial abelian group]]

* [[geometric realization of simplicial topological spaces]]

## References

Basics theory of simplicial topological groups is in

* E. H. Brown and R. H. Szczarba, _Continuous cohomology and real homotopy
type_ , Trans. Amer. Math. Soc. 311 (1989), no. 1, 57 ([pdf](http://www.ams.org/journals/tran/1989-311-01/S0002-9947-1989-0929667-6/S0002-9947-1989-0929667-6.pdf))
{#BrownSzczarba}

and

* [[Peter May]], _Geometry of iterated loop spaces_ , SLNM 271, Springer-Verlag, 1972 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))
{#May}

Discussion of their [[geometric realization of simplicial topological spaces|geometric realization]] and [[principal infinity-bundles|principal $\infty$-bundles]]:

* {#BaezStevenson08} [[John Baez]], [[Danny Stevenson]], _The Classifying Space of a Topological 2-Group_,  In: Baas N., Friedlander E., Jahren B., Østvær P. (eds.) Algebraic Topology_. Abel Symposia, vol 4. Springer 2009 ([arXiv:0801.3843](https://arxiv.org/abs/0801.3843), [doi:10.1007/978-3-642-01200-6_1](https://doi.org/10.1007/978-3-642-01200-6_1))

* {#RobertsStevenson12} [[David Roberts]], [[Danny Stevenson]], _Simplicial principal bundles in parametrized spaces_, New York Journal of Mathematics Volume 22 (2016) 405-440 ([arXiv:1203.2460](http://arxiv.org/abs/1203.2460), [nyjm:22-19](http://nyjm.albany.edu/j/2016/22-19.html))




Discussion of [[homotopy theory]] over a base $B$ is in

* [[Peter May]], [[Johann Sigurdsson]], _[[Parametrized Homotopy Theory]]_ ([web](http://www.math.uiuc.edu/K-theory/0716/))

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
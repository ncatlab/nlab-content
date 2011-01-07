
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $X_\bullet$ a [[simplicial object]] in [[Top]] --  a [[simplicial topological space]] -- its _geometric realization_ is a plain [[topological space]] $|X_\bullet| \in Top$ whose construction is a direct analog of the ordinary notion of [[geometric realization]] of a [[simplicial set]], but taking into account the topology on the spaces of $n$-simplices $X_n$.

## Definition

Let [[Top]] in the following denote the [[category]] of [[compactly generated space|compactly generated]] [[Hausdorff space]]s.

Write $\Delta_{Top} : \Delta \to Top : [n] \mapsto \Delta^n_{Top}$ for the standard [[cosimplicial object|cosimplicial]] [[topological space]].

For $X_\bullet : \Delta^{op} \to Top$ any simplicial topological space, its _geometric realization_ is the [[coend]]

$$
  |X_\bullet| :  \int^{n \in \Delta} X_n \times \Delta^n_{Top}
$$

formed in [[Top]].


This naturally extends to a functor

$$
  |-| : Top^{\Delta^{op}} \to Top
  \,.
$$

One also considers geometric realization after restricting to the subcategory $\Delta_+ \hookrightarrow \Delta$ of the [[simplex category]] on the strictly increasing maps. The corresponding coend is called the **fat geometric realization** 

$$
  \Vert X_\bullet\Vert :  \int^{n \in \Delta_+} X_n \times \Delta^n_{Top}
$$

(fat, because it does not divide out the relations induced by the degeneracy maps and hence is "bigger" than ordinary geometric realization).


## Properties

+-- {: .un_lemma}
###### Observation

If $X_\bullet : \Delta^{op} \to Set \hookrightarrow Top$ is a degreewise [[discrete space]], hence just a [[simplicial set]], the notion of geometric realization above coincided with the notion of [[geometric realization|geometric realization of simplicial sets]].

=--


+-- {: .un_prop}
###### Proposition

Geometric realization preserves [[pullback]]s: for $X_\bullet \to Y_\bullet \leftarrow Z_\bullet$ a [[diagram]] in $Top^{\Delta^{op}}$ there are [[natural transformation|natural]] [[homeomorphism]]s

$$
  |X_\bullet| \times_{|Y_\bullet|} |Z_\bullet|
  \simeq
  |X_\bullet \times_{Y_\bullet} Z_\bullet|
  \,.
$$

=--

See for instance corollary 11.6 of ([May](#May)).

In certain cases geometric realisation computes the [[homotopy colimit]] of the diagram $X_\bullet : \Delta^{op} \to Top$ given by the simplicial space, with respect to the standard [[model structure on topological spaces]].

+-- {: .un_defn}
###### Definition 

A simplicial topological space $X_\bullet$ is _good_ in the sense of [[Graeme Segal|Segal]] if all the degeneracy maps $X_{n-1} \hookrightarrow X_n$ are closed cofibrations.

=--

+-- {: .un_defn}
###### Definition

A simplicial topological space $X_\bullet$ is _proper_ in the sense of [[Peter May|May]] if the inclusion $sX_n \hookrightarrow X_n$ of the degenerate simplices is a closed cofibration, where $sX_n = \bigcup_i s_i(X_{n-1})$.

=--

For more on these conditions see [[simplicial topological space]].

+-- {: .un_prop}

###### Proposition

A good simplicial topological space is proper.

=--

_Proof._ This appears to be a folk statement. A proof can be found in unpublished work by [[David Roberts]] and [[Danny Stevenson]].

+-- {: .un_prop}

###### Proposition

Let $X_\bullet$ be a simplicial topological space. Then there is a natural [[weak homotopy equivalence]] 
$$
 \Vert X_\bullet\Vert \simeq hocolim_{n \in \Delta} X_n
$$
If moreover $X_\bullet$ is proper, then the natural morphism  $ \Vert X\Vert \to |X|$ is a weak homotopy equivalence.

=-- 

+-- {: .un_remark}

###### Remark

In case $X_\bullet$ is a good simplicial topological space, a direct (i.e., not using the fact that goodness implies properness) proof that $ \Vert X\Vert  \to |X|$ is a weak homotopy equivalence has been sketched by Graeme Segal and then refined by Tammo tom Dieck.

=--


## References

A standard textbook reference is chapter 11 of

* [[Peter May]], _The geometry of iterated loop spaces_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))
{#May}


[[!redirects geometric realization of a simplicial space]]
[[!redirects geometric realization of simplicial spaces]]

[[!redirects fat geometric realization of simplicial spaces]]
[[!redirects fat geometric realization of simplicial topological spaces]]

[[!redirects fat realization]]
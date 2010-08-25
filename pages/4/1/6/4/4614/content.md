
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

In certain cases geometric realisation computes the homotopy colimit of the diagram given by the simplicial space. A sufficient condition (goodness, due to Segal) is that the degeneracy maps $X_{n-1} \hookrightarrow X_n$ are all closed cofibrations. Another (properness, due to May) is that the inclusion $sX_n \hookrightarrow X_n$ of the degenerate simplices is a closed cofibration, where $sX_n = \bigcup_i s_i(X_{n-1})$. The former condition implies the latter.

When these conditions are not met, then the [[fat realization]] $||X||$ of the simplicial space, i.e. the coend of the diagram given by restricting to the subcategory of $\Delta$ with only the coface maps. Generally, there is a map $||X|| \to |X|$ which is a (weak?) homotopy equivalence when $X$ is good or proper (this is in the 'good' case I think due to Segal, and Tammo tom Dieck finished up/cleaned up the proof).

+--{: .query}
[[David Roberts]]: this needs expanding/clarifying. I'm not sure who the result that good $\Rightarrow$ proper is due to, but I proved it in unpublished work with [[Danny Stevenson]]. I'm sure we're not the first, but it seems like folklore.
=--


## References

A standard textbook reference is chapter 11 of

* [[Peter May]], _The geometry of iterated loop spaces_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))
{#May}


[[!redirects geometric realization of a simplicial space]]
[[!redirects geometric realization of simplicial spaces]]


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


## References

A standard textbook reference is chapter 11 of

* [[Peter May]], _The geometry of iterated loop spaces_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))
{#May}


[[!redirects geometric realization of a simplicial space]]
[[!redirects geometric realization of simplicial spaces]]

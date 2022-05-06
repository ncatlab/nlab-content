
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
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

## Idea

The [[category]] of [[dendroidal sets]] is often denoted $dSet$ or similar, following the common denotation _[[sSet]]_ for the [[category]] of [[simplicial sets]].

## Properties


Some [[mathematical structure|structure]] carried by the [[category]] [[dSet]] of [[dendroidal sets]]:


### $sSet$-enriched structure 

Using the fact that [[dSet]] is a [[closed monoidal category]] with [[internal hom]] dendroidal sets $[C,D]$ for dendroidal sets $C$ and $D$, and using the functor $i^* : dSet \to SSet$ we obtain canonically the structure of an [[simplicially enriched category]] / [[sSet]]-[[enriched category]] on $dSet$ with the hom-simplicial set between $C$ and $D$ being $i^*[C,D]$.




### Model category structure

The category $dSet$ of [[dendroidal sets]] carries a [[monoidal model category|monoidal]] [[model category]]-[[structure]] -- the [[model structure on dendroidal sets]] -- which serves to [[presentable (infinity,1)-category|present]] the [[(∞,1)-category]] of [[(∞,1)-operads]]:

Together with the fact that $i^*: dSet \to sSet$ is a [[right Quillen functor]] (with respect to the [[model structure for quasi-categories]]) this imples that [[dSet]] is an $sSet_{Joyal}$-[[enriched model category]] (but not, without further work, an $sSet_{Quillen}$-enriched model category!).


[[!include table - models for (infinity,1)-operads]]

## Related entries

* [[model structure on dendroidal sets]]

* [[sSet]]


## References

See the [list of references](dendroidal+set#References) at _[[dendroidal set]]_.

For instance:

* [[Ieke Moerdijk]] and [[Ittay Weiss]], _Dendroidal Sets_, Algebraic and Geometric Topology, Volume 7, Number 3 (2007), 1441-1470. ([doi:10.2140/agt.2007.7.1441](https://msp.org/agt/2007/7-3/p13.xhtml), [arXiv:math/0701293](https://arxiv.org/abs/math/0701293))

category: category
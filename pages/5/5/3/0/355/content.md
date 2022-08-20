
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
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

An $n$-groupoid is an 

* [[n-category]] in which all [[k-morphism]]s are [[equivalence]]s;

* [[(n,r)-category|(n,0)-category]];

* $n$-[[truncated]] [[∞-groupoid]] (a [[homotopy n-type]]).



## Definitions

In terms of a known notion of [[(n,r)-category]], we can define an __$n$-groupoid__ explicitly as an $\infty$-category such that:

* every $j$-morphism (at any level) is an [[equivalence]];
* every parallel pair of $j$-morphisms is equivalent, for $j\gt n$.

Or we define an __$n$-groupoid__ abstractly as an [[n-truncated object of an (infinity,1)-category|n-truncated object in]] the [[(∞,1)-category]] [[∞Grpd]].

The $n$-groupoids form an [[(n,1)-category|(n+1,1)-category]], [[nGrpd]].

## Models

### As Kan complexes
 {#AsKanComplexes}

A general model for [[∞-groupoids]] is provided by [[Kan complexes]] (the [[fibrant objects]] in the [[classical model structure on simplicial sets]] which [[presentable (infinity,1)-category|presents]] [[∞Grpd]]). 

In this context an  $n$-groupoid in the general sense is modeled by a Kan complex all of whose [[homotopy groups]] vanish in degree $k \gt n$. In this generality one also speaks of a *[[homotopy n-type|homotopy $n$-type]]* or an *[[n-truncated object of an (infinity,1)-category|$n$-truncated object]]* of [[∞Grpd]]. 

Every such $n$-type is [[equivalence in an (infinity,1)-category|equivalent]] to a "small" model, an $(n+1)$-[[coskeletal]] Kan complex (see [there](simplicial+skeleton#Truncation)): one in which every $k$-sphere $\partial \Delta^{k+1}$ for $k \geq n+1$ has a _unique_ filler. 

Yet a bit smaller than this are Kan complexes that is an $n$-[[hypergroupoid]], where in addition to these sphere-fillers also the [[horn]] fillers in degree $n+1$ are unique.

(For [[1-groupoids]]/[1-hypergroupoids](hypergroupoid#OneHypergroupoids)  this situation is further spelled out [here](simplicial+skeleton#CoskeletalityOfSimplicialNervesOfCategories)).



## Related entries

[[!include homotopy n-types - table]]


* [[homotopy n-type]] / [[n-groupoid]] / [[n-truncated object in an (∞,1)-category]]

* [[model structure for homotopy n-types]]




[[!redirects n-groupoid]]
[[!redirects n-groupoids]]

[[!redirects k-groupoid]]
[[!redirects k-groupoids]]

[[!redirects 4-groupoid]]
[[!redirects 4-groupoids]]

[[!redirects higher groupoid]]
[[!redirects higher groupoids]]

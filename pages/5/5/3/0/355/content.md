
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* [[groupoid]]

* [[2-groupoid]]

* [[3-groupoid]]

* **n-groupoid**

* [[∞-groupoid]]


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

An $n$-groupoid is an 

* [[n-category]] in which all [[k-morphism]]s are [[equivalence]]s;

* [[(n,r)-category|(n,0)-category]];

* $n$-[[truncated]] [[∞-groupoid]] (a [[homotopy n-type]]).



## Definitions

In terms of a known notion of [[(n,r)-category]], we can define an __$n$-groupoid__ explicitly as an $\infty$-category such that:

* every $j$-morphism (at any level) is an [[equivalence]];
* every parallel pair of $j$-morphisms is equivalent, for $j > n$.

Or we define an __$n$-groupoid__ abstractly as an [[n-truncated object of an (infinity,1)-category|n-truncated object in]] the [[(∞,1)-category]] [[∞Grpd]].

## Models

### As Kan complexes

A general model for [[∞-groupoid]]s are [[Kan complex]]es. In this context an  $n$-groupoid in the general sense is modeled by a Kan complex all whose [[homotopy group]]s vanish in degree $k \gt n$. In this generality one also speaks of a [[homotopy n-type]]. 

Every such $n$-type is equivalent to a "small" model, an $(n+1)$-[[coskeletal]] Kan complex: one in which every $k$-sphere $\partial \Delta^{k+1}$ for $k \geq n+1$ has a _unique_ filler.

Even a bit smaller than this is a Kan complex that is an $n$-[[hypergroupoid]], where in addition to these spheres also the [[horn]] fillers in degree $n+1$ are unique.


[[!redirects n-groupoid]]
[[!redirects n-groupoids]]

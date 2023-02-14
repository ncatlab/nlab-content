
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

* [[n-truncation modality]]

## References

Discussion of [[homotopy n-types|homotopy $n$-types]]/[[n-truncated object in an (infinity,1)-category|$n$-truncated objects]] in [[homotopy type theory]]:

* [[Univalent Foundations Project]], §7 of: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* [[Nicolai Kraus]], *Truncation levels in Homotopy Type Theory*, Nottingham (2015) &lbrack;[pdf](https://eprints.nottingham.ac.uk/28986/1/thesis.pdf), [eprints:28986](https://eprints.nottingham.ac.uk/28986)&rbrack;

* [[Felix Cherubini]], [[Egbert Rijke]], Thm. 3.10 of: *Modal Descent*, Mathematical Structures in Computer Science , **31** 4 (2021) 363-391  &lbrack;[doi:10.1017/S0960129520000201](https://doi.org/10.1017/S0960129520000201), [arXiv:2003.09713](https://arxiv.org/abs/2003.09713)&rbrack;




[[!redirects n-groupoid]]
[[!redirects n-groupoids]]

[[!redirects k-groupoid]]
[[!redirects k-groupoids]]

[[!redirects 4-groupoid]]
[[!redirects 4-groupoids]]

[[!redirects higher groupoid]]
[[!redirects higher groupoids]]

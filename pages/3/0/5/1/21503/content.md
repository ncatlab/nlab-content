
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
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

There may be different [[model category]]-[[mathematical structure|structures]] on the [[category]] of [[diffeological spaces]].

Of practical interest would be a model structure whose [[weak equivalences]] are the [[isomorphisms]] on standard _smooth_ [[homotopy groups]] of [[diffeological spaces]], i.e. the [[weak equivalences]] between the [[cohesive shapes]] of [[diffeological spaces]] regarded as the [[concrete objects]] in the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoids]]. By the discussion at _[[shape via cohesive path ∞-groupoid]]_ these are detected by smooth functions out of [[simplices]] or [[cubes]] with their canonical diffeological structure (as discussed in [Christensen-Wu 14](#ChristensenWu14)).

A model category with this property has been claimed in [Haraguchi-Shimakawa 13](#HaraguchiShimakawa13),, [Haraguchi-Shimakawa 20](#HaraguchiShimakawa20)

Another model category structure is discussed in [Kihara 16](#Kihara16), but this uses a non-standard diffeology on simplices (to enforce that all smooth [[singular simplicial complexes]] are [[fibrant objects]]).

## Details


The approach of [Haraguchi-Shimakawa 13](#HaraguchiShimakawa13), [Haraguchi-Shimakawa 20](#HaraguchiShimakawa20)
proceeds as follows:


[[!include adjunction between topological spaces and diffeological spaces]]


## References
 {#References}

A proof of a model structure on diffeological spaces, with weak equivalences detected on standard smooth homotopy groups, is claimed in 

* {#HaraguchiShimakawa13} [[Tadayuki Haraguchi]], [[Kazuhisa Shimakawa]], _A model structure on the category of diffeological spaces_ ([arXiv:1311.5668](https://arxiv.org/abs/1311.5668))

though [Kihara 16](#Kihara16) writes ([p. 2](https://arxiv.org/pdf/1605.06794.pdf#page=2)) that 

> there exists a gap in the proof of [Haraguchi-Shimakawa 13](#HaraguchiShimakawa13), Theorem 5.6

This gap is addressed in

* {#Haraguchi18} [[Tadayuki Haraguchi]], _Homotopy structures of smooth CW complexes_ ([arXiv:1811.06175](https://arxiv.org/abs/1811.06175))

* {#HaraguchiShimakawa20} [[Tadayuki Haraguchi]], [[Kazuhisa Shimakawa]], _A model structure on the category of diffeological spaces, I_ ([arXiv:2011.12842](https://arxiv.org/abs/2011.12842))


A different model structure, however not using the standard smooth homotopy groups(!), is claimed (and published) in 

* {#Kihara16} [[Hiroshi Kihara]], _Model category of diffeological spaces_, Journal of Homotopy and Related Structures, (2018), 1-40 ([arXiv:1605.06794](https://arxiv.org/abs/1605.06794))



See also 

* {#ChristensenWu14} [[J. Daniel Christensen]],  [[Enxin Wu]], _The homotopy theory of diffeological spaces, I. Fibrant and cofibrant objects_, New York J. Math. 20 (2014), 1269-1303 ([arXiv:1311.6394](http://arxiv.org/abs/1311.6394))

* [[Tadayuki Haraguchi]], [[Kazuhisa Shimakawa]], _On homotopy types of diffeological cell complexes_ ([arXiv:1912.05359](https://arxiv.org/abs/1912.05359))

[[!redirects model category of diffeological spaces]]

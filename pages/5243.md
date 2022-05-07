

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Oka-Grauert principle_ states that for any [[Stein manifold]] $X$ the holomorphic and the topological classification of [[complex vector bundles]] on $X$ coincide. The original reference is ([Grauert 58](#Grauert58)).

The principle should maybe better be called the _Oka-Grauert-Gromov principle/theory_. Gromov viewed it in his book on partial differential relations as one of the examples of [[h-principle]]. 

## Statement in higher complex analytic geometry
 {#StatementInComplexAnalyticGeometry}

In ([Larusson 01](#Larusson01), [Larusson 03](#Larusson03)) this is formulated in terms of [[higher complex analytic geometry]] of [[complex analytic infinity-groupoids]].

Say that a [[complex manifold]] $X$ is an _[[Oka manifold]]_ if for every [[Stein manifold]] $\Sigma$ the canonical morphism

$$
  Maps_{hol}(\Sigma, X) \longrightarrow Maps_{top}(\Sigma, X)
$$

from the [[mapping space]] of [[holomorphic functions]] to that of [[continuous functions]] (both equipped with the [[compact-open topology]]) is a [[weak homotopy equivalence]].

+-- {: .num_theorem}
###### Theorem

This is the case precisely if $Maps_{hol}(-,X) \in Psh_\infty(SteinSp)$ satisfies [[descent]] with respect to [[finite set|finite]] [[covers]].

=--

 ([Larusson 01, theorem 2.1](#Larusson01))

+-- {: .num_theorem}
###### Theorem

The category of [[complex manifolds]] and [[holomorphic maps]] can be embedded into a Quillen [[model category]] such that:

* a holomorphic map is a weak equivalence in the ambient model category if and only if it is a [[homotopy equivalence]] in the usual topological sense.

* a holomorphic map is a fibration if and only if it is an Oka map. In particular, a complex manifold is fibrant if and only if it is an [[Oka manifold]].

* a [[complex manifold]] is cofibrant if and only if it is [[Stein manifold|Stein]].

* a Stein inclusion is a cofibration.

=--

([Larusson 03](#Larusson03))

## Related concepts

*  [[Oka manifold]]. 

* [[smooth Oka principle]]

## References

Original articles include

* K. Oka, _Sur les fonctions des plusieurs variables. III: Deuxi&#232;me probl&#232;me de Cousin_, J. Sc. Hiroshima Univ. __9__, 7&#8211;19 (1939)

* [[Hans Grauert]], _Analytische Faserungen &#252;ber holomorph-vollst&#228;ndigen R&#228;umen_, Math. Ann. __135__, 263&#8211;-273 (1958) [doi](http://dx.doi.org/10.1007/BF01351803)
 {#Grauert58}

* [[Mikhail Gromov]], _Oka's principle for holomorphic sections
of elliptic bundles_, J. Amer. Math. Soc. __2__ (1989), 851&#8211;-897.

* [[Franc Forstnerič]], _The Oka principle for sections of stratified fiber bundles_, Pure Appl. Math. Quarterly (Special Issue in honor of Joseph J. Kohn), 6 (2010), no. 3, 843--874, [arxiv/0705.0591](http://arxiv.org/abs/0705.0591)


Surveys and reviews include

* [[Finnur Lárusson]], _What is an Oka manifold_, Notices AMS, [pdf](http://www.ams.org/notices/201001/rtx100100050p.pdf)

* [[Franc Forstnerič]], [[Finnur Lárusson]], _Survey of Oka theory_, [arxiv/1009.1934](http://arxiv.org/abs/1009.1934)

* {#Forstneric11} [[Franc Forstnerič]], section 5.3 of _Stein manifolds and holomorphic mappings -- The homotopy principle in complex analysis_, Springer 2011




Discussion in terms of [[higher complex analytic geometry]] and [[complex analytic infinity-groupoids]] is in 

* {#Larusson01} [[Finnur Lárusson]], _Excision for simplicial sheaves on the Stein site and Gromov's Oka principle_ ([arXiv:math/0101103](http://arxiv.org/abs/math/0101103))


* {#Larusson03} [[Finnur Lárusson]], _Model structures and the Oka principle_, [math.CV/0303355](http://arxiv.org/abs/math/0303355)

This construction stems from some observations from Jardine, and uses his intermediate model structure from

*  [[John Frederick Jardine]], _Intermediate model structures for simplicial presheaves_, Canad. Math. Bull. __49__ (2006), no. 3, 407&#8211;413, [MR2007d:18021](http://www.ams.org/mathscinet-getitem?mr=2252262)

Some other articles on Oka principle:

* Tyson Ritter, _A strong Oka principle for embeddings of some planar domains into $C\times C^*$_, [arxiv/1011.4116](http://arxiv.org/abs/1011.4116)


Related MO discussion: [by Georges Elencwajg](http://mathoverflow.net/a/60053/381)

[[!redirects Oka theory]]
[[!redirects Oka's theory]]
[[!redirects Oka's principle]]

[[!redirects Oka-Grauert principle]]

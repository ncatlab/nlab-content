
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In analogy to [[rational homotopy theory]], the idea of *real homotopy theory* is to study those aspects of [[homotopy types]] that are visible when the [[ground ring]] is the [[real numbers]], such as their [[real cohomology]]-[[cohomology groups|groups]] and the [[tensor product of abelian groups|tensor product]] of their [[homotopy groups]] with the additive [[abelian group]] of [[real numbers]]. This is of central relevance in relation to [[differential cohomology theory]], which needs real instead of rational [[coefficients]] in order to connect to [[de Rham complexes]] of [[differential forms]] on [[smooth manifolds]].
 
But a technical issue with generalizing the [[fundamental theorem of dg-algebraic rational homotopy theory]] to the case of real homotopy theory is that the 
[[PL de Rham complex|PL de Rham]]-[[Quillen adjunction between simplicial sets and connective dgc-algebras]] -- which does exist over any [[ground field]] $k$ of [[characteristic zero]] and relates to the one over the [[rational numbers]] by [[derived functor|derived]] [[extension of scalars]] (all reviewed in [FSS 2020, Sec. 3.2](#FSS20)) -- models $k$-[[localization]] only for $k = \mathbb{Q}$ the [[rational numbers]] -- then: [[rationalization]]. 

From the point of [[algebra]], the issue is (see [this Remark](core+of+a+ring#NoOtherCharZeroFieldIsSolid)) that other $k$ are not [[solid rings]], so that the iterations of the [[tensor product of abelian groups|tensor products]] $(-) \otimes_{\mathbb{Z}} k$ on [[homotopy groups]] are not, in general, [[isomorphism|isomorphic]] to each other, for $k \neq \mathbb{Q}$.

On the other hand, from the point of [[topology]] the issue is that the [[real numbers]] $k = \mathbb{R}$ are naturally a [[topological ring]], whose topology, however, is ignored in the standard [[Quillen adjunction between simplicial sets and connective dgc-algebras]] over the real numbers.

Therefore, the *real homotopy theory* of [Brown & Szczarba 1995](#BrownSzczarba95) replaces, in the [[fundamental theorem of dg-algebraic rational homotopy theory]], the plain [[real cohomology]]-groups by real [[continuous cohomology]] and plain [[dgc-algebras]] with [[topological ring|topological algebras]].


> The authors of ([Brown-Szczarba 95](#BrownSzczarba95)) show how the Bousfield-Gugenheim approach to [[rational homotopy theory]] may be extended to the framework of [[continuous cohomology]]. In the usual theory, the extension from the [[rational numbers|rationals]] to the [[real numbers|reals]] has always been effected by a formal tensoring with the reals. While this allows a connection to [[de Rham complex|de Rham theory]], it has always been preferable to have a direct construction of real homotopy theory akin to the [[Postnikov tower]]-like construction of [[rational homotopy theory]]. Unfortunately, in the usual situation, such a construction is impossible due to the incompatibility of the algebra of $\mathbb{R}$ (as an [[abelian group]]) with its natural [[topology]]. The authors of ([Brown-Szczarba 95](#BrownSzczarba95)) remedy this problem by creating a theory of [[minimal models]] which incorporates the usual topology of the reals and a generalization of [[van Est's theorem]] saying that $H^*(K(\mathbb{R},n); \mathbb{R})$ is a freely generated algebra on one generator (a result which is not true in the discrete topology case). By using the natural topology of $\mathbb{R}$, there is an immediate connection to [[continuous cohomology]] and applications such as [[characteristic classes]] of [[foliations]]. 

> (from the [Zentralblatt review](http://mirrors.library.cornell.edu/ZMATH/zmath/en/zmath/search/?an=0865.55009) of ([Brown-Szczarba 95](#BrownSzczarba95)))


## Related concepts

* [[rational homotopy theory]]

* [[p-adic homotopy theory]]

## References
 {#References}

On [[real homotopy theory]] ([[rational homotopy theory]] over the [[real numbers]]) using [[continuous cohomology|continuous]] [[real cohomology]] and [[topological algebra|topological]] [[dgc-algebras]]:

* {#BrownSzczarba95} [[Edgar Brown]], [[Robert H. Szczarba]], _Real and Rational Homotopy Theory_, Chapter 17 in: *[[Handbook of Algebraic Topology]]*,  Elsevier, 1995 869-915 ([doi:10.1016/B978-044481779-2/50018-3](https://doi.org/10.1016/B978-044481779-2/50018-3), [ZB](http://mirrors.library.cornell.edu/ZMATH/zmath/en/zmath/search/?an=0865.55009))

with emphasis on globally [[Kan complex|Kan fibrant]] [[simplicial topological spaces]] (such as [[simplicial topological groups]]);

* {#BrownSzczarba89} [[Edgar H. Brown]], [[Robert H. Szczarba]], *Continuous cohomology and real homotopy type*, Trans. Amer. Math. Soc. 311 (1989), no. 1, 57 ([doi:10.1090/S0002-9947-1989-0929667-6](https://doi.org/10.1090/S0002-9947-1989-0929667-6),  [pdf](http://www.ams.org/journals/tran/1989-311-01/S0002-9947-1989-0929667-6/S0002-9947-1989-0929667-6.pdf))

with arbitrary [[fundamental group]]:

* {#BrownSzczarba90} [[Edgar Brown]], [[Robert H. Szczarba]], _Continuous cohomology and Real homotopy type II_ Asterisque 191, Societe Mathematique De France (1990) ([numdam:AST_1990__191__45_0](http://www.numdam.org/book-part/AST_1990__191__45_0))

* [[Edgar Brown]], [[Robert H. Szczarba]], *Real and rational homotopy theory for spaces with arbitrary fundamental group*, Duke Mathematical Journal 71. (1993): 229-316 ([doi:10.1215/S0012-7094-93-07111-6](https://projecteuclid.org/journals/duke-mathematical-journal/volume-71/issue-1/Rational-and-real-homotopy-theory-with-arbitrary-fundamental-groups/10.1215/S0012-7094-93-07111-6.short))

Discussion of the plain [[Quillen adjunction between simplicial sets and connective dgc-algebras]] over the real numbers, and its relation to [[rationalization]] followed by [[derived functor|derived]] [[extension of scalars]]:

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The character map in (twisted differential) non-abelian cohomology]]* ([arXiv:2009.11909](https://arxiv.org/abs/2009.11909))



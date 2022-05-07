
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{: toc}

## Idea

The idea of **formal category theory**  is to handle the fundamental notions and constructions of [[category theory]] -- such as [[adjoint functors]], [[monads]], [[limits]], etc. -- [[axiom|axiomatically]] via abstract properties enjoyed by the ([[very large category|very large]]) [[2-category]] [[Cat]] of all [[categories]], which is the archetypical [[2-topos]].


In the words of [Gray 1974, p. VII](#Gray74):


> The purpose of category theory is to try to describe certain general aspects of the structure of mathematics.  Since category theory is also part of mathematics, this categorical type of description should apply to it as well as to other parts of mathematics. $[\dots]$

> The basic  idea is that the category of small categories, $Cat$, is a 2-category with properties and that one  should attempt to identify those properties  that  enable one to do the "structural parts of category heory".

This is analogous to -- in fact is a [[categorification]] of -- how ([[structural set theory|structural]]) [[set theory]] may be understood as the study of the [[1-category]] [[Set]] of all [[sets]], whose good abstract properties are largely captured by understanding it as being the archetypical [[topos]] ("1-topos"). 

In the other direction of [[higher category theory]] there would be room for "formal" [[(infinity,1)-category theory|$(\infty,1)$-category theory]] via axiomatization of the ([[very large category|very large]]) [[(infinity,2)-category of (infinity,1)-categories|$(\infty,2)$-category of $(\infty,1)$-categories]] $Cat_{(\infty,1)}$ -- the archetypical [[(infinity,2)-topos|$(\infty,2)$-topos]]. 

While this has not been developed, it is interesting to observe ([Riehl & Verity 13](#RiehlVerity13), following [Joyal 08](#Joyal08) [p. 158](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=10)) that already its truncation down to a plain [[2-category]] $2Ho\big( Cat_{(\infty,1)}\big)$ -- the [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category of $(\infty,1)$-categories]] -- retains much of the interesting structure of [[(infinity,1)-category theory|$(\infty,1)$-category theory]]. For example, formal [[2-category theory|2-category theoretic]] [[adjunctions]] -- as envisioned by [Gray 1974](#Gray74) in $Cat$, but now interpreted in $2Ho\big( Cat_{(\infty,1)}\big)$ -- turn out to encode the correct notion of [[adjoint (infinity,1)-functors|adjoint $(\infty,1)$-functors]] (see [there](adjoint+infinity1-functor#InTheHomotopy2Category) for more).

By analogy, this may be referred to as a *formal theory of $(\infty,1)$-categories* ([Riehl 2021](#Riehl21)).

At least for [[presentable (infinity,1)-categories|presentable $(\infty,1)$-categories]] this formal $\infty$-category theory is directly accessible from "abstract [[homotopy theory]]" in the sense of [[combinatorial model category|combinatorial]] [[model category]]-theory, in that $2Ho\big( PresCat_{(\infty,1)}\big) \,\simeq\,$ [[2Ho(CombModCat)]] ([Pavlov 2021](HoCombModCat#Pavlov21)).




## Details

Contexts for developing formal category theory: 

* [[Yoneda structures]]

* [[proarrow equipments]]

  [[virtual double category]]

  [[virtual equipment]]

* [[KZ doctrines]]


## Related pages

* [[ETCC]]

* [[2-topos]], [[(infinity,2)-topos|$(\infty,2)$-topos]]

## References

### For 1-categories

An axiomatization of (just) the ([[very large category|very large]]) [[1-category]] of all categories, but fully in [[formal logic]] is the *[[elementary theory of the category of categories]]* (ETCC) due to:

* {#Law66} [[William Lawvere]], *The Category of Categories as a Foundation for Mathematics*, pp.1-20 in Eilenberg, Harrison, MacLane, R&#246;hrl (eds.), _Proceedings of the Conference on Categorical Algebra - La Jolla 1965_, Springer Heidelberg 1966 ([doi:10.1007/978-3-642-99902-4_1](https://doi.org/10.1007/978-3-642-99902-4_1))

The undertaking of laying these foundations instead for the [[2-category]] of all categories is famously associated with:

* {#Gray74} [[John Gray]], *[[Adjointness for 2-Categories|Formal category theory: adjointness for $2$-categories]]*, Lecture Notes in Mathematics, **391**, Springer 1974 ([doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280))

Review and further discussion:

* [[Ivan Di Liberti]], [[Simon Henry]], Mike Lieberman, [[Fosco Loregian]], _Formal category theory_, ([course notes](https://tetrapharmakon.github.io/stuff/course_muni-formal.pdf))

* [[Ivan Di Liberti]], [[Fosco Loregian]], _On the unicity of formal category theories_ ([arXiv:1901.01594](https://arxiv.org/abs/1901.01594))

Discussion in [[double category]]-theory:

* {#Koudenburg15} [[Seerp Roald Koudenburg]], *A double-dimensional approach to formal category theory* ([arXiv:1511.04070](http://arxiv.org/abs/1511.04070)) 2015.  

* {#Koudenburg19} [[Seerp Roald Koudenburg]], *Augmented virtual double categories*, Theory and Applications of Categories, Vol. 35, 2020, No. 10, pp 261-325 ([arXiv:1910.11189](https://arxiv.org/abs/1910.11189), [tac:35-10](http://www.tac.mta.ca/tac/volumes/35/10/35-10abs.html))

  > (On [[augmented virtual double categories]], a expanded version of Sec. 1-3 of [Koudenburg 15](#Koudenburg15) )


### For $(\infty,1)$-categories

With ([[small (infinity,1)-category|small]]) [[(∞,1)-categories]] modeled as [[quasi-categories]], their [[homotopy 2-category of (infinity,1)-categories|their homotopy 2-category]] was considered first in

* {#Joyal08} [[André Joyal]], [p. 158](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=10) in: _The theory of quasicategories and its applications_, lectures at _[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)_, CRM 2008 ([pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]])

and then developed further (in the generality of [[homotopy 2-categories]] of [[∞-cosmoi]]) in:

* {#RiehlVerity13} [[Emily Riehl]], [[Dominic Verity]], _The 2-category theory of quasi-categories_, Advances in Mathematics Volume 280, 6 August 2015, Pages 549-642 ([arXiv:1306.5144](http://arxiv.org/abs/1306.5144), [doi:10.1016/j.aim.2015.04.021](https://doi.org/10.1016/j.aim.2015.04.021))


* {#RiehlVerity16} [[Emily Riehl]], [[Dominic Verity]],  _Infinity category theory from scratch_, Higher Structures Vol 4, No 1 (2020) ([arXiv:1608.05314](https://arxiv.org/abs/1608.05314), [pdf](http://www.math.jhu.edu/~eriehl/scratch.pdf))

* {#RiehlVerity21} [[Emily Riehl]], [[Dominic Verity]], *Elements of $\infty$-Category Theory*, 2021- ([pdf](https://math.jhu.edu/~eriehl/elements.pdf))

* {#Riehl21} [[Emily Riehl]], *The formal theory of ∞-categories*, talk at *[Categories and Companions Symposium June 8–12, 2021](http://web.science.mq.edu.au/groups/coact/seminar/CaCS2021/)* ([video](https://youtu.be/iX5Fxen3K-U))

[[!redirects formal (infinity,1)-category theory]]


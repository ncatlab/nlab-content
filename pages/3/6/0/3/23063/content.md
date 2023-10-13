
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

The idea of **formal category theory**  is to handle the fundamental notions and constructions of [[category theory]] -- such as [[adjoint functors]], [[monads]], [[limits]], etc. -- [[axiom|axiomatically]].


In the words of [Gray 1974, p. VII](#Gray74):


> The purpose of category theory is to try to describe certain general aspects of the structure of mathematics.  Since category theory is also part of mathematics, this categorical type of description should apply to it as well as to other parts of mathematics. $[\dots]$

> The basic  idea is that the category of small categories, $Cat$, is a 2-category with properties and that one  should attempt to identify those properties  that  enable one to do the "structural parts of category theory".

Early approaches to formal category theory took place in the setting of plain [[2-categories]] with [[property-like structure]] (e.g. [[2-limits]], [[exponentials]], etc.), as alluded to in Gray's quote above. (But to capture also [[enriched category theory]] it is necessary to consider extra [[structure]], see the *[Approaches](#Approaches)* below.)


This is analogous to -- in fact is a [[categorification]] of -- how ([[structural set theory|structural]]) [[set theory]] may be understood as the study of the [[1-category]] [[Set]] of all [[sets]], whose good abstract properties are largely captured by understanding it as being the archetypical [[topos]] ("1-topos").



In the other direction of [[higher category theory]] there would be room for "formal" [[(infinity,1)-category theory|$(\infty,1)$-category theory]] via axiomatization of the ([[very large category|very large]]) [[(infinity,2)-category of (infinity,1)-categories|$(\infty,2)$-category of $(\infty,1)$-categories]] $Cat_{(\infty,1)}$ -- the archetypical [[(infinity,2)-topos|$(\infty,2)$-topos]]. 

While this has not been developed, it is interesting to observe ([Riehl & Verity 13](#RiehlVerity13), following [Joyal 08](#Joyal08) [p. 158](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=10)) that already its truncation down to a plain [[2-category]] $2Ho\big( Cat_{(\infty,1)}\big)$ -- the [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category of $(\infty,1)$-categories]] -- retains much of the interesting structure of [[(infinity,1)-category theory|$(\infty,1)$-category theory]]. For example, formal [[2-category theory|2-category theoretic]] [[adjunctions]] -- as envisioned by [Gray 1974](#Gray74) in $Cat$, but now interpreted in $2Ho\big( Cat_{(\infty,1)}\big)$ -- turn out to encode the correct notion of [[adjoint (infinity,1)-functors|adjoint $(\infty,1)$-functors]] (see [there](adjoint+infinity1-functor#InTheHomotopy2Category) for more).

By analogy, this may be referred to as a *formal theory of $(\infty,1)$-categories* ([Riehl 2021](#Riehl21)).

At least for [[presentable (infinity,1)-categories|presentable $(\infty,1)$-categories]] this formal $\infty$-category theory is directly accessible from "abstract [[homotopy theory]]" in the sense of [[combinatorial model category|combinatorial]] [[model category]]-theory, in that $2Ho\big( PresCat_{(\infty,1)}\big) \,\simeq\,$ [[2Ho(CombModCat)]] ([Pavlov 2021](HoCombModCat#Pavlov21)).

## Approaches
 {#Approaches}

Roughly speaking, there are three main approaches to formal category theory:

1. [[Yoneda structures]] 

   (cf. [Street & Walters 1978](Yoneda+structure#SW78))

1. [[proarrow equipments]]/[[framed bicategories]]/(augmented) [[virtual equipments]] 

   (cf. [Wood 1982](2-category+equipped+with+proarrows#Wood82), [1985](2-category+equipped+with+proarrows#Wood85); [Shulman 2008](framed+bicategory#Shulman08); [Cruttwell & Shulman 2010](generalized+multicategory#CruttwellShulman10); [Koudenburg 2022](#Koudenburg22))

1. [[lax-idempotent 2-monads]] 

   (cf. [Bunge & Funk 1999](lax-idempotent+2-monad#BF99))

Most recent authors take the second approach (although the precise formalism varies). The relationship between the approaches, for the most part, is not laid out clearly in the literature, but a basic intuition is that:

1. Yoneda structures are based on formalising the [[category of presheaves|presheaf construction]].

1. Proarrow equipments and related structures are based on formalising [[distributors]]/[[profunctors]].

1. Lax-idempotent pseudomonads are based on formalising the [[free cocompletion]]-construction.

In nice settings, e.g. in [[enriched category theory]] for a well-behaved [[base of enrichment]] (eg. a [[Bénabou cosmos]]) all three approaches are viable. However, with weaker assumptions, not all of them are. 

For instance, one may not in general have a [[presheaf category]]-construction or [[free cocompletion]], and so Yoneda structures and lax-idempotent pseudomonads are not applicable in general. Without enough [[coequalisers]] in the base, [[distributors]] do not compose, and so proarrow equipments and fibrant double categories are not applicable.

The most general settings are those of [[virtual equipments]] and augmented virtual equipments. Here it is possible to formalise presheaves (as in the work of Koudenburg), thus recovering Yoneda structures; as well as free cocompletions (though not yet in the literature), and so these approaches subsume the others.


## Related pages

* [[ETCC]]

* [[2-topos]], [[(infinity,2)-topos|$(\infty,2)$-topos]]

* [[synthetic (infinity,1)-category theory]]

## References

### For 1-categories

An axiomatization of (just) the ([[very large category|very large]]) [[1-category]] of all categories, but fully in [[formal logic]] is the *[[elementary theory of the category of categories]]* (ETCC) due to:

* {#Law66} [[William Lawvere]], *The Category of Categories as a Foundation for Mathematics*, pp. 1-20 in: [[Samuel Eilenberg|S. Eilenberg]], [[D. K. Harrison]], [[S. MacLane]], [[H. Röhrl]] (eds.): *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;



The undertaking of laying these foundations instead for the [[2-category]] of all categories is famously associated with:

* {#Gray74} [[John Gray]], *[[Adjointness for 2-Categories|Formal category theory: adjointness for $2$-categories]]*, Lecture Notes in Mathematics, **391**, Springer 1974 ([doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280))

Review and further discussion, including on the relationship between the different approaches:

* [[Ivan Di Liberti]], [[Simon Henry]], Mike Lieberman, [[Fosco Loregian]], _Formal category theory_, ([course notes](https://tetrapharmakon.github.io/stuff/course_muni-formal.pdf))

* [[Ivan Di Liberti]], [[Fosco Loregian]], _On the unicity of formal category theories_ ([arXiv:1901.01594](https://arxiv.org/abs/1901.01594))

The relation between [[lax-idempotent pseudomonads]] and [[Yoneda structures]] is due to:

* Charles Walker, *Yoneda Structures and KZ Doctrines*, [arxiv](https://arxiv.org/abs/1703.08693)
 {#WalkerYS}

Discussion in [[double category]]-theory:

* [[Michael Shulman]], _Framed bicategories and monoidal fibrations_.

* {#CruttwellShulman10} [[Geoff Cruttwell]] and [[Mike Shulman]], _A unified framework for generalized multicategories_, Theory Appl. Categ. **24** 21 (2010) 580-655 &lbrack;[arxiv/0907.2460](http://arxiv.org/abs/0907.2460), [TAC:24-21](http://www.tac.mta.ca/tac/volumes/24/21/24-21abs.html)&rbrack;

* {#Koudenburg15} [[Seerp Roald Koudenburg]], *A double-dimensional approach to formal category theory* ([arXiv:1511.04070](http://arxiv.org/abs/1511.04070)) 2015.  

* {#Koudenburg19} [[Seerp Roald Koudenburg]], *Augmented virtual double categories*, Theory and Applications of Categories, Vol. 35, 2020, No. 10, pp 261-325 ([arXiv:1910.11189](https://arxiv.org/abs/1910.11189), [tac:35-10](http://www.tac.mta.ca/tac/volumes/35/10/35-10abs.html))  

* {#Koudenburg22} [[Seerp Roald Koudenburg]], *Formal category theory in augmented virtual double categories* &lbrack;[arXiv:2205.04890](https://arxiv.org/abs/2205.04890)&rbrack;


  > (On [[augmented virtual double categories]], a expanded version of Sec. 1-3 of [the previous reference](#Koudenburg15).)

A domain-specific [[type theory]] for formal category theory: 

* [[Max S. New]], [[Daniel Licata]], _A Formal Logic for Formal Category Theory_ ([arXiv:2210.08663](https://arxiv.org/abs/2210.08663))



### For $(\infty,1)$-categories

With ([[small (infinity,1)-category|small]]) [[(∞,1)-categories]] modeled as [[quasi-categories]], their [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category]] was considered first in

* {#Joyal08} [[André Joyal]], [p. 158](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=10) in: _The theory of quasicategories and its applications_, lectures at _[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)_, CRM 2008 ([pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]])

and then developed further (in the generality of [[homotopy 2-categories]] of [[∞-cosmoi]]) in:

* {#RiehlVerity13} [[Emily Riehl]], [[Dominic Verity]], _The 2-category theory of quasi-categories_, Advances in Mathematics Volume 280, 6 August 2015, Pages 549-642 ([arXiv:1306.5144](http://arxiv.org/abs/1306.5144), [doi:10.1016/j.aim.2015.04.021](https://doi.org/10.1016/j.aim.2015.04.021))


* {#RiehlVerity16} [[Emily Riehl]], [[Dominic Verity]],  _Infinity category theory from scratch_, Higher Structures Vol 4, No 1 (2020) ([arXiv:1608.05314](https://arxiv.org/abs/1608.05314), [pdf](http://www.math.jhu.edu/~eriehl/scratch.pdf))

* {#RiehlVerity21} [[Emily Riehl]], [[Dominic Verity]], _[[Elements of ∞-Category Theory]]_, Cambridge studies in advanced mathematics **194**, Cambridge University Press (2022) $[$[doi:10.1017/9781108936880](https://doi.org/10.1017/9781108936880), ISBN:978-1-108-83798-9, [pdf](https://emilyriehl.github.io/files/elements.pdf)$]$

* {#Riehl21} [[Emily Riehl]], *The formal theory of ∞-categories*, talk at *[Categories and Companions Symposium June 8–12, 2021](http://web.science.mq.edu.au/groups/coact/seminar/CaCS2021/)* ([video](https://youtu.be/iX5Fxen3K-U))

In an [[(∞,1)-category theory|(∞,1)-category theoretic]] version of [[proarrow equipments]]:

* Jaco Ruit, _Formal category theory in ∞-equipments I_ ([arXiv:2308.03583](https://arxiv.org/abs/2308.03583))

[[!redirects formal (infinity,1)-category theory]]


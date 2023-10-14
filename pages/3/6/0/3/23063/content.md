## Idea

There are many flavours of category:

- ordinary [[categories]]
- [[enriched categories]]
- [[internal categories]]
- [[fibred categories]]
- [[indexed categories]]
- [[monoidal categories]]

and so on. In each flavour of category theory, one finds essentially the same definitions and theorems:

- [[presheaves]] and the [[Yoneda lemma]]
- [[adjunctions]] and [[adjoint functor theorems]]
- [[monads]] and [[monadicity theorems]]
- theories of [[accessible category|accessible]] and [[locally presentable categories]] and [[Gabriel--Ulmer duality|duality theorems]]

and so on. Rather than define these concepts and prove these theorems in each of the different flavours of category theory independently (as has been done traditionally), one would rather be able to define these concepts and prove these theorems abstractly, and then specialise to each of these flavours, obtaining for instance the statements for enriched category theory as a corollary of the more abstract version. This is the motivation for formal category theory.

**Formal category theory** may be thought of as applying the philosophy of category theory to category theory itself. Typically, this takes the form of applying 2-dimensional category theories (e.g. [[2-category|2-category theory]] or [[double category|double category theory]]) to study 1-dimensional category theory. This may be viewed as a [[synthetic mathematics|synthetic]] approach to category theory.

This may be seen as a [[categorification]] of the approach of [[structural set theory]], which is a [[synthetic mathematics|synthetic]] approach to [[set theory]]. (In fact, just as a [[topos]] is intended as an axiomatisation of the logical nature of the archetypical topos [[Set]], [Street & Walters](Yoneda+structure#SW78) introduced [[Yoneda structures]], one of the earliest approaches to formal category theory, as an axiomatisation of the "logical" nature of the archetypical [[2-topos]] [[Cat]].)

## Approaches

An important question is: what is the appropriate setting in which to study the formal theory of categories? There is not one obvious answer, and several approaches have been proposed in the literature.

Roughly speaking, there are four main approaches (listed in chronological order of the first time they were proposed).

1. [[2-categories]] with [[property-like structure]]

   (cf. [Gray 1974](#Gray74))

1. [[Yoneda structures]] 

   (cf. [Street & Walters 1978](Yoneda+structure#SW78))

1. [[proarrow equipments]]/[[framed bicategories]]/(augmented) [[virtual equipments]] 

   (cf. [Wood 1982](2-category+equipped+with+proarrows#Wood82), [1985](2-category+equipped+with+proarrows#Wood85); [Shulman 2008](framed+bicategory#Shulman08); [Cruttwell & Shulman 2010](generalized+multicategory#CruttwellShulman10); [Koudenburg 2022](#Koudenburg22))

1. [[lax-idempotent 2-monads]] 

   (cf. [Bunge & Funk 1999](lax-idempotent+2-monad#BF99), Trimble's [epistemologies](https://ncatlab.org/toddtrimble/published/Epistemologies))

The relationship between the approaches, for the most part, is not laid out clearly in the literature, but a basic intuition is that:

1. [[2-categories]] may be equipped with various [[property-like structure]] possessed by the 2-category [[Cat]], e.g. [[2-limits]] and [[2-colimits]], [[exponentials]], etc.

1. Yoneda structures are based on formalising the [[category of presheaves|presheaf construction]].

1. Proarrow equipments and related structures are based on formalising [[distributors]]/[[profunctors]].

1. Lax-idempotent pseudomonads (also called **KZ-doctrines**) are based on formalising the [[free cocompletion]]-construction.

The first, purely 2-categorical, approach is unsufficient to capture [[enriched categories]] (though captures many aspects of ordinary and internal category theory), and is therefore not viable as a general approach to formal category theory.

On the other hand, in nice settings, e.g. in [[enriched category theory]] for a well-behaved [[base of enrichment]] (eg. a [[Bénabou cosmos]]), approaches (2 -- 4) are all viable, and are distinguished primarily by their methodology. However, in weaker settings, some approaches are no longer viable.

For instance, one may not in general have a [[presheaf category]]-construction or [[free cocompletion]], and so Yoneda structures and [[lax-idempotent pseudomonads]] are not applicable in general. Without enough [[coequalisers]] in the base, [[distributors]] do not compose, and so proarrow equipments and fibrant double categories are not applicable. For instance, for a general [[monoidal category]] $V$, only the formalisms of [[virtual equipments]] and [[augmented virtual equipments]] capture the structure of $V$-[[enriched categories]]. These are thus the most general approaches to formal category theory. Here it is possible to formalise [[presheaves]] as in [Koudenburg 2022](#Koudenburg22), thus recovering [[Yoneda structure]]; as well as free cocompletions (though this had not been developed in the literature): these approaches consequently strictly subsume the others.

## Theorems in formal category theory

Below, we list some fundamental theorems in category theory that have been formulated in formal category theory.

* General results about [[weighted limits]] and [[weighted colimits]] are developed in [Street & Walters 1978](Yoneda+structure#SW78) (for [[Yoneda structures]]); [Wood 1982](2-category+equipped+with+proarrows#Wood82) (for [[proarrow equipments]]); [Arkor & McDermott 2023a](#AM23b) (for [[virtual equipments]]).
* Adjoint functor theorems are proven in Proposition 21 of [Street & Walters 1978](Yoneda+structure#SW78); Corollary 10 of [Wood 1982](2-category+equipped+with+proarrows#Wood82); Theorem 2.16 of [Arkor, Di Liberti, Loregian](#ALL23).
* An analogue of the [[bijective-on-objects functor|bijective-on-objects]]/[[fully faithful functor|fully faithful]] factorisation system is established in [Wood 1985](2-category+equipped+with+proarrows#Wood85).
* General results about [[monads]] are developed in [Street & Walters 1978](Yoneda+structure#SW78) (for [[Yoneda structures]]); [Wood 1985](2-category+equipped+with+proarrows#Wood85) (for [[proarrow equipments]]); [Arkor & McDermott 2023a](#AM23b) in the additional generality of [[relative monads]] (for [[virtual equipments]]).
* The theory of [[total categories]] is developed in [Street & Walters 1978](Yoneda+structure#SW78) (for [[Yoneda structures]]); [Koudenburg 2022](#Koudenburg22) (for [[augmented virtual equipments]]).
* A general duality theorem subsuming [[Gabriel–Ulmer duality]] (and many others) is proven in [Di Liberti & Loregian 2023](#DL18) (for [[lax-idempotent pseudomonads]]).
* General results about [[presheaves]] are developed in [Koudenburg 2022](#Koudenburg22) (for [[augmented virtual equipments]]).
* A ([[relative monad|relative]]) [[monadicity theorem]] is proven in [Arkor & McDermott 2023a](#AM23b) (for [[virtual equipments]]).

## Related pages

* [[enriched category theory]]

* [[ETCC]]

* [[2-topos]]

* [[formal (infinity,1)-category theory]]

## References

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

On the intuition for [[Yoneda structures]] as [[2-toposes]]:

* [[Ross Street]], *An Australian conspectus of higher category theory*, talk at Institute for Mathematics and its Applications Summer Program: *$n$-Categories: Foundations and Applications* at the University of Minnesota (Minneapolis, 7–18 June 2004), in: *[[Towards Higher Categories]]*, The IMA Volumes in Mathematics and its Applications **152**, Springer (2010) 237-264 &lbrack;[pdf](http://www.math.uchicago.edu/~may/IMA/Street.pdf), [[Street-Conspectus.pdf:file]], [doi:10.1007/978-1-4419-1524-5](https://link.springer.com/book/10.1007/978-1-4419-1524-5)&rbrack;

Papers developing general theorems in formal category theory:

* {#DL23} [[Ivan Di Liberti]], [[Fosco Loregian]], _Accessibility and Presentability in 2-Categories_, Journal of Pure and Applied Algebra 227.1 (2023)([arXiv:1804.08710](https://arxiv.org/abs/1804.08710))
* {#ALL23} [[Nathanael Arkor]], [[Ivan Di Liberti]], and [[Fosco Loregian]]. _Adjoint functor theorems for lax-idempotent pseudomonads_, ([arXiv:2306.10389](https://arxiv.org/abs/2306.10389))
* {#AM23a} [[Nathanael Arkor]], [[Dylan McDermott]], _The formal theory of relative monads_, 2023. &lbrack;[arXiv:2302.14014](https://arxiv.org/abs/2302.14014)&rbrack;
* {#AM23b} [[Nathanael Arkor]], [[Dylan McDermott]], _Relative monadicity_, 2023. &lbrack;[arXiv:2305.10405](https://arxiv.org/abs/2305.10405)&rbrack;
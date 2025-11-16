

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Where 

* [[categorical logic]] is [[formal logic]]/[[type theory]] regarded as the [[internal logic]]/[[internal language]] of [[categories]], notably of categories well-suited for this purposes, such as [[elementary toposes]],

so 

* 2-categorical logic, or *2-logic* for short, as understood in this entry here, is (or should be, once developed) the [[categorification]] of this situation, namely the study of the [[internal logic]]/[[internal language|language]] of [[two-dimensional categories]] (understood in the generality including [[2-categories]], [[bicategories]], [[double categories]], [[virtual double categories]], etc.), and notably of two-dimensional categories well-suited for this purpose, such as those one will want to call *elementary [[2-toposes]]*.

Therefore, the step from [[formal logic]]/[[categorical logic]] to formal 2-logic/2-categorical logic is analogous to the step from the former to [[homotopy type theory]], where one instead considers the [[internal language]] of [[(infinity,1)-categories|$(\infty,1)$-categories]]. 

This means that 2-logic is a genuine extension of ordinary logic with new logical constructions and phenomena (largely still to be isolated properly) --- analogous to how [[homotopy type theory]] enhances ordinary logical [[types]] to [[homotopy types]], so 2-logic will be speaking about "1-types" of sorts (meaning: [[(n,r)-category|$(1,1)$]]-types also known as *[[small categories]]*, as opposed to the more restrictive [[homotopy 1-types|homotopy $(1,0)$-types]] also known as *[[groupoids]]*, both generalizing the [[homotopy 0-types|0-types]] also known as *[[sets]]*).

For example:

* where [[subobject classifiers]] in ordinary [[elementary toposes]] serve as [[universes of propositions]] for their [[first order logic|first order]] [[internal logic]], 

* where [[object classifiers]] in [[(infinity,1)-toposes|$(\infty,1)$-toposes]] serve as [[type universes]] for their   [[homotopy type theory|homotopy]] [[internal logic]],  

* so [[2-toposes]] have *fibration classifiers* which should serve as universes of "2-types" for their internal 2-logic.

  Accordingly, [[powersets]] in ordinary logic/[[set theory]] become [[categories of presheaves]] in 2-logic, and the Cantor embedding becomes the [[Yoneda embedding]], etc.


In fact, there should be a joint generalization and unification of 2-logic of "2-types" with the "$(\infty,1)$-logic" of [[homotopy types]], namely given by the internal language of [[(infinity,2)-categories|$(\infty,2)$-categories]] (notably of [[(infinity,2)-toposes|$(\infty,2)$-toposes]]): This $(\infty,2)$-logic is currently being developed under the name *[[directed homotopy type theory]]* and as such, even if itself nascent, may be the most developed form of [[syntax|syntactic]] 2-logic that has found attention so far.

This means that 2-logic in the sense of this page here is *not* about the related but different idea of using general tools from [[2-category theory]] in the study of ordinary [[1-category|1-]][[categorical logic]], hence is *not* along the lines of how [[formal category theory]] uses [[2-category theory]] to study [[1-categories]]. 

Of course, there may be relation and overlap between 2-logic proper and such "formal categorical logic" using 2-categorical methods in 1-logic. With genuine 2-logic not being developed much at all at this point, most of the references listed below actually fall on the side of 2-categorical methods in 1-logic.

For instance, for a suitable 2-dimensional [[sketch]]-like object its 2-category of [[models]] in [[Cat]] is a category of [[algebraic theories|1-theories]]: [[coherent categories]], [[regular categories]], [[lex categories]]. Thus, on one side we have the study of 2-sketch like objects, of [[2-monads]] on [[Cat]] and [[Lex]], and on [[2-functor|2-]][[functorial semantics]]. This is the adagio that *2-theories are logics*. On the other we have the study of 2-categories of (1)-theories, i.e. the idea that *2-models are 1-theories*.




## Related concepts

* [[type theory]], [[logic]]

* [[2-type theory]]

* [[(∞,1)-type theory]], [[(∞,1)-logic]]


## References
 {#References}

An early explicit logic for a class of structured 2-categories (namely lax [[cartesian closed]] [[2-categores]]) may be found in:

* [[R. A. G. Seely]]. _Modelling Computations : a 2-categorical Framework_. LICS 1987. ([pdf](http://www.math.mcgill.ca/rags/WkAdj/LICS.pdf))

Remarks on [[geometric logic|geometric]] 2-logic:

* {#BourkeGarner} [[John Bourke]], [[Richard Garner]], Remks. 42 & 47 in: *Two-dimensional regularity and exactness*, Journal of Pure and Applied Algebra, **218** 7 (2014) 1346–1371 &lbrack;[doi:10.1016/j.jpaa.2013.11.021](https://doi.org/10.1016/j.jpaa.2013.11.021), [arXiv:1304.5275](https://arxiv.org/abs/1304.5275)&rbrack;


{#ReferencesOnElementary2Topoi} On further aspects of [[elementary topos|elementary]] [[2-topoi]]:

* {#Weber07} [[Mark Weber]]: *Yoneda structures from 2-toposes*, Appl Categor Struct **15** (2007) 259–323 &lbrack;[doi:10.1007/s10485-007-9079-2](https://doi.org/10.1007/s10485-007-9079-2), [pdf](https://sites.google.com/site/markwebersmaths/home/yoneda-structures-from-2-toposes)&rbrack;
  > (introduces a notion of *elementary 2-topos* but explicitly disregards discussion of logical aspects)

* [[Steve Awodey]], [[Jacopo Emmenegger]], _Toward the effective 2-topos_ (2025) &lbrack;[arXiv:2503.24279](http://arxiv.org/abs/2503.24279)&rbrack;
  > (a 2-dimensional version of the [[effective topos]])


{#ReferencesOnHigherClassifiers} Specifically on higher classifiers (higher analogs of what is the [[subobject classifier]] in ordinary [[elementary topos|elementary]] [[toposes]]):

* [[Luca Mesiti]]: _Pointwise Kan extensions along 2-fibrations and the 2-category of elements_, Theory and Applications of Categories **41** 30 960–994 (2024) &lbrack;[arXiv:2302.04566](http://arxiv.org/abs/2302.04566), [doi:10.70930/tac/b9u5z003](http://doi.org/10.70930/tac/b9u5z003)&rbrack;
  > (via a [[2-Grothendieck construction]])

* [[Elena Caviglia]], [[Luca Mesiti]], _Indexed Grothendieck construction_, Theory and Applications of Categories **41** 28 (2024) 894–926 &lbrack;[arXiv:2307.16076](http://arxiv.org/abs/2307.16076), [doi:10.70930/tac/xzio144a](https://doi.org/10.70930/tac/xzio144a)&rbrack;
  > (via the [[indexed Grothendieck construction]])

* [[Luca Mesiti]], _2-classifiers via dense generators and Hofmann-Streicher universe in stacks_, Canadian Journal of Mathematics (2025) 1–52 &lbrack;[arXiv:2401.16900](http://arxiv.org/abs/2401.16900), [doi:10.4153/S0008414X24000865](https://doi.org/10.4153/S0008414X24000865)&rbrack;

* [[Calum Hughes]], Adrian Miranda: _The elementary theory of the 2-category of small categories_, Theory and Applications of Categories *43* 8 (2025) 196–242 &lbrack;[arXiv:2403.03647](https://arxiv.org/abs/2403.03647), [doi:10.70930/tac/c97jx7g2](https://doi.org/10.70930/tac/c97jx7g2)&rbrack;
  > (via [ET2CC](ETCC#ET2CC))

On 2-[[functorial semantics]]:

* [[John Power]]: _Why tricategories?_, Information and Computation **120** 2 (1995) 251–262 &lbrack;[doi:10.1006/inco.1995.1112](https://doi.org/10.1006/inco.1995.1112)&rbrack;
  > (in a context of [[tricategories]])

* [[John Power]]: _Enriched Lawvere theories_, Theory and Applications of Categories **6** 7 (1999) 83–93 &lbrack;[tac:6-07](http://www.tac.mta.ca/tac/volumes/6/n7/6-07abs.html), [doi:10.70930/tac/soye1d6v](https://doi.org/10.70930/tac/soye1d6v)&rbrack;

* [[John Power]]: _Categories with algebraic structure_, International Workshop on Computer Science Logic, Springer (1997) 389–405 &lbrack;[doi:10.1007/BFb0028027](http://doi.org/10.1007/BFb0028027)&rbrack;

* [[Renato Betti]], [[Marco Grandis]], _Complete theories in 2-categories_, [[Cahiers]] **29** 1 (1988) 9–57 &lbrack;[numdam:CTGDC_1988__29_1_9_0](https://www.numdam.org/item/CTGDC_1988__29_1_9_0)&rbrack;

* [[Nathanael Arkor]], [[John Bourke]], Joanna Ko, _Enhanced 2-categorical structures, two-dimensional limit sketches and the symmetry of internalisation_ &lbrack;[arXiv:2412.07475](https://arxiv.org/abs/2412.07475)&rbrack;

* [[Ivan Di Liberti]], [[Axel Osmond]]: _Bi-accessible and bipresentable 2-categories_, Applied Categorical Structures **33** 3 (2025) &lbrack;[arXiv:2203.07046](https://arxiv.org/abs/2203.07046), [doi:10.1007/s10485-024-09794-9](http://doi.org/10.1007/s10485-024-09794-9)&rbrack;
  > (not on 2-logic but on [[locally presentable categories|locally presentable]] [[2-categories]])

On [[2-categories]] as [[2-theories]]:

* {#Garner09} [[Richard Garner]]: *Two-dimensional models of type theory*, Mathematical Structures in Computer Science **19** 4 (2009) 687-736 &lbrack;[doi:10.1017/S0960129509007646](https://doi.org/10.1017/S0960129509007646), [pdf](https://www.irif.fr/~mellies/mpri/mpri-ens/articles/garner-two-dimensional-models-of-type-theory.pdf)&rbrack;

* {#CDL21} Greta Coraglia, [[Ivan Di Liberti]]: _Context, judgement, deduction_ (2021) &lbrack;[arXiv:2111.09438](https://arxiv.org/abs/2111.09438)&rbrack;

* [[Benedikt Ahrens]], [[Paige Randall North]], [[Niels van der Weide]]: *Semantics for two-dimensional type theory*, LICS '22: Proceedings of the 37th Annual ACM/IEEE Symposium on Logic in Computer Science, 12 (2022) 1–14, &lbrack;[doi:10.1145/3531130.3533334](https://doi.org/10.1145/3531130.3533334)&rbrack;

* Vít Jelínek: _Type theory and its semantics_, Master thesis, Masaryk University (2024) &lbrack;[is.muni.cz:th/fl75q/](https://theses.cz/id/n7t9ei)&rbrack;

* Jonathan Osser:  _A 2‑Sketchy Approach to Type Theory_, Master thesis, University of Amsterdam (2025) &lbrack;[scripties:56899](https://scripties.uba.uva.nl/search?id=record_56899)&rbrack;



On [[rewriting]]:

* [[John Power]]: _An abstract formulation for rewrite systems_, In Category Theory and Computer Science, Springer Berlin Heidelberg (1989) 300–312 &lbrack;[doi:10.1007/BFb0018358](http://doi.org/10.1007/BFb0018358)&rbrack;

* [[Tom Hirschowitz]]: _Cartesian closed 2-categories and permutation equivalence in higher-order rewriting_, Logical Methods in Computer Science **9** 3 (2013) pp.10 &lbrack;[pdf](https://hal.archives-ouvertes.fr/hal-00540205v2/document), [arXiv:1307.6318](http://arxiv.org/abs/1307.6318), [doi:10.2168/LMCS-9(3:10)2013](https://doi.org/10.2168/LMCS-9%283%3A10%292013)&rbrack;

* [[Samuel Mimram]], _Categorical Coherence from Term Rewriting Systems_, 8th International Conference on Formal Structures for Computation and Deduction (FSCD 2023), Leibniz International Proceedings in Informatics (LIPIcs) **260** (2023) 16:1–16:17 &lbrack;[doi:10.4230/LIPIcs.FSCD.2023.16](http://doi.org/10.4230/LIPIcs.FSCD.2023.16)&rbrack;

* [[Samuel Mimram]]: _Rewriting techniques for relative coherence_, Logical Methods in Computer Science **21** 3 (2025) &lbrack;[arXiv:2402.18170](http://arxiv.org/abs/2402.18170), [doi:10.46298/lmcs-21(3:7)2025](http://doi.org/10.46298/lmcs-21(3:7)2025)&rbrack;


On [[2-categories]] of [[theory|1-theories]]:

* [[Richard Garner]], [[Stephen Lack]]: _Lex colimits_, Journal of Pure and Applied Algebra **216** 6 (2012) 1372–1396 &lbrack;[arXiv:1107.0778](https://arxiv.org/abs/1107.0778), [doi:10.1016/j.jpaa.2012.01.003](http://doi.org/10.1016/j.jpaa.2012.01.003)&rbrack;

* [[Ivan Di Liberti]], [[Gabriele Lobbia]]: _Sketches and Classifying Logoi_ (2024) &lbrack;[arXiv:2403.09264](http://arxiv.org/abs/2403.09264)&rbrack;

* Greta Coraglia, [[Jacopo Emmenegger]], _A 2-categorical analysis of context comprehension_, Theory and Applications of Categories **41** 42 (2024) 1476–1512 &lbrack;[arXiv:2403.03085](http://arxiv.org/abs/2403.03085), [doi:10.70930/tac/dcvkbg9f](http://doi.org/10.70930/tac/dcvkbg9f)&rbrack;

* [[Benedikt Ahrens]], [[Peter LeFanu Lumsdaine]], [[Paige Randall North]]: _Comparing semantic frameworks for dependently-sorted algebraic theories_, Asian Symposium on Programming Languages and Systems (APLAS 2024), Lect. Notes Comp. Sci. **15194** (2024) 3–22 &lbrack;[arXiv:2412.19946](http://arxiv.org/abs/2412.19946), [doi:10.1007/978-981-97-8943-6_1](http://doi.org/10.1007/978-981-97-8943-6_1)&rbrack;

* Greta Coraglia, [[Jacopo Emmenegger]]: _Categorical models of subtyping_, 29th International Conference on Types for Proofs and Programs (TYPES 2023), Leibniz International Proceedings in Informatics (LIPIcs) **303** (2024) 3:1–3:19 &lbrack;[arXiv:2312.14600](http://arxiv.org/abs/2312.14600), [doi:10.4230/LIPIcs.TYPES.2023.3](http://doi.org/10.4230/LIPIcs.TYPES.2023.3)&rbrack;

* [[Ivan Di Liberti]], [[Lingyuan Ye]]: _Logics and concepts in the 2-category of Topoi_ (2025) &lbrack;[arXiv:2504.16690](http://arxiv.org/abs/2504.16690)&rbrack;



On [[(∞,2)-topoi]]:

* Fernando Abellán, [[Louis Martini]]: _$(\infty,2)$-Topoi and descent_ &lbrack;[arXiv:2410.02014](https://arxiv.org/abs/2410.02014)&rbrack;

On [[directed type theory]] and [[ends]] and [[coends]] as *directed* [[quantifiers]]:

* Andrea Laretto, [[Fosco Loregian]], Niccolò Veltri, _Directed equality with dinaturality_ &lbrack;[arXiv:2409.10237](https://arxiv.org/abs/2409.10237)&rbrack;

A treatment of [[doctrines]] in terms of [[double categories]]:

* Michael Lambert, [[Evan Patterson]], *Cartesian double theories: A double-categorical framework for categorical doctrines* &lbrack;[arXiv:2310.05384](https://arxiv.org/abs/2310.05384)&rbrack;

Notes on assorted topics related to 2-categorical logic:

* {#Shulman2009} [[Mike Shulman]]: *[[michaelshulman:2-categorical logic]]* (Unfinished notes, 2009)
  > (also includes exposition of other aspects of 2-logic, such as exactness and Grothendieck 2-topoi).

[[!redirects 2-logic]]

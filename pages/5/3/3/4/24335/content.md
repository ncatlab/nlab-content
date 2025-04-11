
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

**Formal $(\infty,1)$-category theory** is to [[(infinity,1)-category theory|$(\infty,1)$-category theory]] what [[formal category theory]] is to [[category theory|1-category theory]], that is: a [[synthetic mathematics|synthetic]] approach to $(\infty,1)$-categories standing in relation to [[synthetic homotopy theory]] as $(\infty, 1)$-category theory stands to [[homotopy theory]]. Consequently, formal $(\infty,1)$-category theory has also been called **synthetic $(\infty,1)$-category theory**.

## Approaches

There have been two main styles of approaches to formal $(\infty,1)$-category theory: *categorical*, which are $(\infty,2)$-categorical in nature; and *type theoretic*, which propose [[deductive systems]] for reasoning about $(\infty,1)$-categories.

### Category theoretic approaches

* Following [Joyal 2008](#Joyal08) [p. 158](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=10), [Riehl & Verity 2013](#RiehlVerity13) observe that the [[homotopy 2-category|homotopy 2-category of $(\infty,1)$-categories]] $2Ho\big( Cat_{(\infty,1)}\big)$ retains much of the interesting structure of the $(\infty,2)$-category $Cat_{(\infty,1)}$. Thus, one may use the techniques of [[formal category theory]] to study certain aspects of the formal theory of $(\infty,1)$-categories. For instance, this includes the theory of [[adjoint (infinity,1)-functors|adjoint $(\infty,1)$-functors]] (which are automatically homotopy coherent), but not the theory of [[(infinity,1)-monads|$(\infty,1)$-monads]] (which are not). This is developed in [[Elements of ∞-Category Theory]] in the setting of a [[virtual equipment]].

* For [[presentable (infinity,1)-categories|presentable $(\infty,1)$-categories]], formal $(\infty,1)$-category theory is directly accessible from "abstract [[homotopy theory]]" in the sense of [[combinatorial model category|combinatorial]] [[model category]]-theory, in that $2Ho\big( PresCat_{(\infty,1)}\big) \,\simeq\,$ [[2Ho(CombModCat)]] ([Pavlov 2021](HoCombModCat#Pavlov21)).
- [Ruit 2023](#Ruit23) has introduced an $\infty$-double categorical generalisation of [[fibrant double categories]].

* There is also the approach by [Cisinski et al](#CCNW). 

### Type theoretic approaches

The type theoretic approaches attempt to formalise the [[internal logic]] of a [[cohesive (infinity,1)-topos|cohesive $(\infty,1)$-topos]] or [[local (infinity,1)-topos|local $(\infty,1)$-topos]] $\mathbf{H}$ over $\infty\mathrm{Grpd}$, such that $(\infty,1)\mathrm{Cat} \hookrightarrow \mathbf{H}$ is a $(\infty,1)$-subcategory of $\mathbf{H}$. Examples include

* [Riehl & Shulman 2017](#RiehlShulman17) propose a type theory called *[[simplicial type theory]]*, which have [[categorical semantics]] in [[simplicial infinity-groupoids]] or [[bisimplicial sets]]. This is further developed by [Buchholtz & Weinberger 2021](#BuchholtzWeinberger21). 

* [Gratzer, Weinberger & Buchholtz 2024](#GWB24) propose a modification of simplicial type theory called *[[triangulated type theory]]*, which have [[categorical semantics]] in [[cubical infinity-groupoids]] or [[cubical-simplicial sets]]. 

* [Weaver & Licata 2020](#WeaverLicata20) propose a type theory, which has semantics in [[bicubical sets]].

* [Kolomatskaia & Shulman 2023](#KS23) propose a type theory called *[[displayed type theory]]*, which has [[categorical semantics]] in [[augmented simplicial set|augmented]] [[semi-simplicial object|semi-simplicial]] $\infty$-groupoids. Unlike the previous three type theories, the semantics is not cohesive over $\infty\mathrm{Grpd}$ ([Aberlé 2024](#Aberle24)). 

## Related pages

* [[formal category theory]]

* [[(infinity,2)-topos|$(\infty,2)$-topos]]

* [[internal category in homotopy type theory]]

* [[synthetic mathematics]], [[synthetic homotopy theory]]

* [[(infinity,1)-category theory|$(\infty,1)$-category theory]]

* [[directed homotopy type theory]]

* [[simplicial type theory]], [[cubical type theory]]

## References

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

### Category theoretic approaches

With ([[small (infinity,1)-category|small]]) [[(∞,1)-categories]] modeled as [[quasi-categories]], their [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category]] was considered first in

* {#Joyal08} [[André Joyal]], [p. 158](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=10) in: _The theory of quasicategories and its applications_, lectures at _[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)_, CRM 2008 ([pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]])

and then developed further (in the generality of [[homotopy 2-categories]] of [[∞-cosmoi]]) in:

* {#RiehlVerity13} [[Emily Riehl]], [[Dominic Verity]], _The 2-category theory of quasi-categories_, Advances in Mathematics Volume 280, 6 August 2015, Pages 549-642 ([arXiv:1306.5144](http://arxiv.org/abs/1306.5144), [doi:10.1016/j.aim.2015.04.021](https://doi.org/10.1016/j.aim.2015.04.021))

* {#RiehlVerity16} [[Emily Riehl]], [[Dominic Verity]],  _Infinity category theory from scratch_, Higher Structures Vol 4, No 1 (2020) ([arXiv:1608.05314](https://arxiv.org/abs/1608.05314), [pdf](http://www.math.jhu.edu/~eriehl/scratch.pdf))

* {#RiehlVerity21} [[Emily Riehl]], [[Dominic Verity]], _[[Elements of ∞-Category Theory]]_, Cambridge studies in advanced mathematics **194**, Cambridge University Press (2022) $[$[doi:10.1017/9781108936880](https://doi.org/10.1017/9781108936880), ISBN:978-1-108-83798-9, [pdf](https://emilyriehl.github.io/files/elements.pdf)$]$

* {#Riehl21} [[Emily Riehl]], *The formal theory of ∞-categories*, talk at *[Categories and Companions Symposium June 8–12, 2021](http://web.science.mq.edu.au/groups/coact/seminar/CaCS2021/)* ([video](https://youtu.be/iX5Fxen3K-U))

In an [[(∞,1)-category theory|(∞,1)-category theoretic]] version of [[proarrow equipments]]:

* {#Ruit23} Jaco Ruit, _Formal category theory in ∞-equipments I_ ([arXiv:2308.03583](https://arxiv.org/abs/2308.03583))

### Type theoretic approaches

For synthetic (infinity, 1)-category theory in [[cubical type theory]] via [[bicubical sets]]:

* {#WeaverLicata20} [[Matthew Weaver]], [[Daniel Licata]], *A Constructive Model of Directed Univalence in Bicubical Sets*, in: *Proceedings of the 35th Annual ACM/IEEE Symposium on Logic in Computer Science. LICS ’20*, Association for Computing Machinery (2020) 915–928 &lbrack;[doi:10.1145/3373718.3394794](https://doi.org/10.1145/3373718.3394794)&rbrack;

Exposition in 

* [[Matthew Weaver]], *A Constructive Model of Directed Univalence in Bicubical Sets*, talk at HoTTEST (April 2020) &lbrack;[pdf](https://www.cs.princeton.edu/~mzweaver/pdfs/HoTTEST.pdf), [video](https://youtu.be/kkfNjqSx4Nw)&rbrack;

For synthetic (infinity, 1)-category theory in [[simplicial type theory]]:

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* {#BuchholtzWeinberger21} [[Ulrik Buchholtz]], [[Jonathan Weinberger]], *Synthetic fibered $(\infty,1)$-category theory* $[$[arXiv:2105.01724](https://arxiv.org/abs/2105.01724), [talk slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Weinberger-2022-01-20-HoTTEST.pdf)$]$

* [[Jonathan Weinberger]], *A Synthetic Perspective on $(\infty,1)$-Category Theory: Fibrational and Semantic Aspects* $[$[arXiv:2202.13132](https://arxiv.org/abs/2202.13132)$]$

* Fredrik Bakke, *Segal Spaces in Homotopy Type Theory*. Master thesis $[$[no.ntnu:inspera:99217069:14871483	](https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/2995704)$]$

* [[César Bardomiano Martínez]], *Limits and colimits of synthetic $\infty$-categories* $[$[arXiv:2202.12386](https://arxiv.org/abs/2202.12386)$]$

* [[Jonathan Weinberger]], *Strict stability of extension types* $[$[arXiv:2203.07194](https://arxiv.org/abs/2203.07194)$]$

* [[Jonathan Weinberger]], *Two-sided cartesian fibrations of synthetic $(\infty,1)$-categories* $[$[arXiv:2204.00938](https://arxiv.org/abs/2204.00938)$]$

* [[Jonathan Weinberger]], *Internal sums for synthetic fibered $(\infty,1)$-categories* $[$[arXiv:2205.00386](https://arxiv.org/abs/2205.00386)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#GWB25} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *The Yoneda embedding in simplicial type theory* ([arXiv:2501.13229](https://arxiv.org/abs/2501.13229))

A talk on [[synthetic (infinity,1)-category theory]] in [[simplicial type theory]] and [[infinity-cosmos | infinity-cosmos theory]]:

* [[Emily Riehl]], *The synthetic theory of infinity-categories vs the synthetic theory of infinity-categories*, [[Homotopy Type Theory Electronic Seminar Talks]], 1 March 2018, ([video](https://www.youtube.com/watch?v=ge-9m1SsEmc), [slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Riehl-2018-03-01-HoTTEST.pdf))

The authors of the following paper suggest that it should be possible to formalise $(\infty,1)$-categories in [[displayed type theory]]:

* {#KS23} [[Astra Kolomatskaia]], [[Michael Shulman]], *Displayed Type Theory and Semi-Simplicial Types* &lbrack;[arXiv:2311.18781](https://arxiv.org/abs/2311.18781)&rbrack; 

* {#Aberle24} [[C.B. Aberlé]], *Parametricity via Cohesion* &lbrack;[arXiv:2404.03825](https://arxiv.org/abs/2404.03825)&rbrack; 

[[!redirects formal (∞,1)-category theory]]
[[!redirects formal infinity1-category theory]]

[[!redirects synthetic (infinity,1)-category theory]]
[[!redirects synthetic (∞,1)-category theory]]
[[!redirects synthetic infinity1-category theory]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

[[!redirects category of categories]]

## Idea

> The explicit formulation of the principles of category theory ... is still in need of improved axiomatization. I will be overjoyed when some young person responds to that need. Lawvere ([2016](#Law16), p.1)

**Elementary theory of the category of categories**, or _ETCC_ for short, is in a broad sense an appropriate name for any [[first order logic|first order]] [[theory]] axiomatizing the metacategory [[Cat|CAT]] of categories that forms the intuitive background for naive [[category theory]] with a view to the categorical [[foundations of mathematics]].

Historically, the first attempt to formulate such a system of axioms has been undertaken by [[William Lawvere|F. W. Lawvere]] in his dissertation in 1963 and a subsequent publication (Lawvere 1966), and it is this system that is sometimes referred to as _the_ ETCC. We will discuss it together with subsequent attempts to repair its technical flaws under this heading in the next section.

Taking into account that the intuitively given category of categories is a 2-category, from an _n-categorical perspective_ one would prefer to axiomatize CAT directly as a 2-category, and the resulting _elementary theory of the 2-category of categories_, or **ET2CC**, is the subject of a subsequent [section](#ET2CC).

## ETCC: Lawvere (1963) and beyond {#ETCC}

>In 1964, F. W. Lawvere proposed to found mathematics on the category of categories. When he lectured on this at an international conference in Jerusalem, [[Alfred Tarski]] objected: "But what is a category if not a set of objects together with a set of morphisms?" Lawvere replied by pointing out that set theory axiomatized the binary relation of membership, while category theory axiomatized the ternary relation of composition. [^LS] 

[^LS]: [Lambek&Scott 2009](#LS11), pp.171-172.

W. Lawvere launched in the early 60s an ambitious long-term project to replace membership based mathematics by more invariant concepts in order to arrive at a renewal of analysis and geometry adapted for the needs of modern (continuum) physics. 

His 1963 [[Functorial Semantics of Algebraic Theories|dissertation]] takes issue with set-theoretic notions at various levels, e.g. redefining [[adjoint functors]] via [[comma categories]] in order to avoid reference to Hom-sets, but the most radical step is the attempt at a first-order axiomatization of the category of categories that he proposes to bypass [[set theory]] completely at a foundational level.

The system of axioms that he published in a more elaborate form in 1966, is layered in three parts:

* The _elementary theory of [[category|abstract categories]]_ (ETAC) has besides equality three primitive predicates for domain, codomain, and composition and as axioms the usual axioms for identity, associativity etc. (See at [[theory of categories]] for a variant of such an axiomatisation!)

* The _basic theory_ (BT) adds axioms for e.g. **1**, a one-morphism category, **2**, a category with one non-identity morphism between two objects, **3**, a category with a commutative triangle of morphisms, and various exactness properties among which is the existence of exponentials. This permits then to define e.g. sets as discrete objects $A$ with $A^1\cong A^2$ i.e. as categories whose morphisms are all identity morphisms. The final axiom of the basic theory tries to express the _[[dense subcategory|density]]-adequacy_ of the simple categories like **1** etc. within the metacategory.

* The _stronger theory_ (ST) then adds two further axioms to the basic theory concerning existence of completions and an 'inaccessible' category (p.18).

As pointed out by [[John Isbell|J. Isbell]] in 1967, one of Lawvere's results (namely, the theorem on the 'construction of categories  by description' on p.14) was mistaken, which left the axiomatics dangling with insufficient power to construct models for categories. Several ways to overcome these problems where suggested in the following but no system achieved univocal approval (cf. Blanc-Preller(1975), Blanc-Donnadieu(1976), Donnadieu(1975),  McLarty(1991)).

As ETCC also lacked the simplicity of [[ETCS]], it rarely played a role in the practice of category theory in the following and was soon eclipsed by [[topos theory]] in the attention of the research community that generally preferred to hedge their foundations with appeals to G&#246;del-Bernays set-theory or Grothendieck universes.

Nevertheless, the axiomatic treatment of 1963/66 contained also the seminal idea to internally define discrete set-theoretic 'foundations' within a bigger category, that will later on play a central role in Lawvere's approach to [[cohesion]]. So when one can view the 1964 ETCS as a forerunner of the Lawvere-Tierney axioms for an elementary topos, one could view ETCC as an anticipation of the 2007 axioms for a [[cohesive topos]].


## ET2CC: an elementary theory of the 2-category of categories{#ET2CC}

For Lawvere ETCS and ETCC have a different status, the first provides abstract constant sets as convenient carriers for structured objects, whereas the latter provides the overall ontology of concepts, the intellectual working space.

Yet from an **n-categorical perspective**, the categories they axiomatize differ in level only and so it is tempting to think of the second as a sort of [[categorification]] of the first: this suggests to posit an abstract concept 'foundation' that at the level of ETCS shows up as set theory, gets refined to 'category theory' one step higher, then as 2-category theory, and so on.

Now what comes closest to such a vision at the moment is probably [[homotopy type theory]] but truncating such a tower of 'foundations' might be still relevant for applications where concepts of [[2-topos|2-toposes]] are considered. It would also provide an axiomatisation for the 'familiar' meta 2-category CAT suggestive for the generalization to n-CAT.

At the time no such axiomatisation is fully worked out, but in 2009 [[Mike Shulman|M. Shulman]] gave a rough sketch of how such an **elementary theory of the 2-category of categories** (ET2CC) should look like:

> Firstly, some exactness axioms amounting to its being a "2-pretopos" in the sense I described here:[[michaelshulman:2-categorical logic]] . This gives you an "internal logic" like that of an ordinary (pre)topos.
  
> Secondly, the existence of certain exponentials (this is optional).

> Thirdly, the existence of a "classifying discrete opfibration" el&#8594;set in the sense introduced by [[Mark Weber]] ("Yoneda structures from 2-toposes") which serves as "the category of sets," and internally satisfies some suitable axioms.

> Finally, a "well-pointedness" axiom saying that the terminal object is a generator, as is the case one level down with in ETCS. This is what says you have a 2-category of categories, rather than (for instance) a 2-category of stacks.

> Once you have all this, you can use finite 2-categorical limits and the "internal logic" to construct all the usual concrete categories out of the object "set".      ([Shulman 2009](#MO-CC))

We can see here how at the end Lawvere's idea of internal set-theoretic 'foundations' resurfaces. Such a level of _discreteness_ seems to be pervasive in this context and e.g. the approach of Przybylek (2014) to the concept of internal 2-cartesian closure takes discreteness as a starting point.

### Remark

Note that already B. Walters and R. Street conceived of their work on [[Yoneda structure|Yoneda structures]] in the early 1970s as a 2-dimensional version of ETCC (cf. Walters [1971](#W71)).

## Related entries

* [[ETCS]]
* [[Yoneda structure]]
* [[Functorial Semantics of Algebraic Theories]]
* [[foundations of mathematics]]
* [[theory of categories]]

## References

* F. W. Lawvere, *[[Functorial Semantics of Algebraic Theories]]*, Ph.D. thesis, Columbia University New York 1963. (With an author's comment and a supplement in: Reprints in Theory and Applications of Categories, no.5 (2004) pp.1-121 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/5/tr5.pdf)))

A revised version of the axioms appears as

* {#Law66} [[William Lawvere]], *The Category of Categories as a Foundation for Mathematics*, pp.1-20 in Eilenberg, Harrison, MacLane, R&#246;hrl (eds.), _Proceedings of the Conference on Categorical Algebra - La Jolla 1965_, Springer Heidelberg 1966 ([doi:10.1007/978-3-642-99902-4_1](https://doi.org/10.1007/978-3-642-99902-4_1))

Important reviews of the paper pointing out technical problems appeared here

* [[John Isbell|J. R. Isbell]], *Review of Lawvere 1966*, Mathematical Reviews **34** (1967) #7332.

* G. Blanc. A. Preller, *Lawvere's basic theory of the category of categories*, JSL **40** (1975) pp.14-18.

A more recent view of Lawvere exposing in particular his 'M&#252;nchhausen' approach to set-theoretic 'foundations' is in

* [[William Lawvere|F. W. Lawvere]], _Foundations and Applications: Axiomatization and Education_, Bulletin of Symbolic Logic **9** no.2 (2003) pp.213-224. ([ps-preprint](https://www.math.ucla.edu/~asl/bsl/0902/0902-006.ps))

Lawvere briefly comments on his 1965 system 50 years later p.6 in

* {#Law16}F. W. Lawvere, *Alexander Grothendieck and the Concept of Space*, address CT15 Aveiro 2016. ([link](http://www.acsu.buffalo.edu/~wlawvere/GrothendiekAveiro15.htm))

An insightful and non-partisan view of ETCC can be found in a section of:

* [[Andreas Blass]], Yuri Gurevich, *Why Sets?*, Bull. Europ. Assoc. Theoret. Comp. Sci. **84** (2004) pp.139-156.  ([draft](http://www.math.lsa.umich.edu/~ablass/set.pdf))

Alternative or complementary approaches are

* [[J. Bénabou]], *Fibered Categories and the foundations of naive category theory*, JSL **50** (1985) pp.10-37. ([preprint](http://www.cwru.edu/artsci/phil/Benabou%20Fibered.pdf))

* G. Blanc, *Propri&#233;t&#233;s du Premier Ordre et Cat&#233;gories*, Cah. Top. G&#233;om. Diff. Cat. **16** (1975) pp.222-224. ([Colloque Amiens 1975 proceedings](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1975__16_3/CTGDC_1975__16_3_217_0/CTGDC_1975__16_3_217_0.pdf),6.81 MB)

* G. Blanc, M. R. Donnadieu, *Axiomatisation de la cat&#233;gorie des cat&#233;gories*, Cah.Top.G&#233;om.Diff.Cat. **XVII** no. 2 (1976) pp.1-35. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1976__17_2/CTGDC_1976__17_2_135_0/CTGDC_1976__17_2_135_0.pdf))

* M. W. Bunder, *Category Theory Based on Combinatory Logic*, Arch. Math. Logik **24** (1984) pp.1-15. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002045680))

* N. C. A. da Costa, O. Bueno, A. Volkov, *Outline of a Paraconsistent Category Theory*, pp.95-114 in Weingartner (ed.), *Alternative Logics. Do Science Need Them?*, Springer Heidelberg 2004. ([draft](http://homepage.mac.com/otaviobueno/.Public/ParacCategTheory.pdf))

* M. R. Donnadieu, *D&#233;monstration du th&#233;or&#232;me de construction de cat&#233;gories d'apr&#232;s description de Lawvere sous certains axiomes*, C. R. Acad. Sc. Paris **280** s&#233;rie A (1975) pp.307-308. ([gallica](http://gallica.bnf.fr/ark:/12148/bpt6k6228238v/f59.image))

* E. Engeler, H. R&#246;hrl, *On the problem of foundations of category theory*, Dialectica **23** (1969) pp.58-66.

* [[Colin McLarty|C. McLarty]], *Axiomatizing a category of categories*, JSL **56** (1991) pp.1243-1260. ([preprint](http://www.cwru.edu/artsci/phil/AxiomatizingCategoryCategories.pdf))

* L. Oubi&#241;a, *Teor&#237;a axiomatica de categor&#237;as*, Cah. Top. G&#233;om. Diff. Cat., **X** no. 3 (1968) pp.375-394. ([numdam](http://www.numdam.org/numdam-bin/item?id=CTGDC_1968__10_3_375_0))

* J. Sonner, *On the formal definition of categories*, Math. Zeitschr. **80**  (1962) pp.163-176. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002392232))

* H. Tsukuda, *Category theory not based upon set theory*, Sci. Papers
College Gen. Ed. Univ. Tokyo **31** (1981) pp.1-24.

A critical view of purely categorical foundations can be found in a series of [papers](http://math.stanford.edu/~feferman/papers.html) by S. Feferman e.g. :

* [[Solomon Feferman|S. Feferman]], *Categorical Foundations and Foundations of Category Theory*, pp.149-169 in Butts&Hintikka (eds.), _Logic, Foundations of Mathematics, and Computability Theory_, Reidel Dordrecht 1977. ([pdf](http://math.stanford.edu/~feferman/papers/Cat_founds.pdf))

An inconsistency in a recent formalisation by Feferman is discussed in

* M. Ernst, *The Prospects of Unlimited Category Theory: Doing What Remains to be Done*, Review Symbolic Logic **8** no.2 (2015) pp.306-327.

The above remarks from [[Mike Shulman|M. Shulman]] come from the following MO discussion that also offers additional perspectives on ETCC and ET2CC:

* {#MO-CC}mathoverflow, *Category of categories as a foundation for mathematics*, December 2009 . ([link](http://mathoverflow.net/questions/9269/category-of-categories-as-a-foundation-of-mathematics))

See also

* {#Blass84}[[Andreas Blass]], _The interaction of category theory and set theory_ , Cont. Math. **30** (1984) pp.5-29. ([draft](http://www.math.lsa.umich.edu/~ablass/interact.pdf))

* [[Jim Lambek]], [[Phil Scott]], *Reflections on Categorical Foundations of Mathematics*, pp.171-185 in  Sommaruga (ed.), _Foundational Theories of Classical and Constructive Mathematics_,  Springer New York 2011. ([draft](https://www.site.uottawa.ca/~phil/papers/LS11.final.pdf)) {#LS11}

* [[Colin McLarty|C. McLarty]], [[Andrei Rodin|A. Rodin]], _A Discussion between Colin McLarty and Andrei Rodin about Structuralism and Categorical Foundations of Mathematics_, n.d. ([pdf](http://canoe.ens.fr/~rodin/spip/IMG/pdf/colin.pdf))

* M. R. Pryzbylek, _Logical systems I: Lambda calculi through discreteness_, arxiv:1306.3703v3 (2014). ([pdf](http://arxiv.org/pdf/1306.3703v3))

* {#W71}[[Bob Walters]], _Yoneda 2Categories_ , talk at the University of New South Wales December 1971. ([manuscript](https://dl.dropboxusercontent.com/u/92056191/Archive/temporary_new_material/yoneda.pdf))


[[!redirects elementary theory of the 2-category of categories]]
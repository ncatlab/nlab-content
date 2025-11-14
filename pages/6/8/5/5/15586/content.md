
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

> The explicit formulation of the principles of category theory ... is still in need of improved axiomatization. I will be overjoyed when some young person responds to that need.  ([[William Lawvere|Lawvere]], [2016](#Law16), p.1)

{#IsInABroadSense} The **elementary theory of the category of categories**, or _ETCC_ for short, is a name for any [[first order logic|first order]] [[theory]] axiomatizing the metacategory [[Cat|CAT]] of [[categories]] that forms the intuitive background for naive [[category theory]] with a view to the categorical [[foundations of mathematics]]. This is in [[categorification]] of the analogous first-order axiomatization of the metacategory [[Set|SET]] of [[sets]], for which see *[[ETCS]]*.

Historically, the first attempt to formulate such a system of axioms was undertaken by [[William Lawvere|F. W. Lawvere]] in his dissertation ([Lawvere 63](#Lawvere63)) and a subsequent publication ([Lawvere 1966](#Lawvere66)), and it is this system that is sometimes referred to as _the_ ETCC. We will discuss it together with subsequent attempts to repair its technical flaws under this heading in the next section.

Taking into account that the intuitively given category of categories is a [[2-category]], from an _[[nPOV|n-categorical perspective]]_ one would prefer to axiomatize CAT directly as a 2-category, and the resulting _elementary theory of the 2-category of categories_, or **ET2CC**, is the subject of a subsequent [section](#ET2CC).

## ETCC: Lawvere (1963) and beyond {#ETCC}

>In 1964, F. W. Lawvere proposed to [[foundations of mathematics|found]] mathematics on the [[category of categories]]. When he lectured on this at an international conference in Jerusalem, [[Alfred Tarski]] objected: "But what is a category if not a [[set]] of [[objects]] together with a [[set]] of [[morphisms]]?" Lawvere replied by pointing out that set theory axiomatized the binary relation of membership, while category theory axiomatized the ternary relation of [[composition]]. [^LS] 

[^LS]: [Lambek&Scott 2009](#LS11), pp.171-172.

In the early 60s, Lawvere launched an ambitious long-term project to replace membership-based mathematics by more invariant concepts in order to arrive at a renewal of analysis and geometry adapted for the needs of modern (continuum) physics. 

His 1963 [[Functorial Semantics of Algebraic Theories|dissertation]] takes issue with set-theoretic notions at various levels, e.g. redefining [[adjoint functors]] via [[comma categories]] in order to avoid reference to Hom-sets, but the most radical step is the attempt at a first-order axiomatization of the category of categories that he proposed to bypass [[set theory]] completely at a foundational level.

The system of axioms that he published in a more elaborate form in 1966 is layered in three parts:

* The _elementary theory of [[category|abstract categories]]_ (ETAC) has, besides equality, three primitive predicates for domain, codomain, and composition and, as axioms, the usual axioms for identity, associativity, and so on. (See [[theory of categories]] for a variant of such an axiomatisation!)

* The _basic theory_ (BT) adds axioms for, e.g. **1**, a one-morphism category, **2**, a category with one non-identity morphism between two objects, **3**, a category with a commutative triangle of morphisms, and various exactness properties, among which is the existence of exponentials. This permits the definition of, e.g., sets as discrete objects $A$ with $A^1\cong A^2$, i.e., as categories whose morphisms are all identity morphisms. The final axiom of the basic theory tries to express the _[[dense subcategory|density]]-adequacy_ of the simple categories like **1** etc. within the metacategory.

* The _stronger theory_ (ST) then adds two further axioms to the basic theory concerning existence of completions and an 'inaccessible' category (p.18).

As pointed out by [[John Isbell|J. Isbell]] in 1967, one of Lawvere's results (namely, the theorem on the 'construction of categories  by description' on p.14) was mistaken, which left the axiomatics with insufficient power to construct models for categories. Several ways to overcome these problems were suggested in the following, but no system achieved unanimous approval: cf. Blanc-Preller(1975), Blanc-Donnadieu(1976), Donnadieu(1975),  and McLarty(1991).

As the ETCC also lacked the simplicity of [[ETCS]], it rarely played a role in the practice of category theory and was soon eclipsed by [[topos theory]] in the attention of the research community that generally preferred to hedge their foundations with appeals to G&#246;del-Bernays set-theory or Grothendieck universes.

Nevertheless, the axiomatic treatment of 1963/66 also contained the seminal idea to define discrete set-theoretic 'foundations' internally within a bigger category, and that would later on play a central role in Lawvere's approach to [[cohesion]]. So, as one can view the 1964 ETCS as a forerunner of the Lawvere-Tierney axioms for an elementary topos, one could also view the ETCC as an anticipation of the 2007 axioms for a [[cohesive topos]].


## ET2CC: an elementary theory of the 2-category of categories{#ET2CC}

For Lawvere, ETCS and ETCC had a different status. The former provides abstract constant sets as convenient carriers for structured objects, whereas the latter provides the overall ontology of concepts, the intellectual working space.

However, from an **n-categorical perspective**, the categories they axiomatize differ in level only, so it is tempting to think of the latter as a sort of [[categorification]] of the former.  This suggests to posit an abstract concept of 'foundation' that, at the level of ETCS, shows up as set theory, gets refined to 'category theory' one step higher, then as 2-category theory, and so on.  In addition, from this perspective it is more natural to axiomatize not the *category* of categories, but the *2-category* of categories.

[Hughes and Miranda](#HM25) have axiomatized an *elementary theory of the 2-category of small categories* (ET2CSC), and proven that a 2-category $K$ satisfies these axioms if and only if it is of the form $Cat(E)$, the 2-category of [[internal categories]] in some category $E$ that satisfies [[ETCS]].  The axioms are:

1. Exactness and projectivity conditions due to [Bourke](#Bourke) that ensure $K$ is of the form $Cat(E)$ for a category $E$ with pullbacks:

   1. $K$ has [[pullbacks]] and [[powers]] by the [[interval category]].
   2. $K$ has quotients of [[2-congruences]].
   3. Codescent morphisms are effective.
   4. [[discrete objects]] are [[projective object|projective]].
   5. Every object admits a codescent morphism from a projective object.

2. $K$ has a [[terminal object]].

3. $K$ is [[cartesian closed]], as a 2-category.

4. $K$ is [[well-pointed]], in an appropriate 2-categorical sense.

5. $K$ has a [[natural numbers object]], in an appropriate 2-categorical sense.

6. $K$ has a [[subobject classifier|classifier]] for [[fully faithful morphism|fully faithful]] [[monomorphisms]]

7. $K$ satisfies a suitable 2-categorical form of the [[axiom of choice]].

These axioms are called an elementary theory of the 2-category of *small* categories because they do not include an *object* of $K$ playing the role of [[Set]].  A formal theory incorporating such an object has not been completely written down; one expects it to be the base of a [[michaelshulman:classifying discrete opfibration]], as introduced by [Weber](#Weber07), probably satisfying categorified forms of the axioms of [[algebraic set theory]].

Given this, one may hope to use finite 2-categorical limits and the "internal logic" to construct all the usual concrete categories out of this object $Set$.  We can see here how, at the end, Lawvere's idea of internal set-theoretic 'foundations' resurfaces.

Such a level of _discreteness_ seems to be pervasive in this context. For instance, the approach of [Przybylek](#Przybylek14) to the concept of internal 2-cartesian closure takes discreteness as a starting point.

## Remarks

R. F. C. Walters and R. Street had already conceived of their work on [[Yoneda structure|Yoneda structures]] in the early 1970s as a 2-dimensional version of ETCC (cf. Walters [1971](#W71)).

## Related entries

* [[ETCS]]

* [[ETCR]]

* [[Yoneda structure]]

* [[Functorial Semantics of Algebraic Theories]]

* [[foundations of mathematics]]

* [[theory of categories]]

* [[formal category theory]]

## References

* {#Lawvere63} [[William Lawvere]], *[[Functorial Semantics of Algebraic Theories]]*, Ph.D. thesis, Columbia University New York 1963. (With an author's comment and a supplement in: Reprints in Theory and Applications of Categories, no.5 (2004) pp.1-121 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/5/tr5.pdf)))

A revised version of the axioms appears as

* {#Lawvere66} [[William Lawvere]], *The Category of Categories as a Foundation for Mathematics*, pp. 1-20 in: [[Samuel Eilenberg|S. Eilenberg]], [[D. K. Harrison]], [[S. MacLane]], [[H. Röhrl]] (eds.): *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;


Important reviews of the paper pointing out technical problems appeared here:

* [[John Isbell|J. R. Isbell]], *Review of Lawvere 1966*, Mathematical Reviews **34** (1967) #7332.

* G. Blanc. A. Preller, *Lawvere's basic theory of the category of categories*, JSL **40** (1975) pp.14-18.

A more recent view of Lawvere, exposing in particular his 'M&#252;nchhausen' approach to set-theoretic 'foundations', is in

* [[William Lawvere|F. W. Lawvere]], _Foundations and Applications: Axiomatization and Education_, Bulletin of Symbolic Logic **9** no.2 (2003) pp.213-224. ([ps-preprint](https://www.math.ucla.edu/~asl/bsl/0902/0902-006.ps))

Lawvere briefly comments on his 1965 system 50 years later in (p. 6)

* {#Law16}F. W. Lawvere, *Alexander Grothendieck and the Concept of Space*, address CT15 Aveiro 2016. ([link](http://www.acsu.buffalo.edu/~wlawvere/GrothendiekAveiro15.htm)) 

An insightful and non-partisan view of the ETCC can be found in a section of:

* [[Andreas Blass]], [[Yuri Gurevich]], *Why Sets?*, Bull. Europ. Assoc. Theoret. Comp. Sci. **84** (2004) 139-156.  &lbrack;[doi:10.1007/978-3-540-78127-1_11](https://doi.org/10.1007/978-3-540-78127-1_11), [pdf](https://web.eecs.umich.edu/~gurevich/Opera/172.pdf), [pdf](http://www.math.lsa.umich.edu/~ablass/set.pdf)&rbrack;

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

A critical view of purely categorical foundations can be found in a series of [papers](http://math.stanford.edu/~feferman/papers.html) by S. Feferman:

* [[Solomon Feferman|S. Feferman]], *Categorical Foundations and Foundations of Category Theory*, pp.149-169 in Butts&Hintikka (eds.), _Logic, Foundations of Mathematics, and Computability Theory_, Reidel Dordrecht 1977. ([pdf](http://math.stanford.edu/~feferman/papers/Cat_founds.pdf))

The unattainability of all the formal desiderata proposed by Feferman is discussed in

* M. Ernst, *The Prospects of Unlimited Category Theory: Doing What Remains to be Done*, Review Symbolic Logic **8** no.2 (2015) pp.306-327.

In the following MO discussion, [[Mike Shulman]] also offers additional perspectives on ETCC and ET2CC:

* {#MO-CC}mathoverflow, *Category of categories as a foundation for mathematics*, December 2009 . ([link](http://mathoverflow.net/questions/9269/category-of-categories-as-a-foundation-of-mathematics))

The above worked-out ET2CSC (where the "S" stands for "small") can be found in

* {#HM25} [[Calum Hughes]], Adrian Miranda: _The elementary theory of the 2-category of small categories_, Theory and Applications of Categories *43* 8 (2025) 196–242 &lbrack;[arXiv:2403.03647](https://arxiv.org/abs/2403.03647), [doi:10.70930/tac/c97jx7g2](https://doi.org/10.70930/tac/c97jx7g2)&rbrack;

See also

* {#Blass84}[[Andreas Blass]], _The interaction of category theory and set theory_ , Cont. Math. **30** (1984) pp.5-29. ([draft](http://www.math.lsa.umich.edu/~ablass/interact.pdf))

* {#Weber07} [[Mark Weber]], _Yoneda structures from 2-toposes_, Appl. Categ. Structures, 2007

* [[Jim Lambek]], [[Phil Scott]], *Reflections on Categorical Foundations of Mathematics*, pp.171-185 in  Sommaruga (ed.), _Foundational Theories of Classical and Constructive Mathematics_,  Springer New York 2011. ([draft](https://www.site.uottawa.ca/~phil/papers/LS11.final.pdf)) {#LS11}

* [[Colin McLarty|C. McLarty]], [[Andrei Rodin|A. Rodin]], _A Discussion between Colin McLarty and Andrei Rodin about Structuralism and Categorical Foundations of Mathematics_, n.d. ([pdf](http://canoe.ens.fr/~rodin/spip/IMG/pdf/colin.pdf))

* {#Pryzbylek14} M. R. Pryzbylek, _Logical systems I: Lambda calculi through discreteness_, arxiv:1306.3703v3 (2014). ([pdf](http://arxiv.org/pdf/1306.3703v3))

* {#W71}[[Bob Walters]], _Yoneda 2Categories_ , talk at the University of New South Wales December 1971. ([manuscript](https://dl.dropboxusercontent.com/u/92056191/Archive/temporary_new_material/yoneda.pdf))

[[!redirects elementary theory of the category of categories]]

[[!redirects elementary theory of the 2-category of categories]]



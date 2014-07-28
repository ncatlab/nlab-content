
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

The **elementary theory of the 2-category of categories**, or _ETCC_ for short, is the [[first order logic|first order]] [[theory|axiomatics]] proposed by [[William Lawvere|F.W. Lawvere]] in 1963 for describing the [[Cat|(2-)category of categories]], in view of a categorical [[foundation of mathematics|foundation for mathematics]].

The set of axioms proposed could be thought of as a first step toward refining or [[categorification|categorifying]] the _elementary theory of the category of sets_ ([[ETCS]]). Where the latter axiomatizes a [[base topos]], a fully satisfactory future form of ETCC would axiomatize a base [[2-topos]].

## Idea
In a broad sense, **elementary theory of the category of categories**, or _ETCC_for short, is an appropriate name for any [[first order logic|first order]] [[theory]] axiomatizing the metacategory [[Cat|CAT]] of categories that forms the intuitive background for naive [[category theory]].

Historically, the first attempt to formulate such a system of axioms has been undertaken by [[William Lawvere|F. W. Lawvere]] in his dissertation in 1963 and a subsequent publication (Lawvere 1966) and is this system that is sometimes referred to as _the_ ETCC. In the following we will discuss it and the subsequent attempts to repair its technical flaws under this heading in the next [section](#ETCC).

Taking into account that the intuitively given category of categories is a 2-category, from an n-categorical perspective one would prefer to axiomatize CAT directly as a 2-category and the resulting _elementary theory of the 2-category of categories_, or **ET2CC**, is the subject of section(#ET2CC).

### ETCC: Lawvere (1966) and beyond. {#ETCC}

In his 1963 dissertation launched a life-time project to replace membership based mathematics by more invariant concepts in order to arrive at a renewal of analysis and geometry adapted for the needs of modern (continuum) physics. 

The text takes issue with set-theoretic notions at various levels, e.g. redefining [[adjoint functors]] via [[comma categories]] in order to avoid reference to Hom-sets, but the most radical step is the attempt at a first-order axiomatization of the category of categories that he proposes to bypass set-theory completely as a foundational level.

The system of axiom that he proposes in a more elaborate form in 1966 is layered in three parts:

* The _elementary theory of abstract categories_ (ETAC) has besides equality three primitive predicates for domain, codomain, and composition and as axioms the usual axioms for identity, associativity etc.

* The _basic theory_ adds axioms for **1**, **2** and various exactness properties among which is existence of exponentials. This permits then to define e.g. sets as discrete objects $A$ with $A^1\cong A^2$. The last axiom of the basic theory tries to express the _density-adequacy_ of the simple categories like **1** etc. within the metacategory.

* The _stronger theory_ then adds two further axioms to the basic theory concerning existence of completions and an 'inaccessible' category (p.18).



### ET2CC{#ET2CC}

## Related Pages

* [[ETCS]]
* [[Functorial Semantics of Algebraic Theories]]
* [[foundations of mathematics]]

## References

* F. W. Lawvere, _[[Functorial Semantics of Algebraic Theories]]_ , Ph.D. thesis, Columbia University New York 1963. (With an author's comment and a supplement in: Reprints in Theory and Applications of Categories, no.5 (2004) pp.1-121 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/5/tr5.pdf)))

A revised version of the axioms appears as

* F. W. Lawvere, _The Category of Categories as a Foundation for Mathematics_ , pp.1-20 in Eilenberg, Harrison, MacLane, R&#246;hrl (eds.), _Proceedings of the Conference on Categorical Algebra - La Jolla 1965_ , Springer Heidelberg 1966.

Important reviews of the paper pointing out technical problems appeared here

* [[John Isbell|J. R. Isbell]], _Review of Lawvere 1966_ , Mathematical Reviews **34** (1967) #7332.

* G. Blanc. A. Preller, _Lawvere's basic theory of the category of categories_ , JSL **40** (1975) pp.14-18.

A more recent view of Lawvere exposing in particular his 'M&#252;nchhausen' approach to set-theoretic 'foundations' is in

* [[William Lawvere|F. W. Lawvere]], _Foundations and Applications: Axiomatization and Education_, Bulletin of Symbolic Logic **9** no.2 (2003) pp.213-224. ([ps-preprint](https://www.math.ucla.edu/~asl/bsl/0902/0902-006.ps))

Alternative or complementary approaches are

* [[J. Bénabou]], _Fibered Categories and the foundations of naive category theory_ , JSL **50** (1985) pp.10-37. ([preprint](http://www.cwru.edu/artsci/phil/Benabou%20Fibered.pdf))

* G. Blanc, M. R. Donnadieu, _Axiomatisation de la cat&#233;gorie des cat&#233;gories_ , Cah.Top.G&#233;om.Diff.Cat. **XVII** no. 2 (1976) pp.1-35. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1976__17_2/CTGDC_1976__17_2_135_0/CTGDC_1976__17_2_135_0.pdf))

* [[Colin McLarty|C. McLarty]], _Axiomatizing a category of categories_ , JSL **56** (1991) pp.1243-1260. ([preprint](http://www.cwru.edu/artsci/phil/AxiomatizingCategoryCategories.pdf))

See also

* [[Colin McLarty|C. McLarty]], [[Andrei Rodin|A. Rodin]], _A Discussion between Colin McLarty and Andrei Rodin about Structuralism and Categorical Foundations of Mathematics_, n.d. ([pdf](http://canoe.ens.fr/~rodin/spip/IMG/pdf/colin.pdf))

* mathoverflow, _Category of categories as a foundation for mathematics_ , December 2009 . ([link](http://mathoverflow.net/questions/9269/category-of-categories-as-a-foundation-of-mathematics))

[[!redirects elementary theory of the 2-category of categories]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

Sensible reasoning in [[mathematics]] in general, and particularly in [[higher structures]], such as ([[higher category theory|higher]]) [[category theory]], [[homotopy theory]],  [[homotopy type theory]], etc., should be suitably [[invariant]] under the respective notion of _[[equivalence]]_. This is a common issue whenever some structure is _[[generators and relations|presented]]_ by other structures, since the notion of equivalence of the presentation can be finer than that of the notion being presented. 

For instance, a [[category]] can be presented by a [[simplicial set]] (the [[nerve]] of a corresponding [[strict category]], see [there](nerve#NerveOfACategory)), but [[isomorphism]] of simplicial sets is much finer than [[equivalence of categories|equivalences]] of their corresponding categories. It is generally a _mistake_ to mix up these two levels and, for instance, assign to a category properties that are shared only by _some_ of the simplicial sets representing it, say, by distinguishing between [[isomorphism|isomorphic]] [[objects]]. This _breaks the equivalence invariance_.  (However, see [below](#Breaking).)

The ideas here generalize in many directions.  For example, not only properties, but also constructions involving categories and functors, can fail to preserve equivalences.  

## Terminology
{#terminology}

* [[Michael Makkai]] proposed  the _Principle of Isomorphism_, "all grammatically correct properties of objects of a fixed category are to be invariant under isomorphism", in his [paper](https://projecteuclid.org/ebooks/lecture-notes-in-logic/Logic%20Colloquium%20'95:%20Proceedings%20of%20the%20Annual%20European%20Summer%20Meeting%20of%20the%20Association%20of%20Symbolic%20Logic,%20held%20in%20Haifa,%20Israel,%20August%209-18,%201995/chapter/Towards%20a%20Categorical%20Foundation%20of%20Mathematics/lnl/1235415906)
"Towards a categorical foundation of mathematics", in Johann A. Makowsky, Elena V. Ravve, eds., Logic Colloquium '95: Proceedings of the Annual European Summer Meeting of the Association of Symbolic Logic, held in Haifa, Israel, August 9-18, 1995 (Berlin: Springer-Verlag, 1998), 153-190.

* [[Peter Aczel]] mentioned a similar concept, the _[[structure identity principle|Structure Identity Principle]]_, "isomorphic structures have the same structural properties" in Oberwolfach [report 52/2011](http://www.mfo.de/document/1145/OWR_2011_52.pdf). This seems a priori a little weaker to [[David Roberts|me]], but if we demand that objects should be seen as only having structural properties (as opposed to the category of [[ZF]]-[[sets]]), then we look like we get back the Principle of Isomorphism.

* A very precise way of stating this idea is encapsulated in [[Vladimir Voevodsky]]'s [[univalence axiom]], which is a fundamental part of [[homotopy type theory]] as a [[foundation]] for mathematics.  By identifying equivalences/isomorphisms with inhabitants of an [[identity type]], it ensures that all properties and structure which can be expressed within the formal [[type theory]] are invariant under such (see [AhrensNorth18](#AhrensNorth18)).

* {#evil} In the [[category theory]] and [[higher category theory]] literature, a [[mathematical structure]] or [[definition]] is **evil** if it breaks equivalence invariance (see e.g. [Pavlovic 2023](#Pavlovic23), [Ferrer et al. 2024](#FerrerEtAl24)). The usage of the term "evil" in category theory originated from [[John Baez]] and [[Toby Bartels]] in 2008 in the early days of the nLab (see [[2008 changes]]). 

**Note:** *Due to confusion with the concept of evil in moral [[philosophy]], the nLab now discourages the usage of the term "evil" on the nLab itself to refer to the concept of breaking equivalence invariance, instead preferring alternative ways to describe the concept. If you encounter uses of this sort elsewhere on the nLab, please replace them if possible.* 

*Sometimes it is not possible to remove instances of "evil" on the nLab that are used for "breaking equivalence invariance", such as if "evil" is used in a quotation from a reference. For example, in the [[Center for Quantum and Topological Systems]] article, "evil" appears in the quoted abstract of the 2023 [[CQTS]] talk [Johnson-Freyd 2023](#JohnsonFreyd23) that appears on the article, and so is unavoidable unless the quoted abstract itself is removed from the article. In this case, it is fine to leave "evil" in the article as part of the quote.*

## Motivation

### From mathematical practice

...

>Draw an analogy with vector spaces (maybe just finite-dimensional ones?).  We can *use* a basis to study a vector space, but the basis is not *part of* the vector space.  Even if we use a foundation of mathematics in which the basis literally is part of the vector space (which arguably was the case for 18th-century linear algebra, which studied only Cartesian spaces; and is still the case today if we study finite-dimensional vector spaces using a foundational type theory with propositions as types, but probably this is too obscure), anything that we consider to be a property *of the vector space* should be independent of the basis.  We can make this precise by comparing the groupoids $Vect_\sim$ and $Vect_b$.

...

### From foundations and logic

In [[material set theory]] based on [[ZFC]], any two objects are [[pure sets]] and can be compared for [[equality]].  Yet this is often mathematical nonsense which depends on precisely how one writes definitions; for example, the [[ordered pair]] $(0,0)$ is equal to the [[natural number]] $1$ by some standards and equal to $2$ by other standards (while $(1,1) = 2$ by yet other standards), but this makes no difference mathematically.  In contrast, [[structural set theory]] either implicitly (as in [[ETCS]]) or explicitly (as in [[SEAR]] or [[ETCS with elements]]) considers only equality between [[elements]] of a given [[set]] (or [[functions]] or [[binary relations]] between two given sets, etc).  This can be built into the [[logic]] using [[dependent type theory]] (which can serve as a foundation all by itself). The result is that, depending on precisely how one writes definitions, it may or may not be possible to compare two things for equality. For example, the ordered pair $(1, 1)$ is equal to $2$ under triangular encoding, equal to $3$ under binary encoding, and equal to $1$ under Chinese Remainder encoding. But if we take ordered pairs as primitive, it makes no sense to compare $(1, 1)$ to $2$. (Of course, we could do this in material set theory as well; but allowing non-set primitives there would defeat the traditional attraction of the theory.)

Does it make sense, then, to ask whether two arbitrary *sets* are equal?  In material set theory, of course it does; two sets are equal if they have the same elements (by the [[axiom of extensionality]]).  But structurally, this definition is meaningless.  All the same, a structural set theory built on [[first-order logic]] with equality automatically gives this question (whether two arbitrary sets are equal) a meaning, as do the most common forms of foundational type theory, but this is again never used in mathematics.  ($SEAR$, which is based on first-order logic without equality, does not give this question a meaning and does not suffer for it.)  So just as we don\'t need to ask whether $(0,0) = 2$, we don\'t need to ask whether $\{(0,0)\} = \{2\}$ as sets.  (Note that this is a completely different question, structurally, from whether, say, $\{(0,0)\} = \{2\}$ as *[[subsets]]* of $\mathbb{N} \coprod (\mathbb{N} \times \mathbb{N})$.)

Now let us move from the foundations of [[set theory]] to those of [[category theory]].  Usually, category theory is founded on set theory, or something very much like it; if the [[objects]] of a category don\'t form a set, then this is only because of [[size issues]], and they still form a [[proper class]].  Accordingly, it makes sense to compare them for equality.  However, if the [[category of sets]] is itself an example of a category, then by the previous paragraph, it does *not* have to make sense (and is mathematically meaningless) to test the objects of this category for equality.  So we get the idea that we cannot compare objects of a given category for equality in general (although this may make sense for particular categories).  In other words, a [[category]] is not by default a [[strict category]] (a category equipped with the [[extra stuff]] of an explicit equality predicate on its objects).

We can found mathematics on type theory without identity types, and then it is literally true that (in general) it makes no sense to compare objects of a given type for equality; one has to *define* a relevant equality predicate when there is one.  From the other direction, we can found mathematics on (weak) $\infty$-[[infinity-groupoid]] theory, i.e. [[homotopy theory]] (as in [[homotopy type theory]]), where the automatic notion of equality between object of a category is actually only isomorphism.

However, these are not commonly used foundations.  Therefore, category theory is usually written in a language in which it does literally make sense to ask whether two objects of a given category are equal (meaning something stronger than that they are isomorphic), whether two functors between two given categories are equal, etc.  If we want these definitions to make sense in the general mathematical situation (where $Set$ is an example of a category, even though comparing two arbitrary sets for equality makes no mathematical sense), then we need to check that our definitions are compatible with the principle of equivalence.

(Strictly speaking, it does not even make sense to ask if two arbitrary sets are isomorphic; going back to our earlier example, $\{(0,0)\}$ is isomorphic to $\{2\}$ as objects of $Set$ because they are both singletons, but they are not isomorphic as objects of the poset of subsets of $\mathbb{N} + \mathbb{N}\times \mathbb{N}$, because neither is a subset of the other.)

### From philosophy

In [[Tractatus Logico-Philosophicus]], 2.02331, [[Wittgenstein]] writes

> Either a thing has properties that nothing else has, in which case we can immediately use a description to distinguish it from the others and refer to it; or, on the other hand, there are several things that have the whole set of their properties in common, in which case it is quite impossible to indicate one of them. For if there is nothing to distinguish a thing, I cannot distinguish it, since otherwise it would be distinguished after all.

Given that a main theme of the Tractatus is on the limits of language, it is tempting to consider this as a description not just for 'the world' (as in _Tractatus_ 1.), but for any given language and the objects about which one reasons in that language. This seems to encapsulate Makkai's motivation alluded to above.

## General definition

If $X$ is an $\infty$-[[infinity-groupoid|groupoid]], then a property $P$ of objects of $X$ is _compatible with equivalence_ if, whenever $P(a)$ holds for an object $a$ of $X$ and $b$ is [[equivalence|equivalent]] (as an object of $X$) to $a$, then $P(b)$ holds. Alternatively, an operation $f$ from objects of $X$ to objects of (another $\infty$-groupoid) $Y$ is __compatible with equivalence__ if, whenever $a$ and $b$ are equivalent objects of $X$, $f(a)$ and $f(b)$ are equivalent objects of $Y$.

(Note that everything is an object of some $\infty$-groupoid. For example, a $2$-morphism in some random $5$-category is an object of a hom-$3$-category, which has an [[core|underlying]] $3$-groupoid, which is a special kind of $\infty$-groupoid. For some purposes, this $2$-morphism may instead need to be seen as an object in a $2$-arrow $5$-category, which has an underlying $\infty$-groupoid as well; exactly which $\infty$-groupoid is relevant depends on the [[context]]. Also note that we really do need $\infty$-groupoids here, rather than $\infty$-categories, since dualities do respect equivalences.)

The operation-version of the principle of equivalence gives the property-version if you think of a property as an operation taking values in the $\infty$-groupoid (in fact a $0$-groupoid, or [[set]]) of [[truth value|truth values]]. (The property-version also gives the operation-version, although that is a little more involved.) An operation will obey the principle of equivalence if it is given (as the object-operation) by a [[functor]] ('$\infty$-functor', if you prefer). A property adheres to the principle of equivalence precisely if it\'s a functor to the $\infty$-groupoid of truth values.

This definition should be the conclusion of a theorem that using certain language (including avoiding equations between objects of a category) makes it impossible to say anything that violates the principle of equivalence. [[Michael Makkai]] works on such a language, [[FOLDS]] ('first-order logic with dependent sorts'), which does not include an axiomatic notion of [[equality]] at all. This pertains to the [mathematical foundations of category theory](foundations#MFCT). To learn more, see his paper _[First Order Logic with Dependent Sorts, with Applications to Category Theory](http://www.math.mcgill.ca/makkai/)_.


## Examples

### In category theory

A common misconception in category theory is that [[strict categories]] violate the principle of equivalence. However, this is not true; strict categories are the mathematical structures in which the equivalence of objects are precisely equality on objects: important examples of strict categories which do not violate the principle of equivalence include [[posets]] and the [[walking parallel pair]]. In fact, every strict category is equivalent to a [[setoid]]-valued [[presheaf]] on the [[simplex category]] or the full subcategory of the [[arrow category]] of the [[(2,1)-category]] of [[weak categories]], consisting of [[essentially surjective functors]] whose [[domain]] is a [[setoid]]. 

Instead, what does break the principle of equivalence is to say that certain [[concrete categories]] with non-trivial [[automorphisms]] such as [[Set]] or [[Grp]] are strict categories, as the objects of the categories are [[sets]], and equality of objects is equality of sets. In this case, one has to instead say that they are [[isomorphism|isomorphic]] and then (usually) impose some [[coherence relation]] on the relevant family of isomorphisms.  But of course, this is more complicated!

#### Identity-on-objects functors

The concept of an [[identity-on-objects functor]] appears in category theory as well, particularly when defining [[Freyd categories]] and [[dagger categories]]. The traditional definition goes as follows:

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ is a functor between categories with the same collection of [[objects]], and has as its underlying object function $F_{ob}$ the [[identity function]] on the collection of objects. 
\end{definition}

However, in [[material set theories]] or material class theories, "having the same collection of objects" is sometimes defined as $Ob = ob(A) = ob(B)$. This definition involves equality of sets, which violates the principle of equality. 

Instead, what category theorists usually mean by two categories having the same objects is actually having a single $(Set \times Set)$-[[enriched category]], where morphisms are in families of sets of pairs $(f,g):A(x,y) \times B(x,y))$ for objects $x$ and $y$, and composition is composition of pairs of morphisms $(h,k)\circ(f,g) = (h \circ f,k \circ g)$ for $f:A(x,y)$, $g:B(x,y)$, $h:A(y,z)$, and $k:B(y,z)$. 

Another problem occurs in [[set theories]] with certain [[concrete categories]] like [[Rel]], [[Hilb]], and the [[permutation category]] $\mathbb{P}$: the objects of the categories are sets, and so saying that the underlying function $F_ob$ on the objects is the identity function violates the principle of equality, because by definition $F_ob(x) = x$ for all objects $x$, and because objects are sets, one is talking about equality of sets. 

Instead, when category theorists are talking about two categories with the same collection of objects and and identity-on-objects functor, what they really are talking about is an $Set^I$-enriched category, where $Set^I$ is the [[arrow category]] of $Set$. 

#### In the concept of $\dagger$-categories
  {#daggers}

A **[[†-category]]** is a [[category]] $C$ with a function $(-)^\dagger: Hom_C(A,B) \to hom_C(B,A)$ for every object $A,B \in Ob(C)$, such that 

* For every $A \in Ob(C)$, $(1_A)^\dagger = 1_A$
* For every $A,B \in Ob(C)$ and every $f \in Hom_C(A,B)$ and $g \in Hom_C(B,C)$, $(g \circ f)^\dagger = f^\dagger \circ g^\dagger$
* For every $A,B \in Ob(C)$ and every $f \in Hom_C(A,B)$, $((f)^\dagger)^\dagger = f$. 

However, there is another definition of a †-category, as a category $C$ with a functor

$$F\colon C \to C^{op} $$

which is the identity on objects and has $F^2 = 1$.  

This second definition break equivalence-invariance: it imposes equations between objects, so we cannot transport a dagger-category structure along an equivalence of categories.

##### Historical comments

It was once believed that there was no known way to express the idea without equations between objects. This stemmed from the fact that category theorists were using functors to define the dagger. It was only later that it was recognized that one could include the dagger in the definition of dagger categories in the same way that one includes composition of morphisms in the definition of category, which resulted in a definition of dagger category that doesn't violate the principle of equivalence. 

A discussion about this is [archived on the nForum](https://nforum.ncatlab.org/discussion/4201/principle-of-equivalence/?Focus=101442#Comment_101442).


#### In higher category theory

It violates the principle of equivalence to state that two morphisms in a $2$-[[2-category|category]] are equal, because these morphisms are objects in a [[hom-category]], but does not violate the principle of equivalence to state that that two $2$-morphisms are equal, given a common source and target.  And so on.  In an $\infty$-[[infinity-category|category]], *every* claim of equality break equivalence-invariance.

Defining higher categorial structures using such equalities tends to lead to *strict* concepts; avoiding them and imposing coherence relations leads to *weak* concepts.  Sometimes there is a [[coherence theorem]] showing that every weak concept can be strictified, which justifies using equality as a figure of speech.  See [[bicategory]], [[Gray-category]], and [[model category]] for examples of this in action.

### In physics

Since [[Hilb]] and [[nCob]] are [[dagger-categories]], the discussion [above](#daggers) is relevant, particularly for [[TQFT]].


#### In gauge theory

See at

* [[gauge transformation]], [[gauge equivalence]], [[gauge invariance]]


#### In gravity


The principle of equivalence in [[general relativity]] (see [[equivalence principle (physics)]]) is a special case of this principle of equivalence; the objects of the $\infty$-groupoid are physical "fields" (not to be confused with algebraic fields!), and the isomorphisms are [[coordinate transformation]]s. So physical properties and operations should not depend on the choice of coordinate system, and this is enforced by allowing only functorial operations, which are specifically taken to be generated by [[trace]]s, [[tensor product]]s, and linear operations acting on the [[pseudo-Riemannian metric]], and the [[covariant derivative]].

See at

* [[general covariance]]


## How to break equivalence-invariance
{#Breaking}

Just as we can make use of [[basis|bases]] in [[linear algebra]], so we may make use of [[strict categories]] to discuss [[category theory]].  Philosophically, the concept of strict category is not in itself a breaking of equivalence-invariance; what does break equivalence-invariance is to say that $Set$ (and other well-known categories such as [[Grp]], etc) *are* strict categories.  Mathematically, strict categories form a $1$-[[1-groupoid|groupoid]] $Str Cat_\sim$ that is different from the $2$-[[2-groupoid|groupoid]] $Cat_\sim$, but there is still a canonical [[pseudo functor]] from $Str Cat_\sim$ to $Cat_\sim$ that we may find useful.

Much as the [[axiom of choice]] tells us that every vector space has a basis, so the global axiom of choice tells us that every category may be given the structure of a strict category.  Then we can use this extra structure (in either case), as long as we prove that the result is independent of the structure chosen.  Even if we don\'t wish to accept the axiom of choice, we can still prove a theorem about those vector spaces that have bases or those categories that can be given a strict structure.

Perhaps the extreme case of this is using [[model categories]] to study [[homotopy theory]], which is (from the [[nPOV]]) really about $(\infty,1)$-[[(infinity,1)-category|categories]].  Even if model categories are not taken to be strict categories, they still form a $2$-groupoid and thus are still far more strict than $(\infty,1)$-categories, which only form an $\infty$-[[infinity-groupoid|groupoid]].  Nevertheless, they are quite useful (at least assuming the axiom of choice?).


## References
 {#References}

A discussion of the principle of equivalence in the very [[foundations]] of mathematics by replacing [[ZFC]] by [[homotopy type theory]] is in

* [[Vladimir Voevodsky]], _Foundations/formalization of mathematics and homotopy theory_, talk at IAS ([video](http://video.ias.edu/node/68))

* {#CoquandDanielsson} [[Thierry Coquand]], Nils Anders Danielsson, _Isomorphism is equality_ ([pdf](http://www.cse.chalmers.se/~nad/publications/coquand-danielsson-isomorphism-is-equality.pdf))

* {#Awodey14} [[Steve Awodey]], _Structuralism, Invariance, and Univalence_ (2014) ([pdf](https://www.andrew.cmu.edu/user/awodey/preprints/siu.pdf))

* {#AhrensNorth18} [[Benedikt Ahrens]], [[Paige Randall North]], _Univalent foundations and the equivalence principle_, ([pdf](https://paigenorth.github.io/ep.pdf))

For the use of the term "evil" to refer to the violation of the [[principle of equivalence]] in [[category theory]] and [[higher category theory]]:

* {#JohnsonFreyd23} [[Theo Johnson-Freyd]], *Higher Dagger Categories*, [talk at](Center+for+Quantum+and+Topological+Systems#JohnsonFreydNov2023) [[CQTS]] (08 Nov 2023) &lbrack;slides:[pdf](http://categorified.net/NYUADtalk.pdf), [[JohnsonFreyd-HigherDaggerNYUAD.pdf:file]], video:[YT](https://youtu.be/zvtziTpl2T0)&rbrack;

* {#Pavlovic23} [[Dusko Pavlovic]], *Catales: From topologies without points to categories without objects* &lbrack;[arXiv:2311.10342](https://arxiv.org/abs/2311.10342)&rbrack;

* {#FerrerEtAl24} [[Giovanni Ferrer]], [[Brett Hungar]], [[Theo Johnson-Freyd]], [[Cameron Krulewski]], [[Lukas Müller]], [[Nivedita]], [[David Penneys]], [[David Reutter]], [[Claudia Scheimbauer]], [[Luuk Stehouwer]], [[Chetan Vuppulury]], *Dagger n-categories* &lbrack;[arXiv:2403.01651](https://arxiv.org/abs/2403.01651)&rbrack;

[[!redirects principle of isomorphism]]
[[!redirects principle of equivalence]]
[[!redirects principle of invariance]]
[[!redirects principle of covariance]]

[[!redirects evil]]
[[!redirects evil definition]]
[[!redirects evil structure]]

[[!redirects non-evil]]
[[!redirects non-evil definition]]
[[!redirects non-evil structure]]
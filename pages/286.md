
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

Sensible reasoning in [[mathematics]] in general, and in [[higher structures]], such as ([[higher category theory|higher]]) [[category theory]], [[homotopy theory]],  [[homotopy type theory]], etc., should be suitably [[invariant]] under the respective notion of _[[equivalence]]_. This is a common issue whenever some structure is _[[generators and relations|presented]]_ by other structures, since the notion of equivalence of the presentation can be finer than that of the notion being presented. 

For instance, a [[category]] can be presented by a [[simplicial set]], but [[isomorphism]] of simplicial sets is much finer than [[equivalence of categories|equivalences]] of their corresponding categories. It is generally a _mistake_ to mix up these two levels and, for instance, assign to a category properties that are shared only by _some_ of the simplicial sets representing it, say, by distinguishing between [[isomorphism|isomorphic]] [[objects]]. This _breaks the equivalence invariance_.  (However, see [below](#Breaking).)

The ideas here generalize in many directions.  For example, not only properties, but also constructions involving categories and functors, can fail to preserve equivalences.  


## Terminology
{#terminology}

* [[Michael Makkai]] proposed  the _Principle of Isomorphism_, "all grammatically correct properties of objects of a fixed category are to be invariant under isomorphism", in his [paper](https://projecteuclid.org/ebooks/lecture-notes-in-logic/Logic%20Colloquium%20'95:%20Proceedings%20of%20the%20Annual%20European%20Summer%20Meeting%20of%20the%20Association%20of%20Symbolic%20Logic,%20held%20in%20Haifa,%20Israel,%20August%209-18,%201995/chapter/Towards%20a%20Categorical%20Foundation%20of%20Mathematics/lnl/1235415906)
"Towards a categorical foundation of mathematics", in Johann A. Makowsky, Elena V. Ravve, eds., Logic Colloquium '95: Proceedings of the Annual European Summer Meeting of the Association of Symbolic Logic, held in Haifa, Israel, August 9-18, 1995 (Berlin: Springer-Verlag, 1998), 153-190.

* [[Peter Aczel]] mentioned a similar concept, the _Structure Identity Principle_, "isomorphic structures have the same structural properties" in Oberwolfach [report 52/2011](http://www.mfo.de/document/1145/OWR_2011_52.pdf). This seems a priori a little weaker to [[David Roberts|me]], but if we demand that objects should be seen as only having structural properties (as opposed to the category of [[ZF]]-[[sets]]), then we look like we get back the Principle of Isomorphism.

* A very precise way of stating this idea is encapsulated in [[Vladimir Voevodsky]]'s [[univalence axiom]], which is a fundamental part of [[homotopy type theory]] as a [[foundation]] for mathematics.  By identifying equivalences/isomorphisms with inhabitants of an [[identity type]], it ensures that all properties and structure which can be expressed within the formal [[type theory]] are invariant under such (see [AhrensNorth18](#AhrensNorth18)).

* {#evil} Floating around the web (and maybe the $n$Lab) is the idea of half-jokingly referring to a breaking of equivalence invariance as "evil". This is probably meant as a pedagogical way of amplifying that it is to be avoided.


## Motivation

### From mathematical practice

...

>Draw an analogy with vector spaces (maybe just finite-dimensional ones?).  We can *use* a basis to study a vector space, but the basis is not *part of* the vector space.  Even if we use a foundation of mathematics in which the basis literally is part of the vector space (which arguably was the case for 18th-century linear algebra, which studied only Cartesian spaces; and is still the case today if we study finite-dimensional vector spaces using a foundational type theory with propositions as types, but probably this is too obscure), anything that we consider to be a property *of the vector space* should be independent of the basis.  We can make this precise by comparing the groupoids $Vect_\sim$ and $Vect_b$.

...


### From foundations and logic

In [[material set theory]] based on [[ZFC]], any two objects are [[pure sets]] and can be compared for [[equality]].  Yet this is often mathematical nonsense which depends on precisely how one writes definitions; for example, the [[ordered pair]] $(0,0)$ is equal to the [[natural number]] $1$ by some standards and equal to $2$ by other standards (while $(1,1) = 2$ by yet other standards), but this makes no difference mathematically.  In contrast, [[structural set theory]] either implicitly (as in [[ETCS]]) or explicitly (as in [[SEAR]]) considers only equality between [[elements]] of a given [[set]] (or [[functions]] or [[binary relations]] between two given sets, etc).  This can be built into the [[logic]] using [[dependent type theory]] (which can serve as a foundation all by itself). The result is that, depending on precisely how one writes definitions, it may or may not be possible to compare two things for equality. For example, the ordered pair $(1, 1)$ is equal to $2$ under triangular encoding, equal to $3$ under binary encoding, and equal to $1$ under Chinese Remainder encoding. But if we take ordered pairs as primitive, it makes no sense to compare $(1, 1)$ to $2$. (Of course, we could do this in material set theory as well; but allowing non-set primitives there would defeat the traditional attraction of the theory.)

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

If $X$ is an $\infty$-[[infinity-groupoid|groupoid]], then a property $P$ of objects of $X$ is _compatible with equivalence_ if, whenever $P(a)$ holds for an object $a$ of $X$ and $b$ is [[equivalence|equivalent]] (as an object of $X$) to $a$, then $P(b)$ holds. Alternatively, an operation $f$ from objects of $X$ to objects of (another $\infty$-groupoid) $Y$ is __compatible with equivalence__ if, whenever $a$ and $b$ are equivalent objects of $X$, $f(a)$ and $f(b)$ are equivalent (as objects of $Y$).

(Note that everything is an object of some $\infty$-groupoid. For example, a $2$-morphism in some random $5$-category is an object of a hom-$3$-category, which has an [[core|underlying]] $3$-groupoid, which is a special kind of $\infty$-groupoid. For some purposes, this $2$-morphism may instead need to be seen as an object in a $2$-arrow $5$-category, which has an underlying $\infty$-groupoid as well; exactly which $\infty$-groupoid is relevant depends on the [[context]]. Also note that we really do need $\infty$-groupoids here, rather than $\infty$-categories, since dualities do respect equivalences.)

The operation-version of the principle of equivalence gives the property-version if you think of a property as an operation taking values in the $\infty$-groupoid (in fact a $0$-groupoid, or [[set]]) of [[truth value|truth values]]. (The property-version also gives the operation-version, although that is a little more involved.) An operation will obey the principle of equivalence if it is given (as the object-operation) by a [[functor]] ('$\infty$-functor', if you prefer). A property adheres to the principle of equivalence precisely if it\'s a functor to the $\infty$-groupoid of truth values.

This definition should be the conclusion of a theorem that using certain language (including avoiding equations between objects of a category) makes it impossible to say anything that violates the principle of equivalence. [[Michael Makkai]] works on such a language, [[FOLDS]] ('first-order logic with dependent sorts'), which does not include an axiomatic notion of [[equality]] at all. This pertains to the [mathematical foundations of category theory](foundations#MFCT). To learn more, see his paper _[First Order Logic with Dependent Sorts, with Applications to Category Theory](http://www.math.mcgill.ca/makkai/)_.


## Examples

### In category theory

The most common source of the breaking of equivalence-invariance is a statement that two [[objects]] of a given [[category]] are [[equality|equal]].  One should instead say that they are [[isomorphism|isomorphic]] and then (usually) impose some [[coherence relation]] on the relevant family of isomorphisms.  But of course, this is more complicated!

It does not break equivalence-invariance to state that two [[morphisms]] are equal, given a common [[source]] and [[target]]; this is because a [[hom-set]] is a [[set]], where equality is meaningful.  However, it violates the principle of equivalence to state that two morphisms are equal if the source and target are *not* given, because this includes the claim that their sources (which are objects) are equal, and similarly for the targets.


#### In higher category theory

It violates the principle of equivalence to state that two morphisms in a $2$-[[2-category|category]] are equal, because these morphisms are objects in a [[hom-category]], but does not violate the principle of equivalence to state that that two $2$-morphisms are equal, given a common source and target.  And so on.  In an $\infty$-[[infinity-category|category]], *every* claim of equality break equivalence-invariance.

Defining higher categorial structures using such equalities tends to lead to *strict* concepts; avoiding them and imposing coherence relations leads to *weak* concepts.  Sometimes there is a [[coherence theorem]] showing that every weak concept can be strictified, which justifies using equality as a figure of speech.  See [[bicategory]], [[Gray-category]], and [[model category]] for examples of this in action.


#### In the concept of $\dagger$-categories
  {#daggers}

A **[[†-category]]** is a category $C$ with a functor

$$F\colon C \to C^{op} $$

which is the identity on objects and has $F^2 = 1$.  

This definition break equivalence-invariance: it imposes equations between objects, so we cannot transport a dagger-category structure along an equivalence of categories.
Often concepts violating the principle of equivalence (like the concept of "strict monoidal category") have equivalence-invariant counterparts (like the concept of "monoidal category").  But in this particular case there appears to be no known way to express the idea without equations between objects.  Both [[Hilb]] and [[nCob]] are dagger-categories.  This fact is important.  Try saying it in a way that obeys the principle of equivalence!  

It is possible that this problem will force a change in thinking in either the concept of the principle of equivalence or our thinking in quantum theory.

+-- {: .query}
[[Mike Shulman]]: Actually, I believe that $\dagger$-structure on a category *can* be transported along an equivalence of categories!  Suppose that $F\colon C \to D \colon G$ is an [[adjoint equivalence]] with unit $\eta\colon Id_C \overset{\cong}{\to} G F$ and counit $\varepsilon\colon F G \overset{\cong}{\to} Id_D$, where $D$ is a $\dagger$-category.  Given $f\colon x\to y$ in $C$, define $f^\dagger$ to be the following composite:
$$ y \overset{\eta}{\to} G F y \overset{G((F f)^\dagger)}{\to} G F x \overset{\eta^{-1}}{\to} x. $$
This evidently defines a functor $C^{op} \to C$ that is the identity on objects.  Now $F(f^\dagger)$ is given by
$$ F y \overset{F \eta}{\to} F G F y \overset{F G((F f)^\dagger)}{\to} F G F x \overset{F \eta^{-1}}{\to} F x $$
but by the triangle identities this is equal to
$$ F y \overset{\varepsilon^{-1}_F}{\to} F G F y \overset{F G((F f)^\dagger)}{\to} F G F x \overset{\varepsilon_F}{\to} F x $$
and hence equal to $(F f)^\dagger$ by naturality of $\varepsilon$.  Thus, since $((F f)^\dagger)^\dagger = F f$ in $D$, in $C$ we have that $(f^\dagger)^\dagger$ is given by
$$ x \overset{\eta}{\to} G F x \overset{G F f}{\to} G F y \overset{\eta^{-1}}{\to} y. $$
which is equal to $f$ by naturality of $\eta$.  Thus, $C$ is a $\dagger$-category, and essentially by construction $F$ and $G$ are $\dagger$-functors (though $\eta$ and $\varepsilon$ need not be unitary).

So if a notion refers to equality of objects in a seemingly irreducible way, but it can nevertheless be transported along an equivalence of categories, does it break equivalence invariance or not?  Thinking about it some more, I'm actually not convinced that $\dagger$-structure violates the principle of equivalence at all.  Consider the assertion that a category is a groupoid.  Clearly this does not break equivalence-invariance!  But what it means is that for any morphism $f\colon x\to y$, there exists a morphism $f^{-1}\colon y\to x$ whose source is *equal* to the target of $f$, and whose target is *equal* to the source of $f$, and such that $f f^{-1}$ and $f^{-1} f$ are identities.  The notion of $\dagger$-category is entirely analogous: for any morphism $f\colon x\to y$, we are given a specified morphism $f^\dagger\colon y\to x$ with certain properties.  The only difference is that the first is a *property* and the second is *structure*, but why should that matter?

As remarked in the discussion below, equality of objects is all over the place in category theory: whenever we introduce an arrow, we have to say what its source and target are, and one or the other (or both) will often be *equal* to some object we are already considering.  But this does not really break equivalence-invariance; it's really just a *typing assertion*.  (If you write category theory in a logic of [[dependent types]] like [[FOLDS]], then that's exactly what it is.)  Maybe $\dagger$-structure is just the same.

[[Mike Shulman]]: Here's an interesting analogy: let $G$ be a group and consider categories enriched over $G$-sets.  In such a category, for every morphism $f\colon x\to y$ and every $g\in G$ we have another morphism $f^g\colon x\to y$ satisfying certain axioms, which may look like breaking equivalence-invariance (since $f^g$ has equal source and target to $f$) but is really not.  Moreover, just like for $\dagger$-categories and unitary isomorphisms, in this case the "underlying groupoid" is not the naive core of the original category, but consists of only the $G$-fixed isomorphisms.  Actually, $\dagger$-categories have always felt a lot like enriched categories to me, though the "enrichment" is sort of "non-local" in that the structure on homsets relates more than one of them, so it's hard to make this precise.

_Toby_:  I agree, the concept is not really violating the principle of equivalence, although you have clarified the ideas for me, so that now I think that I can write a good note to the mailing list.  (In particular, the idea that a dagger structure is analogous to the property of being a groupoid, only slightly harder to grok since it is not a property-like structure, was helpful.)

If you specify a functor $\dagger\colon C^{op} \to C$ and ask whether it is a dagger structure, that is (taken literally) a question that breaks equivalence-invariance; you can ask instead whether it is naturall isomorphic to a dagger structure.  But the concept of dagger structure does not itself violate the principle of equivalence,  if broken down a little.

[[Peter Selinger]]: what you have shown here is a special case of the fact that dagger structure is reflected by full and faithful functors. Specifically, given $F\colon C\to D$ full and faithful, and a dagger structure on $D$, you can define a dagger structure on $C$ by the equation $F(f^\dagger) = (F(f))^\dagger$. This obviously uniquely determines $f^\dagger$, because $F$ is full and faithful.
It is also the unique dagger structure on $C$ such that $F$ becomes a dagger functor. It's almost trivial to verify that this is indeed a dagger structure. 

It coincides with what Mike Shulman has defined, showing in particular that his definition is independent of $G$, $\eta$, and $\epsilon$. Moreover, the definition is _not_ invariant under natural isomorphism of $F$; given a different $F'$ naturally isomorphic to $F$, this will in general induce a different dagger structure on $C$. Also, $G$ will not be a dagger functor with respect to the structure Mike defined.

To me, the facts listed in the last paragraph are good indication that Mike's notion is not the right notion of "transporting structure along an equivalence". I would expect both $F$ and $G$ to respect the transported structure. I would even go as far as requiring $\eta$ and $\epsilon$ to be dagger natural transformations w.r.t. the transported structure. (A dagger natural transformation is one that is componentwise unitary). 

I proposed a formal definition of "transporting structure along an equivalence" on the categories list. It works for any 2-functor between 2-categories.

[[Peter Selinger]]: Here is another view of dagger categories.  What makes
some people uneasy about the dagger structure is
that it runs counter to the usual categorical intuition that all
information is contained in the morphisms. Or more precisely, that all
information about an object $A$ is contained in the natural family of
hom-sets $(X,A)$. So in ordinary category theory, we consider two objects
$A$, $B$ "the same" if they have "the same" generalized points, i.e., if
the contravariant representable functors $(X,A)$ and $(X,B)$ are naturally
isomorpic.

$$ (X,A) \overset{nat.\;isomorphism}\to (X,B) $$

Alternatively, one can say that $A$ and $B$ are the same if the covariant
representable functors are naturally isomorphic. 

$$ (A,X) \overset{nat.\;isomorphism}\to (B,X) $$

Of course, by the Yoneda Lemma, both conditions are equivalent to an
isomorphism between $A$ and $B$, and therefore to each other. But that is
just a lucky simplification.

In dagger categories, the hom-sets are also equipped with
distinguished bijections $\dagger\colon(X,A)\to (A,X)$. It therefore makes sense
to say that, for two objects to be "really" the same, not only should
one have natural isomorphisms such as above, but further that the
diagram should commute:

$$ \array {
   (X,A)              & \overset{nat.\;isomorphism}\to & (X,B) \\
   \dagger \downarrow &                                & \downarrow \dagger \\
   (A,X)              & \overset{nat.\;isomorphism}\to & (B,X)
} $$

In general, an isomorphism $f \colon A \to B$ will induce natural isomorphisms
$(X,A) \to (X,B)$ and $(A,X) \to (B,X)$ that do _not_ make the diagram
commute. It makes the diagram commute if and only if for all $g\in(X,A)$, $g^\dagger \circ f^{-1} = (f \circ g)^\dagger$, in other words, if and
only if $f$ is unitary. This is why unitary isomorphisms are the "real" isomorphisms of dagger categories, and unitary natural transformations are the "real" natural transformations of dagger categories. They preserve and transport everything.

All this indicates to me that dagger is a primitive operation (like
composition). In this respect I completely agree with Toby. As a primitive operation, dagger must be included in the definition of primitive
concepts, such as equivalence. And primitive operations (like
composition) are allowed to talk about objects and be strict.

If someone knows how to wiki-ize the above diagrams, please feel free.

_Toby_:  I did the diagrams a bit, but I don\'t have any more time for a complete reply tonight.

[[Mike Shulman]]: Okay, you are right.  "Transporting along an equivalence" should mean that the forgetful functor is an equiv-fibration, i.e. lifts entire adjoint equivalences rather than merely functors that happen to be equivalences.  I think I disagree, however, that primitive operations (in something that we want to think of as a kind of category theory) should be freely allowed to talk about objects and be strict; I think they should also be formulated in a dependent type theory that only uses equality of objects as a typing assertion.  Dagger categories also satisfy this property.
=--

See also the MO discussion -- [Are dagger categories truly evil?](https://mathoverflow.net/q/220032/447).

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

[[!redirects principle of isomorphism]]
[[!redirects principle of equivalence]]
[[!redirects principle of invariance]]
[[!redirects principle of covariance]]

[[!redirects evil]]
[[!redirects non-evil]]
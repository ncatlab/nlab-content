
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

In [[category theory]], a concept is (half-jokingly) said to be _evil_ if it involves equations between [[object|objects]], or more generally if it distinguishes between [[isomorphism|isomorphic]] objects.  More precisely:

* A property of categories is _non-evil_ if when it holds for a [[category]] $C$, it also holds for any category $C'$ that is [[equivalence of categories|equivalent]] to $C$.

* A property of functors is _non-evil_ if when it holds for a [[functor]] $F$, it also holds for any functor $F'$ that is [[natural isomorphism|naturally isomorphic]] to $F$.

By rigorously avoiding equations between objects, we can ensure that the properties we define are non-evil.  (This should be made more precise, to become a theorem in the [[foundations of mathematics]].)

The ideas here generalize in many directions.  For example not only properties, but also constructions involving categories and functors, can be evil or non-evil.  The idea also generalizes to $n$-categories and to objects, morphisms etc. [[internalization|internal]] to $n$-categories.


## Terminology

The terminology 'evil' was originally intended as a joke and has not been used in any published paper.  It arguably also puts the emphasis on the wrong place, since what matters is what is *not* evil.  Other possibilities which have been proposed are:

*  'kosher' in place of 'non-evil'.  One could then say 'treif' or 'treyf' instead of 'evil', but this word is less well-known so probably 'non-kosher' would be easier to understand.

*  An imprecise term suitable for motivation in serious papers is 'too strict' for 'evil', with 'sufficiently weak' for 'non-evil'.  But one would probably need to explain, at least the first time, *why* the concept being discussed is too strict.

*  A precise term for use in higher category theory is 'invariant under equivalence' (as the definition suggests).  One can make various versions of this, such as 'equivalence-invariant' or a portmanteau such as 'equinvariant'.  Of course, only properties are actually invariant; non-evil [[stuff, structure, property|structure]] must actually be *covariant*.  One might argue that simply saying 'covariant' for 'non-evil' has the correct meaning and connotations in all cases.

*  From the other side, instead of 'evil' one could say 'non-invariant' or 'unstable under equivalence' or 'equi-unstable'.

*  In discussions of [[foundations of mathematics]], a rough translation of 'non-evil' is 'definable in a [[type theory]] without [[identity types]] (or least only intensional identity types)', but that is not very concise.

*  Other proposed possibilities for 'evil' include 'precarious', 'unstable', 'fragile', 'private' (in the sense of private and public methods in computer science), 'dangerous', and 'risky'.


## Motivation

### From mathematical practice

...

>Draw an analogy with vector spaces (maybe just finite-dimensional ones?).  We can *use* a basis to study a vector space, but the basis is not *part of* the vector space.  Even if we use a foundation of mathematics in which the basis literally is part of the vector space (which arguably was the case for 18th-century linear algebra, which studied only Cartesian spaces; and is still the case today if we study finite-dimensional vector spaces using a foundational type theory with propositions as types, but probably this is too obscure), anything that we consider to be a property *of the vector space* should be independent of the basis.  We can make this precise by comparing the groupoids $Vect_\sim$ and $Vect_b$.

...


### From foundations and logic

In [[material set theory]] based on [[ZFC]], any two objects are [[pure sets]] and can be compared for [[equality]].  Yet this is often mathematical nonsense which depends on precisely how one writes definitions; for example, the [[ordered pair]] $(0,0)$ is equal to the [[natural number]] $1$ by some standards and equal to $2$ by other standards (while $(1,1) = 2$ by yet other standards), but this makes no difference mathematically.  In contrast, [[structural set theory]] either implicitly (as in [[ETCS]]) or explicitly (as in [[SEAR]]) considers only equality between [[elements]] of a given [[set]] (or [[functions]] or [[binary relations]] between two given sets, etc).  This can be built into the [[logic]] using [[dependent type theory]] (which can serve as a foundation all by itself).

Does it make sense, then, to ask whether two arbitrary *sets* are equal?  In material set theory, of course it does; two sets are equal if they have the same elements (by the [[axiom of extensionality]]).  But structurally, this definition is meaningless.  All the same, a structural set theory built on [[first-order logic]] with equality automatically gives this question (whether two arbitrary sets are equal) a meaning, as do the most common forms of foundational type theory, but this is again never used in mathematics.  ($SEAR$, which is based on first-order logic without equality, does not give this question a meaning and does not suffer for it.)  So just as we don\'t need to ask whether $(0,0) = 2$, we don\'t need to ask whether $\{(0,0)\} = \{2\}$ as sets.  (Note that this a completely different question, structurally, from whether, say, $\{(0,0)\} = \{(0,1)\}$ as *[[subsets]]* of $\mathbb{N} \times \mathbb{N}$.)

Now let us move from the foundations of [[set theory]] to those of [[category theory]].  Usually, category theory is founded on set theory, or something very much like it; if the [[objects]] of a category don\'t form a set, then this is only because of [[size issues]], and they still form a [[proper class]].  Accordingly, it makes sense to compare them for equality.  However, if the [[category of sets]] is itself an example of a category, then by the previous paragraph, it does *not* have to make sense (and is mathematically meaningless) to test the objects of this category for equality.  So we get the idea that we cannot compare objects of a given category for equality in general (although this may make sense for particular categories).  In other words, a [[category]] is not by default a [[strict category]] (a category equipped with the [[extra stuff]] of an explicit equality predicate on its objects).

We can found mathematics on type theory without identity types, and then it is literally true that (in general) it makes no sense to compare objects of a given type for equality; one has to *define* a relevant equality predicate when there is one.  However, this is not a commonly used foundation.  Therefore, category theory is usually written in a language in which it does literally make sense to ask whether two objects of a given category are equal, whether two functors between two given categories are equal, etc.  If we want these definitions to make sense in the general mathematical situation (where $Set$ is an example of a category, even though comparing two arbitrary sets for equality makes no mathematical sense), then we need to check that our definitions are not evil.


## How to be evil

> Or: just because it looks evil doesn\'t mean that it really is

Just as we can make use of [[basis|bases]] in [[linear algebra]], so we may make use of [[strict categories]] to discuss [[category theory]].  Philosophically, the concept of strict category is not in itself evil; what is evil is to say that $Set$ (and other well-known categories such as [[Grp]], etc) are strict categories.  Mathematically, strict categories form a $1$-[[1-groupoid|groupoid]] $Str Cat_\sim$ that is different from the $2$-[[2-groupoid|groupoid]] $Cat_\sim$, but there is still a canonical [[pseudo functor]] from $Str Cat_\sim$ to $Cat_\sim$ that we may find useful.

Much as the [[axiom of choice]] tells us that every vector space has a basis, so the global axiom of choice tells us that every category may be given the structure of a strict category.  Then we can use this extra structure (in either case), as long as we prove that the result is independent of the structure chosen.  Even if we don\'t wish to accept the axiom of choice, we can still prove a theorem about those vector spaces that have bases or those categories that can be given a strict structure.

Perhaps the extreme case of this is using [[model categories]] to study [[homotopy theory]], which is (from the [[nPOV]]) really about $(\infty,1)$-[[(infinity,1)-category|categories]].  Even if model categories are not taken to be strict categories, they still form a $2$-groupoid and thus are still far more strict than $(\infty,1)$-categories, which form an $\infty$-[[infinity-groupoid|groupoid]].  Nevertheless, they are quite useful (at least assuming the axiom of choice?).


## Criticism

Periodically, there is discussion on the [categories mailing list](http://www.mta.ca/~cat-dist/) about the concept, including objections to the term 'evil'. Please refer there for further details.

## General definition

If $X$ is an $\infty$-[[infinity-groupoid|groupoid]], then a property $P$ of objects of $X$ is __non-evil__ if, whenever $P(a)$ holds for an object $a$ of $X$ and $b$ is [[equivalence|equivalent]] (as an object of $X$) to $a$, then $P(b)$ holds. Alternatively, an operation $f$ from objects of $X$ to objects of (another $\infty$-groupoid) $Y$ is __non-evil__ if, whenever $a$ and $b$ are equivalent objects of $X$, $f(a)$ and $f(b)$ are equivalent (as objects of $Y$).

(Note that everything is an object of some $\infty$-groupoid. For example, a $2$-morphism in some random $5$-category is an object of a hom-$3$-category, which has an [[core|underlying]] $3$-groupoid, which is a special kind of $\infty$-groupoid. For some purposes, this $2$-morphism may instead need to be seen as an object in a $2$-arrow $5$-category, which has an underlying $\infty$-groupoid as well; exactly which $\infty$-groupoid is relevant depends on the [[context]]. Also note that we really do need $\infty$-groupoids here, rather than $\infty$-categories, since dualities are not evil.)

The operation-version of evil gives the property-version if you think of a property as an operation taking values in the $\infty$-groupoid (in fact a $0$-groupoid, or [[set]]) of [[truth value|truth values]]. (The property-version also gives the operation-version, although that is a little more involved.) An operation will be non-evil if it is given (as the object-operation) by a [[functor]] ('$\infty$-functor', if you prefer). A property is non-evil precisely iff it\'s a functor to the $\infty$-groupoid of truth values.

This definition should be the conclusion of a theorem that using certain language (including avoiding equations between objects of a category) makes it impossible to say anything evil. [[Michael Makkai]] works on such a language, [[FOLDS]] ('first-order logic with dependent sorts'), which does not include an axiomatic notion of [[equality]] at all. This pertains to the [[foundations|mathematical foundations of category theory]]. To learn more, see his paper _[First Order Logic with Dependent Sorts, with Applications to Category Theory](http://www.math.mcgill.ca/makkai/)_.


## Examples

The most common source of evil is a statement that two [[objects]] of a given category are [[equality|equal]].  One should instead say that they are [[isomorphism|isomorphic]] and then (usually) impose some [[coherence relation]] on the relevant family of isomorphisms.  But of course, this is more complicated!

It is not evil to state that two [[morphisms]] are equal, given a common [[source]] and [[target]]; this is because a [[hom-set]] is a [[set]], where equality is meaningful.  However, it is evil to state that two morphisms are equal if the source and target are *not* given, because this includes the claim that their sources (which are objects) are equal, and similarly for the targets.

It is evil to state that two morphisms in a $2$-[[2-category|category]] are equal, because these morphisms are objects in a [[hom-category]], but it\'s not evil to state that that two $2$-moprhisms are equal, given a common source and target.  And so on.  In an $\infty$-[[infinity-category|category]], *every* claim of equality is evil.

Defining higher categorial structures using such evil equalities tends to lead to *strict* concepts; avoiding them and imposing coherence relations leads to *weak* concepts.  Sometimes there is a [[coherence theorem]] showing that every weak concept can be strictified, which justifies using equality as a figure of speech.  See [[Gray-category]] and [[model category]] for examples of this in action.


### Evil in quantum theory {#daggers}

The concept of [[dagger-category|†-category]] is important in [[topological quantum field theory]] and [[quantum computation]].  A **[[†-category]]** is a category $C$ with a functor

$$F: C \to C^{op} $$

which is the identity on objects and has $F^2 = 1$.  

This definition is evil: it imposes equations between objects, so we cannot transport a dagger-category structure along an equivalence of categories.
Often evil concepts (like the concept of "strict monoidal category") have non-evil counterparts (like the concept of "monoidal category").  But in this particular case there appears to be no known way to express the idea without equations between objects.  Both [[Hilb]] and [[nCob]] are dagger-categories.  This fact is important.  Try saying it in a non-evil way!  

It is possible that this problem will force a change in thinking in either the concept of evil or our thinking in quantum theory.

+--{: .query}
[[Mike Shulman]]: Actually, I believe that $\dagger$-structure on a category *can* be transported along an equivalence of categories!  Suppose that $F\colon C \to D \colon G$ is an [[adjoint equivalence]] with unit $\eta\colon Id_C \overset{\cong}{\to} G F$ and counit $\varepsilon\colon F G \overset{\cong}{\to} Id_D$, where $D$ is a $\dagger$-category.  Given $f\colon x\to y$ in $C$, define $f^\dagger$ to be the following composite:
$$ y \overset{\eta}{\to} G F y \overset{G((F f)^\dagger)}{\to} G F x \overset{\eta^{-1}}{\to} x. $$
This evidently defines a functor $C^{op} \to C$ that is the identity on objects.  Now $F(f^\dagger)$ is given by
$$ F y \overset{F \eta}{\to} F G F y \overset{F G((F f)^\dagger)}{\to} F G F x \overset{F \eta^{-1}}{\to} F x $$
but by the triangle identities this is equal to
$$ F y \overset{\varepsilon^{-1}_F}{\to} F G F y \overset{F G((F f)^\dagger)}{\to} F G F x \overset{\varepsilon_F}{\to} F x $$
and hence equal to $(F f)^\dagger$ by naturality of $\varepsilon$.  Thus, since $((F f)^\dagger)^\dagger = F f$ in $D$, in $C$ we have that $(f^\dagger)^\dagger$ is given by
$$ x \overset{\eta}{\to} G F x \overset{G F f}{\to} G F y \overset{\eta^{-1}}{\to} y. $$
which is equal to $f$ by naturality of $\eta$.  Thus, $C$ is a $\dagger$-category, and essentially by construction $F$ and $G$ are $\dagger$-functors (though $\eta$ and $\varepsilon$ need not be unitary).

So if a notion refers to equality of objects in a seemingly irreducible way, but it can nevertheless be transported along an equivalence of categories, is it evil or isn't it?  Thinking about it some more, I'm actually not convinced that $\dagger$-structure is evil at all.  Consider the assertion that a category is a groupoid.  Clearly this is not evil!  But what it means is that for any morphism $f\colon x\to y$, there exists a morphism $f^{-1}\colon y\to x$ whose source is *equal* to the target of $f$, and whose target is *equal* to the source of $f$, and such that $f f^{-1}$ and $f^{-1} f$ are identities.  The notion of $\dagger$-category is entirely analogous: for any morphism $f\colon x\to y$, we are given a specified morphism $f^\dagger\colon y\to x$ with certain properties.  The only difference is that the first is a *property* and the second is *structure*, but why should that matter?

As remarked in the discussion below, equality of objects is all over the place in category theory: whenever we introduce an arrow, we have to say what its source and target are, and one or the other (or both) will often be *equal* to some object we are already considering.  But this is not really evil; it's really just a *typing assertion*.  (If you write category theory in a logic of [[dependent types]] like [[FOLDS]], then that's exactly what it is.)  Maybe $\dagger$-structure is just the same.

[[Mike Shulman]]: Here's an interesting analogy: let $G$ be a group and consider categories enriched over $G$-sets.  In such a category, for every morphism $f\colon x\to y$ and every $g\in G$ we have another morphism $f^g\colon x\to y$ satisfying certain axioms, which may look evil (since $f^g$ has equal source and target to $f$) but is really not.  Moreover, just like for $\dagger$-categories and unitary isomorphisms, in this case the "underlying groupoid" is not the naive core of the original category, but consists of only the $G$-fixed isomorphisms.  Actually, $\dagger$-categories have always felt a lot like enriched categories to me, though the "enrichment" is sort of "non-local" in that the structure on homsets relates more than one of them, so it's hard to make this precise.

_Toby_:  I agree, the concept is not really evil, although you have clarified the ideas for me, so that now I think that I can write a good note to the mailing list.  (In particular, the idea that a dagger structure is analogous to the property of being a groupoid, only slightly harder to grok since it is not a property-like structure, was helpful.)

If you specify a functor $\dagger\colon C^{op} \to C$ and ask whether it is a dagger structure, that is (taken literally) an evil question; you can ask instead whether it is naturall isomorphic to a dagger structure.  But the concept of dagger structure is not itself evil, if broken down a little.

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


## Discussion

There's been a lot of discussion of this on the $n$-Category Caf&#233; --- someone find it and cite it!


+-- {: .query}
Comment: It seems that at some level you can't avoid equality, at least if you want to completely formalise things (say, in a proof assistant). For example, in the definition of "category" itself (on which the definitions of isomorphism and $\infty$-groupoid seem to depend), we say that $g \circ f$ is defined iff $\dom g = \cod f$.

Now if you start your theorem with "let $a,b,c$ be objects of $C$ and let $g : b \to c$,$f: a \to b$ be morphisms", then there's no problem. But what if you need to compose morphisms whose dom/cod aren't definitionally/syntactically equal? I suppose that at this point it depends on which foundations you use.

Reply:  Yes, it can depend on the foundations.  [[FOLDS]] is a foundation specifically designed to avoid evil, and higher category theory has been formulated in it (by [[Michael Makkai]], who invented both FOLDS and a multitopic definition of higher categories to go with it).  More generally, the style of terminology that you gave comes naturally to a development of (higher) category theory in a foundation based on dependent [[type theory]].

Even in your first example, the quesion of whether we can compose $g \circ f$, we can avoid evil if we try.  Na&#239;vely, we can compose them if and only if $\dom g = \cod f$; composability is a property of the pair ---but an evil property.  Less evilly, we make composability a *structure* on the pair; we can compose them along any isomorphism between $\dom g$ and $\cod f$.  So as usual in category theory, we don\'t ask whether these objects are equal but instead how they might be isomorphic.

Of course, if $f$ and $g$ are given as $g: b \to c$ and $f: a \to b$, then we can compose them along the identity morphism of $b$; this is the usual notion of compoisition in that case.  It is only when $f$ and $g$ are not given to us in such a way that we have to talk about composing along an arbitrary (possibly nonexistent, certainly not likely to exist uniquely) isomorphism.

Can you say everything that you want to say about (higher) categories while avoiding evil throughout?  That will always be an open question, as people think of new things to say about them.  But I think that it is a fruiful attitude to take that one should try.  ---[[Toby Bartels]]

[[Mike Shulman]]: I'm not convinced by "composing along isomorphisms," because what does it mean for an isomorphism $h$ to be "between" $\dom g$ and $\cod f$?  It means that $\dom h = \cod f$ and $\cod h = \dom g$.

_Toby_:  But <del>you</del><ins>the Anonymous Coward</ins> already told us how to phrase things above: "let $a,b,c$ be objects of $C$ and let $g : b \to c$,$f: a \to b$ be morphisms".  So now we take a case where $dom g$ and $cod f$ are not definitionally/syntactically equal, as so:
> Let $a,b,c,d$ be objects and let $g: c \to d,\; f: a \to b$ be morphisms.
Then we can form the composite $g \circ f$ relative to any isomophism $h: b \to c$.  (Of course, the notation $g \circ f$ suppresses $h$, so it\'s more proper to write $g \circ_h f$, or just $g \circ h \circ f$ as a normal person would.)

Note that the definability of $g \circ f$ is now the set $Iso(b,c)$ rather than the truth value $b = c$.  In an $\infty$-category, it would be an $\infty$-groupoid $Iso(b,c)$.

[[Mike Shulman]]: That wasn't me above, I don't think.  I would consider "let $g : b \to c$ and $f: a \to b$ be morphisms" as implicitly using dependent types if you're considering it to avoid evil.  It seems to me that in a non-dependently typed theory, the only thing "let $g : b \to c$ and $f: a \to b$ be morphisms" can mean is "let $g$ and $f$ be morphisms such that $\dom f = a$, $\cod f = b$, $\dom g = b$, and $\cod g=c$," which does involve talking about equality of objects.

_Toby_:  Right on both counts: that was an [[Anonymous Coward]] in the first comment, and the phrasing that the Coward suggested does implicitly use dependent types (as I alluded to in my original reply).  Makkai says 'dependent sorts' (the 'DS' in 'FOLDS') instead for some reason.  Can we avoid evil in an independently typed (possibly even untyped) language?  I think that this should be possible; we would need rules about when you can and can\'t state equalities; maybe, you can state $\forall f, dom f = x \Rightarrow ...$ and the obvious variations, but no others?

[[Mike Shulman]]: In other words, you can secretly make your independent types act like dependent ones?  (-:

_Toby_:  Yeah, a dependent type theory can always be rephrased as an independent type theory, although you have to use equality to do this; this is equivalent to the original dependent type theory if (as is the common practice) that theory also had equality predicates, but otherwise it\'s stonger.  Similarly, a typed theory can be rephrased as an untyped theory, although you have to use typing predicates to do this, and again this is stronger.  Conversely, we know (well, some people know) how to limit the use of the typing predicates in the untyped theory to make it equivalent to the typed theory.  Now I think that there also ought to be rules to limit the use of equality in a simple type theory to make it equivalent to a dependent type theory *without* equality.

[[Mike Shulman]]: Amazingly enough, as you said at latest changes, this conversation does seem to be leading in the direction of actual mathematics.  It does seem like that should be possible, but I don't have the time to think about it any more deeply now.  Aside from pointing out the obvious fact that until we get to $\omega$-categories, we do want to allow equality relations on *some* of the types in the dependent type theory.

_Toby_:  I also don\'t have the time to think about it carefully; I feel pretty secure about my intuition, but that is all.  But I would see the equality relation between parallel $n$-morphisms in an $n$-category as something extralogical, just as much as the type of $n$-morphisms between parallel $(n-1)$-morphisms.

_Harry_: Couldn't we just say: Let $f$ and $g$ be (left? right?)-composable iff $h[dom g]$ is isomorphic to $h[cod f]$ where $h$ is the homotopy category functor (assuming quasicategories, but there should be a good enough way to define this in more generality, no?).  This way, $g \circ f$ is only specified up to homotopy (that is, we know that it's in the homotopy class of $h[g] \circ h[f]$.  I think there might be a few technicalities to work out with 1-Categories, but applying the homotopy functor immediately collapses it to that case.  

_Toby_:  That seems to bring us back to the idea of composing along an isomorphism between $dom g$ and $cod f$, now generalised to quasicategories.

[[Mike Shulman]]: Yes, if you only know that $h[dom g]$ is isomorphic to $h[cod f]$, you still need to *choose* an isomorphism along which to compose $f$ and $g$.  Different choices will give you different "composites".

_Harry_: Can two wrongs (or evils in this case) make a right?  Maybe we can solve the composition problem by passing to the skeleton of the homotopy category?

[[Mike Shulman]]: I think the short answer is "no."  Choosing a skeleton (together with an equivalence to the category one started with, naturally) involves choosing a bunch of specified isomorphisms between isomorphic objects, so really you aren't doing anything different.

[[JCMcKeown]]: Non-sequitur; perhaps it's helpful to try remembering why evil concepts propagate? E.g., "the standard" basis of $\mathbf{k}^n$ doesn't exist as intrinsic to any vector space $\mathbf{k}^n$, but it's implicit in any biproduct diagram for $\mathbf{k}^n$ over $n$ copies of $\mathbf{k}$.  That is, sometimes we want to pretend that some anafunctor is actually a functor --- or that a contractible object is literally terminal --- and once we're comfortable dropping this crutch, we try to relax things and see what's still sensible.  But surely it's not evil to say that $\id_C(A)=A$?  It's not really a statement about *two things*, anyways.  Checking the evilness of this would only lead you to ask "&iquest;$\id_C(A)=B$?" for $A,B$ *equivalent* if you *don't know* that we're looking at a diagonal, where we only ask $\id_C(A)=B$ for $A=B$. --JCM

_Toby_:  In some languages (I am thinking of Coquand-style type theory without identity predicates, but it probably appears elsewhere), it is sometimes necessary to form identity *judgements*.  For example, we may need to be able to know that $\pi(a,b)$ and $a$ are the exact same thing (and other identities given by $\beta$-[[beta-rule|rules]]).  However, we still don\'t want any identity *propositions*.  So given a category $C$ and an object $A$ of $C$, it may well be possible to state, as a judgement of a true fact that we can prove, that $\id_C(A)$ and $A$ are identical; certainly it would be if part of the definition of $\id_C$ is that it acts on objects as $\lambda X. X$ (and we have $\beta$-rule judgements as I suggested above).  However, it should never be necessary to treat the statement that they are identical as a proposition, and indeed we would never want (given additionally an object $B$ of $C$) to treat the statement that $\id_C(A)$ and $B$ are identical as a propostion.

But in other languages, such as FOLDS, even this sort of thing would never come up.  In that language, $\id_C(A)$ is not a term for an object of $C$ at all.  The best that you can do is invoke the existential property of the identity anafunctor to know that there is an object $X$ of $A$ such that $X$ is *a* value of $\id_C$ at $A$, then declare that you will denote $X$ by $\id_C(A)$ from now on.  (One should be able to formalise this abuse of language so as to make ordinary mathematical vernacular sensible, but I\'m not sure how to do it.)
=--


[[!redirects evil]]
[[!redirects non-evil]]


# Strict categories
* table of contents
{: toc}

## Idea

A __strict category__ is a [[category]] together with the structure of a [[set]] (or [[class]]) on its collection of objects---and in particular, come with a notion of [[equality]] (not merely [[isomorphism]]).  In contrast, a __weak category__ is a category *without* such structure.  Similarly, a __strict functor__ is one which preserves equality of objects: $F(x) = F(y)$ if $x = y$.  (NB: this is not size-related---both [[large category|large]] and [[small categories]] can be either strict or weak.)

If we use [[set theory|set-theoretic]] [[foundations]] for category theory, then by definition, a category comes with a set (or class) of objects, and therefore admits the structure of a strict category in a canonical way.  Thus, in this case, it is possible to ignore the adjective "strict" in "strict category", while a "strict functor" basically means a "non-[[anafunctor|ana]] functor" (the usual default, but not necessarily the best concept).

If we additionally assume the (possibly global) [[axiom of choice]], then any strict category is equivalent to a canonical one, and every (ana-)functor is equivalent to a strict functor, so the notions have little to no mathematical content.  But in other foundations, these facts may not be true.

Moreover, even in set-theoretic foundations with AC, the notion of strict category is not meaningless: calling a category strict signals that we intend to *make use of* the fact that its objects form a set.  When taking the [[nPOV]], we often adopt the [[philosophy|philosophical]] position that [[category theory]] is fundamentally about weak categories; see for instance [[evil]].  However, strict categories do occasionally arise in mathematical practice; see for instance [[M-category]].


## Definition

In order to formulate a foundation-independent definition, we make the following assumptions.  Ignoring [[size issues]], suppose that we have a [[bicategory]] $Cat$ consisting of weak [[categories]], [[functors]] (some of which are [[essentially surjective functor|essentially surjective]]), and [[natural transformations]] (some of which are [[natural isomorphisms]]).  Suppose also that we have a [[category]] $Set$ consisting of [[sets]] and [[functions]], and a [[functor]] $Disc\colon Set \to \Cat$ taking each set to the [[discrete category]] on that set.  Note that we do not assume the existence of an "underlying set of objects" functor $Cat\to Set$.

In this context, a __strict category__ $C$ consists of

* a set $Ob(C)$ (to be thought of as the set of [[objects]] of $C$),
* a category $Wk(C)$ (to be thought of as the underlying weak category of $C$), and
* an essentially surjective functor $cl(C)\colon Disc(Ob(C)) \to C$ (to be thought of as taking each object of $C$ to its [[clique]] in $C$).

A __strict functor__ $F$ from $C$ to $D$ (both strict categories) consists of

* a function $Ob(F)\colon Ob(C) \to Ob(D)$,
* a functor $Wk(F)\colon Wk(C) \to Wk(D)$, and
* a natural isomorphism $cl(F)\colon cl(C) ; Wk(F) \to Disc(Ob(F)) ; cl(D)$.

Two strict functors $F, G\colon C \to D$ are __equal__ if

* $Ob(F) = Ob(G)$ and
* there is a (necessarily unique) natural isomorphism from $Wk(F)$ to $Wk(G)$ modulo which $cl(F)$ equals $cl(G)$.

There is an obvious notion of [[composition]] that defines a [[1-category]] $Str Cat$ of strict categories and (equality classes of) strict functors.  Note that this 1-category has a strictly associative and unital composition law, even if $Cat$ is only a [[bicategory]].  (However, $Str Cat$ is not *itself* a strict category, unless the assumed category $Set$ is strict.)  We have a [[forgetful functor]] $Ob\colon Str Cat \to Set$ and a [[pseudofunctor]] $Wk\colon Str Cat \to Cat$.

Finally, a __natural transformation__ between two strict functors $F$ and $G$ is simply

* a natural transformation from $Wk(F)$ to $Wk(G)$.

(That is, a [[natural transformation]] between strict functors is automatically strict.)  With these as 2-cells, we have a [[strict 2-category]] of strict categories, strict functors, and natural transformations.

+-- {: .un_remark}
###### Remark
An equivalent definition is that a strict category is an $\mathcal{M}$-[[M-category|category]] whose underlying category of tight morphisms is discrete, while a strict functor is an $\mathcal{M}$-functor.  In this case, the tight morphisms (which are necessarily [[isomorphisms]]) are sometimes called **special isomorphisms**.
=--


## Foundational choices

We now make the above schematic definition explicit in terms of various different foundational systems.


### Set theory with AC

In [[classical mathematics|classical]] [[set theory|set-theoretic]] foundations including the [[axiom of choice]], we take $Cat$ to be the [[strict 2-category]] consisting of [[categories]], [[functors]], and [[natural transformations]], defined in any of the traditional ways.  The functor $Disc \colon Set\to Cat$ is [[left adjoint]] to the functor $Ob\colon Cat\to Set$, and thus $Str Cat$ is a subcategory of the [[Freyd cover]] of $Cat$.

In this case, the functor $Wk\colon Str Cat \to Cat$ has a [[right adjoint]] which takes a category $C$ to the strict category $Disc(Ob(C)) \to C$.  The adjunction counit is literally the identity, while the adjunction unit consists of [[equivalences]] (but not isomorphisms) in the strict 2-category $Str Cat$.  Thus, $Str Cat$ is equivalent to $Cat$ (as a bicategory).

The right adjoint $Cat \to Str Cat$ also has a further right adjoint defined as follows: given a strict category $C$, let $C'$ be the category with $Ob(C)$ as its set of objects, and morphisms induced from those in $Wk(C)$.  The unit of this adjunction again consists of identities, while the counit consists of equivalences in $Str Cat$.

This analysis applies not only to [[material set theories]] such as [[ZFC]], but also [[structural set theories]] such as [[ETCS]] and [[SEAR]], as long as they have the axiom of choice.


### Set theory without AC

In this case, it is usually best to define [[Cat]] to be the bicategory of categories, [[anafunctors]], and natural transformations.  Now although every category has an underlying set of objects, we no longer have a functor $Ob\colon Cat \to Set$.  It is still true that every category $C$ admits the structure of a strict category in a canonical way (with $Ob(C)$ its set of objects), but not every strict category necessarily arises in this way, and not every morphism $C\to D$ in $Cat$ (i.e. anafunctor) is a strict functor relative to the canonical strict-category structures of $C$ and $D$.  In fact, an anafunctor is a strict functor precisely when it is naturally isomorphic to an ordinary (non-ana) functor.

If we instead defined $Cat$ to consist of non-ana functors, then everything would happen exactly as with AC, except that neither adjunction would be an equivalence.


### Type and preset theories with equality

We include under this heading all theories in which the basic objects, generally called [[type theory|types]] or [[presets]], come with an [[equality]] [[relation]], but the notion of [[set]] is a defined one.  Generally, the issue is that types (or presets) do not admit [[quotient object|quotients]], and so a **set** is defined to be a type equipped with an [[equivalence relation]] called "equality" (sometimes called a [[setoid]] in this context).

In this case, it is natural to define a *category* to have only a type/preset of objects, but a set(oid) of morphisms between each pair of objects.  See [[type-theoretic definition of category]].  Now every category still has an underlying set of objects, but not every set is the set of objects underlying any category (only the [[completely presented sets]] have this property).

Again, it is true that every category can be made into a strict one in a canonical way, but that not every strict category arises in this way.  This is a different sort of failure than in the previous case, and can happen even in the presence of AC.  For instance, consider the [[discrete category]] on the set of [[real numbers]].  Of course this depends on specifics, but typically, there is no type of real numbers per se but only a type of Cauchy (pre)sequences of rational numbers (see [[Cauchy real number]]).  To get the set of real numbers, we must consider this type together with a certain equivalence relation, a setoid.  The discrete category on the set of real numbers is essentially the exact same construction, now with a note that parallel morphisms are always defined to be equal.  The automatic notion of equality on the objects of this category is equality of Cauchy (pre)sequences, but the desired notion of equality for this discrete category as a strict category is isomorphism, which is equality of real numbers.  So while this category may be automatically a strict category, it is a strict category in the wrong way.

Note that we still have a functor $Disc\colon Set \to Cat$ which regards an equivalence relation on a type $A$ as a groupoid with $A$ as its type of objects.  The resulting structure of strict categories behaves much like it does in set theory without AC.

+--{: .query}
[[Mike Shulman]]: I don't understand the following paragraph; see [nForum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=3413).
=--

Furthermore, just because there is a notion of equality of objects, we might not really have a strict category unless this notion behaves as [[equality]] ought.  In particular, if $a$ and $b$ are equal objects, then they ought to be [[isomorphic]] as well.  (In terms of the formal definition of strict category, this goes into the action of the functor $cl$ on morphisms.)  In [[set theory]] and [[extensional type theory]], we have this; the [[identity morphism]] $\id_a\colon a \to a$ is isomorphism $\id_a\colon a \to b$, since after all $a = b$.  But in [[intensional type theory]] (even with identity types), we are not necessarily allowed to switch the type of $\id_a$ from $a \to a$ to $a \to b$ like this.


### Type and preset theories without equality

If types or presets do not come with a notion of equality, as in some preset theories and [[SEAR+?]], then a category does not in general even *have* an "underlying set of objects".  But defining sets as presets with equivalence relations as before, we still have $Disc\colon Set \to Cat$, and we can define strict categories.


### Homotopy type theory

If [[intensional type theory]] is treated as a theory of set-like objects, then it behaves much like extensional type theory with equality, above.  However, if we take the point of view of [[homotopy type theory]], then the basic objects of the theory are [[homotopy types]], a.k.a. [[∞-groupoids]].  A *set* is now defined to be an [[h-set]], i.e. a [[truncated object|0-truncated]] type.

Now the natural definition of (1-)category is something like a [[complete Segal space]], where the type of objects is 1-truncated (a [[groupoid]]) and equivalent to the [[core]] of the category.  Once again, not every category has any underlying set of objects, but we still have $Disc\colon Set \to Cat$ and we can define strict categories.


## Strict higher categories

The notion of strict category is related to the notion of strictness in [[higher category theory]].

For instance, a [[2-category]] must have strict categories as its [[hom-categories]] in order to write down the definition of [[strict 2-category]]; a similar remark holds for [[strict 2-functors]].  As such, strictness in the sense of this page matches and extends strictness in the usual sense of [[higher category theory]] in a "local" sence (every strict 2-category is locally a strict 1-category).  However, we now get a notion of __strict $2$-natural transformation__ as a [[2-natural transformation]] that preserves equality (that is, if two objects are equal, then so are the corresponding components of the natural transformation).  (All [[modifications]] between strict transformations are automatically strict ... until we get to $3$-categories, of course!)

On the other hand, the underlying 1-category of a [[strict 2-category]] (its objects and 1-morphisms) need not be a strict 1-category.  For instance, this is the case for the strict 2-category $Str Cat$ defined in a structural set theory such as [[SEAR]], in which there is no equality predicate on sets.


[[!redirects strict category]]
[[!redirects strict categories]]
[[!redirects strict functor]]
[[!redirects strict functors]]
[[!redirects strict groupoid]]
[[!redirects strict groupoids]]
[[!redirects StrCat]]
[[!redirects Str Cat]]

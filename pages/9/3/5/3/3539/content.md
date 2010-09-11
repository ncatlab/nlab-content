
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* tic
{: toc}

## Idea ##

Generally, a **coherence theorem** in [[category theory]] and [[higher category theory]] asserts that a [[coherence law]] is satisfied: it is a means of getting a handle on categorical structures where laws only hold up to [[isomorphism]] or higher [[k-morphism]] equivalences.  Precisely, it can mean one of several slightly different things.

### Descriptions of free algebras

Given a [[doctrine]], such as the doctrine for monoidal categories, a coherence theorem may provide a full or partial algorithm for deciding equality in free algebras.  Usually such a doctrine is specified only by certain "generating" operations and constraint morphisms between them; the coherence question then consists in determining exactly what additional operations and morphisms are derivable from these, and in particular when two such derived morphisms are equal.  For instance, one may be interested in the coherence problem for closed categories: how does one decide equality of morphisms in freely generated closed categories, or in other words, how does one decide which diagrams (generated from the closed structure) commute?

The first, and perhaps easiest, coherence theorem is Mac Lane's, which says that in a free [[monoidal category]], *every* diagram of constraint morphisms commutes.  The especially nice form of this theorem should not lead one to expect that all coherence theorems are of the form "every diagram commutes"---in many categorical structures, it is *not* the case that all diagrams of constraints commute, and so the coherence question must address more precisely *which* diagrams of constraints commute.  For instance, in a [[braided monoidal category]] not every diagram of constraints commutes, but the coherence theorem gives a concise classification of those that do in terms of their underlying braids.

This sort of coherence theorem is often the most useful when actually working with algebras in a doctrine, since it provides a way to tell whether two particular composites of constraints which may arise in practice are actually equal.  One should beware, however, that coherence theorems only relate to the behavior of *free* algebras, or equivalently to the equality of *formally defined* composites.  Even in a structure having a coherence theorem of the "every diagram commutes" sort, it may happen in a *particular* algebra that there exist diagrams of constraints which do not commute.  For instance, one can find a monoidal category containing objects $x,y,z$ such that $x\otimes (y\otimes z) = (x\otimes y)\otimes z$ on the nose, but such that the [[associator]] isomorphism $a_{x,y,z}:x\otimes (y\otimes z) \stackrel{\simeq}{\to} (x\otimes y)\otimes z$ is not the identity.  (For example, [[skeletons]] of naturally occurring monoidal categories often have this property.  This issue also arises in the classification of [[2-groups]] via cohomology.)

### Strictification

On the other hand, given a doctrine for "weak" categorical structures of some sort, a coherence theorem may provide a means for fully or partially strictifying such structures, to the effect that every weak structure is weakly equivalent to a strictified structure.  The applicable version of Mac Lane's original coherence theorem here is that every monoidal category is (monoidally) equivalent to a *strict* monoidal category.  Similarly, every [[bicategory]] is equivalent to a [[strict 2-category]].

As before, one should not be misled by these examples into thinking that all coherence theorems are of the form "every weak thing is equivalent to a strict thing."  For example, the strictification coherence theorem for symmetric monoidal categories states that every symmetric monoidal category is symmetric-monoidally equivalent, not to a commutative monoid in $Cat$, but to a symmetric strict monoidal category, whose monoidal structure is strict but whose symmetry is not.  This may be regarded as a "partial" or "semi-"strictification result.

Naturally, it should not be thought that coherence problems are restricted to 1-category theory.  For instance, the main result in Gordon, Power and Street's _Coherence for Tricategories_ is that every [[tricategory]] is equivalent (not to a [[strict 3-category]] but) to a [[Gray-category]].  This is another example of a semi-strictification result, and is the tip of an iceberg of hoped-for further coherence theorems for algebraic notions of $n$-category.

### Relating coherence theorems

These two senses of "coherence theorem" are connected, of course.  On the one hand, an explicit description of the free algebras for a doctrine is often helpful, if not essential, in proving a strictification result, since in a strict structure where constraints become equalities, many more diagrams will turn out to commute (being composed of identities).  On the other hand, given a strictification theorem, if we have an explicit description of the strict structure (which is generally easier to come by), we can often deduce a characterization of the free algebras for the weak structure.

One thing to beware of is that even for structures whose free-algebra coherence theorem is of the form "all diagrams commute," it does not necessarily follow that all such algebras can be fully strictified.


## List of coherence theorems

+--{: .query}
I think it would be nice to have pages about all the different coherence theorems, with links to them all from here.
=--

* [[coherence theorem for monoidal categories]]
* [[coherence theorem for symmetric monoidal categories]]
* [[coherence theorem for braided monoidal categories]]
* [[coherence theorem for tortile categories]]
* [[coherence theorem for closed symmetric monoidal categories]]
* [[coherence theorem for bicategories]]
* [[coherence theorem for tricategories]]


## General frameworks for coherence theorems

There exist several general frameworks for describing "doctrines" or algebraic structures on categories, which can be used to describe free algebras and state coherence theorems.  All are closely related.

### 2-monads {#2monads}

A [[2-monad]] can be regarded as the "extensional essence" of an algebraic structure on categories (or on objects of some other 2-category).  Of course, if $T$ is a 2-monad describing some structure, then $T A$ is the free such structure on $A$; thus the first sort of coherence theorem can be precisely stated as "describe $T A$ as explicitly as possible in terms of $A$."

However, the notion of monad is so general that in practice, for proving coherence theorems it is useful to have a more explicit way of "presenting" a monad in terms of generating operations and relations; this is the purpose of the structures presented below, such as [[operads]] and [[clubs]].  Not all monads can be presented in such a more explicit way, but for those that can, it is a very useful simplification.

The notion of *strict* 2-monad on a [[strict 2-category]] also provides a general way to state a strictification theorem, although one must beware that this theorem is not always true, and when it is true, it doesn't necessarily give what one was looking for.  This general "coherence theorem schema" for a 2-monad $T$ would be that every [[pseudoalgebra for a 2-monad|pseudo]] $T$-algebra is equivalent to a strict one.  A stronger statement, which is true in most cases when the weaker version is, would be that the inclusion
$$ Str T Alg \hookrightarrow Ps T Alg $$
of the 2-category of strict $T$-algebras and strict $T$-morphisms into the 2-category of pseudo $T$-algebras and pseudo $T$-morphisms has a strict left 2-adjoint, usually written $(-)'$, and moreover for a pseudo algebra $A$, the unit $A \to A'$ is an [[equivalence]] in $Ps T Alg$.  Thus $A$ is not only equivalent to a strict $T$-algebra, it is equivalent to a canonically defined one which is characterized by a universal property.

This "coherence theorem" is true in a lot of generality, although there are 2-monads for which it fails.  However, often it leaves a lot of work to be done in order to extract what is commonly thought of as a coherence theorem.  This is because the notion of pseudo $T$-algebra is always an *unbiased* weak structure, whereas it is more usual to study biased structures.  Moreover, in most cases, proving an equivalence between biased and unbiased notions requires the full strength of the coherence theorem (in the description-of-free-algebras sense) for the biased notion!


### Operads

See [[operad]].


### Clubs ## 

See [[club]].

+--{: .query}
[[Mike Shulman]]: I would be wary of putting too much focus on clubs here.  There are lots of ways to present solutions to the first sort of coherence problem, corresponding to all the different ways to describe general algebraic structures: monads, clubs, operads, multicategories, props, etc.  We can certainly have a page on [[club]]s that describes their applications to coherence theorems, but I'd rather have this page talk more generally about coherence theorems and have links to other pages about specific coherence theorems or general methods for proving them.
=--

## References

* Steve Lack, Codescent objects and coherence, [MR](http://www.ams.org/mathscinet-getitem?mr=1935980)

[[!redirects coherence theorems]]

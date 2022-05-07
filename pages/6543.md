
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Stack semantics
* table of contents
{:toc}

## Idea

The **stack semantics** is an extension of the [[internal logic]] of a [[category]] (or [[higher category]]) $C$ which allows us to talk about, and [[quantifier|quantify over]], *objects* of $C$.  (Such quantification is sometimes called "unbounded" quantification.)

In the ordinary internal language, an internal "element" of an object $A$ is interpreted into a [[generalized element]] $X\to A$ for some object $X\in C$, which consists intuitively of one "actual" element of $A$ for every element of $X$.  Similarly, in the stack semantics, an internal "object" is interpreted as a "generalized object" defined at some stage $X$, which we define to mean an object of the [[slice category]] $C/X$.  This makes sense because an object of $C/X$ consists intuitively of one "actual" object of $C$ for each "element" of $X$ (namely, the [[fiber]] over that element).

The stack semantics is so-called because in most categories $C$ where we consider it (such as [[toposes]] or [[pretoposes]]), the [[self-indexing]] is a [[stack]] for some naturally defined [[Grothendieck topology]] on $C$, and the stack semantics can be regarded as the ordinary internal logic of a higher topos of stacks on $C$ (see below).  Analogously, the ordinary internal logic is often called *sheaf semantics*, because in a [[subcanonical topology]] all [[representable functors]] are [[sheaves]], and because it can often be regarded as part of the internal logic of the topos of sheaves on $C$.


## Definition

### Direct description

...

### As internal logic

While on the one hand, the stack semantics *generalizes* the internal logic of a category, it can also be regarded as a special case thereof.

The basic idea of this is that if we have a chosen morphism $\widetilde{U}\to U$ in $C$, then generalized elements of $U$ at stage $X$ can be regarded as "names" for generalized *objects* of $C$ at stage $X$.  Namely, the generalized element $u\colon X\to U$ names the [[pullback]] of $\widetilde{U}\to U$ along $u$.

There are two issues with this idea, which can prevent it from faithfully representing the *idea* of the stack semantics sketched above.

The first issue is that a given "generalized object" over $X$ may have multiple names, whereas the stack semantics ought to speak directly about objects rather than about names for them.  Moreover, since $C/X$ is actually a category (or a higher category, if $C$ is such), generalized objects [[evil|should]] be considered "the same" only if they are [[isomorphism|isomorphic]] or [[equivalence|equivalent]], whereas morphisms $X\to U$ may admit a stricter notion of sameness.  In particular, when $C$ is a [[1-category]] (the classical case), the morphisms $X\to U$ form a *set*, whereas $C/X$ should be regarded as a category, or at worst as a [[groupoid]] (its [[core]]).

More generally, if $C$ is an [[n-category]] for some finite $n$, then $C(X,U)$ is only an $(n-1)$-category, whereas $C/X$ is also an $n$-category or at worst an [[n-groupoid]].  Thus, there is no hope of solving this problem *inside* of $C$ unless $C$ is at least an [[(∞,1)-category]].  In that case, the notion of [[object classifier in an (∞,1)-category]] does solve this problem: the $\infty$-groupoid $C(X,U)$ is equivalent to the core of (a suitable subcategory of) $C/X$.  (The presence of noninvertible morphisms in $C/X$ is not nearly so big a problem; at least when $C$ is an $(n,1)$-category, these can be described already in the ordinary internal logic if $C$ is [[locally cartesian closed category]].)

If $C$ is only an $(n,1)$-category for some finite $n$, however, then in order to obtain its stack semantics as an internal logic, we must pass to some higher category containing it which is at least an $(n+1,1)$-category.  The obvious choice is a category of [[presheaves]] or [[sheaves]]/[[stacks]] on $C$ valued in $n$-categories or $n$-groupoids (or $m$-groupoids for some $m\ge n$).

The second issue is that not every "generalized object" over $X$ may have a name.  This is almost impossible to get around while remaining within $C$, due to issues with paradoxes.  Even [[object classifiers in an (∞,1)-category]] only classify the core of some [[subcategory]] of $C/X$.

One way to deal with this is to suppose some (possibly [[ordinal|transfinite]]) sequence of object classifiers, each contained in the next, such that every generalized object is eventually classified by some one of them.  In the internal logic, this corresponds roughly to the idea of [[universe polymorphism]] in [[type theory]].

Another way is, of course, to move outside of $C$.  In particular, if we work in a category of presheaves/sheaves/stacks on $C$ at one category-level up, then the [[self-indexing]] of $C$ (or its [[core]]) will be an object $U$ which classifies *exactly* the desired category $C/X$ of generalized objects for each $X\in C$.  (The exhaustive sequence of universes can also be regarded as moving outside of $C$, perhaps to a category of [[ind-objects]] in $C$.)  The fragment of the internal logic of this category of stacks which deals only with objects of $C$ itself can then be identified with the direct Kripke--Joyal style stack-semantics described above.

Of course, one can also embrace this second limitation and just live with a "partial" stack semantics that only allows us to talk about a particular subclass of generalized objects.  The [[Mitchell–Bénabou language]] of a [[topos]] can be regarded as a partial stack semantics in this sense, in which the only generalized objects we can classify over are the [[subterminal objects]] (i.e. the [[subobjects]] $A \hookrightarrow X$).  The object $U$ in this case is, of course, the [[subobject classifier]].

One can also embrace the first limitation and not worry about having multiple names for the same object.  This leads to notions such as a [[universe in a topos]] and the field of [[algebraic set theory]].


## Relationship to locally internal categories

The stack semantics for a topos $\mathcal{E}$ can be used to talk about [[locally internal category|locally internal categories]] of $\mathcal{E}$ (in the sense of ([Penon 1974](#Penon))) as if they're ordinary locally small categories over $\mathrm{Set}$.

Examples:

* A geometric morphism $f: \mathcal{F} \to \mathcal{E}$ looks like the canonical morphism $\mathcal{F} \to \mathrm{Set}$ when using the stack semantics of $\mathcal{E}$.

* The internal statement "$\mathcal{F}$ is a compact topos" is equivalent to $f$ being a [[proper geometric morphism|proper morphism]].

* The internal statement "$\mathcal{F}$ is an indiscrete topos" (i.e. "the canonical morphism $\mathrm{Sub}_{\mathcal{F}}(1) \to \mathrm{Sub}_{\mathrm{Set}}(1)$ is a bijection", where $\mathrm{Sub}$ refers to the corresponding [[poset of subobjects|posets of subobjects]]) is true iff $f$ is [[hyperconnected geometric morphism|hyperconnected]].

* Because the proof that indiscrete toposes are compact is constructive, it immediately follows that hyperconnected morphisms are proper.


## Related concepts

* [[semantics]]

* [[Kripke–Joyal semantics]]


## References

* [[Mike Shulman]], _[Stack semantics and the comparison of material and structural set theories](http://arxiv.org/abs/1004.3802)_ (2010)

* [[Mike Shulman]], _Large categories and quantifiers in topos theory_, [slides](http://home.sandiego.edu/~shulman/papers/cambridge-stacksem.pdf) (2021)

* J. Penon, _Categories localement internes_, C. R. Acad. Sci. Paris __278__ (1974) A1577--1580
{#Penon}

* Locally internal categories, Appendix in: [[Peter Johnstone]], _Topos theory_, London Math. Soc. Monographs __10__, Acad. Press 1977, xxiii+367 pp.
{#Johnstone}
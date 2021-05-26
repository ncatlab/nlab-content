
# Monotone functions
* table of contents
{: toc}

## Idea

A monotone function is a [[functor]] between [[preordered sets]].


## Explicit definitions

Let $S$ and $T$ be preordered sets, that is [[sets]] equipped with a [[reflexive relation|reflexive]] and [[transitive relation|transitive]] binary [[relation]] $\leq$.  (By convention, the same symbol is used for both sets, even technically it is not the same relation.)

Then a [[function]] $f$ from $S$ to $T$ is __monotone (increasing)__, __isotone__, __weakly increasing__, or __order-preserving__ if it preserves $\leq$:
$$ x \leq y \;\Rightarrow\; f(x) \leq f(y) $$
for all $x, y$ in $S$.

A __strictly increasing__ function is a weakly increasing function that is also [[injective function|injective]], at least if $S$ and $T$ are [[partial order|partially ordered]].  Between arbitrary preordered sets, however, it is probably better to accept as strictly increasing any weakly increasing function that is weakly injective in that $x \leq y$ whenever $f(x) = f(y)$; such a function must be injective if $S$ is a partial order (since $y \leq x$ will also follow) but not necessarily in general.

+-- {: .query}
_[[Mike Shulman]]_: Is that really the right definition?  I think of "strictly increasing" as meaning that $x \lt y$ implies $f(x) \lt f(y)$, which is equivalent to the above for linear orders but weaker for partial orders.  But I don't have much experience with strictly increasing functions between non-linear orders, so maybe that is the right definition for partial orders.

However, I don't think it is the right definition for preorders; among other things, it's not invariant under equivalence of categories.  It seems to me that what you really want to say is that it is [[pseudomonic functor|pseudomonic]] as a functor (whereas my weaker definition would become the statement that it is [[conservative functor|conservative]] as a functor.)

_Toby_:  This is the definition in _[[HAF]]_ (Section 3.17), which defines it for posets (and is a smart enough book that it wouldn\'t blindly extend a definition from a special case).  Although I don\'t have a reference, I\'m pretty sure that this also used in analysis and topology when thinking about convergence and nets, where they may be prosets.  However, I think that you have a good point about preordered sets, so I\'ve changed the wording above.  (I\'ll also try to confirm how covergence theorists define 'strictly increasing' functions between directed prosets.)

It occurs to me that, in the absence of the axiom of choice, one ought to accept even anafunctors between prosets as morphisms, even though these may not be representable as strict functions at all.  I\'ll save that for another day, however.

[[Mike Shulman]]: Of course, the definition you gave above isn't the same as pseudomonic unless $T$ is a partial order; in general you want to say $x\leq y$ whenever $f(x) \cong f(y)$.  The version with $=$ is still not invariant under equivalence of $T$.

I don't know a whole lot about convergence and nets, but I don't remember seeing strictly increasing functions used there; I look forward to seeing what you find.  Does HAF use the poset version for any application that makes clear why this is a good definition?  Of course, monomorphisms of posets may quite naturally something to be interested in, but the question is why they should be called "strictly increasing."
=--

A function $f$ is __monotone decreasing__, __antitone__, __weakly decreasing__, or __order-reversing__ if it reverses $\leq$:
$$ x \leq y \;\Rightarrow\; f(y) \leq f(x) $$
for all $x, y$ in $S$.

A __strictly decreasing__ function is a weakly decreasing function that is also (weakly) injective.

Sometimes the term 'monotone' or 'isotone' (but rarely both) is used for function from $S$ to itself such that
$$ x \leq f(x) $$
for all $x$ in $S$.

+-- {: .query}
Is there a widely accepted term for this?  I\'ve seen both of these, I think, but the other meaning seems to be more common for both.  ---[[Toby Bartels|Toby]]
=--


## High-level explanation

As a preordered set is the same thing as a [[category]] in which any two [[parallel morphisms]] are equal, so a monotone function is simply a [[functor]] between such categories.  An antitone function is a [[contravariant functor]].  That 'monotone' may be used for both matches that 'functor' may be used for both covariant and contravariant functors.

Strictly increasing (and strictly decreasing) functions are particularly important between [[linearly ordered sets]], where are the most natural kind of morphism.  Between partially ordered sets in general (and between preordered sets using the stricter definition), the strictly increasing functions are simply the [[monomorphisms]] (if weakly increasing functions are taken as the morphisms).  If we use the weaker definition between preordered sets, then the strictly increasing functions correspond to [[pseudomonic functors]], which is an appropriate sort of [[higher category theory|higher]] monomorphism; this is one reason for preferring that definition.

The alternative sort of monotone function on a single proset $S$ is rather different; we mention it here largely because of the potential terminological confusion, but it might as well have its own article if we find a nice name for it.  As a functor, it is a functor for which every object is an [[algebra for a functor|algebra]]; the condition is part of the requirements of a [[Moore closure]] (a [[monad]] on $S$).


[[!redirects monotone]]
[[!redirects monotone function]]
[[!redirects monotone functions]]
[[!redirects monotone map]]
[[!redirects monotone maps]]
[[!redirects monotone mapping]]
[[!redirects monotone mappings]]
[[!redirects monotonic]]
[[!redirects monotonic function]]
[[!redirects monotonic functions]]
[[!redirects monotonic map]]
[[!redirects monotonic maps]]
[[!redirects monotonic mapping]]
[[!redirects monotonic mappings]]
[[!redirects monotone-increasing]]
[[!redirects monotone increasing]]
[[!redirects monotone-increasing function]]
[[!redirects monotone-increasing functions]]
[[!redirects monotone increasing function]]
[[!redirects monotone increasing functions]]
[[!redirects increasing function]]
[[!redirects increasing functions]]
[[!redirects weakly increasing function]]
[[!redirects weakly increasing functions]]
[[!redirects weakly-increasing function]]
[[!redirects weakly-increasing functions]]
[[!redirects isotone function]]
[[!redirects isotone functions]]
[[!redirects order-preserving function]]
[[!redirects order-preserving functions]]
[[!redirects order preserving function]]
[[!redirects order preserving functions]]

[[!redirects monotone-decreasing]]
[[!redirects monotone decreasing]]
[[!redirects monotone-decreasing function]]
[[!redirects monotone-decreasing functions]]
[[!redirects monotone decreasing function]]
[[!redirects monotone decreasing functions]]
[[!redirects decreasing function]]
[[!redirects decreasing functions]]
[[!redirects weakly decreasing function]]
[[!redirects weakly decreasing functions]]
[[!redirects weakly-decreasing function]]
[[!redirects weakly-decreasing functions]]
[[!redirects antitone]]
[[!redirects antitones]]
[[!redirects antitone function]]
[[!redirects antitone functions]]
[[!redirects order-reversing function]]
[[!redirects order-reversing functions]]
[[!redirects order reversing function]]
[[!redirects order reversing functions]]

[[!redirects strictly increasing function]]
[[!redirects strictly increasing functions]]
[[!redirects strictly-increasing function]]
[[!redirects strictly-increasing functions]]
[[!redirects strictly decreasing function]]
[[!redirects strictly decreasing functions]]
[[!redirects strictly-decreasing function]]
[[!redirects strictly-decreasing functions]]
[[!redirects strictly order-preserving function]]
[[!redirects strictly order-preserving functions]]
[[!redirects strict order-preserving function]]
[[!redirects strict order-preserving functions]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


# Monotone functions
* table of contents
{: toc}

## Idea
 {#Idea}

A function between [[preordered sets]] is called *monotone* if it respects the (pre)[[ordering]].

When [[preordered sets]] are regarded as [[categories]] (namely: [[(0,1)-categories]]) then monotone functions are equivalently the *[[functors]]* between these.


## Definition

### In components

Let $S$ and $T$ be [[preordered sets]], that is [[sets]] equipped with a [[reflexive relation|reflexive]] and [[transitive relation|transitive]] binary [[relation]] $\leq$.  (By convention, the same symbol is used for both sets, even though technically it is not the same relation.)

Then a [[function]] $f$ from $S$ to $T$ is __monotone (increasing)__, __isotone__, __weakly increasing__, or __order-preserving__ if it preserves $\leq$:
$$ x \leq y \;\Rightarrow\; f(x) \leq f(y) $$
for all $x, y$ in $S$.

A __strictly increasing__ function is a weakly increasing function that is also [[injective function|injective]], at least if $S$ and $T$ are [[partial order|partially ordered]].  Between arbitrary preordered sets, however, it is probably better to accept as strictly increasing any weakly increasing function that is weakly injective in that $x \leq y$ whenever $f(x) = f(y)$; such a function must be injective if $S$ is a partial order (since $y \leq x$ will also follow) but not necessarily in general.



A function $f$ is __monotone decreasing__, __antitone__, __weakly decreasing__, or __order-reversing__ if it reverses $\leq$:
$$ x \leq y \;\Rightarrow\; f(y) \leq f(x) $$
for all $x, y$ in $S$.

A __strictly decreasing__ function is a weakly decreasing function that is also (weakly) injective.





### Category-theoretic

As a preordered set is the same thing as a [[category]] in which any two [[parallel morphisms]] are equal, so a monotone function is simply a [[functor]] between such categories.  An antitone function is a [[contravariant functor]].  That 'monotone' may be used for both matches that 'functor' may be used for both covariant and contravariant functors.

Strictly increasing (and strictly decreasing) functions are particularly important between [[linearly ordered sets]], where are the most natural kind of morphism.  Between partially ordered sets in general (and between preordered sets using the stricter definition), the strictly increasing functions are simply the [[monomorphisms]] (if weakly increasing functions are taken as the morphisms).  If we use the weaker definition between preordered sets, then the strictly increasing functions correspond to [[pseudomonic functors]], which is an appropriate sort of [[higher category theory|higher]] monomorphism; this is one reason for preferring that definition.

The alternative sort of monotone function on a single proset $S$ is rather different; we mention it here largely because of the potential terminological confusion, but it might as well have its own article if we find a nice name for it.  As a functor, it is a functor for which every object is an [[algebra for a functor|algebra]]; the condition is part of the requirements of a [[Moore closure]] (a [[monad]] on $S$).

## Related concepts

* [[enriched monotone]]

* [[injective function]]

* [[surjective function]]

* [[equivariant function]]


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


[[!redirects strictly monotone function]]
[[!redirects strictly monotone functions]]

[[!redirects strictly monotonic]]

[[!redirects antitonic]]


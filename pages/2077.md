## Idea

A monotone function is a [[functor]] between [[preordered sets]].


## Explicit definitions

Let $S$ and $T$ be preordered sets, that is [[sets]] equipped with a [[reflexive relation|reflexive]] and [[transitive relation|transitive]] binary [[relation]] $\leq$.  (By convention, the same symbol is used for both sets, even technically it is not the same relation.)

Then a __monotone (increasing)__, __isotone__, or __weakly increasing__ function $f$ from $S$ to $T$ is a [[function]] from the set $S$ to the set $T$ that preserves $\leq$:
$$ x \leq y \;\Rightarrow\; f(x) \leq f(y) $$
for all $x, y$ in $S$.

A __strictly increasing__ function is a weakly increasing function that is also [[injective function|injective]].

An __antitone__, __weakly decreasing__, or __monotone decreasing__ function $f$ from $S$ to $T$ is a [[function]] from the set $S$ to the set $T$ that reverses $\leq$:
$$ x \leq y \;\Rightarrow\; f(y) \leq f(x) $$
for all $x, y$ in $S$.

A __strictly decreasing__ function is a weakly decreasing function that is also injective.

Sometimes the term 'monotone' or 'isotone' (but rarely both) is used for function from $S$ to itself such that
$$ x \leq f(x) $$
for all $x$ in $S$.

+-- {: .query}
Is there a widely accepted term for this?  I\'ve seen both of these, I think, but the other meaning seems to be more common for both.  ---[[Toby Bartels|Toby]]
=--


## High-level explanation

As a preordered set is the same thing as a [[category]] in which any two [[parallel morphisms]] are equal, so a monotone function is simply a [[functor]] between such categories.  An antitone function is a [[contravariant functor]].  That 'monotone' may be used for both matches that 'functor' may be used for both covariant and contravariant functors.

Strictly increasing (and strictly decreasing) functions are particularly important between [[linearly ordered sets]], where are the most natural kind of morphism.  Between preordered sets in general (taking the weakly increasing functions as morphisms), the strictly increasing functions are simply the [[monomorphisms]].

The alternative sort of monotone function on a single proset $S$ is rather different; we mention it here largely because of the potential terminological confusion, but it might as well have its own article if we find a nice name for it.  As a functor, it is a functor for which every object is an [[algebra for a functor|algebra]]; the condition is part of the requirements of a [[Moore closure]] (a [[monad]] on $S$).


[[!redirects increasing function]]
[[!redirects isotone function]]
[[!redirects antitione function]]
[[!redirects decreasing function]]
[[!redirects monotone functions]]
[[!redirects increasing functions]]
[[!redirects isotone functions]]
[[!redirects antitione functions]]
[[!redirects decreasing functions]]
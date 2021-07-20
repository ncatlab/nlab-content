
# Too simple to be simple
* table of contents
{: toc}

## Idea

There is a general principle in mathematics that
+-- {: .standout}
A trivial object is too simple to be simple.
=--

Quite often, classical references will define 'simple' (or an analogous term) in na&#239;ve way, so that a 'trivial' object *is* simple, but later it will become clear that more sophisticated theorems (especially classification theorems) work better if the definition is changed so that the trivial object is *not* simple.  Usually this can be done by changing 'if' to 'iff' (or sometimes changing 'or' to 'xor') in the classical definition.

The general pattern is a progression of definitions (of 'simple') from more to less na&#239;ve:

1.  Imprecise summary: there are no foos.  (Example: in a field, every element is invertible.)
2.  Classical definition: there are no nontrivial foos.  (Example: in a field, every element other than $0$ is invertible.)
3.  Modern definition: there are no nontrivial foos, but there is the trivial foo.  (Example: in a field, every element other than $0$ is invertible, and $0$ is non-invertible.)


## Examples

Examples include:

*  [[one|1]] is not a [[prime number]].
*  The [[trivial ring]] is not a [[field]] (or even an [[integral domain]]).
*  The [[trivial group]] is not a [[simple group]] (which is the trope-namer).
*  A [[zero object]] is not a [[simple object]] (generalizing the previous example).
*  The [[empty space]] is not a [[path-connected space]] (or even a [[connected space]]).
*  The [[improper ideal]] is not a [[maximal ideal]] (or even a [[prime ideal]]).
*  The [[improper filter]] is not an [[ultrafilter]].
*  The [[empty function]] from the [[empty set]] to $X$ is not a [[constant function]].

But of course one may still find definitions used that disagree (see discussion at [[connected space]] and [[empty space]], for example).

This should be distinguished from barring the trivial object entirely.  Historically, many people wanted to say that the [[empty set]] is not a [[set]], and some people still say that the [[trivial ring]] is not a [[ring]] or that the [[improper filter]] is not a [[filter]].  This allows one to state later definitions (as of [[field]] or [[ultrafilter]]) without having to exclude the trivial object, but this does the exclusion too early.

Perhaps the basic example is that

*  [[false|False]] is not [[true]].

Nobody would be na&#239;ve enough to believe otherwise in this case, of course.  The point with this example is that, in the other cases, the na&#239;ve definition imposes only a uniqueness requirement (so that some set of possibilities ---such as the set of proper divisors of a prime number, or the set of non-invertible elements of a field--- must be a [[subsingleton]]) when it should in fact impose an *existence and uniqueness* requirement (so that the set of possibilities must be a [[singleton]]).  With [[truth values]], uniqueness is automatic, so existence is easier to notice.  More abstractly, the na&#239;ve definition is about $(-1)$-[[(-1)-truncation|truncation]], while the more sophisticated definition is about $(-2)$-[[(-2)-truncation|truncation]], which is more often relevant.


## Relationship to biased definitions

In many of the above examples one can obtain the sophisticated definition from the na&#239;ve definition by replacing a $2$-ary function by a function of arbitrary (finite) arity. For example we would replace

* $n$ is prime if whenever $n = a b$ we have $n = a$ or $n = b$

with

* $n$ is prime if whenever $n = \prod_{i=1}^k a_i$ we have $n = a_i$ for some $i$

Then $1$ is not a prime because it is equal to the empty product ($k = 0$) but not equal to any of the $a_i$ (because there aren't any)! Similarly we have:

* The [[empty space]] is the empty union, and therefore not [[connected space|connected]].
* In the [[trivial ring]] the empty product is equal to zero,
and so this ring is not [[integral domain|integral]].
* [[false|False]] is the empty disjunction, and hence is not [[true]].

This illustrates one advantage of using unbiased rather than [[biased definition|biased]] definitions: if one has replaced "for all $n$" with "for both $0$ and $2$" then it is very easy to forget the $0$ case and end up with a definition that fails for the trivial case.  (Unfortunately, it seems to be easy to forget $0$ even when using unbiased definitions, but hopefully less easy.)

In a similar vein we can define [[path-connected space|path connected]] by

* A space is path connected if for each ([[Kuratowski-finite|Kuratowski]])-finite subset there is a [[path]] (a [[continuous map]] from the [[unit interval]]) passing through every point of that subset.

Then the empty space is not path connected because it has no paths at all and hence no path through the empty subset.


[[!redirects too simple to be simple]]
[[!redirects too simple]]
[[!redirects trivial]]
[[!redirects trivial object]]
[[!redirects trivial objects]]

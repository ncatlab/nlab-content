There is a general principle in mathematics that
+-- {: .standout}
A trivial object is too simple to be simple.
=--

Quite often, classical references will define 'simple' (or an analogous term) in na&#239;ve way, so that a 'trivial' object *is* simple, but later it will become clear that more sophisticated theorems (especially classification theorems) work better if the definition is changed so that the trivial object is *not* simple.  Usually this can be done by changing 'if' to 'iff' (or sometimes changing 'or' to 'xor') in the classical definition.

Examples include:

*  [[one|1]] is not a [[prime number]].
*  The [[trivial ring]] is not a [[field]].
*  The [[zero object]] is not a [[simple object]] (which is the trope-namer).
*  The [[empty space]] is not a [[connected space]] (although one can argue about this, depending on the definition of "connected").
*  The [[improper ideal]] is not a [[maximal ideal]] or a [[prime ideal]].
*  The [[improper filter]] is not an [[ultrafilter]].

Not that anybody would be na&#239;ve enough to believe otherwise, but perhaps the basic example is that

*  [[false|False]] is not [[true]].

The point is that, in many cases, the na&#239;ve definition imposes only an uniqueness requirement (so that some set of possibilities ---such as the set of proper divisors of a prime number, or the set of non-invertible elements of a field--- must be a [[subsingleton]]) when it should in fact impose an *existence and uniqueness* requirement (so that the set of possibilities must be a [[singleton]]).

The general pattern is a progression of definitions (of 'simple') from more to less na&#239;ve:

1.  Suitable for an Idea section but obviously not correct: there are no foos (a field has no non-invertible elements).
2.  Original na&#239;ve definition: there are no nontrivial foos (a field has no non-invertible elements except $0$).
3.  Sophisticated definition: there are no nontrivial foos, but the trivial foo is there (a field has no non-invertible elements except $0$, and $0$ is non-invertible).

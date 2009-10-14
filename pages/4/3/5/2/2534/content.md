A multiset is like a [[set]], just allowing that the elements have multiplicities. Thus the multiset $\{1,1,2\}$ differs from the multiset $\{1,2\}$, while $\{1,2,1\}$ is the same as $\{1,1,2\}$. Multisets are useful in [[combinatorics]]. See [wikipedia](http://en.wikipedia.org/wiki/Multiset).


## Definitions 

While it is possible to take multisets as a fundamental concept in [[foundations]], it is more common to define them in terms of [[sets]] and [[functions]].


A **multiset** can be defined as a set $A$ (its __underlying set__) together with a function $\mu$ (giving each element its __multiplicity__) from $A$ to the class of nonzero [[cardinal numbers]].  A multiset is **locally finite** if multiplicity takes values in the (nonzero) [[natural numbers]].  Many authors take all multisets to be locally finite; that is the default in combinatorics.  The multiset is **finite** if it is locally finite and $A$ is a [[finite set]].  We can also define a multiset to be a function from the [[proper class]] of all objects to the class of all cardinal numbers, with the proviso that the objects whose multiplicity is nonzero form a set (the set $A$ above).


The above definition does not work in all foundations; without the [[axiom of choice]] it may be too weak, and there is no class of all objects in a structural set theory.  However, if we are only interested in multisets with elements drawn from a given set $U$ (as is common in combinatorics), then an alternative definition is very useful: a __multisubset__ of $U$ is a function $f\colon B \to U$, where two multisubsets $f\colon B \to U$ and $f'\colon B' \to U$ are considered _equal_ if there is a [[bijection]] $g\colon B \to B'$ that makes a commutative triangle.  In other words, a multisubset of $U$ is an isomorphism class in the [[slice category]] $Set/U$.  (Compare this to the structural definition of _[[subset]]_ of $U$ as an [[injective function]] to $U$.)


A multisubset of $U$ is locally finite if every [[fibre]] is finite; it is finite if additionally the [[image]] of $f$ (which corresponds to $A$ in the original definition) is finite.  A locally finite multisubset can also be described as a function from $U$ to the set of natural numbers; this is just the multiplicity function $\mu$ again, now with $U$ (rather than $A$ or the class of all objects) specified as the domain.


## Operations on multisets

The operations on cardinal numbers induce operations on multisets (or on multisubsets of any given set $U$).

*  An __[[intersection]]__ of multisets is given by the [[infimum]] operation on cardinal numbers.

+--{.query}

[[Eric]]: Given $X = \{1,1,2\}$ and $Y = \{1,1,3\}$, is $X\cap Y = \{1,1\}$ or is $X\cap Y = \{1\}$?

=--

*  A __[[union]]__ of multisets is given by the [[supremum]] operation on cardinal numbers.
*  A __sum__ of multisets (written $A \oplus A'$) is given by addition of cardinal numbers; this has no analogue for ordinary sets.


[[!redirects multisubset]]
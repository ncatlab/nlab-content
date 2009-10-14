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

[[Todd Trimble|Todd]]: It's $\{1, 1\}$. (To make the question structural, we should think of $X$ and $Y$ as multisubsets of some other multiset, but never mind.) 

As a writer (perhaps Toby) was saying above, a locally finite multiset $M$ can be thought of as an ordinary set $X$ equipped with a multiplicity function $\mu: X \to \mathbb{N}$. A multisubset of $M$ can then be reckoned as
$X$ equipped with a function $\nu: X \to \mathbb{N}$ which is bounded above by $\mu$. To take the intersection of two multisubsets $\nu, \nu': X \to \mathbb{N}$, you take the minimum or inf of $\nu, \nu'$. Your question can then be translated to one where $X = \{1, 2, 3\}$, where $\nu(1) = 2, \nu(2) = 1, \nu(3) = 0$ and $\nu'(1) = 2, \nu'(2) = 0, \nu'(3) = 1$. 

[[Eric]]: Thanks Todd! The reference [Mathematics of Multisets](http://obelix.ee.duth.gr/~apostolo/Articles/MathMSet.pdf) explains this nicely too.

=--

*  A __[[union]]__ of multisets is given by the [[supremum]] operation on cardinal numbers.
*  A __sum__ of multisets (written $A \oplus A'$) is given by addition of cardinal numbers; this has no analogue for ordinary sets.

## Morphisms

What is a function between multisets?  I would be inclined to say that for multisubsets of an ambient universe $U$ considered as objects of $Set/U$, a function from $B\to U$ to $B'\to U$ would be an arbitrary function $B\to B'$ (not necessarily commuting with the projections to $U$).  But this doesn't work if a multisubset of $U$ is an *isomorphism class* in $Set/U$ rather than merely an object of it.  -- [[Mike Shulman]]

[[Eric]]: This definition is taken from Syropoulos:

**Definition**. Category $\mathbf{MSet}$ is a category of all possible multisets.

1. The objects of the category consist of pairs $(A, P)$, where $A$ is a set and $P:A\to Set$ a presheaf on $A$.
1. If $(A,P)$ and $(B,Q)$ are two objects of the category, an arrow between these objects is a pair $(f,\lambda)$, where $f:A\to B$ is a function and $\lambda:P\to Q\circ f$ is a natural transformation, i.e., a family of functions.
1. Arrows compose as follows: suppose that $(A,P)\stackrel{(f,\lambda)}{\to}(B,Q)$ and $(B,Q) \stackrel{(g,\mu)}{\to}(C,R)$ are arrows of the category, then $(f,\lambda)\circ (g,\mu) = (g\circ f, \mu\times\lambda)$, where $g\circ f$ is the usual function composition and $\mu\times\lambda:P\to R\circ (g\circ f)$.
4. Given an object $(A,P)$, the identity arrow is $(id_A, id_P)$.

The last part of the definition is a kind of wreath product (see [4]). However, it is not clear at the moment how this definition fits into the general theory of
wreath products.

[[Mike Shulman]]: Huh.  So his definition takes a multiset to assign a *set* to every element, rather than a *cardinality* to every element, so that the multisubsets of $U$ are exactly objects of $Set/U$.  I'm surprised, though, that with his definition the only functions $\{1,1\} \to \{2,3\}$ are constant; why can't I send the two copies of $1$ to different places?

## Examples

...

## References

* [Mathematics of Multisets](http://obelix.ee.duth.gr/~apostolo/Articles/MathMSet.pdf), Apostolos Syropoulos

* [Categorical Models of Multisets](http://obelix.ee.duth.gr/~apostolo/Articles/mset.pdf), Apostolos Syropoulos

[[!redirects multisubset]]
A category is __equationally presentable__ if it may be described, beginning with the category [[Set]], as the category of [[sets]] equipped with certain operations satisfying certain [[equation]]s involving these operations as [[objects]], and [[functions]] that preserve these operations as [[morphisms]].  A category is __equationally presented__ if it is equipped with such a description.

A more formal definition would be useful here (but perhaps a bit tedious); the point is that an equationally presentable category is given by an [[algebraic theory]] interpreted in [[Set]].

We can generalise to categories given by laws which may be [[implications]] between equations rather than simply equations themselves; call such a category __quasi-equationally presentable__ or __quasi-equationally presented__.

In general, we allow largely many operations and equations (that is a [[proper class]] of them, too many be parametrised by an object of $Set$ itself), although each individual operation must have small arity and each equation must be well-founded.


## Monadic and algebraic categories

Equationally presentable categories capture precisely the categories of [[varieties of algebras]] studied in [[universal algebra]].  However, to study them with [[category theory]], it is somewhat more manageable to use [[monadic categories]] instead.  We have that an algebraic category $C$ is monadic if and only if it has [[free objects]]; that is, the [[forgetful functor]] from $C$ to $Set$ has a [[left adjoint]].

Let a (quasi)-equationally presentable category $C$ be __bounded__ if it may be described using only a small set of operations (and hence a small set of equations); in this case it follows that $C$ is monadic (if it is equationally presentable) or at least [[algebraic category|algebraic]] (if it is only quasi-equationally presentable), although the converse does not hold.  Similarly, let $C$ be __finitary__ if it may be described using only a small set of operations, each of which has finite arity (in which case it must be bounded).  We can characterise boundedness and finite arity nicely in category-theoretic terms; thus one speaks of bounded monadic categories, finitary algebraic categories, etc.  See [[algebraic category]] for the definitions; it is a theorem that the definitions there are equivalent to the definitions here.

+-- {: .query}
Is it true that a quasi-equationally presentable category is algebraic if it has free objects?  Both Johnstone and AHS stop short of this case.
=--

Finitary monadic categories are particularly nice; they are given by [[Lawvere theories]].

Warning:  The meaning of 'algebraic category' varies in the literature; Johnstone in _[[Stone Spaces]]_ defines it to mean monadic, while we follow (here and at [[algebraic category]]) AHS in _The [[Joy of Cats]]_ .  The term 'equationally presentable' is from Johnstone, and the claim that this is equivalent to being given by an [[algebraic theory]] requires using Johnstone\'s definition of the latter from the _[[Elephant]]_.  The term 'quasi-equationally presentable' is [[Toby Bartels|my own]], following a pattern set down by AHS.


## References

Same as [[algebraic category]].


[[!redirects equationally presentable category]]
[[!redirects equationally presented category]]
[[!redirects equationally-presentable category]]
[[!redirects equationally-presented category]]
[[!redirects equationally presentable categories]]
[[!redirects equationally presented categories]]
[[!redirects equationally-presentable categories]]
[[!redirects equationally-presented categories]]

[[!redirects quasi-equationally presentable category]]
[[!redirects quasi-equationally presented category]]
[[!redirects quasiequationally presentable category]]
[[!redirects quasiequationally presented category]]
[[!redirects quasi-equationally-presentable category]]
[[!redirects quasi-equationally-presented category]]
[[!redirects quasiequationally-presentable category]]
[[!redirects quasiequationally-presented category]]
[[!redirects quasi-equationally presentable categories]]
[[!redirects quasi-equationally presented categories]]
[[!redirects quasiequationally presentable categories]]
[[!redirects quasiequationally presented categories]]
[[!redirects quasi-equationally-presentable categories]]
[[!redirects quasi-equationally-presented categories]]
[[!redirects quasiequationally-presentable categories]]
[[!redirects quasiequationally-presented categories]]
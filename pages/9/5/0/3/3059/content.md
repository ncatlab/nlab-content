A category is __equationally presentable__ if it may be described, beginning with the category [[Set]], as the category of [[sets]] equipped with certain operations satisfying certain [[equation]]s involving these operations as [[objects]], and [[functions]] that preserve these operations as [[morphisms]].  A category is __equationally presented__ if it is equipped with such a description.

A more formal definition may be handy here; the point is that an equationally presentable category is given by an [[algebraic theory]] interpreted in [[Set]].

In general, we allow largely many operations and equations (that is a [[proper class]] of them, too many be parametrised by an object of $Set$ itself).  A category is __smally__ equationally presentable (or presented) if it may be (or is) described using only a small set of operations and equations.  It is __finitely__ equationally presentable if it may be described using only a small set of operations and equations, such that every operation has finite arity.

Equationally presentable categories capture precisely the categories of [[varieties of algebras]] studied in [[universal algebra]].  However, to study them with [[category theory]], it is somewhat more manageable to use [[monadic categories]] instead.  The theorem is: every smally equationally presentable category is monadic, and every monadic category is largely equationally presentable, but neither converse holds.

It may be useful to generalise to categories given by laws which may be [[implications]] between equations rather than simply equations themselves.  Following _The [[Joy of Cats]]_, let us call a monadic category that may be so given _[[algebraic category|algebraic]]_.  Then we can call an algebraic category __small algebraic__ if it is given by a small set of operations and laws; more generally, a __large algebraic__ category is given by a (possibly large) class of operations and laws.  Again we have the theorem: every small algebraic category is algebraic, and every algebraic category is large algebraic, but neither converse holds.

While monadic categories are easier to handle than (small or large) equationally presentable categories, there is no problem for finitely equationally presentable categories.  These are simply given by [[Lawvere theories]].

Beware of terminology:  The meaning of 'algebraic category' varies in the literature; Johnstone in _[[Stone Spaces]]_ defines it to mean monadic, while AHS in _The [[Joy of Cats]]_ (which we follow at [[algebraic category]]) use a definition equivalent to the one above.  The term 'equationally presentable' is from Johnstone, and the claim that this is equivalent to being given by an [[algebraic theory]] requires using Johnstone\'s definition of the latter from the _[[Elephant]]_.  The terms with 'small' and 'large' in them are [[Toby Bartels|my own]].


[[!redirects equationally presentable category]]
[[!redirects equationally presented category]]
[[!redirects smally equationally presentable category]]
[[!redirects smally equationally presented category]]
[[!redirects small equationally presentable category]]
[[!redirects small equationally presented category]]
[[!redirects largely equationally presentable category]]
[[!redirects largely equationally presented category]]
[[!redirects large equationally presentable category]]
[[!redirects large equationally presented category]]
[[!redirects smally algebraic category]]
[[!redirects small algebraic category]]
[[!redirects largely algebraic category]]
[[!redirects large algebraic category]]
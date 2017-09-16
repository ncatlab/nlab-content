[[!redirects loop(algebra)]]


A _quasigroup_ is a generalization of a [[group]] without the associativity law.  (More precisely, a quasigroup has neither binary nor nullary associativity, that is no identity element either.  If you keep the identity element, then you get a _loop_.)

Note that, in the absence of associativity, it\'s not enough (even for a loop) to say that every element has an [[inverse element]] (on either side); instead, you must say that division is always possible.  This is because the definition $x/y = x y^{-1}$ won\'t work right without associativity.

## Definitions

The usual definition is this:
+-- {: .un_defn}
###### Definition

A __quasigroup__ is a [[set]] $G$ equipped with a binary operation $G \times G \to G$ (which we will write with concatenation) such that:

*  for all $x$ and $y$, there exist unique $l$ and $r$ such that $l x = y$ and $x r = y$.

Then $l$ is called the __left quotient__ $y / x$ ($y$ divided by $x$, $y$ over $x$) and $r$ is called the __right quotient__ $x \backslash y$ ($x$ dividing $y$, $x$ under $y$).
=--

As with the inverse elements of a group, we can make the quotients into operations so that all axioms are equations:
+-- {: .un_defn}
###### Definition

A __quasigroup__ is a [[set]] $G$ equipped with three binary operations (product, left quotient, and right quotient) such that these equations always hold:
*  $(x / y) y = x$,
*  $x (x \backslash y) = y$,
*  $(x y) / y = x$,
*  $x \backslash (x y) = y$.
=--
Thus quasigroups are described by a [[Lawvere theory]] and can therefore be [[internalization|internalized]] into any [[cartesian monoidal category]].

In any case:
+-- {: .un_defn}
###### Definition

A __loop__ is a quasigroup with an [[identity element]].
=--
Loops are also described by a Lawvere theory.

Note that, even in a loop, left and right inverses need not agree.  See [the discussion on the English Wikipedia](http://secure.wikimedia.org/wikipedia/en/wiki/Quasigroup#Inverse_properties) for convenient inverse properties.

For good measure, here is another special kind of quasigroup:
+-- {: .un_defn}
###### Definition

A __[[group]]__ is an associative loop.
=--

## Examples

*  Any group is a loop, of course.
*  Any [[abelian group]] is a quasigroup in two other ways: the product switches places with one of the quotients.  (The other quotient remains a quotient.)
*  The nonzero elements of a (not necessarily associative) [[division algebra]] (such as the [[octonion]]s) form a quasigroup; this fact is basically the definition of 'division algebra'.
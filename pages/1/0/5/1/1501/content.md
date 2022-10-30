
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _rigid (monoidal) category_, also called an _autonomous (monoidal) category_ is a kind of [[category with duals]].  Specifically, all of its objects are [[dualisable object|dualisable]] on both the left and the right.


## Definition

A [[monoidal category]] is **rigid** if every [[object]] has [[dualizable object|duals]] on both sides.  If only one type of dual exists, we speak of **left rigid** (or left autonomous) or **right rigid** categories.

Conventions differ regarding which type of duals are which.  One convention is as follows: a _right dual_ of an object $V$ in a monoidal category $M$ is an object $V^*$ equipped with unit $\eta : 1 \rightarrow V^* \otimes V$ and counit maps $\epsilon: V \otimes V^* \rightarrow 1$ satisfying the [[triangle identities]] (the snake diagrams), while a left dual is the dual notion.  This convention fits in with the standardized conventions regarding [[adjoint functor]]s: an endofunctor $F : C \rightarrow C$ has a right adjoint $F^* : C \rightarrow C$ if and only if $F^*$ is a right dual of $F$ in the [[monoidal category]] $End(C)$. 


## Remarks

Note that this definition only asserts the existence of the dual objects. It does _not_ assert that specific duals have been chosen. However, the choice of duals is unique up to unique isomorphism, justifying reference to '[[the]]' dual of an object; in fact, this extends to a [[contravariant functor|contravariant]] [[anafunctor]] ${}^*\colon M \to M$.  (Using the [[axiom of choice]] to pick duals for every object at once, we can make this into a [[strict functor]].)

Nor does this definition assert that the right dual of an object is isomorphic to its left dual: this need not be the case in general, though it is true in a [[braided monoidal category]], and thus automatically also in a [[symmetric monoidal category]] (this last fact can be considered an algebraic form of the "Whitney trick" for knots; see this [MO discussion](http://mathoverflow.net/questions/162677/why-is-a-braided-left-autonomous-category-also-right-autonomous/162693#162693)). Note that a rigid monoidal category which is also symmetric is sometimes called [[compact closed category|compact closed]], or simply "compact".

In practice, algebraic geometers are the most frequent users of the term 'rigid', and they focus on the symmetric monoidal case, so they ignore the difference between right and left duals.

## Properties

### Tannaka duality 

The statement of [[Tannaka duality]] for associative algebras says that rigid monoidal categories equipped with a [[fiber functor]] are [[categories of modules]] over a [[Hopf algebra]].

[[!include structure on algebras and their module categories - table]]


## References

* N. Saavedra Rivano, "Cat&#233;gories Tannakiennes." _Bulletin de la Soci&#233;t&#233; Math&#233;matique de France_ 100 (1972): 417-430. [EuDML](https://eudml.org/doc/87193)

## Related concepts

* [[star-autonomous category]]

* [[(∞,n)-category with duals]]

* [[linguistics|natural language syntax]]

[[!redirects rigid monoidal category]]
[[!redirects rigid monoidal categories]]
[[!redirects rigid category]]
[[!redirects rigid categories]]
[[!redirects autonomous monoidal category]]
[[!redirects autonomous monoidal categories]]
[[!redirects autonomous category]]
[[!redirects autonomous categories]]
[[!redirects left autonomous monoidal category]]
[[!redirects left autonomous monoidal categories]]
[[!redirects left autonomous category]]
[[!redirects left autonomous categories]]
[[!redirects right autonomous monoidal category]]
[[!redirects right autonomous monoidal categories]]
[[!redirects right autonomous category]]
[[!redirects right autonomous categories]]

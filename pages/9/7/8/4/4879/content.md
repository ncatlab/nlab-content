
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **Street fibration**, or **weak fibration**, is a generalization of a [[Grothendieck fibration]] which is [[non-evil]], i.e. covariant under equivalence of categories.  In [[Cat]], every Street fibration is equivalent to a Grothendieck one, so the extra generality is not very useful; since it is also fairly cumbersome, it is rarely used.  However, when working internally to a [[bicategory]], Street fibrations are really the only sensible notion.

## Definition

Let $p\colon E\to B$ be a [[functor]].  The notion of when a morphism of $E$ is [[cartesian morphism|cartesian]] is unchanged from the version for [[Grothendieck fibrations]].  However, now we say that $p$ is a **Street fibration** if for any $f:a\to b$ and $e\in E_b$ there exists a cartesian $\phi:e'\to e$ and an _isomorphism_ $h:p(e') \cong a$ such that $f\circ h = p(\phi)$.

### In terms of adjoint inverses

Back in the 60s J. Gray characterized fibrations as the functors $p\colon E\to B$ 
where for every $a \in E$ the slice functor $p/a \colon E/a \to B/p(a)$ has a right
adjoint right inverse $c_a$. One avoids evilness if one just requires that $c_a$ is
full and faithful, i.e. the counit of the adjunction $p/a \dasv c_a$ is an isomorphism. Explicitating this condition in elementary terms one arrives at the above definition.


## Properties

Every Grothendieck fibration is a Street fibration, as is every [[equivalence of categories]] (the latter are not in general Grothendieck fibrations).  Conversely, every Street fibration (in Cat) is the composite of an equivalence with a Grothendieck fibration: the latter can be taken to be a [[fibrant replacement]] of it in the [[canonical model structure]] on Cat.  In fact, a Street fibration is a Grothendieck fibration precisely when it is also a [[isofibration]].

When working with Street fibrations, one must always replace [[fibers]] with [[essential fibers]].  In particular, the lifting property of a Street fibration is insufficient for a morphism $u\colon J\to I$ in $B$ to induce a functor $u^*\colon E^I\to E^J$ between strict fibers, but such a functor is induced between essential fibers.  In this way we can reconstruct a [[pseudofunctor]] $B^{op}\to Cat$ from any Street fibration, and show that the [[2-category]] of Street fibrations is equivalent to that of such pseudofunctors (though not, as in the case of Grothendieck fibrations, [[strict 2-equivalence of 2-categories|strictly 2-equivalent]]).


## References

The notion was originally defined in 

* [[Ross Street]], *Fibrations in bicategories*

although there it was given in a very abstract form.  A more explicit form like that given above can be found in

* Ross Street, *Conspectus of variable categories*

[[!redirects Street fibrations]]
[[!redirects weak fibration]]
[[!redirects weak fibrations]]

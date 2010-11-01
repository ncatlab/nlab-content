
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A **Street fibration**, or **weak fibration**, is a generalization of a [[Grothendieck fibration]] which is [[non-evil]], i.e. covariant under [[equivalence of categories]].  In [[Cat]], almost all Street fibrations which arise in practice are actually Grothendieck fibrations, so the extra generality is not very useful; since it is also fairly cumbersome, it is rarely used.  However, when working with [[anafunctors]] or internally to a [[bicategory]] (a weak [[2-category]]), one is essentially forced to work with Street fibrations instead; see below.


## Definition

Let $p\colon E\to B$ be a [[functor]].  The notion of when a morphism of $E$ is [[cartesian morphism|cartesian]] is unchanged from the version for [[Grothendieck fibrations]].  However, now we say that $p$ is a **Street fibration** if for any $f:a\to b$ and $e\in E_b$ there exists a cartesian $\phi:e'\to e$ and an _isomorphism_ $h:p(e') \cong a$ such that $f\circ h = p(\phi)$.

An [[internalization|internalized]] version of this definition can be given in any [[2-category]]; see [[fibration in a 2-category]].  The above definition corresponds to the special case of the 2-category [[Cat]].


### In terms of adjoint inverses

Back in the 1960s, J. Gray characterized fibrations as the functors $p\colon E\to B$ 
where for every $a \in E$ the [[slice functor]] $p/a \colon E/a \to B/p(a)$ has a [[right
adjoint]] [[right inverse]] $c_a$. One avoids evilness if one just requires that $c_a$ is
[[fully faithful functor|full and faithful]], i.e. the [[counit of the adjunction]] $p/a \dashv c_a$ is an isomorphism. Explicating this condition in elementary terms, one arrives at the above definition.

### Other definitions

Most other characterizations of Grothendieck fibrations can also be given in a "non-evil" version to characterize Street fibrations.

## Comparison to Grothendieck fibrations

Every Grothendieck fibration is a Street fibration, as is every [[equivalence of categories]] (the latter are not in general Grothendieck fibrations).  Since Street fibrations are closed under composition, any functor equivalent to a Street fibration is also a Street fibration (this is the "covariance" property).  As remarked above, however, almost all functors in [[Cat]] which one wants to treat as "fibrations" are actually Grothendieck fibrations.  Moreover, in $Cat$ every Street fibration is the composite of an equivalence with a Grothendieck fibration: the latter can be taken to be a [[fibrant replacement]] of it in the [[canonical model structure]] on Cat.  (In fact, a Street fibration is a Grothendieck fibration precisely when it is also a [[isofibration]].)

For these reasons, Street fibrations in $Cat$ are little-studied.  The fact that they exist, and that any Street fibration is equivalent to a Grothendieck one, can be useful in assuaging philosophical worries about the "[[evil|evilness]]" of the notion of Grothendieck fibration, but in practice in $Cat$ one usually wants to use Grothendieck fibrations.

However, when internalizing in other 2-categories, covariance becomes more important.  This is most obvious when the 2-category in which one wishes to internalize is only a weak 2-category (a [[bicategory]]), in which it does not even make much sense to internalize the notion of Grothendieck fibration.  (This is even the case in [[Cat]] if we define it using [[anafunctors]], as is often important to do in the absence of the [[axiom of choice]].)  However, even when internalizing in a [[strict 2-category]], if the strict 2-category itself is "only defined up to [[biequivalence]]," then one is again compelled to use internal Street fibrations, since they are "covariant under biequivalence" of the containing bicategory, whereas Grothendieck fibrations are not.

For example, this is arguably the case in the 2-category [[Topos]], where we have to make the arbitrary choice of whether to define the [[geometric morphism|morphisms]] to be [[left exact functor|left-exact]] left [[adjoint functor|adjoints]] $f^*$, right adjoints $f_*$ having a left-exact left adjoint, or adjoint pairs $(f^*,f_*)$ in which $f^*$ is left exact.  The three choices give three strict 2-categories which are all biequivalent, but not strictly 2-equivalent; thus it is more sensible to consider internal Street fibrations in $Topos$ than strict Grothendieck ones.


## Properties

Since Street fibrations are the "minimal covariant modification" of Grothendieck ones, any property enjoyed by Grothendieck fibrations which is itself covariant under equivalence will also be possessed by Street fibrations.

One thing to note is that in general, when working with Street fibrations, one must always replace [[fibers]] with [[essential fibers]].  In particular, the lifting property of a Street fibration is insufficient for a morphism $u\colon J\to I$ in $B$ to induce a functor $u^*\colon E^I\to E^J$ between strict fibers, but such a functor is induced between essential fibers.  In this way we can reconstruct a [[pseudofunctor]] $B^{op}\to Cat$ from any Street fibration, and show that the [[2-category]] of Street fibrations is equivalent to that of such pseudofunctors (though not, as in the case of Grothendieck fibrations, [[strict 2-equivalence of 2-categories|strictly 2-equivalent]]).

Just as every Grothendieck fibration is a [[strictly exponentiable functor]], i.e. an [[exponential object|exponentiable morphism]] in the [[strict 2-category]] [[Cat]], every Street fibration is a non-strictly exponentiable functor, i.e. an exponentiable morphism in the weak [[2-category]] Cat.


## References

The notion was originally defined in 

* [[Ross Street]], *Fibrations in bicategories*

although there it was given in a very abstract form.  A more explicit form like that given above can be found in

* Ross Street, *Conspectus of variable categories*

Some alternate characterizations, and applications in [[Topos]], are discussed in

* [[Peter Johnstone]], *Fibrations and partial products in a 2-category*.


[[!redirects Street fibration]]
[[!redirects Street fibrations]]
[[!redirects weak fibration]]
[[!redirects weak fibrations]]

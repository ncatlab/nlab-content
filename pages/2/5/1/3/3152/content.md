Let $p\colon E\to B$ be a [[Grothendieck fibration|fibered category]]. A **cleavage** of $p$ is a choice, for each $e\in E$ and $u\colon b\to p(e)$ in $B$, of a single cartesian arrow $f:e'\to e$ such that $p(f) = u$.  A fibered category equipped with a cleavage is said to be **cloven**.  If $f$ is an identity whenever $u$ is, the cleavage is said to be **normal**, and if each composite $f_2 f_1$ is the specified lifting of $u_2 u_1$, the cleavage is said to be a **splitting**.

If we assume the [[axiom of choice]], then every fibered category has a cleavage, and even a normal cleavage (but not neccesarily a splitting).  Given a cleavage of $p$ and an arrow $u:b'\to b$ in $B$, there is a functor $u^*\colon p^{-1}(b)\to p^{-1}(b')$ which to every object $e\in p^{-1}(b)$ assigns the domain of the specified arrow in the cleavage which is above $u$ and whose codomain is $e$.  This correspondence extends to a functor thanks to the universal property of the cartesian arrows.

The functor $u^*$ may be called either the *inverse image functor* along $u$, or the *direct image functor* of $u$, depending on the context; see the remarks on notation at [domain opfibration](http://ncatlab.org/nlab/show/domain+opfibration#notation).  It depends on the choice of cleavage as well as on $u$, although different cleavages produce canonically naturally isomorphic functors.  If one doesn't choose a cleavage, then $u^*$ can still be defined as an [[anafunctor]].

The direct image functors corresponding to varying morphisms in $B$ together form a [[pseudofunctor]].  The inverse [[Grothendieck construction]] produces a cloven fibration from a pseudofunctor, setting up an equivalence of 2-categories.

[[!redirects pseudo-splitting]]
[[!redirects split fibration]]
[[!redirects cloven fibration]]
[[!redirects pseudo-splittings]]
[[!redirects split fibrations]]
[[!redirects cloven fibrations]]
[[!redirects cleavages]]

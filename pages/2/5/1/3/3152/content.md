
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Being a [[Grothendieck fibration]] is a [[property-like structure]] on a [[functor]], like the existence of [[limits]] in a [[category]]: it is defined by the existence of certain [[objects]] (in this case, [[cartesian morphisms]]) which, when they exist, are unique up to unique [[isomorphism]].  Any [[property]]-like [[structure]] can be "algebraicized" by requiring a specific *choice* of the objects that are required to exist; a *cleavage* is this "algebraicization" for the property of being a [[Grothendieck fibration]].

## Definition

Let $p\colon E\to B$ be a functor.  A **cleavage** of $p$ is a choice, for each $e\in E$ and $u\colon b\to p(e)$ in $B$, of a single [[cartesian arrow]] $f:e'\to e$ such that $p(f) = u$.  Evidently if there exists a cleavage for $p$, then $p$ is a [[Grothendieck fibration]].  If $p$ is equipped with a cleavage, it said to be **cloven**.  Conversely, if we assume the [[axiom of choice]], then every fibered category has a cleavage.

If the cartesian arrow $f$ is an identity whenever $u$ is, the cleavage is said to be **normal**, and if each composite $f_2 f_1$ is the specified lifting of $u_2 u_1$, the cleavage is said to be a **splitting**.  Any cleavage can be modified to become normal, but not necessarily to become split.  (Any fibration is, however, *equivalent* to a split fibration.)

## Cloven fibrations vs pseudofunctors

Given a cleavage of $p$ and an arrow $u:b'\to b$ in $B$, there is a functor $u^*\colon p^{-1}(b)\to p^{-1}(b')$ which to every object $e\in p^{-1}(b)$ assigns the domain of the specified arrow in the cleavage which is above $u$ and whose codomain is $e$.  This correspondence extends to a functor, thanks to the universal property of the cartesian arrows.

The functor $u^*$ may be called either the *inverse image functor* along $u$, or the *direct image functor* of $u$, depending on the context; see the remarks on notation at [domain opfibration](http://ncatlab.org/nlab/show/domain+opfibration#notation).  It depends on the choice of cleavage as well as on $u$, although different cleavages produce canonically naturally isomorphic functors.  If one doesn't choose a cleavage, then $u^*$ can still be defined as an [[anafunctor]].

The direct image functors corresponding to varying morphisms in $B$ together form a [[pseudofunctor]] $B^{op}\to Cat$.  The inverse [[Grothendieck construction]] produces a cloven fibration from a pseudofunctor, setting up an equivalence of 2-categories (in fact, a [[strict 2-equivalence of strict 2-categories]]) between cloven fibrations and pseudofunctors $B^{op} \to Cat$.  If we either assume the axiom of choice, or allow the morphisms in [[Cat]] to be anafunctors, then this extends to an equivalence between pseudofunctors and not-necessarily-cloven fibrations.

## Non-strict cleavages

There is a corresponding notion of cleavage for a [[Street fibration]], namely a choice of, for each $e\in E$ and $u\colon b\to p(e)$ in $B$, a cartesian arrow $f:e'\to e$ in $E$ and an isomorphism $v\colon p(e') \xrightarrow{\cong} b$ such that $u\circ v = p(f)$.  Such a cleavage induces, for every $u\colon b'\to b$, a functor between the [[essential fibers]] of $b$ and $b'$, and thereby a pseudofunctor and another equivalence of 2-categories (though not a strict 2-equivalence).

## References

The original reference:

* [[Alexander Grothendieck]], §VI.7 of: _Revêtements Étales et Groupe Fondamental - Séminaire de Géometrie Algébrique du Bois Marie 1960/61_ ([[SGA 1]]) , LNM **224** Springer (1971) &lbrack;updated version with comments by M. Raynaud: [arxiv.0206203](http://arxiv.org/abs/math/0206203)&rbrack;

Review:

* [[Angelo Vistoli]], Def. 3.9 in: *Grothendieck topologies, fibered categories and descent theory*, in: *[[Fundamental algebraic geometry -- Grothendieck's FGA explained]]*, Mathematical Surveys and Monographs **123**, Amer. Math. Soc. (2005) 1-104 &lbrack;[ISBN:978-0-8218-4245-4](https://bookstore.ams.org/surv-123-s), [math.AG/0412512](http://arxiv.org/abs/math/0412512)&rbrack;



[[!redirects pseudo-splitting]]
[[!redirects split fibration]]
[[!redirects cloven fibration]]
[[!redirects split opfibration]]
[[!redirects cloven opfibration]]
[[!redirects pseudo-splittings]]
[[!redirects split fibrations]]
[[!redirects cloven fibrations]]
[[!redirects split opfibrations]]
[[!redirects cloven opfibrations]]
[[!redirects cleavages]]

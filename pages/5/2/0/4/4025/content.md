
# Functionals
* table of contents
{: toc}

## Disambiguation

This is about functionals in the sense of [[higher-order logic]], which is the original sense and which has only that name.  For functionals in the sense of [[functional analysis]], see _[[linear functional]]_; for the relation between these, see under Examples below.  For functionals on [[infinite-dimensional manifolds]], see at _[[nonlinear functional]]_.


## Definition

In a [[type theory]] with [[function types]], given a [[type]] $X$, a __functional__ of base type $X$ is a [[term]] of type $X^{X^X}$ aka $(X \to X) \to X$.  This should be distinguished from (on the one hand) an [[operator]], which is a term of type $(X^X)^{X^X}$ aka $(X \to X) \to (X \to X)$, and (on the other hand) a [[endofunction|function]], which (in this context) is a term of type $X^X$ aka $X \to X$.

More generally, any term whose type has the form $A^{B^C}$ aka $(C \to B) \to A$ may be called a functional, although usually not if any of these types is very trivial (since any type has this form, up to equivalence, if $B,C \coloneqq 1$).

Although one typically interprets type theory within [[set theory]] so that operations between types become [[functions]], one may also use [[partial functions]], which is necessary for many of the examples below.

A functional could also be interpreted within [[category theory]] as a [[simplex|simplicial]] [[2-morphism]] in the [[2-category|2-]][[category of sets]]. 

## Examples

In [[variational calculus]] one studies functions on spaces of [[sections]] of [[jet bundles]] or other [[mapping spaces]].  The notion of [[nonlinear functional]] is an abstraction of this.  For example, such functionals appear in [[physics]] as [[action functionals]].  See [[covariant phase space]] and [[path integral]] for other functionals in physics.

If we interpret $X$ as the [[real line]], then $X^X$ consists of real-valued maps of a real variable, which form a [[vector space]].  The [[linear maps]] from $X^X$ to $X$ are the original [[linear functionals]].  In [[functional analysis]], we now replace $X^X$ with an arbitrary [[topological vector space]] $V$ (originally but no longer necessarily taken to be a [[vector subspace|subspace]] of $X^X$) and consider linear maps from $V$ to $X$ instead; so these linear functionals are actually unstructured operations in a type-theoretic sense.


[[!redirects functional]]
[[!redirects functionals]]

# Weak adjoints

* table of contents
{: toc}

## Idea

A **weak adjoint** is like an [[adjoint functor]] but without the uniqueness of factorizations.

## Definition

Let $G:D\to C$ be a [[functor]].  We say $G$ has a **left weak adjoint** if for each $x\in C$ there exists a morphism $\eta_x:x\to G z$ such that for any morphism $f:x\to G y$ there exists a (not necessarily unique) morphism $g:y\to z$ such that $f = G g \circ\eta_x$.

## Examples

* A [[weak limit]] is a weak right adjoint to a constant-diagram functor.

## Remarks

Of course, if the factorizations $g$ are always unique, this is precisely an ordinary [[left adjoint]].  A weak adjoint can also be regarded as a stronger form of the [[solution set condition]] in which the solution sets are required to be singletons.  The "dual" property, in which the solution sets need not be singletons but the factorizations are unique, is called a [[multi-adjoint]].

[[!redirects weak adjoints]]
[[!redirects weak adjunction]]
[[!redirects weak left adjoint]]
[[!redirects weak left adjoint]]
[[!redirects weak right adjoint]]
[[!redirects weak right adjoint]]
[[!redirects left weak adjoint]]
[[!redirects left weak adjoints]]
[[!redirects right weak adjoint]]
[[!redirects right weak adjoints]]

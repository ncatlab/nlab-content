## Definition

Let $T\colon A\to B$ be a [[functor]] such that $A$ has a [[terminal object]] $1$.  Then $T$ can be factored as the composite
$$ A \overset{T_1}{\to} B/T1 \overset{\Sigma_{T1}}{\to} B.$$
We say that $T$ is a **parametric right adjoint**, or **p.r.a.**, if the functor $T_1$ has a left adjoint.

A [[monad]] is called **p.r.a.** if its functor part is p.r.a. and moreover its unit and multiplication are [[cartesian natural transformation|cartesian]].

## Properties

Since $\Sigma_{T1}$ [[created limit|creates]] [[connected limit|connected limits]], if $T$ is p.r.a. then it [[preserved limit|preserves]] connected limits, and in particular preserves [[pullbacks]].  It follows that any p.r.a. monad is a [[cartesian monad]].

Any [[polynomial functor]] $\Sigma_h \Pi_g f^*$ is p.r.a., since then $T_1$ can be identified with $\Pi_g f^*$, which has the left adjoint $\Sigma_f g^*$.

## Examples

[[!redirects parametric right adjoints]]
[[!redirects p.r.a. functor]]
[[!redirects p.r.a. functors]]
[[!redirects p.r.a. monad]]
[[!redirects p.r.a. monads]]

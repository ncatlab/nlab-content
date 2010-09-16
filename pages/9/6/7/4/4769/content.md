
# Exponential maps
* table of contents
{: toc}

## Idea

The exponential [[function]] of classical [[analysis]],
\[ \label{series} \exp x \coloneqq \sum_{i = 0}^{\infty} \frac{x^i}{i!} ,\]
is the solution of the [[differential equation]]
$$ f' = f $$
with initial value $f(0) = 1$.

This classical function is defined on the [[real line]] (or the [[complex plane]]).  To generalise it to other [[manifolds]], we need two things:

*  By [[dimensionalysis]], the argument of the function should be a [[tangent vector]]; so in the classical function $\mathbb{R} \to \mathbb{R}$, the [[source]] $\mathbb{R}$ is really the [[tangent space]] to the [[target]] $\mathbb{R}$ at the point $\exp 0 = 1$.
*  We need a [[covariant derivative]] to tell us what $f'$ means.

So in the end we have, for any [[point]] $p$ on a [[differentiable manifold]] $M$ with an [[affine connection]] $\Del$, a map $\exp_p\colon T_p M \to M$, which is defined at least on a [[neighbourhood]] of $0$ in the [[tangent space]] $T_p M$.

Note that $p$ here comes from the initial value $\exp_p 0 = p$; we usually take $p = 1$ when we work in a [[Lie group]], but otherwise we are really generalising the classical exponential function $x \mapsto p \exp x$; every solution to $f' = f$ takes this form.

Classically, there are some other functions called 'exponential'; given any nonzero real (or complex) number $b$, the map $x \mapsto b^x$ (or even $x \mapsto p\, b^x$) is also an exponential map.  Using the [[natural logarithm]], we can define $b^x$ in terms of the natural exponential map $\exp$:
$$ b^x \coloneqq \exp (x \ln b) .$$
So while $b$ is traditionally called the 'base', it is really the number $\ln b$ that matters, or even better the operation of multiplication by $\ln b$.  This operation is an [[endomorphism]] of the real line (or complex plane), and every such endomorphism takes this form for some nonzero $b$ (and some branch of the natural logarithm, in the complex case).  So we see that this generalised exponential map is simply the [[composite]] of the natural exponential map after a linear endomorphism.


## Definition

Let $M$ be a [[differentiable manifold]], let $\Del$ be an [[affine connection]] on $M$, and let $p$ be a [[point]] in $M$.  Then by the general theory of [[differential equations]], there is a unique [[maximal partial function|maximally]] defined [[partial function]] $\exp_p$ from the [[tangent space]] $T_p M$ to $M$ such that:

*  $\Del \exp_p = \exp_p$ and
*  $\exp_p(0) = 1$.

This function is the __natural exponential map on $M$ at $p$ relative to $\Del$__.  We have $\exp_p\colon U \to M$, where $U$ is some [[neighbourhood]] of $0$ in $T_p M$.  If $M$ is [[complete manifold|complete]] (relative to $\Del$), then $U$ will be all of $T_p M$.

Given any [[endomorphism]] $\phi\colon T_p M \to T_p M$, we can also consider the __exponential map on $M$ at $p$ relative to $\Del$ with logarithmic base $\phi$__, which is simply $x \mapsto \exp_p \phi(x)$.  We say 'logarithmic base' since a classical exponential function with base $b$ corresponds to an exponential function whose logarithmic base is multiplication by $\ln b$.


## Via geodesics

Recall that a [[geodesic]] is a [[curve]] on a manifold whose [[velocity]] is constant (as measured along that curve relative to a given affine connection).  Working na&#239;vely, we may write
$$ \gamma' = v ,$$
pretend that this is a differential equation for a function $\gamma\colon \mathbb{R} \to \mathbb{R}$, and take the solution
$$ \gamma(t) = p \exp t x ,$$
where $p$ is given by the initial value $\gamma(0) = p$.  We recognise this as being, morally, $\exp_p t x$.  This suggests (although we need more work for a proof) the following result:

Let $M$ be a [[differentiable manifold]], let $\Del$ be an [[affine connection]] on $M$, and let $p$ be a [[point]] in $M$.  Given a [[tangent vector]] $x$ at $p$, there is a unique [[maximal geodesic]] $\gamma$ on $M$ tangent to $x$ at $p$.  If $\gamma(1)$ is defined (which it will be whenever $M$ is [[complete manifold|complete]] and may be in any case), we have $exp_p x = \gamma(1)$.  In any case, we have $\exp_p (t x) = \gamma(t)$ for sufficiently small $t$.


## In Riemannian manifolds

Let $M$ be a [[Riemannian manifold]] (or a [[pseudo-Riemannian manifold]]) and let $p$ be a point in $M$.  Then $M$ may be equipped with the [[Levi-Civita connection]] $\Del_{lc}$, so we define the __natural Riemannian exponential map on $M$ at $p$__ to be the natural exponential map on $M$ at $p$ relative to $\Del_{lc}$.


## In Lie groups

Let $M$ be [[Lie group]] and let $\mathfrak{g}$ be its [[Lie algebra]] $T_1 M$, the tangent space to the [[identity element]] $1$.  Then $M$ may be equipped with the canonical left-invariant connection $\Del_l$ or the canonical right-invariant connection $\Del_r$.  It turns out that the natural Riemannian exponential maps on $M$ at $1$ relative to $\Del_l$ and $\Del_r$ are the same; we define this to be the __natural Lie exponential map on $M$ at the identity__, denoted simply $\exp$.  Several nice properties follow:

*  $\exp$ is defined on all of $\mathfrak{g}$.
*  $\exp$ is a [[smooth map|smooth]] [[homomorphism]] to $G$ from the underlying additive Lie group of $\mathfrak{g}$.
*  $\exp$ is [[surjection|surjective]] (a [[regular epimorphism]]) if $G$ is [[connected space|connected]] and [[compact space|compact]] (and also in some other situations, such as the classical cases where $G$ is $]0,\infty[$ or $\mathbb{C} \setminus \{0\}$).
*  If $G$ is [[compact space|compact]], then it may be equipped with a [[Riemannian metric]]; then the Lie exponential map is the same as the Riemannian exponential map at $1$.
*  If $G$ is a [[matrix Lie group]], then $\exp$ is given by the classical series formula (eq:series).


## Logarithms

A __[[logarithm]]__ is a [[partial section]] of an exponential map.


[[!redirects exponential map]]
[[!redirects exponential maps]]
[[!redirects exponential function]]
[[!redirects exponential functions]]

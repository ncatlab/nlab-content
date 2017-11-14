
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Integration theory
+-- {: .hide}
[[!include integration theory - contents]]
=--
=--
=--

# Line integrals
* table of contents
{: toc}

## Idea

A _line integral_ is an [[integral]] along a [[curve]].  These are sometimes called _path integrals_ (not to be confused with the [[path integral]] in [[quantum physics]], which is integration over a space of curves rather than along a curve in some space) and _[[contour integrals]]_ (especially in [[complex analysis]]).

By the modern understanding of the [[integration of differential forms]], one integrates [[differential 1-forms]] ([[cotangent vector fields]]) along [[orientation|oriented]] [[curves]], and so this would be the natural way to understand a line integral.  However, there are several slightly different line integrals, and not all of them are reducible to integration of $1$-forms along oriented curves.  Sometimes we have to fall back on more basic notions, ultimately the integration of [[pseudoform|pseudo]]-$1$-forms on a $1$-dimensional space.


## Definitions

Here we assume familiarity with integration of differential forms and pseudoforms, defining in terms of them the various classical notions of line integral.

In each case, the classical notation (developed before the rigorous treatment of analysis in the 19th century) is not taken literally by the classical definition (developed after the rigorous treatment and still found in calculus texts), and this definition is accompanied by a [[parametrization|reparametrisation]] theorem.  We would like to make sense of the classical notation and eliminate the reparametrisation theorems (or at least make them all special cases of [a general theorem to be proved once for all](differential+form#IntegrationTheorem)) using differential forms.  Often we find that we can relax some of the restrictions in the classical definition as well.


### Line integral of a vector field

Classically, we have a [[Cartesian space]] $X$, a [[continuous map]] $\vec{F}\colon X \to X$, and a [[continuously differentiable map]] $C\colon [a,b] \to X$; the __line integral__ of $\vec{F}$ along $C$ is defined as
$$ \int_C \vec{F} \cdot \mathrm{d}\vec{r} \coloneqq \int_a^b \vec{F}(C(t)) \cdot C'(t) \,\mathrm{d}t ,$$
where the integral on the right is a [[Riemann integral]] and $C'$ is the [[derivative]] of $C$ componentwise.  If $\phi\colon [e,f] \to [a,b]$ is a continuously differentiable [[monotone function|increasing]] [[bijection]], then
$$ \int_{C \circ \phi} \vec{F} \cdot \mathrm{d}\vec{r} = \int_C \vec{F} \cdot \mathrm{d}\vec{r} ,$$
the reparametrisation theorem.

We can start to justify the classical notation by interpreting $\vec{r}$ as the same map $[a,b] \to X$ as $C$; then we have
$$ \int_C \vec{F} \cdot \mathrm{d}\vec{r} \coloneqq \int_a^b \vec{F}(\vec{r}(t)) \cdot \vec{r}'(t) \,\mathrm{d}t ,$$
in which case the classical notation simply seems to be suppressing some of the notation in the formal definition on the right.  In particular, we interpret $\mathrm{d}\vec{r}$ as meaning $\vec{r}'(t) \,\mathrm{d}t$.

But this suggests that we should really be looking at differential forms.  Since $X$ is a Cartesian space, we may identify it with any of its [[tangent spaces]] and so identify $\vec{F}$ with a [[tangent vector field]] on $X$, or equivalenty a vector-valued $0$-form.  Since $\vec{r}$ is only serving to parametrise the curve, it should be interpreted as something trivial, in this case the [[identity map]] on $X$, also viewed as a vector-valued $0$-form.  Then $\mathrm{d}\vec{r}$ is a vector-valued $1$-form (which we can do since a Cartesian space has a trivial [[connection]]), and $\vec{F} \cdot \mathrm{d}\vec{r}$ is an ordinary $1$-form.  Finally, since the curve $C$ is given up to an increasing reparametrisation, it is an [[orientation|oriented]] $1$-submanifold of $X$.  Now we may interpret the notation
$$ \int_C \vec{F} \cdot \mathrm{d}\vec{r} $$
literally as the integral of a $1$-form.  It is now no longer necessary that $C$ be given by a continuously differentiable parametrisation; the vector-valued $0$-form $\vec{r}$ is continuously differentiable regardless, and so we only need $C$ to be a [[rectifiable curve]] (although it is a theorem that such a curve must have a parametrisation ---by [[arclength]] if nothing else--- that is continuously differentiable [[almost everywhere]], so that the classical definition still covers this using a [[Riemann integral]]).

However, this operation from $\vec{F}$ to $\vec{F} \cdot \mathrm{d}\vec{r}$ is something more fundamental in differential geometry; in fact, $\vec{F} \cdot \mathrm{d}\vec{r}$ is simply $\vec{F}^\flat$, the [[cotangent vector field]] that corresponds to the tangent vector field $\vec{F}$.  Understanding this, we wish to generalise $X$ to any (pseudo)-[[Riemannian manifold]].  In this case, we cannot interpret $\vec{r}$ literally, but we may still interpret $\mathrm{d}\vec{r}$ as a vector-valued $1$-form, indeed as the tautological one that (viewing a $1$-form as an operation on vector fields) is the [[identity map]] on vector fields.  With this understanding, the classical notation still makes sense, although it is probably easier to write
$$ \int_C \vec{F} \cdot \mathrm{d}\vec{r} = \int_C \vec{F}^\flat $$
as the most general definition of the line integral of a vector field along an oriented curve in a (pseudo)-Riemannian manifold.


### Line integral of a scalar field

Classically, we again have a [[Cartesian space]] $X$, now a [[continuous map]] $f$ from $X$ to $\mathbb{R}$ or $\mathbb{C}$, and again a [[continuously differentiable map]] $C\colon [a,b] \to X$; the __line integral__ of $f$ along $C$ is defined as
$$ \int_C f \mathrm{d}s \coloneqq \int_a^b f(C(t)) {\|C'(t)\|} \,\mathrm{d}t ,$$
where again the integral on the right is a [[Riemann integral]] and $C'$ is the [[derivative]] of $C$ componentwise.  If $\phi\colon [e,f] \to [a,b]$ is a continuously differentiable [[bijection]] (whether increasing *or* decreasing), then
$$ \int_{C \circ \phi} f \mathrm{d}s = \int_C f \mathrm{d}s ,$$
the reparametrisation theorem.

We cannot interpret $\mathrm{d}s$ as the differential of anything; rather, $\mathrm{d}s$ is the magnitude of the line integral element $\mathrm{d}\vec{r}$ from the previous section. In particular, identifying $\vec{r}$ with $C$ again, we have
$$ \int_C f \mathrm{d}s \coloneqq \int_a^b f(\vec{r}(t)) {\|\vec{r}'(t)\|} \,\mathrm{d}t ,$$
so $\mathrm{d}s$ seems to mean ${\|\vec{r}'(t)\|} \,\mathrm{d}t$.  Using the standard orientation on $[a,b]$ to change the $1$-form $\mathrm{d}t$ to the pseudo-$1$-form ${|\mathrm{d}t|}$, this is consistent with $\mathrm{d}s = {\|\mathrm{d}\vec{r}\|}$.

But for this to really make sense, we have to see what kind of object $\mathrm{d}s$ is on $X$.  It is neither a $1$-form (which can be integrated along an oriented curve) nor a pseudo-$1$-form (which can be integrated along a pseudo-oriented curve, that is a transversely oriented curve); it is instead an *[[absolute differential form|absolute]]* $1$-form, which can be integrated along an *unoriented* curve.  If we interpret $\mathrm{d}\vec{r}$ as the canonical vector-valued $1$-form again, then we can take its magnitude to get a positive semidefinite (nonnegative-scalar-valued, and in this case actually definite) absolute $1$-form, so $\mathrm{d}s = {\|\mathrm{d}\vec{r}\|}$ is literally true.

It would be nice to have notation without fake differentials and with the one piece of structure that actually plays a role: the metric.  If we multiply two $1$-forms using the [[symmetric product]] (instead of the [[exterior product]] as usual for differential forms), then we get a symmetric [[bilinear form]], and in this way the (symmetric) square of the arclength element $\mathrm{d}s$ is the metric $g$.  Since $\mathrm{d}s$ is positive, we can reasonably call it the *principal* [[square root]] of $g$.  Thus,
$$ \int_C f \mathrm{d}s = \int_C f \sqrt{g} $$
defines the line integral of a scalar field along an unoriented curve in a Riemannian manifold.

On a *pseudo*-Riemannian manifold, $g$ itself may not be positive and so may not have a square root.  In that case, we can take the absolute value of $g$ first and use
$$ \int_C f \mathrm{d}s = \int_C f \sqrt{|g|} ,$$
although this is most intuitive for curves that are consistently [[timelike curve|timelike]] or [[spacelike curve|spacelike]].  It\'s also possible to keep the previous formula and allow one of these two types of curve to have [[purely imaginary number|imaginary]] arclength; which one depends on conventions.  In any case, a line integral along a [[lightlike curve]] is zero.


### Contour integral of a complex function

Classically, we have the [[complex plane]] $\mathbb{C}$, a [[continuous map]] $f\colon \mathbb{C} \to \mathbb{C}$, and a [[continuously differentiable map]] $C\colon [a,b] \to \mathbb{C}$; the __[[contour integral]]__ (or __line integral__ again) of $f$ along $C$ is defined as
$$ \int_C f \mathrm{d}z \coloneqq \int_a^b f(C(t)) C'(t) \,\mathrm{d}t ,$$
where the integral on the right is a [[Riemann integral]] and $C'$ is the [[derivative]] of $C$.  If $\phi\colon [e,f] \to [a,b]$ is a continuously differentiable [[monotone function|increasing]] [[bijection]], then
$$ \int_{C \circ \phi} f \mathrm{d}z = \int_C f \mathrm{d}z ,$$
the reparametrisation theorem.

We start to justify the classical notation by interpreting $z$ as the same map $[a,b] \to \mathbb{C}$ as $C$; then we have
$$ \int_C f \mathrm{d}z \coloneqq \int_a^b f(z(t)) z'(t) \,\mathrm{d}t ,$$
in which case the classical notation seems again to be suppressing some of the notation in the formal definition.  In particular, $\mathrm{d}z$ is interpreted as $z'(t) \,\mathrm{d}t$.

But again, we should really be looking at differential forms.  We may identify the space $\mathbb{C}$ with the [[scalar field]] and so identify $f$ with a [[scalar field]] on $\mathbb{C}$, or equivalenty a $0$-form.  Since $z$ is only serving to parametrise the curve, it should be interpreted as the [[identity map]] on $\mathbb{C}$, also viewed as a $0$-form.  Then $\mathrm{d}z$ is a $1$-form, and $f \mathrm{d}z$ is a $1$-form.  Finally, since the curve $C$ is given up to an increasing reparametrisation, it is an [[orientation|oriented]] $1$-submanifold of $X$.  Now we may interpet the notation
$$ \int_C f \mathrm{d}z $$
literally as the integral of a $1$-form.  It is now no longer necessary that $C$ be given by a continuously differentiable parametrisation; the vector-valued $0$-form $z$ is continuously differentiable regardless, and so we only need $C$ to be a [[rectifiable curve]] (although it is a theorem that such a curve must have a continuously differentiable parametrisation after all).


### Absolute contour integral of a complex function

Classically, we have the [[complex plane]] $\mathbb{C}$, a [[continuous map]] $f\colon \mathbb{C} \to \mathbb{C}$, and a [[continuously differentiable map]] $C\colon [a,b] \to \mathbb{C}$; the __absolute contour integral__ (or whatever one calls it) of $f$ along $C$ is defined as
$$ \int_C f {|\mathrm{d}z|} \coloneqq \int_a^b f(C(t)) {|C'(t)|} \,\mathrm{d}t ,$$
where the integral on the right is a [[Riemann integral]] and $C'$ is the [[derivative]] of $C$.  If $\phi\colon [e,f] \to [a,b]$ is a continuously differentiable [[bijection]] (whether increasing or decreasing), then
$$ \int_{C \circ \phi} f {|\mathrm{d}z|} = \int_C f {|\mathrm{d}z|} ,$$
the reparametrisation theorem.

As before, if $z$ is interpreted as the same map $[a,b] \to \mathbb{C}$ as $C$; then we have
$$ \int_C f {|\mathrm{d}z|} \coloneqq \int_a^b f(z(t)) {|z'(t)|} \,\mathrm{d}t ,$$
so ${|\mathrm{d}z|}$ seems to mean ${|z'(t)|} \,\mathrm{d}t$.  As before, if we use the standard orientation on $[a,b]$ to change the $1$-form $\mathrm{d}t$ to the pseudo-$1$-form ${|\mathrm{d}t|}$, then ${|\mathrm{d}z|}$ is the absolute value of $\mathrm{d}z$ from before.

Of course, we should really be looking at differential forms.  Again, $f$ is a [[scalar field]] on $\mathbb{C}$, or equivalenty a $0$-form.  Again $z$ is the [[identity map]] on $\mathbb{C}$, viewed as a $0$-form.  Then $\mathrm{d}z$ is a $1$-form, its absolute value ${|\mathrm{d}z|}$ is a (positive definite) [[absolute form|absolute]] $1$-form, and $f {|\mathrm{d}z|}$ is a (more general) absolute $1$-form.  Since $C$ is given up to an arbitrary reparametrisation, it is an unoriented $1$-submanifold of $X$, which is just what we need for an absolute $1$-form.  Now we may interpet the notation
$$ \int_C f {|\mathrm{d}z|} $$
literally as the integral of an absolute $1$-form.

This is actually a special case of the line integral of a scalar field, since
$$ {|\mathrm{d}z|} = {|\mathrm{d}(x + \mathrm{i}y)|} = {|\mathrm{d}x + \mathrm{i} \,\mathrm{d}y|} = \sqrt{(\mathrm{d}x)^2 + (\mathrm{d}y)^2} = \sqrt{g} = \mathrm{d}s ,$$
since $\mathrm{d}x^2 + \mathrm{d}y^2$ is the standard metric on $\mathbb{C}$.


## Properties

### Cauchy's theorems

* [[Cauchy integral formula]]

* [[Cauchy integral theorem]]

## References

Here are a couple of old Usenet posts that explain how line integrals of scalar fields should be viewed in terms of forms and pseudoforms.

* [first](https://groups.google.com/group/sci.physics.research/msg/2774cbbc982e200e?dmode=source)
* [second](https://groups.google.com/group/sci.physics.research/msg/424da828e75b6b90?dmode=source)

These are obsolete with the concept of [[absolute forms]], but they contain more explicit calculations.

See also


* Wikipedia, _[Line integral](https://en.wikipedia.org/wiki/Line_integral)_


[[!redirects line integral]]
[[!redirects line integrals]]
[[!redirects contour integral]]
[[!redirects contour integrals]]
[[!redirects contour integration]]

[[!redirects contour integration]]
[[!redirects contour integrations]]


# Indefinite integrals
* table of contents
{: toc}

## Idea

An indefinite integral is something less definite than a [[definite integral]].  Whereas a definite integral is typically some kind of [[number]] or other concrete quantity, an indefinite integral is typically another variable quantity of the same type as the integrand.

The term 'indefinite integral' is itself rather indefinite, having been used for a variety of slightly different concepts.  Both _semidefinite integrals_ and _antiderivatives_ are more precise versions of indefinite integrals.  The [[fundamental theorem of calculus]] is basically the [[theorem]] that these different kinds of indefinite integral are essentially the same thing.


## Definitions and notation

To begin with, we will discuss the [[integration]] of [[real number|real]]-valued [[functions]] on the [[real line]], but much of this can be generalized to other contexts.  So let $f$ be a [[partial function]] from $\mathbb{R}$ to $\mathbb{R}$; typically, the [[domain]] of $f$ will be an [[interval]], but we do not require this.

+-- {: .num_defn #semi}
###### Definition

If $a$ is a [[real number]] (usually in the domain of $f$, or at least in the domain\'s [[topological closure|closure]]), then the __semidefinite integral__ of $f$ from $a$ (or with __initial point__ $a$) is the function
$$ x \mapsto \int_a^x f(t) \,\mathrm{d}t .$$
(If $x \lt a$, then we must define $\int_a^x$ as $-\int_x^a$.)
=--

The semidefinite integral is defined in terms of the definite integral.  We can put names such as 'Riemann' and 'Lebesgue' between 'semidefinite' and 'integral' to specify a particular kind of definite integral to be used.  Note that the domain of the semidefinite integral is an interval containing $a$ and contained in the domain of $f$ (or at least in its closure if we allow [[improper integral]]s or integrating [[almost functions]]).  If we start by defining $f$ as a [[locally integrable function]] on a closed interval $I$ containing $a$, then the semidefinite integral will also have $I$ as its domain.

The value at $x$ of the semidefinite integral from $a$ may be denoted
$$ \int_a f(x) \,\mathrm{d}x $$
for short.  Notice that this notation has no dummy variable; we only need to introduce the dummy variable $t$ to unfold the definition.  (Indeed, some writers will abuse notation, writing $\int_a^x f(x) \,\mathrm{d}x$ for the semidefinite integral.)  But as in $\mathrm{d}y/\mathrm{d}x$, the $x$ here is not a [[free variable]] either, since we cannot freely use substitution; it has to be viewed as [[variable quantity]] instead.  Rather, if you want to evaluate $\int_a f(x) \,\mathrm{d}x$ when $x$ is some number $b$, then the notation for this is $(\int_a f(x) \,\mathrm{d}x)|_{x=b}$ following the general logic of variable quantities; but unwrapping the definition of semidefinite integral, this can also be written as $\int_a^b f(x) \,\mathrm{d}x$.  (In each of these, $x$ has now become a dummy variable.)

+-- {: .num_defn #semiIV}
###### Definition

If $a$ and $C$ are real numbers (with $a$ in the domain of $f$ or its closure), then the __indefinite integral__ of $f$ from $a$ with __initial value__ $C$ is the function
$$ x \mapsto C + \int_a^x f(t) \,\mathrm{d}t .$$
We may write this value as $C + \int_a f(x) \,\mathrm{d}x$ for short.
=--

This is only one of the meanings of 'indefinite integral', but it is the only one that doesn\'t have alternative unambiguous terminology.  Note that $C$ is the value of the indefinite integral at $a$; thus, $C$ is the initial value if $a$ is the initial point.  But for authors who use this concept, there is often no need to mention either $a$ or $C$ (and hence no terminology needed for them), because they are interested only in whether some other function $F$ is an indefinite integral of $f$, where $f$ is a locally integrable function on some closed interval.

+-- {: .num_defn #antider}
###### Definition

If $F$ is a partial function from $\mathbb{R}$ to $\mathbb{R}$, then $F$ is an __antiderivative__ of $f$ (or an __antidifferential__ of $f \,\mathrm{d}x$) if $f$ is the [[derivative]] of $F$ on its domain:
$$ \forall\, x \in \dom F,\; f(x) = F'(x) .$$
A posteriori, $F$ must be [[differentiable function|differentiable]].
=--

This is the usual meaning of 'indefinite integral' in modern Calculus textbooks using the [[Riemann integral]], especially when the domain of $f$ is an interval.

+-- {: .num_defn #almostantider}
###### Definition

If $F$ is a Lebesgue-measurable partial [[almost function]] from $\mathbb{R}$ to $\mathbb{R}$, then $F$ is an __almost antiderivative__ of $f$ if $f$ is the derivative of $F$ [[almost everywhere]]:
$$ \operatorname{ess}\forall\, x \in \dom F,\; f(x) = F'(x) .$$
We are especially interested in the case where $F$ is [[absolutely continuous function|absolutely continuous]].
=--

This is not standard terminology, but it fits in well with other 'almost' terminology in [[measure theory]].  This is a common meaning of 'indefinite integral' when using the [[Lebesgue integral]].


## Properties

The main property linking the different kinds of indefinite integral is the _[[fundamental theorem of calculus]]_ (FTC).  For various definitions of integral, one can prove that every semidefinite integral, or more generally any indefinite integral in the sense of Definition \ref{semiIV}, is an antiderivative; and that every antiderivative, or more generally every almost antiderivative, is an indefinite integral; possibly with technical conditions (depending on the type of integral concerned) such as differentiability or absolute continuity.  See that article for details.

Indefinite integrals provide solutions to [[differential equations]].  Of course, the definition of an antiderivative is that it is the solution to a particularly simple differential equation.  Employing the FTC, we see that the indefinite integrals are the solutions to the corresponding initial-value problems.  Specifically, the solution to
$$ \frac{\mathrm{d}y}{\mathrm{d}x} = f(x),\; y|_{x=a} = C $$
is the indefinite integral of $f$ with initial point $a$ and initial value $C$:
$$ y = C + \int_a f(x) \,\mathrm{d}x .$$
Some more general initial-value problems can be solved similarly; for example, the implicit solution to the separable IVP
$$ g(y) \frac{\mathrm{d}y}{\mathrm{d}x} = f(x),\; y|_{x=a} = C $$
is
$$ \int_C g(y) \,\mathrm{d}y = \int_a f(x) \,\mathrm{d}x .$$
Similarly, the solution to the linear IVP
$$ \frac{\mathrm{d}y}{\mathrm{d}x} + P(x) \,y = Q(x),\; y|_{x=a} = C $$
is
$$ y = \frac{C + \int_a Q(x) \,\mu(x) \,\mathrm{d}x}{\mu(x)} ,$$
where $\mu(x) = \exp \int_a P(x) \,\mathrm{d}x$.


## Generalizations

### In cartesian spaces

When $\omega$ is an exterior $1$-form on a subspace $S$ of the [[cartesian space]] $\mathbb{R}^n$, then we can define an antiderivative (or antidifferential) of $\omega$ to be any real-valued function $f$ on $S$ such that $\mathrm{d}f = \omega$.  Then when $P$ is a point in $S$ (or perhaps its closure), we can define the value of the semidefinite integral of $\omega$ with initial point $P$ to be the integral of $\omega$ along a straight line segment from $P$; the domain is a [[star-convex set]] radiating from $P$ and contained in (the closure of) $S$.  If we define an indefinite integral as a semidefinite integral plus a constant initial value, then every antiderivative of $\omega$ on a star-convex set is an indefinite integral.  Conversely, every indefinite integral is an antiderivative if $\omega$ is closed.  If $\omega$ is not closed, then it still has indefinite integrals (as long as it\'s continuous or otherwise locally integrable), but these are no longer antiderivatives (which non-closed forms never have).

This can perhaps be generalized to [[Riemannian manifolds]] by considering integrals along [[geodesics]]; although the geodesic between two points is not always unique (even when it exists), it is unique on a sufficiently small (and often quite large) neighbourhood.  (For example, on a [[sphere]], as long as $\omega$ is integrable, we can define the indefinite integral this way at every point except the one directly opposite the initial point.)

However, this straight-line definition seems rather artificial, and it might be best to use the more notion of semidefinite integral below, applicable only to closed forms but on more general manifolds.


### On manifolds

We can generalize to [[exterior differential forms]] on [[differentiable manifolds]], generalizing the FTC to the [[Stokes theorem]].  It\'s clear what an antiderivative is in this context: $\alpha$ is an __exterior antiderivative__ of $\omega$ iff $\omega$ is the [[exterior derivative]] of $\alpha$.  On a [[smooth manifold]], we know what 'almost' means and so can also define exterior almost antiderivatives.

If $\omega$ is a $1$-form on any differentiable manifold and $P$ is a point in its domain, then the semidefinite integral of $\omega$ with initial point $P$ is defined at another point $Q$ iff the integral of $\omega$ is the same along any path from $P$ to $Q$ (and then that integral is the value).  We can define an indefinite integral by adding a constant initial value.  Then every antiderivative on a [[path-connected space|path-connected]] domain is an indefinite integral, and conversely every indefinite integral is an antiderivative.  By definition, $\omega$ is exact iff an antiderivative exists, and therefore iff an indefinite integral exists on each [[path-connected component]].  Similarly, $\omega$ is closed iff it has an indefinite integral on a neighbourhood of each point; if the domain of $\omega$ is [[simply-connected space|simply connected]], then the indefinite integral can be extended to the entire domain.

It remains to consider a good notion of semidefinite and indefinite integrals for higher-rank forms.


### In algebraic limit fields

In an [[algebraic limit field]] $F$, the notion of a derivative is well defined and is represented by the [[Newton-Leibniz operator]] $\tilde{D}$. Given a [[subset]] $S \subseteq F$, and a function $f:S \to F$, the set of antiderivatives of $f$ is the [[fiber]] of the [[Newton-Leibniz operator]] at $f$:

$$\{g \in D^1(S, F) \vert \tilde{D}(g) = f\}$$

An __antiderivative__ is an element of the above subset. 


## See also

* [[differentiable function]]
* [[integrable function]]


[[!redirects indefinite integral]]
[[!redirects indefinite integrals]]
[[!redirects indefinite integration]]
[[!redirects indefinite integrations]]

[[!redirects semidefinite integral]]
[[!redirects semidefinite integrals]]
[[!redirects semidefinite integration]]
[[!redirects semidefinite integrations]]

[[!redirects antiderivative]]
[[!redirects antiderivatives]]
[[!redirects antidifferential]]
[[!redirects antidifferentials]]
[[!redirects antidifferentiation]]
[[!redirects antidifferentiations]]

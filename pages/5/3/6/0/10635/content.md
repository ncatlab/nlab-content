
# The fundamental theorem of calculus
* table of contents
{: toc}

## Idea

The fundamental theorem of the [[infinitesimal calculus]] (FTC) states that the [[antiderivatives]] and [[indefinite integrals]] of a [[function]] (typically a [[real number|real]]-valued function on a closed [[interval]] in the [[real line]]) are the same.  It is now such a truism that calculus textbooks tend to use 'indefinite integral' to simply mean an antiderivative, but there is a different concept, definable from the [[definite integral]] and sometimes called the *semidefinite* integral, that is really in play here.

The FTC is usually split into two parts.  The first part (sometimes called the second part) states that every indefinite integral is an antiderivative.  The second part (sometimes called the first part) states that every antiderivative is an indefinite integral.  Somewhere in here (usually in the first part) we also want to state that such antiderivatives and indefinite integrals actually exist.  Their uniqueness (such as it is) may also be included.

The second part is a low-dimensional version of the [[Stokes theorem]].

The FTC may or may not actually be true, depending on what class of functions is considered and what notions of [[derivative]] and [[integral]] are used.


## Statements

Let $f\colon [a, b] \to \mathbb{R}$ be a [[function]].  Recall that an __antiderivative__ of $f$ is a solution $F$ to the [[differential equation]]
$$ F'(x) = f(x) .$$
Also recall (or learn) than an __indefinite integral__ of $f$ is any function $F$ of the form
$$ F(x) = \int_a^x f(t) \,\mathrm{d}t + C $$
for a real constant $C$.

+-- {: .un_theorem #FTC}
###### Theorems (Fundamental Theorem of Calculus)

Suppose that $F$ and $f$ are appropriate functions, and use an appropriate notion of derivative and integral.  Then:

1. First part: If $F$ is an indefinite integral of $f$, then $F$ is an antiderivative of $f$.
2. Second part: If $F$ is an antiderivative of $f$, then $F$ is an indefinite integral of $f$.
3. Existence: $f$ has an indefinite integral / antiderivative.
4. Uniqueness: If $F_1$ and $F_2$ are antiderivatives of $f$, then $F_1 - F_2$ is a [[constant function]].
=--

This holds under any of the following conditions:

1. $F$ is [[continuously differentiable function|continuously differentiable]], $f$ is [[continuous function|continuous]], differentiation is pointwise, and integration is the [[Riemann integral]].
2. $F$ is [[absolutely continuous function|absolutely continuous]], $f$ is [[integrable function|integrable]], differentiation is [[almost everywhere]], and integration is the [[Lebesgue integral]].
3. In pointwise [[constructive mathematics]] with the [[fan theorem]], we may proceed as in (1).
4. In pointwise constructive mathematics with [[countable choice]], $F$ is uniformly continuously differentiable, $f$ is [[uniformly continuous function|uniformly continuous]], differentiation is uniform differentiability, and integration is the [[Riemann integral]].
5. In constructive [[locale theory]], we may proceed as in (1) if the 'functions' involved are locale-theoretic [[continuous maps]] rather than set-theoretic functions.
6. In [[synthetic differential geometry]], $F$ and $f$ are [[smooth map|smooth]], differentiation is axiomatic, and integration is given by the [[integration axiom]].

One may rephrase the first part in various ways as follows.  First, simply incorporating the definitions of 'indefinite integral' and 'antiderivative', we have
$$ \frac{\mathrm{d}}{\mathrm{d}x} \left(\int_a^x f(t) \,\mathrm{d}t + C\right) = f(x) .$$
Taking for granted that adding a constant to a function leaves its derivative unchanged, this simplifies to
$$ \frac{\mathrm{d}}{\mathrm{d}x} \left(\int_a^x f(t) \,\mathrm{d}t\right) = f(x) .$$
When combined with the [[chain rule]], this generalizes to
$$ \frac{\mathrm{d}}{\mathrm{d}x} \left(\int_a^{q(x)} f(t) \,\mathrm{d}t\right) = f(q(x)) q'(x).$$
Taking for granted that $\int_u^v = \int_a^v - \int_a^u$, this generalizes to
$$ \frac{\mathrm{d}}{\mathrm{d}x} \left(\int_{p(x)}^{q(x)} f(t) \,\mathrm{d}t\right) = f(q(x)) q'(x) - f(p(x)) p'(x).$$
Writing $u$ for $p(x)$ and $v$ for $q(x)$ and multiplying both sides by $\mathrm{d}x$, we get the [[differential]] form
$$ \mathrm{d}\left(\int_u^v f(t) \,\mathrm{d}t\right) = f(v) \,\mathrm{d}v - f(u) \,\mathrm{d}u .$$
In other words, the differential and definite integral operators cancel upon performing the [[substitution]] directed by the limits of the definite integral.

One may rephrase the second part in various ways as follows.  First, simply incorporating the definitions of 'indefinite integral' and 'antiderivative', we have
$$ \int_a^x F'(t) \,\mathrm{d}t + C = F(x) $$
for some constant $C$.  Taking for granted that $\int_a^a = 0$, we see that $C = F(a)$, so
$$ F(x) = F(a) + \int_a^x F'(t) \,\mathrm{d}t .$$
It is sufficient to consider the special case where $x = b$:
$$ \int_a^b F'(t) \,\mathrm{d}t = F(b) - F(a) .$$
This can also be written
$$ \int_a^b \mathrm{d}F(t) = F(b) - F(a) $$
to match the last version of the first part; again, the differential and definite integral operators cancel (but now in the opposite order) upon performing the substitution directed by the limits of the definite integral.


## Proofs

If convenient, one may prove the theorem first for the [[unit interval]] $[0, 1]$. By applying a suitable [[affine transformation]], we can deduce the corresponding result for each interval $[a, b]$ where $a$ and $b$ are real numbers with $a \leq b$.

In [[classical mathematics]] and pointwise constructive mathematics, existence of definite integrals must be proved first; existence of indefinite integrals follows.  We can then prove that every indefinite integral is an antiderivative by applying the [[mean value theorem]].  Uniqueness of antiderivatives has a simple direct proof; since at least one antiderivative is an indefinite integral, this shows that every antiderivative is an indefinite integral.  Of course, we have existence of an antiderivative, so now everything is proved.

In the locale-theoretic approach, we essentially *define* an antiderivative to be an indefinite integral.  Formally, the data in a [[continuously differentiable map]] on $[a,b]$ consists of a [[continuous map]] (its derivative) and a real number (its value at $a$).  We must prove the existence of indefinite integrals directly; a definite integral up to each point is not sufficient.  Then there is nothing more to prove (but one might want to prove that differentiation has its usual properties).

Conversely, in synthetic differential geometry, we essentially define an indefinite integral to be an antiderivative.  We must prove uniqueness of antiderivatives; but their existence is given by an [[axiom]], the [[integration axiom]], and then there is nothing more to prove.  Sometimes one studies versions of SDG without this axiom; then there is no FTC (and indeed no integrals).


## Integral formula for antiderivative

In the literature, the first part of the FTC is sometimes stated as merely existence of an antiderivative.  The purpose of this section is to show, independent of foundations, that the second part gives the integral formula for the antiderivative as an indefinite integral.

+-- {: .proof}
###### Proof

Suppose $x$ is in $[0, 1]$. By assumption, there is $F$ such that $F' = f$. By the other part of the fundamental theorem, we have $\int_0^x F'(t) \, {\mathrm{d}}t = F(x) - F(0)$. Thus, $\int_0^x f(t) \, {\mathrm{d}}t = F(x) - F(0)$. Differentiating gives the required result.  
=--


## References

* Wikipedia, _[Fundamental theorem of calculus](http://en.wikipedia.org/wiki/Fundamental_theorem_of_calculus)_

* [[Steve Vickers]], *The Fundamental Theorem of Calculus point-free, with applications to exponentials and logarithms*, ([arXiv:2312.05228](https://arxiv.org/abs/2312.05228))

* [[Steve Vickers]], *The Fundamental Theorem of Calculus: point-free*, talk at the [[Topos Institute Colloquium]], 30 May 2024 ([video](https://www.youtube.com/watch?v=L6LPEFteLts), [slides](https://topos.site/events/topos-colloquium/slides/2024-05-30.pdf))

[[!redirects fundamental theorem of calculus]]
[[!redirects fundamental theorems of calculus]]
[[!redirects fundamental theorem of infinitesimal calculus]]
[[!redirects fundamental theorems of infinitesimal calculus]]
[[!redirects fundamental theorem of differential calculus]]
[[!redirects fundamental theorems of differential calculus]]
[[!redirects fundamental theorem of integral calculus]]
[[!redirects fundamental theorems of integral calculus]]
[[!redirects Fundamental Theorem of Calculus]]
[[!redirects FTC]]

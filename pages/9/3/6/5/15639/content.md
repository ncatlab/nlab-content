
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The fundamental example of [[theta functions]] is the _Jacobi theta function_ given by

$$
  \vartheta(z,\tau)
  =
  \underoverset{n = - \infty}{\infty}{\sum}
   \exp(\pi i n^2 \tau + 2\pi i n z)
 \,.
$$

As a variable of two arguments, this is actually a _[[Jacobi form]]_. These are the local [[coordinate]] expressions of the the [[covariant derivative|covariantly constant]] [[sections]] of the [[Hitchin connection]] (for [[circle group|circle]] [[gauge group]]) on the [[moduli space of elliptic curves]] ([Hitchin 90, remark 4.12](#Hitchin90)). See there for more and see at _[[theta function]]_ for the general idea.

At $z =0$ the function

$$
  \vartheta(0,\tau)
  =
  \underoverset{n = - \infty}{\infty}{\sum}
   \exp(\pi i n^2 \tau)
 \,.
$$

is what in [[number theory]] is often just called "the theta function". This is the one whose [[Mellin transform]] is the [[Riemann zeta function]], see at _[Riemann zeta function -- Relation to Jacobi theta function](http://ncatlab.org/nlab/show/Riemann+zeta+function#RelationToThetaFunctions)

## Properties


### Functional equation and Reciprocity
 {#FunctionalEquation}

By the [[Poisson summation formula]] the number-theoretic theta function $\theta(0,z)$ satisfies the following [[functional equation]]:

$$
  \theta(0,\tau) = \frac{1}{\sqrt{\tau}} \theta(0,\frac{1}{\tau}) 
  \,.
$$

Under the [[Mellin transform]] this implies the functional equation of the [[Riemann zeta function]], see at _[Riemann zeta function -- Functional equation](Riemann+zeta+function#functional_equation)_.


It also provides an analytic proof of the [[Landsberg-Schaar relation]]

$$\frac{1}{\sqrt{p}}\sum_{n=0}^{p-1}\exp\left(\frac{2\pi i n^2 q}{p}\right)=\frac{e^{\pi i/4}}{\sqrt{2q}}\sum_{n=0}^{2q-1}\exp\left(-\frac{\pi i n^2 p}{2q}\right)$$

where $p$ and $q$ are arbitrary positive integers. To prove it, apply theta reciprocity to $\tau=2iq/p+\epsilon$, $\epsilon \gt 0$, and then let $\epsilon\to 0$.

This reduces to the formula for the quadratic Gauss sum when $q=1$:

$$\sum_{n=0}^{p-1} e^{2 \pi i n^2 / p} =
\left\{
\array{
\sqrt{p} & {if } \; p\equiv 1\mod 4 \\
i\sqrt{p} & {if } \; p\equiv 3\mod 4
}
\right.
$$

(where $p$ is an odd prime). From this, it's not hard to deduce Gauss's "golden theorem".

[[quadratic reciprocity]]: $\left(\frac{p}{q}\right)\left(\frac{q}{p}\right)=(-1)^{(p-1)(q-1)/4}$ for odd primes $p$ and $q$.

See e.g. ([Karlsson](#Karlsson)).

> some of this material from  [this MO discussion](http://mathoverflow.net/q/120067/381)

## Related concepts


* [[Poisson summation formula]], [[functional equation]]

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## References

Due to [[Carl Jacobi]].

Review includes

* Wikipedia, _[Jacobi theta-function](http://en.wikipedia.org/wiki/Theta_function#Jacobi_theta_function)_

* section 9 in _Analytic theory of modular forms_ ([pdf](https://web.archive.org/web/20150326115730/http://www.math.harvard.edu/~jbland/ma259x_notes.pdf))

* {#Karlsson} Anders Karlsson, _Applications of heat kernels on abelian groups: $\zeta(2n)$, quadratic reciprocity, Bessel integrals_  ([psd](http://www.math.kth.se/~akarl/langmemorial.pdf))

* {#Hitchin90} [[Nigel Hitchin]], _Flat connections and geometric quantization_, : Comm. Math. Phys. Volume 131, Number 2 (1990), 347-380. ([Euclid](http://projecteuclid.org/euclid.cmp/1104200841))
 

[[!redirects Jacobi theta functions]]

[[!redirects Jacobi theta-function]]
[[!redirects Jacobi theta-functions]]
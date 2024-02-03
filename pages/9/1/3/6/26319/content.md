+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

The algebra obtained from the [generalization of the Cayley-Dickson construction](https://ncatlab.org/nlab/show/Cayley-Dickson+construction#cayleydicksonalbert_construction) applied on the [[complex number|complex numbers]] applied to the [[real numbers]] with parameter $\gamma=-1$.

A split-complex number $z$ may be represented as
$$
z= x+ j y
$$
where $j^2=1$ (in contrast with the [[imaginary unit]] $i^2=-1$ in the complex numbers). Conjugation is similarly given by
$$
z^* = x- j y
$$

A consequence is that the product $z z^*$ is not non-negative anymore, since
$$
z z^* = x^2 - j^2 y^2 = x^2 - y^2
$$
meaning in particular that [[zero-divisors]] exist (for example $(1 - j)(1 + j)=1 - j^2=0$). Using the diagonal basis
$$
e = \frac{1 - j}{2}
$$
$$
e^* = \frac{1 + j}{2}
$$
of idempotent elements, hence for which $e^2=e$ and $(e^*)^2=e^*$, and fulfilling $e e^*=e^* e=0$ results in multiplication given by
$$
(a e+b e^*)(c e+d e^*)
=(a c) e+(b d) e^*
$$
which yields that the algebra $\mathbb{R}[j]=\mathbb{R}[e]$ of split-complex numbers is isomorphic to the algebra $\mathbb{R}\oplus\mathbb{R}$ with pointwise multiplication.

## Related concepts

* [[tessarines]]

* [[split quaternions]]

* [[split octonions]]

## References

* Robert Brown. *On generalized Cayley-Dickson algebras.* Pacific Journal of Mathematics 20, no. 3 (1967): 415-422. ([doi](http://dx.doi.org/10.2140/pjm.1967.20.415))



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Harmonic analysis
+-- {: .hide}
[[!include harmonic analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $f$ a suitable ([[generalized function|generalized]]) [[function]] on an [[affine space]], its [[Fourier transform]] is given by $\hat f (a) \propto \int f(x) e^{i x a} d x$, while its [[Laplace transform]] is $\tilde f(a) \propto \int f(x) e^{-a x} d x $, when defined. Clearly these are two special cases of a single "transform" where $a$ is allowed to be [[complex number|complex]]; this is hence called the _Fourier-Laplace transform_.

## Definition


+-- {: .num_defn #FourierTransformOfCompactlySupportedDistribution}
###### Proposition/Definition
**(Fourier-Laplace transform of [[compactly supported distributions]])**

For $n \in \mathbb{N}$, let $u \in \mathcal{E}'(\mathbb{R}^n)$ be a compactly supported distribution on [[Cartesian space]] $\mathbb{R}^n$. Then its _[[Fourier transform of distributions]]_ is the function

$$
  \array{
    \mathbb{R}^n &\overset{\hat u}{\longrightarrow}& \mathbb{R}
    \\
    \zeta &\mapsto& u\left(e^{-i\langle -,\zeta \rangle} \right)
  }
$$

where on the right we have the application of $u$, regarded as a [[linear function]] $u \colon C^\infty(\mathbb{R}^n) \to \mathbb{R}$, to the [[exponential function]] applied to the canonical [[inner product]] $\langle -,-\rangle$ on $\mathbb{R}^n$.

This same formula makes sense more generally for [[complex numbers]] $\zeta \in \mathbb{C}^n$. This is then called the _[[Fourier-Laplace transform]]_ of $u$, still denoted by the same symbol:


$$
  \array{
    \mathbb{C}^n &\overset{\hat u}{\longrightarrow}& \mathbb{R}
    \\
    \zeta &\mapsto& u\left(e^{-i\langle -,\zeta \rangle} \right)
  }
$$

This is an [[entire analytic function]] on $\mathbb{C}^n$.

=--

([H&#246;rmander 90, theorem 7.1.14](#Hoermander90))

## Related concepts

* [[Paley-Wiener-Schwartz theorem]]

* [[wave front set]]

## References

* {#Hoermander90} [[Lars Hörmander]], section 2.3 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

[[!redirects Fourier-Laplace transforms]]



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

In [[harmonic analysis]], the _Fourier inversion theorem_ states that the [[Fourier transform]] is an [[isomorphism]] on the [[Schwartz space]] of [[functions with rapidly decreasing partial derivatives]]. Moreover, it is its own [[inverse]] up to a prefactor and reflection at the origin.

For Fourier transform over [[Cartesian spaces]], see e.g. [H&#246;rmander 90 ,theorem 7.1.5, theorem 7.1.10](#Hoermander90), [this prop.](Fourier+transform#FourierInversion).

## Statement

Let $n \in \mathbb{N}$ and consider $\mathbb{R}^n$ the [[Cartesian space]] of [[dimension]] $n$.


+-- {: .num_defn #FourierInversion}
###### Proposition
**([[Fourier inversion theorem]])**

The [[Fourier transform]] $\widehat{(-)}$ (def. \ref{FourierTransformSmoothFunctionsWithRapidlyDecayingDerivativesOnCartesianSpace}) on the [[Schwartz space]] $\mathcal{S}(\mathbb{R}^n)$ (def. \ref{SchwartzSpace}) is an [[isomorphism]], with [[inverse function]] the _inverse Fourier transform_

$$
  \widecheck {(-)}
     \;\colon\;
  \mathcal{S}(\mathbb{R}^n) \longrightarrow \mathcal{S}(\mathcal{R}^n)
$$

given by

$$
  \widecheck g (x)
    \;\coloneqq\;
   \underset{k \in \mathbb{R}^n}{\int}
      g(k) e^{2 \pi i k \cdot x}
   \, \frac{d^n k}{(2\pi)^n}
   \,.
$$

Hence in the language of [[harmonic analysis]] the function $\widecheck g \colon \mathbb{R}^n \to \mathbb{C}$ is the [[superposition]] of [[plane waves]] in which the plane wave with [[wave vector]] $k\in \mathbb{R}^n$
appears with [[amplitude]] $g(k)$.

=--

(e.g. [H&#246;rmander, theorem 7.1.5](#Hoermander90))



## Related theorems

* [[Parseval's theorem]]

* [[Paley-Wiener-Schwartz theorem]]

## References

* {#Hoermander90} [[Lars Hörmander]], theorem 7.1.5 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

[[!redirects inverse Fourier transform]]
[[!redirects inverse Fourier transforms]]

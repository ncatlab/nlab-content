

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The generalization of the concept of [[Fourier transform]] from suitable function to [[distributions]].

## Definition

+-- {: .num_defn #FourierTransformOfTemperedDistribution}
###### Definition
**(Fourier transform of [[tempered distributions]])**

For $n \in \mathbb{N}$, let $u \in \mathcal{S}'(\mathbb{R}^n)$ be a [[tempered distribution]]. Then its _Fourier transform_ $\hat u \in \mathcal{S}'(\mathbb{R}^n)$ is defined by

$$
  \array{
    \mathcal{S}(\mathbb{R}^n)
      &\overset{\hat u}{\longrightarrow}&
    \mathbb{C}
    \\
    f &\mapsto& \langle u, \hat f\rangle
  }
  \,,
$$

where on the right $\hat f$ is the ordinary [[Fourier transform]] of the function $f$ (an element of the [[Schwartz space]] $\mathcal{S}(\mathbb{R}^n)$).

=--

(e.g. [H&#246;rmander 90, def. 7.1.9](#Hoermander90))

## Properties

+-- {: .num_prop}
###### Proposition

The operation of Fourier transform of [[tempered distributions]] (def. \ref{FourierTransformOfTemperedDistribution}) induces a [[linear isomorphism]] of the space of temptered distributions with itself:

$$
  \widehat{(-)}
  \;\colon\;
  \mathcal{S}'(\mathbb{R}^n)
   \overset{\simeq}{\longrightarrow}
  \mathcal{S}'(\mathbb{R}^n)
$$

=--

(e.g. [Melrose 03, corollary 1.1](#Melrose03))



+-- {: .num_prop #FourierTransformOfCompactlySupportedDistributions}
###### Proposition
**(Fourier transform of [[compactly supported distributions]])**

If $u \in \mathcal{D}'(\mathbb{R}^n) \hookrightarrow \mathcal{E}'(\mathbb{R}^n)$ happens is a [[compactly supported distribution]], regarded as a [[tempered distribution]], then its Fourier transform according to def. \ref{FourierTransformOfTemperedDistribution} is a smooth function 

$$
  \hat u \in \mathcal{S}(\mathbb{R}^n)
$$

given by

$$
  \hat u \;\colon\; \xi \mapsto \langle  u, \exp(-i \langle -, \xi\rangle) \rangle
  \,.
$$

=--

(e.g. [H&#246;rmander 90, theorem 7.1.14](#Hoermander90))

(This plays a role for instance in the [[Paley-Wiener-Schwartz theorem]].)

+-- {: .num_prop}
###### Proposition

The Fourier transform (def. \ref{FourierTransformOfTemperedDistribution}) of the [[convolution of distributions]] of a [[compactly supported distribution]] $u_1 \in \mathcal{E}'$ with a [[tempered distribution]] $u_2 \in \mathcal{S}'$ is the [[product of distributions]] of their separate Foruier transforms:

$$
  \widehat {u_1 \star u_2}
  \;=\;
  \hat u_1 \hat u_2
  \,.
$$

(Here, by prop. \ref{FourierTransformOfCompactlySupportedDistributions}, $\hat u_1$ is just a smooth function, so that the product on the right is just that of a distribution with a function.)

=--

([H&#246;rmander 90, theorem 7.1.15](#Hoermander90))

## Related concepts

* [[pullback of distributions]]

* [[product of distributions]]

* [[composition of distributions]]

* [[extension of distributions]]


## References

* {#Hoermander90} [[Lars Hörmander]], chapter VII of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990


* {#Melrose03} [[Richard Melrose]], chapter 1 of _Introduction to microlocal analysis_, 2003 ([pdf](http://www-math.mit.edu/~rbm/iml90.pdf))


[[!redirects Fourie transforms of distributions]]

[[!redirects Fourier transform of a distribution]]
[[!redirects Fourier transforms of a distribution]]

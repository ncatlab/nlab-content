


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

Let $n \in \mathbb{N}$ and write $\mathbb{R}^n$ for the [[Cartesian space]] of [[dimension]] $n$. Then a _plane wave_ on $\mathbb{R}^n$ is a [[function]]

$$
  \mathbb{R}^n \longrightarrow \mathbb{C}
$$

given by the [[exponential function]] with [[complex number|complex]] argument of the form

$$
  \vec x \;\mapsto\; A e^{2 \pi i \vec k \cdot \vec x}
  \,.
$$ 

Here $\vec k \in \mathbb{R}^n$ is the _[[wave vector]]_ of this plane wave (and $A \in \mathbb{C}$ is its [[amplitude]]).

In [[Fourier analysis]] over [[Cartesian space]], the [[Fourier transform]] expresses every [[function with rapidly decreasing partial derivatives]] as a [[superposition]] of plane waves.

If here $\mathbb{R}^n \simeq \mathbb{R}^{p,1}$ is identified with [[Minkowski spacetime]] with canonical [[coordinates]] labeled $(x^0, x^1, \cdots x^p)$, then  the 0-component of the [[wave vector]]

$$
  \nu \coloneqq k_0
$$

is called the _[[frequency]]_ of the wave (in this chosen [[coordinate system]]). If in this situation the [[wave vector]]  satisfies $k_\mu k^\mu = 0$, then the plane wave is a solution to the [[wave equation]] on Minkowski spacetime. If more generally it satisfies $k_\mu k^\mu + m^2 = 0$ for some $m^2 \in \mathbb{R}$, the it is a solution to the [[Klein-Gordon equation]] on Minkowski spacetime.

## Related concepts

* [[wave]]

* [[wave vector]]

* [[wavelength]], [[frequency]]

* [[Fourier transform]]

* [[wave function]]

## References

See also

* Wikipedia, _[Plane wave](https://en.wikipedia.org/wiki/Plane_wave)_

[[!redirects plane waves]]

[[!redirects planewave]]
[[!redirects planewabes]]


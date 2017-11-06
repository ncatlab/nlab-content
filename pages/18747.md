
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

A _wave vector_ is a [[vector]] that encodes [[wavelength]] and direction of a _[[plane wave]]_.

## Definition

Let $n \in \mathbb{N}$ and write $\mathbb{R}^n$ the [[Cartesian space]] of [[dimension]] $n$. Thinking of $\mathbb{R}^n$ as a [[vector space]], then each point in it is a [[vector]] $\vec x \in \mathbb{R}^n$ and hence a [[smooth function]] $f \colon \mathbb{R}^n \to \mathbb{C}$ may be thought of as a function of these "position vectors".

If $f$ is a [[function with rapidly decreasing partial derivatives]], then its [[Fourier transform]] $\hat f \;\colon\; \mathbb{R}^n \to \mathbb{C}$ exists. By the [[Fourier inversion theorem]], this function is such that it expresses $f$ as a [[superposition]] of "[[plane wave]]" functions $\vec x \mapsto e^{2\pi i \vec x \cdot \vec k}$ as

$$
  f(\vec x) 
  \;=\;
  \underset{\vec k \in \mathbb{R}^n}{\int}
   \hat f(k) \, e^{2 \pi i \vec k \cdot \vec x}
  \, d \vec k
  \,.
$$

Here the [[vector]] $\vec k \in \mathbb{R}^n$ determines 

1. the [[wavelength]] $\lambda \coloneqq 1/{\vert \vec k\vert}$ (the inverse of the [[norm]] of $\vec k$);

1. the direction $\frac{\vec k}{{\vert \vec k\vert }} \in S(\mathbb{R}^n)$ (the corresponding unit vector in the [[unit sphere]])

of the "[[plane wave]]" $\vec x \mapsto e^{2 \pi i \vec x \cdot \vec k}$.

If here $\mathbb{R}^n \simeq \mathbb{R}^{p,1}$ is identified with [[Minkowski spacetime]] with canonical coordinates denoted $(x^0, x^1, \cdots, x^p)$, then the 0-component of the wave vector

$$
  \nu \coloneqq k_0
$$

is called the _[[frequency]]_ of the corresponding [[plane wave]] (in the chosen [[coordinate system]]).


## Related concepts

* [[plane wave]]

* [[Fourier transform]]
x^1
* [[wave]]

* [[frequency]]

## References

See also

* Wikipedia, _[Wave vector](https://en.wikipedia.org/wiki/Wave_vector)_

[[!redirects wave vectors]]

[[!redirects wavevector]]
[[!redirects wavevectors]]

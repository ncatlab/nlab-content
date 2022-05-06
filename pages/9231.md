
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A [[probability distribution]] on a [[Cartesian space]] $\mathbb{R}^n$ is called **Gaussian** or a **normal distribution** if it is of the form

$$
  \mu_A \;\colon\; \vec x \mapsto \frac{\sqrt{det A}}{(2\pi)^{n/2}} 
  \exp\left(-\tfrac{1}{2} \left\langle \vec x , A \vec x\right\rangle\right)
  \,d x^1 \cdots d x^n
  \,.
$$

where $A$ is some $n \times n$ [[matrix]] such that $\langle -, A-\rangle$ is a positive definite [[bilinear form]]. Here $\det A$ denotes the [[determinant]] and $\langle -,-\rangle$ is the canonical [[bilinear form]] on $\mathbb{R}^n$.

Since $\sqrt{\det A}$ is the coordinate of the [[volume element]] $vol_A$ associated with $A$, we may equivalently write this as

$$
  \mu_A \;\colon\; \vec x \mapsto \frac{1}{(2\pi)^{n/2}} 
  \exp\left(-\tfrac{1}{2} \left\langle \vec x , A \vec x\right\rangle\right)
  \,vol_A  \,.
$$

The [[mean]] of this distribution is $\vec{0}$; for a distribution with mean $\vec{c}$, replace $\langle{\vec{x},A \vec{x}}\rangle$ with $\langle{\vec{x} - \vec{c},A \vec{x} - A \vec{c}}\rangle$.

The matrix $A$ is the [[inverse matrix|inverse]] of the [[covariance matrix]].  In particular, for $n = 1$, we may write $x^2/\sigma^2$ (or $(x-c)^2/\sigma^2$ for mean $c$) in place of $\langle{\vec{x},A \vec{x}}\rangle$, where $\sigma$ is the [[standard deviation]]; similarly, $\sqrt{\det A}$ becomes $1/\sigma$.  This gives the form

$$
  \mu_\sigma \;\colon\; x \mapsto \frac{1}{\sigma \sqrt{2\pi}} 
  \exp\left(-\frac{(x-c)^2}{2\sigma^2}\right)
  \,d x
  \,,
$$

which may be more familiar to some readers.


## Related concepts

* [[Wick's theorem]]

* [[Feynman diagram]]

* [[statistical significance]]

## References

See also 

* Wikipedia, _[Normal distribution](https://en.wikipedia.org/wiki/Normal_distribution)_

* Wikipedia, _[Standard deviation](https://en.wikipedia.org/wiki/Standard_deviation)_

* Good Calculators, _[Standard deviation calculator](https://goodcalculators.com/standard-deviation-calculator/)_

[[!redirects Gaussian probability measure]]
[[!redirects Gaussian probability measures]]

[[!redirects Gaussian distribution]]
[[!redirects Gaussian distributions]]

[[!redirects Gaussian probability distribution]]
[[!redirects Gaussian probability distributions]]

[[!redirects normal distribution]]
[[!redirects normal distributions]]

[[!redirects multivariate normal distribution]]
[[!redirects multivariate normal distributions]]


[[!redirects standard deviation]]
[[!redirects standard deviations]]

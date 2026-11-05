
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

The matrix $A$ is the [[inverse matrix|inverse]] of the covariance matrix.  In particular, for $n = 1$, we may write $x^2/\sigma^2$ (or $(x-c)^2/\sigma^2$ for mean $c$) in place of $\langle{\vec{x},A \vec{x}}\rangle$, where $\sigma$ is the [[standard deviation]]; similarly, $\sqrt{\det A}$ becomes $1/\sigma$.  This gives the form 

$$\mu_\sigma \;\colon\; x \mapsto \frac{1}{\sigma \sqrt{2\pi}} \exp\left(-\frac{(x-c)^2}{2\sigma^2}\right) \, dx $$

In the case that $n = 1$ one denotes this distribution by $\mathcal{N}(c,\sigma^2)$.


## Square as a random variable

The square $Y = X^2$ of a random number with probability distribution $\mathcal{N}(0,\sigma^2)$ follows a scaled Chi-squared distribution.

This has positive expected value $0 \lt \mathbb{E}[X^2]$ and bounded variance $\text{Var}(X^2) \lt \infty$.

The probability density function of $Y = X^2$ is 

$$
f_Y(y) = \frac{1}{\sqrt{2\pi \sigma^2 y}} \exp\left(-\frac{y}{2\sigma^2}\right), y \in (0,\infty)
$$

with $f_Y(0) = 0$. For $X \sim \mathcal{N}(0, \sigma^2)$, the general moment formulas are:

$$
\mathbb{E}[X^n] = \begin{cases} (n-1)!! \, \sigma^n = \frac{n!}{2^{n/2}(n/2)!} \, \sigma^n & \text{if }\, n\, \text{ is even} \\ 0 & \text{if }\, n\, \text{ is odd} \end{cases}
$$

and

$$
\text{Var}(X^n) = \mathbb{E}[X^{2n}] - (\mathbb{E}[X^n])^2 = \sigma^{2n} \text{Var}(Z^n)
$$

where $Z \sim \mathcal{N}(0, 1)$ is the standard normal variable.
 
Specifically, for $n = 2$, one has $\mathbb{E}[X^2] = \text{Var}(X) = \sigma^2$ and $\text{Var}(X^2) = \mathbb{E}[X^4] - (\mathbb{E}[X^2])^2 = 3\sigma^4 - \sigma^4 = 2\sigma^4$.

If we define the standardized centered variable $W = \frac{X^2 - \mathbb{E}[X^2]}{\text{Var}(X)} = \frac{X^2 - \sigma^2}{\sigma^2}$, then by linearity of expectation:
 
$$
\mathbb{E}[W] = \frac{\mathbb{E}[X^2] - \sigma^2}{\sigma^2} = \frac{\sigma^2 - \sigma^2}{\sigma^2} = 0
$$
 
By scaling properties of variance, dividing by the constant $\sigma^2$ rescales the variance by $\frac{1}{\sigma^4}$:
 
$$
\text{Var}(W) = \text{Var}\left(\frac{X^2 - \sigma^2}{\sigma^2}\right) = \frac{1}{\sigma^4}\text{Var}(X^2) = \frac{2\sigma^4}{\sigma^4} = 2
$$
 
Substituting $X = \sigma Z$ directly into $W$ confirms this independence from $\sigma$:
 
$$
W = \frac{(\sigma Z)^2 - \sigma^2}{\sigma^2} = \frac{\sigma^2(Z^2 - 1)}{\sigma^2} = Z^2 - 1
$$

Because $W = Z^2 - 1$ identically for all $0 \lt \sigma $, the standardized deviation $W$ is strictly scale-invariant with zero mean and variance $\text{Var}(W) = 2$.

## Related concepts

* [[Wick's theorem]]

* [[Feynman diagram]]

* [[statistical significance]]

## References

See also 

* Wikipedia, _[Normal distribution](https://en.wikipedia.org/wiki/Normal_distribution)_

* Wikipedia, _[Standard deviation](https://en.wikipedia.org/wiki/Standard_deviation)_

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

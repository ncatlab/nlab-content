> This entry is about a notion in [[mathematics]]. For the related notion i  [[physics]] and [[music]], see at *[[overtone series]]*.

***

# Contents
* table of contents
{: toc}

## Definition

Let $f:\mathbb{N} \to (\mathbb{R} \to \mathbb{R})$ defined as

$$f(n)(x) \coloneqq \sum_{i = 1}^n \frac{\cos(n x)}{n}$$ 

be a [[Fourier series]]. The **harmonic series** is defined as 

$$h(n) \coloneqq f(n)(2 \pi m) = \sum_{i = 1}^n \frac{\cos(2 \pi m n)}{n} = \sum_{i = 1}^n \frac{1}{n}$$

for any [[integer]] $m \in \mathbb{Z}$ and the **alternating harmonic series** is defined as 

$$h_\mathrm{alt}(n) \coloneqq - f(n)(2 \pi m + \pi) = - \sum_{i = 1}^n \frac{\cos(2 \pi m n + \pi n)}{n} = - \sum_{i = 1}^n \frac{(-1)^{n}}{n} = \sum_{i = 1}^n \frac{(-1)^{n + 1}}{n}$$

for any [[integer]] $m \in \mathbb{Z}$. 

The harmonic series diverges: 

$$\lim_{n \to \infty} h(n) = \infty$$

while the alternating harmonic series converges:

$$\lim_{n \to \infty} h_\mathrm{alt}(n) = \ln(2)$$

where $\ln$ is the [[natural logarithm]]. This is because the Fourier series above [[converges]] everywhere in $\mathbb{R}$ that is [[tight apartness relation|apart]] from an integer multiple of $2 \pi$. 

## See also

* [[series]]

* [[convergence]]

* [[Fourier analysis]]

## References

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Harmonic_series_(mathematics)">Harmonic series (mathematics)</a>*
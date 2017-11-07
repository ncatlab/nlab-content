

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let $n \in \mathbb{N}$ and consider $\mathbb{R}^n$ the [[Cartesian space]] of [[dimension]] $n$.


+-- {: .num_defn #ProductOfDistributionWithSmoothFunction}
###### Definition
**(product of a [[distribution]] with a [[smooth function]])**

For $u \in \mathcal{D}'(\mathbb{R}^n)$ a [[distribution]], and $f \in C^\infty(\mathbb{R}^n)$ a [[smooth function]], their _product_

$$
  f \cdot u \;\in\; C^\infty(\mathbb{R}^n)
$$

is the [[distribution]] given on a [[compactly supported function|compactly supported]] [[smooth function]] $g \in C^\infty_{cp}(\mathbb{R}^n) = \mathcal{D}(\mathbb{R}^n)$ by

$$
  (f\cdot u)(g) \;\coloneqq\; u\left( f \cdot g\right)
  \,,
$$

where on the right we have the application of $u$ regarded as a [[continuous linear functional]] $u \colon \mathcal{D}(\mathbb{R}^n) \to \mathbb{C}$ to the ordinary pointwise product of smooth functions $f \cdot g$.

=--

## Properties


+-- {: .num_defn #ProductOfADistributionWithANonSingularDistribution}
###### Definition
**([[product of distributions|product of a distribution]] with a [[non-singular distributions]] is product of distribution with a smooth function)**

The [[wave front set]] of a [[non-singular distribution]] $u_f$ corresponding to a [[smooth function]] $f \in C^\infty(\mathbb{R}^n)$, is [[empty]] ([this prop.](Paley-Wiener-Schwartz+theorem#DecayPropertyOfFourierTransformOfCompactlySupportedFunctions)). Therefore the product of distributions (def. \ref{ProductOfDistributions}) of a [[non-singular distribution]] with any distribution $u$ is defined, and given by the product of distributions with smooth functions according to def. \ref{ProductOfDistributionWithSmoothFunction}:

$$
  u_f \cdot u = f \cdot u = u(f\cdot (-))
  \,.
$$

=--

## Related concepts

* [[convolution product]]

* [[convolution product of distributions]]

* [[derivative of a distribution]]

## References

See also

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Distribution_(mathematics)#Multiplication_by_a_smooth_function">Distribution (mathematics) -- Multiplication by a smooth function</a>_

[[!redirects products of distributions with a smooth function]]

[[!redirects product of a distribution with a smooth function]]
[[!redirects products of distributions with smooth functions]]

[[!redirects product of distributions with smooth functions]]
[[!redirects products of distributions with smooth functions]]

[[!redirects product of a distribution with smooth functions]]
[[!redirects products of a distribution with smooth functions]]

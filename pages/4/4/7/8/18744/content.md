
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

## Idea

The generalization of the [[convolution product]] on [[smooth function]] to [[distributions]], viewing distributions as [[generalized functions]] (via [this prop.](non-singular+distribution#NonSingularDistributionsAreDenseInAllDistributions)).

## Definition

+-- {: .num_defn #ConvolutionOfADistributionWithSmoothFunction}
###### Definition
**(convolution of a [[distribution]] with a [[smooth function]])**

Let $u \in \mathcal{D}'(\mathbb{R}^n)$ be a [[distribution]], and $f \in C^\infty_0(\mathbb{R}^n)$ a [[compactly supported smooth function]]. Then the convolution of the two is the smooth function

$$
  u \star f \in C^\infty(\mathbb{R}^n)
$$

defined by

$$
  (u \star f)(x) \;\coloneqq\; u\left( f(x-(-))\right)
  \,.
$$

=--

([H&#246;rmander 90, top of section 4.1](#Hoermander90))


+-- {: .num_defn #ConvolutionOfADistributionWithACompactlySupportedDistribution}
###### Definition
**(convolution of a [[distribution]] with a [[compactly supported distribution]])**


Let $u_1, u_2 \in \mathcal{D}'(\mathbb{R}^n)$ be two [[distributions]], such that at least one of them is a [[compactly supported distribution]] in $\mathcal{E}'(\mathbb{R}^n) \hookrightarrow \mathcal{D}'(\mathbb{R}^n)$, then their convolution product

$$
  u_1 \star u_2 \;\in \; \mathcal{D}'(\mathbb{R}^n)
$$

is the unique distribution such that for $f \in C^\infty(\mathbb{R}^n)$ a [[smooth function]], it satisfies

$$
  (u_1 \star u_2) \star f = u_1 \star (u_2 \star f)
  \,,
$$ 

where on the right we have twice a convolution of a distribution with a smooth function according to def. \ref{ConvolutionOfADistributionWithSmoothFunction}.

=--

([H&#246;rmander 90, def. 4.2.2](#Hoermander90))



## Properties

### Relation to pointwise product of distributions

+-- {: .num_prop #FourierTransformOfDistributionsInterchangesConvolutionOfDistributionsWithPointwiseProduct}
###### Proposition
**([[Fourier transform of distributions]] interchanges [[convolution of distributions]] with pointwise product)**

Let 

$$
  u_1 \in \mathcal{S}'(\mathbb{R}^n)
$$ 

be a [[tempered distribution]] and 

$$
  u_2 \in \mathcal{E}'(\mathbb{R}^n) \hookrightarrow \mathcal{S}'(\mathbb{R}^n)
$$

be a [[compactly supported distribution]].

Observe here that the [[Paley-Wiener-Schwartz theorem]] implies that the [[Fourier transform of distributions]] of $u_1$ is a [[non-singular distribution]]
$\widehat{u_1} \in C^\infty(\mathbb{R}^n)$ so that the product $\widehat{u_1} \cdot \widehat{u_2}$ is always defined.

Then the [[Fourier transform of distributions]] of the convolution product of distributions (def. \ref{ConvolutionOfADistributionWithACompactlySupportedDistribution}) is the product of the [[Fourier transform of distributions]]:

$$
  \widehat{u_1 \star u_2}
  \;=\;
  \widehat{u_1} \cdot \widehat{u_2}
  \,.
$$


=--

(e.g. [H&#246;rmander 90, theorem 7.1.15](#Hoermander90))

For the converse: [Friedlander-Joshi 98, p. 102](#FriedlanderJoshi98)

+-- {: .num_remark #ProductOfDistributionsViaFourierTransformOfConvolution}
###### Remark
**([[product of distributions]] via [[Fourier transform of distributions]])**

Prop. \ref{FourierTransformOfDistributionsInterchangesConvolutionOfDistributionsWithPointwiseProduct} together with the [[Fourier inversion theorem]] suggests to _define_ the [[product of distributions]] $u_1 \cdot u_2$ for [[compactly supported distributions]] $u_1, u_2 \in \mathcal{E}'(\mathbb{R}^n) \hookrightarrow \mathcal{S}'(\mathbb{R}^n)$ by the formula

$$
  \widehat{ u_1 \cdot u_2 }
  \;\coloneqq\;
  (2\pi)^{-n} \widehat{u_1} \star \widehat{u_2}
  \,.
$$

For this to make sense, the [[convolution product]] of the [[smooth functions]] on the right needs to exist, which is not guaranteed. The condition that this exists is the [[Lars Hörmander|Hörmander]]-condition on the _[[wave front set]]_ of $u_1$ and $u_2$. See at _[[product of distributions]]_ for more.


=--

### Relation to  singular support and wave front set

+-- {: .num_prop #WaveFrontSetOfCompactlySupportedDistributions}
###### Proposition
**([[wave front set]] of [[convolution of distributions|convolution of]] [[compactly supported distributions]])**


Let $u,v \in \mathcal{E}'(\mathbb{R}^n)$ be two  [[compactly supported distributions]]. Then the [[wave front set]] of their convolution of distributions (def. \ref{ConvolutionOfADistributionWithACompactlySupportedDistribution}) is

$$
  WF(u \star v)
  \;\subseteq\;
  \left\{
    (x + y, k)
    \;\vert\;
    (x,k) \in WF(u) \,\text{and}\, (y,k) \in WF(u)
  \right\}
  \,.
$$

=--

([Bengel 77, prop. 3.1](#Bengel77))


## Related concepts

* [[product of a distribution with a smooth function]]

* [[product of distributions]]

* [[Fourier transform of distributions]]

## References

* {#Hoermander90} [[Lars Hörmander]], section 4 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

* {#FriedlanderJoshi98} Friedlander F G and Joshi M 1998 _Introduction  to  the  Theory  of  Distributions_ 2nd ed. (Cambridge: Cambridge University Press)

* {#Bengel77} Gunter Bengel, _Wave front sets and Singular Supports of Convolutions_, Publ. RIMS, Kyoto Univ. 12 Suppl. (1977), 1-4 and Math. Ann. 226, 247-252 (1977) ([web](https://gdz.sub.uni-goettingen.de/en/dms/loader/img/?PID=GDZPPN002313952), [pdf](https://gdz.sub.uni-goettingen.de/download/PPN235181684_0226/PPN235181684_0226___LOG_0044.pdf))

[[!redirects convolution products of distributions]]

[[!redirects convolution of distributions]]
[[!redirects convolutions of distributions]]

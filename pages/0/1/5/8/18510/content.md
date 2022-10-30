
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

### Generally

The _product_ of two [[distributions]] is an operation that generalizes, when defined, the ordinary pointwise product of [[functions]] when we think of distributions as [[generalized functions]] (via [this prop.](non-singular+distribution#NonSingularDistributionsAreDenseInAllDistributions)). However, as opposed to ordinary functions, the product of distributions is not defined for arbitrary pairs of distributions, but only for those pairs such that the sum of their [[wave front sets]] does not intersect the zero section of the [[cotangent bundle]] ([H&#246;rmander 90, theorem 8.2.10](#Hoermander90)). The study of distributions with proper attention to their singularity structure via [[wave-front sets]] is known as _[[microlocal analysis]]_.

(There is also the way to  deform the product to make it globally defined, see at _[[Colombeau algebra]]_.)


The product of distributions may be understood as follows:

Let $u,v \in  \mathcal{D}'(\mathbb{R}^1)$ be two [[distributions]] on the [[real line]], for simplicity. 

First of all, since the their product $u \cdot v$, if it exists, is supposed to generalize the _pointwise_ product of smooth functions, it ought to be fixed by determining it locally: for every point $x \in \mathbb{R}$ there ought to be a [[compactly supported function|compactly supported]] [[smooth function]] $f \in C^\infty_{cp}(\matbb{R})$ with $f(x) = 1$ such that 

$$
  f^2 (u \cdot v) = (f u) \cdot (f v)
  \,.
$$

But now $f v$ and $f u$ are both [[compactly supported distributions]], and these have the special property that their [[Fourier transform of distributions|Fourier transform]] is, in particular, a [[smooth function]] (by the [[Paley-Wiener-Schwartz theorem]]). Moreover, the [[Fourier transform]] intertwines pointwise products with [[convolution products]]. This means that if the product of distributions exists, it must be given by the inverse Fourier transform of the [[convolution product]] of the Fourier transforms $\widehat {f u}$ and $\widehat f v$ of $f v$ and $g v$, respectively:

$$
  \widehat{ f^2 (u \cdot v) }
  \propto
  \int \widehat (f u)(k) \widehat (f v)((-) - k) d k
  \,.
$$

This shows that the product of distributions exists once there is a [[bump fuction]] $f$ such that this [[integral]] is defined.

Now the [[Paley-Wiener-Schwartz theorem]] says more, it says that the Fourier transforms $\widehat {f u}$ and $\widehat {f u}$ are generally polynomially bounded. On the other hand, the [[integral]] above is well defined if the integrand decays at least quadratically. 

This means that for the product to be well defined, either $\widehat f u$ has to polynomially decay faster with $k \to \pm \infty$ than $\widehat {f v}$ grows in the other direction, $k \to \mp \infty$. 

Moreover, one will want the product of distributions to to satisfy the [[Leibnitz rule]] with respect to [[derivatives of distributions]]. But the degree of polynomial growth of the [[Fourier transform of distributions|Fourier transform]] grows by one with each derivative. Therefore if the [[Leibnitz rule]] is to hold generally, we will need that either $\widehat{f u}$ or $\widehat{f v}$ decays faster than _any_ polynomial in the opposite direction in which the respective other transform does not decay.

This is the H&#246;rmander wave front set condition (...)

### In perturbative quantum field theory
 {#IdeaInPerturbativeQFT}

The issue of mutliplying distributions has prominently been perceived in [[perturbative quantum field theory]], where [[operator-valued distributions]] serve to give the [[algebra of observables]] such as the [[Wick algebra]] of the [[free fields]] or more generally the [[interacting field algebra]].

A popular impression is (or has been) that the failure of distributions to have a globally defined product is a failure of the mathematical formalism to support the structures needed to model [[perturbative quantum field theory]]. But in fact the opposite is true: Handling the product of distributions correctly via proper analysis of their [[wave front set]] and handling the [[point-extension of distributions]] properly via analysis of their [[scaling degree of a distribution|scaling degree]] leads to a mathematical rigorous construction and mathematically captures all the effects expected from the non-rigorous treatmeants, notably the [[renormalization]] freedom. This is the topic of [[causal perturbation theory]]/[[locally covariant perturbative quantum field theory]], see there for more.




## Definition
 {#Definition}


+-- {: .num_defn #ProductOfDistributions}
###### Definition
**(multiplication of distributions)

Let $u,v \in \mathcal{D}'(X)$ be two [[distributions]] such that the sum of their [[wave front sets]] $WF(u) + WF(v)$  does not intersect zero. Then their _product distribution_

$$
  u \cdot v \in \mathcal{D}'(X)
$$

is the [[pullback of a distribution|pullback]] (via [this prop.](pullback+of+a+distribution#PullbackOfDistributionsWhoseWaveFrontDoesNotIntersectNormalBundle)) of their [[tensor product of distributions|tensor product]] along the [[diagonal]] map $\Delta_X \;\colon\; X \to X \times X$:

$$
  u \cdot v 
    \;\coloneqq\; 
  \Delta_X^\ast( u \otimes v )
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Def. \ref{ProductOfDistributions} is indeed well defined.

=--

([H&#246;rmander 90, theorem 8.2.10](#Hoermander90), [Melrose 03, prop. 4.11](#Melrose03))

+-- {: .proof}
###### Proof

We need to check that the [[pullback of distributions]] is well defined. By [this prop.](pullback+of+a+distribution#PullbackOfDistributionsWhoseWaveFrontDoesNotIntersectNormalBundle) this means to check that the [[wave front set]] of the $u \otimes v$ does not intersect the [[conormal bundle]] of the diagonal map

Now the conormal bundle of the diagonal map consists of those pairs of covectors whose sum vanishes:

$$
  N^\ast_{\Delta_X}
  = 
  \left\{
    (x,(\xi, -\xi))
    \;\vert\;
    \xi \in T^\ast_x X
  \right\}
  \,.
$$

Moreover, by [this example](tensor+product+of+distributions#WaveFrontOfTensorProductDistribution) the wave front set of the tensor product distribution $u \otimes v$ is

$$
  WF(u \otimes v)
  \;\subset\;
  \left(
     WF(u) \times WF(v)
  \right)
    \;\cup\;
  \left(
    \left( supp(u) \times \{0\} \right)
    \times WF(v)
  \right)
    \;\cup\;
   \left(
     WF(u)
     \times
     \left(
       supp(v) \times \{0\}
     \right)
   \right)
  \,,
$$

Since any wave front set excludes the zero-section by definition, the second and the third summand in this union never intersect the above conormal bundle. The first summand intersects the above conormal bundle precisely if there is a covector in $WF(u)$ which is minus a covector contained in $WF(v)$. That this is not the case is precisely the assumption.


=--

## Properties

### Non-existence of a global product
 {#NonExistenceOfAGlobalProduct}


The fact that there is no general extension of multiplication to distributions (without condition on the [[wave front set]]) is a famous [[no-go theorem]] of [[Laurent Schwartz]].

A quick way to see the problem is the following: 

Let $H(x)$ be the [[Heaviside function]], we clearly have

$$
      H(x) = H^{n} (x)
$$

where the product on the right side is the product of classical functions. Applying differentiation and the product rule naivly results in a contradiction immediatly:
$$
   \delta(x) = n H^{n-1} (x) \delta(x)
$$

The inconsistency of this product is detected by the [[wave front sets]] as follows: The wave front set both of the [[Heaviside distribution]] as well as of the [[delta distribution]] on the line is $\{(0,k) \vert k \neq 0\}$ ([this example](wavefront+set#WaveFrontOfDeltaDistribution) and [this example](wavefront+set#WaveFrontSetOfHeavisideDistribution)). Therefore for both of these distributions mutliplication is only defined, according to def. \ref{ProductOfDistributions}, with a distribution $u$ for which there exists a [[bump function]] $b$ with $b(0) = 1$ such that $b \cdot u$ is again a bump function. This excludes the products of these distributions with themselves and with each other.

## Examples
 {#Examples}

+-- {: .num_defn #ProductOfADistributionWithANonSingularDistribution}
###### Definition
**(product of a [[distribution]] with a [[non-singular distributions]])**

The [[wave front set]] of a [[non-singular distribution]], hence of a genuine [[smooth function]] $f$, is [[empty]] ([this prop.](Paley-Wiener-Schwartz+theorem#DecayPropertyOfFourierTransformOfCompactlySupportedFunctions)). Therefore the product of distributions (def. \ref{ProductOfDistributions}) of a [[non-singular distribution]] with any distribution $u$ is defined, and given by the product of distributions with smooth functions:

$$
  f \cdot u = u(f\cdot (-))
  \,.
$$

=--



## Related concepts

* [[Hadamard distribution]]

* [[microcausal functional]], [[Wick algebra]]

* [[operator-valued distribution]]

* [[Fourier transform of distributions]]

## References

* {#Hoermander90} [[Lars Hörmander]], section 8.1 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

* {#Melrose03} [[Richard Melrose]], chapter 1 of _Introduction to microlocal analysis_, 2003 ([pdf](http://www-math.mit.edu/~rbm/iml90.pdf))


* [[Michael Oberguggenberger]], _Products of distributions_, Journal f&#252;r die reine und angewandte Mathematik (1986) Volume: 365, page 1-11 ([EuDML](https://eudml.org/doc/152801))

* [[Michael Oberguggenberger]], _Multiplication of Distributions and Applications to Partial Differential Equations_, Longman 1992

Slides with exposition of the role of multiplication of distributions in [[renormalization]] of [[Feynman diagrams]] via [[causal perturbation theory]]/[[perturbative AQFT]]:

* {#Brouder10} [[Christian Brouder]], _Multiplication of distributions_, 2010 ([[BrouderProductOfDistributions.pdf:file]])


[[!redirects products of distributions]]

[[!redirects multiplication of distributions]]
[[!redirects multiplications of distributions]]

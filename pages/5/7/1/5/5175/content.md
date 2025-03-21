
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

A **Dirac distribution** or **Dirac $\delta$-distribution** $\delta(p)$ is the [[distribution]] that is given by [[evaluation|evaluating]] a [[function]] at a point $p$.

It is closely related to [[Dirac measures]], in the language of [[measure theory]].

## Properties


+-- {: .num_prop #DerivativeOfHeavisideDistribution}
###### Proposition

The [[derivative of distributions|distributional derivative]] of the [[Heaviside distribution]] $\Theta \in \mathcal{D}'(\mathbb{R})$ is the [[delta distribution]] $\delta \in \mathcal{D}'(\mathbb{R})$:

$$
  \partial \Theta = \delta
  \,.
$$

=--

+-- {: .proof}
###### Proof

For $b \in C^\infty_c(\mathbb{R})$ any [[bump function]] we compute:

$$
  \begin{aligned}
    \int \partial\Theta(x) b(x) \, d x
    & =
    - \int \Theta(x) \partial b(x)\, dx
    \\
    & =
    - \int_0^\infty \partial b(x) d x
    \\
    & =
    - \left( b(x)\vert_{x \to \infty} - b(0) \right)
    \\
    & =
    b(0)
    \\
    &
    =
    \int \delta(x) b(x) \, dx
    \,.
  \end{aligned}
$$

=--


### Fourier transform
 {#FourierTransform}


+-- {: .num_defn #FourierTransformOfDeltaDistribution}
###### Example
**([[Fourier transform of distributions|Fourier transform]] of the [[delta-distribution]])**

The [[Fourier transform of distributions|Fourier transform]] ([this def.](Fourier+transform#FourierTransformOnTemperedDistributions)) of the [[delta distribution]], via [this example](Fourier+transform#CompactlySupportedDistributionFourierTransform), is the [[constant function]] on 1:

$$
  \begin{aligned}
    \widehat {\delta}(k)
    & =
    \underset{x \in \mathbb{R}^n}{\int} \delta(x) e^{- 2\pi i k x} \, d x
    \\
    & =
    1
  \end{aligned}
$$

This implies by the [[Fourier inversion theorem]] ([this prop.](Fourier+transform#FourierInversionTheoremForDistributions)) that the [[delta distribution]] itself has equivalently, in [[generalized function]]-notation, the expression

$$
  \label{FourierModeExpansionOfDeltaDistribution}
  \begin{aligned}
    \delta(x)
    & =
    \widehat{\widehat{\delta}}(-x)
    \\
    & =
    \int_{k \in \mathbb{R}^n} e^{2 \pi i k \cdot x} \, d k
  \end{aligned}
$$

in the sense that for every [[function with rapidly decreasing partial derivatives]] $f \in \mathcal{S}(\mathbb{R}^n)$ we have

$$
  \begin{aligned}
    f(x)
    & =
    \underset{y \in \mathbb{R}^n}{\int}
    f(y) \delta(y-x)  \, dvol(y)
    \\
    & =
    \underset{y \in \mathbb{R}^n}{\int}
    \underset{k \in \mathbb{R}^n}{\int}
    f(y) e^{2 \pi i k \cdot (y-x)}
    \, dvol(k)\, dvol(y)
    \\
    & =
    \underset{k \in \mathbb{R}^n}{\int}
    e^{- 2 \pi i k \cdot x}
    \underset{= (-1)^n\widehat{f}(-k)}{
    \underbrace{
      \underset{y \in \mathbb{R}^n}{\int}
      f(y) e^{2 \pi i k \cdot y}
      \, dvol(y)
    }  
    }
    \, dvol(k)
    \\
    & = 
    \widehat{\widehat{f}}(-x)
  \end{aligned}
$$

which is just the statement of the [[Fourier inversion theorem]] for smooth functions ([this prop.](Fourier+transform#FourierInversion)).

=--



### Relation to point-supported distributions

It is clear that:

The delta distribution is a [[compactly supported distribution]], and in fact a [[point-supported distribution]].

+-- {: .num_prop #PointSupportedDistributionsAreSumsOfDerivativesOfDeltaDistibutions}
###### Proposition

Every [[point-supported distribution]] $u$  with $supp(u) = \{p\}$ is a [[finite set|finite]] [[sum]] of multiplies of [[derivative of a distribution|derivatives]] of the delta distribution at that point:

$$
  u = 
  \underset{ {\alpha \in \mathbb{N}^n} \atop { {\vert \alpha\vert} \leq k } }{\sum}  c^\alpha \partial_\alpha \delta(p)
$$

where $\{c^\alpha \in \mathbb{R}\}_\alpha$,
and for $k \in \mathbb{N}$ the [[order of a distribution|order]] of $u$.

=--

(e.g. [H&#246;rmander 90, theorem 2.3.4](#Hoermander90))


## Related entries

* [[Green's function]]

* [[Kronecker delta]]

* [[Dirac measure]]

## References


* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990


[[!redirects Dirac distribution]]
[[!redirects Dirac distributions]]
[[!redirects Dirac delta-distribution]]
[[!redirects Dirac delta-distributions]]
[[!redirects Dirac delta distribution]]
[[!redirects Dirac delta distributions]]
[[!redirects delta-distribution]]
[[!redirects delta-distributions]]
[[!redirects delta distribution]]
[[!redirects delta distributions]]


[[!redirects ∞-distribution]]
[[!redirects ∞-distributions]]
[[!redirects Dirac ∞-distribution]]
[[!redirects Dirac ∞-distributions]]

[[!redirects Dirac delta]]
[[!redirects Dirac deltas]]
[[!redirects Dirac δ]]

[[!redirects delta-function]]
[[!redirects delta-functions]]
[[!redirects delta function]]
[[!redirects delta functions]]
[[!redirects ∞-function]]
[[!redirects ∞-functions]]
[[!redirects Dirac delta-function]]
[[!redirects Dirac delta-functions]]
[[!redirects Dirac delta function]]
[[!redirects Dirac delta functions]]
[[!redirects Dirac ∞-function]]
[[!redirects Dirac ∞-functions]]

[[!redirects Dirac functional]]

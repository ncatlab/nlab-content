
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

+-- {: .num_prop #FourierTransform}
###### Proposition
**([[Fourier transform of a distribution|Fourier transform]])

The [[Fourier transform]] of the delta-distirbution on $\mathbb{R}^n$ is

$$
  \widehat {\delta}(\vec k)
  \;=\; 
  \int \delta(\vec x) e^{- i \vec x \cdot \vec k} d^n \vec x
$$

and hence the delta distribution itself has the expression

$$
  \delta(\vec x)
  \;=\;
  (2 \pi)^{-n}
  \int
    e^{ i \vec x \cdot \vec k}
  d^n \vec k
  \,.
$$

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
[[!redirects Dirac ?]]

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

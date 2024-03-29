

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

The concept of _derivative of a [[distribution]]_ is the generalization of the concept of [[derivative]] of a [[smooth function]] with distributions thought of as [[generalized functions]]. The concept is uniquely fixed by enforcing the formula for [[integration by parts]] to extend from [[integrals]] against [[compact support|compactly supported]] [[densities]] to distributions.

## Definition

Let $X \subset \mathbb{R}^n$ be an [[open subset]] of [[Euclidean space]] of [[dimension]] $n$. For $\alpha \in \mathbb{N}^n$ a multi-index, write

$$
  \partial_\alpha \coloneqq \frac{\partial^{\alpha_1}}{\partial^{\alpha_1} x^{1}}
  \cdots
  \frac{\partial^{\alpha_n}}{\partial^{\alpha_n} x^{n}}
$$

for the corresponding operation of [[differentiation]] and write

$$
  {\vert \alpha \vert}
  \;\coloneqq\;
  \underoverset{i = 1}{n}{\sum} \alpha_i
$$

for the total degree.

For $u \in \mathcal{D}'(X)$ then its [[derivative]] $\partial_\alpha u \in \mathcal{D}'(X)$ of order $\alpha$ is defined by

$$
  \langle 
    \partial_\alpha u, b
  \rangle 
  \;=\;
  (-1)^{\vert \alpha \vert} \langle u, \partial_\alpha b\rangle
$$

for any [[bump function]] $b$, where $\partial_\alpha b$ is the ordinary [[derivative]] of [[smooth functions]].

(e.g. [H&#246;rmander 90, def. 3.1.1 with (3.1.1)'](#Hoermander90))


## Properties



+-- {: .num_prop #DerivativeOfDistributionRetainsOrShrinksWaveFrontSet}
###### Proposition
**(derivative of distributions retains or shrinks [[wave front set]])**

Taking derivatives of distributions retains or shrinks the [[wave front set]]:

For $u \in \mathcal{D}'(\mathbb{R}^n)$ a distribution and $\alpha \in \mathbb{N}^n$ a multi-index with $D^\alpha$ denoting the corresponding [[partial derivative]], then 

$$
  WF(D^\alpha u) \subset WF(u)
  \,.
$$ 

=--

([H&#246;rmander 90, (8.1.10), p. 256](#Hoermander90))



## Examples


+-- {: .num_prop #DerivativeOfHeavisideDistribution}
###### Proposition

The [[derivative of distributions|distributional derivative]] of the Heaviside distribution $\Theta \in \mathcal{D}'(\mathbb{R})$ is the [[delta distribution]] $\delta \in \mathcal{D}'(\mathbb{R})$:

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


+-- {: .num_example #PointSupportedDistributionsAreSumsOfDerivativesOfDeltaDistibutions}
###### Example

Every [[point-supported distribution]] $u$, hence with $supp(u) = \{p\}$ for some point $p$, is a [[finite set|finite]] [[sum]] of multiplies of derivatives of the [[delta distribution]] at that point:

$$
  u = 
  \underset{ {\alpha \in \mathbb{N}^n} \atop { {\vert \alpha\vert} \leq k } }{\sum}  c^\alpha \partial_\alpha \delta(p)
$$

where $\{c^\alpha \in \mathbb{R}\}_\alpha$,
and for $k \in \mathbb{N}$ the [[order of a distribution|order]] of $u$.

=--

(e.g. [H&#246;rmander 90, theorem 2.3.4](#Hoermander90))

## Related concepts

* [[product of a distribution with a smooth function]]

* [[Fourier transform of distributions]]

## References


* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990


[[!redirects derivatives of a distribution]]

[[!redirects derivative of distributions]]
[[!redirects derivatives of distributions]]


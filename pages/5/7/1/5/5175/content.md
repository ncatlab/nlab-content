
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

## References


* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990


[[!redirects Dirac distribution]]
[[!redirects Dirac distributions]]
[[!redirects Dirac delta-distribution]]
[[!redirects Dirac delta-distributions]]
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

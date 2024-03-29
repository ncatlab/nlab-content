
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

A _point-supported distribution_ is a [[distribution]] whose [[support of a distribution]] is a single point. These turn out to be precisely the sums of multiples of the [[delta distribution]] and its [[derivative of a distribution|derivatives]] at that point (prop. \ref{PointSupportedDistributionsAreSumsOfDerivativesOfDeltaDistibutions} below).



## Definition

+-- {: .num_defn #PointSupportedDistribution}
###### Definition


A [[distribution]] $u \in \mathcal{D}'(X)$ is _point-supported_ if its [[support of a distribution]] is a [[singleton]] set:

$$
  supp(u) = \{p\}
$$

for some $p \in X$.

=--

## Properties


+-- {: .num_prop #PointSupportedDistributionsAreSumsOfDerivativesOfDeltaDistibutions}
###### Proposition

Every point-supported distribution $u$ (def. \ref{PointSupportedDistribution}) with $supp(u) = \{p\}$ is a [[finite set|finite]] [[sum]] of multiplies of [[derivative of a distribution|derivatives]] of the [[delta distribution]] at that point:

$$
  u = 
  \underset{ {\alpha \in \mathbb{N}^n} \atop { {\vert \alpha\vert} \leq k } }{\sum}  c^\alpha \partial_\alpha \delta(p)
$$

where $\{c^\alpha \in \mathbb{R}\}_\alpha$,
and for $k \in \mathbb{N}$ the [[order of a distribution|order]] of $u$.

=--

(e.g. [H&#246;rmander 90, theorem 2.3.4](#Hoermander90))

Clearly a point-supported distribution is in particular a [[compactly supported distribution]].

## Related concepts

* [[extension of distributions]]

## References

* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

[[!redirects point-supported distributions]]

[[!redirects point supported distribution]]
[[!redirects point supported distributions]]


[[!redirects distribution supported at a point]]
[[!redirects distributions supported at points]]

[[!redirects distribution with point support]]
[[!redirects distributions with point support]]

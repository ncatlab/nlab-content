
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

A [[distribution]], being a [[generalized function]], is called _non-singular_ if it is (defined by) an actual [[smooth function]] (def. \ref{NonSingularCompactlySupportedDistributions} below). The subspace of non-singular distributions is a [[dense subspace]] of that of all distributions.

## Definition

+-- {: .num_defn #NonSingularCompactlySupportedDistributions}
###### Definition
**(non-singular distributions)

For $n \in \mathbb{N}$, a [[smooth function]] $b \in C^\infty(\mathbb{R}^n)$  induces a [[distribution]]

$$
  \int_{\mathbb{R}^n} (-) b dvol_{\mathbb{R}^n}
  \;\colon\;
  C_{cp}^\infty(\mathbb{R}^n) \longrightarrow \mathbb{R}
$$

by [[integration]] of smooth functions against $b dvol$.

This construction defines a linear inclusion

$$
  C^\infty(\mathbb{R}^n) \hookrightarrow \mathcal{D}'(\mathbb{R}^n)
$$

of the [[real vector space]] of [[smooth functions]] into that of [[distributions]].

The distributions arising this way are called the _non-singular distributions_.

=--



+-- {: .num_defn #SingularSupport}
###### Definition
**([[singular support of a distribution]])**

For $n \in \mathbb{N}$ let $\phi \in \mathcal{D}'(\mathbb{R}^n)$ be a [[distribution]]. Then the _[[singular support of a distribution|singular support]]_  $supp_{sing}(\phi) \subset X$ is the [[subset]] of points such that for every [[open neighbourhood]] $U_x \subset X$ the [[restriction of distributions|restriction]] $\phi\vert_{U_x}$ is singular, hence not a non-singular distribution (def. \ref{NonSingularCompactlySupportedDistributions}).

=--


## Properties


+-- {: .num_prop #NonSingularDistributionsAreDenseInAllDistributions}
###### Proposition
**(non-singular distributions are [[dense subspace|dense]] in all distributions)**

The inclusion of non-singular distributions into all distributions

$$
  C^\infty(\mathbb{R}^n) \hookrightarrow \mathcal{D}'(\mathbb{R}^n)
$$

from def. \ref{NonSingularCompactlySupportedDistributions} exhibits a [[dense subspace]] of $\mathcal{D}'(\mathbb{R}^n)$ (equipped with the [[dual space]] topology, [this def.](dual+vector+space#LinearDualOfATopologicalVectorSpace) or [H&#246;rmander 90, p. 38](#Hoermander90)): 

Every [[distribution]] $u \in \mathcal{D}'(\mathbb{R}^n)$ is the [[limit of a sequence|limit]] of a [[sequence]] $\{f_n \in C^\infty(\mathbb{R}^n)\}_{n \in \mathbb{N}}$ of smooth functions in that for every [[compactly supported function|compactly supported]] [[smooth function]] $\phi \in C^\infty_{cp}(\mathbb{R}^n)$ we have that the value $u(\phi)$ is the [[limit of a sequence|limit]] of [[integrals]]

$$
  u(\phi) 
    \;=\; 
  \underset{n \to \infty}{\lim} \int_{\mathbb{R}^n} \phi(x) f_n(x) dvol(x)
  \,.
$$

=--

([H&#246;rmander 90, theorem 4.1.5](#Hoermander90))


+-- {: .num_defn #DistributionsAsGeneralizedFunctions}
###### Remark

Proposition \ref{NonSingularDistributionsAreDenseInAllDistributions} justifies to think of [[distributions]] as "[[generalized functions]]", and to seek generalizations of standard operations on functions, such as concepts of _[[product of distributions]]_ and _[[composition of distributions]]_.


=--

## References

* {#Hoermander90} [[Lars Hörmander]], section 2.3 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

[[!redirects non-singular distributions]]

[[!redirects regular distribution]]
[[!redirects regular distributions]]



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

The concept of _support of a distribution_ is an evident generalization of [[support]] of a [[continuous functions]] as functions are generalized to [[distributions]].

Of particular interest is the _singular support_ of distributions, which is the subset of those points inside their support around which they are singular when regarded as [[generalized functions]]. This "local analysis" of singularities of distributions may be further refined to their [[microlocal analysis]] by considering not such the singular points, but also the directions of the [[propagation of singularities theorem|propagation of the singularities]] at these points, which is the set of [[covectors]] over the singular support called the _[[wave front set]]_.

## Definition

+-- {: .num_defn #SupportOfADistribution}
###### Definition
**(support of a distribution)**

Let $X$ be a [[smooth manifold]] and let $\phi \colon C^\infty_c(X) \longrightarrow \mathbb{R}$ be a [[distribution]]. Then the _support_ of $\phi$ is the [[subset]] $supp(\phi) \subset X$ of all those points $x \in X$ such that for every [[open neighbourhood]] $U_x \subset X$ the restricted distribution $\phi\vert_{U_x}$ is not the zero-distribution

$$
  supp(\phi) 
  \;\coloneqq\;
  \left\{
    x \in X \;\vert\; \underset{ \text{nbhd}\, U_x }{\forall}\left( \phi\vert_{U_x} \neq 0 \right)
  \right\}
  \,.
$$

=--

(e.g. [H&#246;rmander 90, def. 2.2.2](#Hoermander90))

+-- {: .num_remark}
###### Remark

By construction, the support of a distribution $\phi$ according to def. \ref{SupportOfADistribution} is a [[closed subset]].
If it happens to be a [[compact space|compact]] subset, then the 
distribution is said to be a _[[compactly supported distribution]]_.

=--

(e.g. [H&#246;rmander 90, section 2.3](#Hoermander90))


+-- {: .num_defn #SingularSupport}
###### Definition
**(singular support)**

Let $X$ be a [[smooth manifold]] and let $\phi \colon C^\infty_c(X) \longrightarrow \mathbb{R}$ be a [[distribution]]. Then the _singular support_  $singsupp(\phi) \subset X$ is the [[subset]] of points such that for every [[open neighbourhood]] $U_x \subset X$ the restriction $\phi\vert_{U_x}$ is not represented by a [[smooth function|smooth]] [[density]].

=--

+-- {: .num_remark}
###### Remark
**([[wave front set]])**

A refinement of the information contained in the singular support of a distribution (def. \ref{SingularSupport}) is its _[[wave front set]]_, which over each point of the singular support records those [[covectors]] "along which the singularity propagates", as made precise by the [[propagation of singularities theorem]].

=--

## Properties


+-- {: .num_remark}
###### Remark

If a [[bump function]] $f \in C^\infty_c(X)$ has its ([[compact support|compact]]) [[support]] $supp(f)$ [[disjoint subset|disjoint]] from the support of of a distribution $\phi$ (def. \ref{SupportOfADistribution}), then the [[evaluation]] vanishes:

$$
  supp(f) \cap supp(\phi) = \emptyset
  \;\Rightarrow\;
  \phi(f) = 0
  \,.
$$

=--

(e.g. [H&#246;rmander 90, theorem 2.2.1 and (2.2.1)](#Hoermander90))

## Examples



## Related entries

* [[support]]

* [[point-supported distribution]]

* [[order of a distribution]]

* [[scaling degree of a distribution]]

## References

* {#Hoermander90} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990


[[!redirects support of distributions]]

[[!redirects singular support of a distribution]]

[[!redirects distributional support]]
[[!redirects distributional supports]]


[[!redirects singular support]]
[[!redirects singular supports]]




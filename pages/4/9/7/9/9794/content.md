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

In [[functional analysis]], 

* a [[Schwartz space]] ([Terzioglu 69](#Terzioglu69)) is a [[locally convex topological vector space]] $E$ with the property that whenever $U$ is an [[absolutely convex]] neighbourhood of $0$ then it contains another, say $V$, such that $U$ maps to a [[precompact set]] in the [[normed vector space]] $E_V$.

* _the_ Schwartz space of an open subset of Euclidean space is the space of smoooth functions all whose derivative are rapidly decreasing (def. \ref{RapidlyDecreasingFunction} below). On this space the operation of [[Fourier transform]] is a linear automorphism (prop. \ref{FourierTransformIsIsomorphismOnSchwartzSpace} below). The [[continuous linear functionals]] on this space are the [[tempered distributions]].

## Definition

+-- {: .num_defn #RapidlyDecreasingFunction}
###### Definition
**(function with rapidly decreasing derivatives)**

For $n \in \mathbb{N}$, a [[smooth function]] $f \colon \mathbb{R}^n \to \mathbb{R}$ on the [[Euclidean space]] $\mathbb{R}^n$ has _rapidly decreasing derivatives_ if the [[absolute value]] of the product of any [[derivative]] $\partial_\beta f$ of the function with any [[polynomial]] function is a [[bounded function]]:

$$
  \underset{\alpha, \beta \in \mathbb{N}^n}{\forall}
  \left(
  \underset{x \in \mathbb{R}^n}{sup} {\Vert x^\alpha \partial_{\beta} f(x)  \Vert} \lt 0
  \right)
$$

=--

(e.g. [H&#246;rmander 90, def. 7.1.2](#Hoermander90))

+-- {: .num_defn #SchwartzSpaceOfFunctionsWithRapidlyDecreasingDerivatives}
###### Definition
**(Schwartz space of functions with rapidly decreasing derivatives)**

For $n \in \mathbb{N}$ the _Schwartz space_ $\mathcal{S}(\mathbb{R}^n)$ is the  [[topological vector space]] whose 

* underlying [[real vector space]] is the subspace of the space $C^\infty(\mathbb{R}^n)$ of [[smooth functions]] (with pointwise addition and scalar multiplication) on the functions with rapidly decreasing derivatives (def. \ref{RapidlyDecreasingFunction});

* whose [[topological space|topology]] is that induced b the [[semi-norms]] given by $p_{\alpha,\beta}(f) \coloneqq {\Vert x^\alpha \partial_{\beta} (f)(x)  \Vert}$ is called the _Schwartz space_ $\mathcal{S}(\mathbb{R}^n)$.

=--

(e.g. [H&#246;rmander 90, def. 7.1.2](#Hoermander90))


+-- {: .num_defn #TemperedDistribution}
###### Definition
**([[tempered distributions]])**

A _[[tempered distribution]]_ on $\mathbb{R}^n$ is a [[continuous linear functional]] on the Schwartz space $\mathcal{S}(\mathbb{R}^n)$ (def. \ref{SchwartzSpaceOfFunctionsWithRapidlyDecreasingDerivatives}).

=--


(e.g. [H&#246;rmander 90, def. 7.1.7](#Hoermander90))

## Properties

+-- {: .num_prop #FourierTransformIsIsomorphismOnSchwartzSpace}
###### Proposition
**([[Fourier transform]] is linear automorphism of Schwartz space)**

For $n \in \mathbb{N}$ the operation of [[Fourier transform]] $f \mapsto \hat f$ is well defined on all smooth functions on $\mathbb{R}^n$ with rapidly decreasing derivatives (def. \ref{RapidlyDecreasingFunction}) and indeed constitutes a [[linear isomorphism]] from the Schwartz space (def. \ref{SchwartzSpaceOfFunctionsWithRapidlyDecreasingDerivatives}) to itself:

$$
  \widehat {(-)}
  \;\colon\;
  \mathcal{S}(\mathbb{R}^n)
    \longrightarrow
  \mathcal{S}(\mathbb{R}^n)
$$

=--

(e.g. [Melrose 03, theorem 1.3](#Melrose03))

## References


* {#Terzioglu69} T. Terzioglu, _On Schwartz spaces_,  Mathematische Annalen September 1969, Volume 182, Issue 3, pp 236&#8211;242  ([web](https://link.springer.com/article/10.1007/BF01350326))

* {#Hoermander90} [[Lars Hörmander]], section 7.1 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

* {#Melrose03} [[Richard Melrose]], chapter 1 of _Introduction to microlocal analysis_, 2003 ([pdf](http://www-math.mit.edu/~rbm/iml90.pdf))


* Wikipedia, _[Schwartz space](https://en.wikipedia.org/wiki/Schwartz_space)_

[[!redirects smooth function with rapidly decreasing derivatives]]
[[!redirects smooth functions with rapidly decreasing derivatives]]


[[!redirects function with rapidly decreasing derivatives]]
[[!redirects functions with rapidly decreasing derivatives]]
[[!redirects rapidly decreasing derivatives]]


category: functional analysis
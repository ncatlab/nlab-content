
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Two-variable and $n$-variable adjunctions
* table of contents
{: toc}

## Idea

An _adjunction of two variables_ is a straightforward generalization of both:

* the [[internal hom]] in a [[biclosed monoidal category]] 

and

* a $V$-[[enriched category]] having [[powers]] and [[copowers]]

by extracting the central pattern.

## Definition

Let $C$, $D$ and $E$ be [[category|categories]]. An **adjunction of two variables** or **two-variable adjunction**

$$
 (\otimes, hom_l, hom_r) : C \times D \to E
$$

consists of [[bifunctors]]

$$
\begin{aligned}
  \otimes & : C \times D \to E
  \\
  hom_l &: C^{op} \times E \to D
  \\
  hom_r &: D^{op} \times E \to C
\end{aligned}
$$

together with natural [[isomorphism]]s

$$
  Hom_E(c \otimes d, e)
  \simeq
  Hom_C(c, hom_l(d,e))
  \simeq
  Hom_D(d, hom_r(c,e))
  \,.
$$

## Cyclicity

If $(\otimes, hom_l, hom_r) : C \times D \to E$ is a two-variable adjunction, then so are
$$
 (hom_l^{op}, \otimes^{op}, hom_r) : E^{op} \times C \to D^{op}
$$
and
$$
 (hom_r^{op}, hom_l, \otimes^{op}) : D\times E^{op} \to C^{op}.
$$
giving an action of the [[cyclic group]] of order 3.  This can be made to look more symmetrical by regarding the original two-variable adjunction as a "two-variable left adjunction" $C\times D \to E^{op}$; see [Cheng-Gurski-Riehl](#CGR).

## Adjunctions of $n$ variables

There is a straightforward generalization to an adjunction of $n$ variables, which involves $n+1$ categories and $n+1$ functors.  Adjunctions of $n$ variables assemble into a 2-[[multicategory]].  They also have a corresponding notion of [[mates]]; see [Cheng-Gurski-Riehl](#CGR).

This 2-multicategory can also be promoted to a 2-[[polycategory]]; see [Shulman](#Shulman).

## Related concepts

* [[Quillen bifunctor]]

## References

* [[John Gray]], *Closed categories, lax limits and homotopy limits*. J. Pure Appl. Algebra 19 (1980), 127--158.  Possibly the oldest abstract definition of the concept, under the name "THC-situation".

* [[Mark Hovey]]. *Model Categories*, volume 63 of Mathematical Surveys and Monographs. American Mathematical Society, 1999.  See Chapter 4.

* [[Rene Guitart]], *Trijunctions and triadic Galois connections*. Cah. Topol. Géom. Différ. Catég. 54 (2013), no. 1, 13--27.

* {#CGR} [[Eugenia Cheng]], [[Nick Gurski]], [[Emily Riehl]], "Multivariable adjunctions and mates", [arXiv:1208.4520](http://arxiv.org/abs/1208.4520).

* {#Shulman} [[Mike Shulman]], *The 2-Chu-Dialectica construction and the polycategory of multivariable adjunctions*, [arxiv:1806.06082](https://arxiv.org/abs/1806.06082), [blog post](https://golem.ph.utexas.edu/category/2017/11/the_polycategory_of_multivaria.html)

[[!redirects two-variable adjunction]]
[[!redirects two-variable adjunctions]]
[[!redirects 2-variable adjunction]]
[[!redirects 2-variable adjunctions]]
[[!redirects adjunction of two variables]]
[[!redirects adjunctions of two variables]]
[[!redirects adjunction of 2 variables]]
[[!redirects adjunctions of 2 variables]]
[[!redirects n-variable adjunction]]
[[!redirects n-variable adjunctions]]
[[!redirects adjunction of n variables]]
[[!redirects adjunctions of n variables]]
[[!redirects multivariable adjunction]]
[[!redirects multivariable adjunctions]]
[[!redirects multi-variable adjunction]]
[[!redirects multi-variable adjunctions]]

[[!redirects THC-situation]]
[[!redirects THC situation]]
[[!redirects THC-situations]]
[[!redirects THC situations]]

[[!redirects trijunction]]
[[!redirects trijunctions]]

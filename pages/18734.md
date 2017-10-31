[[!redirects non-singular distributions]]

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

A [[distribution]], being a [[generalized function]] is called _non-singular_ if it is (defined by) an actual [[smooth function]].

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

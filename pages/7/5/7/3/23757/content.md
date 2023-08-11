
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition ##

Given a [[dense linear order]] $A$ and a [[countable dense linear order]] $B$ such that $B \subseteq A$, a **$B$-indexed locator** for an [[element]] $c \in A$ is a family of functions [[indexed set|indexed]] by the [[cartesian product]] [[set]] $B \times B$ 

$$(a, b) \in B \times B \vdash l(a, b) \in (\mathrm{OpenInt}(a,c) \uplus \mathrm{OpenInt}(c,b))^{\mathrm{OpenInt}(a,b)}$$ 

or equivalently an element of the indexed [[cartesian product]]

$$l \in \prod_{a \in B} \prod_{b \in B} (\mathrm{OpenInt}(a,c) \uplus \mathrm{OpenInt}(c,b))^{\mathrm{OpenInt}(a,b)}$$

Equivalently, a **$B$-indexed locator** is a [[family]] of [[pairs]] of [[functions]] [[indexed set|indexed]] by the [[cartesian product]] [[set]] $B \times B$ 

$$(a, b) \in B \times B \vdash l(a, b) \in \mathrm{OpenInt}(a,c)^{\mathrm{OpenInt}(a,b)} \times \mathrm{OpenInt}(c,b)^{\mathrm{OpenInt}(a,b)}$$ 

or equivalently an element of the indexed [[cartesian product]]

$$l \in \prod_{a \in B} \prod_{b \in B} \mathrm{OpenInt}(a,c)^{\mathrm{OpenInt}(a,b)} \times \mathrm{OpenInt}(c,b)^{\mathrm{OpenInt}(a,b)}$$

where $\mathrm{OpenInt}(a,b)$, $\mathrm{OpenInt}(a,c)$, $\mathrm{OpenInt}(c,b)$ are [[open intervals]] in $A$. 

## Properties ##

* A locator is equivalent to having the structure of a [[Cauchy sequence]] with [[modulus of convergence]]. This is stronger than merely being a [[modulated Cauchy real number]].

* That every [[Dedekind real number]] has a $\mathbb{Q}$-indexed locator implies the weak [[limited principle of omniscience]]. 

## See also ##

* [[Dedekind cut]]
* [[Dedekind cut structure]]
* [[dense linear order]]
* [[lifting to locators]]

## References ##

* [[Auke Booij]], *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

[[!redirects locators]]


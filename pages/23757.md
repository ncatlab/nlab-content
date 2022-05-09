
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

Given a [[dense linear order]] $A$ and a [[countable dense linear order]] $B$ such that $B \subseteq A$, a **$B$-indexed locator** for an [[element]] $c \in A$ is an element of the indexed [[cartesian product]] of the [[family]] of [[functions]] 

$$\left(]a,b[ \to (]a,c[ + ]c,b[)\right)_{(a,b) \in B \times B}$$ 

[[indexed set|indexed]] by the [[cartesian product]] [[set]] $B \times B$ 

$$l \in \prod_{a:B} \prod_{b:B} ]a,b[ \to (]a,c[ + ]c,b[)$$

where $]a,b[$, $]a,c[$, $]c,b[$ are [[open intervals]] in $A$. 

## Properties ##

* That every [[Dedekind real number]] has a $\mathbb{Q}$-indexed locator implies the weak [[limited principle of omniscience]]. 

* That every [[modulated Cauchy real number]] has a $\mathbb{Q}$-indexed locator implies that the modulated Cauchy real numbers are [[sequentially complete]]. 

## See also ##

* [[Dedekind cut]]
* [[dense linear order]]
* [[lifting to locators]]

## References ##

* Auke Booij, *Extensional constructive real analysis via locators*, ([abs:1805.06781](https://arxiv.org/abs/1805.06781))

[[!redirects locators]]


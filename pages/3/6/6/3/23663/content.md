[[!redirects prealgebra real numbers]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

The real numbers as encountered in prealgebra. 

## Definition ##

Let $R$ be an [[Archimedean integral domain]] and let $[0, 1]_R$ be the [[unit interval]] in $R$. Let $a:\mathbb{N} \to [0, 9]_\mathbb{N}$ be a sequence of decimal digits, where $n \in [0, 9]_\mathbb{N}$ is the set of all natural numbers $0 \leq n \leq 9$, and let $\mathcal{I}:[0, 9]_\mathbb{N} \to F$ be the canonical embedding of $[0, 9]_\mathbb{N}$ into $R$. The __prealgebra real numbers__ $\mathbb{R}$ is the [[initial object|initial]] [[Archimedean integral domain]] such that for every such sequence $a:\mathbb{N} \to [0, 9]_\mathbb{N}$, the [[sequence]] 

$$b(n) \coloneqq \sum_{i=0}^{n} \frac{\mathcal{I}(a_i)}{10^{i+1}}$$

has a [[limit of a sequence|limit]] in the [[unit interval]] $[0, 1]_\mathbb{R}$.

## Properties ##

If the [[limited principle of omniscience]] is true, then every [[Cauchy real number]] is a prealgebra real number. 

## See also ##

* [[real numbers]]
* [[limited principle of omniscience]]
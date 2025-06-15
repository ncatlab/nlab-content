
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Material set theory
* table of contents
{: toc}

## Overview

__Material set theory__ (also called _membership-based set
theory_) is a style of [[set theory]] with a primitive global membership relation "$\in$" where sets are characterized only by "$\in$" and [[propositional equality]] of sets. (The terminology 'material', or at least 'materialistic', goes back at least to [Friedman 1997](#Friedman1997).) Material set theory contrasts with *[[structural set theory]]* (cf. *[[material versus structural set theory]]*), as well as with set theories which are neither structural nor material. Material set theories are [[simple type theory|simply sorted]] [[set theory]]. 

## Material higher groupoid theory

In [[dependent type theory]], there has been a recent development generalizing material set theories from sets to [[higher groupoids]] in [Gylterud and Stenholm 2023](#GS23). The key distinction between what can be called *material higher groupoid theory* and the traditional material set theory discussed in the literature is that the membership type family $x \in y$ is not necessarily a [[mere proposition]]. 

What these material higher groupoid theories have in common with material set theory is that assuming the [[axiom of extensionality]] violates the [[principle of equivalence]]: if the membership type family $x \in y$ is an $n$-groupoid for all $x:V$ and $y:V$, then $V$ is an $(n + 1)$-groupoid by the axiom of extensionality, and the [[universal type family]] $\left(\sum_{x:V} x \in y\right)_{y:V}$ is a family of $(n + 1)$-groupoids, meaning that the object type of the $(n + 2, 1)$-category of objects in $V$ is an $(n + 1)$-groupoid and [[Rezk completion|does not coincide]] with the [[core]] $(n + 2)$-groupoid. 

## Related concepts

* [[cumulative hierarchy]]

* [[unsorted set theory]]

* [[two-sorted set theory]]

* [[set-theoretic multiverse]]

* [[material versus structural set theory]]

* [[principle of equivalence]]

## References

* {#GS23} [[Håkon Robbestad Gylterud]], [[Elisabeth Stenholm]], *Univalent material set theory* ([arXiv:2312.13024](https://arxiv.org/abs/2312.13024))

Relation to [[structural set theory]] is discussed in

* {#Shulman18} [[Michael Shulman]], _Comparing material and structural set theories_ ([arXiv:1808.05204](https://arxiv.org/abs/1808.05204))

See also

* {#Friedman1997} [[Harvey Friedman]] (1997). [Foundational Completeness](https://cs.nyu.edu/pipermail/fom/1997-November/000143.html). FOM, 1997 November.

[[!redirects material set theory]]
[[!redirects material set theories]]

[[!redirects material higher groupoid theory]]
[[!redirects material higher groupoid theories]]

[[!redirects material infinity-groupoid theory]]
[[!redirects material infinity-groupoid theories]]
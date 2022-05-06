[[!redirects Complete theory ]]
[[!redirects complete ]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

**Deductive completeness** is maximality condition on a [[logical theory]] $\mathbb{T}$ saying that the deductive closure of $\mathbb{T}$ is as large as possible within the bounds of consistency.


## Definition (in classical model theory)

Let $\mathbb{T}$ be a consistent logical theory over signature $\Sigma$. $\mathbb{T}$ is called _complete_ if for any sentence $\sigma$ over $\Sigma$ either $\mathbb{T}\vdash \sigma$ or $\mathbb{T}\cup\sigma$ is inconsistent.

## The case of geometric logic

A [[geometric theory]] $\mathbb{T}$ over a signature $\Sigma$ is called _complete_ if for any geometric sentence $\sigma$ over $\Sigma$ is either $\mathbb{T}$-provably equivalent to $\top$ or to $\bot$, but not both.

+-- {: .num_theorem}
###### Proposition
A geometric theory $\mathbb{T}$ is complete iff the [[classifying topos]] of $\mathbb{T}$ is [[two-valued topos|two-valued]].
=--

This occurs as remark 2.5 in Caramello ([2012](#Ca12)).

Remark: a first-order theory $\mathbb{T}$ is complete in the sense of classical model theory iff its [[coherent logic|Morleyization]] is complete in the sense of geometric logic.

## Related entries

* [[Gödel's incompleteness theorem]]

* [[compactness theorem]]

* [[model complete theory]]

* [[substructure completeness]]

* [[two-valued topos]]

## References

* {#Ca12}[[Olivia Caramello]], _Atomic toposes and countable categoricity_ , Appl. Cat. Struc. **20** no. 4 (2012) pp.379-391. ([arXiv:0811.3547](http://arxiv.org/abs/0811.3547))

* C. C. Chang, [[Jerome Keisler|H. J. Keisler]], _Model theory_ , North-Holland Amsterdam 1973.
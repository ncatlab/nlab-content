
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


# Quasi-Borel Space
* table of contents
{: toc}

## Idea

A **quasi-Borel space** (QBS) is a [[set]] equipped with a notion of _[[random variable]]_, providing a model of [[measurable space]] suitable for [[probability theory]]. The advantage of quasi-Borel spaces over traditional formulations is that they provide a nice [[category]] of [[measurable spaces]]: it is [[cartesian closed category|cartesian closed]], and the set of [[probability measures]] of a QBS forms a QBS.

## Definition

A quasi-Borel space $X$ consists of an underlying [[set]] $|X|$ and a set of [[functions]] $M_X \subseteq (\mathbb{R} \to |X|)$ satisfying:

1. $M_X$ contains all [[constant functions]].
2. $M_X$ is closed under [[composition]] with [[measurable functions]]: if $f : \mathbb{R} \to \mathbb{R}$ is measurable and $\alpha \in M_X$, $\alpha \circ f \in M_X$.
3. $M_X$ is closed under gluing functions with [[disjoint union|disjoint]] [[Borel subset|Borel]] domains: for any partition $\mathbb{R} = \biguplus_{i\in\mathbb{N}} S_i$ by Borel $S_i$, and $\{\alpha_i \in M_X\}_{i\in\mathbb{N}}$, then the function $\beta(x) = \alpha_i(x)$ when $x \in S_i$ is in $M_X$.

## Applications

The category of quasi-Borel spaces can be used as a [[denotational semantics]] for higher-order [[probabilistic programming languages]].

## As a quasitopos of concrete sheaves

The category of quasi-Borel spaces is the category of [[concrete sheaves]] on the category of standard Borel spaces considered with the [[extensive category#Superextensive sites|extensive coverage]].  As such, quasi-Borel spaces form a Grothendieck [[quasitopos]]. 
(A standard Borel space is a [[measurable space]] that is a retract of $\mathbb{R}$, equivalently, it is a measurable space that comes from a [[Polish space]], equivalently, it is either isomorphic to $\mathbb{R}$ or countable, discrete and non-empty.)


## Related Concepts

* [[quasi-topological space]]
* [[subsequential space]]
* [[concrete sheaf]]

## References

Quasi-Borel spaces were introduced in 

* [[Chris Heunen]], Ohad Kammar, [[Sam Staton]] and Hongseok Yang, _A convenient category for higher-order probability theory_, Logic in Computer Science 2017 ([arXiv:1701.02547](https://arxiv.org/abs/1701.02547))

[[!redirects quasi-Borel spaces]]
[[!redirects quasi-Borel structure]]
[[!redirects quasi-Borel structures]]
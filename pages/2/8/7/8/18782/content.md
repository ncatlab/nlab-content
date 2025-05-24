
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

A **quasi-Borel space** (QBS) is a [[set]] equipped with a notion of _[[random variable]]_, providing a model of [[measurable space]] suitable for [[probability theory]]. The advantage of quasi-Borel spaces over traditional formulations is that they provide a nice [[category]] of [[measurable spaces]]: it is [[cartesian closed category|cartesian closed]], and the set of [[probability measures]] of a QBS forms a QBS.

## Definition

A quasi-Borel space $X$ consists of an underlying [[set]] $|X|$ and a set of [[functions]] $M_X \subseteq (\mathbb{R} \to |X|)$ satisfying:

1. $M_X$ contains all [[constant functions]].
2. $M_X$ is closed under [[composition]] with [[measurable functions]]: if $f : \mathbb{R} \to \mathbb{R}$ is measurable and $\alpha \in M_X$, then $\alpha \circ f \in M_X$.
3. $M_X$ is closed under gluing functions with [[disjoint union|disjoint]] [[Borel subset|Borel]] domains: for any partition $\mathbb{R} = \biguplus_{i\in\mathbb{N}} S_i$ by Borel $S_i$, and $\{\alpha_i \in M_X\}_{i\in\mathbb{N}}$, then the function $\beta(x) = \alpha_i(x)$ when $x \in S_i$ is in $M_X$.

A morphism of quasi-Borel spaces is a function that respects composition with these functions. 

For example, $\mathbb{R}$ is a quasi-Borel space, with the Borel functions. The two-element set $2$ is a quasi-Borel space, with the functions that are characteristic functions of [[Borel subsets]]. 

The category of quasi-Borel spaces is [[cartesian closed]], unlike the category of [[measurable spaces]].

## Applications

The category of quasi-Borel spaces can be used as a [[denotational semantics]] for higher-order [[probabilistic programming languages]].

## As a quasitopos of concrete sheaves

The category of quasi-Borel spaces is the category of [[concrete sheaves]] on the category of standard Borel spaces considered with the [[extensive category#Superextensive sites|extensive coverage]].  As such, quasi-Borel spaces form a Grothendieck [[quasitopos]]. 
(A standard Borel space is a [[measurable space]] that is a retract of $\mathbb{R}$, equivalently, it is a measurable space that comes from a [[Polish space]], equivalently, it is either isomorphic to $\mathbb{R}$ or countable, discrete and non-empty.)

## Connection to measurable spaces

There is an [[adjunction]] between quasi-Borel spaces and [[measurable spaces]] (related to the [[nerve and realization]] construction). 

$$
   Meas \stackrel{\leftarrow}{\rightarrow} Qbs,
$$

The right adjoint takes a measurable space $X$ to the quasi-Borel space where $M_X$ comprises the measurable functions. The left adjoint regards a quasi-Borel space $X$ with the sigma-algebra comprising all those sets $U\subseteq X$ for which the characteristic function $X\to 2$ is a morphism. 

## Probability distributions

A _probability measure_ on a quasi-Borel space is defined to be a function $\mathbb{R}\to X$ in $M_X$. This is regarded as a [[random variable]]. In particular we regard two probability measures as equal if the [[law of a random variable|laws]] are the same [[probability distributions]] on the underlying measurable spaces, when $\mathbb{R}$ is regarded with the uniform distribution on $[0,1]$. 

This leads to an affine, [[commutative monad]] on the category of quasi-Borel spaces. Restricted to standard Borel spaces, it agrees with the [[Giry monad]]. 


The monad can be regarded as a [[probability monad]], and  its [[Kleisli category]] is a [[Markov category]]. 

## Related Concepts

* [[quasi-topological space]]
* [[subsequential space]]
* [[concrete sheaf]]
* [[standard Borel space]]

## References

Quasi-Borel spaces were introduced in 

* [[Chris Heunen]], Ohad Kammar, [[Sam Staton]] and Hongseok Yang, _A convenient category for higher-order probability theory_, Logic in Computer Science 2017 ([arXiv:1701.02547](https://arxiv.org/abs/1701.02547))

[[!redirects quasi-Borel spaces]]
[[!redirects quasi-Borel structure]]
[[!redirects quasi-Borel structures]]
# Quasi-Borel Space
* table of contents
{: toc}

## Idea

A **quasi-Borel space** (QBS) is a set equipped with a notion of _random variable_, providing a model of measurable space suitable for [[probability theory]]. The advantage of quasi-Borel spaces over traditional formulations is that they provide a nice category of measurable spaces: it is cartesian closed, and the set of [[probability measures]] of a QBS forms a QBS.

## Definition

A quasi-Borel space $X$ consists of an underlying set $|X|$ and a set of functions $M_X \subset \mathbb{R} \to |X|$ satisfying:

1. $M_X$ contains all constant functions.
2. $M_X$ is closed under composition with measurable functions: if $f : \mathbb{R} \to \mathbb{R}$ is measurable and $\alpha \in M_X$, $\alpha \circ f \in M_X$.
3. $M_X$ is closed under gluing functions with disjoint, Borel domains: for any partition $\mathbb{R} = \uplus_{i\in\mathbb{N}} S_i$ by Borel $S_i$, and $\{\alpha_i \in M_X\}_{i\in\mathbb{N}}$, then the function $\beta(x) = \alpha_i(x)$ when $x \in S_i$ is in $M_X$.

## Applications

The category of quasi-Borel spaces can be used as a [[denotational semantics]] for higher-order [[probabilistic programming languages]].

## Related Concepts

* [[quasi-topological space]]
* [[subsequential space]]
* [[concrete sheaf]]

## References

quasi-Borel spaces were introduced in 

* Chris Heunen, Ohad Kammar, [[Sam Staton]] and Hongseok Yang, _A convenient cateogry for higher-order probability theory_, Logic in Computer Science 2017

[[!redirects quasi-Borel spaces]]

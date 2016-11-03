
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of _length_ of an [[object]] in a suitable [[category]] $\mathcal{C}$ is akin to the concept of [[dimension]] of [[vector spaces]], to which it reduces in the case that $\mathcal{C} = $ [[Vect]]. The 1-dimensional vector space is a [[simple object]], and the [[dimension]] of a vector space $V$, if it is finite, may be thought of as the number of times that one may split off such a simple object from $V$. The definition of _length_ generalizes this concept, notably to [[modules]] over some [[ring]].

## Definition

Given an [[object]] $X$ in a suitable [[tensor category]], then a _Jordan-H&#246;lder sequence_ or _composition series_ for $X$ is a [[filtration]]

$$
  0 = X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X_{n-1} \hookrightarrow X_n = X
$$

such that for all $i$ then the [[quotient]] $X_i/X_{i-1}$ exists and is a [[simple object]].

If this exists, then under suitable conditions $n$ is uniquely specified and is then called the _length_ of $X$.

## References

* [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], section 1.5 in  _Topics in Lie theory and Tensor categories -- 9 Tensor categories_, Lecture notes (spring 2009) ([pdf](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/MIT18_769S09_lec09.pdf) [web](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/)) 

* Wikipedia, _[Composition series](https://en.wikipedia.org/wiki/Composition_series)_

[[!redirects lenghts of objects]]

[[!redirects Jordan-Hölder series]]
[[!redirects Jordan-Holder series]]

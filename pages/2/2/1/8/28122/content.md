+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Dual Stiefel-Whitney classes_ are $\mathbb{Z}_2$-valued [[characteristic classes]] for real [[vector bundles]]. The total [[Stiefel-Whitney class]] is invertible in the [[cohomology ring]] (using $w_0=1$ and the [[geometric series]]) and the dual Stiefel-Whitney classes are then the components of its inverse, meaning in particular that they can be expressed by [[Stiefel-Whitney classes]] again and carry the exact same information. Nonetheless, dual Stiefel-Whitney classes can be used to simplfy calculations. An important application is the description of embedding problems.

## Definition

Let $E\twoheadrightarrow B$ be a real [[vector bundle]] of rank $n$ with total [[Stiefel-Whitney class]] $w(E)\in H^*(B,\mathbb{Z}_2)$, then its total dual Stiefel-Whitney class $\overline{w}(E)\in H^*(B,\mathbb{Z}_2)$ is defined by:
$$
w(E)\overline{w}(E)
=1.
$$
If the [[Stiefel-Whitney classes]] are known, then the equation can be solved inductively due to their linear and triangular form. Solving the equation in order $n$ yields:
$$
\overline{w}_n(E)
=-\sum_{k=1}^n w_k(E)\overline{w}_{n-k}(E).
$$
Another direct computation uses the [[geometric series]]:
$$
\overline{w}(E)
=w(E)^{-1}
=\left(
1+\sum_{k=1}^n w_k(E)
\right)^{-1}
=\sum_{l\in 0}^\infty\left(
\sum_{k=1}^n w_k(E)
\right)^l.
$$

## Examples

Low dual Stiefel-Whitney classes are:
$$
\overline{w}_0
=1;
$$
$$
\overline{w}_1
=-w_1;
$$
$$
\overline{w}_2
=-w_2
+w_1^2.
$$

## Related concepts

* [[Serge class]] (dual Chern class)

## References

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))

[[!redirects dual Stiefel-Whitney classes]]
[[!redirects total dual Stiefel-Whitney class]]
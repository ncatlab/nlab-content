[[!redirects Serge class]]
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

_Segre classes_ (or _dual Chern classes_) are $\mathbb{Z}$-valued [[characteristic classes]] for complex [[vector bundles]]. The total [[Chern class]] is invertible in the [[cohomology ring]] (using $c_0=1$ and the [[geometric series]]) and the Segre classes are then the components of its inverse, meaning in particular that they can be expressed by [[Chern classes]] again and carry the exact same information. Nonetheless, Segre classes can be used to simplfy calculations.

## Definition

Let $E\twoheadrightarrow B$ be a complex [[vector bundle]] of rank $n$ with total [[Chern class]] $c(E)\in H^*(B,\mathbb{Z})$, then its total Segre class $s(E)\in H^*(B,\mathbb{Z})$ is defined by:
$$
c(E)s(E)
=1.
$$
If the [[Chern classes]] are known, then the equation can be solved inductively due to their linear and triangular form. Solving the equation in order $n$ yields:
$$
s_n(E)
=-\sum_{k=1}^n c_k(E)s_{n-k}(E).
$$
Another direct computation uses the [[geometric series]]:
$$
s(E)
=c(E)^{-1}
=\left(
1+\sum_{k=1}^n c_k(E)
\right)^{-1}
=\sum_{l\in 0}^\infty\left(
\sum_{k=1}^n c_k(E)
\right)^l.
$$

## Examples

Low Segre classes are:
$$
s_0
=1;
$$
$$
s_1
=-c_1;
$$
$$
s_2
=-c_2
+c_1^2.
$$

## Properties

For complex [[vector bundles]] $E,F\twoheadrightarrow B$, one has $c(E\oplus F)=c(E)c(F)$, meaning that $c(F)=s(E)c(E\oplus F)$. In particular, if $B$ is a [[compact]] [[Hausdorff space]], then for every $E$ there exists a $F$ with $E\oplus F\cong\mathbb{R}^n$, ([Hatcher 17, Prop. 1.4](#Hatcher17)) which with $w(E\oplus F)=w(\mathbb{R}^n)=1$ makes the formula simplify to:
$$
s(E)
=c(F).
$$
Hence in this case the Segre classes can be seen as the Chern classes of a complement to a trivial bundle.

## Related concepts

* [[dual Stiefel-Whitney class]]

## References

* {#Hatcher17} [[Allen Hatcher]]: _Vector bundles and K-Theory_, book draft (2017) &lbrack;[webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf)&rbrack;

[[!redirects Segre classes]]
[[!redirects total Segre class]]

[[!redirects dual Chern class]]
[[!redirects dual Chern classes]]
[[!redirects total dual Chern class]]
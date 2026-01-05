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

## Properties

For real [[vector bundles]] $E,F\twoheadrightarrow B$, one has $w(E\oplus F)=w(E)w(F)$, meaning that $w(F)=\overline{w}(E)w(E\oplus F)$. In particular, if $B$ is a [[compact]] [[Hausdorff space]], then for every $E$ there exists a $F$ with $E\oplus F\cong\mathbb{R}^n$, ([Hatcher 17, Prop. 1.4](#Hatcher17)) which with $w(E\oplus F)=w(\mathbb{R}^n)=1$ makes the formula simplify to:
$$
\overline{w}(E)
=w(F).
$$
Hence in this case the dual Stiefel-Whitney classes can be seen as the Stiefel-Whitney classes of a complement to a trivial bundle.

Using this fact, an imporant application of the dual Stiefel-Whitney classes are embedding problems. For a $n$-dimensional [[smooth manifold]] $M$ and a smooth [[embedding]] $M\hookrightarrow\mathbb{R}^{n+k}$, the [[Whitney embedding theorem]] assures one can chose $k\leq n-1$ while the dual Stiefel-Whitney classes give a lower bound. Using the standard [[scalar product]] on $\mathbb{R}^{n+k}$ and [[orthogonal]] subspaces, there is a [[normal bundle]] $N_i M\twoheadrightarrow M$ with $TM\oplus N_i M\cong\underline{\mathbb{R}^{n+k}}$ and therefore:
$$
w(N_i M)
=\overline{w}(TM).
$$

([Milnor & Stasheff 74, p. 49](#MilnorStasheff74))

Since Stiefel-Whitney classes vanish in orders larger than the rank of the vector bundle, $k$ must be equal or larger than the highest degree in which this equation relates non-vanishing classes. With the right side, a lower bound can therefore be determined by the (dual) Stiefel-Whitney classes of $M$, explicitly by:
$$
k
\geq\max\{l\in\mathbb{N}|\overline{w}_l(M)\neq 0\}.
$$
Examples are easy to compute for simple [[smooth manifolds]], for which their Stiefel-Whitney classes are known, for example  [[real projective spaces]]. In fact, the real projective spaces $\mathbb{R}P^{2^n}$ has its lower bound $k\geq 2^n-1$ reach all the way up to the upper bound of the [[Whitney embedding theorem]]. ([Milnor & Stasheff 74, Thrm 4.8](#MilnorStasheff74))

## Related concepts

* [[Segre class]] (dual [[Chern class]])

## References

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))

* {#Hatcher17} [[Allen Hatcher]]: _Vector bundles and K-Theory_, book draft (2017) &lbrack;[webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf)&rbrack;

[[!redirects dual Stiefel-Whitney classes]]
[[!redirects total dual Stiefel-Whitney class]]
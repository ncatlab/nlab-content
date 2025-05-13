## Definition

A __connective differential graded $\mathrm{C}^\infty$-ring__ is a (homologically graded with nonnegative degrees) real [[commutative differential graded algebra]] $A$ equipped with a structure of a [[C^∞-ring]] on $A_0$.

A __coconnective differential graded $\mathrm{C}^\infty$-ring__ is a (cohomologically graded with nonnegative degrees) real [[commutative differential graded algebra]] $A$ equipped with a structure of a [[C^∞-ring]] on $A_0$ such that the differential $d\colon A_0\to A_1$ in degree 0 is a [[C^∞-derivation]].

In the unbounded case, [Carchedi–Roytenberg](#CR) proposed the following definition:

An __unbounded differential graded $\mathrm{C}^\infty$-ring__ is a (homologically graded with arbitrary degrees) real [[commutative differential graded algebra]] $A$ equipped with a structure of a [[C^∞-ring]] on $A_0^c=\ker(A_0\to A_{-1})$.

\begin{remark}
Every coconnective differential graded C^∞-ring in the sense defined above is also an unbounded differential graded C^∞-ring concentrated in nonpositive homological degrees, since the kernel of a [[C^∞-derivation]] is a [[C^∞-ring]].  The converse is false: an unbounded differential graded C^∞-ring concentrated in nonpositive homological degrees has a [[C^∞-ring]] structure on its 0-cocycles only, which is not enough to reconstruct a C^∞-structure on the whole degree 0 part or ensure that the degree 0 differential is a C^∞-derivation.  The stronger condition is essential for some theorems about coconnective differential graded [[C^∞-rings]], such as the one that states that [[smooth differential forms form the free C^∞-DGA on smooth functions]].
\end{remark}

\begin{remark}
In fact, having a C^∞-structure in degree 0 together an ordinary algebra structure in higher degrees
is sufficient to define a C^∞-structure for nonhomogeneous elements of mixed degrees: given a smooth function $f(x_1, \ldots, x_n)$ and some nonhomogeneous even elements $b_1, \ldots, b_n$ (i.e., formal sums of homogeneous elements of even degrees), set $b_i = c_i + d_i$, where $c_i$ has degree 0 and $d_i$ is a sum of homogeneous elements of positive cohomological degree.
Now set
$$f(b_1, \ldots, b_n) = \sum_m (\partial_m f)(c_1, \ldots, c_n) \prod_k d_k^{m_k} / m_k!,$$
where $m$ is a multi-index and $\partial_m f$ is the partial derivative of $f$, which can be evaluated on $c_1, \ldots, c_n$ using the C^∞-structure.
This formula yields a (possibly infinite) formal sum of homogeneous elements.
Nonhomogeneous elements of odd degrees can be incorporated in the picture by taking $f\in \mathrm{C}^\infty(\mathbf{R}^m)\otimes\Lambda(\mathbf{R}^n)$ (i.e., $f$ has $m$ even and $n$ odd variables) and modifying the formula accordingly.
This yields an equivalent notion of differential graded C^∞-rings.
The price to pay is having to manipulate infinite formal sums of homogeneous elements, so we choose the equivalent definition given above, even though it may seem slightly ad hoc on the first sight.
\end{remark}

## Properties

Differential graded C^∞-rings can be equipped with the [[model structure]] [[transferred model structure|transferred]] from the projective model structure on [[chain complexes]] via the forgetful functor.

Restricting to __connective__ differential graded C^∞-rings, the resulting model structure is [[Quillen equivalence|Quillen equivalent]] to the [[model category]] of simplicial [[C^∞-rings]] equipped with the model structure transferred along the forgetful functor to [[simplicial sets]] equipped with the [[Kan–Quillen model structure]].
The right adjoint functor is the [[normalized chains]] functor, which sends a simplicial [[C^∞-rings]] to its [[normalized chains]] equipped with the induced structure of a differential graded C^∞-ring.  This is analogous to the [[monoidal Dold–Kan correspondence]].

In this form, the statement was first proved in [Taroyan 2023](#Taroyan).
Similar, but not entirely equivalent results can be found in [Nuiten 2018, Remark 2.2.11](#Nuiten), which uses a homotopy coherent variant of [[C^∞-rings]] and does not explicitly identify the adjoint functors.

## References

The essential ingredients ([[Kähler C^∞-differentials]] and [[C^∞-derivations]]) appear in

* [[E. J. Dubuc]], [[A. Kock]], _On 1-form classifiers_, Communications in Algebra 12:12 (1984), 1471–1531.  [doi:10.1080/00927878408823064](https://doi.org/10.1080/00927878408823064), ([author pdf](https://tildeweb.au.dk/au76680/DK84.pdf))

The earliest known occurrence of differential graded [[C^∞-rings]] is in the paper

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _Čech cocycles for differential characteristic classes: an ∞-Lie theoretic construction_, Advances in Theoretical and Mathematical Physics 16:1 (2012), 149-250.  [arXiv](https://arxiv.org/abs/1011.4735), [doi](https://doi.org/10.4310/atmp.2012.v16.n1.a5)

where at the bottom of page 28 in arXiv version 1 one reads:

> The underlying algebra in degree 0 can be generalized to an algebra over some Lawvere theory. In particular in a proper setup of higher differential geometry, we would demand $CE(\mathfrak{g})_0$ to be equipped with the structure of a [[C^∞-ring]].

Additional references:

On unbounded differential graded rings for arbitrary [[Fermat theories]] (including [[C^∞-rings]]):

* {#CR} [[David Carchedi]], [[Dmitry Roytenberg]], _Homological Algebra for Superalgebras of Differentiable Functions_, [arXiv](https://arxiv.org/abs/1212.3745).

On the equivalence of connective differential graded C^∞-rings and simplicial C^∞-rings via the [[normalized chains]] functor:

* {#Taroyan} [[Gregory Taroyan]], _Equivalent models of derived stacks_, [arXiv](https://arxiv.org/abs/2303.12699).

For a similar statement, see also

* {#Nuiten} [[Joost Nuiten]], _Lie algebroids in derived differential topology_, PhD dissertation, 2018, [doi](https://doi.org/1874/364151).
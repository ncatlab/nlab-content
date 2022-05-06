
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

If $1\leq p \lt \infty$ and $\Omega$ is a [[domain]] (in a $n$-dimensional real space with easy generalization to [[manifolds]]), one first considers the [[Lebesgue spaces]] $L_p = L_p(\Omega)$ ([wikipedia](http://en.wikipedia.org/wiki/Lp_space)) of (equivalence classes of) [[measurable function|measurable]] (complex- or real-valued) functions $f$ whose (absolute values of) $p$-th powers are [[Lebesgue integral|Lebesgue integrable]]; i.e. whose norm 

$$\| f\|_{L_p} = \left(\int_\Omega |f|^p d\mu\right)^{1/p}$$

is finite. For $p = \infty$, one looks at the [[essential supremum]] norm $\|f\|_{L_\infty}$ instead.

For $1\leq p \leq \infty$, and $k\geq 1$ the **Sobolev space** $W^k_p = W^k_p(\Omega)$ or $W^{k,p}(\Omega)$ is the [[Banach space]] of measurable functions $f$ on $\Omega$ such that its generalized [[partial derivative]]s $\partial_1^{i_1}\ldots\partial_n^{i_n} f$ (e.g. in the sense of [[generalized function]]s) for all multiindices $i = (i_1,\ldots, i_n)\in\mathbb{Z}^n_{\geq 0}$ with $i_1+\ldots +i_n\leq k$ are in $L_p(\Omega)$. The most important case is the case of the Sobolev spaces $H^k(\Omega) := W^k_2(\Omega)$. Sobolev spaces are particularly important in the theory of partial differential equations. 

## References

* L. C. Evans, _Partial Differential Equations_, Amer. Math. Soc. 1998.

* R.A. Adams, _Sobolev spaces_, Acad. Press 1975.

* wikipedia: [Sobolev space](http://en.wikipedia.org/wiki/Sobolev_space).

* Springer Encyclopaedia of Mathematics: [Sobolev space](http://eom.springer.de/S/s085980.htm)

* G. Wilkin, _Sobolev spaces on Euclidean space_, Liber Mathematicae 2011,  [link](http://math.colorado.edu/libermath/repositorium/article.php?doc=4)

category: analysis
[[!redirects Sobolev spaces]]
[[!redirects Higher Kac-Moody algebras]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The idea underpinning the definition of higher Kac-Moody algebras in [FHK 19](#FHK19) is that the natural framework to construct higher-dimensional generalizations of [[Kac-Moody algebras]] is [[derived algebraic geometry]].

## Details

### Faonte-Hennion-Kapranov higher Kac-Moody algebras

Let $X$ be an $n$-dimensional [[variety]] over $\mathbb{C}$ and $\mathfrak{g}$ a [[Lie algebra]]. We can define the __higher current algebra__ by the [[dg-Lie algebra]]
$$ \mathfrak{g}_n \;=\; \mathfrak{g}\otimes\mathbb{R}\Gamma(\mathbb{D}_n^\circ,\mathcal{O}_X), $$
where $\mathbb{R}\Gamma(\mathbb{D}_n^\circ,\mathcal{O}_X)$ is the [[commutative dg-algebra]] of derived [[global sections]] of the [[structure sheaf]] $\mathcal{O}_X$ on the punctured [[formal disk]] $\mathbb{D}_n^\circ = \mathrm{Spec}(\mathbb{C}[[z_1,\dots,z_n]])-\{0\}$.

A __higher Kac-Moody algebra__ $\tilde{\mathfrak{g}}_{n,P}$ is the [[central extension]] of the higher current algebra $\mathfrak{g}_n$ by an invariant polynomial $P$ on $\mathfrak{g}_n$ of degree $(n+1)$.

## Examples

### Ordinary Kac-Moody algebras

For $n=1$, one recovers $\mathfrak{g}_1 = \mathfrak{g}((z))$ and its [[central extension]] $\tilde{\mathfrak{g}}_{1,P}$ is an ordinary [[Kac-Moody algebra]].

### Affine space $\mathbb{A}^n_{\mathbb{C}}$

Consider the [[affine space]] $X=\mathbb{A}^n_{\mathbb{C}} = \mathrm{Spec}(\mathbb{C}[z_1,\dots,z_n])$. The cohomology of the complex of derived [[global sections]] $\mathbb{R}\Gamma(\mathbb{D}_n^\circ,\mathcal{O}_X)$ will be the following:

$$ \mathrm{H}^i(\mathbb{D}_n^\circ,\mathcal{O}_X) \;=\; \begin{cases}\mathbb{C}[[z_1,\dots,z_n]], & i=0\\z_1^{-1}\cdots z_n^{-1}\mathbb{C}[z_1^{-1},\dots,z_n^{-1}], & i=n-1\\ 0, & \text{otherwise}\end{cases} $$

## Related concepts

* [[Kac-Moody algebra]]

* [[derived algebraic geometry]]


## References

Higher Kac-Moody algebras were proposed in

* {#FHK19} G. [[Faonte]], B. [[Hennion]] and M. [[Kapranov]], _Higher Kac-Moody algebras and moduli spaces of $G$-bundles_, Advances in Mathematics, Volume 346, 13 April 2019, pages 389-466, [math.AG/1701.01368](https://arxiv.org/abs/1701.01368v3).

* M. [[Kapranov]], _Infinite-dimensional (dg) Lie algebras and factorization algebras in algebraic geometry_, Japanese Journal of Mathematics volume 16, pages 49–80 (2021) [https://doi.org/10.1007/s11537-020-1921-4](https://doi.org/10.1007/s11537-020-1921-4).

Higher Kac-Moody algebras were casted in the language of [[factorization algebras]] in

* O. Gwilliam and B.R. Williams, _Higher Kac-Moody algebras and symmetries of holomorphic field theories_, Adv.Theor.Math.Phys. 25 (2021) 1, pages 129-239 [math.QA/1810.06534](https://arxiv.org/abs/1810.06534v2).


[[!redirects higher Kac-Moody algebra]]
[[!redirects higher Kac-Moody algebras]]
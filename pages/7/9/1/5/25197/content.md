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

* In dimension $1$, we have that $\mathcal{O}(\mathbb{A}^1-\{0\})\otimes\mathfrak{g} = \mathfrak{g}[z,z^{-1}]$ and, thus, we can consider its non-trivial [[central extensions]] by $2$-[[cocycles]]. These are the essential ingredients of an (ordinary) [[Kac-Moody algebra]].

* In higher dimension, [[analytic geometry#hartogs_theorem|Hartogs' extension theorem]] tells us that $\mathcal{O}(\mathbb{A}^n-\{0\})\otimes\mathfrak{g} \cong \mathcal{O}(\mathbb{A}^n)\otimes\mathfrak{g}$, which means that we do not have any interesting central extension. On the other hand, the punctured affine spaces $\mathbb{A}^n-\{0\}$ have non-trivial higher [[cohomology]].

The idea underpinning the definition of higher Kac-Moody algebras in [FHK 19](#FHK19) is that the natural framework to solve this issue and construct a higher-dimensional generalization of [[Kac-Moody algebras]] is [[derived algebraic geometry]]. This is achieved by replacing the algebra $\mathcal{O}(\mathbb{A}^n-\{0\})$ with the dg-algebra $\mathbb{R}\Gamma(\mathbb{A}^{n}-\{0\},\mathcal{O})$ of derived sections, which allows interesting [[central extensions]].

This principle can be applied not only to punctured [[affine spaces]] $\mathbb{A}^{n}-\{0\}$, but also to punctured [[formal disks]] $\mathbb{D}_n^\circ$.

## Details

### Faonte-Hennion-Kapranov higher Kac-Moody algebras

Let $X$ be an $n$-dimensional [[variety]] over $\mathbb{C}$ and $\mathfrak{g}$ a [[Lie algebra]]. We can define the __higher current algebra__ by the [[dg-Lie algebra]]
$$ \mathfrak{g}_n \;=\; \mathfrak{g}\otimes\mathbb{R}\Gamma(\mathbb{D}_n^\circ,\mathcal{O}_X), $$
where $\mathbb{R}\Gamma(\mathbb{D}_n^\circ,\mathcal{O}_X)$ is the [[commutative dg-algebra]] of derived [[global sections]] of the [[structure sheaf]] $\mathcal{O}_X$ on the punctured [[formal disk]] $\mathbb{D}_n^\circ = \mathrm{Spec}(\mathbb{C}[[z_1,\dots,z_n]])-\{0\}$.

A __higher Kac-Moody algebra__ $\widehat{\mathfrak{g}}_{n,\Theta}$ is the [[central extension]] of the higher current algebra $\mathfrak{g}_n$ by an invariant polynomial $\Theta$ on $\mathfrak{g}_n$ of degree $(n+1)$.

### Gwilliam-Williams higher Kac-Moody factorisation algebras

Let $X$ be a [[complex manifold]] of dimension $n$ equipped with a holomorphic [[principal bundle]] $P\rightarrow X$ with [[structure group]] $G$. 

Let $\mathfrak{ad}(P) \coloneqq P\times_G\mathfrak{g}$ be the [[adjoint bundle]] associated to $P$.
Now, let $\mathscr{Ad}(P)$ be the [[sheaf of L-∞ algebras#LocalLieAlgebra|local Lie algebra]] whose sections are $\Omega_c^{0,\ast}(U,\mathfrak{ad}(P))$ on any open set $U\subset X$ and whose differential is the $(0,1)$-connection $\bar{\partial}_P$. 

Let $\Theta$ be a degree $1$ [[cocycle]] in the [[sheaf of L-∞ algebras#LocalLieAlgebra|local Chevalley-Eilenberg cochains]] $\mathrm{CE}_{\mathrm{loc}}(\mathscr{Ad}(P))$, which defines a $1$-shifted [[central extension]] $\widehat{\mathscr{Ad}(P)}_\Theta$.

The __higher Kac-Moody factorization algebra__ on $X$ of type $\Theta$ is defined in [GW 21](#GW21) as the twisted [[universal enveloping algebra|enveloping]] [[factorization algebra]] $\mathbb{U}_\Theta(\mathscr{Ad}(P))$ whose sections are

$$ \mathbb{U}_\Theta\left(\mathscr{Ad}(P)\right)(U) \;=\; \Big(\mathrm{Sym}\left(\Omega_c^{0,\ast}(U,\mathfrak{ad}(P))[1]\right), \; \bar{\partial} + \mathrm{d}_\mathrm{CE} + \Theta \Big) $$

on any open set $U\subset X$.

### Relation between the two

Let $r : \mathbb{A}^{n}_{\mathbb{C}} - \{0\} \rightarrow (0,+\infty)$ be the radial projection map sending $(z_1,\dots,z_n)\mapsto \sqrt{|z_1|^2+\dots+|z_n|^2}$.

In [GW 21](#GW21) the following map of [[factorization algebras]] on the positive reals is constructed:

$$ \mathbb{U}(\hat{\pi}_{\mathfrak{g},n,\Theta}) \, : \; \mathbb{U}(\Omega^{0,\ast}_c\otimes\hat{\mathfrak{g}}_{n,\Theta}) \; \longrightarrow \; r_\ast\mathbb{U}_\Theta(\mathscr{Ad}(P)), $$

where on the left-hand side we have the enveloping factorization algebra which encodes the [[universal enveloping algebra|enveloping $A_\infty$-algebra]] of the [FHK 19](#FHK19) higher Kac-Moody algebra $\hat{\mathfrak{g}}_{n,\Theta}$.

This map establishes a relation between [[derived algebraic geometry]] and [[quantum field theory]], formulated the language of [[factorization algebras]]. In particular, the _higher Kac-Moody algebra_ $\hat{\mathfrak{g}}_{n,\Theta}$ "controls" its corresponding _higher Kac-Moody factorization algebra_ just like an affine [[Kac-Moody algebra]] "controls" its corresponding [[vertex algebra]].

## Examples

### Ordinary Kac-Moody algebras

For $n=1$ and $X=\mathbb{A}^1_{\mathbb{C}}$, one recovers the formal current algebra $\mathfrak{g}_1 = \mathfrak{g}((z))$, whose [[central extensions]] $\tilde{\mathfrak{g}}_{1,\Theta}$ are ordinary [[Kac-Moody algebras]].

### Affine space $\mathbb{A}^n_{\mathbb{C}}$

Consider the [[affine space]] $X=\mathbb{A}^n_{\mathbb{C}} = \mathrm{Spec}(\mathbb{C}[z_1,\dots,z_n])$. The cohomology of the complex of derived [[global sections]] $\mathbb{R}\Gamma(\mathbb{D}_n^\circ,\mathcal{O}_X)$ will be the following:

$$ \mathrm{H}^i(\mathbb{D}_n^\circ,\mathcal{O}_X) \;=\; \begin{cases}\mathbb{C}[[z_1,\dots,z_n]], & i=0\\z_1^{-1}\cdots z_n^{-1}\mathbb{C}[z_1^{-1},\dots,z_n^{-1}], & i=n-1\\ 0, & \text{otherwise}\end{cases} $$

## Related concepts

* [[Kac-Moody algebras]]

* [[derived algebraic geometry]]

* [[factorization algebras]]


## References

Higher Kac-Moody algebras were proposed in

* {#FHK19} G. [[Faonte]], B. [[Hennion]] and M. [[Kapranov]], _Higher Kac-Moody algebras and moduli spaces of $G$-bundles_, Advances in Mathematics, Volume 346, 13 April 2019, pages 389-466, [math.AG/1701.01368](https://arxiv.org/abs/1701.01368v3).

* M. [[Kapranov]], _Infinite-dimensional (dg) Lie algebras and factorization algebras in algebraic geometry_, Japanese Journal of Mathematics volume 16, pages 49–80 (2021) [https://doi.org/10.1007/s11537-020-1921-4](https://doi.org/10.1007/s11537-020-1921-4).

Higher Kac-Moody algebras casted in the language of [[factorization algebras]]:

* {#GW21} [[Owen Gwilliam]], B. R. Williams, _Higher Kac-Moody algebras and symmetries of holomorphic field theories_, Adv. Theor. Math. Phys. **25** 1 (2021) 129-239 &lbrack;[math.QA/1810.06534](https://arxiv.org/abs/1810.06534v2)&rbrack;

A variant of this construction on the product of a [[worldsheet]] and a [[spectral curve|spectral plane]] (i.e. another copy of
the complex plane $\mathbb{C}$ with marked points which defines any rational [[Gaudin integrable model|Gaudin model]]):

* [[Luigi Alfonsi]], [[Charles A. S. Young]], *Higher current algebras, homotopy Manin triples, and a rectilinear adelic complex*, Journal of Geometry and Physics **191** (2023) 104903 &lbrack;[doi:10.1016/j.geomphys.2023.104903](https://doi.org/10.1016/j.geomphys.2023.104903), [math.QA/2208.06009](https://arxiv.org/abs/2208.06009)&rbrack;

Review:

* [[Luigi Alfonsi]], §7 in: *Higher geometry in physics*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2312.07308](https://arxiv.org/abs/2312.07308)&rbrack;


[[!redirects higher Kac-Moody algebra]]
[[!redirects higher Kac-Moody algebras]]
[[!redirects higher current algebra]]
[[!redirects higher current algebras]]
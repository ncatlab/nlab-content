
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _sheaf of $L_\infty$-algebras_ is a suitable [[sheaf]]/[[stack]]/[[∞-stack]] of [[L-∞ algebras]]/[[dg-Lie algebras]]. 

These structures appear in the [[deformation theory]] of the given base [[space]]/[[site]]: where a single [[L-∞ algebra]] is equivalently a [[formal moduli problem]] (hence "over the point), so a sheaf of these over some base $X$ may be thought of as an $X$-parameterized [[formal moduli problem]] (eg. [Hinich 03](#Hinich03)).

## Local $L_\infty$-algebras {#LocalLieAlgebra}

\begin{definition}
\label{LocalLieAlgebra}

A __local $L_\infty$-algebra__ on a [[smooth manifold]] $X$ is defined by the following data:

1. A graded vector bundle $L\rightarrow X$,

1. A square $0$ [[differential operator]] $\mathrm{d}:\Gamma(X,L)\rightarrow\Gamma(X,L)$ of cohomological degree $1$,

1. A collection $\{ l_n \}_{n \geq 2}$ of poly-differential operators
$$l_n \,:\; \Gamma(X,L)^{\otimes n} \rightarrow \Gamma(X,L),$$
which are alternating, of cohomological degree $2-n$ and such that they endow $\Gamma(X,L)$ with an $L_\infty$ structure.

\end{definition}

One usually denotes by $\mathcal{L}$ the sheaf of sections of the bundle $L$.

\begin{definition}

The __Chevalley-Eilenberg cochain complex__ $\mathrm{CE}(\mathcal{L})$ of the local $L_\infty$-algebra $\mathcal{L}$ is defined by

$$ \mathrm{CE}\left(\mathcal{L}(U)\right) \;=\; \prod_{n\geq 0} \mathrm{Hom}\left( (\mathcal{L}(U)[1])^{\hat{\otimes} n}, \,\mathbb{R}  \right)_{S_n} $$

equipped with the usual [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg]] differential; where $\hat{\otimes}$ denotes the completed projective tensor product, $\mathrm{Hom}$ denotes the dg-vector space of continuous linear maps and the subscript $S_n$ denotes the [[coinvariants]] respect to the action of the [[symmetric group]] $S_n$.

\end{definition}

\begin{definition}

The __reduced Chevalley-Eilenberg cochain complex__ $\mathrm{CE}_{\mathrm{red}}(\mathcal{L})$ of the local $L_\infty$-algebra $\mathcal{L}$ is defined by the [[kernel]]

$$ \mathrm{CE}_{\mathrm{red}}(\mathcal{L}) \subset \mathrm{CE}(\mathcal{L}) $$

of the natural augmentation map $\mathrm{CE}\left(\mathcal{L}(U)\right) \rightarrow \mathbb{R}$.

\end{definition}

Both $\mathrm{CE}(\mathcal{L})$ and $\mathrm{CE}_{\mathrm{red}}(\mathcal{L})$ are differentiable pro-cochain complexes.


\begin{definition}

The __local Chevalley-Eilenberg cochain complex__ $\mathrm{CE}_{\mathrm{loc}}(\mathcal{L})$ of the local $L_\infty$-algebra $\mathcal{L}$ is defined by

$$ \mathrm{CE}_{\mathrm{loc}}(\mathcal{L}) \;\coloneqq\;  \mathscr{Dens}_X \otimes_{D_X} \mathrm{CE}_{\mathrm{red}}(\mathscr{Jet}(L)) $$

where $\mathscr{Jet}(L)$ is the local $L_\infty$-algebra, in the category of $D_X$-modules, of sections of the [[jet bundle]] of $L$ and $mathscr{Dens}_X$ is the right $D_X$-module of densities on $X$.

\end{definition}

The cochain complex $\mathrm{CE}_{\mathrm{loc}}(\mathcal{L})$ can be thought as the sheaf of [[Lagrangian density|Lagrangian densities]] on the graded vector bundle $L$.


## Related concepts

* [[descent for L-∞ algebras]]

* [[factorization algebras]]

* [[formal moduli problems]]

* [[L-∞ algebroid]]

* [[homotopy theory of L-∞ algebras]]

* [[sheaf of spectra]]

## References

Discussion in the context of [[deformation theory]]/parameterized [[formal moduli problems]] is in

* [[Vladimir Hinich]], _Deformations of sheaves of algebras_ ([arXiv:math/0310116](http://arxiv.org/abs/math/0310116))
 {#Hinich03}

[[quasi-coherent sheaf|Quasi-coherent sheaves]] of dg-Lie algebras appear in

* [[Amnon Yekutieli]], appendix A of _Twisted Deformation Quantization of Algebraic Varieties_ ([arXiv:0905.0488](http://arxiv.org/abs/0905.0488))


* I. Ciocan-Fontanine, [[Mikhail Kapranov]], _Derived Quot schemes_ ([arXiv:math/9905174](http://arxiv.org/abs/math/9905174))

Discussion in [[physics]], of sheaves of $L_\infty$-algebras of [[physical fields]] in [[prequantum field theory]] includes

* [[Anton Zeitlin]], _Conformal Field Theory and Algebraic Structure of Gauge Theory_ ([arXiv:0812.1840](http://arxiv.org/abs/0812.1840))


Local $L_\infty$-algebras are defined and discussed by

* [[Kevin Costello]], [[Owen Gwilliam]], _[[Factorization algebras in perturbative quantum field theory]]_

[[!redirects sheaf L-∞ algebras]]
[[!redirects sheaves L-∞ algebras]]

[[!redirects sheaves of L-∞ algebras]]


[[!redirects sheaf of L-infinity algebras]]
[[!redirects sheaves of L-infinity algebras]]

[[!redirects sheaf of dg-Lie algebras]]
[[!redirects sheaves of dg-Lie algebras]]

[[!redirects local L-∞ algebras]]
[[!redirects local L-∞ algebra]]
[[!redirects local L-infinity algebras]]
[[!redirects local L-infinity algebra]]
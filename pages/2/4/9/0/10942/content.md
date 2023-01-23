
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

## Related concepts

* [[descent for L-∞ algebras]]

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

[[!redirects sheaf L-∞ algebras]]
[[!redirects sheaves L-∞ algebras]]

[[!redirects sheaves of L-∞ algebras]]


[[!redirects sheaf of L-infinity algebras]]
[[!redirects sheaves of L-infinity algebras]]

[[!redirects sheaf of dg-Lie algebras]]
[[!redirects sheaves of dg-Lie algebras]]
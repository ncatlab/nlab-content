+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For a scalar function, a curve whose derivative is opposite to its [[gradient]] is called a *gradient flow*. It always points down the way of steepest descent and hence is monotonically descreasing with respect to the scalar function. It is then possible to study its convergence to [[critical points]], especially those that are [[local minima]].

If the scalar function is the *Yang-Mills-Higgs action functional*, then the gradient flow is called *Yang-Mills-Higgs flow*. It is described by the [[Yang-Mills-Higgs equations]] and can be used to find [[Yang-Mills-Higgs pairs]], the critical points, as well as study [[stable Yang-Mills-Higgs pairs]], the local minima.

The [[Yang-Mills flow]] is named after [[Chen Ning Yang]] and [[Robert Mills]], who introduced [[Yang-Mills theory]] in 1954, and [[Peter Higgs]], who proposed the [[Higgs field]] in 1964.

## Basics

Let $G$ be a [[compact]] [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and $E\twoheadrightarrow B$ be a principal $G$-bundle with a [[compact]] [[orientable]] [[Riemannian manifold]] $B$ having a metric $g$ and a [[volume form]] $vol_g$. Let $Ad(E)\coloneqq E\times_G\mathfrak{g}$ be its [[adjoint bundle]]. One has $\Omega_{Ad}^k(E,\mathfrak{g})\cong\Omega^k(B,Ad(E))$, which are either under the [[adjoint representation]] $Ad$ invariant Lie-algebra valued or vector bundle valued differential forms. Since the [[Hodge star operator]] $\star$is defined on the Base manifold $B$ as it requires the metric $g$ and the volume form $vol_g$, the second space is usually used.

All spaces $\Omega^k(B,Ad(E))$ are [[vector spaces]], which from $B$ together with the choice of an $Ad$-invariant pairing on $\mathfrak{g}$ (which for [[semisimple]] $\mathfrak{g}$ must be proportional to its [[Killing form]]) inherits a local pairing $\langle-,-\rangle\colon\Omega^k(B,Ad(E))\times\Omega^k(B,Ad(E))\rightarrow\C^\infty(B)$. It defined the [[Hodge star operator]] by $\langle\omega,\eta\rangle vol_g=\omega\wedge\star\eta$ for all $\omega,\eta\in\Omega^k(B,Ad(E))$. Through postcomposition with [[integration]], there is fuethermore a [[scalar product]] $\langle-,-\rangle\colon\Omega^k(B,Ad(E))\times\Omega^k(B,Ad(E))\rightarrow\mathbb{R}$. It's induced [[norm]] is exactly the $L^2$ [[norm]].

## Definition

The _Yang-Mills-Higgs action functional_ is given by:
$$
YMH\colon
\Omega^1(B,Ad(E))\times\Gamma^\infty(B,Ad(E))\rightarrow\mathbb{R},
YMH(A,\Phi)
\coloneqq\int_B\|F_A\|^2+\|\mathrm{d}_A\Phi\|^2\mathrm{d}vol_g
\geq 0.
$$
Its first term is also called [[Yang-Mills action]].

Hence the gradient of the Yang-Mills-Higgs action functional gives exactly the [[Yang-Mills-Higgs equations]]:
$$
grad(YMH)(A,\Phi)_1
=\delta_AF_A
+[\Phi,\mathrm{d}_A\Phi],
$$
$$
grad(YMH)(A,\Phi)_2
=\delta_A\mathrm{d}_A\Phi.
$$
For an [[open interval]] $I\subseteq\mathbb{R}$, two $C^1$ maps $\alpha\colon I\rightarrow\Omega^1(B,Ad(E))$ and $\varphi\colon I\rightarrow\Gamma^\infty(B,Ad(E))$ (hence [[continuously differentiable]]) fulfilling:
$$
\alpha'(t)
=-grad(YMH)(\alpha(t),\varphi(t))_1
=-\delta_{\alpha(t)}F_{\alpha(t)}
-[\varphi(t),\mathrm{d}_{\alpha(t)}\varphi(t)]
$$
$$
\varphi'(t)
=-grad(YMH)(\alpha(t),\varphi(t))_2
=-\delta_{\alpha(t)}\mathrm{d}_{\alpha(t)}\varphi(t)
$$
are a _Yang-Mills-Higgs flow_.

## Related entries

* [[Yang-Mills flow]]
* [[Seiberg-Witten flow]]

## References

See also:

* Wikipedia, _[Yang-Mills-Higgs flow](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills%E2%80%93Higgs_flow)_
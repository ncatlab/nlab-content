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

For a [[scalar]]-valued [[function]], a [[curve]] whose [[derivative]] is the negative of its [[gradient]] is called a *[[gradient flow]]*. It always points down the direction of [[steepest descent]] and hence is [[monotone function|monotonically descreasing]] with respect to the scalar function. It is then possible to study its [[convergence]] to [[critical points]], especially those that are [[local minima]].

If the scalar function is the *[[Yang-Mills-Higgs equations|Yang-Mills-Higgs]] [[action functional]]*, then this [[gradient flow]] is called *Yang-Mills-Higgs flow*. It is described by the [[Yang-Mills-Higgs equations]] and can be used to find [[Yang-Mills-Higgs pairs]], the [[critical points]], as well as study [[stable Yang-Mills-Higgs pairs]], the [[local minima]].

The [[Yang-Mills flow]] is named after [[Chen Ning Yang]] and [[Robert Mills]], who introduced [[Yang-Mills theory]] in 1954, and [[Peter Higgs]], who proposed the [[Higgs field]] in 1964.

## Basics

Let $G$ be a [[compact]] [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and $E\twoheadrightarrow B$ be a principal $G$-bundle with a [[compact]] [[orientable]] [[Riemannian manifold]] $B$ having a metric $g$ and a [[volume form]] $vol_g$. Let $Ad(E)\coloneqq E\times_G\mathfrak{g}$ be its [[adjoint bundle]]. One has $\Omega_{Ad}^k(E,\mathfrak{g})\cong\Omega^k(B,Ad(E))$, which are either under the [[adjoint representation]] $Ad$ invariant Lie-algebra valued or vector bundle valued differential forms. Since the [[Hodge star operator]] $\star$is defined on the Base manifold $B$ as it requires the metric $g$ and the volume form $vol_g$, the second space is usually used.

All spaces $\Omega^k(B,Ad(E))$ are [[vector spaces]], which from $B$ together with the choice of an $Ad$-invariant pairing on $\mathfrak{g}$ (which for [[semisimple]] $\mathfrak{g}$ must be proportional to its [[Killing form]]) inherits a local pairing $\langle-,-\rangle\colon\Omega^k(B,Ad(E))\times\Omega^k(B,Ad(E))\rightarrow\C^\infty(B)$. It defined the [[Hodge star operator]] by $\langle\omega,\eta\rangle vol_g=\omega\wedge\star\eta$ for all $\omega,\eta\in\Omega^k(B,Ad(E))$. Through postcomposition with [[integration]], there is furthermore a [[scalar product]] $\langle-,-\rangle\colon\Omega^k(B,Ad(E))\times\Omega^k(B,Ad(E))\rightarrow\mathbb{R}_0^+$. Its induced [[norm]] is exactly the $L^2$ [[norm]].

## Definition

The _Yang-Mills-Higgs action functional_ is given by:
$$
YMH\colon
\mathcal{A}
\coloneqq\Omega^1(B,Ad(E))\times\Gamma^\infty(B,Ad(E))\rightarrow\mathbb{R}_0^+,
YMH(A,\Phi)
\coloneqq\int_B\|F_A\|^2+\|\mathrm{d}_A\Phi\|^2\mathrm{d}vol_g
\geq 0.
$$
Its first term is also called [[Yang-Mills action]]. $\mathcal{A}$ is called _configuration space_.

Hence the gradient of the Yang-Mills-Higgs action functional gives exactly the [[Yang-Mills-Higgs equations]]:
$$
grad(YMH)(A,\Phi)_1
=\delta_A F_A
+[\Phi,\mathrm{d}_A\Phi],
$$
$$
grad(YMH)(A,\Phi)_2
=\delta_A\mathrm{d}_A\Phi.
$$
For an [[open interval]] $I\subseteq\mathbb{R}$, a $C^1$ map $(\alpha,\varphi)\colon I\rightarrow\mathcal{A}=\Omega^1(B,Ad(E))\times\Gamma^\infty(B,Ad(E))$ (hence [[continuously differentiable]]) fulfilling:
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
is a _Yang-Mills-Higgs flow_.

## Properties

\begin{corollary}
For a Yang-Mills-Higgs pair $(A,\Phi)\in\mathcal{A}$, the constant path on it is a Yang-Mills-Higgs flow.
\end{corollary}
\begin{lemma}
For a Yang-Mills-Higgs flow $(\alpha,\varphi)\colon\mathbb{R}\supseteq I\rightarrow\mathcal{A}$, the composition $YMH\circ(\alpha,\varphi)\colon\mathbb{R}\supseteq I\rightarrow\mathbb{R}_0^+$ with the Yang-Mills-Higgs [[action functional]] is [[monotone function|monotonically descreasing]] and in particular fulfills:
$$
(YMH\circ(\alpha,\varphi))'(t)
=-2\int_B\|\alpha'(t)\|^2+\|\varphi'(t)\|^2\mathrm{d}\vol_g
\leq 0.
$$
\end{lemma}
\begin{proof}
Using the flow equations yields:
$$
\frac{1}{2}\frac{\mathrm{d}}{\mathrm{d}t}\|F_{\alpha(t)}\|^2
=\left\langle\frac{\mathrm{d}}{\mathrm{d}t}F_{\alpha(t)},F_{\alpha(t)}\right\rangle
=\left\langle\mathrm{d}_{\alpha(t)}\alpha'(t),F_{\alpha(t)}\right\rangle
=\left\langle\alpha'(t),\delta_{\alpha(t)}F_{\alpha(t)}\right\rangle;
$$
$$
\frac{1}{2}\frac{\mathrm{d}}{\mathrm{d}t}\|\mathrm{d}_{\alpha(t)}\varphi(t)\|^2
=\left\langle\frac{\mathrm{d}}{\mathrm{d}t}\mathrm{d}_{\alpha(t)}\varphi(t),\mathrm{d}_{\alpha(t)}\varphi(t)\right\rangle
=\left\langle\mathrm{d}_{\alpha(t)}\varphi'(t)
+[\alpha'(t),\varphi(t)],\mathrm{d}_{\alpha(t)}\varphi(t)\right\rangle
=\langle\alpha'(t),[\varphi(t),\mathrm{d}_{\alpha(t)}\varphi(t)]\rangle
+\langle\varphi'(t),\delta_{\alpha(t)}\mathrm{d}_{\alpha(t)}\varphi(t)\rangle;
$$
$$
\frac{1}{2}\frac{\mathrm{d}}{\mathrm{d}t}\left(
\|F_{\alpha(t)}\|^2
+\|\mathrm{d}_{\alpha(t)}\varphi(t)\|^2
\right)
=\langle\alpha'(t),[\varphi(t),\delta_{\alpha(t)}F_{\alpha(t)}+\mathrm{d}_{\alpha(t)}\varphi(t)]\rangle
+\langle\varphi'(t),\delta_{\alpha(t)}\mathrm{d}_{\alpha(t)}\varphi(t)\rangle
=\|\alpha'(t)\|^2
+\|\varphi'(t)\|^2.
$$
\end{proof}
\begin{lemma}
For an infinitely long Yang-Mills-Higgs flow $(\alpha,\varphi)\colon[0,\infty)\rightarrow\mathcal{A}$, the [[limits]] $(\lim_{t\rightarrow\infty}\alpha(t),\lim_{t\rightarrow\infty}\varphi(t))\in\mathcal{A}$ exist and are a Yang-Mills-Higgs pair.
\end{lemma}
\begin{proof}
According to the previous lemma, the [[limit]] $\lim_{t\rightarrow\infty}(YMH\circ(\alpha,\varphi))(t)\in\mathbb{R}_0^+$ exists, since the function $YMH\circ(\alpha,\varphi)\colon[0,\infty)\rightarrow\mathbb{R}_0^+$ is [[monotone function|monotonically descreasing]] and bounded from below. The inequality in the previous lemma then yields $\lim_{t\rightarrow\infty}\alpha'(t)=0$ and $\lim_{t\rightarrow\infty}\varphi'(t)=0$, which implies that the limits $A=\lim_{t\rightarrow\infty}\alpha(t)$ and $\Phi=\lim_{t\rightarrow\infty}\varphi'(t)$ exist. Using the flow equations then shows, that they are a Yang-Mills-Higgs pair:
$$
\delta_A F_A+[\Phi,\mathrm{d}_A\Phi]
=\lim_{t\rightarrow\infty}\delta_{\alpha(t)}F_{\alpha(t)}+[\varphi(t),\mathrm{d}_{\alpha(t)}\varphi(t)]
=\lim_{t\rightarrow\infty}\alpha'(t)
=0;
$$
$$
\delta_A\mathrm{d}_A\Phi
=\lim_{t\rightarrow\infty}\delta_{\alpha(t)}\mathrm{d}_{\alpha(t)}\varphi(t)
=\lim_{t\rightarrow\infty}\varphi'(t)
=0.
$$
\end{proof}

## Related entries

* [[Yang-Mills flow]]
* [[Seiberg-Witten flow]]

## References

* {#Zhang20} [[Pan Zhang]], _Gradient Flows of Higher Order Yang-Mills-Higgs Functionals_ (2020), &lbrack;[arXiv:2004.00420](https://arxiv.org/abs/2004.00420)&rbrack;
* {#PanShenZhang23} Changpeng Pan, Zhenghan Shen, [[Pan Zhang]], _The Limit of the Yang-Mills-Higgs Flow for twisted Higgs pairs_ (2023), &lbrack;[arXiv:2301.02552](https://arxiv.org/abs/2301.02552)&rbrack;

See also:

* Wikipedia, _[Yang-Mills-Higgs flow](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills%E2%80%93Higgs_flow)_
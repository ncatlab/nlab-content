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

If the scalar function is the *Yang-Mills action functional*, then the gradient flow is called *Yang-Mills flow*. It is described by the [[Yang-Mills equation]] and can be used to find [[Yang-Mills connections]], the critical points, as well as study [[stable Yang-Mills connections]], the local minima.

The [[Yang-Mills flow]] is named after [[Chen Ning Yang]] and [[Robert Mills]], who introduced [[Yang-Mills theory]] in 1954. But it was first studied by [[Michael Atiyah]] and [[Raoul Bott]] in 1982. It was also studied by [[Simon Donaldson]] in the context of the [[Kobayashi-Hitchin correspondence]] (or [[Donaldson-Uhlenbeck-Yau theorem]]).

## Basics

Let $G$ be a [[compact]] [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and $E\twoheadrightarrow B$ be a [[principal bundle|principal $G$-bundle]] with a [[compact]] [[orientable]] [[Riemannian manifold]] $B$ having a [[metric]] $g$ and a [[volume form]] $vol_g$. Let $Ad(B)\coloneqq E\times_G\mathfrak{g}$ be its [[adjoint bundle]]. One has $\Omega_{Ad}^k(E,\mathfrak{g})\cong\Omega^k(B,Ad(E))$, which are either under the [[adjoint representation]] $Ad$ invariant Lie algbera valued or vector bundle valued differential forms. Since the [[Hodge star operator]] $\star$ is defined on the base manifold $B$ as it requires the metric $g$ and the volume form $vol_g$, the second spaces are usually used.

## Definition

The _Yang-Mills action functional_ is given by:
$$
YM\colon
\Omega^1(B,Ad(E))\rightarrow\mathbb{R},
YM(A)
\coloneqq\int_B\|F_A\|^2\mathrm{d}vol_g
\geq 0.
$$
Hence the gradient of the Yang-Mills action functional gives exactly the [[Yang-Mills equations]]:
$$
grad(YM)(A)
=-\delta_A F_A.
$$
For an [[open interval]] $I\subseteq\mathbb{R}$, a $C^1$ map $\alpha\colon I\rightarrow\Omega^1(B,Ad(E))$ (hence [[continuously differentiable]]) fulfilling:
$$
\alpha'(t)
=-grad(YM)(\alpha(t))
=-\delta_{\alpha(t)}F_{\alpha(t)}
$$
is a _Yang-Mills flow_.

## Related entries

* [[Yang-Mills-Higgs flow]]
* [[Seiberg-Witten flow]]

## References

* {#KelleherStreets16} Casey Lynn Kelleher, Jeffrey Streets, _Singularity formation of the Yang-Mills flow_ (2016), &lbrack;[arXiv:1602.03125](https://arxiv.org/abs/1602.03125)&rbrack;
* {#Waldron219} Alex Waldron, _Long-time existence for Yang-Mills flow_ (2019), &lbrack;[arXiv:1610.03424](https://arxiv.org/abs/1610.03424)&rbrack;
* {#Zhang20} [[Pan Zhang]], _Gradient Flows of Higher Order Yang-Mills-Higgs Functionals_ (2020), &lbrack;[arXiv:2004.00420](https://arxiv.org/abs/2004.00420)&rbrack;

See also:

* Wikipedia, _[Yang-Mills flow](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills_flow)_
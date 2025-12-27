+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The Kronheimer-Mrowka basic classes are [[cohomology classes]] of the second [[cohomology]] of a [[simply connected]] [[4-manifold]] generating its Donaldson polynomials in [[Donaldson theory]], introduced by [[Peter Kronheimer]] and [[Tomasz Mrowka]].

## Description

For a 4-manifold $M$, its Donaldson invariants are an [[integer]] $\gamma_0(M)\in\mathbb{Z}$ and maps $\gamma_d(M)\colon H_2(M,\mathbb{Z})\rightarrow\mathbb{Z}[1/2]$ (into half-integers), which combine into the Donaldson polynomial:
$$
\mathcal{D}_M\colon H_2(M,\mathbb{Z})\rightarrow\mathbb{R},
\mathcal{D}_M(x)
=\sum_{d=0}^\infty\frac{\gamma_d(M)(x)}{d!}.
$$

([Kronheimer & Mrowka 94, p. 3](#KronheimerMrowka94), [Naber 11, p. 399](#Naber11))

[[Peter Kronheimer]] and [[Tomasz Mrowka]] introduced a condition known as Kronheimer–Mrowka simple type (KM symple type), which is sufficient to obtain the separate [[Donaldson invariants]] from their common Donaldson polynomial. For a KM-simple manifold $M$ there are cohomology classes $K_1,\ldots,K_s\in H^2(M,\mathbb{Z})$, called _Kronheimer–Mrowka basic classes_ (short _KM basic classes_), as well as rational numbers $a_1,\ldots,a_s\in\mathbb{Q}$, called _Kronheimer–Mrowka coefficients_ (short _KM coefficients_), so that:
$$
\mathcal{D}_M(x)
=\exp(Q_M(x,x)/2)\sum_{r=1}^s a_r\exp(K_r(x))
$$
for all $x\in H_2(M,\mathbb{Z})$. Furthermore $w_2(M)=K_r\operatorname{mod}2\in H^2(M,\mathbb{Z}_2)$ for all KM basic classes.

([Kronheimer & Mrowka 94, Prop. 3](#KronheimerMrowka94), [Kronheimer & Mrowka 95, Thrm. 1.7](#KronheimerMrowka95), [Naber 11, Theorem A.5.1](#Naber11))

Although this reduction of the infinite sum of the Donaldson polynomial to a finite sum in early 1994 brought a significant simplification to Donaldson theory, it was overhauled just a few months later in late 1994 by the development of [[Seiberg-Witten theory]]. [[Edward Witten]], presented  in a lecture at MIT, used a purely physical argument to conjecture that Kronheimer-Mrowka basic classes are exactly the [[support]] of the [[Seiberg-Witten invariants]] $\operatorname{SW}\colon
\operatorname{Spin}^\mathrm{c}(M)\rightarrow\mathbb{Z}$(hence the first [[Chern class]] $c_1\colon
\operatorname{Spin}^\mathrm{c}(M)\rightarrow H^2(M,\mathbb{Z})$ of [[spinᶜ structures]] with a non-vanishing Seiberg-Witten invariant) and their Kronheimer-Mrowka coefficients are up to a topological factor exactly their Seiberg-Witten invariants. More concretely, it claims that a [[compact]] [[connected]] [[simply connected]] orientable smooth 4-manifold $M$ with $b_2^+(M)\geq 2$ odd is of Kronheimer–Mrowka simple type if and only if is of Seiberg–Witten simple type (meaning non-vanishing Seiberg-Witten invariants only come from zero-dimensional [[Seiberg-Witten moduli spaces]] by counting its points with a sign determined by their orientation). In this case the Donaldson polynomial is given by:
$$
\mathcal{D}_M(x)
=\exp(Q_M(x,x)/2)\sum_{\mathfrak{s}\in\operatorname{Spin}^\mathrm{c}(M), \dim\mathcal{M}_{\mathfrak{s}}^\mathrm{SW}=0}2^{2+\frac{1}{4}(7\chi(M)+11\sigma(M))}\operatorname{SW}(M,\mathfrak{s})\exp(c_1(\mathfrak{s})(x)).
$$

([Naber 11, p. 400](#Naber11))

## References

* {#KronheimerMrowka94} [[Peter Kronheimer]], [[Tomasz Mrowka]], _Recurrence relations and asymptotics for four-manifold invariants_, Bulletin of the American Mathematical Society, New Series, **30** (2): 215–221, [arXiv:math/9404232](https://arxiv.org/abs/math/9404232), [doi:10.1090/S0273-0979-1994-00492-6](https://doi.org/10.1090%2FS0273-0979-1994-00492-6), [ISSN 0002-9904](https://search.worldcat.org/de/search?q=n2:0002-9904), [MR 1246469](https://mathscinet.ams.org/mathscinet/relay-station?mr=1246469)

* {#KronheimerMrowka95} [[Peter Kronheimer]], [[Tomasz Mrowka]], _Embedded surfaces and the structure of Donaldson's polynomial invariants_, Journal of Differential Geometry, **41** (3): 573–734, [doi:10.4310/jdg/1214456482](https://doi.org/10.4310%2Fjdg%2F1214456482), [ISSN 0022-040X](https://search.worldcat.org/de/search?q=n2:0022-040X), [MR 1338483](https://mathscinet.ams.org/mathscinet/relay-station?mr=1338483)

* {#Naber11} [[Gregory L. Naber]], *Topology, Geometry and Gauge fields -- Foundations*,  Texts in Applied Mathematics **25** (2011) &lbrack;[doi:10.1007/978-1-4419-7254-5](https://doi.org/10.1007/978-1-4419-7254-5)&rbrack;

See also

* Wikipedia , _[Kronheimer–Mrowka basic class](https://en.wikipedia.org/wiki/Kronheimer%E2%80%93Mrowka_basic_class)_

[[!redirects Kronheimer-Mrowka basic classes]]
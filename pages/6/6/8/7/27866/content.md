+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Seiberg-Witten invariants_ are invariants for certain [[4-manifolds]] (with $b_2^+-b_1$ odd and $b_2^+\geq 2$ for the [[Betti numbers]]) and [[spinᶜ structures]] on them. Their definition is based on the [[moduli space]] of the [[Seiberg-Witten equations]], which is usually [[compact]] unlike the [[moduli]] space of the [[Yang-Mills equations]], which first requires [[compactification]]. Seiberg-Witten invariants have therefore turned out to often be both easier in calculations and yielding stronger results than [[Donaldson invariants]].

## Basics

Let $M$ be a [[compact]] [[orientable]] [[Riemannian manifold|Riemannian]] [[4-manifold]] with a [[Riemannian metric]] $g$ and [[spinᶜ structure]] $\mathfrak{s}$. Both always exist. In particular the latter is a lift of the [[classifying map]] $\tau\colon M\rightarrow BSO(4)$ of the [[tangent bundle]] $TM\cong\tau^*\gamma_\mathbb{R}^4$ to a map $\mathfrak{s}\colon M\rightarrow BSpin^\mathrm{c}(4)$. Because of the [[exceptional isomorphism]]:
$$
Spin^\mathrm{c}(4)
\cong U(2)\times_{U(1)}U(2)
=\{A^\pm\in U(2)|det(A^-)=det(A^+)\}
$$
the [[spinᶜ structure]] $\mathfrak{s}$ consists of two complex plane bundles $W^\pm\twoheadrightarrow M$, called _associated spinor bundles_, with same [[determinant line bundle]] $L=det(W^\pm)$. Since it preserves the first [[Chern class]] one has $c_1(L)=c_1(W^\pm)\in H^2(M,\mathbb{Z})$. Furthermore let $W=W^-\oplus W^+$ be the [[Whitney sum]] of the spinor bundles.

## Seiberg-Witten invariants

Let $\mathcal{M}_{M,\mathfrak{s},g,\eta}^\mathrm{SW}$ (or just $\mathcal{M}$ in the following) be the [[moduli space]] of the [[disturbed Seiberg-Witten equations]], hence the space of its solution up to gauge, depending on the manifold $M$, the [[spinᶜ structure]] $\mathfrak{s}$, the metric $g$ and the disturbation $\eta$. Using the [[Atiyah-Singer index theorem]], its [[dimension]] is given by the [[Euler characteristic]] and the [[signature]] of the underlying manifold as:
$$
\dim\mathcal{M}
=\frac{1}{4}\left(
c_1(L)^2
-2\chi(M)
-3\sigma(M)
\right)
$$
If the right expression is positive. Otherwise the [[moduli space]] is empty.

The group $\mathcal{G}=C^\infty(M,U(1))$ and its subgroup $\mathcal{G}_0=\{u\in\mathcal{G}|u(x_0)=1\}$ with a basepoint $x_0\in M$ act on the [[moduli space]]. The canonical projection $\mathcal{M}/\mathcal{G}_0\rightarrow\mathcal{M}/\mathcal{G}$ is a principal U(1)-bundles with [[Euler class]] $e\in H^2(M,\mathbb{Z})$.

If $b_2^+(M)-b_1(M)$ is odd, then $dim\mathcal{M}=2d$ is even and the Seiberg-Witten invariant can be defined as:
$$
SW(M,\mathfrak{s},g,\eta)
=\int_{\mathcal{M}}e^d
\in\mathbb{Z}.
$$
If $b_2^+(M)\geq 2$, then $SW(M,\mathfrak{s}):=SW(M,\mathfrak{s},g,\eta)$ is independent of the metric $g$ and the disturbation $\eta$. With the space $Spin^\mathrm{c}(M)\cong H^2(M,\mathbb{Z})$ of [[spinᶜ structures]], for which the isomorphism is given by the first Chern class, one can express the Seiberg-Witten invariant as a map:
$$
SW\colon
Spin^\mathrm{c}(M)\cong H^2(M,\mathbb{Z})\rightarrow\mathbb{Z}.
$$
A similar map with the choice of a [[fundamental class]] $[M]\in H_4(M,\mathbb{Z})\cong\mathbb{Z}$, which is a generator, is the [[intersection form]] $H^2(M,\mathbb{Z})\rightarrow\mathbb{Z},c\mapsto\langle c^2,[M]\rangle$, which is essential for the classification of [[4-manifolds]].

A [[spinᶜ structure]] $\mathfrak{s}\in Spin^\mathrm{c}(M)$, or alternatively its corresponding cohomology class $c_1(L)\in H^2(M,\mathbb{Z})$, with $SW(M,\mathfrak{s})\neq 0$ is called _basic class_. Hence the basic classes are the [[support]] of the Seiberg-Witten invariant and there always exist only finitely many. Every basic class fulfills:
$$
c^2
\geq 2\chi(M)
+3\sigma(M).
$$

[[!redirects Seiberg-Witten invariants]]
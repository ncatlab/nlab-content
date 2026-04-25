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

Let $\mathcal{M}_{M,\mathfrak{s},g,\eta}^\mathrm{SW}$ (or just $\mathcal{M}$ in the following) be the [[moduli space]] of the [[perturbed Seiberg-Witten equations]], hence the space of its solution up to gauge, depending on the manifold $M$, the [[spinᶜ structure]] $\mathfrak{s}$, the metric $g$ and the disturbation $\eta$. Using the [[Atiyah-Singer index theorem]], its [[dimension]] is given by the [[Euler characteristic]] and the [[signature]] of the underlying manifold as:
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
\coloneqq\int_{\mathcal{M}}e^d
\in\mathbb{Z}.
$$
If $b_2^+(M)\geq 2$, then $SW(M,\mathfrak{s})\coloneqq SW(M,\mathfrak{s},g,\eta)$ is independent of the metric $g$ and the disturbation $\eta$. With the space $Spin^\mathrm{c}(M)\cong H^2(M,\mathbb{Z})$ of [[spinᶜ structures]], for which the isomorphism is given by the first Chern class, one can express the Seiberg-Witten invariant as a map:
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

## Properties

\begin{proposition}
On a smooth [[4-manifold]] $M$ with $b_2^+(M)=1$, which admits a [[Riemannian metric]] of positive [[scalar curvature]], all [[Seiberg-Witten invariants]] vanish.
\end{proposition}

([Nicolaescu 00, Crl. 2.3.8](#Nicolaescu00))

\begin{proposition}
Let $M$ be a [[closed manifold|closed]] [[oriented]] [[Riemannian manifold|Riemannian]] [[4-manifold]] with $b_2^+(M)\geq 2$.

* If $SW_M(\mathfrak{s})=0$ for all [[spinᶜ structures]] $\mathfrak{s}$, then $M$ doesn't admit [[symplectic structures]].

* If $|SW_M(\mathfrak{s})|\neq 1$ for all [[spinᶜ structures]] $\mathfrak{s}$, then $M$ doesn't admit [[symplectic structures]].

\end{proposition}

([Nicolaescu 00, Crl. 3.3.33](#Nicolaescu00))

A combination of both previous results shows that if $M$ has a [[Riemannian metric]] of positive [[scalar curvature]], it doesn't admit [[symplectic structures]].

\begin{proposition}
For two [[compact]] [[oriented]] [[Riemannian manifold|Riemannian]] [[4-manifolds]] $M$ and $N$ with $b_2^+(M),b_2^+(N)\geq 1$, one has:
$$
SW_{M#N}(\mathfrak{s})
=0
$$
for all [[spinᶜ structures]] $\mathfrak{s}$.
\end{proposition}

([Nicolaescu 00, Thrm. 4.6.1](#Nicolaescu00))

A combination of both previous results shows that [[symplectic manifolds]] don't decompose as a [[connected sum]] $M#N$ with $b_2^+(M),b_2^+(N)\geq 1$. ([Nicolaescu 00, Crl. 4.6.2](#Nicolaescu00)) Since the classification of [[4-manifolds]] is extremely difficult and still unresolved, many attempts have therefore focussed on [[symplectic manifolds]].

Let $\mathfrak{s}_n$ be the [[spinᶜ structure]] on the [[orientation]]-reveresed second [[complex projective space]] $\overline{\mathbb{C}P^2}$ with $c_1(\mathfrak{s}_n)=(2n+1)c_1(S^5)$ (with the latter being the first [[Chern class]] of the [[principal U(1)-bundle]] $S^5\twoheadrightarrow\mathbb{C}P^2$ and a generator $c_1(S^5)\in H^2(\mathbb{C}P^2,\mathbb{Z})\cong\mathbb{Z}$).
\begin{proposition}
**(Blow-up formula)**
For a [[compact]] [[orientable]] [[Riemannian manifold|Riemannian]] [[4-manifold]] $M$ with a [[spinᶜ structure]] $\mathfrak{s}$, one has:
$$
|SW_{M#\overline{\mathbb{C}P^2},\mathfrak{s}#\mathfrak{s}_n}|
=\begin{cases}
0 & dim\mathcal{M}_{M,\mathfrak{s}}\lt\pm n(n+1) \\
|SW_M(\mathfrak{s})| & dim\mathcal{M}_{M,\mathfrak{s}}\geq n(n+1)
\end{cases}
$$
\end{proposition}

([Nicolaescu 00, Thrm. 4.6.7](#Nicolaescu00))

\begin{proposition}
For a [[Kähler surface]] $M$ with canonical [[spinᶜ structure]] $\mathfrak{s}_0$, one has:
$$
SW_M(\mathfrak{s}_0)
=1;
$$
$$
SW_M^+(\mathfrak{s}_0)
=1
$$
for $b_2^+(M)\geq 2$ and $b_2^+(M)=1$, respectively. If $M$ is a [[K3 surface]], then $\overline\mathfrak{s}_0=\mathfrak{s}_0$ and it is the only basic class.
\end{proposition}

([Nicolaescu 00, Thrm. 3.3.2 & Crl. 3.3.3](#Nicolaescu00))

## Related concepts

[[!include Seiberg-Witten theory -- table]]

## References

* {#Nicolaescu00} [[Liviu Nicolaescu]], *Notes on Seiberg-Witten theory*, American Mathematical Society (2000) &lbrack;[ISBN:978-0-8218-2145-9](https://bookstore.ams.org/GSM/28), [pdf](https://www3.nd.edu/~lnicolae/new1.pdf)&rbrack;

* {#EichhornFriedrich} [[Jürgen Eichhorn]], [[Thomas Friedrich]], _Seiberg-Witten theory_ ([pdf](http://matwbn.icm.edu.pl/ksiazki/bcp/bcp39/bcp3925.pdf))

* [[Simon Donaldson]], _The Seiberg-Witten equations and 4-manifold topology_ ([pdf](http://www.ams.org/journals/bull/1996-33-01/S0273-0979-96-00625-8/S0273-0979-96-00625-8.pdf))

* [[Matilde Marcolli]], _Seiberg-Witten gauge theory_, [pdf](http://www.its.caltech.edu/~matilde/swcosi.pdf)

On [[Seiberg-Witten invariants]] and [[symplectic manifolds]]:

* {#KotschickSWsymplectic95} [[Dieter Kotschick]], _The Seiberg-Witten invariants of symplectic four-manifolds_ (1995) &lbrack;[pdf](https://users.math.msu.edu/users/parker/993Spring11/Kotschick.pdf)&rbrack;

* {#KotschickMorganTaubes95} [[Dieter Kotschick]], [[John Morgan]], and [[Clifford Taubes]], _Four-Manifold without symplectic structure but with non-trivial Seiberg-Witten invariants_, Mathematical Research Letters **2**, pp. 119–124 (1995) &lbrack;[doi:10.4310/MRL.1995.v2.n2.a1](https://doi.org/10.4310/MRL.1995.v2.n2.a1) [pdf](https://projecteuclid.org/journals/mathematical-research-letters/volume-2/issue-2/Four-manifolds-without-symplectic-structures-but-with-nontrivial-Seiberg-Witten/10.4310/MRL.1995.v2.n2.a1.pdf)&rbrack;

See also:

* Wikipedia, _[Seiberg-Witten invariants](https://en.wikipedia.org/wiki/Seiberg%E2%80%93Witten_invariants)_

[[!redirects Seiberg-Witten invariants]]
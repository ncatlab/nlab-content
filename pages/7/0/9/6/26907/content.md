+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Differential topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Donaldson's theorem states that the [[intersection form]] of a [[compact]] [[orientable]] [[4-manifold]] is [[diagonalizable matrix|diagonalizable]] if it is [[definite]]. It was proven by [[Simon Donaldson]] in 1983 in [Donaldson 83](#Donaldson93) (with additionaly using [[simply connected|simple-connectedness]]) and improved in 1987 in [Donaldson 87](#Donaldson87) (without using [[simply connected|simple-connectedness]]). It became one of the reasons for him getting the Fields Medal in 1986 due to the new method of using the [[moduli space]] of the anti-self-dual [[Yang-Mills equations]] (ASDYM equations) to study the base manifold, which became the ground of [[Donaldson theory]].

Central consequences of Donaldson's theorem are the existence of [[exotic smooth structures]] on euclidean space in four dimensions and the failure of the [[h-cobordism theorem]] in four dimensions.

## Sketch of proof

Let $X$ be a [[compact]] [[orientable]] [[4-manifold]] and $P\twoheadrightarrow X$ be a principal $SU(2)$-bundle. According to the [[Atiyah-Singer index theorem]], the dimension of the moduli space $\mathcal{M}^-$ of anti-self-dual Yang-Mills connections (ASDYM connections) is given by:
$$
\dim\mathcal{M}^-
=8\langle c_2(P),[X]\rangle
-3(1-b_1(X)+b_+(X))
$$
with the second [[Chern class]] $c_2(P)\in H^4(X;\mathbb{Z})$, the [[fundamental class]] $[X]\in H_4(X;\mathbb{Z})$ given by the orientation of $X$, the Kronecker pairing $\langle-,-\rangle\colon H^4(X;\mathbb{Z})\times H_4(X;\mathbb{Z})\rightarrow\mathbb{Z}$ (which is often obmitted), the first [[Betti number]] $b_1(X)=\dim H_1(X;\mathbb{R})$ and the dimension $b_+(X)$ of the positive definite subspace of $H^2(X;\mathbb{R})$ with respect to the [[intersection form]].

If considering a [[simply connected]] $X$ as in the original version, then $H_1(X;\mathbb{Z})\cong\pi_1(X)^\mathrm{ab}$ and hence $b_1(X)=0$, which simplifies the formula. Consider a principal $SU(2)$-bundle $P$ with $\langle c_2(P),[X]\rangle=1$, hence $\dim\mathcal{M}^-=5$. Reducible connections modulo gauge, which are the singularities of $\mathcal{M}^-$, correspond to decompositions $P\times_{SU(2)}\mathbb{C}^2\cong L\oplus L^{-1}$ with a complex line bundle $L\twoheadrightarrow X$, which implies:
$$
c_2(P)
=c_2(P\times_{SU(2)}\mathbb{C}^2)
=c_1(L\oplus L^{-1})
=-c_1(L)\smile c_1(L);
$$
$$
Q(c_1(L),c_1(L))
=-\langle c_1(L)\smile c_1(L),[X]\rangle
=-\langle c_2(P),[X]\rangle
=-1.
$$
Let $n(Q)$ be the number of pairs $\pm\alpha\in H^2(X;\mathbb{Z})$ with $Q(\alpha,\alpha)=-1$, then $n(Q)\leq\operatorname{rk}(Q)$ with equality iff $Q$ is [[diagonalizable matrix|diagonalizable]].

$\mathcal{M}^-$ resembles the base manifold $X$ at infinity and the [[complex projective plane]] $\mathbb{C}P^2$ around the $n(Q)$ singularities. Gluing them in yields a [[compactification]], which contains a cobordism between $X$ and $n(Q)$ disjoint $\mathbb{C}P^2$. Since the [[signature]] is a coborism invariant, this implies:
$$
\operatorname{rk}(Q)
=\sigma(X)
=\sigma\left(\coprod_{n(Q)}\mathbb{C}P^2\right)
=n(Q)\sigma(\mathbb{C}P^2)
=n(Q).
$$

## Application to the 4-sphere

The [[4-sphere]] $S^4$ is a [[compact]] [[orientable]] [[4-manifold]]. Although its intersection form is trivial, it gives insight into the concepts used in the proof and their relation to each other. The principal $SU(2)$-bundle over $S^4$ with [[Chern class]] $1$ is the [[quaternionic]] [[Hopf fibration]] $S^7\twoheadrightarrow S^4$. It can abstractly be defined as the [[Hopf construction]] of the group structure on $S^3\cong SU(2)$ or more directly by the unit quaternions $Sp(1)\cong SU(2)$ acting on both components of $S^7\subset\mathbb{H}^2$ and the projection on the [[orbit space]], which is the [[quaternionic projective space]] $\mathbb{H}P^1\cong S^4$. The adjoint [[vector bundle]] $Ad(P)=P\times_{\mathfrak{su}(2)}SU(2)$ is the [[quaternionic]] [[tautological line bundle]] (considered as complex plane bundle) $\gamma_{\mathbb{H}}^{1,1}$ again defined using the identification $S^4\cong\mathbb{H}P^1$, in which points in $S^4$ correspond to one-dimensional linear subspaces of $\mathbb{H}^2$. One has $H_1(S^4;\mathbb{Z})=1$ and $H^2(S^4;\mathbb{Z})=1$, hence $b_1(S^4)=0$ and $b_+(S^4)=0$.According to the above formula, this yields $\dim\mathcal{M}^-=5$, which for [[instantons]] corresponds to the four freedoms regarding position and the one freedom regarding size.

See also:

* [[Kronheimer-Mrowka basic class]]

## References

* {#Donaldson83} [[Simon Donaldson]]. _An application of gauge theory to four-dimensional topology_. In: Journal of Differential Geometry. 18. Jahrgang, Nr. 2, 1. Januar 1983, [doi:10.4310/jdg/1214437665](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-18/issue-2/An-application-of-gauge-theory-to-four-dimensional-topology/10.4310/jdg/1214437665.full)
* {#Donaldson87} [[Simon Donaldson]]. _The orientation of Yang-Mills moduli spaces and 4-manifold topology_. In: Journal of Differential Geometry. 26. Jahrgang, Nr. 3, 1. Januar 1987, [doi:10.4310/jdg/1214441485](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-26/issue-3/The-orientation-of-Yang-Mills-moduli-spaces-and-4-manifold/10.4310/jdg/1214441485.full)

## Related concepts

* Wikipedia, _[Donaldson's theorem](https://en.wikipedia.org/wiki/Donaldson%27s_theorem)_

[[!redirects Donaldson's Theorem]]
[[!redirects Donaldson theorem]]
[[!redirects Donaldson Theorem]]
[[!redirects Donaldson's Diagonalisibility Theorem]]
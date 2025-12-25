+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Super-geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Idea

The _Seiberg-Witten moduli space_ (short _SW moduli space_, also _monopole moduli space_) is the [[moduli space]] of the [[Seiberg-Witten equations]], hence the space of its solutions up to [[gauge]]. It is used to defined the [[Seiberg-Witten invariants]] used to study [[4-manifolds]]. A very useful property of the Seiberg-Witten moduli space is that it is always [[compact]], which is an improvement over the previously used [[Yang-Mills moduli space]] and allowed to simplify the derivation of many results from [[Donaldson theory]]. The Seiberg-Witten moduli space is named after [[Nathan Seiberg]] and [[Edward Witten]], who introduced the underlying [[Seiberg-Witten equations]] in 1994.

## Basics

Let $M$ be a [[compact]] [[orientable]] [[Riemannian manifold|Riemannian]] [[4-manifold]] with [[Riemannian metric]] $g\in\Gamma^\infty(S^2T^*M)$ and [[spinᶜ structure]] $\mathfrak{s}\colon M\rightarrow BSpin^\mathrm{c}(4)$. Because of the [[exceptional isomorphism]]: ([Perutz 2002, p. 2](#Perutz02), [Naber 11, Eq. (A.2.34) and (A.2.35)](#Naber11))
$$
Spin^\mathrm{c}(4)
\cong U(2)\times_{U(1)}U(2)
=\{A^\pm\in U(2)|det(A^-)=det(A^+)\}
$$
the [[spinᶜ structure]] $\mathfrak{s}$ consists of two complex plane bundles $W^\pm\twoheadrightarrow M$, called _associated spinor bundles_ (whose sections are called _(anti) self-dual spinors_), with same [[determinant line bundle]] $L=det(W^\pm)$. Since the [[determinant line bundle]] preserves the first [[Chern class]], one has $c_1(\mathfrak{s})\coloneqq c_1(L)=c_1(W^\pm)$ with $c_1(\mathfrak{s})mod 2=w_2(M)$. ([Perutz 2002, p. 2](#Perutz02)) Given a [[fundamental class]] $[M]_\mathbb{Z}\in H^4(M,\mathbb{Z})\cong\mathbb{Z}$ and its reduction $
[M]_{\mathbb{Z}_2}:=[M]_\mathbb{Z}\operatorname{mod}2\in H^4(M,\mathbb{Z}_2)\cong\mathbb{Z}_2$, one therefore has:
$$
c_1^2(\mathfrak{s})[M]_\mathbb{Z} mod 2
=w_2^2(M)[M]_{\mathbb{Z}_2}
=\sigma(M) mod 2,
$$
hence $
c_1^2(\mathfrak{s})[M]_\mathbb{Z}-\sigma(M)$ is always even.

Let $\Omega_+^2(M)$ be the space of _self-dual forms_ fulfilling $\star\eta=\eta$ and let $\mathcal{H}_+^2(M)$ be the vector subspace of additionally harmonic forms fulfilling $\Delta\eta=0$. Let $b_+(M)=dim\mathcal{H}_+^2(M)$ be the _self-dual Betti number_, then there is a vector subspace $\Pi\lt\Omega_+^2(M)$ with $codim\Pi=b_+(M)$ (using the [[Hodge decomposition]]), so that a self-dual form $\eta\in\Omega_+^2(M)$ is the self-dual part of the [[curvature form]] of a connection $A\in\Omega^1(M)$, hence:
$$
\eta
=F_A^+
=\frac{1}{2}(\star d A+d A),
$$
if and only if $\eta\in\Pi$. Both the vector subspace and this result play an essential role as they are the reason the [[Seiberg-Witten equations]] are perturbed with a self-dual form before considering their [[moduli space]]. Both also lead to topological obstructions since for $b_+(X)=0$ there is no complement and for $b_+(X)=1$ the complement is not connected. Let $\Omega_-^2(X)$ be the analogous space of _anti self-dual forms_ with $\star\eta=-\eta$ and $\mathcal{H}_-^2(M)$ be the analogous vector subspace of additionally harmonic forms fulfilling $\Delta\eta=0$. Let $b_-(M)=dim\mathcal{H}_-^2(M)$ be the _anti self-dual Betti number_, then the second [[Betti number]] and [[signature]] can be expressed as:
$$
b_2(M)
=b_+(M)
+b_-(M);
$$
$$
\sigma(M)
=b_+(M)
-b_-(M).
$$
Both formulas, which are later used to calculate the dimension of the [[moduli space]], can also be reversed:
$$
b_+(M)
=\frac{1}{2}(b_2(M)+\sigma(M));
$$
$$
b_-(M)
=\frac{1}{2}(b_2(M)-\sigma(M)).
$$

## Configuration space

It is helpful to first consider the space of all possible solutions. Since the space of connections on the complex [[line bundle]] $L$ is an affine vector space, it is helpful to chose a single such connection $d_A$ and express every other as being shifted from it by a form $ia\in\Omega^1(M,\mathfrak{u}(1))$ with $a\in\Omega^1(M)$ using $\mathfrak{u}(1)\cong i\mathbb{R}$. Self-dual spinors also form a vector space with the zero section providing a canonical center. Let the _configuration space_ and _reduced configuration space_ be: ([Moore 2010, p. 77-79](#Moore10)) 
$$
\mathcal{A}
\coloneqq\{(d_A-ia,\psi)|a\in\Omega^1(M),\psi\in\Gamma^\infty(W^+)\};
$$
$$
\mathcal{A}^*
\coloneqq\{(d_A-ia,\psi)\in\mathcal{A}|\psi\neq 0\}.
$$
Since the reduced configuration space $\mathcal{A}^*$ is an infinite dimensional vector space without a single point and hence [[homotopy equivalent]] to the [[infinite-dimensional sphere]], it is contractible.

Although the definition of the reduced configuration space $\mathcal{A}^*$ is mainly motivated by the action of the [[gauge group]] below, its excluded cases are already important in the [[Seiberg-Witten equations]] themselves, which then reduced to the [[self-dual Yang-Mills equations]].

## Gauge group

Smooth maps $g\colon M\rightarrow U(1)$ act on the elements of the configuration space by: ([Perutz 2002, p. 6](#Perutz02), [Moore 2010, p. 77-79](#Moore10), [Naber 11, Eq. (A.4.15)](#Naber11))
$$
g\cdot(d_A-ia,\psi)
=(d_A-ia+g d(g^{-1}),g\psi).
$$
Hence the _gauge group_ can be taken as: ([Perutz 2002, p. 6](#Perutz02), [Moore 2010, p. 77-79](#Moore10))
$$
\mathcal{G}
\coloneqq C^\infty(M,U(1)).
$$
Using that the first [[unitary group]] $U(1)$ is the [[Eilenberg-MacLane space]] $K(\mathbb{Z},1)$, which [[Brown representability theorem
|classifies]] [[singular cohomology]], as well as the [[universal coefficient theorem]] and the [[Hurewicz theorem]] yields:
$$
[M,U(1)]
=[M,K(\mathbb{Z},1]
=H^1(M,\mathbb{Z})
\cong\Hom(H_1(M,\mathbb{Z}),\mathbb{Z})
=\Hom(\pi_1(M)^\mathrm{ab},\mathbb{Z}).
$$
Hence for $M$ [[simply connected]] or more generally if its [[fundamental group]] is [[perfect group|perfect]], every gauge is [[nullhomotopic]] and therefore has a global [[logarithm]], meaning that for every smooth map $g\colon M\rightarrow U(1)$ there exists a smooth map $u\colon M\rightarrow\mathbb{R}$ with $g=e^{iu}$. In this case, the action on the configuration space simplifies to: ([Moore 2010, p. 77-79](#Moore10))
$$
e^{iu}\cdot(d_A-ia,\psi)
=(d_A-i(a+d u),e^{iu}\psi).
$$
For a base point $x_0\in M$, the [[gauge group]] can be separated as a product using the _based gauge group_:
$$
\mathcal{G}_0
\coloneqq\{g\in\mathcal{G}|g(x_0)=1\};
$$
$$
\mathcal{G}
=\mathcal{G}_0\times U(1).
$$
As the product shows, the gauge group $\mathcal{G}$ is not contractible. But as the argument above shows, for $M$ [[simply connected]], the based gauge group $\mathcal{G}_0$ is contractible.

## Moduli space

Since both the [[gauge group]] $\mathcal{G}$ and its [[subgroup]], the based gauge group $\mathcal{G}_0$, act on the configuration space $\mathcal{A}$ and its subspace, the reduced configuration space $\mathcal{A}^*$, there are [[quotient spaces]]: ([Nicolaescu 2000, p. 89](#Nicolaescu00), [Kronheimer & Mrowka 2007, Def. 1.3.1. & Eq. (1.16)](#KronheimerMrowka07), [Moore 2010, p. 77-79](#Moore10), [Naber 11, p. 392](#Naber11))
$$
\mathcal{B}
\coloneqq\mathcal{A}/\mathcal{G};
$$
$$
\widetilde\mathcal{B}
\coloneqq\mathcal{A}/\mathcal{G}_0;
$$
$$
\mathcal{B}^*
\coloneqq\mathcal{A}^*/\mathcal{G};
$$
$$
\widetilde\mathcal{B}^*
\coloneqq\mathcal{A}^*/\mathcal{G}_0.
$$
As the formula of the action above shows, the [[gauge group]] $\mathcal{G}$ doesn't act free on the configuration space $\mathcal{A}$, since the points with vanishing self-dual spinor field $\psi=0$ are invariant under all constant gauges $g=const$, but it therefore does act free on the reduced configuration space $\mathcal{A}^*$ and the based gauge group $\mathcal{G}_0$ even acts free on both. $\mathcal{B}$ therefore has singularities, while the other spaces don't. If $M$ is [[simply connected]], then $\widetilde\mathcal{B}$ can furthermore be identified with a linear subspace of the configuration space $\mathcal{A}$ by: ([Moore 2010, p. 77-79](#Moore10))
$$
\widetilde\mathcal{B}
\cong\{(d_A-ia,\psi)\in\mathcal{A}|\delta a=0\}.
$$
Equivalently, for every $a\in\Omega^1(M)$, there is a unique smooth map $u\colon M\rightarrow\mathbb{R}$ with $\delta(a+\mathrm{d}u)=\delta a+\Delta u=0$, which can be shown again using the [[Hodge decomposition]] $C^\infty(M,\mathbb{R})=\mathcal{H}_0(M)\oplus\delta\Omega^1(M)$ with $\mathcal{H}_0(M)$ just being the constant functions for $M$ [[connected]]. ([Moore 2010, p. 77-79](#Moore10))

Although the canonical projection $\widetilde\mathcal{B}\rightarrow\mathcal{B}$ might not be even be a [[fiber bundle]] due to the singularities, the canonical projection $\widetilde\mathcal{B}^*\rightarrow\mathcal{B}^*$, after a suitable Sobolev completion, is a [[principal U(1)-bundle]]. For $M$ [[simply connected]], $\widetilde\mathcal{B}^*$ is contractible, since $\mathcal{A}^*$ always is and $\mathcal{G}_0$ is in this case as argued before. It then follows from the [[long exact sequence]] of [[homotopy groups]] of the [[principal U(1)-bundle]] $\widetilde\mathcal{B}^*\rightarrow\mathcal{B}^*$, that $\mathcal{B}^*$ is an [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$ (as $S^1$ is a $K(\mathbb{Z},1)$) and since the infinite [[complex projective space]] $\mathbb{C}P^\infty$ is as well, there is a [[weak homotopy equivalence]] $\mathcal{B}^*\rightarrow\mathbb{C}P^\infty$. ([Moore 2010, p. 81](#Moore10)) Homotopy classes of such maps are classified by $[K(\mathbb{Z},2),K(\mathbb{Z},2)]\cong\mathbb{Z}$ and the [[weak homotopy equivalence]] must correspond to a generator $\pm 1\in\mathbb{Z}$. But the [[principal U(1)-bundle]] also bijectively corresponds to the [[homotopy class]] of a classifying map $f\colon\mathcal{B}^*\rightarrow BU(1)\cong\mathbb{C}P^\infty$ with $\widetilde\mathcal{B}^*\cong f^*EU(1)\cong f^*S^\infty$, which falls under the exact same classification, but doesn't necessarily correspond to a generator. It is exactly the first [[Chern class]] $c_1(\mathcal{B})\in H^2(\mathcal{B}^*,\mathbb{Z})\in\mathbb{Z}$ of the [[principal U(1)-bundle]], but the [[perturbed Seiberg-Witten equations]] need to enter for it to be of use for the [[Seiberg-Witten invariants]]. Its [[moduli spaces]] are then given by the subspaces of its solutions: ([Perutz 2002, p. 6](#Perutz02), [Moore 2010, p. 81](#Moore10), [Naber 11, p. 391](#Naber11))
$$
\mathcal{M}
\coloneqq\{[d_A-ia,\psi]\in\mathcal{B}|(d_A-ia,\psi)\text{fulfills SW eq.}\};
$$
$$
\mathcal{M}_\eta
\coloneqq\{(d_A-ia,\psi)\in\widetilde\mathcal{B}|(d_A-ia,\psi)\text{fulfills pSW eq. with per.}\eta\};
$$
$$
\widetilde\mathcal{M}_\eta
\coloneqq\{(d_A-ia,\psi)\in\widetilde\mathcal{B}|(d_A-ia,\psi)\text{fulfills pSW eq. with per.}\eta\}.
$$
With the canonical projection $\widetilde\mathcal{B}\rightarrow\mathcal{B}$, there is a canonical projection $\widetilde\mathcal{M}_\eta\rightarrow\mathcal{M}_\eta$. Since the former isn't a [[fiber bundle]], it seems that the latter isn't as well. But this isn't necessarily the case and exactly the reason why the [[Seiberg-Witten equations]] are considered with a perturbation. For this, the self-dual Betti number is important:

* If $b_+(M)\geq 1$, then a perturbation $\eta\in\Omega_+^2(M)\setminus\Pi\neq\emptyset$ forces solutions of the [[perturbed Seiberg-Witten equations]] with $\psi=0$ to fulfill $F_A^+=\eta$, which is not possible due to $\eta\notin\Pi$. Hence both perturbed [[moduli spaces]] avoid all singularities in this case and $\widetilde\mathcal{M}_\eta\rightarrow\mathcal{M}_\eta$ becomes a [[principal U(1)-bundle|principal U(1)-subbundle]] of $\widetilde\mathcal{B}^*\rightarrow\mathcal{B}^*$ with first [[Chern class]]$c_1(\widetilde\mathcal{M}_\eta)\in H^2(\mathcal{M}_\eta,\mathbb{Z})$, which is then used to define the [[Seiberg-Witten invariants]].

* If $b_+(M)\geq 2$, then any two perturbations $\eta_1,\eta_2\in\Omega_+^2(M)\setminus\Pi\neq\emptyset$ can furthermore be connected by a path $\gamma\colon[0,1]\rightarrow\Omega_+^2(M)\setminus\Pi$, which describes a [[bordism]] $\widetilde\mathcal{M}_{\eta_1}\rightarrow\widetilde\mathcal{M}_{\eta_2}$. Hence all perturbations give the same [[bordism]] class. ([Moore 2010, p. 100](#Moore10)) (If $b_+(M)=1$, one has to chose a connected component of $\Omega_+^2(M)\setminus\Pi$, which might give two different [[bordism classes]].)

For the [[Seiberg-Witten invariant]], which is in particular [[Chern number]], the necessary amount of [[cup products]] of the [[Chern class]] with itself is evaluated with the [[fundamental class]] of the [[moduli space]] in the [[Kronecker pairing]]. Since the [[Chern class]] has even degree, the [[moduli space]] must have even dimension for this to work and it furthermore has to be known precisely for the amount of [[cup products]]. First relating it to the [[index]] of the [[Dirac operator]] and then applying the [[Atiyah-Singer index theorem]] yields formulas containing the [[Euler characteristic]] and the [[signature]]:

Let $M$ be [[simply connected]]. If $ind(D_A^+)\gt 0$ for $b_+(M)=0$ or $b_+(M)\gt 0$, then $\mathcal{M}_\eta$ is an [[oriented]] [[smooth manifold]] with dimension: ([Gompf & Stipsicz 99, Thrm. 2.4.24](#GompfStipsicz99), [Nicolaescu 2000, Lem. 2.2.10](#Nicolaescu00), [Kronheimer & Mrowka 2007, Thrm 1.4.4.](#KronheimerMrowka07), [Moore 2010, Transversality Theorem 2 on p. 91](#Moore10), [Naber 11, p. 394](#Naber11)) 
$$
dim\mathcal{M}_\eta
=2 ind(D_A^+)
-b_+(M)
-1
=\frac{1}{4}(c_1^2(\mathfrak{s})[M]-2\chi(M)-3\sigma(M)).
$$
While the first expression is obviously always an integer, it is more difficult to see for the second expression. But as shown in the basics, $c_1^2(\mathfrak{s})[M]-\sigma(M)$ is always even, which already makes the term in the brackets even as well.

Let $M$ be [[simply connected]]. If $b_+(M)\gt 0$, then $\widetilde\mathcal{M}_\eta$ is a [[compact]] ([Donaldson 1996, Eq. (7)](#Donaldson96), [Moore 2010, Compactness Theorem on p. 83](#Moore10)) [[oriented]] [[smooth manifold]] with dimension: ([Moore 2010, Transversality Theorem 1 on p. 86](#Moore10))
$$
dim\widetilde\mathcal{M}_\eta
=2 ind(D_A^+)
-b_+(M)
=\frac{1}{4}(c_1^2(\mathfrak{s})[M]-2\chi(M)-3\sigma(M))+1.
$$
(Some literature uses the convention $L^2=\det(W^\pm)$ since it is indeed the square of a line bundle, which makes the above formula not include a factor in front of the [[Chern class]].) Hence for $b_+(M)$ even, $dim\mathcal{M}_\eta$ is also even and the [[Seiberg-Witten invariants]], which are independent of the [[Riemannian metric]] $g$ and the perturbation $\eta$ [Kronheimer & Mrowka 2007, Thrm 1.5.2.](#KronheimerMrowka07)  as argued above for the latter, can then be defined as: ([Donaldson 1996, Eq. (6)](#Donaldson96), [Gompf & Stipcisz 99, Def. 2.4.2](#GompfStipcisz99), [Nicolaescu 2000, p. 113](#Nicolaescu00), [Kronheimer & Mrowka 2007, Def. 1.5.3. & 1.5.4.](#KronheimerMrowka07))
$$
SW(M,\mathfrak{s})
\coloneqq\langle c_1(\mathcal{M}_\eta)^{\frac{dim\widetilde\mathcal{M}_\eta}{2}},[\widetilde\mathcal{M}_\eta]\rangle.
$$

## Related entries

* [[Yang-Mills moduli space]] (instanton moduli space)

## References

* {#Donaldson96} [[Simon Donaldson]], _The Seiberg-Witten equations and 4-manifold topology_ (1996), _Bulletin of the American Mathematical Society, *33* (1): 45–70, &lbrack;[doi:10.1090/S0273-0979-96-00625-8](https://doi.org/10.1090%2FS0273-0979-96-00625-8)&rbrack;

* {#GompfStipsicz99} [[Robert Gompf]], [[András Stipsicz]]: _4-Manifolds and Kirby Calculus_, Graduate Studies in Mathematics **20**, AMS (1999) &lbrack;[ISBN:978-0-8218-0994-5](https://www.ams.org/books/gsm/020), [doi:10.1090/gsm/020](https://www.ams.org/books/gsm/020)&rbrack;

* {#Nicolaescu00} [[Liviu Nicolaescu]], _Notes on Seiberg-Witten Theory_ (2000), &lbrack;[pdf](https://www3.nd.edu/~lnicolae/swnotes.pdf)&rbrack;

* {#Perutz02} Tim Perutz, _Basics of Seiberg-Witten theory_ (May 2002), &lbrack;[pdf](https://www.imperial.ac.uk/media/imperial-college/research-centres-and-groups/geometry/junior-geometry-seminar/Seiberg-Witten-theory.pdf)&rbrack;

* {#KronheimerMrowka07} [[Peter Kronheimer]], [[Tomasz Mrowka]], _Monopoles and Three-Manifolds_ (2007), &lbrack;[ISBN:978-0-521-88022-0](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/kronmrowka.pdf)&rbrack;

* {#Moore10} John Douglas Moore, _Lecture Notes on Seiberg-Witten Invariants (Revised Second Edition)_, &lbrack;[pdf](https://web.math.ucsb.edu/~moore/seibergwittenrev2edition.pdf)&rbrack;

* {#Naber11} [[Gregory L. Naber]], *Topology, Geometry and Gauge fields -- Foundations*,  Texts in Applied Mathematics **25** (2011) &lbrack;[doi:10.1007/978-1-4419-7254-5](https://doi.org/10.1007/978-1-4419-7254-5)&rbrack;

See also:

* Wikipedia, _[Seiberg–Witten moduli space](https://en.wikipedia.org/wiki/Seiberg–Witten_moduli_space)_

[[!redirects SW moduli space]]
[[!redirects monopole moduli space]]
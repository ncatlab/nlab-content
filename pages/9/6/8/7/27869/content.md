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

If the scalar function is the *Seiberg-Witten action functional*, then the gradient flow is called *Seiberg-Witten flow*. It is described by the [[Seiberg-Witten equation]] and can be used to find solutions of the [[Seiberg-Witten equations]], which are the critical points.

The [[Seiberg-Witten flow]] was introduced by [[Lorenz Schabrun]] in his 2010 PhD thesis. [Schabrun 10](#Schabrun10) It is named after [[Nathan Seiberg]] und [[Edward Witten]], who introduced [[Seiberg-Witten theory]] in 1994.

## Basics

Let $M$ be a [[compact]] [[orientable]] [[Riemannian manifold|Riemannian]] [[4-manifold]] with [[Riemannian metric]] $g\in\Gamma^\infty(S^2T^*M)$ and [[spinᶜ structure]] $\mathfrak{s}\colon M\rightarrow BSpin^\mathrm{c}(4)$. Because of the [[exceptional isomorphism]]: ([Perutz 2002, p. 2](#Perutz02))
$$
Spin^\mathrm{c}(4)
\cong U(2)\times_{U(1)}U(2)
=\{A^\pm\in U(2)|det(A^-)=det(A^+)\}
$$
the [[spinᶜ structure]] $\mathfrak{s}$ consists of two complex plane bundles $W^\pm\twoheadrightarrow M$, called _associated spinor bundles_ (whose sections are called _(anti) self-dual spinors_), with same [[determinant line bundle]] $L=det(W^\pm)$. Since the [[determinant line bundle]] preserves the first [[Chern class]], one has $c_1(\mathfrak{s})\coloneqq c_1(L)=c_1(W^\pm)$ with $c_1(\mathfrak{s})mod 2=w_2(M)$. ([Perutz 2002, p. 2](#Perutz02)) Let $\mathcal{A}$ be the space of connections on $L$.

## Definition

The *Seiberg-Witten action functional* is given by:
$$
\begin{aligned}
S_{SW}(A,\varphi)
&=\int_M|F_A^+|^2
+|\nabla_A\varphi|^2
+\frac{1}{4}scal|\varphi|^2
+\frac{1}{8}|\varphi|^4\mathrm{d}vol_g \\
&=\int_M\frac{1}{2}|F_A|^2
+|\nabla_A\varphi|^2
+\frac{1}{4}scal|\varphi|^2
+\frac{1}{8}|\varphi|^4\mathrm{d}vol_g
+\pi^2c_1(\mathfrak{s})^2[M]
\end{aligned}
$$

([Schabrun 10, Eq. (4) & (6)](#Schabrun10))

The last expression uses [[Chern-Weil theory]] to express the [[Chern class]], which as a constant has no effect on the flow equations and can therefore be obmitted, independent of the connection $A\in\mathcal{A}$ as:
$$
c_1(\mathfrak{s})^2[M]
=\frac{1}{4\pi^2}\int_M|F_A^+|^2-|F_A^-|^2\mathrm{d} vol_g.
$$

([Schabrun 10, Eq. (5)](#Schabrun10))

The gradients of the Seiberg-Witten action functional are given by:
$$
grad(S_{SW})(A,\Phi)_1
=\mathrm{d}^*F_A
+i Im\langle\nabla_A\Phi,\Phi\rangle,
$$
$$
grad(S_{SW})(A,\Phi)_2
=\nabla_A^*\nabla_A\Phi
-\frac{1}{4}(scal+\|\Phi\|^2)\Phi.
$$

([Schabrun 10, Eq. (7) & (8)](#Schabrun10))

For an [[open interval]] $I\subseteq\mathbb{R}$, two $C^1$ maps $\alpha\colon I\rightarrow\mathcal{A}$ and $\varphi\colon I\rightarrow\Gamma^\infty(M,W^+)$ (hence [[continuously differentiable]]) fulfilling:
$$
\alpha'(t)
=-grad(S_{SW})(\alpha(t),\varphi(t))_1
=-\mathrm{d}^*F_{\alpha(t)}
-i Im\langle\nabla_{\alpha(t)}\varphi(t),\varphi(t)\rangle,
$$
$$
\varphi'(t)
=-grad(S_{SW})(\alpha(t),\varphi(t))_2
=-\nabla_{\alpha(t)}^*\nabla_{\alpha(t)}\varphi(t)
-\frac{1}{4}(scal+\|\varphi(t)\|^2)\varphi(t).
$$
are a *Seiberg-Witten flow*.

([Schabrun 10, Eq. (9) & (10)](#Schabrun10))

## Related entries

* [[Yang-Mills flow]]
* [[Yang-Mills-Higgs flow]]

## References

* {#Nicolaescu00} [[Liviu Nicolaescu]], *Notes on Seiberg-Witten theory*, American Mathematical Society (2000) &lbrack;[ISBN:978-0-8218-2145-9](https://bookstore.ams.org/GSM/28), [pdf](https://www3.nd.edu/~lnicolae/new1.pdf)&rbrack;
* {#Perutz02} Tim Perutz, _Basics of Seiberg-Witten theory_ (May 2002), &lbrack;[pdf](https://www.imperial.ac.uk/media/imperial-college/research-centres-and-groups/geometry/junior-geometry-seminar/Seiberg-Witten-theory.pdf)&rbrack; 
* {#HongSchabrun09} Min-Chun Hong, [[Lorenz Schabrun]], _Global Existence for the Seiberg-Witten Flow_ (2009), &lbrack;[arXiv:0909.1855](https://arxiv.org/abs/0909.1855)&rbrack;
* {#Schabrun10} [[Lorenz Schabrun]], _Seiberg-Witten Flow in Higher Dimensions_ (2010), &lbrack;[arXiv:1003.1765](https://arxiv.org/abs/1003.1765)&rbrack;

See also:

* Wikipedia, _[Seiberg-Witten flow](https://en.wikipedia.org/wiki/Seiberg%E2%80%93Witten_flow)_
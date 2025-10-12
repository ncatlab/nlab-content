+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Vafa-Witten twist_ is one of three inequivalent [[topological twists]] in [[topologically twisted D=4 super Yang-Mills theory]], the other two being the _Donaldson-Witten twist_ and the _Kapustin-Witten twist_ (or _geometric Langlands twist_). The _Vafa-Witten equations_ are the equations obtained from the Vafa-Witten twist.

## Formulation

Consider

* $G$ a [[Lie group]] and $\mathfrak{g}$ its [[Lie algebra]],

* $X$ an [[orientable]] [[Riemannian manifold|Riemannian]] [[4-manifold]] with Riemannian metric $g$ and volume form $vol_g$,

* $P\twoheadrightarrow X$ a [[principal bundle|principal $G$-bundle]] and $Ad(P)\coloneqq P\times_G\mathfrak{g}\twoheadrightarrow X$ its [[adjoint bundle]],

* $A\in\Omega^1(X,Ad(P))$ a [[principal connection]],

* $F_A\coloneqq\mathrm{d}A+\frac{1}{2}[A\wedge A]\in\Omega^2(X,Ad(P))$ its [[curvature]] and $F_A^+=\frac{1}{2}(F_A+\star F_A)$ its self-dual part,

* $a\in\Omega_+^2(X,Ad(P))$ a self-dual form.

The _Vafa-Witten equations_ are:
$$
\mathrm{d}_A a
=0;
$$
$$
F_A^+
=\frac{1}{8}[a\bullet a].
$$

([Clifford 17, Eq. (1)](#Clifford17), [Guan 22C, Eq (1.3)](#Guan22C))

For $a=0$, the Vafa-Witten equations reduce to the [[self-dual Yang-Mills equations]] $F_A^+=0$.

It is also possible to consider a generalization with a smooth section $\Phi\in\Gamma^\infty(X,Ad(P))$ given by:
$$
\mathrm{d}_A a
+\star\mathrm{d}_A\Phi
=0;
$$
$$
F_A^+
=\frac{1}{8}[a\bullet a]
+\frac{1}{2}[\Phi,a].
$$

([Tanaka 13, p. 2](#Tanaka13), [Tanaka 14, Eq. (1.1) & (1.2)](#Tanaka14), [Clifford 17, Eq. (1.6)](#Clifford17), [Manshot 23, Eq. (3.3)](#Manshot23), [Guan 22A, Eq (1.1)](#Guan22A), [Guan 22B, Eq (1.1)](#Guan22B) , [Guan 22C, Eq (1.1)](#Guan22C), [Dai & Guan 2025, Eq (1.1)](#DaiGuan25))

## References

*  {#Tanaka13} [[Yuuji Tanaka]], _Some boundedness properties of solutions to the Vafa-Witten equations on closed four-manifolds_ (2013), [arXiv:1308.0862](https://arxiv.org/abs/1308.0862) 
*  {#Tanaka14} [[Yuuji Tanaka]], _A perturbation and generic smoothness of the Vafa–Witten moduli spaces on closed symplectic four-manifolds_ (2014), [arXiv:1410.1691](https://arxiv.org/abs/1410.1691) 
* {#Clifford17} [[Clifford Taubes]], _The behavior of sequences of solutions to the Vafa-Witten equations_ (2017), [arXiv:1702.04610](https://arxiv.org/abs/1702.04610)
* {#Guan22A} [[Ren Guan]], _On the general part of the perturbed Vafa-Witten moduli spaces on 4-manifolds_ (2022), [arXiv:2207.03701](https://arxiv.org/abs/2207.03701)
* {#Guan22B} [[Ren Guan]], _A variation of the reduced Vafa-Witten equations on 4-manifolds_ (2022), [arXiv:2208.06131](https://arxiv.org/abs/2208.06131) 
* {#Guan22C} [[Ren Guan]], _Transversality of the perturbed reduced Vafa-Witten moduli spaces on 4-manifolds_ (2022), [arXiv:2212.01586](https://arxiv.org/abs/2212.01586) 
* {#Manshot23} [[Jan Manshot]], _Four-Manifold Invariants and Donaldson-Witten Theory_ (2023), [arXiv:2312.14709](https://arxiv.org/abs/2312.14709)
* {#DaiGuan25} [[Bo Dai]] and [[Ren Guan]], _A simple perturbation of Vafa-Witten equations and a transversality result_ (2025), [arXiv:2505.14702](https://arxiv.org/abs/2505.14702)

[[!redirects Vafa-Witten theory]]
[[!redirects Vafa-Witten theories]]

[[!redirects Vafa-Witten equation]]
[[!redirects Vafa-Witten equations]]
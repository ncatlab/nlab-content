+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The *linearized Yang-Mills equation* is a linearization of the non-linear [[Yang-Mills equation]], hence the best approximation by a linear equation at a given solution, called [[Yang-Mills connections]]. It is obtained as the differential of the *Yang-Mills map*, which maps the space of [[principal connections]] to their evaluation of the [[Yang-Mills equation]] term, so that its solutions are exactly those mapped to the origin. (Due to the [[affine space|affinity]] of the space of [[principal connections]] and the non-linearity, this is not the [[kernel]].)

Since the tangent space has the same dimension as its underlying manifold, the local virtual dimension of the [[Yang-Mills moduli space]] can be obtained from the linearization using the [[Atiyah-Singer index theorem]].

## Yang-Mills map

Consider the setup described in detail in [[Yang-Mills equation]]. The *Yang-Mills map* is given by:
$$
f\colon
\mathcal{A}\rightarrow\Omega^1(M,Ad(P)),
A\mapsto\delta_A F_A.
$$
$A\in\mathcal{A}$ is a solution of the [[Yang-Mills equations]] if and only if $f(A)=0$. The differential of the Yang-Mills map in it is given by:
$$
D_A f
=\delta_A d_A+\star[-,\star F_A]\colon
\Omega^1(M,Ad(P))\rightarrow\Omega^1(M,Ad(P)).
$$

## Linearized Yang-Mills equations

Let $B\in\Omega^1(M,Ad(P))$, then the linearized Yang-Mills equations at a solution $A\in\mathcal{A}$ are given by $D_A f(B)=0$ or equivalently by:
$$
\delta_A d_A B+\star[B,\star F_A]
=0.
$$

## Elliptic complex

Let $act\colon\mathcal{G}\rightarrow\mathcal{A}$ be the action of the [[gauge group]] $\mathcal{G}=Aut(P)$ on a solution $A$. Since the [[Yang-Mills equations]] are gauge invariant, one has $f\circ act=0$ for the composition and therefore $D_A f\circ D_1 act=0$ for their differential, which yields an [[elliptic complex]] $\mathcal{E}(A,\phi)$ given by:
$$
1
\rightarrow End(Ad(P))
\xrightarrow{D_1 act}\Omega^1(M,Ad(P))
\xrightarrow{D_A f}\Omega^1(M,Ad(P))
\rightarrow 1.
$$
It has the cohomology vector spaces:
$$
H^0(\mathcal{E}(A))
=ker(D_1 act);
$$
$$
H^1(\mathcal{E}(A))
=ker(D_A f)/img(D_1 act);
$$
$$
H^2(\mathcal{E}(A))
=\Omega^1(M,Ad(P))/img(D_A f).
$$
$H^0(\mathcal{E}(A))$ can be identified with the [[tangent space]] $T_1 Stab_A(\mathcal{G})$. $H^1(\mathcal{E}(A))$ can be identified with the [[tangent space]] $T_{[A]}\mathcal{M}$ of the [[Yang-Mills moduli space]]. If $H^0(\mathcal{E}(A))$ and $H^2(\mathcal{E}(A))$ vanish, then the [[analytic index]] is:
$$
ind\mathcal{E}(A,\psi)
=-dim H^0(\mathcal{E}(A))
+dim H^1(\mathcal{E}(A))
-dim H^2(\mathcal{E}(A))
=dim H^1(\mathcal{E}(A))
=dim T_{[A]}\mathcal{M}
$$
(For finite-dimensional [[vector spaces]] in the complex, these can replace the cohomology [[vector spaces]] in the index due to the [[homomorphism theorem]].) The [[Atiyah-Singer index theorem]] assures this [[analytic index]] to be equal to the [[topological index]], which depends only on [[topological invariants]].

## Related concepts

[[!include Yang-Mills theory -- table]]

[[!redirects Yang-Mills equations]]
[[!redirects YM equation]]
[[!redirects YM equations]]

[[!redirects Yang-Mills map]]
[[!redirects Yang-Mills maps]]
[[!redirects YM map]]
[[!redirects YM maps]]
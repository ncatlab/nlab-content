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

The *linearized Seiberg-Witten equations* are a linearization of the non-linear [[Seiberg-Witten equations]], hence the best approximation by a linear equation at a given solution, called Seiberg-Witten monopoles. They are obtained as the differential of the *Seiberg-Witten map*, which maps the space of [[principal connections]] and self-dual [[spinors]] to their evaluation of the [[Seiberg-Witten equations]] term, so that its solutions are exactly those mapped to the origin. (Due to the [[affine space|affinity]] of the space of [[principal connections]] and the non-linearity, this is not the [[kernel]].)

Since the tangent space has the same dimension as its underlying manifold, the local virtual dimension of the [[Seiberg-Witten moduli space]] can be obtained from the linearization using the [[Atiyah-Singer index theorem]].

## Seiberg-Witten map

Consider the setup described in detail in [[Seiberg-Witten equations]]. The *Seiberg-Witten map* is given by:
$$
f\colon
\mathcal{A}\oplus\Gamma^\infty(S^+)\rightarrow\Omega_+^2(M,\mathfrak{u}(1))\oplus\Gamma^\infty(S^-),
(A,\psi)\mapsto(F_A^+-\sigma(\psi),\partial_A\psi).
$$
$(A,\psi)\in\mathcal{A}$ is a solution of the [[Seiberg-Witten equations]] if and only if $f(A,\psi)=0$. the differential of the Seiberg-Witten map in it is given by:
$$
D_{(A,\psi)}f
=\begin{pmatrix}
d_+ & -D_\psi \\
\frac{1}{2}\psi & -\partial_A
\end{pmatrix}\colon
\Omega^1(M,\mathfrak{u}(1))\oplus\Gamma^\infty(S^+)\rightarrow\Omega_+^2(M,\mathfrak{u}(1))\oplus\Gamma^\infty(S^-).
$$

## Linearized Seiberg-Witten equations

Let $(B,\phi)\in\Omega^1(M,\mathfrak{u}(1))\oplus\Gamma^\infty(S^+)$, then the *linearized Seiberg-Witten equations* at a solution $(A,\psi)\in\mathcal{A}\oplus\Gamma^\infty(S^+)$ are given by $D_{A,\psi}f(B,\phi)=0$ or expanded by:
$$
d_+B
-D_\psi\phi
=0;
$$
$$
\frac{1}{2}B\cdot\psi
-\partial_A\phi
=0.
$$

## Elliptic complex

Let $act\colon\mathcal{G}\rightarrow\mathcal{A}\oplus\Gamma^\infty(S^+)$ be the action of the [[gauge group]] $\mathcal{G}=C^\infty(M,U(1))$ on a solution $(A,\psi)$. Since the [[Seiberg-Witten equations]] are gauge invariant, one has $f\circ act=0$ for the composition and therefore $D_{(A,\psi)}f\circ D_1 act=0$ for their differential, which yields an [[elliptic complex]] $\mathcal{E}(A,\phi)$ given by:
$$
1
\rightarrow C^\infty(M,\mathfrak{u}(1))
\xrightarrow{D_1 act}\Omega^1(M,\mathfrak{u}(1))\oplus\Gamma^\infty(S^+)
\xrightarrow{D_{(A,\psi)}f}\Omega_+^2(M,\mathfrak{u}(1))\oplus\Gamma^\infty(S^-)
\rightarrow 1.
$$
It has the cohomology vector spaces:
$$
H^0(\mathcal{E}(A,\phi))
=ker(D_1 act);
$$
$$
H^1(\mathcal{E}(A,\phi))
=ker(D_{(A,\psi)}f)/img(D_1 act);
$$
$$
H^2(\mathcal{E}(A,\phi))
=(\Omega_+^2(M,\mathfrak{u}(1))\oplus\Gamma^\infty(S^-))/img(D_{(A,\psi)}f).
$$
$H^0(\mathcal{E}(A,\phi))$ can be identified with the [[tangent space]] $T_1 Stab_{(A,\phi)}(\mathcal{G})$, so that $H^0(\mathcal{E}(A,\psi))=\{0\}$ is equivalent to $(A,\psi)$ being irreducible or $\psi\neq 0$. $H^1(\mathcal{E}(A,\psi))$ can be identified with the [[tangent space]] $T_{[A,\psi]}\mathcal{M}$ of the [[Seiberg-Witten moduli space]].
$$
ind\mathcal{E}(A,\psi)
=-\dim H^0(\mathcal{E}(A,\psi))
+\dim H^1(\mathcal{E}(A,\psi))
-\dim H^2(\mathcal{E}(A,\psi))
=\dim H^1(\mathcal{E}(A,\psi))
=dim T_{[A,\psi]}\mathcal{M}
$$
(For finite-dimensional [[vector spaces]] in the complex, these can replace the cohomology [[vector spaces]] in the index due to the [[homomorphism theorem]].) The [[Atiyah-Singer index theorem]] assures this [[analytic index]] to be equal to the [[topological index]], which depends only on [[topological invariants]].

## Related concepts

[[!include Seiberg-Witten theory -- table]]

[[!redirects Seiberg-Witten equations]]
[[!redirects SW equation]]
[[!redirects SW equations]]

[[!redirects Seiberg-Witten map]]
[[!redirects Seiberg-Witten maps]]
[[!redirects SW map]]
[[!redirects SW maps]]
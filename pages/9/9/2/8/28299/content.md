
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


\tableofcontents


## Idea

The *Floreanini-Jackiw Lagrangian* (FL, due to [Floreanini & Jackiw 1987](#FloreaniniJackiw1987)) is a [[Lagrangian density]] for a [[scalar field]] in 2-dimensions whose [[equations of motion]] single out (essentially) just the "right moving" ("chiral") half of solutions of the usual [[relativistic field theory|relativistic]] [[wave equation]]: the *[[chiral boson]]*. As such, the FJ-Lagrangian density is an approach, in low dimension, to the notoriously subtle problem of finding [[Lagrangian densities]] for [[self-dual higher gauge fields]].

The FL-Lagrangian arises also as the [[effective field theory|effective]] [[boundary field theory]] of [[abelian Chern-Simons theory]] ([Wen 1992 §2.5](#Wen1992), [1995 §3.3](#Wen1995), cf. [Tong 2016 §6.1.2](#Tong2016)). This realizes the FL theory as the abelian case of [[Wess-Zumino-Witten theory]] (cf. [[CS/WZW correspondence]]) and witnesses it as the [[effective field theory]] of [[edge modes]] in [[fractional quantum Hall systems]].

## From abelian Chern-Simons theory

The [[Lagrangian density]] of [[abelian Chern-Simons theory]] with [[gauge field]] [[differential 1-form|1-form]] $a$ is 

\[
  \propto \tfrac{1}{2} a \wedge \mathrm{d}a
  \mathrlap{\,.}
\]

Setting

\[
  a = \mathrm{d}\phi
\]

and on the 3D [[spacetime]] [[manifold with boundary|with boundary]] $\mathbb{R}^{0,1} \times \mathbb{R}^2_{y \leq 0}$ gives, by [[Stokes' theorem]], the [[boundary field theory|boundary]] Lagrangian density for $\phi$ ([Wen 1992 (2.62)](#Wen1992))

\[
  L(\phi) 
    = 
  \tfrac{1}{2} (\partial_x \phi) (\partial_{t'}\phi) 
\]

for $t'$ and $x$ two [[coordinate functions]] on the 2D [[spacetime]] $\mathbb{R}^2$. Understanding ([Wen '92 (2.64)](#Wen1992))

\[
  t' \coloneqq t - c x
\]

as a [[lightcone gauge]] coordinate, this is

\[
  L(\phi) 
    = 
  \tfrac{1}{2} (\partial_x \phi) 
  \big(
    \partial_{t} - c \partial_x\phi 
  \big) 
  \mathrlap{\,.}
\]

This is the FL-Lagrangian density:

## Lagrangian and Equations of motion

For $\phi$ a [[scalar field]] on $\mathbb{R}^2$ (the latter equipped with its canonical [[coordinate functions]], here denoted $t$ for *[[time]]* and $x$ for *[[space]]*), the FL [[Lagrangian density]] is ([FL '87 (20)](#FloreaniniJackiw1987)):

\[
  L(\phi)
  \;\coloneqq\;
  \tfrac{1}{2}
  (\partial_x\phi) 
  \big(
    \partial_t \phi
      - 
    c
    \partial_x \phi
  \big)
  \mathrlap{\,,}
\]

where $c \in \mathbb{R} \setminus \{0\}$ is a constant which sets the [[velocity]] (the [[speed of light]], often set to $c = 1$).

The corresponding [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] is 

\[
  \big(
    \partial_t - c \partial_x
  \big)
  \partial_x
  \phi
  = 0
  \mathrlap{\,.}
\]

The general solutions to this equation are of the form

\[
  \label{TheEquationOfMotion}
  \phi(t,x)
  = 
  \phi_c(x + c t)
  + 
  g(t)
\]

where $g$ is an arbitrary ([[smooth function|smooth]]) function of just the temporal coordinate $t$ (hence is a "spatial zero mode"), while $\phi_c$ is a solution of the *chiral/right-moving wave equation*

\[
  \big(
    \partial_t - c \partial_x
  \big)
  \phi_c
  = 0
  \mathrlap{\,.}
\]

## As effective theory of FQH edge modes

When the the FL theory is understood as an [[effective field theory]] for [[edge modes]] of [[fractional quantum Hall liquids]] ([Wen 1992 §2.5](#Wen1992), review in  [Tong 2016](#Tong2016) [p. 207](https://ncatlab.org/nlab/files/Tong-QuantumHallEffect.pdf#page=209)), it is the spatial derivative

\[
  \rho \coloneqq \partial_x \phi
\]

which represents the [[current density]] on the edge, and by (eq:TheEquationOfMotion) this again satisfies the chiral wave equation

\[
  \big(
    \partial_t - c \partial x
  \big)
  \rho
  = 0
  \mathrlap{\,.}
\]



## References

### General

The original article:

* {#FloreaniniJackiw1987} [[Roberto Floreanini]], [[Roman Jackiw]]: *Self-dual fields as charge-density solitons*, Phys. Rev. Lett. **59** (1987) 1873 &lbrack;[doi:10.1103/PhysRevLett.59.1873](https://doi.org/10.1103/PhysRevLett.59.1873)&rbrack;
  > (the FR-Lagrangian appears in equation (20))

A manifestly [[Lorentz group]]-[[invariant]] re-formulation:

* {#Townsend202} [[Paul K. Townsend]]: *Manifestly Lorentz invariant chiral boson action*, Phys. Rev. Lett. **124** (2020) 101604 \[<a href="https://doi.org/10.1103/PhysRevLett.124.101604">doi:10.1103/PhysRevLett.124.101604</a>, [arXiv:1912.04773](https://arxiv.org/abs/1912.04773)\]

### As EFT for FQH edge modes

Review as the [[boundary field theory]] of [[abelian Chern-Simons theory]], in the context of [[effective field theory]] for [[edge modes]] of [[fractional quantum Hall systems]]:

* {#Wen1992} [[Xiao-Gang Wen]]; §2.5 in: *Theory of Edge States in Fractional Quantum Hall Effects*, International Journal of Modern Physics B **06** 10 (1992) 1711-1762 &lbrack;[doi:10.1142/S0217979292000840](https://doi.org/10.1142/S0217979292000840), [[Wen-EdgeStatesEffective.pdf:file]]&rbrack;

* {#Wen1995} [[Xiao-Gang Wen]]; §3.3 in: *Topological order in rigid states and edge excitations in fractional quantum Hall states*, Advances in Physics **44** 5 (1995) 405-437 &lbrack;[arXiv:cond-mat/9506066](https://arxiv.org/abs/cond-mat/9506066), [doi;10.1080/00018739500101566](https://doi.org/10.1080/00018739500101566)&rbrack;

reviewed in:

* {#Tong2016} [[David Tong]]; §6.1.2 in: *The Quantum Hall Effect*, lecture notes (2016) &lbrack;[arXiv:1606.06687](https://arxiv.org/abs/1606.06687), [course webpage](https://www.damtp.cam.ac.uk/user/tong/qhe.html), [pdf](http://www.damtp.cam.ac.uk/user/tong/qhe/qhe.pdf), [[Tong-QuantumHallEffect.pdf:file]]&rbrack;


[[!redirects Floreanini-Jackiw Lagrangian]]

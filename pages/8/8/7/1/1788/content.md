> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak


***


\tableofcontents


## Idea of Topological Quantum Gates

The [[quantum adiabatic theorem]] entails:

\linebreak

Given a [[quantum system]] (e.g., a [[quantum material]])

depending on external parameters $p$ in a parameter space $P$

with a [[energy gap|gapped]] [[Hilbert space]] $\mathscr{H}_p$ of [[quantum state|quantum]] [[ground states]]

then sufficiently gentle ("adiabatic") tuning $\gamma$ of parameters

brings about unitary transformation $U_\gamma$ of the quantum state

$
  \begin{array}{ccc}
    \mathscr{H}_p &\overset{U_\gamma}{\longrightarrow}& \mathscr{H}_{p'}
    \\
    p &\overset{\gamma}{\rightsquigarrow}& p'
  \end{array}
$

\linebreak

This is called "*[[topological quantum computing|topological]]*" (really: "homotopical") if

$U_\gamma$ depends only on the [[homotopy class]] of $\gamma$ (rel. endpoints),

whence the $\mathscr{H}_p$ form a *[[local system]]* of [[Hilbert spaces]] over $P$,

which over each [[connected component]] $[\phi] \in \pi_0(P)$

is equivalently a [[unitary group|unitary]] [[linear representation|representation]] of the [[fundamental group]]

$
  U_{(-)}
  \,\colon\,
  \pi_1 \big(P, [\phi]\big)
  \longrightarrow
  \mathrm{U}(\mathscr{H})
$

\linebreak

Regarded as [[quantum gates]], these $U_\gamma$ are "topologically protected"  

in that they are undisturbed by noise in control parameter $\gamma$.

There are [arguments](/nlab/show/topological+quantum+computation#ReferencesNeedForTopologicalProtection) that some such topological protection 

is *necessary* for [[quantum computers]] to reach interesting scale.

\linebreak

Big question: How to find/build quantum systems with such

nontrivial (nonabelian) topological [[monodromy]] $U_{(-)}$

(jargon: "[[topological order]]") ??

\linebreak

Old idea: If one could arrange that 

$P \sim Conf(\mathbb{R}^2)$ 

is a [[configuration space of points]] in the plane, such as of

some kind of [[soliton]]/[[defect]] positions in a $\sim$2D material

then

$ Br(n) \simeq \pi_1(P, n) \longrightarrow U(\mathscr{H})  $

is a [[braid representation]] of a [[braid group]] on $n$ strands

if non-trivial, the [[solitons]]/[[defects]] are called "[[anyons]]"


\linebreak

It remains underappreciated that: $P$ could be different.

Let's have a closer look which $P$ actually arise in practice.

\linebreak

## Idea of Topological Phases of Matter

The [[Bloch theorem]] entails that:

\linebreak

The [[Hamiltonians]] $H$ of [[electrons]] in a [[crystal]] are [[direct integrals]]

$
 H 
   \;=\;
 \underset
  {{[k] \in \widehat{T}{}^d}}
  {\displaystyle{\int}}
 H_k
$

over the [[Brillouin torus]] $\widehat{T}{}^d$ of crystal momenta 

of [[Bloch Hamiltonians]], given by [[continuous maps]]

$
 H_{(-)}
  \;\colon\;
 \widehat{T}{}^d
 \longrightarrow
 Herm(\mathscr{H}_{Bl})
 \mathrlap{\,.}
$

Here $H_{[k]}$ encodes the energy states available to electrons

with a well-defined ([[plane wave]]) momentum $[k]$.

\linebreak

The [[graph]] of [[eigenvalues]] of $H_{(-)}$ are the [[energy bands]].

\linebreak

If all the $H_{[k]}$ are [[energy gap|gapped]], say at $E = 0$,

then the *[[valence bundle]]* is the negative [[eigenspace]] [[fiber bundle|bundle]] 

$
  \mathcal{V} 
  \,\coloneqq\,
  Eig_{\lt 0}\big(
    H_{(-)}
  \big)
  \longrightarrow
  \widehat{T}{}^d
$

\linebreak

The relevant [[equivalence class]] of the [[valence bundle]]

depends on how fine/coarse the resolution is. Given a choice

then the class $[\mathcal{V}]$ is the observed *[[topological phase of matter]]*.

\linebreak

For *[[fragile topological phases]]* one considers the system

exploring only the given space of gapped Bloch Hamiltonians

$
 \mathcal{B}\big(\mathbb{C}^{v+c}\big)
 \,\coloneqq\,
 \Bigg\{
 H \in Herm(\mathbb{C}^{v+c})
 \,\Bigg\vert\,
    \substack{
      Eig_{\lt 0}(H) \simeq \mathbb{C}^v
      \\
      Eig_{\gt 0}(H) \simeq \mathbb{C}^c 
    }
 \,
 \Bigg\}
 \sim
 Gr_{v}^{v+c}
 \,,
$

which is [[homotopy equivalence|homotopy equivalent]] to the [[Grassmannian]] 

$
 Gr_{v}^{v+c}
 \,\coloneqq\,
 \left\{
 \substack{
    v\;\text{dimensional linear}
    \\
    \text{subspaces of} \mathbb{C}^{v+c}
 }  
 \right\}
 \mathrlap{\,,}
$

whence the parameter space of fragile topological couplings is

the [[mapping space]] from the [[Brillouin torus]] to the [[Grassmannian]]

$
 P 
 \,\equiv\,
 Map\big(
  \widehat{T}{}^d
  ,\,
  Gr_{v}^{v+c}
 \big)
 \mathrlap{\,.}
$

\linebreak

Whereas the coarser *stable* topological phases classify the

deformation classes where the system is allowed to explore

1. any of the higher [[conduction bands]], where

   $
     \bigcup_{c \in \mathbb{N}}
     Gr_v^{v + c}
     \,\simeq\,
     B \mathrm{U}(v)
   $

2. moreover any number of [[valence bands]], where

   $
     \bigcup_{v \in \mathbb{N}}
     \bigcup_{c \in \mathbb{N}}
     Gr_v^{v + c}
     \,\simeq\,
     \bigcup_{v \in \mathbb{N}}
     B \mathrm{U}(v)
     \,\simeq\,
     B \mathrm{U}
   $



\linebreak

For $\left\{\begin{aligned}c & \to \infty \\v & = 1\end{aligned}\right.$ these phases are in [[ordinary cohomology]]:

$
  H^2\big(
    \widehat{T}{}^d
    ;\,
    \mathbb{Z}
  \big)
  \,\simeq\,
  \pi_0\, Map\big(
    \widehat{T}{}^d
    ,\,
    Gr_{1}^\infty
  \big)
  \mathrlap{\,,}
$

\linebreak

while for $\left\{\begin{aligned}c & \to \infty \\ v & \to \infty\end{aligned}\right.$ these phases are in ([[reduced K-theory|reduced]]) [[topological K-theory]]

$
  KU^0\big(
    \widehat{T}{}^d
  \big)
  \,\simeq\,
  \pi_0\, Map\big(
    \widehat{T}{}^d
    ,\,
    B \mathrm{U} {\color{gray} \times \mathbb{Z}}
  \big)
  \mathrlap{\,,}
$

\linebreak

but general fragile phases are in extraordinary *[[nonabelian cohomology]]*

classified by any (pointed connected) [[topological space]] $\mathcal{A}$:

$
  H^1\big(
    X
    ;\,
    \Omega \mathcal{A}
  \big)
  \,\coloneqq\,
  \pi_0\, Map\big(
    X
    ,\,
    \mathcal{A}
  \big)
$

here specifically:

$
  H^1\big(
    \widehat{T}{}^d
    ;\,
    \Omega Gr_{v}^c
  \big)
  \,\simeq\,
  \pi_0\, Map\big(
    \widehat{T}{}^d
    ,\,
    Gr_{v}^\infty
  \big)
  \mathrlap{\,.}
$


\linebreak

For example:

In the case of "2 accessible bands", $\mathscr{H}_{Bl} \simeq \mathbb{C}^2$,

where the classifying space  $ Gr_1^{2} \simeq \mathbb{C}P^2 \simeq S^2$ is the [[2-sphere]],

the fragile topological phases are classified in 2-*[[Cohomotopy]]*:

$
 pi^2(X)
 \,\equiv\,
 \pi_0\, Map\big(X, S^2\big)
 \mathrlap{\,.}
$


\linebreak

For 2D materials this coincides already with the stable phases

$
 \begin{array}{ccc}
   \pi^2\big(
     \widehat{T}{}^2
   \big)
   &
    \xrightarrow{\phantom{-}\sim\phantom{-}}
   &
   H^2\big(
     \widehat{T}{}^2
     ,\,
     \mathbb{Z}
   \big)
   & \simeq \mathbb{Z}
   \\
   = && =
   \\
   \pi_0 \, 
   Map\big(
    \widehat{T}{}^2
    ,\, 
    \mathbb{C}P^1
   \big)
   &\xrightarrow[\iota_\ast]{\phantom{-}\sim\phantom{-}}&
   \pi_0 \, 
   Map\big(
    \widehat{T}{}^2
    ,\, 
    \mathbb{C}P^\infty
   \big)
   \\
  S^2 \simeq Gr_1^2 
  &\xhookrightarrow{\phantom{--}}&
  Gr_1^{\infty} \simeq B \mathrm{U}(1)
 \end{array}
$

This integer class is the *[[Chern class]]* of the [[valence bundle|valence]] [[complex line bundle|line bundle]]

whence one speaks of [[topological insulator|topological]] *[[Chern insulators]]*.


\linebreak


## Fragile Crystalline Topological Phases

More precisely, in general a [[space group|crystalline symmetry]] $G \curvearrowright \widehat{T}{^2}$

is respected by the Bloch Hamiltonian and its deformations:

$
 \underset{[k] \in \widehat{T}{}^d}{\forall}
 \;\;\;\;\;\;
 H_{g \cdot [k]}
 \,=\,
 U_g
 \circ
 H_{[k]}
 \circ
 U_g^{-1}
$

for [[unitary operators]] $U_{(-)}$, in which case one speaks of 

"*[[symmetry protected topological phases]]*".

\linebreak

Observation: This means that the classifying maps are *[[equivariant maps]]*

$
  P 
  \;\equiv\;
  Map\big(\widehat{T}{}^d, Gr_{v}^{c+c}\big)^G
$

and the classification is in [[equivariant cohomology|equivariant]] [[nonabelian cohomology]]

$
 H^1_G\big(
  \widehat{T}{}^d
  ;\,
  \Omega
  Gr_{v}^{v+x}
 \big)
 \,\equiv\,
 \pi_0\,
 Map\big(\widehat{T}{}^d, Gr_{v}^{c+c}\big)^G
 \mathrlap{\,.}
$

\linebreak

In particular:

*Fragile crystalline 2-band phases are classified by [[equivariant Cohomotopy|equivariant 2-Cohomotopy]].*

Evident as this is, it has not been classified or even stated before.

\linebreak

While filling such gaps we also also point out that the topological

parameter space really ought to be the [[homotopy quotient]] 

$
 P
 \;=\;
 Map\big(
  \widehat{T}{}^2
  ,\,
  \mathcal{A}
 \big)^G
 {
 \color{purple}
 \sslash
 Diff\big(\widehat{T}{}^2\big)^G
 }
$

by the equivariant [[diffeomorphism group]] (acting by [[precomposition]])

as befits the [[modular functor]] of a [[topological field theory]].



\linebreak


## Identifying Anyons in FQAH Materials

Hence if there is [[topological order]]/[[anyons]]

in [[crystalline topological insulator|crystalline]] [[fractional quantum Hall systems]] it ought to be 

reflected in nontrivial parameter [[fundamental groups]] $\pi_1(P,[\phi])$,

in a given topological phase $[\phi] \in \pi_0(P)$

$
  \pi_1\big(
    P,\, [\phi]
  \big)
  \;\equiv\;
  \pi_1\Big(
    Map\big(
      \widehat{T}{}^2
      ,\,
      Gr_{1}^2
    \big)^G
    \sslash
    Diff\big(
     \widehat{T}{}^2
    \big)^G
    ,\,
    [\phi]
  \Big)
$

\linebreak

Two examples (1.) [[soliton|solitonic]] and (2.) [[defect]] anyons:

\linebreak

**Proposition 1** (potential solitonic FQAH anyons): 

When all symmetry is broken ($G = 1$ the [[trivial group]]):

$
  \pi_1\Big(
    Map\big(
      \widehat{T}{}^2
      ,\,
      S^2
    \big)
    \sslash
    Diff\big(
     \widehat{T}{}^2
    \big)
  \Big)
  \,\simeq\,
  \widehat{\mathbb{Z}^2}
  \rtimes
  Mod
  \mathrlap{\,,}
$

where $\widehat{\mathbb{Z}^2}$ is the [[integer Heisenberg group]] at level=2

$
  \widehat{\mathbb{Z}^2}
  \,=_{{}_{Set}}\,
  (\mathbb{Z}_a \times \mathbb{Z}_b)
  \times 
  \mathbb{Z}
$

with generators

$
  \left.
  \begin{aligned}
    W_a & \coloneqq \big((1,0),0\big)
    \\
    W_b & \coloneqq \big((0,1),0\big)
    \\
    \zeta & \coloneqq \big((0,0),1\big)
  \end{aligned}
  \right\}
  \,\in\, 
  (\mathbb{Z}_a \times \mathbb{Z}_b)
  \times 
  \mathbb{Z}
$

and the only nontrivial [[group commutator]] being

$
 [W_a, W_b] \,=\, \zeta^2
 \,.
$

\linebreak

This $\widehat{\mathbb{Z}^2}$ is precisely the relation characterizing [[fractional quantum Hall system|FQH anyons]] on the [[torus]]!

And $\widehat{\mathbb{Z}^2} \rtimes Mod$ imposes their expected modular data.

\linebreak

**Proposition 2** (potential defect FQAH anyons): 

For [p3](/nlab/show/wallpaper+group#TorusWithC3RotationAction) symmetry

$
  \pi_1\Big(
    Map\big(
      \widehat{T}{}^2
      ,\,
      S^2
    \big)^{\mathbb{Z}_{/3}}
    \sslash
    Diff\big(
     \widehat{T}{}^2
    \big)^{\mathbb{Z}_{/3}}
  \Big)
  \,\supset\,
  \mathbb{Z}^3 \rtimes Sym(3)
  \mathrlap{\,,}
$

where the [[symmetric group]] $Sym(3)$ acts by [[permutation]] of the high symmetry points.

\linebreak

This implies that the high symmetry points themselves

may constitute [[parastatistics|para-]] [[defect]] [[anyons]].

\linebreak

## Computing Equivariant 2-Cohomotopy

of $G$-tori is among the most basic questions 

not just for the physics of crystalline fragile topological phases

but also in pure [[Cohomotopy]] theory as such

but seems not to have found any attention before.

\linebreak

One approach: 

Determine minimal [[G-CW complex]]-structure on $G$-torus

for [[point group]]-symmetries $G$ of [[wallpaper groups]].

(Worked out [here](/nlab/show/wallpaper+group#EquivariantCellStructureOf2Tori).)

Observe that filtering the equivariant mapping space into $S^2$

by the skeleta of this [[G-CW complex]] gives homotopy fiber

realizations from which the homotopy groups may be deduced.





\linebreak

***

\linebreak

For [[5D Maxwell-Chern-Simons theory]] on a [[spacetime]] $X^{1,4}$

* the local [[field (physics)|field]] content is a 1-form [[gauge potential]] $A \in \Omega^1_{dR}(X^{1,4})$

* the [[Lagrangian density]] is:

  $$
    L 
    \;\coloneqq\;
    \tfrac{1}{2}\mathrm{d}A \wedge \star \mathrm{d}A
    \,-\,
    \tfrac{1}{6} A \wedge \mathrm{d}A \wedge \mathrm{d}A
    \mathrlap{\,,}
  $$

where $\star$ is the [[Hodge star operator]] for the [[pseudo-Riemannian metric]] on $X^{1,d}$.

The [[Euler-Lagrange equations]] [[equations of motion|of motion]] are

$$
  \left.
  \begin{aligned}
    \mathrm{d}\, F_2 & = 0
    \\
    \mathrm{d}\, G_3 & = \tfrac{1}{2} F_2 \wedge F_2
  \end{aligned}
  \right\}
  \,,
  \;\;
  \text{where}
  \;\;
  \left\{
  \begin{aligned}
    F_2 & \coloneqq \mathrm{d}A
    \\
    G_3 & \coloneqq \star F_2
    \,.
  \end{aligned}
  \right.
$$

While $G_3$ is not closed, the combination
$$
  \widetilde G_3 
  \,\coloneqq\,
  G_3 - \tfrac{1}{2} A \wedge F_2
$$
is closed:
$$
  \mathrm{d}\, \widetilde G_3
  \;=\;
  0
  \mathrlap{\,.}
$$

Considering now

* a [[globally hyperbolic spacetime]]

  $$
    X^{1,4} \simeq \mathbb{R}^{1,0} \times X^4
  $$

  with [[Cauchy surface]] 

  $$
    \iota \colon X^d \hookrightarrow X^{1,4}
    \mathllap{\,,}
  $$

* [[temporal gauge]]$\;$$A_0 = 0$

  whence we now understand $A \in \Omega^1_{dR}(X^4)$.

The [[canonical momentum]] to the [[gauge potential]] $A$ is

$$
  \widetilde E_3 
    \;\coloneqq\;
  \tfrac{\partial L}{\partial (\partial_0 A)}
    \;=\;
  \iota^\ast G_3 
    \,-\,
  \tfrac{1}{3} A \wedge B_2
  \,,
$$

whence the basic [[Poisson bracket]] is, for $\omega \in \Omega^1_{dR}(X^4)$, given by

$$
  \Big\{
    \textstyle{\int_{X^4}} \omega \wedge E
    ,\,
    A(x)
  \Big\}
  \;=\;
  \omega(x)
  \mathrlap{\,.}
$$

Setting 

$$
  \begin{aligned}
    B_2 
      & \coloneqq\, 
    \iota^\ast \mathrm{d}A
    \\
    E_3 
      & \coloneqq\, 
    \iota^\ast G_3
    \\
    & = 
    \widetilde E_3 + \tfrac{1}{3} A \wedge B_2 
  \end{aligned}
$$

we have Poisson brackets

$$
  \Big\{
    \textstyle{\int_{X^4}} \omega \wedge E_3
    ,\,
    \textstyle{\int_{X^4}} \omega' \wedge E_3
  \Big\}
  \;=\;
  \tfrac{4}{3}
  \int_{X^4} \omega \wedge \omega' \wedge B_2
  \mathrlap{\,,}
$$

Now say that the *topological observables* are these integrals for closed $\omega$ modulo exact.

Consider this on 

$$
  X^4
  =
  \mathbb{R}^1 \times [0,1] \times 
  T^2
$$

Then the space of topological observables is spanned by 

$\big(O^{(a)}_1, O_1^{(b)}, O_2\big)$ with the only non-trivial Poisson bracket being
$$
  \big\{ O^{(a)}_1,  O^{(b)}_1 \big\} = \tfrac{4}{3}O_2  
$$

\linebreak

Alternatively, consider the Pontrjagin algebra

$$
  H_0\big(
    \Omega\, Map\big(T^2, S^2\big)
  \big)
  \;\simeq\;
  \big(
    U\mathfrak{l}Map(T^2, S^2)
  \big)_0
  \mathrlap{\,,}
$$

which is the universal enveloping algebra of the $\mathbb{C}$-Whitehead bracket Lie algebra, in degree=0, of the mapping space. 

Here
$$
  \mathfrak{l}Map(T^2, S^2)
  \;\simeq\;
  tor^2 \mathfrak{l}S^2
$$

and the degree=0 elements in here are spanned by

$$
  \overset{1}{s} v_1
  ,\,
  \overset{2}{s} v_1
  ,\,
  \overset{1}{s} \overset{2}{s} v_2
$$

with the only non-trivial bracket being
$$
  \big[
    \overset{1}{s} v_1
    ,\,
    \overset{2}{s} v_1
  \big]
  \;=\;
  \overset{1}{s} \overset{2}{s} v_2
$$






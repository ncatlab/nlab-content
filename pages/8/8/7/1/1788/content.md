> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).


\linebreak


***


## Idea of topological quantum gates

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

which over each [[connected component]] $c \in \pi_0 P$

is equivalently a [[unitary group|unitary]] [[linear representation|representation]] of the [[fundamental group]]

$
  U_{(-)}
  \,\colon\,
  \pi_1 (P, c)
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

But $P$ could be different.

Let's have a closer look which $P$ actually arise in practice.

\linebreak

## Idea of topological phases of matter

The [[Bloch theorem]] entails that 

the [[Hamiltonians]] $H$ of [[electrons]] in a [[crystal]] are [[direct integrals]]

$
 H 
   \;=\;
 \underset
  {{[k] \in \widehat{T}^d}}
  {\displaystyle{\int}}
 H_k
$

over the [[Brillouin torus]] $\widehat{T}^d$ of crystal momenta 

of [[Bloch Hamiltonians]], given by [[continuous maps]]

$
 H_{(-)}
  \;\colon\;
 \widehat{T}^d
 \longrightarrow
 Herm(\mathscr{H}_{Bl})
$

\linebreak

The [[graph]] of [[eigenvalues]] of $H_{(-)}$ are the [[energy bands]].

\linebreak

If all the $H_{[k]}$ are [[energy gap|gapped]] at, say $E = 0$,

then the *[[valence bundle]]* is the negative [[eigenspace]] [[fiber bundle|bundle]] 

$
  \mathcal{V} 
  \,\coloneqq\,
  Eig_{\lt 0}\big(
    H_{(-)}
  \big)
  \longrightarrow
  \widehat{T}^d
$

\linebreak

The relevant [[equivalence class]] of the [[valence bundle]]

depends on how fine/coarse this description is. Given a choice

then the class $[\mathcal{V}]$ is the observed [[topological phase of matter]].

\linebreak

For *[[fragile topological phases]]* one considers

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
$

whence the parameter space of fragile topological couplings is

the [[mapping space]] from the [[Brillouin torus]] to the [[Grassmannian]]

$
 P 
 \,\equiv\,
 Map\big(
  \widehat{T}
  ,\,
  Gr_{v}^{v+c}
 \big)
$


Consider "2 accessible bands", $\mathscr{H}_{Bl} \simeq \mathbb{C}^2$,

then the space of gapped Bloch Hamiltonians is




## Idea of Crystalline Phases


## Equivariant 2-Cohomotopy





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






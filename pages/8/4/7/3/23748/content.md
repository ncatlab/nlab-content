+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--



\tableofcontents


## Idea

In [[quantum physics]], the *quantum adiabatic theorem* for a [[parameterized quantum system]] says the following. Under a sufficiently slow motion of the external parameters along a [[path]] $\gamma \,\colon\, [0,1] \to X$ in *parameter space* $X$, [[eigenstates]] of the [[Hamiltonian]] at $\gamma(0)$ approximately evolve into eigenstates at $\gamma(1)$, even if the corresponding [[eigenvalues]] change significantly. More generally, this holds for states in any part of the [[spectrum of an operator|spectrum]] which stays separated from the rest of the spectrum by a gap. 

For adiabatic transport along a [[loop]], $\gamma(0) = \gamma(1)$, this implies that the [[eigenspaces]] of the system are acted on by [[unitary operators]]. These are the [[holonomy|holonomies]] of the *[[Berry connection]]*, known as *[[Berry phases]]* in the case of eigen-dimension 1, and as *non-abelian Berry phases* in the case of degenerate eigenspaces (see [below](#ForGappedGroundStates)).

{#AsAModelForQuantumComputation} The adiabatic parameter-action on [[ground states]] of ([[topological order|topologically ordered]]) [[quantum materials]] is one model for [[quantum computation]]: see at *[[holonomic quantum computation]]* and *[[adiabatic quantum computation]]*. If these adiabatic [[quantum gates]] depend only on the [[isotopy]] [[equivalence class|class]] of the parameter path, then one speaks of *[[topological quantum computation]]*. This is made explicit in [Arovas, Schrieffer & Wilczek 1984](#ArovasSchriefferWilczek84), [Freedman, Kitaev, Larsen & Wang 2003, p. 7](#FreedmanKitaevLarsenWang03) and [Nayak, Simon, Stern, Freedman & Das Sarma 2008, §II.A.2 (p. 6)](#NayakSimonSternFreedman08); see also at *[braiding of anyonic defects](braid+group+statistics#AsBraidingOfDefects)* and [below](#OutlookAdiabaticQuantumGates).

The following graphic is meant to illustrate this general idea for the case of adiabatic transformation along the [[braid group|braiding]] of nodal points in the [[Brillouin torus]] of [[semi-metal]] [[quantum materials]] (see the discussion at *[[braid group statistics]] -- [anyonic band nodes](braid+group+statistics#AnyonicBandNodes)*):

\begin{imagefromfile}
    "file_name": "AdiabaticBraidingOfBandNodes-220604.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


> (graphics from [[schreiber:Topological Quantum Computation in TED-K|SS22]])


## Statement


### Preliminaries
 {#Preliminaries}

Throughout, $\mathcal{H}$ denotes a [[complex Hilbert space]], $\mathcal{B}(\mathcal{H})$ its [[algebra]] of [[bounded operators]] equipped with the [[operator norm]] $\Vert - \Vert$, and we use [[physical unit|units]] with $\hbar = 1$.

#### Adiabatic time evolution
 {#AdiabaticTimeEvolution}

+-- {: .num_defn #PathOfHamiltonians}
###### Definition
**(path of Hamiltonians)**

A *path of [[Hamiltonians]]* is a function
$$
  \begin{array}{ccc}
    [0,1] &\longrightarrow& \mathcal{B}(\mathcal{H})
    \\
    s &\mapsto& H(s)
  \end{array}
$$
to [[self-adjoint operators]], which is twice continuously [[differentiable function|differentiable]] in the [[operator norm]].

=--

+-- {: .num_remark #OnPathsOfHamiltonians}
###### Remark
**(on paths of Hamiltonians)**

1. Typically such a path arises from a *[[parameterized quantum system]]*, namely from a family of Hamiltonians 
   $$
     \begin{array}{ccc}
       X &\longrightarrow& \mathcal{B}(\mathcal{H})
       \\
       x &\mapsto& \hat H(x)
     \end{array}
   $$
   over a [[smooth manifold]] $X$ of external parameters, by restriction along a smooth [[path]] $\gamma \colon [0,1] \to X$ in parameter space:
   $$
     H(s) \;\coloneqq\; \hat H\big(\gamma(s)\big)
     \,.
   $$

1. The restriction to [[bounded operators]] is for simplicity of exposition. Everything below generalizes to [[unbounded operator|unbounded]] Hamiltonians which are bounded below and have a common [[domain]] $D$, such that $s \mapsto H(s)$ is $C^2$ as a function to bounded operators from $D$, equipped with the [[graph norm]] of $H(0)$, to $\mathcal{H}$ ([Avron, Seiler & Yaffe 1987, §2](#AvronSeilerYaffe87), [Teufel 2003](#Teufel03)).

1. The $C^2$-assumption is convenient but stronger than necessary: [Kato 1950](#Kato50) only assumes that the first and second derivatives of the spectral projections (Def. \ref{SpectralProjection} below) are piecewise continuous.

=--

Running through such a path in physical [[time]] $t \in [0,\tau]$ means that the system evolves under the time-dependent Hamiltonian $t \mapsto H(t/\tau)$. In terms of the rescaled time parameter $s \coloneqq t/\tau \in [0,1]$, the [[Schrödinger equation]] then reads as follows:

+-- {: .num_defn #AdiabaticSchroedingerEquation}
###### Definition
**(actual time evolution)**

For $\tau \in (0,\infty)$ write
$$
  \varepsilon \;\coloneqq\; 1/\tau
$$
(the *adiabatic parameter*), and let 
$$
  \begin{array}{ccc}
    [0,1] &\longrightarrow& \mathcal{B}(\mathcal{H})
    \\
    s &\mapsto& U_\varepsilon(s)
  \end{array}
$$
be the [[solution]] of
$$
  \mathrm{i}\, \varepsilon \, \partial_s U_\varepsilon(s)
  \;=\;
  H(s)\, U_\varepsilon(s)
  \,,
  \;\;\;\;\;
  U_\varepsilon(0) \;=\; \mathrm{id}_{\mathcal{H}}
  \,.
$$
This exists, is unique, and is [[unitary operator|unitary]] for all $s$, being given by the [[time-ordered exponential]] of $-\tfrac{\mathrm{i}}{\varepsilon}\int H$. (It is called the *dynamical transformation* in [Kato 1950, §2](#Kato50).)

=--

The *adiabatic limit* is the limit $\varepsilon \to 0$, i.e. $\tau \to \infty$, in which the path of Hamiltonians is traversed infinitely slowly. In the rescaled time $s$ the dynamics becomes *fast* in this limit. For instance, if $H(s) = H$ is constant and $H \psi = E \psi$, then $U_\varepsilon(s)\psi = e^{-\mathrm{i} E s/\varepsilon} \psi$.


#### Gap condition and spectral projections
 {#GapConditionAndSpectralProjections}

+-- {: .num_defn #GapCondition}
###### Definition
**(gap condition)**

A path of Hamiltonians (Def. \ref{PathOfHamiltonians}) satisfies the *gap condition* if, for all $s \in [0,1]$, the [[spectrum of an operator|spectrum]] of $H(s)$ decomposes into two [[disjoint subset|disjoint]] non-empty [[closed subsets]]
$$
  \sigma\big(H(s)\big)
  \;=\;
  \sigma_\ast(s) \,\sqcup\, \sigma_\perp(s)
$$
such that

1. there is a [[contour]] $\Gamma(s) \subset \mathbb{C}$ encircling $\sigma_\ast(s)$ but not $\sigma_\perp(s)$, which may be chosen to depend continuously on $s$,

1. the *gap* between the two parts is bounded below uniformly in $s$:
   $$
     g 
     \;\coloneqq\; 
     \inf_{s \in [0,1]}
     \mathrm{dist}\big( \sigma_\ast(s),\, \sigma_\perp(s) \big)
     \;\gt\;
     0
     \,.
   $$

We speak of *gapped [[ground states]]* if $\sigma_\ast(s)$ is the bottom part of the spectrum: $\sup \sigma_\ast(s) \lt \inf \sigma_\perp(s)$.

In the special case that $\sigma_\ast(s) = \{\lambda(s)\}$ is a single [[eigenvalue]], we say that the selected eigenstates are *exactly degenerate*, where the degeneracy may be 1. This is the case considered in [Kato 1950](#Kato50).

=--

+-- {: .num_defn #SpectralProjection}
###### Definition
**(spectral projection)**

Given a path satisfying the gap condition (Def. \ref{GapCondition}), the *spectral projections* onto $\sigma_\ast(s)$ are given by the [[Riesz formula]]
$$
  P(s)
  \;\coloneqq\;
  \frac{1}{2\pi\mathrm{i}}
  \oint_{\Gamma(s)}
  \big( z - H(s) \big)^{-1}
  \, \mathrm{d}z
  \,.
$$
We write
$$
  \mathcal{H}_\ast(s) 
  \;\coloneqq\;
  \mathrm{im}\big(P(s)\big)
  \;\subset\;
  \mathcal{H}
$$
for their [[image]] spaces, which in the case of gapped ground states are the spaces of (quasi-)[[ground states]].

=--

+-- {: .num_prop #PropertiesOfSpectralProjections}
###### Proposition
**(properties of the spectral projections)**

The spectral projections $P(s)$ (Def. \ref{SpectralProjection}) satisfy:

1. Each $P(s)$ is an [[orthogonal projection]] which [[commutator|commutes]] with $H(s)$.

1. The function $s \mapsto P(s)$ is $C^2$ in the [[operator norm]].

1. The [[dimension]] of $\mathcal{H}_\ast(s)$ is independent of $s$ (possibly infinite).

1. The [[derivative]] $P' \coloneqq \partial_s P$ is *off-diagonal* with respect to the decomposition $\mathcal{H} = \mathcal{H}_\ast(s) \oplus \mathcal{H}_\ast(s)^\perp$, in that
   $$
     P \, P' \, P \;=\; 0
     \,,
     \;\;\;\;\;
     P' \;=\; P' P + P P'
     \,,
   $$
   and hence
   $$
     P' \;=\; \big[ [P', P],\, P \big]
     \,.
   $$

=--

+-- {: .proof}
###### Proof

The first statement is standard [[functional calculus]] (see at *[[Riesz formula]]*). The second follows since the [[resolvent]] $(z - H(s))^{-1}$ is $C^2$ in $s$, locally uniformly for $z$ on the contour. The third follows from the general fact that projections at operator-norm distance $\Vert P(s) - P(s') \Vert \lt 1$ are [[unitary operator|unitarily]] equivalent, together with [[continuous function|continuity]] of $P$ and [[connected topological space|connectedness]] of $[0,1]$. For the last statement, differentiate $P^2 = P$ to get $P' P + P P' = P'$, and then multiply this from both sides by $P$ to get $2 P P' P = P P' P$. With this, $\big[[P',P],P\big] = P'P - 2 P P' P + P P' = P'$. (These are equations (17) and (19) in [Kato 1950](#Kato50), and (2.5) in [Avron, Seiler & Yaffe 1987](#AvronSeilerYaffe87).)

=--


#### Kato's parallel transport
 {#KatoParallelTransport}

+-- {: .num_defn #KatoTransport}
###### Definition
**(Kato's parallel transport)**

Given a $C^1$ path $s \mapsto P(s)$ of orthogonal projections, its *Kato transport*, called the *adiabatic transformation* in [Kato 1950, §3](#Kato50), is the solution 
$$
  \begin{array}{ccc}
    [0,1] &\longrightarrow& \mathcal{B}(\mathcal{H})
    \\
    s &\mapsto& K(s)
  \end{array}
$$
of
$$
  \partial_s K(s) 
  \;=\; 
  \big[ P'(s),\, P(s) \big] \, K(s)
  \,,
  \;\;\;\;\;
  K(0) \;=\; \mathrm{id}_{\mathcal{H}}
  \,.
$$

=--

+-- {: .num_prop #KatoTransportIsUnitaryAndIntertwining}
###### Proposition
**(Kato transport is unitary and intertwining)**

The Kato transport $K(s)$ (Def. \ref{KatoTransport}) is [[unitary operator|unitary]] for all $s$, and it intertwines the projections:
$$
  K(s)\, P(0) 
  \;=\; 
  P(s)\, K(s)
  \,.
$$
Hence it restricts to unitary [[isomorphisms]]
$$
  K(s)\vert_{\mathcal{H}_\ast(0)}
  \;\colon\;
  \mathcal{H}_\ast(0)
  \xrightarrow{\;\;\sim\;\;}
  \mathcal{H}_\ast(s)
  \,,
$$
and similarly between the [[orthogonal complements]] $\mathcal{H}_\ast(0)^\perp \xrightarrow{\sim} \mathcal{H}_\ast(s)^\perp$.

=--

+-- {: .proof}
###### Proof

The generator $[P', P]$ is anti-[[self-adjoint operator|self-adjoint]], since $[P',P]^\dagger = [P, P'] = -[P', P]$, so that $K(s)$ is unitary. For the intertwining property, consider $Q(s) \coloneqq K(s)^\dagger P(s) K(s)$. Then
$$
  Q'
  \;=\;
  K^\dagger 
  \Big(
    P' - \big[ [P',P], P \big]
  \Big) 
  K
  \;=\;
  0
$$
by Prop. \ref{PropertiesOfSpectralProjections}, so that $Q(s) = Q(0) = P(0)$. Kato's original argument instead observes that $P(s) K(s)$ satisfies the same differential equation as $K(s)$, and hence coincides with $K(s)P(0)$ ([Kato 1950, (20-22)](#Kato50)). The statement about the orthogonal complements follows since $[P',P] = \big[(1-P)', 1-P\big]$, so that $K$ is also the Kato transport of $1 - P$.

=--

+-- {: .num_remark #KatoTransportAsParallelTransport}
###### Remark
**(Kato transport as parallel transport of the Berry connection)**

For $\psi_0 \in \mathcal{H}_\ast(0)$, the transported vectors $\psi(s) \coloneqq K(s)\psi_0 \in \mathcal{H}_\ast(s)$ satisfy (using Prop. \ref{PropertiesOfSpectralProjections})
$$
  P(s)\, \psi'(s) \;=\; 0
  \,.
$$
This says that they are *covariantly constant* with respect to the [[connection on a bundle|connection]] $\nabla \coloneqq P \circ \mathrm{d}$ on the [[vector bundle]] whose [[fibers]] are the spaces $\mathcal{H}_\ast$. This is the [[sub-bundle]] of the [[trivial bundle]] with fiber $\mathcal{H}$ cut out by the projections $P$. Therefore the Kato transport is the [[parallel transport]] of this connection, which is known as the *[[Berry connection]]*:

* If $\hat H$ is a family of Hamiltonians over parameter space $X$ (Rem. \ref{OnPathsOfHamiltonians}) satisfying the gap condition at every point, then the spaces $\mathcal{H}_\ast\big(\hat H(x)\big)$ form a vector bundle $\mathcal{E} \to X$ with connection $\nabla = P \circ \mathrm{d}$. Kato transport along a [[loop]] $\gamma$ in $X$ is the [[holonomy]] 
  $$
    \mathrm{hol}_\nabla(\gamma) 
    \;\in\; 
    \mathrm{U}\big(\mathcal{E}_{\gamma(0)}\big)
  $$
  of this connection. It depends on the loop, not just on its base point. In general it also depends on more than the [[homotopy]] class of the loop.

* In terms of a local [[orthonormal basis|orthonormal frame]] $(\psi_a)_a$ of $\mathcal{E}$, the [[connection form]] has components
  $$
    A_{a b} 
    \;=\; 
    \mathrm{i}\, {\langle \psi_a \vert \mathrm{d} \psi_b \rangle}
    \,.
  $$
  This is the *non-abelian Berry connection* ([Wilczek & Zee 1984](#WilczekZee84)). In the case of rank 1, it is the original Berry connection $A = \mathrm{i}\langle \psi \vert \mathrm{d}\psi \rangle$ ([Simon 1983](#Simon83), [Berry 1984](#Berry84)), whose holonomy along a loop is multiplication by the *[[Berry phase]]* $\exp\big(\mathrm{i}\oint_\gamma A\big) \in \mathrm{U}(1)$.

=--

+-- {: .num_remark #KatoTransportForSeveralProjections}
###### Remark
**(transport of several spectral subspaces)**

More generally, for a family of mutually orthogonal projections $P_n(s)$ with $\sum_n P_n(s) = 1$, the solution of
$$
  \partial_s K(s) 
  \;=\; 
  \tfrac{1}{2} \textstyle{\sum_n} \big[ P_n'(s),\, P_n(s) \big] \, K(s)
  \,,
  \;\;\;\;\;
  K(0) = \mathrm{id}_{\mathcal{H}}
$$
is unitary and intertwines all of these projections simultaneously, $K(s) P_n(0) = P_n(s) K(s)$ ([Kato 1950, §5](#Kato50)). For two projections $P_1 = P$ and $P_2 = 1-P$ this reduces to Def. \ref{KatoTransport}.

=--



### General
 {#GeneralStatement}

The adiabatic theorem says that the actual dynamics follows the spectral subspaces $\mathcal{H}_\ast(s)$ bordered by gaps. To make this precise, one compares the actual time evolution $U_\varepsilon$ (Def. \ref{AdiabaticSchroedingerEquation}) with a modified evolution which preserves these spectral subspaces *exactly*:

+-- {: .num_defn #AdiabaticEvolution}
###### Definition
**(adiabatic evolution)**

Given a path of Hamiltonians satisfying the gap condition (Def. \ref{GapCondition}), its *adiabatic evolution* ([Avron, Seiler & Yaffe 1987, (1.0)](#AvronSeilerYaffe87), following [Kato 1950](#Kato50)) is the solution
$$
  \begin{array}{ccc}
    [0,1] &\longrightarrow& \mathcal{B}(\mathcal{H})
    \\
    s &\mapsto& U^A_\varepsilon(s)
  \end{array}
$$
of
$$
  \mathrm{i}\, \varepsilon \, \partial_s U^A_\varepsilon(s)
  \;=\;
  \Big(
    H(s) 
    + 
    \mathrm{i}\,\varepsilon \big[ P'(s),\, P(s) \big]
  \Big)
  \, U^A_\varepsilon(s)
  \,,
  \;\;\;\;\;
  U^A_\varepsilon(0) \;=\; \mathrm{id}_{\mathcal{H}}
  \,.
$$

=--

The correction term $\mathrm{i}\varepsilon[P',P]$ is the generator of Kato's parallel transport (Def. \ref{KatoTransport}), rescaled to the time parameter of the Schrödinger equation. It is the unique correction to $H$ which makes the evolution decouple $\mathcal{H}_\ast$ from its complement while approximating the actual evolution as well as possible ([Avron, Seiler & Yaffe 1987, §1](#AvronSeilerYaffe87)). Accordingly, the adiabatic evolution splits into a geometric and a dynamical part:

+-- {: .num_prop #StructureOfAdiabaticEvolution}
###### Proposition
**(structure of the adiabatic evolution)**

The adiabatic evolution (Def. \ref{AdiabaticEvolution}) factors as
$$
  U^A_\varepsilon(s)
  \;=\;
  K(s) \, D_\varepsilon(s)
  \,.
$$
Here $K(s)$ is the Kato transport of $P(s)$ (Def. \ref{KatoTransport}), and $D_\varepsilon(s)$ is the solution of
$$
  \mathrm{i}\,\varepsilon\, \partial_s D_\varepsilon(s)
  \;=\;
  \big(
    K(s)^\dagger H(s) K(s)
  \big)
  \, D_\varepsilon(s)
  \,,
  \;\;\;\;\;
  D_\varepsilon(0) \;=\; \mathrm{id}_{\mathcal{H}}
  \,,
$$
which is unitary and [[commutator|commutes]] with $P(0)$. Consequently, $U^A_\varepsilon(s)$ is unitary and exactly intertwines the spectral projections:
$$
  U^A_\varepsilon(s) \, P(0)
  \;=\;
  P(s) \, U^A_\varepsilon(s)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using $\partial_s K = [P',P] K$, we have
$$
  \mathrm{i}\varepsilon\, \partial_s \big( K D_\varepsilon \big)
  \;=\;
  \mathrm{i}\varepsilon [P',P] K D_\varepsilon
  +
  K \big( K^\dagger H K \big) D_\varepsilon
  \;=\;
  \big( H + \mathrm{i}\varepsilon[P',P] \big) K D_\varepsilon
  \,,
$$
which gives the factorization, by uniqueness of solutions. The generator $K^\dagger H K$ of $D_\varepsilon$ is self-adjoint, so that $D_\varepsilon$ is unitary. It commutes with $P(0)$, since by Prop. \ref{KatoTransportIsUnitaryAndIntertwining} and Prop. \ref{PropertiesOfSpectralProjections} we have
$$
  K^\dagger H K \, P(0)
  \;=\;
  K^\dagger H P K
  \;=\;
  K^\dagger P H K
  \;=\;
  P(0)\, K^\dagger H K
  \,.
$$
Hence $D_\varepsilon(s)$ commutes with $P(0)$, and the intertwining property of $U^A_\varepsilon$ follows from that of $K$. (For a direct proof of the intertwining property see [Avron, Seiler & Yaffe 1987, Lem. 2.3](#AvronSeilerYaffe87).)

=--

In words: The adiabatic evolution moves the spectral subspace $\mathcal{H}_\ast(0)$ onto $\mathcal{H}_\ast(s)$ by Kato's unitary parallel transport $K(s)$, while inside the spectral subspace it runs the actual dynamics $D_\varepsilon$. The adiabatic theorem says that this correctly describes the actual dynamics up to errors of order $\varepsilon = 1/\tau$:

+-- {: .num_theorem #AdiabaticTheorem}
###### Theorem
**(quantum adiabatic theorem)**

Given a path of Hamiltonians (Def. \ref{PathOfHamiltonians}) satisfying the gap condition (Def. \ref{GapCondition}), there is a constant $C \in (0,\infty)$, depending on the path but not on $\varepsilon$, such that for all $\varepsilon \gt 0$:
$$
  \sup_{s \in [0,1]}
  \big\Vert
    U_\varepsilon(s) - U^A_\varepsilon(s)
  \big\Vert
  \;\leq\;
  C \, \varepsilon
  \,.
$$
In particular, transitions out of the spectral subspace are suppressed:
$$
  \sup_{s \in [0,1]}
  \big\Vert
    \big( 1 - P(s) \big) \, U_\varepsilon(s) \, P(0)
  \big\Vert
  \;\leq\;
  C \, \varepsilon
  \,.
$$

=--

This is due to [Kato 1950, (29)](#Kato50) for the case of an exactly degenerate eigenvalue of finite multiplicity (Def. \ref{GapCondition}). In the above generality it is due to [Nenciu 1980](#Nenciu80), [1981](#Nenciu81) for bounded Hamiltonians, and [Avron, Seiler & Yaffe 1987, Thm. 2.4](#AvronSeilerYaffe87) for unbounded Hamiltonians. A textbook account is in [Teufel 2003](#Teufel03).

+-- {: .proof}
###### Proof
(sketch)

The key observation is that the off-diagonal operator $[P',P]$ is a [[commutator]] with $H$. Namely, with the [[resolvent]] $R(z) \coloneqq (z - H)^{-1}$, the operator
$$
  Y(s)
  \;\coloneqq\;
  -\frac{1}{2\pi \mathrm{i}}
  \oint_{\Gamma(s)}
  R(z) \, P'(s) \, R(z)
  \, \mathrm{d}z
$$
satisfies
$$
  \big[ H(s),\, Y(s) \big] 
  \;=\; 
  \big[ P'(s),\, P(s) \big]
  \,.
$$
This follows from the identity $H R(z) = R(z) H = z R(z) - 1$, which gives $[H, R X R] = R X - X R$ for any $X$, together with the [[Riesz formula]] for $P$. Moreover, $Y$ is $C^1$ in $s$, since $H$ is $C^2$.

Now consider the [[wave operator]] $\Omega(s) \coloneqq U^A_\varepsilon(s)^\dagger \, U_\varepsilon(s)$, so that $\Vert U_\varepsilon(s) - U^A_\varepsilon(s) \Vert = \Vert \Omega(s) - 1 \Vert$. The two differential equations give
$$
  \Omega'
  \;=\;
  - U^{A \dagger}_\varepsilon \, [P', P] \, U_\varepsilon
  \;=\;
  - U^{A \dagger}_\varepsilon \, [H, Y] \, U_\varepsilon
  \,.
$$
This is of order 1, but it oscillates fast and may be integrated by parts:
$$
  U^{A \dagger}_\varepsilon \, [H, Y] \, U_\varepsilon
  \;=\;
  - \mathrm{i}\varepsilon \,
  \partial_s
  \big(
    U^{A \dagger}_\varepsilon \, Y \, U_\varepsilon
  \big)
  +
  \mathrm{i}\varepsilon \,
  U^{A \dagger}_\varepsilon 
  \big( Y' - [P',P]\,Y \big) 
  U_\varepsilon
  \,.
$$
Integrating, and using unitarity of $U_\varepsilon$ and $U^A_\varepsilon$, yields
$$
  \big\Vert \Omega(s) - 1 \big\Vert
  \;\leq\;
  \varepsilon
  \Big(
    \Vert Y(0) \Vert 
    + 
    \Vert Y(s) \Vert
    +
    \textstyle{\int_0^s}
    \big(
      \Vert Y' \Vert + \Vert P' \Vert \, \Vert Y \Vert
    \big)
  \Big)
  \,.
$$
For the second statement, observe that $(1-P(s))\, U^A_\varepsilon(s)\, P(0) = 0$, by Prop. \ref{StructureOfAdiabaticEvolution}.

This is the argument of [Avron, Seiler & Yaffe 1987, §2](#AvronSeilerYaffe87) (wave operator (2.6), integration by parts Lemma 2.5), which in turn generalizes that of [Kato 1950, §4](#Kato50).

=--

+-- {: .num_remark #OnTheAdiabaticTheorem}
###### Remark
**(on the adiabatic theorem)**

1. **(size of the constant)** By the above proof, the constant $C$ in Theorem \ref{AdiabaticTheorem} is controlled by $\Vert Y \Vert$ and $\Vert Y' \Vert$. Roughly, it scales like
   $$
     \frac{\Vert H' \Vert}{g^2}
     \,,
     \;\;
     \frac{\Vert H'' \Vert}{g^2}
     \,,
     \;\;
     \frac{\Vert H' \Vert^2}{g^3}
     \,,
   $$
   so that the adiabatic regime is $\tau \gg \Vert H' \Vert / g^2$, etc. Explicit bounds of this form are given in [Jansen, Ruskai & Seiler 2007](#JansenRuskaiSeiler07).

1. **(higher order and exponential accuracy)** The error of order $\varepsilon$ comes from the boundary terms in the integration by parts. If $s \mapsto H(s)$ is smooth and constant near the endpoints of the path, then repeated integration by parts shows that the transitions $(1-P(1))\, U_\varepsilon(1)\, P(0)$ out of the spectral subspace at the end of the path are of order $\varepsilon^n$ for all $n$ ([Avron, Seiler & Yaffe 1987, Cor. 2.6](#AvronSeilerYaffe87)). Under suitable analyticity assumptions they are even exponentially small in $1/\varepsilon$ ([Nenciu 1993](#Nenciu93), [Hagedorn & Joye 2002](#HagedornJoye02), [Teufel 2003](#Teufel03)).

1. **(level crossings and gapless cases)** If $\sigma_\ast(s)$ touches the rest of the spectrum at finitely many points $s$, then the conclusion of Theorem \ref{AdiabaticTheorem} still holds, but with $o(1)$ in place of $O(\varepsilon)$ ([Kato 1950, §4](#Kato50)). There are versions of the adiabatic theorem without any gap condition, again without an error rate in general ([Avron & Elgart 1999](#AvronElgart99)).

1. **(on the hypotheses)** The theorem concerns a *fixed* path, traversed ever more slowly. Heuristic "adiabaticity conditions" formulated only in terms of instantaneous matrix elements may fail ([Marzlin & Sanders 2004](#MarzlinSanders04), [Amin 2009](#Amin09)).

1. **(many-body systems)** For quantum lattice systems, $\Vert H' \Vert$ grows with the [[volume]], so that the above bounds become useless in the [[thermodynamic limit]]. There are versions of the adiabatic theorem with error bounds uniform in the system size, for local observables and assuming a uniform gap ([Bachmann, De Roeck & Fraas 2017](#BachmannDeRoeckFraas17), [2018](#BachmannDeRoeckFraas18), [Monaco & Teufel 2019](#MonacoTeufel19), [Henheik & Teufel 2022](#HenheikTeufel22)). A related approach is the *quasi-adiabatic continuation* of [Hastings & Wen 2005](#HastingsWen05) (see also [Bachmann, Michalakis, Nachtergaele & Sims 2012](#BMNS12)). It provides *quasi-local* unitaries which map ground states along gapped paths onto each other, whereas the generator $[P',P]$ of Kato's transport is in general not quasi-local.

=--



### For gapped ground states
 {#ForGappedGroundStates}

We now specialize to the case of gapped [[ground states]] (Def. \ref{GapCondition}). Here the dynamical part $D_\varepsilon$ of the adiabatic evolution (Prop. \ref{StructureOfAdiabaticEvolution}) becomes trivial up to a global phase. Hence the adiabatic theorem says that slow motion of parameters acts on ground states by the unitary parallel transport of the [[Berry connection]].

#### Exactly degenerate ground states
 {#ExactlyDegenerateGroundStates}

Assume first that the ground states are exactly degenerate, so that $\sigma_\ast(s) = \{E_0(s)\}$ is a single eigenvalue and
$$
  \mathcal{H}_0(s)
  \;\coloneqq\;
  \mathcal{H}_\ast(s)
  \;=\;
  \mathrm{ker}\big( H(s) - E_0(s) \big)
$$
is the ground state space.

+-- {: .num_prop #AdiabaticEvolutionOfDegenerateGroundStates}
###### Proposition
**(adiabatic evolution of degenerate ground states)**

In this case the adiabatic evolution (Def. \ref{AdiabaticEvolution}) on ground states is
$$
  U^A_\varepsilon(s) \, P(0)
  \;=\;
  e^{- \tfrac{\mathrm{i}}{\varepsilon} \int_0^s E_0(u) \, \mathrm{d}u}
  \,
  K(s) \, P(0)
  \,.
$$

=--

+-- {: .proof}
###### Proof

On $\mathcal{H}_0(0)$, the generator of $D_\varepsilon$ is $K^\dagger H K P(0) = K^\dagger H P K = E_0 \, P(0)$, by Prop. \ref{KatoTransportIsUnitaryAndIntertwining}. So $D_\varepsilon(s)$ acts on $\mathcal{H}_0(0)$ as multiplication by the phase $\exp\big(-\tfrac{\mathrm{i}}{\varepsilon}\int_0^s E_0\big)$, and the claim follows by Prop. \ref{StructureOfAdiabaticEvolution}. (Cf. [Avron, Seiler & Yaffe 1987, p. 34](#AvronSeilerYaffe87).)

=--

Combined with Theorem \ref{AdiabaticTheorem}, this gives the main statement of [Kato 1950, (29)](#Kato50):

+-- {: .num_cor #AdiabaticTransportOfGroundStates}
###### Corollary
**(adiabatic transport of ground states)**

Given a path of Hamiltonians with exactly degenerate gapped ground states, the actual time evolution on ground states satisfies, for all $s \in [0,1]$,
$$
  \Big\Vert
    U_\varepsilon(s)\, P(0)
    \;-\;
    e^{- \mathrm{i}\, \theta_\varepsilon(s)}
    \, K(s)\, P(0)
  \Big\Vert
  \;\leq\;
  C\, \varepsilon
  \,,
  \;\;\;\;\;\;
  \text{where}
  \;\;
  \theta_\varepsilon(s) 
  \;\coloneqq\; 
  \frac{1}{\varepsilon}\int_0^s E_0(u)\, \mathrm{d}u
  \,.
$$
Hence in the adiabatic limit $\varepsilon \to 0$, the time evolution acts on ground states, up to the *dynamical phase* $\theta_\varepsilon$, by the unitary operator
$$
  \begin{array}{ccc}
    \mathcal{H}_0(0) 
      &\xrightarrow{\;\;\sim\;\;}& 
    \mathcal{H}_0(s)
    \\
    \psi &\mapsto& K(s)\, \psi
    \,,
  \end{array}
$$
which is the [[parallel transport]] of the [[Berry connection]] (Rem. \ref{KatoTransportAsParallelTransport}).

=--

+-- {: .num_remark #PropertiesOfAdiabaticGroundStateTransport}
###### Remark
**(geometric nature of adiabatic ground state transport)**

The unitary $K(s)\vert_{\mathcal{H}_0(0)}$ in Cor. \ref{AdiabaticTransportOfGroundStates} has the following properties.

1. It is independent of the running time $\tau = 1/\varepsilon$.

1. It is independent of the parameterization of the path, since the defining equation $\partial_s K = [P',P]\, K$ is invariant under reparameterization $s \mapsto f(s)$. So $K$ depends only on the curve of ground state spaces $s \mapsto \mathcal{H}_0(s)$. For a parameterized system (Rem. \ref{OnPathsOfHamiltonians}) it therefore depends only on the unparameterized path in parameter space $X$.

1. The dynamical phase $\theta_\varepsilon(s)$ does depend on $\tau$ and on the parameterization, and it diverges as $\varepsilon \to 0$. But it is a *global* phase on all of $\mathcal{H}_0$, the same for all ground states. So it does not affect the relative phases and amplitudes between ground states.

Therefore the physically meaningful part of the adiabatic evolution of ground states is the purely geometric operation of [[parallel transport]] in the [[vector bundle]] $\mathcal{E} \to X$ of ground state spaces, with respect to the Berry connection $\nabla = P \circ \mathrm{d}$ (Rem. \ref{KatoTransportAsParallelTransport}).

=--

In particular, adiabatic transport along a [[loop]] $\gamma$ in parameter space, based at $x_0 \in X$, maps the ground state space back to itself, acting on it by the [[holonomy]]
$$
  \mathrm{hol}_\nabla(\gamma)
  \;\in\;
  \mathrm{U}\big( \mathcal{H}_0(x_0) \big)
  \,:
$$

* For non-degenerate ground states, $\mathrm{dim}\, \mathcal{H}_0 = 1$, this is multiplication by the *[[Berry phase]]* $\exp\big( \mathrm{i}\oint_\gamma A \big) \in \mathrm{U}(1)$ ([Simon 1983](#Simon83), [Berry 1984](#Berry84)).

* For degenerate ground states, $\mathrm{dim}\, \mathcal{H}_0 = n \geq 2$, this is a [[unitary group|unitary]] $n \times n$ [[matrix]], the *non-abelian Berry phase* ([Wilczek & Zee 1984](#WilczekZee84)). It is given by the [[path-ordered exponential]] of the non-abelian Berry connection form $A_{a b} = \mathrm{i}\langle \psi_a \vert \mathrm{d}\psi_b \rangle$.


#### Quasi-degenerate ground states
 {#QuasiDegenerateGroundStates}

In practice, ground state degeneracy is often only approximate. The bottom part $\sigma_\ast(s)$ of the spectrum is then a narrow band of width
$$
  \delta(s) 
  \;\coloneqq\; 
  \sup \sigma_\ast(s) - \inf \sigma_\ast(s)
$$
much smaller than the gap $g$ to the rest of the spectrum. Write $\bar E_0(s)$ for the midpoint of this band. The above conclusions still hold, provided the running time $\tau$ is long compared to the inverse gap but short compared to the inverse splitting:

+-- {: .num_prop #AdiabaticEvolutionOfQuasiDegenerateGroundStates}
###### Proposition
**(adiabatic evolution of quasi-degenerate ground states)**

With $C$ as in Theorem \ref{AdiabaticTheorem}, we have for all $s \in [0,1]$
$$
  \Big\Vert
    U_\varepsilon(s)\, P(0)
    \;-\;
    e^{- \tfrac{\mathrm{i}}{\varepsilon} \int_0^s \bar E_0(u) \, \mathrm{d}u}
    \, K(s)\, P(0)
  \Big\Vert
  \;\leq\;
  C\, \varepsilon
  \;+\;
  \frac{1}{2\varepsilon} \int_0^s \delta(u)\, \mathrm{d}u
  \,.
$$
Hence, up to a global phase, the ground states are transported by $K(s)$ as in Cor. \ref{AdiabaticTransportOfGroundStates}, within the time window
$$
  C 
  \;\ll\; 
  \tau 
  \;\ll\; 
  1/\sup_s \delta(s)
  \,.
$$

=--

+-- {: .proof}
###### Proof

On $\mathcal{H}_\ast(0)$, the generator of $D_\varepsilon$ (Prop. \ref{StructureOfAdiabaticEvolution}) is $K^\dagger H K P(0) = \bar E_0 P(0) + B$, where $B \coloneqq K^\dagger (H - \bar E_0) P K$ is self-adjoint with $\Vert B \Vert \leq \delta/2$. Since the scalar part commutes with everything, we have $D_\varepsilon(s) P(0) = e^{-\tfrac{\mathrm{i}}{\varepsilon}\int_0^s \bar E_0} \widetilde D_\varepsilon(s) P(0)$, where $\mathrm{i}\varepsilon\, \partial_s \widetilde D_\varepsilon = B \widetilde D_\varepsilon$. This implies $\Vert (\widetilde D_\varepsilon(s) - 1) P(0) \Vert \leq \tfrac{1}{\varepsilon}\int_0^s \Vert B \Vert$. Now combine with Theorem \ref{AdiabaticTheorem}.

=--

+-- {: .num_remark #TopologicalGroundStateDegeneracy}
###### Remark
**(topological ground state degeneracy)**

This quasi-degenerate situation is that of [[topological order|topologically ordered]] [[quantum materials]]. Here the splitting $\delta$ of the ground state degeneracy is [[exponential function|exponentially]] small in the system size $L$, $\delta \sim e^{- L/\xi}$, while the gap $g$ remains finite as $L \to \infty$ ([Hastings & Wen 2005](#HastingsWen05)). So the time window in Prop. \ref{AdiabaticEvolutionOfQuasiDegenerateGroundStates}, in which adiabatic transport of ground states is the unitary parallel transport $K$, is wide for large systems.

=--


#### Outlook: Adiabatic quantum gates
 {#OutlookAdiabaticQuantumGates}

The above statements make adiabatic transport of gapped ground states a means for implementing [[quantum gates]]. The (quasi-)degenerate ground state space $\mathcal{H}_0$ serves as the *code space*, and slowly cycling the external parameters through a loop $\gamma$ executes the gate $\mathrm{hol}_\nabla(\gamma)$, up to a global phase:

* **[[holonomic quantum computation]]** ([Zanardi & Rasetti 1999](#ZanardiRasetti99), [Pachos, Zanardi & Rasetti 1999](#PachosZanardiRasetti99)) uses the non-abelian Berry holonomies $\mathrm{hol}_\nabla(\gamma)$ as quantum gates. Since these depend only on the geometry of the loop, and not on its timing (Rem. \ref{PropertiesOfAdiabaticGroundStateTransport}), they are insensitive to some control errors. 

  The achievable gates form the [[holonomy group]] $\mathrm{Hol}(\nabla) \subset \mathrm{U}(\mathcal{H}_0)$. By the [[Ambrose-Singer theorem]], this is all of $\mathrm{U}(\mathcal{H}_0)$ if the components of the [[curvature]] of the Berry connection span the [[Lie algebra]] $\mathfrak{u}(\mathcal{H}_0)$. Such "irreducible" connections are the generic case, and then already two generic loops generate a dense set of gates ([Zanardi & Rasetti 1999, p. 96-97](#ZanardiRasetti99)). Explicit loops for a universal set of gates in a concrete model are constructed in [Pachos, Zanardi & Rasetti 1999](#PachosZanardiRasetti99).

* **[[topological quantum computation]]** arises when the Berry connection is ([[projectively flat connection|projectively]]) [[flat connection|flat]]. Then the holonomy depends only on the [[homotopy]] class of the loop, so that adiabatic transport constitutes a (projective) [[monodromy]] [[representation]]
  $$
    \begin{array}{ccc}
      \pi_1(X, x_0) &\longrightarrow& \mathrm{U}\big(\mathcal{H}_0(x_0)\big)
      \\
      [\gamma] &\mapsto& \mathrm{hol}_\nabla(\gamma)
    \end{array}
  $$
  of the [[fundamental group]] of parameter space. In the main example, $X$ is a [[configuration space of points]] of [[anyons]] (or of other [[defects]], such as [[band nodes]]), $\pi_1(X)$ is a [[braid group]], and the monodromy representation is the [[braid group statistics]] of the anyons ([Arovas, Schrieffer & Wilczek 1984](#ArovasSchriefferWilczek84), [Nayak, Simon, Stern, Freedman & Das Sarma 2008, §II.A.2](#NayakSimonSternFreedman08)). The gates are then protected against all small deformations of the braiding paths. In realistic systems, flatness holds up to corrections which are exponentially small in the separation of the anyons, as for the splitting $\delta$ in Rem. \ref{TopologicalGroundStateDegeneracy}. In this sense, holonomic quantum computation is "the (continuous) differential-geometric counterpart of the (discrete) topological QC with anyons" ([Pachos, Zanardi & Rasetti 1999, p. 1](#PachosZanardiRasetti99)).

* This is to be distinguished from **[[adiabatic quantum computation]]** in the sense of [Farhi, Goldstone, Gutmann & Sipser 2000](#FarhiGoldstoneGutmannSipser00). There one considers a *non-degenerate* ground state, and the result of the computation is encoded in the ground state of the final Hamiltonian $H(1)$ rather than in a holonomy. The running time required by Theorem \ref{AdiabaticTheorem}, governed by the minimal gap $g$ (Rem. \ref{OnTheAdiabaticTheorem}), then measures the complexity of the computation (see [Albash & Lidar 2018](#AlbashLidar18)).



## Related concepts

* [[Berry connection]], [[Berry phase]], [[Zak phase]]

* [[parallel transport]], [[holonomy]]

* [[adiabatic]]

* [[adiabatic switching]]

* [[adiabatic quantum computation]]

* [[holonomic quantum computation]]

* [[topological quantum computation]]

  * [[anyon]]

  * [[braid group statistics]]



## References

### General

The original formulation:

* {#BornFock28} [[Max Born]], [[Vladimir A. Fock]]: *Beweis des Adiabatensatzes*, Zeitschrift für Physik **51** (1928) 165-180 &lbrack;[doi:10.1007/BF01343193](https://doi.org/10.1007/BF01343193)&rbrack;

* {#Kato50} [[Tosio Kato]]: *On the Adiabatic Theorem of Quantum Mechanics*, J. Phys. Soc. Jpn. **5** (1950) 435-439 &lbrack;[doi:10.1143/JPSJ.5.435](https://doi.org/10.1143/JPSJ.5.435)&rbrack;

  > (introducing the "adiabatic transformation" $U'(s) = [E'(s), E(s)]\, U(s)$, now known as *Kato's parallel transport*, and proving that the actual time evolution of an isolated eigenspace approaches it, up to a dynamical phase, with error $O(1/\tau)$; or $o(1)$ in the presence of finitely many level crossings)

Textbook accounts:

* {#Messiah62} [[Albert Messiah]]: Chapter XVII of: *Quantum Mechanics*, Volume II, North-Holland (1962), reprinted by Dover (1999, 2014) &lbrack;[ISBN:9780486409245](https://store.doverpublications.com/products/9780486409245)&rbrack;

* {#Teufel03} [[Stefan Teufel]]: *Adiabatic Perturbation Theory in Quantum Dynamics*, Lecture Notes in Mathematics **1821**, Springer (2003) &lbrack;[doi:10.1007/b13355](https://doi.org/10.1007/b13355)&rbrack;

Rigorous generalizations and refinements, including higher-order and exponentially small error estimates:

* {#Nenciu80} [[Gheorghe Nenciu]]: *On the adiabatic theorem of quantum mechanics*, J. Phys. A: Math. Gen. **13** (1980) L15 &lbrack;[doi:10.1088/0305-4470/13/2/002](https://doi.org/10.1088/0305-4470/13/2/002)&rbrack;

* {#Nenciu81} [[Gheorghe Nenciu]]: *Adiabatic theorem and spectral concentration*, Commun. Math. Phys. **82** (1981) 121-135 &lbrack;[doi:10.1007/BF01206948](https://doi.org/10.1007/BF01206948)&rbrack;

* {#AvronSeilerYaffe87} [[Joseph E. Avron]], [[Ruedi Seiler]], Laurence G. Yaffe: *Adiabatic theorems and applications to the quantum Hall effect*, Commun. Math. Phys. **110** (1987) 33-49 &lbrack;[doi:10.1007/BF01209015](https://doi.org/10.1007/BF01209015)&rbrack;, Erratum: Commun. Math. Phys. **156** (1993) 649-650 &lbrack;[doi:10.1007/BF02096867](https://doi.org/10.1007/BF02096867)&rbrack;

  > (introducing the "adiabatic evolution" generated by $H(s) + \tfrac{\mathrm{i}}{\tau}[P'(s), P(s)]$ for spectral subspaces bordered by gaps, and proving that it approximates the actual dynamics to order $1/\tau$, with tunneling out of the spectral subspace smaller than any power of $1/\tau$ for smooth switching)

* {#Nenciu93} [[Gheorghe Nenciu]]: *Linear adiabatic theory. Exponential estimates*, Commun. Math. Phys. **152** (1993) 479-496 &lbrack;[doi:10.1007/BF02096616](https://doi.org/10.1007/BF02096616)&rbrack;

* {#HagedornJoye02} George A. Hagedorn, [[Alain Joye]]: *Elementary exponential error estimates for the adiabatic approximation*, J. Math. Anal. Appl. **267** (2002) 235-246 &lbrack;[doi:10.1006/jmaa.2001.7765](https://doi.org/10.1006/jmaa.2001.7765)&rbrack;

With explicit bounds (motivated by [[adiabatic quantum computation]]):

* {#JansenRuskaiSeiler07} Sabine Jansen, Mary Beth Ruskai, [[Ruedi Seiler]]: *Bounds for the adiabatic approximation with applications to quantum computation*, J. Math. Phys. **48** (2007) 102111 &lbrack;[arXiv:quant-ph/0603175](https://arxiv.org/abs/quant-ph/0603175), [doi:10.1063/1.2798382](https://doi.org/10.1063/1.2798382)&rbrack;

* {#AmbainisRegev04} Andris Ambainis, [[Oded Regev]]: *An elementary proof of the quantum adiabatic theorem* &lbrack;[arXiv:quant-ph/0411152](https://arxiv.org/abs/quant-ph/0411152)&rbrack;

On the failure of naive "adiabaticity conditions" when the rigorous hypotheses are dropped:

* {#MarzlinSanders04} Karl-Peter Marzlin, Barry C. Sanders: *Inconsistency in the Application of the Adiabatic Theorem*, Phys. Rev. Lett. **93** (2004) 160408 &lbrack;[arXiv:quant-ph/0404022](https://arxiv.org/abs/quant-ph/0404022), [doi:10.1103/PhysRevLett.93.160408](https://doi.org/10.1103/PhysRevLett.93.160408)&rbrack;

* {#Amin09} Mohammad H. S. Amin: *Consistency of the Adiabatic Theorem*, Phys. Rev. Lett. **102** (2009) 220401 &lbrack;[arXiv:0810.4335](https://arxiv.org/abs/0810.4335), [doi:10.1103/PhysRevLett.102.220401](https://doi.org/10.1103/PhysRevLett.102.220401)&rbrack;

Without a spectral gap condition:

* {#AvronElgart99} [[Joseph E. Avron]], Alexander Elgart: *Adiabatic Theorem without a Gap Condition*, Commun. Math. Phys. **203** (1999) 445-463 &lbrack;[arXiv:math-ph/9805022](https://arxiv.org/abs/math-ph/9805022), [doi:10.1007/s002200050620](https://doi.org/10.1007/s002200050620)&rbrack;

See also:

* Wikipedia: *[Adiabatic theorem](https://en.wikipedia.org/wiki/Adiabatic_theorem)*


### Holonomy and Berry phases

Interpretation of adiabatic transport as [[parallel transport]] in a [[vector bundle]] of [[eigenspaces]] over parameter space, with [[holonomy]] given by [[Berry phases]]:

* {#Simon83} [[Barry Simon]]: *Holonomy, the Quantum Adiabatic Theorem, and Berry's Phase*, Phys. Rev. Lett. **51** (1983) 2167 &lbrack;[doi:10.1103/PhysRevLett.51.2167](https://doi.org/10.1103/PhysRevLett.51.2167)&rbrack;

* {#Berry84} [[Michael Berry]]: *Quantal phase factors accompanying adiabatic changes*, Proc. Roy. Soc. Lond. A **392** (1984) 45-57 &lbrack;[doi:10.1098/rspa.1984.0023](https://doi.org/10.1098/rspa.1984.0023)&rbrack;

On the [[non-abelian group|non-abelian]] generalization to degenerate eigenspaces:

* {#WilczekZee84} [[Frank Wilczek]], [[Anthony Zee]]: *Appearance of Gauge Structure in Simple Dynamical Systems*, Phys. Rev. Lett. **52** (1984) 2111 &lbrack;[doi:10.1103/PhysRevLett.52.2111](https://doi.org/10.1103/PhysRevLett.52.2111)&rbrack;

* {#RigolinOrtiz12} [[Gustavo Rigolin]], [[Gerardo Ortiz]]: *The Adiabatic Theorem for Quantum Systems with Spectral Degeneracy*, Phys. Rev. A **85** (2012) 062111 &lbrack;[arXiv:1111.5333](https://arxiv.org/abs/1111.5333), [doi:10.1103/PhysRevA.85.062111](https://doi.org/10.1103/PhysRevA.85.062111)&rbrack;

Textbook account:

* {#BMKNZ03} Arno Bohm, Ali Mostafazadeh, Hiroyasu Koizumi, [[Qian Niu]], Joseph Zwanziger: *The Geometric Phase in Quantum Systems*, Texts and Monographs in Physics, Springer (2003) &lbrack;[doi:10.1007/978-3-662-10333-3](https://doi.org/10.1007/978-3-662-10333-3)&rbrack;

On adiabatic transport subject to repeated [[quantum measurement]]:

* Ludmila Viotti, Ana Laura Gramajo, Paula I. Villar, Fernando C. Lombardo, Rosario Fazio: *Geometric phases along quantum trajectories*, Quantum **7** (2023) 1029 &lbrack;[arXiv:2301.04222](https://arxiv.org/abs/2301.04222), [doi:10.22331/q-2023-06-02-1029](https://doi.org/10.22331/q-2023-06-02-1029)&rbrack;


### In condensed matter theory

Discussion in [[solid state physics]] and in view of gapped [[topological phases of matter]] ([[quantum Hall effect]], [[topological insulators]]), see also [Avron, Seiler & Yaffe 1987](#AvronSeilerYaffe87):

* [[Joseph E. Avron]], A. Raveh, B. Zur: *Adiabatic quantum transport in multiply connected systems*, Rev. Mod. Phys. **60** (1988) 873-915 &lbrack;[doi:10.1103/RevModPhys.60.873](https://doi.org/10.1103/RevModPhys.60.873)&rbrack;

* {#HastingsWen05} [[Matthew B. Hastings]], [[Xiao-Gang Wen]]: *Quasiadiabatic continuation of quantum states: The stability of topological ground-state degeneracy and emergent gauge invariance*, Phys. Rev. B **72** (2005) 045141 &lbrack;[arXiv:cond-mat/0503554](https://arxiv.org/abs/cond-mat/0503554), [doi:10.1103/PhysRevB.72.045141](https://doi.org/10.1103/PhysRevB.72.045141)&rbrack;

* {#BMNS12} [[Sven Bachmann]], [[Spyridon Michalakis]], [[Bruno Nachtergaele]], [[Robert Sims]]: *Automorphic Equivalence within Gapped Phases of Quantum Lattice Systems*, Commun. Math. Phys. **309** (2012) 835-871 &lbrack;[arXiv:1102.0842](https://arxiv.org/abs/1102.0842), [doi:10.1007/s00220-011-1380-0](https://doi.org/10.1007/s00220-011-1380-0)&rbrack;

* Jan Carl Budich, Björn Trauzettel: *From the adiabatic theorem of quantum mechanics to topological states of matter*, physica status solidi (RRL) **7** 1-2 (2013) 109-129 &lbrack;[arXiv:1210.6672](https://arxiv.org/abs/1210.6672), [doi:10.1002/pssr.201206416](https://doi.org/10.1002/pssr.201206416)&rbrack;

* David Aasen, [[Zhenghan Wang]], [[Matthew B. Hastings]]: *Adiabatic paths of Hamiltonians, symmetries of topological order, and automorphism codes*, Phys. Rev. B **106** (2022) 085122 &lbrack;[arXiv:2203.11137](https://arxiv.org/abs/2203.11137), [doi:10.1103/PhysRevB.106.085122](https://doi.org/10.1103/PhysRevB.106.085122)&rbrack;

With error bounds uniform in the system size, for gapped quantum many-body systems:

* {#BachmannDeRoeckFraas17} [[Sven Bachmann]], [[Wojciech De Roeck]], [[Martin Fraas]]: *Adiabatic Theorem for Quantum Spin Systems*, Phys. Rev. Lett. **119** (2017) 060201 &lbrack;[arXiv:1612.01505](https://arxiv.org/abs/1612.01505), [doi:10.1103/PhysRevLett.119.060201](https://doi.org/10.1103/PhysRevLett.119.060201)&rbrack;

* {#BachmannDeRoeckFraas18} [[Sven Bachmann]], [[Wojciech De Roeck]], [[Martin Fraas]]: *The adiabatic theorem and linear response theory for extended quantum systems*, Commun. Math. Phys. **361** (2018) 997-1027 &lbrack;[arXiv:1705.02838](https://arxiv.org/abs/1705.02838), [doi:10.1007/s00220-018-3117-9](https://doi.org/10.1007/s00220-018-3117-9)&rbrack;

* {#MonacoTeufel19} Domenico Monaco, [[Stefan Teufel]]: *Adiabatic currents for interacting fermions on a lattice*, Rev. Math. Phys. **31** (2019) 1950009 &lbrack;[arXiv:1707.01852](https://arxiv.org/abs/1707.01852), [doi:10.1142/S0129055X19500090](https://doi.org/10.1142/S0129055X19500090)&rbrack;

* {#HenheikTeufel22} Joscha Henheik, [[Stefan Teufel]]: *Adiabatic theorem in the thermodynamic limit: Systems with a uniform gap*, J. Math. Phys. **63** (2022) 011901 &lbrack;[arXiv:2012.15238](https://arxiv.org/abs/2012.15238), [doi:10.1063/5.0051632](https://doi.org/10.1063/5.0051632)&rbrack;

Review:

* {#BachmannDeRoeckFraas20} [[Sven Bachmann]], [[Wojciech De Roeck]], [[Martin Fraas]]: *The adiabatic theorem in a quantum many-body setting*, in: *Analytic Trends in Mathematical Physics*, Contemporary Mathematics **741** (2020) 43-58 &lbrack;[arXiv:1808.09985](https://arxiv.org/abs/1808.09985), [ISBN:978-1-4704-5388-6](https://bookstore.ams.org/conm-741)&rbrack;


### For adiabatic quantum computation

On [[adiabatic quantum computation]] via non-degenerate ground states:

* {#FarhiGoldstoneGutmannSipser00} [[Edward Farhi]], Jeffrey Goldstone, Sam Gutmann, Michael Sipser: *Quantum Computation by Adiabatic Evolution* &lbrack;[arXiv:quant-ph/0001106](https://arxiv.org/abs/quant-ph/0001106)&rbrack;

Review:

* {#AlbashLidar18} Tameem Albash, Daniel Lidar: *Adiabatic quantum computation*, Rev. Mod. Phys. **90** (2018) 015002 &lbrack;[arXiv:1611.04471](https://arxiv.org/abs/1611.04471), [doi:10.1103/RevModPhys.90.015002](https://doi.org/10.1103/RevModPhys.90.015002)&rbrack;


### For holonomic quantum computation
 {#ReferencesForHolonomicQuantumComputation}

On [[holonomic quantum computation]] by non-abelian Berry phases of degenerate ground states:

* {#ZanardiRasetti99} [[Paolo Zanardi]], [[Mario Rasetti]]: *Holonomic quantum computation*, Phys. Lett. A **264** (1999) 94-99 &lbrack;[arXiv:quant-ph/9904011](https://arxiv.org/abs/quant-ph/9904011), [doi:10.1016/S0375-9601(99)00803-8](https://doi.org/10.1016/S0375-9601(99)00803-8)&rbrack;

* {#PachosZanardiRasetti99} [[Jiannis Pachos]], [[Paolo Zanardi]], [[Mario Rasetti]]: *Non-Abelian Berry connections for quantum computation*, Phys. Rev. A **61** (1999) 010305(R) &lbrack;[arXiv:quant-ph/9907103](https://arxiv.org/abs/quant-ph/9907103), [doi:10.1103/PhysRevA.61.010305](https://doi.org/10.1103/PhysRevA.61.010305)&rbrack;

  > "In a sense HQC can be considered as the (continuous) differential-geometric counterpart of the (discrete) topological QC with anyons."


### For topological quantum computation
 {#ReferencesForTopologicalQuantumComputing}

References which make explicit that the standard model of [[topological quantum computation]] by [[braid group statistics|braiding]] of [[anyons]] is a form of adiabatic quantum computation:

* {#ArovasSchriefferWilczek84} [[Daniel P. Arovas]], [[Robert Schrieffer]], [[Frank Wilczek]]: *Fractional Statistics and the Quantum Hall Effect*, Phys. Rev. Lett. **53** (1984) 722 &lbrack;[doi:10.1103/PhysRevLett.53.722](https://doi.org/10.1103/PhysRevLett.53.722)&rbrack;

  > "The statistics of quasiparticles entering the quantum Hall effect are deduced from the adiabatic theorem."

* {#ArovasSchriefferWilczekZee85} [[Daniel P. Arovas]], [[Robert Schrieffer]], [[Frank Wilczek]], [[Anthony Zee]]: *Statistical mechanics of anyons*, Nuclear Physics B **251** (1985) 117-126 (reprinted in [Wilczek 1990, p. 173-182](anyon#Wilczek90)) &lbrack;<a href="https://doi.org/10.1016/0550-3213(85)90252-4">doi:10.1016/0550-3213(85)90252-4</a>&rbrack;

* {#FreedmanKitaevLarsenWang03} [[Michael Freedman]], [[Alexei Kitaev]], [[Michael Larsen]], [[Zhenghan Wang]]: *Topological quantum computation*, Bull. Amer. Math. Soc. **40** (2003) 31-38 &lbrack;[arXiv:quant-ph/0101025](https://arxiv.org/abs/quant-ph/0101025), [doi:10.1090/S0273-0979-02-00964-3](https://doi.org/10.1090/S0273-0979-02-00964-3)&rbrack;

* {#NayakSimonSternFreedman08} [[Chetan Nayak]], [[Steven H. Simon]], [[Ady Stern]], [[Michael Freedman]], [[Sankar Das Sarma]]: §II.A.2 (p. 6) of: *Non-Abelian Anyons and Topological Quantum Computation*, Rev. Mod. Phys. **80** (2008) 1083 &lbrack;[arXiv:0707.1889](https://arxiv.org/abs/0707.1889), [doi:10.1103/RevModPhys.80.1083](https://doi.org/10.1103/RevModPhys.80.1083)&rbrack;

* {#ChengGalitskiDasSarma11} [[Meng Cheng]], [[Victor Galitski]], [[Sankar Das Sarma]]: *Non-adiabatic Effects in the Braiding of Non-Abelian Anyons in Topological Superconductors*, Phys. Rev. B **84** (2011) 104529 &lbrack;[arXiv:1106.2549](https://arxiv.org/abs/1106.2549), [doi:10.1103/PhysRevB.84.104529](https://doi.org/10.1103/PhysRevB.84.104529)&rbrack;

* {#CLBFN15} Chris Cesare, Andrew J. Landahl, Dave Bacon, Steven T. Flammia, Alice Neels: *Adiabatic topological quantum computing*, Phys. Rev. A **92** (2015) 012336 &lbrack;[arXiv:1406.2690](https://arxiv.org/abs/1406.2690), [doi:10.1103/PhysRevA.92.012336](https://doi.org/10.1103/PhysRevA.92.012336)&rbrack;



[[!redirects quantum adiabatic theorems]]

[[!redirects adiabatic theorem]]
[[!redirects adiabatic theorems]]
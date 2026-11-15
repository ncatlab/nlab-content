

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", there is no harm in breaking the lock, as it is just caused by bot traffic. When the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***



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
  H 
  \;\colon\; 
  [0,1] \longrightarrow \mathcal{B}(\mathcal{H})
  \,,
  \;\;\;
  s \mapsto H(s)
$$
to [[self-adjoint operators]], which is twice continuously [[differentiable function|differentiable]] in the operator norm.

=--

+-- {: .num_remark #OnPathsOfHamiltonians}
###### Remark
**(on paths of Hamiltonians)**

1. Typically such a path arises from a *[[parameterized quantum system]]*, namely from a family of Hamiltonians $\hat H \colon X \to \mathcal{B}(\mathcal{H})$ over a [[smooth manifold]] $X$ of external parameters, by restriction along a smooth [[path]] $\gamma \colon [0,1] \to X$ in parameter space:
   $$
     H(s) \;\coloneqq\; \hat H\big(\gamma(s)\big)
     \,.
   $$

1. The restriction to [[bounded operators]] is for simplicity of exposition. Everything below generalizes to [[unbounded operator|unbounded]] Hamiltonians with common [[domain]], such that $H(s) \big(H(0) + \mathrm{i}\big)^{-1}$ is bounded and $C^2$ in $s$ (cf. [Avron, Seiler & Yaffe 1987](#AvronSeilerYaffe87), [Teufel 2003](#Teufel03)).

=--

Running through such a path in physical [[time]] $t \in [0,T]$ means that the system evolves under the time-dependent Hamiltonian $t \mapsto H(t/T)$. In terms of the rescaled time parameter $s \coloneqq t/T \in [0,1]$, the [[Schrödinger equation]] then reads as follows:

+-- {: .num_defn #AdiabaticSchroedingerEquation}
###### Definition
**(adiabatic time evolution)**

For $T \in (0,\infty)$ write
$$
  \varepsilon \;\coloneqq\; 1/T
$$
(the *adiabatic parameter*) and let $U_\varepsilon \colon [0,1] \to \mathcal{B}(\mathcal{H})$ be the [[solution]] of
$$
  \mathrm{i}\, \varepsilon \, \partial_s U_\varepsilon(s)
  \;=\;
  H(s)\, U_\varepsilon(s)
  \,,
  \;\;\;\;\;
  U_\varepsilon(0) \;=\; \mathrm{id}_{\mathcal{H}}
  \,.
$$
This exists, is unique and [[unitary operator|unitary]] for all $s$ (being given by the [[time-ordered exponential]] of $-\tfrac{\mathrm{i}}{\varepsilon}\int H$).

=--

The *adiabatic limit* is the limit $\varepsilon \to 0$, i.e. $T \to \infty$, in which the path of Hamiltonians is traversed infinitely slowly. Notice that in the rescaled time $s$ the dynamics becomes *fast* in this limit: For instance, if $H(s) = H$ is constant and $H \psi = E \psi$, then $U_\varepsilon(s)\psi = e^{-\mathrm{i} E s/\varepsilon} \psi$.


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

We speak of *gapped [[ground states]]* if $\sigma_\ast(s)$ is the bottom part of the spectrum: $\sup \sigma_\ast(s) \lt \inf \sigma_\perp(s)$. In the special case that $\sigma_\ast(s) = \{E(s)\}$ is a single [[eigenvalue]], we speak of *exactly degenerate* ground states (where the degeneracy may be 1).

=--

+-- {: .num_defn #SpectralProjection}
###### Definition
**(spectral projection)**

Given a path satisfying the gap condition (Def. \ref{GapCondition}), the *spectral projections* onto $\sigma_\ast(s)$ are given by the [[Riesz projection|Riesz formula]]
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

1. The function $s \mapsto P(s)$ is $C^2$ in the operator norm.

1. The [[dimension]] of $\mathcal{H}_\ast(s)$ is independent of $s$ (possibly infinite).

1. The derivative $P' \coloneqq \partial_s P$ is *off-diagonal* with respect to the decomposition $\mathcal{H} = \mathcal{H}_\ast(s) \oplus \mathcal{H}_\ast(s)^\perp$, in that
   $$
     P \, P' \, P \;=\; 0
     \,,
     \;\;\;\;\;
     P' \;=\; P' P + P P'
     \,.
   $$

=--

+-- {: .proof}
###### Proof

The first statement is standard [[functional calculus]]. The second follows since the [[resolvent]] $(z - H(s))^{-1}$ is $C^2$ in $s$, locally uniformly for $z$ on the contour. The third follows by the general fact that projections at operator-norm distance $\Vert P(s) - P(s') \Vert \lt 1$ are [[unitary operator|unitarily]] equivalent, together with [[continuous function|continuity]] of $P$ and [[connected topological space|connectedness]] of $[0,1]$. The last statement follows by differentiating $P^2 = P$ to get $P' P + P P' = P'$, and then multiplying this from both sides by $P$, to get $2 P P' P = P P' P$.

=--


#### Kato's parallel transport
 {#KatoParallelTransport}

+-- {: .num_defn #KatoTransport}
###### Definition
**(Kato's parallel transport)**

Given a $C^1$ path $s \mapsto P(s)$ of orthogonal projections, its *Kato transport* ([Kato 1950](#Kato50)) is the solution $T \colon [0,1] \to \mathcal{B}(\mathcal{H})$ of
$$
  \partial_s T(s) 
  \;=\; 
  \big[ P'(s),\, P(s) \big] \, T(s)
  \,,
  \;\;\;\;\;
  T(0) \;=\; \mathrm{id}_{\mathcal{H}}
  \,.
$$

=--

+-- {: .num_prop #KatoTransportIsUnitaryAndIntertwining}
###### Proposition
**(Kato transport is unitary and intertwining)**

The Kato transport $T(s)$ (Def. \ref{KatoTransport}) is [[unitary operator|unitary]] for all $s$, and it intertwines the projections:
$$
  T(s)\, P(0) 
  \;=\; 
  P(s)\, T(s)
  \,.
$$
Hence it restricts to unitary [[isomorphisms]]
$$
  T(s)\vert_{\mathcal{H}_\ast(0)}
  \;\colon\;
  \mathcal{H}_\ast(0)
  \xrightarrow{\;\;\sim\;\;}
  \mathcal{H}_\ast(s)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The generator $[P', P]$ is anti-[[self-adjoint operator|self-adjoint]], since $[P',P]^\dagger = [P, P'] = -[P', P]$, so that $T(s)$ is unitary. For the intertwining property, consider $Q(s) \coloneqq T(s)^\dagger P(s) T(s)$. Then
$$
  Q'
  \;=\;
  T^\dagger 
  \Big(
    P' - \big[ [P',P], P \big]
  \Big) 
  T
  \;=\;
  0
  \,,
$$
because $\big[[P',P],P\big] = P'P - 2 P P' P + P P' = P'$ by Prop. \ref{PropertiesOfSpectralProjections}. Hence $Q(s) = Q(0) = P(0)$.

=--

+-- {: .num_remark #KatoTransportAsParallelTransport}
###### Remark
**(Kato transport as parallel transport of the Berry connection)**

For $\psi_0 \in \mathcal{H}_\ast(0)$, the transported vectors $\psi(s) \coloneqq T(s)\psi_0 \in \mathcal{H}_\ast(s)$ satisfy (using Prop. \ref{PropertiesOfSpectralProjections})
$$
  P(s)\, \psi'(s) \;=\; 0
  \,.
$$
This says that they are *covariantly constant* with respect to the [[connection on a bundle|connection]] $\nabla \coloneqq P \circ \mathrm{d}$ on the [[vector bundle]] whose [[fibers]] are the spaces $\mathcal{H}_\ast$ (the [[sub-bundle]] of the [[trivial bundle]] with fiber $\mathcal{H}$ cut out by the projections $P$). Therefore the Kato transport is the [[parallel transport]] of this connection, which is known as the *[[Berry connection]]*:

* If $\hat H$ is a family of Hamiltonians over parameter space $X$ (Rem. \ref{OnPathsOfHamiltonians}), satisfying the gap condition at every point, then the spaces $\mathcal{H}_\ast\big(\hat H(x)\big)$ form a vector bundle $\mathcal{E} \to X$ with connection $\nabla = P \circ \mathrm{d}$. Kato transport along a [[loop]] $\gamma$ in $X$ is the [[holonomy]] 
  $$
    \mathrm{hol}_\nabla(\gamma) 
    \;\in\; 
    \mathrm{U}\big(\mathcal{E}_{\gamma(0)}\big)
  $$
  of this connection.

* In terms of a local [[orthonormal basis|orthonormal frame]] $(\psi_a)_a$ of $\mathcal{E}$, the [[connection form]] has components
  $$
    A_{a b} 
    \;=\; 
    \mathrm{i}\, \langle \psi_a \vert \mathrm{d} \psi_b \rangle
    \,,
  $$
  which is the *non-abelian Berry connection* ([Wilczek & Zee 1984](#WilczekZee84)). In the case of rank 1, this is the original Berry connection $A = \mathrm{i}\langle \psi \vert \mathrm{d}\psi \rangle$ ([Simon 1983](#Simon83), [Berry 1984](#Berry84)), whose holonomy along a loop is multiplication by the *[[Berry phase]]* $\exp\big(\mathrm{i}\oint_\gamma A\big) \in \mathrm{U}(1)$.

=--

...
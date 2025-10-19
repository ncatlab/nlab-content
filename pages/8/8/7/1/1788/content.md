> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***

## Details


### The classifying space

The assumption that the system and all its accessible deformations are

1. [[energy gap|gapped]]

1. with $v \in \mathbb{N}$ [[valence bands]] filled

1. and $c \in \mathbb{N}$ [[conduction bands]] available

means that the space of available [[fiber]] [[Bloch Hamiltonians]] is (taking the [[energy gap]] to be around zero, without restriction of generality)

$$
  AccBlchHams 
    \coloneqq 
  \Big\{
    H \in \mathcal{B}\big(\mathbb{C}^{v+c}\big)
    \,\Big\vert\,
      H^\dagger = H
      ,\,
      Eig_{\lt 0}(H) \simeq \mathbb{C}^{v}
      ,\,
      Eig_{\gt 0}(H) \simeq \mathbb{C}^c
  \Big\}
  \,,
$$

where 

* $\mathcal{B}\big(\mathbb{C}^{v+c}\big) \simeq Mat_{v+c \times v + c}(\mathbb{C})$ denotes the space of [[bounded linear operators]], hence of [[matrices]],

* "$Eig_{(-)}(H) \subset \mathbb{C}^{v+c}$" denotes the [[eigenspace]] of the [[Hamiltonian]] [[linear operator|operator]] for the given range of [[eigenvalues]].

Since the [[homotopy classes]] of [[maps]] to this space depend only on its [[homotopy type]], we observe that this space is evidently [[homotopy equivalence|homotopy equivalent]] to the space of *normalized* Bloch Hamiltonians whose [[eigenvalues]] have unit [[absolute value]]:

\[
  \label{SpaceOfNormalizedBlochHamiltonians}
  NrmAccBlchHams 
    \;\coloneqq\;
  \Big\{
    H \in \mathcal{B}\big(\mathbb{C}^{v+c}\big)
    \,\Big\vert\,
      H^\dagger = H
      ,\,
      Eig_{-1}(H) \simeq \mathbb{C}^{v}
      ,\,
      Eig_{+1}(H) \simeq \mathbb{C}^c
  \Big\}
  \,,
\]

via

\[
  \label{HomotopyEquivalenceNormalizingBlochHamiltonians}
  \begin{array}{ccc}
    AccBlchHams 
      &\xrightarrow{\phantom{-} \sim  \phantom{-}}&
    NrmAccBlchHams
    \\
    H 
      &\mapsto& 
    N_H \coloneqq \sqrt{H^2}^{-1} \circ H 
    \mathrlap{\,,}
  \end{array}
\]

where 

* $\sqrt{H^2}$ denotes the unique [[positive definite matrix|positive definition]] [[square root]] of $H$, 

* $(-)^{-1}$ denotes the [[inverse]] operator.

In fact, (eq:HomotopyEquivalenceNormalizingBlochHamiltonians) is a [[deformation retraction]]: its [[right inverse]] is given by the inclusion

\[
  \begin{array}{ccc}
    NrmAccBlchHams
      &\xhookrightarrow{\phantom{--}}&
    AccBlchHams 
    \\
    N &\mapsto& N
    \mathrlap{\,,}
  \end{array}
\]

and a [[homotopy]]

$$
  (H \mapsto N_H) \Rightarrow (H \mapsto H)
$$

is given by

\[
  \label{NormalizingHomotopy}
  \begin{array}{ccc}
    AccBlchHams \times [0,1]
    &\longrightarrow&
    AccBlchHams
    \\
    (H, t) 
      &\mapsto&
    \big(
      (1-t)\sqrt{H^2}^{-1} + t \mathrm{I}_{c+v}
    \big)
      \circ
    H
    \mathrlap{\,.}
  \end{array}
\]
 
But this space of normalized Bloch Hamiltonians (eq:SpaceOfNormalizedBlochHamiltonians) is furthermore [[homotopy equivalence|homotopy equivalent]] ([[homeomorphism|homeomorphic]], even) to the space of [[hermitian operator|hermitian]] [rank](rank#RankOfALinearMap)=$c$ [projection operators](projection#InLinearAlgebra)

\[
  \label{SpaceOfProjectors}
  Proj_v^{c+v} 
    \;\coloneqq\;
  \Big\{
    P \in \mathcal{B}\big(\mathbb{C}^{v+c}\big) 
    \,\Big\vert\,
    P^\dagger = P
    ,\,
    P \circ P = P
    ,\,
    rnk(P) = c
  \Big\}
  \mathrlap{\,,}
\]

via

$$
  \begin{array}{ccc}
    NrmAccBlchHams
      &\xrightarrow{\phantom{-} \sim \phantom{-}}&
    Proj_{v}^{v+c}
    \\
    N
      &\mapsto& 
    \tfrac{1}{2}\big(1_{c+v} + N\big)
    \mathrlap{}
  \end{array}
$$

and furthermore to the "[[Grassmannian]]"

$$
  Gr_v^{v+c} 
    \;\coloneqq\;
  \Big\{
    V \subset \mathbb{C}^{v + c}
    \,\Big\vert\,
    dim(V) = v
  \Big\}
    \;\simeq\;
  \frac{ 
    \mathrm{U}(v+c)
   }{
     \mathrm{U}(v) \times \mathrm{U}(c)
   }
  \mathrlap{\,,}
$$

by passage to [[kernels]] $ker(-)$:

$$
  \begin{array}{ccc}
    Proj_{v}^{v+c}
      &\xrightarrow{\phantom{-} \sim \phantom{-}}&
    Gr_v^{v+c}
    \\
    P 
      &\mapsto&
    ker(P)
    \mathrlap{\,.}
  \end{array}
$$


### The symmetry group action

Furthermore assuming that the system and all its available deformations respects ("is [[symmetry protected topological phase|protected]]" by) a [[subgroup]] $G$ of the [[point group]] of the [[crystal|crystalline]] material, acting on [[crystal momenta]] as

$$
  \begin{array}{ccc}
    G \times \widehat{T}{}^d &\longrightarrow& \widehat{T}{}^d
    \\
    \big(g, [\vec k]\big) &\mapsto& g \cdot [\vec k]
  \end{array}
  \mathrlap{\,,}
$$

means to specify a [[unitary representation]] [[group representation]]

\[
  \label{ThePointGroupRepresentation}
  \rho 
    \;\colon\;
  G 
    \longrightarrow 
  \mathrm{U}\big(\mathbb{C}^{c+v}\big)
\] 

such that the [[Bloch Hamiltonian]] satisfies

$$
  H_{ g \cdot [k] }
  \;=\;
  U_g \circ H_{[\vec k]} \circ U_g^{-1}
  \,,
$$

hence that as a [[map]] 

$$
  H_{(-)} \,\colon\,
  \widehat{T}{}^d 
    \longrightarrow
  AccBlchHams
$$

it is *[[equivariant map|equivariant]]*, for $AccBlchHams$ regarded as a [[G-space]] via the [[conjugation action]] of (eq:ThePointGroupRepresentation).

Again, the [[equivariant homotopy theory|equivariant homotopy class]] of such a map depends only on the equivariant homotopy type of $AccBlchHams$ --- but that is the same as that of $NrmAccBlchHams$, because the above normalizing homotopy (eq:NormalizingHomotopy) is itself equivariant.


### The classification statement

In consequence, we find that the unstable $G$-symmetry protected crystalline topological phases seen when $v$ [[valence bands]] are filled and $c$ [[conduction bands]] are accessible are given by the [[equivariant map|equivariant]] [[homotopy classes]] of maps from the [[Brillouin torus]] to $Proj_{v}^{c+v} = Gr_{v}^{c+v}$, hence by the [[equivariant cohomology|equivariant]] [[nonabelian cohomology]] of the [[Brillouin torus]] with [[coefficients]] in $Proj_v^{v+c}$

\[
  \label{UnstablePhasesViaEquivariantNonabelianCohomology}
  (v,c)Phases^G(d)
  \;\simeq\;
  H_G\big( \widehat{T}{}^d;\, Proj_{v}^{c+v} \big)
  \;\coloneqq\;
  \pi_0\,
  Map\big(
    \widehat{T}{}^d
    ,\,
    Proj_{v}^{c+v}
  \big)
  \,.
\]

For example: For $v = 1$ and $c = 1$ (the usual case of [[Chern insulators]], when $d = 2$), the classifying space (eq:SpaceOfProjectors) is the ([[Riemann sphere|Riemann]]) [[2-sphere]]

$$
  Proj_{1}^{2} 
    \;\simeq\; 
  \mathbb{C}P^1 
   \;\simeq\;
  S^2
  \mathrlap{\,,}
$$

and the [[nonabelian cohomology]] theory in (eq:UnstablePhasesViaEquivariantNonabelianCohomology) is *[[equivariant Cohomotopy|equivariant]] 2-[[Cohomotopy]]*.


### Stabilization

The stable situation is obtained by allowing access to *any* number of conduction bands and valence bands.

First, allowing access to arbitrary [[conduction bands]] means to consider the [[union]] ([[colimit]]) of the [[Grassmannians]] with respect to their canonical inclusions $Gr_v^{v + c} \hookrightarrow Gr_v^{v + c + 1}$:

$$
  B \mathrm{U}(v)
    \;\simeq\;
   \textstyle{\bigcup_{c \in \mathbb{N}}}
   Gr_v^{v + c}
  \,.
$$

This yields the [[classifying space]] for [[complex vector bundles]] of [[rank of a vector bundle|rank]]=$v$: the [[valence bundle]].

The corresponding classifying [[nonabelian cohomology]] theory (eq:UnstablePhasesViaEquivariantNonabelianCohomology) is also known as *[[unstable K-theory]]*.

Then also allowing an arbitrary number of [[valence bands]] means to further pass to the [[union]] ([[colimit]])

$$
  B \mathrm{U}
    \;\simeq\;
  \textstyle{\bigcup_{v \in \mathbb{N}}}
  B \mathrm{U}(v)
    \;\simeq\;
  \bigcup_{v \in \mathbb{N}}
  \bigcup_{c \in \mathbb{N}}
   Gr_v^{v + c}
  \,,
$$

which is known as the [[classifying space]] of the *[[stable unitary group]]*. This is the classifying space for [[reduced K-theory|reduced]] [[complex K-theory]] (of [[virtual vector bundles]] with vanishing virtual rank).




















 









+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
#### Harmonic analysis
+-- {: .hide}
[[!include harmonic analysis - contents]]
=--
=--
=--


\tableofcontents


## Idea
 {#Idea}

In [[solid state physics]], *Bloch's theorem* ([Bloch 1929](#Bloch29)) says that the [[energy]] [[eigenstates]] of a single [[electron]] in a [[crystal]] --- hence of a [[Schrödinger operator]] with [[periodic function|periodic]] [[potential energy|potential]] --- may be chosen to be *Bloch waves* (*Bloch states*): [[plane waves]] $e^{i k \cdot x}$ modulated by a [[function]] $u_k$ which is periodic with respect to the crystal [[lattice]] $\Lambda$:

$$
  \psi_k(x)
    \;=\;
  e^{i k \cdot x}\, u_k(x)
  \,,
  \;\;\;\;\;\;
  u_k(x + a) \;=\; u_k(x)
  \;\;\;
  \text{for all}\; a \in \Lambda
  \,.
$$

The wave vector $k$ here is called the *crystal momentum* or *quasi-momentum*. Since $e^{i G \cdot x}$ is itself lattice-periodic when $G$ is in the *reciprocal lattice* $\Lambda^\ast$ (Def. \ref{CrystalLatticeAndBrillouinTorus}), the crystal momentum is well-defined only modulo $\Lambda^\ast$, and hence ranges over a [[torus]]: the *[[Brillouin torus]]*.

Conceptually, Bloch's theorem is an instance of [[harmonic analysis]] on the [[abelian group]] $\Lambda \simeq \mathbb{Z}^d$ of lattice translations: Since these commute with the [[Hamiltonian]], the [[Hilbert space]] of states decomposes as a [[direct integral]] over the [[irreducible representation|irreducible]] [[unitary representations]] of $\Lambda$, hence over its [[characters]], which form the [[Pontrjagin dual group]] of $\Lambda$ --- this is the [[Brillouin torus]]. Accordingly, the Hamiltonian decomposes into a family of *Bloch Hamiltonians* $H(k)$ parametrized by points $k$ of the [[Brillouin torus]], whose [[eigenvalues]], as functions of $k$, are the *energy bands* of [[electron band theory]].

For *tight-binding models* with $N$ orbitals per unit cell (Def. \ref{TightBindingHamiltonian}, Rem. \ref{TerminologyTightBinding}) the Bloch Hamiltonian is simply a map from the [[Brillouin torus]] to the space of [[Hermitian matrix|Hermitian]] $N \times N$ [[matrices]] (Prop. \ref{BlochTheoremForTightBindingModels}), which is the more regular the more local the hopping is (Prop. \ref{RegularityOfBlochHamiltonians}). The condition that the crystal is a band [[insulator]] means that these maps take values in the subspace of Hermitian matrices with a [[spectral gap]] at the [[Fermi energy]], which is [[homotopy equivalence|homotopy equivalent]] to a [[disjoint union]] of [[Grassmannians]] (Prop. \ref{SpaceOfGappedBlochHamiltonians}). Therefore deformation classes of gapped Bloch Hamiltonians are classified by the [[topological K-theory]] of the [[Brillouin torus]], which is the starting point of the [[K-theory classification of topological phases of matter]] (Rem. \ref{KTheoryClassification}).


The tight-binding case captures the general situation of a [[Schrödinger operator]] with periodic potential (Prop. \ref{BlochFloquetDecomposition}) restricted to an isolated family of bands, at least whenever the corresponding *Bloch bundle* over the [[Brillouin torus]] is [[trivial bundle|trivializable]], as is automatic in the presence of [[time-reversal symmetry]] in [[dimension]] $d \leq 3$ (Prop. \ref{TrivialityOfBlochBundles}, Prop. \ref{ReductionToTightBinding}, Rem. \ref{BlochHamiltoniansOfElectronsInCrystals}).

The analogous statement with spatial t0ranslations replaced by time translations, hence for Hamiltonians periodic in time, is the theorem of [[Floquet theory]] ([Floquet 1883](#Floquet1883)), which historically predates Bloch's theorem; hence one also speaks of *Bloch-Floquet theory*.

<center>
<div style="margin:-20px 0px -10px 00px;">
<img src="/nlab/files/BlochTheoremSchematics_26-11-15.png" width="850"/>
</div>
<small>
  Under Bloch's theorem, the Hamiltonian of a single electron in a crystal lattice is decomposed into one Bloch Hamiltonian of internal orbital motion per plane wave vector k ranging over the Brillouin torus of electron quasimomenta in the crystal. The result is a map from the Brillouin torus to the space of accessible internal Bloch Hamiltonians.
</small>
</center>


## Statement
 {#Statement}

### Setup
 {#Setup}

+-- {: .num_defn #CrystalLatticeAndBrillouinTorus}
###### Definition
**(crystal lattice and Brillouin torus)**

Let $d \in \mathbb{N}$ (the spatial [[dimension]], typically $d \in \{1,2,3\}$).

1. A *crystal lattice* is a [[lattice]] $\Lambda \subset \mathbb{R}^d$ in $d$-dimensional [[Euclidean space]], hence a [[discrete group|discrete]] [[subgroup]] of the form $\Lambda = \mathbb{Z} a_1 + \cdots + \mathbb{Z} a_d \simeq \mathbb{Z}^d$ for a [[linear basis]] $(a_1, \cdots, a_d)$ of $\mathbb{R}^d$. A [[fundamental domain]] for the [[action]] of $\Lambda$ on $\mathbb{R}^d$ is called a *unit cell*.

1. Its *reciprocal lattice* is

   $$
     \Lambda^\ast
       \;\coloneqq\;
     \Big\{
       G \in \mathbb{R}^d
       \;\Big\vert\;
       \underset{a \in \Lambda}{\forall} \; G \cdot a \,\in\, 2\pi \mathbb{Z}
     \Big\}
     \,.
   $$

1. Its *[[Brillouin torus]]* is the [[Pontrjagin dual group]] of $\Lambda$, hence the [[group]] of its [[characters]], which is identified with the [[quotient group]] of $\mathbb{R}^d$ by the reciprocal lattice:

   $$
     \widehat{T}{}^d
       \;\coloneqq\;
     \mathrm{Hom}_{Grp}\big(\Lambda,\, U(1)\big)
       \;\simeq\;
     \mathbb{R}^d / \Lambda^\ast
     \,,
   $$

   via $[k] \mapsto \big(a \mapsto e^{i k \cdot a}\big)$. A [[fundamental domain]] $B \subset \mathbb{R}^d$ for this quotient (traditionally the Voronoi cell of $0 \in \Lambda^\ast$) is called a *Brillouin zone*.

   We write $d k$ for the [[Haar measure]] on $\widehat{T}{}^d$ normalized to total volume 1, hence for the [[Lebesgue measure]] on $B$ divided by $\mathrm{vol}(B)$.

=--


### For tight-binding models
 {#ForTightBindingModels}

+-- {: .num_defn #TightBindingHamiltonian}
###### Definition
**(tight-binding Hamiltonians)**

For $N \in \mathbb{N}_{\geq 1}$, a *tight-binding Hamiltonian* with $N$ orbitals per unit cell is a [[bounded operator|bounded]] [[self-adjoint operator]] $H$ on the [[Hilbert space]]

$$
  \mathcal{H}
    \;\coloneqq\;
  \ell^2\big(\Lambda;\, \mathbb{C}^N\big)
    \;\simeq\;
  \ell^2(\Lambda) \otimes \mathbb{C}^N
$$

which commutes with all lattice translations $(T_b \psi)(a) \coloneqq \psi(a - b)$, $b \in \Lambda$.

Equivalently, $H$ is a [[convolution]] operator

$$
  (H \psi)(a)
    \;=\;
  \underset{b \in \Lambda}{\sum} h(a - b) \cdot \psi(b)
$$

with *hopping matrices* $h \colon \Lambda \to \mathrm{Mat}_{N \times N}(\mathbb{C})$ given by

$$
  h_{i j}(a)
    \;\coloneqq\;
  \big\langle
    \delta_a \otimes e_i
    ,\,
    H (\delta_0 \otimes e_j)
  \big\rangle
$$

(the amplitude for an electron to hop from orbital $j$ in cell $0$ to orbital $i$ in cell $a$), which satisfy $h(-a) = h(a)^\dagger$.

We say that the hopping is:

* of *finite range* if $h(a) = 0$ for all but finitely many $a \in \Lambda$;

* *exponentially decaying* if $\Vert h(a) \Vert \leq C e^{- \beta \vert a \vert}$ for some $C, \beta \gt 0$;

* *rapidly decaying* if $\Vert h(a) \Vert \cdot (1 + \vert a \vert)^m$ is bounded, for all $m \in \mathbb{N}$;

* *summable* if $\sum_{a \in \Lambda} \Vert h(a) \Vert \lt \infty$.

=--

+-- {: .num_remark #TerminologyTightBinding}
###### Remark
**(terminology: "tight binding" and "Bloch Hamiltonian")**

* The term *tight binding* refers to the original motivation for such models ([Bloch 1929](#Bloch29), [Slater & Koster 1954](#SlaterKoster54), see [Ashcroft & Mermin 1976, Ch. 10](#AshcroftMermin76)): If the electrons of interest are *tightly bound* to the [[atoms]] (ions) of the crystal, then their [[wave functions]] are well approximated by linear combinations of finitely many localized [[atomic orbitals]] (the *LCAO method*: "linear combination of atomic orbitals"). This means that the single-electron Hilbert space $L^2(\mathbb{R}^d)$ may be truncated to the span of these orbitals, which (after orthonormalization) is $\simeq \ell^2(\Lambda; \mathbb{C}^N)$ if there are $N$ relevant orbitals per unit cell. The matrix elements of the Hamiltonian between orbitals in different cells involve the overlap of their wave functions, which decays rapidly with distance; hence the *hopping matrices* $h(a)$ are dominated by small $\vert a \vert$, and are typically truncated to finite range (often to "nearest neighbours").

* What this reflects in modern understanding is not so much tight binding as the *isolation of a family of $N$ bands* (typically those near the [[Fermi energy]]) from the rest of the spectrum by [[spectral gaps]]: In this situation, the band-projected continuum Hamiltonian is *exactly* (not just approximately) [[unitary equivalence|unitarily equivalent]] to a tight-binding Hamiltonian with exponentially decaying hopping, provided that the corresponding [Bloch bundle](#BlochBundle) is trivializable, in which case the role of the "orbitals" is played by exponentially localized [Wannier functions](#WannierFunctions) (Prop. \ref{ReductionToTightBinding} below). In this sense, "tight-binding model" is used today essentially synonymously with "lattice model with finitely many degrees of freedom per unit cell", irrespective of how tightly the electrons are actually bound.

* Accordingly, the term *Bloch Hamiltonian* for the operators $H(k)$ (Def. \ref{BlochHamiltonian} below, and similarly for the fiber operators in Prop. \ref{BlochFloquetDecomposition}) reflects that these are what remains of the Hamiltonian after diagonalizing the lattice translation symmetry, following Bloch: one Hamiltonian for each value of the crystal momentum, acting only on the internal (orbital, or intra-cell) degrees of freedom.

=--

+-- {: .num_prop #BlochTheoremForTightBindingModels}
###### Proposition
**(Bloch's theorem for tight-binding models)**

Given a tight-binding Hamiltonian $H$ (Def. \ref{TightBindingHamiltonian}), the [[Fourier transform]]

$$
  \array{
    \ell^2\big(\Lambda;\, \mathbb{C}^N\big)
    &\overset{\mathcal{F}}{\longrightarrow}&
    L^2\big(\widehat{T}{}^d;\, \mathbb{C}^N\big)
    \\
    \psi
      &\mapsto&
    \Big(
      k \mapsto \underset{a \in \Lambda}{\sum} e^{- i k \cdot a}\, \psi(a)
    \Big)
  }
$$

is a [[unitary operator]] which transforms $H$ into the operator of [[multiplication]] by the matrix-valued function

$$
  H(-)
    \;\colon\;
  \widehat{T}{}^d \longrightarrow \mathrm{Herm}(N)
  \,,
  \;\;\;\;\;\;
  H(k)
    \;\coloneqq\;
  \underset{a \in \Lambda}{\sum} e^{- i k \cdot a}\, h(a)
  \,,
$$

in that

$$
  \big(\mathcal{F} H \mathcal{F}^{-1} \phi\big)(k)
    \;=\;
  H(k) \cdot \phi(k)
  \,.
$$

(For non-summable hopping the sum defining $H(k)$ is understood as an $L^2$-limit, so that $H(-)$ is an essentially bounded measurable function.)

If the hopping is summable, then furthermore:

1. **(Bloch waves)** For every $k \in \mathbb{R}^d$ and every eigenvector $v \in \mathbb{C}^N$ of $H(k)$ with eigenvalue $E$, the bounded function

   $$
     \psi_k(a) \;\coloneqq\; e^{i k \cdot a}\, v
   $$

   is a generalized eigenvector of $H$, $H \psi_k = E\, \psi_k$, and is quasi-periodic: $\psi_k(a + b) = e^{i k \cdot b}\, \psi_k(a)$.

1. **(band structure)** $H(-)$ is continuous, and so are its ordered eigenvalues $E_1(k) \leq E_2(k) \leq \cdots \leq E_N(k)$, the *band functions*. The [[spectrum of an operator|spectrum]] of $H$ is the union of the *energy bands*:

   $$
     \sigma(H)
       \;=\;
     \underset{k \in \widehat{T}{}^d}{\bigcup} \sigma\big(H(k)\big)
       \;=\;
     \overset{N}{\underset{n = 1}{\bigcup}}\, E_n\big(\widehat{T}{}^d\big)
     \,,
   $$

   which is a union of at most $N$ [[closed intervals]].

=--

+-- {: .proof}
###### Proof

Unitarity of $\mathcal{F}$ is the [[Plancherel theorem]] for the [[Pontrjagin duality]] between $\Lambda$ and $\widehat{T}{}^d$, and the transformation of $H$ is the convolution theorem. Self-adjointness $H(k)^\dagger = H(k)$ follows from $h(-a) = h(a)^\dagger$.

For the Bloch waves, compute:

$$
  (H \psi_k)(a)
    \;=\;
  \underset{b}{\sum} h(a - b)\, e^{i k \cdot b}\, v
    \;=\;
  e^{i k \cdot a}\, \underset{c}{\sum} e^{- i k \cdot c}\, h(c)\, v
    \;=\;
  e^{i k \cdot a}\, H(k)\, v
    \;=\;
  E\, \psi_k(a)
  \,.
$$

For summable hopping, $H(-)$ is a uniform limit of continuous functions, hence continuous, and continuity of the ordered eigenvalues follows by Weyl's inequality $\big\vert E_n(k) - E_n(k') \big\vert \leq \big\Vert H(k) - H(k') \big\Vert$. Finally, the spectrum of a multiplication operator by a continuous function on a [[compact space]] is the union of the pointwise spectra.

=--

+-- {: .num_defn #BlochHamiltonian}
###### Definition
**(Bloch Hamiltonian)**

The function $H(-) \colon \widehat{T}{}^d \to \mathrm{Herm}(N)$ in Prop. \ref{BlochTheoremForTightBindingModels} is called the *Bloch Hamiltonian* of the tight-binding Hamiltonian $H$.

Conversely, the hopping matrices are recovered from the Bloch Hamiltonian as its Fourier coefficients

$$
  h(a)
    \;=\;
  \int_{\widehat{T}{}^d} e^{i k \cdot a}\, H(k)\, d k
  \,,
$$

so that tight-binding Hamiltonians are in [[bijection]] with (essentially bounded, measurable) Bloch Hamiltonians.

=--

+-- {: .num_prop #RegularityOfBlochHamiltonians}
###### Proposition
**(locality of hopping is regularity of the Bloch Hamiltonian)**

Under the bijection of Def. \ref{BlochHamiltonian}, the hopping (Def. \ref{TightBindingHamiltonian}) is:

* *of finite range* $\;\Leftrightarrow\;$ the Bloch Hamiltonian is a trigonometric polynomial (in particular [[real analytic function|real analytic]]);

* *exponentially decaying* $\;\Leftrightarrow\;$ the Bloch Hamiltonian is [[real analytic function|real analytic]] (and then it extends [[holomorphic function|holomorphically]] to a strip $\vert \mathrm{Im}(k) \vert \lt \beta$);

* *rapidly decaying* $\;\Leftrightarrow\;$ the Bloch Hamiltonian is [[smooth function|smooth]];

* *summable* $\;\Rightarrow\;$ the Bloch Hamiltonian is [[continuous function|continuous]].

=--

+-- {: .proof}
###### Proof

These are standard facts about [[Fourier series]] on the torus $\widehat{T}{}^d$: smoothness corresponds to rapid decay of Fourier coefficients via integration by parts; and real analyticity corresponds to exponential decay via the holomorphic extension of the Fourier series to a complex strip and shifting the integration contour in the formula for $h(a)$ (Def. \ref{BlochHamiltonian}) into that strip.

=--

In practice, physically admissible Bloch Hamiltonians are thus real-analytic, if not trigonometric polynomials. For deformation-theoretic questions, however, this regularity is immaterial (Prop. \ref{RegularityIsImmaterialForDeformationClasses} below).

+-- {: .num_remark #ConventionsForBlochHamiltonians}
###### Remark
**(periodic vs. non-periodic convention)**

If the orbital $i$ sits at position $r_i$ within the unit cell, part of the physics literature uses instead of $H(k)$ (Prop. \ref{BlochTheoremForTightBindingModels}) the matrices

$$
  \widetilde{H}(k)_{i j}
    \;\coloneqq\;
  \underset{a \in \Lambda}{\sum}
  e^{- i k \cdot (a + r_i - r_j)}\, h_{i j}(a)
  \,,
  \;\;\;\;\;\;
  \text{hence}
  \;\;\;\;\;\;
  \widetilde{H}(k) \;=\; D(k)\, H(k)\, D(k)^\dagger
  \,,
  \;\;\;
  D(k) \;\coloneqq\; \mathrm{diag}\big( e^{- i k \cdot r_1}, \cdots, e^{-i k \cdot r_N} \big)
  \,,
$$

which have the same spectrum but are *not* periodic in $k$ (see [Bena & Montambaux 2009](#BenaMontambaux09) for discussion in the example of [[graphene]]): instead $\widetilde{H}(k + G) = D(G)\, \widetilde{H}(k)\, D(G)^\dagger$ for $G \in \Lambda^\ast$.

So $\widetilde{H}$ is not a function on the Brillouin torus but a section of a (here: trivialized) bundle of matrix algebras over it. Only the periodic convention of Prop. \ref{BlochTheoremForTightBindingModels} exhibits the Bloch Hamiltonian as a map out of the Brillouin torus. The same issue reappears for continuum models in Rem. \ref{TwistedPeriodicity} below.

=--


### Gapped Bloch Hamiltonians
 {#GappedBlochHamiltonians}

+-- {: .num_defn #GappedHamiltonians}
###### Definition
**(gapped Bloch Hamiltonians)**

For $\mu \in \mathbb{R}$ (the [[Fermi energy]]) and $n \in \{0, \cdots, N\}$ write

$$
  \mathrm{Herm}_\mu(N)
    \;\coloneqq\;
  \big\{
    A \in \mathrm{Herm}(N)
    \,\big\vert\,
    \mu \notin \sigma(A)
  \big\}
    \;=\;
  \overset{N}{\underset{n = 0}{\coprod}}\,
  \mathrm{Herm}^{(n)}_\mu(N)
$$

for the [[open subspace]] of [[Hermitian matrices]] with a [[spectral gap]] at $\mu$, decomposed according to the number $n$ of eigenvalues below $\mu$ (counted with multiplicity).

A continuous Bloch Hamiltonian $H(-)$ (Def. \ref{BlochHamiltonian}) is *gapped at $\mu$* if it takes values in $\mathrm{Herm}_\mu(N)$, hence, by [[connected space|connectedness]] of $\widehat{T}{}^d$, in $\mathrm{Herm}^{(n)}_\mu(N)$ for a fixed $n$. In this case $n$ is the number of *valence bands* (filled bands) and $N - n$ the number of *conduction bands*.

By [[compact space|compactness]] of $\widehat{T}{}^d$ and Prop. \ref{BlochTheoremForTightBindingModels}, $H(-)$ is gapped at $\mu$ iff $\mu \notin \sigma(H)$, i.e. iff the crystal is a band [[insulator]] at Fermi energy $\mu$.

=--

+-- {: .num_prop #SpaceOfGappedBlochHamiltonians}
###### Proposition
**(space of gapped Hamiltonians is a union of Grassmannians)**

The map

$$
  \array{
    \mathrm{Herm}^{(n)}_\mu(N)
    &\overset{P_{\lt \mu}}{\longrightarrow}&
    \mathrm{Gr}_n\big(\mathbb{C}^N\big)
    \\
    A &\mapsto& \mathrm{im}\big(P_{\lt \mu}(A)\big)
  }
$$

which sends a gapped Hermitian matrix to the image of its [[spectral projection]] onto the eigenvalues below $\mu$, regarded as a point in the [[Grassmannian]] $\mathrm{Gr}_n(\mathbb{C}^N) \simeq U(N)/\big(U(n) \times U(N-n)\big)$, is a [[homotopy equivalence]]. In fact it exhibits a [[deformation retraction]] onto the subspace of *flattened Hamiltonians* $\big\{\mu \cdot 1 + 1 - 2 P \,\big\vert\, P \in \mathrm{Gr}_n(\mathbb{C}^N)\big\}$, via the homotopy

$$
  A_t
    \;\coloneqq\;
  (1 - t) \cdot A
    \,+\,
  t \cdot \big( \mu \cdot 1 + 1 - 2 P_{\lt \mu}(A) \big)
  \,,
  \;\;\;\;\;
  t \in [0,1]
  \,.
$$

Accordingly, a gapped Bloch Hamiltonian $\widehat{T}{}^d \to \mathrm{Herm}^{(n)}_\mu(N)$ is, up to homotopy, equivalently a map $\widehat{T}{}^d \to \mathrm{Gr}_n(\mathbb{C}^N)$, hence a rank $n$ [[subbundle]] of the [[trivial vector bundle]] $\widehat{T}{}^d \times \mathbb{C}^N$: the *valence bundle* $\mathcal{V} \to \widehat{T}{}^d$ with fibers $\mathcal{V}_k = \mathrm{im}\big(P_{\lt \mu}(H(k))\big)$.

=--

+-- {: .proof}
###### Proof

Since the spectrum of $A$ stays away from $\mu$ under small perturbations, the spectral projection is given locally by the Riesz projection formula

$$
  P_{\lt \mu}(A)
    \;=\;
  \frac{1}{2\pi i}
  \oint_C (z - A)^{-1} \, d z
$$

for a fixed contour $C$ enclosing the eigenvalues below $\mu$, and is hence continuous (even real analytic) in $A$. The matrix $A_t$ commutes with $A$ and has eigenvalues $(1-t)\lambda + t(\mu \mp 1)$ for each eigenvalue $\lambda \lt \mu$ (resp. $\lambda \gt \mu$) of $A$, which remain on the same side of $\mu$ for all $t \in [0,1]$. Hence $A_t \in \mathrm{Herm}^{(n)}_\mu(N)$, with $A_0 = A$ and with $A_1$ the flattened Hamiltonian corresponding to $P_{\lt \mu}(A)$, which is fixed throughout if $A$ is already flat.

=--

+-- {: .num_prop #RegularityIsImmaterialForDeformationClasses}
###### Proposition
**(regularity is immaterial for deformation classes)**

1. Every continuous gapped Bloch Hamiltonian is homotopic, through gapped Bloch Hamiltonians, to one that is a trigonometric polynomial (hence comes from finite-range hopping, Prop. \ref{RegularityOfBlochHamiltonians}).

1. If two trigonometric-polynomial gapped Bloch Hamiltonians are continuously homotopic through gapped Bloch Hamiltonians, then they are so through trigonometric-polynomial gapped Bloch Hamiltonians.

Hence (with Prop. \ref{SpaceOfGappedBlochHamiltonians}) the deformation classes of gapped tight-binding Hamiltonians --- whether of finite-range, exponentially decaying, rapidly decaying or just summable hopping --- are the [[homotopy classes]] of maps

$$
  \pi_0
  \,
  \mathrm{Map}\big(
    \widehat{T}{}^d
    ,\,
    \mathrm{Herm}^{(n)}_\mu(N)
  \big)
    \;\simeq\;
  \Big[
    \widehat{T}{}^d
    ,\,
    \mathrm{Gr}_n\big(\mathbb{C}^N\big)
  \Big]
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since $\mathrm{Herm}_\mu(N) \subset \mathrm{Herm}(N)$ is [[open subset|open]], every [[compact subset]] $K \subset \mathrm{Herm}_\mu(N)$ has positive distance $\delta_K$ from its complement; so any two maps into $K$ at uniform distance $\lt \delta_K$ are connected by the straight-line homotopy within $\mathrm{Herm}_\mu(N)$. Now the Fejér means (convolution with the $d$-fold product of Fejér kernels) of a continuous function on $\widehat{T}{}^d$ are trigonometric polynomials, preserve Hermiticity, and converge uniformly; and for a homotopy $\widehat{T}{}^d \times [0,1] \to \mathrm{Herm}_\mu(N)$ they do so uniformly also in the homotopy parameter, by equicontinuity. Applying this to a given map or homotopy, and then joining endpoints by straight-line homotopies (which preserve the property of being a trigonometric polynomial) yields the claim.

=--

+-- {: .num_remark #KTheoryClassification}
###### Remark
**(K-theory classification and symmetries)**

* By Prop. \ref{SpaceOfGappedBlochHamiltonians}, the deformation class of a gapped Bloch Hamiltonian determines the [[isomorphism class]] of its valence bundle. Allowing to add further bands far below or above $\mu$ ("stable equivalence"), hence passing to the limit $n, N - n \to \infty$, the [[classifying space]] becomes $\mathbb{Z} \times B U$ and stable deformation classes of gapped Bloch Hamiltonians are classified by the [[topological K-theory]] of the Brillouin torus:

  $$
    \big[
      \widehat{T}{}^d
      ,\,
      \mathbb{Z} \times B U
    \big]
      \;\simeq\;
    K^0\big(\widehat{T}{}^d\big)
    \,,
    \;\;\;\;\;\;
    H(-) \;\mapsto\; [\mathcal{V}]
    \,.
  $$

  This is the case of "class A" in the [[K-theory classification of topological phases of matter]] ([Kitaev 2009](#Kitaev09), [Freed & Moore 2013](#FreedMoore13), [Thiang 2016](#Thiang16)).

* For $d \leq 3$, complex vector bundles over $\widehat{T}{}^d$ are classified by their rank and their [[first Chern class]] $c_1 \in H^2\big(\widehat{T}{}^d; \mathbb{Z}\big) \simeq \mathbb{Z}^{d(d-1)/2}$. For $d = 2$ this is a single integer, the *Chern number*, which is proportional to the [[quantum Hall effect|quantized Hall conductance]] of the insulator ([TKNN 1982](#TKNN82)). Insulators with non-vanishing Chern number are called *[[Chern insulators]]*.

* In the presence of further [[symmetries]] the Bloch Hamiltonian is constrained to be [[equivariant function|equivariant]]. For example, an [[antiunitary operator|anti-unitary]] [[time-reversal symmetry]] $\Theta = U \circ \mathcal{K}$ (with $\mathcal{K}$ complex conjugation) requires $U\, \overline{H(k)}\, U^\dagger = H(-k)$, so that $H(-)$ becomes equivariant with respect to the [[involution]] $k \mapsto -k$ on the Brillouin torus. Accordingly, deformation classes are then classified by variants of [[KR-theory]], giving the "tenfold way" ([Kitaev 2009](#Kitaev09), [Chiu, Teo, Schnyder & Ryu 2016](#ChiuTeoSchnyderRyu16)), and, in the presence of crystallographic point group symmetries, by [[twisted equivariant K-theory]] ([Freed & Moore 2013](#FreedMoore13), [Thiang 2016](#Thiang16)).

=--


### For Schrödinger operators with periodic potential
 {#ForSchroedingerOperators}

+-- {: .num_prop #BlochFloquetDecomposition}
###### Proposition
**(Bloch-Floquet decomposition)**

Let $V \colon \mathbb{R}^d \to \mathbb{R}$ be a $\Lambda$-periodic [[potential energy|potential]], $V(x + a) = V(x)$ for $a \in \Lambda$, which is bounded (or more generally suitably locally integrable, see [Reed & Simon 1978, §XIII.16](#ReedSimon78)), and consider the [[Schrödinger operator]]

$$
  H
    \;=\;
  - \frac{\hbar^2}{2 m_e}\, \Delta \,+\, V
$$

on $L^2(\mathbb{R}^d)$. Then:

1. The *Bloch-Floquet transform* (also: *Zak transform*), given on [[Schwartz functions]] by

   $$
     (U \psi)_k(x)
       \;\coloneqq\;
     \underset{a \in \Lambda}{\sum}
       e^{- i k \cdot (x + a)}\, \psi(x + a)
     \,,
     \;\;\;\;\;
     k, x \in \mathbb{R}^d
     \,,
   $$

   produces functions $(U\psi)_k$ which are $\Lambda$-periodic in $x$ and satisfy $(U \psi)_{k + G} = e^{- i G \cdot x} (U \psi)_k$ for $G \in \Lambda^\ast$. It extends to a [[unitary operator]] onto a [[direct integral]] of [[Hilbert spaces]]

   $$
     U
       \;\colon\;
     L^2(\mathbb{R}^d)
       \xrightarrow{\;\sim\;}
     \int^\oplus_B L^2\big(\mathbb{R}^d/\Lambda\big)\, d k
   $$

   with inverse $\psi(x) = \int_B e^{i k \cdot x}\, (U \psi)_k(x)\, d k$.

1. This transform decomposes $H$ into fiber operators:

   $$
     U H U^{-1}
       \;=\;
     \int^\oplus_B H(k)\, d k
     \,,
     \;\;\;\;\;\;
     H(k)
       \;\coloneqq\;
     \frac{\hbar^2}{2 m_e} \big( - i \nabla + k \big)^2 \,+\, V
     \,,
   $$

   where $H(k)$ acts on $L^2\big(\mathbb{R}^d/\Lambda\big)$ (i.e. with periodic boundary conditions on the unit cell), being self-adjoint on the [[Sobolev space]] $H^2\big(\mathbb{R}^d/\Lambda\big)$.

1. Each $H(k)$ is bounded below and has compact resolvent, hence purely discrete spectrum $E_1(k) \leq E_2(k) \leq \cdots \to \infty$ (eigenvalues ordered and counted with multiplicity).

1. The family $k \mapsto H(k)$ extends to an entire analytic family of type (A) (in the sense of [[Tosio Kato|Kato]]) on $\mathbb{C}^d$, and satisfies

   $$
     H(k + G)
       \;=\;
     \tau_G \, H(k) \, \tau_G^{-1}
     \,,
     \;\;\;\;\;
     \tau_G \;\coloneqq\; e^{- i G \cdot x}
     \,,
     \;\;\;
     G \in \Lambda^\ast
     \,.
   $$

   Hence the band functions $E_n$ are continuous and $\Lambda^\ast$-periodic, thus descend to continuous functions on the Brillouin torus $\widehat{T}{}^d$ (and they are real analytic wherever $E_n(k)$ is a simple eigenvalue).

1. The spectrum of $H$ is the union of the energy bands:

   $$
     \sigma(H)
       \;=\;
     \underset{n \in \mathbb{N}}{\bigcup}\, E_n\big(\widehat{T}{}^d\big)
     \,,
   $$

   a union of closed intervals, possibly separated by *band gaps*.

=--

See [Reed & Simon 1978, §XIII.16](#ReedSimon78) and [Kuchment 2016](#Kuchment16). Moreover, under mild conditions on $V$, the spectrum of $H$ is purely absolutely continuous, i.e. there are no flat bands ([Thomas 1973](#Thomas73), see [Kuchment 2016](#Kuchment16) for the general situation).

+-- {: .num_prop #BlochTheoremForSchroedingerOperators}
###### Corollary
**(Bloch's theorem)**

In the situation of Prop. \ref{BlochFloquetDecomposition}, for every $k \in \mathbb{R}^d$ and $n \in \mathbb{N}$, let $u_{n,k}$ be an eigenfunction of $H(k)$ for the eigenvalue $E_n(k)$. Then the *Bloch wave*

$$
  \psi_{n,k}(x)
    \;\coloneqq\;
  e^{i k \cdot x}\, u_{n,k}(x)
$$

is a generalized eigenfunction of $H$,

$$
  H \psi_{n,k} \;=\; E_n(k)\, \psi_{n,k}
  \,,
  \;\;\;\;\;\;
  \psi_{n,k}(x + a) \;=\; e^{i k \cdot a}\, \psi_{n,k}(x)
  \;\;\;
  \text{for}\; a \in \Lambda
  \,,
$$

and every $\psi \in L^2(\mathbb{R}^d)$ is a superposition of Bloch waves:

$$
  \psi(x)
    \;=\;
  \underset{n}{\sum}
  \int_B
    c_n(k)\, \psi_{n,k}(x)
  \, d k
  \,,
  \;\;\;\;\;
  c_n(k) \;=\; \big\langle u_{n,k} ,\, (U\psi)_k \big\rangle
  \,.
$$

=--

+-- {: .num_remark #TwistedPeriodicity}
###### Remark
**(twisted periodicity)**

In contrast to the tight-binding case (Prop. \ref{BlochTheoremForTightBindingModels}), the fiber operators $H(k)$ in Prop. \ref{BlochFloquetDecomposition} are not periodic in $k$, but only up to unitary conjugation by $\tau_G$. One may instead use the functions $e^{i k \cdot x}\, (U\psi)_k(x)$, which are $\Lambda^\ast$-periodic in $k$, but these are quasi-periodic in $x$, so that the fiber Hilbert spaces $\big\{ \phi \,\big\vert\, \phi(x + a) = e^{i k \cdot a} \phi(x) \big\}$ now depend on $k$. Either way, $H$ decomposes not into a function on the Brillouin torus but into a section of an operator bundle over the Brillouin torus. (This is the continuum analog of Rem. \ref{ConventionsForBlochHamiltonians}.)

A function on the Brillouin torus is obtained only after choosing a [[trivial bundle|trivialization]], which for isolated families of bands is the content of the following.

=--

+-- {: .num_defn #BlochBundle}
###### Definition
**(isolated bands and Bloch bundle)**

In the situation of Prop. \ref{BlochFloquetDecomposition}, a family of $N$ consecutive bands $E_m, \cdots, E_{m + N - 1}$ is called *isolated* if for all $k$ we have $E_{m-1}(k) \lt E_m(k)$ (if $m \gt 1$) and $E_{m+N-1}(k) \lt E_{m+N}(k)$; by compactness of $\widehat{T}{}^d$ the corresponding gaps are then bounded away from zero. In this case the spectral projections

$$
  P(k)
    \;\coloneqq\;
  \frac{1}{2\pi i}
  \oint_{C} \big(z - H(k)\big)^{-1}\, d z
$$

(for $C$ a contour enclosing exactly $E_m(k), \cdots, E_{m + N - 1}(k)$, which may be held fixed locally in $k$) form a real analytic family of rank $N$ projections with $P(k + G) = \tau_G\, P(k)\, \tau_G^{-1}$.

The *Bloch bundle* of the isolated family is the resulting rank $N$ real analytic Hermitian [[vector bundle]] over the Brillouin torus:

$$
  \mathcal{E}
    \;\coloneqq\;
  \Big\{
    (k, u) \in \mathbb{R}^d \times L^2\big(\mathbb{R}^d/\Lambda\big)
    \;\Big\vert\;
    u \in \mathrm{im}\, P(k)
  \Big\}
  \Big/
  \big(
    (k, u) \sim (k + G, \tau_G u)
  \big)_{G \in \Lambda^\ast}
  \;\;
  \longrightarrow
  \;\;
  \widehat{T}{}^d
  \,.
$$

=--

+-- {: .num_prop #TrivialityOfBlochBundles}
###### Proposition
**(triviality of Bloch bundles)**

If $d \leq 3$ and $H$ is [[time-reversal symmetry|time-reversal symmetric]] (as is the case for $H$ as in Prop. \ref{BlochFloquetDecomposition}, with real potential and no magnetic field), then the Bloch bundle (Def. \ref{BlochBundle}) of every isolated family of bands is trivializable, even real-analytically.

=--

This is due to [Panati 2007](#Panati07), building on [Nenciu 1983](#Nenciu83), see also [Brouder et al. 2007](#BrouderEtAl07). The idea is that time-reversal symmetry implies $c_1(\mathcal{E}) = - c_1(\mathcal{E})$, hence $c_1(\mathcal{E}) = 0$, while for $d \leq 3$ the first Chern class is the only obstruction to triviality (cf. Rem. \ref{KTheoryClassification}).

+-- {: .num_prop #ReductionToTightBinding}
###### Proposition
**(isolated bands are tight-binding models)**

Given an isolated family of $N$ bands (Def. \ref{BlochBundle}) with real-analytically trivializable Bloch bundle, choose a real-analytic orthonormal frame, i.e. real-analytic maps $u_1, \cdots, u_N \colon \mathbb{R}^d \to L^2\big(\mathbb{R}^d/\Lambda\big)$ such that $\big(u_{j,k}\big)_{j = 1}^N$ is an [[orthonormal basis]] of $\mathrm{im}\, P(k)$ and $u_{j, k + G} = \tau_G\, u_{j,k}$. Then:

1. The matrices

   $$
     H_{\mathcal{E}}(k)_{i j}
       \;\coloneqq\;
     \big\langle u_{i,k} ,\, H(k)\, u_{j,k} \big\rangle
   $$

   are $\Lambda^\ast$-periodic in $k$ and hence constitute a real-analytic Bloch Hamiltonian

   $$
     H_{\mathcal{E}} \;\colon\; \widehat{T}{}^d \longrightarrow \mathrm{Herm}(N)
   $$

   (Def. \ref{BlochHamiltonian}), whose eigenvalues at $k$ are $E_m(k), \cdots, E_{m+N-1}(k)$.

1. The *[[Wannier functions]]*

   $$
     w_{j,a}
       \;\coloneqq\;
     U^{-1}\big( k \mapsto e^{- i k \cdot a}\, u_{j,k} \big)
     \,,
     \;\;\;\;\;\;
     \text{i.e.}
     \;\;\;
     w_{j,a}(x)
       \;=\;
     \int_B e^{i k \cdot (x - a)}\, u_{j,k}(x)\, d k
     \,,
   $$

   for $j \in \{1, \cdots, N\}$ and $a \in \Lambda$, form an [[orthonormal basis]] of the band subspace $P L^2(\mathbb{R}^d)$, where $P \coloneqq U^{-1} \big(\int^\oplus_B P(k)\, d k\big) U$. They are lattice translates of each other, $w_{j,a}(x) = w_{j,0}(x - a)$, and are exponentially localized.

1. The unitary isomorphism

   $$
     \array{
       \ell^2\big(\Lambda;\, \mathbb{C}^N\big)
       &\xrightarrow{\;\sim\;}&
       P L^2\big(\mathbb{R}^d\big)
       \\
       \delta_a \otimes e_j &\mapsto& w_{j,a}
     }
   $$

   identifies the band-projected Hamiltonian $P H P$ with the tight-binding Hamiltonian (Def. \ref{TightBindingHamiltonian}) whose Bloch Hamiltonian is $H_{\mathcal{E}}$, hence with exponentially decaying hopping matrices

   $$
     h(a)_{i j}
       \;=\;
     \big\langle w_{i,a} ,\, H\, w_{j,0} \big\rangle
       \;=\;
     \int_{\widehat{T}{}^d} e^{i k \cdot a}\, H_{\mathcal{E}}(k)_{i j}\, d k
     \,.
   $$

=--

+-- {: .proof}
###### Proof

Periodicity of $H_{\mathcal{E}}$ follows since $\tau_G$ is unitary and intertwines $H(k)$ with $H(k+G)$ (Prop. \ref{BlochFloquetDecomposition}). From $U(T_a \psi)_k = e^{- i k \cdot a}\, (U\psi)_k$ (with $(T_a \psi)(x) = \psi(x - a)$) one gets $w_{j,a} = T_a w_{j,0}$ and

$$
  \big\langle w_{i,a} ,\, w_{j,b} \big\rangle
    \;=\;
  \int_B e^{i k \cdot (a - b)} \big\langle u_{i,k} ,\, u_{j,k} \big\rangle\, d k
    \;=\;
  \delta_{i j}\, \delta_{a b}
  \,,
$$

and similarly for the matrix elements of $H$. Exponential localization of the $w_{j,a}$ follows from real analyticity of the frame as in Prop. \ref{RegularityOfBlochHamiltonians}.

=--

+-- {: .num_remark #BlochHamiltoniansOfElectronsInCrystals}
###### Remark
**(Bloch Hamiltonians of electrons in crystals)**

In summary, the Hamiltonian of a single [[electron]] in a [[crystal]], restricted to any isolated family of $N$ bands with trivializable Bloch bundle --- such as any isolated family of bands in a time-reversal symmetric crystal in $d \leq 3$ (Prop. \ref{TrivialityOfBlochBundles}) --- is equivalently a real-analytic Bloch Hamiltonian

$$
  H_{\mathcal{E}}
    \;\colon\;
  \widehat{T}{}^d \longrightarrow \mathrm{Herm}(N)
$$

(Prop. \ref{ReductionToTightBinding}), unique up to "gauge transformations" $H_{\mathcal{E}}(k) \mapsto g(k)\, H_{\mathcal{E}}(k)\, g(k)^\dagger$ by real-analytic $g \colon \widehat{T}{}^d \to U(N)$, corresponding to the choice of frame (which do not change the isomorphism class of the valence bundle). If the Fermi energy $\mu$ lies in a gap within this family of bands, then $H_{\mathcal{E}}$ takes values in the space $\mathrm{Herm}^{(n)}_\mu(N) \simeq \mathrm{Gr}_n(\mathbb{C}^N)$ of gapped Hamiltonians (Prop. \ref{SpaceOfGappedBlochHamiltonians}), and its deformation class, which may be represented by finite-range hopping (Prop. \ref{RegularityIsImmaterialForDeformationClasses}), is classified by topological K-theory (Rem. \ref{KTheoryClassification}).

On the other hand, if the Bloch bundle of the family of bands under consideration is non-trivial (which requires broken time-reversal symmetry if $d \leq 3$, e.g. by magnetic fields), then this family admits no basis of exponentially localized Wannier functions ([Brouder et al. 2007](#BrouderEtAl07)). But a larger isolated family containing it (e.g. valence and conduction bands together) may have trivial Bloch bundle, in which case the original family appears as a non-trivial valence bundle of a tight-binding model as above. This is how [[Chern insulators]] are realized by tight-binding models.

=--


### Wannier functions
 {#WannierFunctions}

The functions $w_{j,a}$ in Prop. \ref{ReductionToTightBinding} are called *Wannier functions* ([Wannier 1937](#Wannier37)). Under the Bloch-Floquet transform, they are dual to frames of the Bloch bundle, and their spatial localization is dual to the regularity of the frame in $k$: Wannier functions are exponentially localized iff the frame is real analytic (Prop. \ref{RegularityOfBlochHamiltonians}). The existence of exponentially localized Wannier functions was established by [Kohn 1959](#Kohn59Analytic) for $d = 1$, by [des Cloizeaux 1964](#desCloizeaux64) and [Nenciu 1983](#Nenciu83) for single isolated bands, and by [Brouder et al. 2007](#BrouderEtAl07) and [Panati 2007](#Panati07) for composite families of bands (in $d \leq 3$, under time-reversal symmetry).

Since the frame is unique only up to gauge transformations $g \colon \widehat{T}{}^d \to U(N)$, so are the Wannier functions, and choosing them "maximally localized" is a standard problem in computational solid state physics ([Marzari & Vanderbilt 1997](#MarzariVanderbilt97), [Marzari et al. 2012](#MarzariEtAl12)).


## Variants and generalizations

* **Time-periodic Hamiltonians.** The analog of Bloch theory for Hamiltonians periodic in time is [[Floquet theory]] ([Floquet 1883](#Floquet1883)).

* **Magnetic fields.** In the presence of a uniform [[magnetic field]] the lattice translations commute with the Hamiltonian only up to phases, i.e. they form a [[projective representation]] of $\Lambda$, the *magnetic translations* ([Zak 1964](#Zak64)). For rational magnetic flux per unit cell, Bloch theory applies to a correspondingly enlarged *magnetic unit cell*. For effective Hamiltonians of Bloch electrons in electric and magnetic fields see [Kohn 1959](#Kohn59Magnetic), [Wannier 1960](#Wannier60), [Panati, Spohn & Teufel 2003](#PanatiSpohnTeufel03).

* **Hyperbolic lattices.** For lattices in [[hyperbolic space]] the translation group is a non-abelian [[Fuchsian group]]. Its 1-dimensional unitary representations form a torus of dimension $2g$ (with $g$ the [[genus of a surface|genus]] of the compactified unit cell), on which an abelian Bloch theory applies, while the higher-dimensional representations lead to "non-abelian Bloch states" ([Maciejko & Rayan 2021](#MaciejkoRayan21), [2022](#MaciejkoRayan22), [Attar & Boettcher 2022](#AttarBoettcher22)).

* **Interacting electrons.** For multi-electron systems the simultaneous translation of all electrons by lattice vectors still commutes with the Hamiltonian, so that many-body eigenstates may be labeled by their total crystal momentum (see the [references below](#ReferencesInteracting)).


## Related concepts

* [[solid state physics]]

* [[crystal]]

* [[electron band theory]]

* [[Brillouin torus]]

* [[Pontrjagin duality]], [[Fourier transform]]

* [[direct integral]]

* [[Floquet theory]]

* [[semiconductor]]

* [[topological insulator]], [[Chern insulator]]

* [[Berry connection]]

* [[K-theory classification of topological phases of matter]]


## References

### Original articles
 {#ReferencesOriginal}

The analogous theorem for ordinary differential equations with time-periodic coefficients:

* {#Floquet1883} Gaston Floquet: *Sur les équations différentielles linéaires à coefficients périodiques*, Annales scientifiques de l'École Normale Supérieure, Série 2, **12** (1883) 47-88 &lbrack;[doi:10.24033/asens.220](https://doi.org/10.24033/asens.220)&rbrack;

The original article on Bloch's theorem, including the tight-binding approximation:

* {#Bloch29} [[Felix Bloch]]: *Über die Quantenmechanik der Elektronen in Kristallgittern*, Zeitschrift für Physik **52** 7-8 (1929) 555-600 &lbrack;[doi:10.1007/BF01339455](https://doi.org/10.1007/BF01339455)&rbrack;

Introducing Brillouin zones:

* {#Brillouin30} [[Léon Brillouin]]: *Les électrons libres dans les métaux et le role des réflexions de Bragg*, J. Phys. Radium **1** (1930) 377-400 &lbrack;[doi:10.1051/jphysrad:01930001011037700](https://doi.org/10.1051/jphysrad:01930001011037700)&rbrack;


### Textbook accounts
 {#ReferencesTextbooks}

In [[solid state physics]]:

* {#AshcroftMermin76} Neil W. Ashcroft, N. David Mermin: Ch. 8 (and Ch. 10 for the tight-binding method) of: *Solid State Physics*, Holt, Rinehart and Winston (1976)

* {#Kittel05} Charles Kittel: Ch. 7 of: *Introduction to Solid State Physics*, Wiley (8th ed. 2005)

* {#Li06} [[Sheng San Li]]: Section 4.3 of: *Semiconductor Physical Electronics*, Springer (2006) &lbrack;[doi:10.1007/0-387-37766-2_4](https://doi.org/10.1007/0-387-37766-2_4)&rbrack;

* {#Vanderbilt18} [[David Vanderbilt]]: Ch. 2 of: *Berry Phases in Electronic Structure Theory -- Electric Polarization, Orbital Magnetization and Topological Insulators*, Cambridge University Press (2018) &lbrack;[doi:10.1017/9781316662205](https://doi.org/10.1017/9781316662205)&rbrack;

In [[mathematical physics]]:

* {#ReedSimon78} [[Michael Reed]], [[Barry Simon]]: Sec. XIII.16 *Schrödinger operators with periodic potentials*, of: *[[Methods of Modern Mathematical Physics]] -- IV: Analysis of Operators*, Academic Press (1978) &lbrack;[ISBN:9780080570457](https://www.elsevier.com/books/iv-analysis-of-operators/reed/978-0-08-057045-7), §XIII.16: [[ReedSimon-XIII16.pdf:file]]&rbrack;

* {#Eastham73} M. S. P. Eastham: *The Spectral Theory of Periodic Differential Equations*, Scottish Academic Press (1973)

* {#Kuchment93} Peter Kuchment: *Floquet Theory for Partial Differential Equations*, Operator Theory: Advances and Applications **60**, Birkhäuser (1993) &lbrack;[doi:10.1007/978-3-0348-8573-7](https://doi.org/10.1007/978-3-0348-8573-7)&rbrack;

* {#Kuchment16} Peter Kuchment: *An overview of periodic elliptic operators*, Bull. Amer. Math. Soc. **53** (2016) 343-414 &lbrack;[arXiv:1510.00971](https://arxiv.org/abs/1510.00971), [doi:10.1090/bull/1528](https://doi.org/10.1090/bull/1528)&rbrack;

On absolute continuity of the spectrum:

* {#Thomas73} Lawrence E. Thomas: *Time dependent approach to scattering from impurities in a crystal*, Commun. Math. Phys. **33** (1973) 335-343 &lbrack;[doi:10.1007/BF01646745](https://doi.org/10.1007/BF01646745)&rbrack;

See also:

* Wikipedia: *[Bloch's theorem](https://en.wikipedia.org/wiki/Bloch%27s_theorem)*

* Wikipedia: *[Crystal momentum](https://en.wikipedia.org/wiki/Crystal_momentum)*

* Wikipedia: *[Tight binding](https://en.wikipedia.org/wiki/Tight_binding)*


### Tight-binding models
 {#ReferencesTightBinding}

Besides [Bloch 1929](#Bloch29) and [Ashcroft & Mermin 1976, Ch. 10](#AshcroftMermin76):

* {#SlaterKoster54} John C. Slater, George F. Koster: *Simplified LCAO Method for the Periodic Potential Problem*, Phys. Rev. **94** (1954) 1498 &lbrack;[doi:10.1103/PhysRev.94.1498](https://doi.org/10.1103/PhysRev.94.1498)&rbrack;

On the periodic vs. non-periodic convention for Bloch Hamiltonians (Rem. \ref{ConventionsForBlochHamiltonians}):

* {#BenaMontambaux09} Cristina Bena, Gilles Montambaux: *Remarks on the tight-binding model of graphene*, New J. Phys. **11** (2009) 095003 &lbrack;[arXiv:0712.0765](https://arxiv.org/abs/0712.0765), [doi:10.1088/1367-2630/11/9/095003](https://doi.org/10.1088/1367-2630/11/9/095003)&rbrack;


### Analyticity and the Bloch bundle
 {#ReferencesAnalyticity}

On analytic dependence of Bloch waves on the crystal momentum, triviality of the Bloch bundle and existence of exponentially localized Wannier functions:

* {#Kohn59Analytic} [[Walter Kohn]]: *Analytic Properties of Bloch Waves and Wannier Functions*, Phys. Rev. **115** (1959) 809 &lbrack;[doi:10.1103/PhysRev.115.809](https://doi.org/10.1103/PhysRev.115.809)&rbrack;

* {#desCloizeaux64} Jacques des Cloizeaux: *Energy Bands and Projection Operators in a Crystal: Analytic and Asymptotic Properties*, Phys. Rev. **135** (1964) A685 &lbrack;[doi:10.1103/PhysRev.135.A685](https://doi.org/10.1103/PhysRev.135.A685)&rbrack;

* Jacques des Cloizeaux: *Analytical Properties of n-Dimensional Energy Bands and Wannier Functions*, Phys. Rev. **135** (1964) A698 &lbrack;[doi:10.1103/PhysRev.135.A698](https://doi.org/10.1103/PhysRev.135.A698)&rbrack;

* {#Nenciu83} Gheorghe Nenciu: *Existence of the exponentially localised Wannier functions*, Commun. Math. Phys. **91** (1983) 81-85 &lbrack;[doi:10.1007/BF01206052](https://doi.org/10.1007/BF01206052)&rbrack;

* {#Panati07} [[Gianluca Panati]]: *Triviality of Bloch and Bloch-Dirac bundles*, Ann. Henri Poincaré **8** (2007) 995-1011 &lbrack;[arXiv:math-ph/0601034](https://arxiv.org/abs/math-ph/0601034), [doi:10.1007/s00023-007-0326-8](https://doi.org/10.1007/s00023-007-0326-8)&rbrack;

* {#BrouderEtAl07} Christian Brouder, [[Gianluca Panati]], Matteo Calandra, Christophe Mourougane, Nicola Marzari: *Exponential localization of Wannier functions in insulators*, Phys. Rev. Lett. **98** (2007) 046402 &lbrack;[arXiv:cond-mat/0606726](https://arxiv.org/abs/cond-mat/0606726), [doi:10.1103/PhysRevLett.98.046402](https://doi.org/10.1103/PhysRevLett.98.046402)&rbrack;


### Effective dynamics of Bloch electrons
 {#ReferencesEffectiveDynamics}

* {#Kohn59Magnetic} [[Walter Kohn]]: *Theory of Bloch Electrons in a Magnetic Field: The Effective Hamiltonian*, Phys. Rev. **115** (1959) 1460 &lbrack;[doi:10.1103/PhysRev.115.1460](https://doi.org/10.1103/PhysRev.115.1460)&rbrack;

* {#Wannier60} [[Gregory H. Wannier]]: *Wave Functions and Effective Hamiltonian for Bloch Electrons in an Electric Field*, Phys. Rev. **117** (1960) 432 &lbrack;[doi:10.1103/PhysRev.117.432](https://doi.org/10.1103/PhysRev.117.432)&rbrack;

* {#Zak64} Joshua Zak: *Magnetic Translation Group*, Phys. Rev. **134** (1964) A1602 &lbrack;[doi:10.1103/PhysRev.134.A1602](https://doi.org/10.1103/PhysRev.134.A1602)&rbrack;

* {#PanatiSpohnTeufel03} [[Gianluca Panati]], Herbert Spohn, [[Stefan Teufel]]: *Effective dynamics for Bloch electrons: Peierls substitution and beyond*, Commun. Math. Phys. **242** (2003) 547-578 &lbrack;[arXiv:math-ph/0212041](https://arxiv.org/abs/math-ph/0212041), [doi:10.1007/s00220-003-0950-1](https://doi.org/10.1007/s00220-003-0950-1)&rbrack;


### Bloch Hamiltonians and topological phases
 {#ReferencesTopologicalPhases}

On Bloch Hamiltonians in the context of [[topological phases of matter]] (see also at *[[K-theory classification of topological phases of matter]]*):

* {#TKNN82} [[David J. Thouless]], Mahito Kohmoto, M. P. Nightingale, M. den Nijs: *Quantized Hall Conductance in a Two-Dimensional Periodic Potential*, Phys. Rev. Lett. **49** (1982) 405 &lbrack;[doi:10.1103/PhysRevLett.49.405](https://doi.org/10.1103/PhysRevLett.49.405)&rbrack;

* {#Kitaev09} [[Alexei Kitaev]]: *Periodic table for topological insulators and superconductors*, AIP Conf. Proc. **1134** (2009) 22-30 &lbrack;[arXiv:0901.2686](https://arxiv.org/abs/0901.2686), [doi:10.1063/1.3149495](https://doi.org/10.1063/1.3149495)&rbrack;

* {#FreedMoore13} [[Daniel Freed]], [[Gregory Moore]]: *Twisted equivariant matter*, Ann. Henri Poincaré **14** (2013) 1927-2023 &lbrack;[arXiv:1208.5055](https://arxiv.org/abs/1208.5055), [doi:10.1007/s00023-013-0236-x](https://doi.org/10.1007/s00023-013-0236-x)&rbrack;

* {#BernevigHughes13} [[B. Andrei Bernevig]], [[Taylor L. Hughes]]: *Topological Insulators and Topological Superconductors*, Princeton University Press (2013) &lbrack;[doi:10.1515/9781400846733](https://doi.org/10.1515/9781400846733)&rbrack;

* {#Thiang16} [[Guo Chuan Thiang]]: *On the K-theoretic classification of topological phases of matter*, Ann. Henri Poincaré **17** (2016) 757-794 &lbrack;[arXiv:1406.7366](https://arxiv.org/abs/1406.7366), [doi:10.1007/s00023-015-0418-9](https://doi.org/10.1007/s00023-015-0418-9)&rbrack;

* {#ChiuTeoSchnyderRyu16} [[Ching-Kai Chiu]], [[Jeffrey C. Y. Teo]], [[Andreas P. Schnyder]], [[Shinsei Ryu]]: *Classification of topological quantum matter with symmetries*, Rev. Mod. Phys. **88** (2016) 035005 &lbrack;[arXiv:1505.03535](https://arxiv.org/abs/1505.03535), [doi:10.1103/RevModPhys.88.035005](https://doi.org/10.1103/RevModPhys.88.035005)&rbrack;

* {#CayssolFuchs21} [[Jérôme Cayssol]], [[Jean-Noël Fuchs]]: Section IV.B of: *Topological and geometrical aspects of band theory*, J. Phys. Mater. **4** (2021) 034007 &lbrack;[arXiv:2012.11941](https://arxiv.org/abs/2012.11941), [doi:10.1088/2515-7639/abf0b5](https://doi.org/10.1088/2515-7639/abf0b5)&rbrack;

* {#Sergeev23} [[Alexander S. Sergeev]]: Section 5.1.3 in: *Topological insulators and geometry of vector bundles*, SciPost Physics Lecture Notes **67** (2023) &lbrack;[arXiv:2011.05004](https://arxiv.org/abs/2011.05004), [doi:10.21468/SciPostPhysLectNotes.67](https://doi.org/10.21468/SciPostPhysLectNotes.67)&rbrack;

* {#SatiSchreiber23} [[Hisham Sati]], [[Urs Schreiber]]: *Anyonic topological order in twisted equivariant differential (TED) K-theory*, Rev. Math. Phys. **35** (2023) 2350001 &lbrack;[arXiv:2206.13563](https://arxiv.org/abs/2206.13563), [doi:10.1142/S0129055X23500010](https://doi.org/10.1142/S0129055X23500010)&rbrack;


### Generalizations
 {#ReferencesGeneralizations}

#### Further discussion

* E. Dobardžić, M. Dimitrijević, M. V. Milovanović: *Generalized Bloch theorem and topological characterization*, Phys. Rev. B **91** (2015) 125424 &lbrack;[arXiv:1411.4920](https://arxiv.org/abs/1411.4920), [doi:10.1103/PhysRevB.91.125424](https://doi.org/10.1103/PhysRevB.91.125424)&rbrack;

#### For hyperbolic lattices
 {#ReferencesHyperbolic}

Variant for lattices in [[hyperbolic spaces]]:

* {#MaciejkoRayan21} Joseph Maciejko, Steven Rayan: *Hyperbolic band theory*, Science Advances **7** 36 (2021) eabe9170 &lbrack;[arXiv:2008.05489](https://arxiv.org/abs/2008.05489), [doi:10.1126/sciadv.abe9170](https://doi.org/10.1126/sciadv.abe9170)&rbrack;

* {#MaciejkoRayan22} Joseph Maciejko, Steven Rayan: *Automorphic Bloch theorems for hyperbolic lattices*, Proc. Natl. Acad. Sci. **119** 9 (2022) e2116869119 &lbrack;[arXiv:2108.09314](https://arxiv.org/abs/2108.09314), [doi:10.1073/pnas.2116869119](https://doi.org/10.1073/pnas.2116869119)&rbrack;

* {#AttarBoettcher22} Adil Attar, Igor Boettcher: *Selberg trace formula in hyperbolic band theory*, Phys. Rev. E **106** (2022) 034114 &lbrack;[arXiv:2201.06587](https://arxiv.org/abs/2201.06587), [doi:10.1103/PhysRevE.106.034114](https://doi.org/10.1103/PhysRevE.106.034114)&rbrack;

#### For interacting electrons
 {#ReferencesInteracting}

* Yuejin Guo, Jean-Marc Langlois, William A. Goddard: *Electronic Structure and Valence-Bond Band Structure of Cuprate Superconducting Materials*, Science **239** 4842 (1988) 896-899 &lbrack;[doi:10.1126/science.239.4842.896](https://doi.org/10.1126/science.239.4842.896), [jstor:1700316](https://www.jstor.org/stable/1700316)&rbrack;

* Jingsan Hu, Jianfei Gu, Weiyi Zhang: *Bloch's band structures of a pair of interacting electrons in simple one- and two-dimensional lattices*, Physics Letters A **414** (2021) 127634 &lbrack;[doi:10.1016/j.physleta.2021.127634](https://doi.org/10.1016/j.physleta.2021.127634)&rbrack;


### Wannier functions
 {#ReferencesWannier}

The original article:

* {#Wannier37} [[Gregory H. Wannier]]: *The Structure of Electronic Excitation Levels in Insulating Crystals*, Phys. Rev. **52** (1937) 191 &lbrack;[doi:10.1103/PhysRev.52.191](https://doi.org/10.1103/PhysRev.52.191)&rbrack;

On their exponential localization see the [references above](#ReferencesAnalyticity).

On maximally localized Wannier functions:

* {#MarzariVanderbilt97} Nicola Marzari, [[David Vanderbilt]]: *Maximally-localized generalized Wannier functions for composite energy bands*, Phys. Rev. B **56** (1997) 12847 &lbrack;[arXiv:cond-mat/9707145](https://arxiv.org/abs/cond-mat/9707145), [doi:10.1103/PhysRevB.56.12847](https://doi.org/10.1103/PhysRevB.56.12847)&rbrack;

* {#MarzariEtAl12} Nicola Marzari, Arash A. Mostofi, Jonathan R. Yates, Ivo Souza, [[David Vanderbilt]]: *Maximally localized Wannier functions: Theory and applications*, Rev. Mod. Phys. **84** (2012) 1419 &lbrack;[arXiv:1112.5411](https://arxiv.org/abs/1112.5411), [doi:10.1103/RevModPhys.84.1419](https://doi.org/10.1103/RevModPhys.84.1419)&rbrack;

In the context of [[fractional Chern insulators]] exhibiting a [[fractional quantum anomalous Hall effect]]:

* [[Xiao-Liang Qi]]: *Generic Wavefunction Description of Fractional Quantum Anomalous Hall States and Fractional Topological Insulators*, Phys. Rev. Lett. **107** (2011) 126803 &lbrack;[arXiv:1105.4298](https://arxiv.org/abs/1105.4298), [doi:10.1103/PhysRevLett.107.126803](https://doi.org/10.1103/PhysRevLett.107.126803)&rbrack;

* [[Maissam Barkeshli]], [[Xiao-Liang Qi]]: *Topological Nematic States and Non-Abelian Lattice Dislocations*, Phys. Rev. X **2** (2012) 031013 &lbrack;[arXiv:1112.3311](https://arxiv.org/abs/1112.3311), [doi:10.1103/PhysRevX.2.031013](https://doi.org/10.1103/PhysRevX.2.031013)&rbrack;

* Chao-Ming Jian, [[Xiao-Liang Qi]]: *Crystal-symmetry preserving Wannier states for fractional Chern insulators*, Phys. Rev. B **88** (2013) 165134 &lbrack;[arXiv:1303.1787](https://arxiv.org/abs/1303.1787), [doi:10.1103/PhysRevB.88.165134](https://doi.org/10.1103/PhysRevB.88.165134)&rbrack;




[[!redirects Bloch theorem]]

[[!redirects Bloch theory]]

[[!redirects Bloch-Floquet theory]]
[[!redirects Floquet-Bloch theory]]

[[!redirects Bloch-Floquet transform]]
[[!redirects Bloch-Floquet transforms]]
[[!redirects Bloch-Floquet decomposition]]
[[!redirects Zak transform]]

[[!redirects Bloch state]]
[[!redirects Bloch states]]

[[!redirects Bloch wave]]
[[!redirects Bloch waves]]

[[!redirects Bloch band]]
[[!redirects Bloch bands]]

[[!redirects crystal momentum]]
[[!redirects crystal momenta]]

[[!redirects quasi-momentum]]
[[!redirects quasi-momenta]]

[[!redirects Bloch Hamiltonian]]
[[!redirects Bloch Hamiltonians]]

[[!redirects Bloch bundle]]
[[!redirects Bloch bundles]]

[[!redirects tight-binding model]]
[[!redirects tight-binding models]]

[[!redirects tight-binding Hamiltonian]]
[[!redirects tight-binding Hamiltonians]]

[[!redirects Wannier function]]
[[!redirects Wannier functions]]

[[!redirects Wannier state]]
[[!redirects Wannier states]]

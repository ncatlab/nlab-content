
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--



\tableofcontents

## Idea

The *Su-Schrieffer-Heeger model* (SSH) is a simple [[spin chain]]-like [[model (in theoretical physics)|model]] for a type of 1-dimensional [[topological insulator]] [[quantum material]]. In [[theoretical physics]] it mainly serves as an instructive toy model example of [[topological phases of matter]], while experimentally it gives an approximate description of the [[electron band]]-structure of materials like molecular trans-polyacetylene chains (which was the original motivation of [Su, Schrieffer & Heeger 1979](#SuSchriefferHeeger79).

As a [[lattice model]], SSH has a unit cell with two sites, traditionally denoted "$A$" and "$B$", hence with a 2-dimensional (2 "[[electron band|band]]") [[Hilbert space]] $\mathscr{H}_n \simeq \mathbb{C}^2 \simeq \mathbb{C}\langle A, B\rangle$ at each site, and the [[Hamiltonian operator]] is the [[sum]] of 

1. an *intracell* hopping term between sites $A$ and $B$ in the same cell 

2. an *extracell* hopping term between the $B$-site of one cell with the $A$-site of the next one. 

The parameter space of the model is that of the [[coefficients]] of these two terms:

* $v \in \mathbb{R}_{\gt 0}$, the intracell hopping strength,

* $w \in \mathbb{R}_{\gt 0}$, the intercell hopping strength.

After [[Fourier transform]], the [[Bloch Hamiltonian]] of the SSH model
\[
  H = 
  \textstyle{\int_{[k] \in S^1}} H_{k}
  \;\in\;
  End\Big(
    \textstyle{\int_{k \in S^1}} \mathbb{C}^2 
  \Big)
\]
is given (up to arbitrary [[energy]] shift and [[unitary transformation]]) by (cf. [Asbóth, Oroszlány & Pályi 2016 (1.18)](#AsbóthOroszlányPályi16), [Batra & Sheet 2020](#BatraSheet20)):
\[
  \label{TheBlochHamiltonian}
  \begin{aligned}
  [k] 
  &\mapsto
  H_{[k]} 
  \\
  &\coloneqq 
  \big(
    v + w \cdot cos(k)
  \big)
  \sigma_x
  + 
  \big(
    w \cdot sin(k)
  \big)
  \sigma_y
  \,,
  \end{aligned}
\]
where $\sigma_{(-)} \in End(\mathbb{C}^2)$ denotes the [[Pauli matrices]].

To note here that these Bloch Hamiltonians $H_{[k]}$ (eq:TheBlochHamiltonian)

1. have no contribution of the [[Pauli matrix]] $\sigma_z$, which more abstractly means that they satisfy "chiral symmetry" in the sense that 

   \[
     \label{ChiralSymmetry}
     \sigma_z H_{[k]} \sigma_z = - H_{[k]}
     \,,
   \]

2. generically have two [[real number|real]] [[eigenvalues]] of opposite sign (labeling the [[valence band]] of negative energy and the [[conduction band]] of positive energy, respectively), except when $H_{[k]} = 0$, where the [[energy gap]] between these eigenvalues closes, which happens when $v = w$.

Hence for $v = w$ the SSH model describes an ordinary [[conductor]] and for $v \neq w$ an [[insulator]]. 

In the latter case there are still two qualitatively different regimes: When $v \lt w$, then the [[Bloch Hamiltonian]] (eq:TheBlochHamiltonian) regarded as a [[map]] to the [[subspace]] of *gapped* and *chiral* (eq:ChiralSymmetry) 2-band Hamiltonians
\[
  \begin{aligned}
  H_{(-)}
  \colon
  S^1 
  &
  \longrightarrow
  End(\mathbb{C}^2)_{gap, chr}
  \\
  &
  \coloneqq
  \left\{
    H \in End(\mathbb{C}^2)
    \,\bigg\vert\,
    \substack{
      H^\dagger = H,\, \sigma_z H \sigma_z = - H
      \\
      Eig_{\gt 0}(H) \simeq \mathbb{C}
      ,\,
      Eig_{\lt 0}(H) \simeq \mathbb{C}
    }
  \right\}
  \\
  &
  \simeq
  \mathbb{R}^2 \setminus \{0\}
  \\
  &
  \underset{hmpty}{\simeq}
  S^1
  \end{aligned}
\]
has a non-trivial [[homotopy class]] and [[unstable classification of topological phases|hence]] describes a [[topological insulator]] [[topological phase of matter|phase]], namely it has [[Hopf degree]] ("winding number") equal to $\pm 1$ (depending on conventions); while for $v \gt w$ the Hopf degree winding number vanishes, which hence describes an ordinary [[insulator]] phase. 

## Related entries

* [[Haldane model]]


## References

The original article:

* {#SuSchriefferHeeger79} W. P. Su, J. R. Schrieffer, A. J. Heeger: *Solitons in Polyacetylene*, Phys. Rev. Lett. **42** (1979) 1698 &lbrack;[doi:10.1103/PhysRevLett.42.1698]( https://doi.org/10.1103/PhysRevLett.42.1698)&rbrack;

Review:

* {#AsbóthOroszlányPályi16} János K. Asbóth, László Oroszlány, András Pályi, Chapter 1 of: *A Short Course on Topological Insulators: Band-structure topology and edge states in one and two dimensions*, Lecture Notes in Physics **919**, Springer (2016) &lbrack;[arXiv:1509.02295](https://arxiv.org/abs/1509.02295), [doi:10.1007/978-3-319-25607-8](https://doi.org/10.1007/978-3-319-25607-8)&rbrack;


* {#BatraSheet20} Navketan Batra, Goutam Sheet: *Understanding Basic Concepts of Topological Insulators Through Su-Schrieffer-Heeger (SSH) Model*, Resonance **25** (2020) 765-786 &lbrack;[arXiv:1906.08435](https://arxiv.org/abs/1906.08435), [doi:10.1007/s12045-020-0995-x](https://doi.org/10.1007/s12045-020-0995-x)&rbrack;

* Weibo Xu: *The Su-Schrieffer-Heeger model on a one-dimensional lattice: Analytical wave functions of topological edge states* &lbrack;[arXiv:2509.16708](https://arxiv.org/abs/2509.16708)&rbrack;

See also:

* Wikipedia: *[Su--Schrieffer--Heeger model](https://en.wikipedia.org/wiki/Su%E2%80%93Schrieffer%E2%80%93Heeger_model)*

[[!redirects Su-Schrieffer-Heeger models]]

[[!redirects Su--Schrieffer--Heeger model]]
[[!redirects Su--Schrieffer--Heeger models]]


[[!redirects SSH model]]
[[!redirects SSH models]]



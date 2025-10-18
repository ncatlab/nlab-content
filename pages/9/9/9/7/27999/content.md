

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
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


\tableofcontents

## Idea

A [[crystal|crystalline]] [[quantum material]] in a [[energy gap|gapped]] [[ground state]] is said to be in a *[[topological phase of matter|topological phase]]* if the [[Bloch Hamiltonian]] [[map]] $H_{(-)} \colon \widehat{T}{}^d \longrightarrow \mathscr{A}$ (from the [[Brillouin torus]] of crystal [[momenta]] to the space $\mathscr{A}$ of accessible individual [[Hamiltonians]] $H_{[\vec k]}$) has a non-trivial [[homotopy class]].

Whether and how this is the case depends crucially on the choice of [[classifying space]] $\mathscr{A}$, which in turn reflects the resolution or accuracy with which the material is measurable in [[experiment]]: The larger $\mathscr{A}$, the more freedom is admitted to the system to transition between topological phases which may be disconnected for smaller choices of $\mathscr{A}$.

In the extreme case one allows the system to undergo deformations during which the [[electrons]] may occupy arbitrarily high [[energy bands]]. This *coarsest* resolution of the situation gives the most *stable* classification. This is the situation most commonly considered, notably in the [[K-theory classification of topological phases of matter]].

All other classifications are *unstable*. In the literature such unstable topological phases have also been called *fragile* or *delicate*.

In mathematical language, unstable topological phased are classified by the ([[equivariant cohomology|equivariant]]) *[[nonabelian cohomology]]*

$$
  H_G\big(\widehat{T}{}^d; \mathscr{A} \big)
  \coloneqq
  \pi_0 Map\big(\widehat{T}{}^d, \mathscr{A} \big)^G
$$

(of the [[Brillouin torus]] with respect to the crystal's [[point group]] $G$) with [[classifying spaces]] $\mathscr{A}$ that are indeed unstable in the sense of [[stable homotopy theory]]: they are not [[infinite loop spaces]] (not stages of [[spectra]] of spaces).


## References

[[!include unstable classification of topological phases -- references]]

[[!redirects unstable topological phases of matter]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[physics]], a *mass term* is, quite generally, the [[sum|summand]] in a [[Lagrangian density]], [[Hamiltonian]] or [[equation of motion]] which expresses the [[mass]] of a given (quasi-)[[particle]] or [[field (physics)|field]].

Often the terminology is used specifically for masses of [[spinors]]/[[Dirac fields]], since here a mass term is subject to subtle constraints which may or may not exclude the mere existence of admissible mass terms.

Schematically, if a massless relativistic [[Dirac equation]] (here in [[Minkowski spacetime]]) is written in the form

$$
  \partial_0 \psi
  \;=\;
  k\!\!\!/ \cdot \psi
  \,,
$$

where $k\!\!\!/$ are the [[Feynman slash|Clifford momentum]]-[[linear operator|operator]], then for a mass term addition

$$
  \partial_0 \psi
  \;=\;
  k\!\!\!/ \cdot \psi
  \;+\;
  m \gamma_0
  \,,
$$

to lead to the required [[special relativity|relativistic]] [[dispersion relation]]

$$
  E \,=\, \sqrt{k^2 + m^2}
$$

one needs that the new [[Clifford algebra|Clifford]]-generator $\gamma_0$ exists as an operator on the given [[Hilbert space]] of [[spinor]] $\psi$ such that it skew-commutes with all the Clifford momenta

$$
  \gamma_0 \cdot k\!\!\!/ 
  \;+\;
  k\!\!\!/\cdot \gamma_0 
  \;=\;
  0
  \,.
$$

This is the kind of condition that also appears in [[Karoubi K-theory|Karoubi]]'s formlation of [[topological K-theory]]-classes as [[equivalence classes]] of  [[Clifford modules]] (see [Freed & Hopkins 2021, Thm. 9.63](#FreedHopkins21)). 

In this guise, mass terms for [[electron]]-excitations in [[semi-metals]] play a role in the [[K-theory classification of topological phases of matter]] (see [below](#ExamplesInTopologicalPhasesOfMatter)).


## Examples

### In particle physics

In [[particle physics]] the (non-)existence of mass terms for [[fermions|fermionic]] [[fundamental particles]] goes along with their characterization as [[Dirac spinors]], [[Weyl spinors]] and [[Majorana spinors]]. 

This plays a central role notably in discussion of the (still hypothetical) detailed nature of [[neutrinos]].



### In topological phases of matter
 {#ExamplesInTopologicalPhasesOfMatter}

In [[solid state physics]] of [[crystals]], [[electrons]] are typically well-approximated by the non-relativistic Dirac equation, but around nodal points in the [[Brillouin torus]], where [[electronic band structure|electron bands]] cross, the effective [[dispersion relation]] is again of form of a relativistic Dirac- or Weyl-equation (whence one speaks of *Dirac points* or *Weyl points*). 

\begin{imagefromfile}
    "file_name": "MassTermsForSemiMetalNodalPoints-220517.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(graphics from [SS22](#SS22))"
\end{imagefromfile}

This phenomenon appears in particular in [[topological semi-metals]], in which case the existence of a mass term, whose addition to the [[dispersion relation]] will remove the band crossing by "opening an energy gap", is thought to signal the decay of the [[semi-metal]]-phase into a [[topological insulator]]-phase. 

See for instance the example of the *[[Haldane model]]*.


## Related concepts

* [[mass]]

* [[mass gap]]

* [[Karoubi K-theory]]

* [[K-theory classification of topological phases of matter]]

## References

A careful discussion of relativistic mass terms is in:

* {#FreedHopkins21} [[Daniel S. Freed]], [[Michael J. Hopkins]], *Reflection positivity and invertible topological phases*, Geom. Topol. **25** (2021) 1165-1330 $[$[arXiv:1604.06527](https://arxiv.org/abs/1604.06527), [doi:10.2140/gt.2021.25.1165](https://doi.org/10.2140/gt.2021.25.1165)$]$


Discussion aimed at the description of [[topological semi-metal]]-phases in [[solid state physics]] includes:

* {#MorimotoFurusaki13} Takahiro Morimoto and Akira Furusaki, Sec. V of: *Topological classification with additional symmetries from Clifford algebras*, Phys. Rev. B **88** (2013) 125129 ([arXiv:1306.2505](https://arxiv.org/abs/1306.2505),  [doi:10.1103/PhysRevB.88.125129](https://doi.org/10.1103/PhysRevB.88.125129))

* {#ChiuSchnyder14} [[Ching-Kai Chiu]], [[Andreas P. Schnyder]], Section A.2 of: *Classification of reflection-symmetry-protected topological semimetals and nodal superconductors*, Phys. Rev. B **90** 205136 (2014) $[$[doi:10.1103/PhysRevB.90.205136](https://doi.org/10.1103/PhysRevB.90.205136)$]$

* {#CTSR15} [[Ching-Kai Chiu]], [[Jeffrey C.Y. Teo]], [[Andreas P. Schnyder]], [[Shinsei Ryu]], Section III.C of *Classification of topological quantum matter with symmetries*, Rev. Mod. Phys. **88** (2016) 035005 ([arXiv:1505.03535](https://arxiv.org/abs/1505.03535), [doi:10.1103/RevModPhys.88.035005](https://doi.org/10.1103/RevModPhys.88.035005))

Some of the above material is taken from:

* {#SS22} [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Topological Quantum Computation in TED-K]]*

[[!redirects mass terms]]


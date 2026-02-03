
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



\tableofcontents


## Idea

What is called the *toric code* &lbrack;[Kitaev 2003](#Kitaev03)&rbrack; is a [[quantum error correction|quantum error]] [[error correcting code|correcting code]] whose [[underlying]] [[Hilbert space]] is that of a collection of [[qubits]] ("spins" as in the [[Ising model]]) arranged on the [[vertices]] of a rectangular 2-dimensional [[lattice (discrete subgroup)|lattice]] with periodic [[boundary conditions]], hence a lattice on a [[torus]] -- a [[surface code]]. (If the periodic boundary conditions are disregarded one speaks of a *planar code* or *surface code* and here specifically of the *Kitaev surface code*).

The code subspace of Kitaev's toric code (the subspace whose elements are regarded as error-free quantum states) is the [[kernel]] of an operator that may be thought of as the [[Hamiltonian]] of a hypothetical [[quantum system]] (a lattice-spin model as often considered in [[solid state physics]] akin to the [[Ising model]]) featuring next-to-nearest neighbour interactions of the qubits/spins via [[Pauli operators]]. Therefore one may think of the physical qbits of the toric code as forming the [[ground state]] of this system and of errors to them as the excitations above the ground state.

(The actual physical realization of the toric code Hamiltonian has remained elusive even besides the question of modelling periodic boundary conditions, cf. e.g. [Nussinov & Ortiz 2008](#NussinovOrtiz08), [VLV21](#VLV21).)

This hypothetical [[quantum system]] exhibits a simple form of [[topological order]] in that the local errors happen to look like the creation of [[anyons]] out of the [[vacuum]], the [[quantum error correction|error correction]] looks like moving these anyons back intoeach other for them to annihilate, and the failure of error correction through the code corresponds to these anyons undergoing non-trivial [[braiding]] before re-annihilation. For this reason, the toric code has attracted much interest also as a theoretical toy model for [[anyon|anyonic]] [[topological order]] in addition to or independently of its use in [[quantum error correction]].

## Related concepts

* [[surface code]]

* [[bit flip code]]
  
* [[stabilizer code]]

* [[HaPPY code]]

* [[Majorana dimer code]]



## References

### General

The original article:

* {#Kitaev03} [[Alexei Kitaev]]: *Fault-tolerant quantum computation by anyons*, Annals of Physics **303** 1 (2003) 2-30 \[<a href="https://doi.org/10.1016/S0003-4916(02)00018-0">doi:10.1016/S0003-4916(02)00018-0</a>, [arXiv:quant-ph/9707021](https://arxiv.org/abs/quant-ph/9707021)\]

Review:

* Maria F. Araujo de Resende: *A pedagogical overview on 2D and 3D Toric Codes and the origin of their topological orders*,  Reviews in Mathematical Physics **32** 02 (2020) 2030002 \[<a href="https://doi.org/10.1142/S0129055X20300022">doi:10.1142/S0129055X20300022</a>, [arXiv:1712.01258](https://arxiv.org/abs/1712.01258)\]

* Héctor Bombín, around Fig. 9 in: *An Introduction to Topological Quantum Codes*, in: *Quantum Error Correction*, Cambridge University Press (2013) \[<a href="https://www.cambridge.org/de/universitypress/subjects/physics/quantum-physics-quantum-information-and-quantum-computation/quantum-error-correction?format=HB&isbn=9780521897877">ISBN:9780521897877</a>, [arxiv:1311.0277](https://arxiv.org/abs/1311.0277)\]


* Paul Herringer: *The Toric Code* (2020) \[<a href="https://www.physics.rutgers.edu/grad/602/Lectures/JC_Presentations/0419/Intro_Toric_Code.pdf">pdf</a>\]

See also: 

* Wikipedia, *[Toric code](https://en.wikipedia.org/wiki/Toric_code)*

* errorcorrectionzoo.org: *[Toric code](https://errorcorrectionzoo.org/c/toric)*

On the problem of its experimental realization:

* {#NussinovOrtiz08} [[Zohar Nussinov]], [[Gerardo Ortiz]], pp. 5 in: *Autocorrelations and Thermal Fragility of Anyonic Loops in Topologically Quantum Ordered Systems*, Phys. Rev. B **77** x (2008) Phys. Rev. B 77, 064302 \[<a href="https://doi.org/10.1103/PhysRevB.77.064302">doi:10.1103/PhysRevB.77.064302</a>, [arXiv:0709.2717](https://arxiv.org/abs/0709.2717), [arXiv:0709.2717](https://arxiv.org/abs/0709.2717)\]
  > "the existence of a gap in this system may not protect a finite expectation value of the Toric code operators \[...\] The physical reason behind this result is the proliferation of topological defects (solitons) at any finite $T$."


* {#VLV21} Ruben Verresen, Mikhail D. Lukin, Ashvin Vishwanath: *Prediction of Toric Code Topological Order from Rydberg Blockade*, Phys. Rev. X **11** (2021) 031005 \[<a href="https://doi.org/10.1103/PhysRevX.11.031005">doi:10.1103/PhysRevX.11.031005</a>\]
  > "Unfortunately, the experimental realization of such phases \[...\] has been exceedingly difficult."




[[!include anyonic topological order on tori -- references]]







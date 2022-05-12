
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In [[quantum physics]] and especially in [[condensed matter theory]], *Slater determinants* are certain [[wavefunctions]] expressing the joint [[quantum state]] of multiple [[electrons]] (or possiby other [[fermions]]) as skew-symmetrized products of given single-particle wavefunctions.

Concretely, given a [[linear basis]] 

$$
  \big( \psi_{I} \big)_{I = 1}^\infty
$$

for the [[Hilbert space]] of single-electron [[wavefunctions]], being [[square-integrable functions]] on the ambient [[Euclidean space|Euclidean $d$-space]] 

$$
  \psi_i \;\in\; L^2\big( \mathbb{R}^d; \mathbb{C}\big)
  \,.
$$

a *Slater determinant* for $N \in \mathbb{N}$ particles is a function on the $N$-fold [[product space]] $\big( \mathbb{R}^d\big)^N$ of the following [[determinant]]-form

$$
  \Psi_{\mathcal{I}}
  (\vec x_1, \cdots, \vec x_N)
  \;\coloneqq\;
  det
  \big(
    \psi_{I_i}(\vec x_j) 
  \big)
  \;=\;
  \underset{
    \sigma \in Sym(N)
  }{\sum}
  sgn(\sigma)
  \cdot
  \psi_{I_1}(\vec x_{\sigma(1)})
  \cdot
  \psi_{I_2}(\vec x_{\sigma(2)})
  \cdots
  \psi_{I_N}(\vec x_{\sigma(N)})
  \,,
$$

where $\mathcal{I} = \big( I_1, \cdots, I_N\big)$ is an [[n-tuple|$N$-tuple]] of indices, with $\big( \psi_{I_1}, \cdots \psi_{I_N} \big)$ the corresponding [[n-tuple|$N$-tuple]] of 1-electron wavefunctions.

(Here $Sym(N)$ denotes the [[symmetric group]] of [[permutations]] of $N$ ordered elements, and $sgn(\sigma) \in \{\pm 1\}$ denotes the [[signature of a permutation|signature]] of a given permutation $\sigma$.)

In fact, for actual electrons the wavefunctions are also functions of their [[spin]], which means, in the non-relativistic case,  that the $\psi_I$ depend also on an argument in $\{\uparrow, \downarrow\}$, in addition to their dependence on $\vec x$, and the corresponding Slater determinant states are obtained by skew-symmetrizing over all of these degrees of freedom.

The point of this construction is that it enforces the skew-symmetry under permutation of position of electrons, which is their characteristic property as *[[fermions]]*. As the multi-index set $\mathcal{I}$ ranges, the corresponding Slater determinants span the Hilbert space of $N$-electron quantum states.

In the practice of computing [[ground states]] etc. in [[solid state physics]], one tries to use as few multi-indices $\mathcal{I}$ as possible:

In the extreme case, the *[[Hartree-Fock method]]* tries to approximate a multi-electron system by the clever choice of a *single* Slater determinant. More accurate approximation methods use linear combinations of more and more Slater determinants, as the multi-index set $\mathcal{I}$ ranges. If, in principle, the full space of Slater determinants is used, one speaks of the *[[configuration interaction method]]*.

## Related concepts

* [[Pauli exclusion principle]]


## References

The construction was maybe first made explicit as eq. (15) in

* [[Paul A. M. Dirac]], *On the theory of quantum mechanics*, Proceedings of the Royal Society **112** 762 (1926) $[$[di:10.1098/rspa.1926.0133](https://doi.org/10.1098/rspa.1926.0133)$]$

It is named after:

* [[John C. Slater]], *The Theory of Complex Spectra*, Phys. Rev. **34** (1929) 1293 $[$[doi:10.1103/PhysRev.34.1293](https://doi.org/10.1103/PhysRev.34.1293)$]$

Review:

* C. Lanczos, R. C. Clark, G. H. Derrick (eds.), p. 196 in: *Mathematical Methods in Solid State and Superfluid Theory*, Springer (1986) $[$[doi:10.1007/978-1-4899-6435-9](https://doi.org/10.1007/978-1-4899-6435-9)$]$


* Pablo Echenique, J. L. Alonso, around (33) in:  *A mathematical and computational review of Hartree-Fock SCF methods in Quantum Chemistry*, Molecular Physics **105** (2007) 3057-3098 $[$[doi:10.1080/00268970701757875](https://doi.org/10.1080/00268970701757875)$]$

See also:

* Wikipedia, *[Slater determinant](https://en.wikipedia.org/wiki/Slater_determinant)*


[[!redirects Slater determinants]]

[[!redirects Hartree-Fock method]]
[[!redirects Hartree-Fock methods]]

[[!redirects configuration interaction method]]
[[!redirects configuration interaction methods]]








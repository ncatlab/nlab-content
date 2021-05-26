
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[[entropy]] induced by [[entanglement]] in [[quantum physics]], really a synonym for [[subsystem]] entropy

If $\rho$ is a [[quantum state]] ([[density matrix]]) of some [[quantum systems]] and $A$ is a subsystem with complementary subsystem $\bar A$, the its entanglement entropy is 

$$
  S_A
  \;=\;
  - 
  Tr_{A}\big( \rho_A \ln \rho_A \big)
$$

for 

$$
  \rho_A \;\coloneqq\; Tr_{\bar A}(\rho)
  \,.
$$


## Related concepts

* [[tensor network]]

* [[holographic entanglement entropy]]

* [[black hole entropy]] via [[AdS-CFT duality]]

[[!include states and observables -- content]]


## References

### General

* Matthew Headrick, _Lectures on entanglement entropy in field theory and holography_ ([arXiv:1907.08126](https://arxiv.org/abs/1907.08126))

In [[AQFT]]:

* [[Roberto Longo]], Feng Xu, _Von Neumann Entropy in QFT_ ([arxiv:1911.09390](https://arxiv.org/abs/1911.09390))

See also

* Wikipedia, _[Entropy of entanglement](http://en.wikipedia.org/wiki/Entropy_of_entanglement)_


### Topological entanglement entropy
 {#ReferencesTopologicalEntanglementEntropy}


Identification of a non-vanishing contribution to the (entanglement-)entropy at [[absolute zero]], due to [[topological order]]/[[topological phases of matter|topological phase]] ("topological entropy"):

* [[Alexei Kitaev]], [[John Preskill]], *Topological entanglement entropy*, Phys. Rev. Lett. 96 (2006) 110404 ([arXiv:hep-th/0510092](https://arxiv.org/abs/hep-th/0510092))

* [[Michael Levin]], [[Xiao-Gang Wen]], *Detecting topological order in a ground state wave function*, Phys. Rev. Lett., 96, 110405 (2006) ([arXiv:cond-mat/0510613](https://arxiv.org/abs/cond-mat/0510613))

Review:

* {#Furukawa08} Shunsuke Furukawa, *Entanglement Entropy in Conventional and Topological Orders*, talk at [Topological Aspects of Solid State Physics](http://www.issp.u-tokyo.ac.jp/public/tassp/) 2008 ([pdf](http://www.issp.u-tokyo.ac.jp/public/tassp/pdf_presentation/SY_S_Furukawa.pdf), [[FurukawaEntanglementEntropy.pdf:file]])

In terms of [[Renyi entropy]] (it's indeopendent of the Renyi entropy parameter):

* Ulrich Schollwöck, *(Almost) 25 Years of DMRG - What Is It About?* ([pdf](https://confs.physics.ox.ac.uk/pauli2016/files/slides/Schollwoeck.pdf))

Further discussion:

* Shunsuke Furukawa, Gregoire Misguich, *Topological Entanglement Entropy in the Quantum Dimer Model on the Triangular Lattice*, Phys. Rev. B 75, 214407 (2007) ([arXiv:cond-mat/0612227](https://arxiv.org/abs/cond-mat/0612227))

* A. Hamma, W. Zhang, S. Haas, and D. A. Lidar, *Entanglement, fidelity, and topological entropy in a quantum phase transition to topological order*, Phys. Rev. B 77, 155111 (2008) ([doi:10.1103/PhysRevB.77.155111](https://doi.org/10.1103/PhysRevB.77.155111), [arXiv:0705.0026](https://arxiv.org/abs/0705.0026))

* Hong-Chen Jiang, [[Zhenghan Wang]], Leon Balents, *Identifying Topological Order by Entanglement Entropy*, Nature Physics 8, 902-905 (2012) ([arXiv:1205.4289](https://arxiv.org/abs/1205.4289))



[[!redirects entanglement entropies]]


[[!redirects entropy of entanglement]]

[[!redirects topological entanglement entropy]]
[[!redirects topological entropy]]



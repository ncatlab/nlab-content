
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

* Matthew Headrick, _Lectures on entanglement entropy in field theory and holography_ ([arXiv:1907.08126](https://arxiv.org/abs/1907.08126))

In [[AQFT]]:

* [[Roberto Longo]], Feng Xu, _Von Neumann Entropy in QFT_ ([arxiv:1911.09390](https://arxiv.org/abs/1911.09390))

See also

* Wikipedia, _[Entropy of entanglement](http://en.wikipedia.org/wiki/Entropy_of_entanglement)_

Discussion of entanglement entropy for [[topological phases of matter]]:

* [[Alexei Kitaev]], [[John Preskill]], *Topological entanglement entropy*, Phys. Rev. Lett. 96 (2006) 110404 ([arXiv:hep-th/0510092](https://arxiv.org/abs/hep-th/0510092))


* Hong-Chen Jiang, [[Zhenghan Wang]], Leon Balents, *Identifying Topological Order by Entanglement Entropy*, Nature Physics 8, 902-905 (2012) ([arXiv:1205.4289](https://arxiv.org/abs/1205.4289))



[[!redirects entanglement entropies]]


[[!redirects entropy of entanglement]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
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

[[entropy]] induced by [[entanglement]] in [[quantum physics]], essentially a synonym for *[[subsystem]] entropy*.

If $\rho$ is a [[quantum state]] ([[density matrix]]) of some [[quantum systems]] and $A$ is a [[subsystem]] with complementary subsystem $\overline{A}$, then its *entanglement entropy* is 

$$
  S_A
  \;\coloneqq\;
  - 
  Tr_{A}\big( \rho_A \ln \rho_A \big)
  \,,
  \;\;\;
  \text{where}
  \;\;\;
  \rho_A \;\coloneqq\; Tr_{\bar A}(\rho)
  \,.
$$

Special aspects:

A constant contribution to $S_A$ (i.e. independent of the choice of $A$, in a suitable sense) is called a **[[topological entanglement entropy]]** indicating **[[long-range entanglement]]** and "[[topological order]]", being proportional to the total [[quantum dimension]] of [[anyon]]-excitations. (See the references [below](#ReferencesTopologicalEntanglementEntropy).)

On the other extreme, for **[[short range entanglement]]** the entanglement entropy is thought to scale with the surface [[area]] of the subsystem $A$ (to the extent that this makes sense, say in say in [[lattice models]]), a behaviour reminiscent of [[Bekenstein-Hawking entropy]] of [[black holes]]. For more on this see at **[[holographic entanglement entropy]]**.


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




[[!include topological entanglement entropy -- references]]




[[!redirects entanglement entropies]]


[[!redirects entropy of entanglement]]

[[!redirects topological entanglement entropy]]
[[!redirects topological entropy]]




+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

The notion of _relative entropy_ of [[state|states]] is a generalization of the notion of [[entropy]] to a situation where the entropy of one [[state]] is measured "relative to" another state.


It is also called 

* _Kullback-Leibler divergence_,

* _information divergence_, or

* _information gain_. 


## Definition

### For states on finite probability spaces
 {#OnFiniteDimensionalSpaces}

For two finite [[probability distributions]] $(p_i)$ and $(q_i)$, their **relative entropy** is 

$$
  S(p/q) := \sum_{k = 1}^n p_k(log p_k - log q_k)
  \,.
$$

Alternatively, for $\rho, \phi$ two [[density matrix|density matrices]], their relative entropy is 

$$
  S(\rho/\phi) := tr \rho(log \rho - log \phi)
  \,.
$$


### For states on classical probability spaces

+-- {: .num_defn}
###### Definition

For $X$ a [[measurable space]] and $P$ and $Q$ two [[probability measure|probability measures]] on $X$, such that $Q$ is absolutely continuous with respect to $P$, their relative entropy is the [[integral]]

$$
  S(Q|P) = \int_X log \frac{d Q}{d P} d P
  \,,
$$

where $d Q / d P$ is the [[Radon-Nikodym derivative]] of $Q$ with respect to $P$. 

=--



### For states on quantum probability spaces (von Neumann algebras)

Let $A$ be a [[von Neumann algebra]] and let $\phi$, $\psi : A \to \mathbb{C}$ be two [[state|states]] on it (faithful, positive [[linear functional|linear functionals]]).

+-- {: .num_defn}
###### Definition

The **relative entropy $S(\phi/\psi)$ of $\psi$ relative to $\phi$ is

$$
  S(\phi/\psi) := - (\Psi, (log \Delta_{\Phi,\Psi}) \Psi)
  \,,
$$

where $\Delta_{\Phi,\Psi}$ is the relative [[modular operator]] of any [[cyclic vector|cyclic]] and [[separating vector]] representatives $\Phi$ and $\Psi$ of $\phi$ and $\psi$.

=--

This is due to ([Araki](#Araki)).

+-- {: .num_prop}
###### Proposition

* This definition is independent of the choice of these representatives. 

* In the case that $A$ is finite dimensional and $\rho_\phi$ and $\rho_\psi$ are [[density matrices]] of $\phi$ and $\psi$, respectively, this reduces to the [above definition](#OnFiniteDimensionalSpaces).

=--

## Relation to machine learning

The [[machine learning]] process has been characterized as a minimization of relative entropy ([Ackley, Hinton and Sejnowski 1985](#AckleyHintonSejnowski)).

## Related concepts

* [[Fisher metric]]
* [[information geometry]]
* [[machine learning]]

## References

Relative entropy of [[state on a star-algebra|states]] on  [[von Neumann algebras]] was introduced in:

* {#Araki} [[Huzihiro Araki]], _Relative Entropy of States of von Neumann Algebras_, Publications of the Research Institute for Mathematical Sciences, **11** 3 (1976), 809-833 ([pdf](https://ems.press/content/serial-article-files/2833), [doi:10.2977/prims/1195191148]( https://doi.org/10.2977/prims/1195191148))
 

A characterization of [relative entropy](#OnFiniteDimensionalSpaces) on finite-[[dimension|dimensional]] [[C-star algebra|C-star algebras]] is given in 

* {#Petz} D. Petz, _Characterization of the relative entropy of states of matrix algebras_,  Acta Mathematica Hungarica, **59** (1992), 3-4. ([doi:10.1007/bf00050907](https://doi.org/10.1007/bf00050907)) 


A survey of entropy in [[operator algebra|operator algebras]] is in 

* Erling St&#248;rmer, _Entropy in operator algebras_ ([pdf](http://www.claymath.org/publications/currentvolumes/connes60/Stormer.pdf))

A characterization of [[machine learning]] as a process minimizing relative entropy is proposed in

* {#AckleyHintonSejnowski} David H. Ackley, Geoffrey E. Hilton, Terrence J. Sejnowski. _A learning algorithm for Boltzmann machines_, Cognitive Science, **9** (1985), 147–169. ([web](https://www.sciencedirect.com/science/article/abs/pii/S0364021385800124)) 

[[!redirects relative entropy]]
[[!redirects relative entropies]]

[[!redirects Kullback-Leibler divergence]]
[[!redirects Kullback-Leibler information]]
[[!redirects information divergence]]
[[!redirects information gain]]
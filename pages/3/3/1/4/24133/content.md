
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *parameterized quantum system* is a [[quantum system]] depending on "external" or "classical" parameters.

In typical examples arising in [[quantum mechanics]], this simply means that the [[Hamiltonian]] $H$ is not just one fixed [[linear operator]] on a given [[Hilbert space]] [[space of quantum states|of quantum states]] $\mathcal{H}$, but a [[continuous function|continuous]] (or suitably [[smooth function|smooth]]) [[map]]

$$
  H(-)
  \;\colon\;
  P
  \longrightarrow
  End(\mathcal{H})
$$

of such, from some [[topological space|topological]] "parameter space" $P$.


More abstractly, where a single [[quantum system]] is described by [[linear type theory]] (see also at *[[quantum logic]]*), a parameterized quantum system is described by *[[dependent linear type theory]]*.



## Properties

### Quantum adiabatic theorem and Berry phases

The *[[quantum adiabatic theorem]]* says that/how the evolution of a parameterized quantum system under sufficiently slow movement of the external parameters remains in an [[eigenstate]] for a given system of [[commutator|commuting]] [[quantum observables]]. The remaining transformations on these [[eigenspaces]] are known as (non-abelian) *[[Berry phases]]*.

## Examples

### Time-dependent quantum mechanics

For example, *time-dependent* Hamiltonians/quantum systems are described this way for $P \subset \mathbb{R}$ interpreted as the space of [[time]]-parameters. 

See also at *[[Dyson formula]]*.

### Defect anyon braiding

In some models of [[braid group statistics]] (see [there](braid+group+statistics#AsBraidingOfDefects) for more) the [[anyons]] are [[defects]]/[[solitons]] whose positions serve as external parameters of the system, so that the (non-abelian) [[Berry phases]] under their [[quantum adiabatic theorem|adibatic moverment]] constitutes a [[braid group representation]] on the [[quantum system]]'s [[ground states]].

## Related concepts

* [[Dyson formula]]

* [[quantum adiabatic theorem]]

* [parameterized quantum computation](quantum+computation#ClassicalControlQuantumData)

* [[subsystem]]

[[!redirects parameterized quantum systems]]

[[!redirects time-dependent Hamiltonian]]
[[!redirects time-dependent Hamiltonians]]




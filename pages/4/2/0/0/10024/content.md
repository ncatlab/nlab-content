
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

# Contents
* table of contents
{: toc}

## Definition

Where a [[probability density function]] (on a [[measure space]]) is a [[real numbers|real]]-valued [[function]] $\rho$ (satisfying certain conditions), a _probability amplitude_ is a [[complex numbers|complex]]-valued function $\psi$ such that its pointwise [[absolute value]] squared

$$
  \rho(x) \coloneqq \psi^\ast(x) \psi(x)
$$

is a probability density.


## In quantum physics

### General

Probability amplitudes appear as [[pure states]] of [[quantum mechanical systems]] in the form of _[[wave functions]]_ $\psi$ on the [[phase space]] of a corresponding [[classical mechanics|classical system]]. The [[Born rule]] of [[quantum physics]] says  that the probability density $\rho = \psi^\ast \psi$ describes the probability to find the physical system in a given classical state (in a given region of its phase space).

The fact that probability amplitudes are complex-valued means that under addition ("[[superposition]]") they exhibit [[quantum interference]] (the addition of their [[complex phases]]) in stark contrast to the addition of probability densities, for which this cannot happen.

For instance on some [[probability space]] $(X,\mu)$ there are the probability amplitudes $ \exp(i \pi/2) \mu$ and $\exp(-i \pi/2)\mu$ whose associated probability densities are both just $\mu$ itself again. But the sum of these two probability amplitudes vanishes, in contrast to the sum of their associated probability densities. This is known as "destructive" [[quantum interference]].

### Scattering amplitudes

In [[perturbative quantum field theory]] the key probability amplitudes considered are _[[scattering amplitudes]]_, which encode the probability for a given  configuration of field quanta to come in from the far past, interact with each other and hence "scatter off" each other, and then re-emerge as some other set of field quanta in the far future.

These amplitudes are collected in the _[[scattering matrix]]_ of the [[perturbative quantum field theory]].

## Related concepts

* [[quantum logic]]

* [[interpretation of quantum mechanics]]

[[!include states and observables -- content]]


[[!redirects probability amplitude]]
[[!redirects probability amplitudes]]

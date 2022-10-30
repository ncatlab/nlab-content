
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## In quantum mechanics

In [[quantum mechanics]] what is called the _Dyson formula_ is what in _[[mathematics]]_ is called the _[[iterated integral]]-expression for [[parallel transport]]_: It an expression for the solution to a [[differential equation]] of the form

$$
  \frac{d}{d t} \psi(t)
  \;=\; 
  i H(t)
  \psi(t)
$$

where $t \mapsto \psi(t) \in \mathcal{H}$ is a one-parameter family of elements of some [[Hilbert space]] and $t \mapsto H(t)$ is a one-parameter family of [[linear operators]] on this Hilbert space.

This appears prominently in the expression of the [[Schrödinger equation]] in the [[interaction picture]], in which case $H(t)$ is the [[interaction]] [[Hamiltonian]] in the [[Heisenberg picture]] of the [[free field|free]] theory. In this case the Dyson series gives the _[[S-matrix]]_.
This is the context in which the term "Dyson formula" orginates. But of course also the plain Schr&#246;dinger equation ("in the [[Schrödinger picture]]") is already of this form if the Hamiltonian is time-dependent.

The idea is to think of the solution as given by the [[limit of a sequence|limit]]

$$
  \psi(t)
  \;=\;
  \underset{N \to \infty}{\lim}
  \underset{N \, \text{factors}}{
  \underbrace{
  \left(
    id + \tfrac{i}{N}H(t)
  \right)
  \left(
    id + \tfrac{i}{N}H(t(N-1)/N)
  \right)
  \cdots
  \left(
    id + \tfrac{i}{N}H(t/N)
  \right)
  }
  }
  \psi(0)
$$

and to think of this as the result of forming the [[exponential]] expression $\exp(\int_{[0,t] } H(t)\,d t)$ and then re-ordering in the resulting sum of products all the factors of $H(t)$ such that they are _time ordered_ with larger values of $t$ ordered to the left of smaller values.

Accordingly, in  the physics literature solutions to this equation are written 

$$
  \psi(t)
  \;=\;
  T\left(
    \exp\left(
      \int_{[0,t]} i H(t) \,d t
    \right)
  \right) 
  \psi(0)
  \,, 
$$ 

with $T(-)$ the _time ordering operator_ producing _[[time-ordered products]]_. The corresponding [[series]] of [[iterated integrals]]

$$
  \psi(t)
  \;=\;
  \left(
    \underoverset{n = 0}{\infty}{\sum}
    (i)^n
    \underset{0 \leq t_1 \leq \cdots \leq t_n \leq t}{\int}
    H(t_n) H(t_{n-1})\cdots H(t_1)
  \right)\psi(0)
$$

is called the _Dyson series_.

## In quantum field theory

The idea generalizes to [[quantum field theory]] in [[Lorentzian manifold|Lorentzian]] spacetime if due care is exercised (including [[adiabatic switching]] and [[point-extension of distributions|point extension]] of [[operator-valued distributions]]). Here the "time ordering" is generalized to a [[causal locality|causal ordering]], this is the content of the construction of the [[S-matrix]] and the [[interacting field algebra]] in _[[causal perturbation theory]]_. 

See at _[[S-matrix]]_ for details.

## Related concepts

* [[path integral]]

* [[iterated integral]]

* [[parallel transport]]
 

[[!redirects Dyson series]]

[[!redirects time-ordered product]]
[[!redirects time-ordered products]]

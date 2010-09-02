
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

## Idea

The _Dyson formula_ is an expression for the solution of the [[Schrödinger equation]] in _time dependent_ [[quantum mechanics]].

It expresses the [[parallel transport]] of the [[Hamiltonian operator]] regarded as a Hermitian-operator valued 1-form on the time axis.

## Definition


In time-dependent [[quantum mechanics]] dynamics is encoded in a [[Lie-algebra valued 1-form]]

$$
  A = i H \,d t \in \Omega^1(\mathbb{R}, \mathfrak{u}(V))
$$

on the [[real line]] (time) with values in the [[Lie algebra]] of the [[unitary group]] on a [[Hilbert space]] $V$. 

For $t  = Id : \mathbb{R} \to \mathbb{R}$ the canonical coordinate function and $d t \in \Omega^1(\mathbb{R})$ accordingly the corresponding canonical basis 1-form, the Lie-algebra valued coefficient

$$
  i H : \mathbb{R} \to \mathfrak{u}(V)
$$

of $A$ is called the [[Hamiltonian]] operator. If $H$ is a constant function, one speaks of _time-independent_ quantum mechanics.

A [[state]] of the system is a function

$$
  \psi : \mathbb{R} \to V
  \,.
$$

A _physical state_ is a solution to the [[Schrödinger equation]]

$$
  d \psi + A \cdot \psi = 0
$$

or equivalently

$$
 \partial_t \psi = i H \psi 
  \,.
$$

This [[differential equation]] is that which defines the [[parallel transport]] of $A$. Its unique solution for given $\psi(0)$ is written

$$
  \psi(t) = P \exp(\int_{[0,t]} i H(t) \, d t) \cdot \psi_0
  \,.
$$

This is called the **Dyson formula** . In the special case of time-independent quantum mechanics this becomes an ordinary exponential of an ordinary integral.


 

[[!redirects Dyson series]]
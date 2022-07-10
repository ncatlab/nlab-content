
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
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

## Idea

A _classical state_ is a [[state]] of a [[system of classical mechanics]].

In principle, a [[pure state]] in classical mechanics specifies completely all information about the state of the system, while a [[mixed state]] is a [[probability measure]] on the space of pure states.  This space of pure states may be identified with the [[state space]] in [[Lagrangian mechanics]] or with the [[phase space]] in [[Hamiltonian mechanics]].


## Definition

We give a definition in a very general context.

For $A$ a [[commutative algebra|commutative]] unital [[associative algebra]] that encodes a [[system of classical mechanics]] (say, the associative algebra underlying a [[Poisson algebra]]), a **classical state** is an $\mathbb{R}$-[[linear function]]

$$
  \rho\colon A \to \mathbb{R}
$$

that satisfies

* **normalization** $\rho(1) = 1$;

* **positivity** for all $a \in A$ we have $\rho(a^2) \geq 0$.

This is essentially the definition of [[quantum state]], but formulated for commutative algebras and over the [[real number]]s.

If we take $A$ to be a $*$-[[star-algebra|algebra]] over the [[complex numbers]], then we may take $\rho$ to be a $\mathbb{C}$-linear function from $A$ to $\mathbb{C}$ instead.


## Related concepts

[[!include classical-to-quantum notions - table]]

[[!include states and observables -- content]]

\linebreak



[[!redirects classical state]]
[[!redirects classical states]]

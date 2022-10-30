
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

> under construction

# Contents
* table of contents
{: toc}

## Idea

A _quantum state_ is a [[state]] of a [[physical system|system]] of [[quantum mechanics]].

In the usual formulations over a [[Hilbert space]] $H$, the [[pure state]]s form space $(H \setminus \{0\})/\mathbb{C}$, where we mod out by the [[action]] of $\mathbb{C}$ on $H \setminus \{0\}$ by scalar multiplication.  Equivalently, we can use $S(H)/U(1)$, the [[unit sphere]] in $H$ modulo the action of the [[unitary group]] $U(1)$.  Often by abuse of language, one says that $H$ is the space of (pure) states.  The [[mixed state]]s are then [[density matrix|density matrices]] on $H$.

In principle, any quantum mechanical system can be treated in this way, by imposing [[superselection rule]]s that identify only some [[self-adjoint operator]]s on $H$ as [[observable]]s.  Alternatively, one may take a more abstract approach, starting with an $C^*$-[[C-star-algebra|algebra]] (perhaps a $W^*$-[[W-star-algebra|algebra]]) as the [[algebra of observables]], then defining states as [[state in AQFT and operator algebra|state]]s on that algebra.

## Definition

We discuss the definitions of quantum states in the [[Heisenberg picture]] and in the [[Schrödinger picture]].

### In the Heisenberg picture

Let a [[quantum mechanical system]] be given by its [[C-star algebra]] of [[observable]]s $A$. Then a **state** on $A$ is

* a $\mathbb{C}$-[[linear function]] $\rho : A \to \mathbb{C}$

* such that

  * it is **positive**: for every $a \in A$ we have $\rho(a^\ast a) \geq 0 \in \mathbb{R}$;


  * it is **normalized**: $\rho(1) = 1$.

See also [[state in AQFT and operator algebra]].

### In the Schr&#246;dinger picture

Given a [[Hilbert space]] $H$, a state is a ray in this Hilbert space.

(...)


## Related concepts

* [[state]]

  * [[classical state]], **quantum state**

  * [[state in AQFT and operator algebra]]

* [[observable]]

  * [[algebra of observables]]

  * [[GNS construction]]


[[!redirects quantum state]]
[[!redirects quantum states]]

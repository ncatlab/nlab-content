
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

A _quantum state_ is a [[state]] of a [[physical system|system]] of [[quantum mechanics]].


## Definitions

The precise mathematical notion of state depends on what mathematical formalization of quantum mechanics is used.


### Hilbert spaces

In the simple formulation over a [[Hilbert space]] $H$, a [[pure state]] is a ray in $H$.  Thus, the [[pure states]] form the space $(H \setminus \{0\})/\mathbb{C}$, where we mod out by the [[action]] of $\mathbb{C}$ on $H \setminus \{0\}$ by scalar multiplication; equivalently, we can use $S(H)/\mathrm{U}(1)$, the [[unit sphere]] in $H$ modulo the action of the [[unitary group]] $\mathrm{U}(1)$.  Often by abuse of language, one calls $H$ the 'space of states'.

The [[mixed states]] are [[density matrix|density matrices]] on $H$.  Every pure state may be interpreted as a mixed state; taking a representative normalised vector ${|\psi\rangle}$ from a ray in Hilbert space, the operator ${|\psi\rangle}{\langle\psi|}$ is a density matrix.

In principle, any quantum mechanical system can be treated using Hilbert spaces, by imposing [[superselection rule]]s that identify only some [[self-adjoint operators]] on $H$ as [[observables]].  Alternatively, one may take a more abstract approach, as follows.


### In AQFT

In [[AQFT]], a [[quantum mechanical system]] is given by a $C^*$-[[C-star-algebra|algebra]] $A$, giving the [[algebra of observables]].  Then a **state** on $A$ is

* a $\mathbb{C}$-[[linear function]] $\rho\colon A \to \mathbb{C}$

* such that

  * it is **positive**: for every $a \in A$ we have $\rho(a^\ast a) \geq 0 \in \mathbb{R}$;


  * it is **normalized**: $\rho(1) = 1$.

See also [[state in AQFT and operator algebra]].

If $H$ is a Hilbert space, then the [[bounded operators]] on $H$ form a $C^*$-algebra $\mathcal{B}H$, and states on the Hilbert space correspond directly to states on $\mathcal{B}H$.  Classical mechanics can also be formulated in AQFT; the classical space of states $X$ gives rise to a commutative [[von Neumann algebra]] $L^\infty(X)$ as the algebra of observables.

Arguably, the correct notion of state to use is that of [[quasi-state]]; every state gives rise to a unique quasi-state, but not conversely.  However, when either classical mechanics or Hilbert-space quantum mechanics is formulated in AQFT, every quasi-state *is* a state (at least if the Hilbert space is not of very low dimension, by [[Gleason's theorem]]).  See also the Idea-section at [[Bohr topos]] for a discussion of this point.


### In FQFT

In the [[FQFT]] formulation of [[quantum field theory]], a physical system is given by a [[cobordism]] [[representation]]

$$
  Bord_n^S \to \mathcal{C}
  \,.
$$

In this formulation the [[k-morphism|(n-1)-morphism]] in $\mathcal{C}$ assigned to an $(n-1)$-dimensional [[manifold]] $\Sigma_{n-1}$ is the _space of states_ over that manifold. A state is accordingly a [[generalized element]] of this object.


## Related concepts

* [[potentiality]]

* [[quantum state tomography]]

[[!include states and observables -- content]]

\linebreak


[[!include classical-to-quantum notions - table]]

## References

Discussion in [[algebraic quantum field theory]]:

* [[Nikolay Bogolyubov]], A. A. Logunov, A. I. Oksak, I. T. Todorov, G. G. Gould, *Algebra of Observables and State Space* &lbrack;[doi:10.1007/978-94-009-0491-0_6](https://doi.org/10.1007/978-94-009-0491-0_6)&rbrack;,  Chapter in: *General principles of quantum field theory*, Mathematical Physics and Applied Mathematics **10**, Kluwer (1990) &lbrack;[doi:10.1007/978-94-009-0491-0](https://doi.org/10.1007/978-94-009-0491-0)&rbrack; 


See also:

* [[Roland Omnès]], §3 of: *[[The Interpretation of Quantum Mechanics]]*, Princeton University Press (1994) &lbrack;[ISBN:9780691036694](http://press.princeton.edu/titles/5525.html)&rbrack;


[[!redirects quantum state]]
[[!redirects quantum states]]

[[!redirects quantum state space]]
[[!redirects quantum state spaces]]


[[!redirects mixed quantum state]]
[[!redirects mixed quantum states]]

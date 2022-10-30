
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

_under construction_

## Idea

The Gelfand--Naimark--Segal (GNS) construction establishes a correspondence between cyclic $*$-[[representations]] of $C^*$-[[C*-algebra|algebras]] and certain linear functionals (usually called _[[state on an operator algebra|states]]_) on those same $C^*$-algebras.  The correspondence comes about from an explicit construction of the [[star-representation|*-representation]] from one of the [[linear functionals]] ([[state on an operator algebra|states]]).


## Details

### For $C^\ast$-algebras

+-- {: .num_theorem}
###### Theorem

Given 

1. a [[C*-algebra]], $\mathcal{A}$;

1. a [[states in AQFT and operator algebra|state]], $\rho \;\colon\; \mathcal{A} \to \mathbb{C}$

there exists 

1. a $*$-[[representation]] 

   $$
     \pi 
     \;\colon\;
     \mathcal{A}
      \longrightarrow
      End(\mathcal{H})
   $$

   of $\mathcal{A}$ on some [[Hilbert space]] $\mathcal{H}$

1. a [[cyclic vector]] $\psi \in \mathcal{H}$ 

such that $\rho$ is the state corresponding to $\psi$, in that

$$
  \begin{aligned}
    \rho(A) 
      & = \langle \psi \vert\, A \, \vert \psi \rangle
      \\
      & \coloneqq
      \langle \psi , \pi(A) \psi \rangle
  \end{aligned}
$$

for all $A \in \mathcal{A}$.

=--


### For $C^\ast$-categories

The GNS construction for $C^\ast$-algebras is a special case of a more general construction of Ghez, Lima and Roberts applied to [[C*-categories]] ([[horizontal categorification]] of $C^\ast$-algebras).

+--{: .num_theorem}
###### Theorem

Let $\mathcal{C}$ be a $C^\ast$-category. Fix an object $A \in \operatorname{Ob}\mathcal{C}$ and let $\sigma$ be a state on the $C^\ast$-algebra $\mathcal{C}(A,A)$. Then there exists a $*$-representation
$$
\rho_\sigma \colon \mathcal{C} \to \mathbf{Hilb}
$$
together with a cyclic vector $\xi \in \rho_\sigma(A)$ such that for all $x \in \mathcal{C}(A,A)$,
$$
\sigma(x) = \langle \xi, \rho_\sigma(x)\xi \rangle.
$$
=--


A [[C*-algebra]] $\mathcal{A}$ is a $C^\ast$-category with a single [[object]] $\bullet$, where we make the identification $A = \mathcal{A}(\bullet,\bullet)$. In this case the theorem reduces to the classical GNS construction.






## Applications

The GNS construction is a central ingredient that translates between the [[Heisenberg picture]] and the [[Schrödinger picture]] of [[quantum mechanics]]: the [[AQFT]] and the [[FQFT]] picture of [[quantum field theory]]. In the former one considers $C^\ast$-[[algebras of observables]], in the latter the [[spaces of states]]. Given a $C^\ast$-algebra of observables, the corresponding space of state can be taken to be that given by the GNS construction.

## References
 
See also 

* Wikipedia, _[Gelfand-Naimark-Segal construction](https://en.wikipedia.org/wiki/Gelfand%E2%80%93Naimark%E2%80%93Segal_construction)_


For general unital [[star-algebras]]: 

* {#KhavkineMoretti15}  [[Igor Khavkine]], [[Valter Moretti]], _Algebraic QFT in Curved Spacetime and quasifree Hadamard states: an introduction_, Chapter 5 in [[Romeo Brunetti]] et al. (eds.) _Advances in Algebraic Quantum Field Theory_, , Springer, 2015

For [[formal power series algebras]]:

* {#BordemannWaldmann96} [[Martin Bordemann]], [[Stefan Waldmann]], _Formal GNS Construction and States in Deformation Quantization_, Commun. Math. Phys. (1998) 195: 549.  ([arXiv:q-alg/9607019](https://arxiv.org/abs/q-alg/9607019), [doi:10.1007/s002200050402](https://doi.org/10.1007/s002200050402))

category: operator algebras

[[!redirects Gelfand-Naimark-Segal construction]]
[[!redirects Gelfand–Naimark–Segal construction]]
[[!redirects Gelfand--Naimark--Segal construction]]
[[!redirects GNS construction]]
[[!redirects GNS-construction]]
[[!redirects GNS representation]]
[[!redirects GNS-representation]]
[[!redirects GNS theorem]]
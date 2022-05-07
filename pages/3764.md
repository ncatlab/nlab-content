
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The _Gelfand-Naimark-Segal construction_ ("GNS construction") represents a [[state on a star-algebra]] over the [[complex numbers]] -- which *a priori* is defined purely algebraically as a non-degenerate positive linear function

$$
  \rho \;\colon\; \mathcal{A} \longrightarrow \mathbb{C}
  \,,
$$

-- by a [[vector]] $\psi \in \mathcal{H}$ in a [[complex numbers|complex]] [[Hilbert space]] $\mathcal{H}$ as the "[[expectation value]]"

$$
  \begin{aligned}
    \rho(A) 
    & = \langle \psi \vert \, A \, \vert \psi \rangle
    \\
    & \coloneqq \langle \psi, \pi(A) \psi \rangle  
  \end{aligned}
$$

with respect to some [[star-representation]] 

$$
  \pi \;\colon\; \mathcal{A} \longrightarrow End(\mathcal{H})
$$

of $\mathcal{A}$ on (a [[dense subspace]] of) $\mathcal{H}$; where $\langle -,-\rangle$ denotes the [[inner product]] on the [[Hilbert space]].

Originally this was considered for [[C*-algebras]] and [[C*-representations]] ([Gelfand-Naimark 43](#GelfandNaimark43), [Segal 47](#Segal47)), see for instance ([Schm&#252;dgen 90](#Schmuedgen90)), but the construction applies to general [[unital algebra|unital]] [[star algebras]] $\mathcal{A}$ ([Khavkine-Moretti 15](#KhavkineMoretti15)) as well as to other coefficient rings, such as to  [[formal power series algebras]] over $\mathbb{C}[ [\hbar] ]$ ([Bordemann-Waldmann 96](#BordemannWaldmann96)). 

The GNS-construction plays a central role in [[algebraic quantum field theory]] ([Haag 96](#Haag96), [Moretti 18](#Moretti18), [Khavkine-Moretti 15](#KhavkineMoretti15)), where $\mathcal{A}$ plays the role of an [[algebra of observables]] and $\rho \colon \mathcal{A} \to \mathbb{C}$ the role of an actual state of a [[physical system]] (whence the terminology) jointly constituting the "[[Heisenberg picture]]"-perspective of [[quantum physics]]; so that the GNS-construction serves to re-construct a corresponding [[Hilbert space|Hilbert]] [[space of states]] as in the [[Schrödinger picture]] of quantum physics. In this context the version for [[C*-algebras]] corresponds to [[non-perturbative quantum field theory]], while the generalization to [[formal power series algebras]] corresponds to [[perturbative quantum field theory]].

## Details

> under construction


### For $C^\ast$-algebras

+-- {: .num_theorem}
###### Theorem

Given 

1. a [[C*-algebra]], $\mathcal{A}$;

1. a [[states in AQFT and operator algebra|state]], $\rho \;\colon\; \mathcal{A} \to \mathbb{C}$

there exists 

1. a [[C*-representation]] 

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
 {#ForCStarCategories}

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

## Related concepts

* [[Riesz representation theorem]]

[[!include states and observables -- content]]


## References
 
The original construction for [[C*-algebras]] and [[C*-representations]] is due to 

* {#GelfandNaimark43} [[Israel Gelfand]], [[Mark Naimark]], _On the imbedding of normed rings into the ring of operators on a Hilbert space_. Matematicheskii Sbornik. 12 (2): 197&#8211;217 (1943)

* {#Segal47} [[Irving Segal]], _Irreducible representations of operator algebras_ ([pdf](http://www.ams.org/journals/bull/1947-53-02/S0002-9904-1947-08742-5/S0002-9904-1947-08742-5.pdf)). Bull. Am. Math. Soc. 53: 73&#8211;88, (1947) 

see for instance

* {#Schmuedgen90} K. Schm&#252;dgen, _Unbounded  operator  algebras  and  representation  theory_, Operator  theory, advances and applications, vol. 37. Birkh&#228;user, Basel (1990)

The application to [[algebraic quantum field theory]] is discussed in

* {#Haag96} [[Rudolf Haag]], _Local  Quantum  Physics:  Fields,  Particles,  Algebras_,   Texts  and  Monographs  in Physics. Springer (1996).

* {#Moretti18} [[Valter Moretti]], _Spectral Theory and Quantum Mechanics :Mathematical Structure of Quantum Theories, Symmetries and introduction to the Algebraic Formulation_, 2nd ed.  Springer Verlag, Berlin (2018)


See also 

* Wikipedia, _[Gelfand-Naimark-Segal construction](https://en.wikipedia.org/wiki/Gelfand%E2%80%93Naimark%E2%80%93Segal_construction)_


For general unital [[star-algebras]]: 

* {#KhavkineMoretti15}  [[Igor Khavkine]], [[Valter Moretti]], _Algebraic QFT in Curved Spacetime and quasifree Hadamard states: an introduction_, Chapter 5 in [[Romeo Brunetti]] et al. (eds.) _Advances in Algebraic Quantum Field Theory_, , Springer, 2015

in relation with the classical moment problem and the notion of [[POVM]]

* {#DragoMoretti19} Nicolò Drago,  [[Valter Moretti]], 
 The notion of observable and the moment problem for *-algebras and their GNS representations, Lett. Math. Phys. 2020 in print  ([arXiv.org:1903.07496](https://arxiv.org/abs/1903.07496))

For [[formal power series algebras]] over $\mathbb{C}[ [ \hbar ] ]$:

* {#BordemannWaldmann96} [[Martin Bordemann]], [[Stefan Waldmann]], _Formal GNS Construction and States in Deformation Quantization_, Commun. Math. Phys. (1998) 195: 549.  ([arXiv:q-alg/9607019](https://arxiv.org/abs/q-alg/9607019), [doi:10.1007/s002200050402](https://doi.org/10.1007/s002200050402))

Discussion in terms of [[universal properties]] in ([[higher category theory|higher]]) [[category theory]] is in 

* {#Jacobs10} [[Bart Jacobs]], _Involutive Categories and Monoids, with a GNS-correspondence_, Foundations of Physics, July 2012, Volume 42, Issue 7, pp 874&#8211;895 ([arXiv:1003.4552](https://arxiv.org/abs/1003.4552))

* {#Parzygnat16} [[Arthur Parzygnat]], _From observables and states to Hilbert space and back: a 2-categorical adjunction_ ([arXiv:1609.08975](https://arxiv.org/abs/1609.08975))

category: operator algebras

[[!redirects Gelfand-Naimark-Segal construction]]
[[!redirects Gelfand–Naimark–Segal construction]]
[[!redirects Gelfand--Naimark--Segal construction]]
[[!redirects GNS construction]]
[[!redirects GNS-construction]]
[[!redirects GNS representation]]
[[!redirects GNS-representation]]
[[!redirects GNS theorem]]
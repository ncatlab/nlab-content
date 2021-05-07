
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
  {#ForCStarAlgebras}

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

1. a [[cyclic vector]] $\psi_\rho \in \mathcal{H}$ 

such that $\rho$ is the state corresponding to $\psi_\rho$, in that

$$
  \begin{aligned}
    \rho(A) 
      & = \langle \psi_\rho \vert\, A \, \vert \psi_\rho \rangle
      \\
      & \coloneqq
      \langle \psi_\rho , \pi(A) \psi_\rho \rangle
  \end{aligned}
$$

for all $A \in \mathcal{A}$.

=--

Namely, consider on the underlying [[complex vector space]] of $\mathcal{A}$ the [[sesquilinear form]] (inner product)

$$
  \langle A,B \rangle_\rho
  \;\coloneqq\;
  \rho
  \big(
    A^\ast B
  \big)
  \,.
$$

Since $\rho$ is a "positive functional", hence taking non-negative values, this is, in general, [positive semi-definite](sesquilinear+form#Definity).
It becomes [positive definite](sesquilinear+form#Definity) on the the [[quotient vector space]]

\[
  \label{HilbertSpaceAsQuotientOfStarAlgebraByNullSpace}
  \mathcal{H}
  \;\coloneqq\;
  \mathcal{A}/N
\]

by the subspace of 0-norm elements

\[
  \label{TheNullIdeal}
  N 
    \;\coloneqq\; 
  \big\{
    A \in \mathcal{A}
    \,\vert\,
    \rho(A^\ast A) = 0
  \big\}
  \,.
\]

In fact, $N$ is a left [[ideal]] in $\mathcal{A}$ so that the left multiplication [[action]] of $\mathcal{A}$ on itself descends to an action the quotient Hilbert space (eq:TheNullIdeal)

$$
  \array{
    \mathcal{A} \otimes \mathcal{H}
    &
    \overset{
      \;\;\;\;\;
      \pi
      \;\;\;\;\;
    }{
      \longrightarrow
    }
    &
    \mathcal{H}
    \\
    (A, [\psi]) &\mapsto& [A \cdot \psi]
    \,.
  }
$$

The cyclic vector is hence the tautological

$$
  \psi_\rho \;\coloneqq\; [1]
  \,.
$$

Hence on this Hilbert space $\mathcal{H}$, the original  operator-algebraic state $\rho$ is now represented by the tautological [[density matrix]] 

$$
  \left\vert \psi_\rho \right\rangle \left\langle \psi_\rho \right\rangle
  \;=\;
  \left\vert [1] \right\rangle \left\langle [1] \right\rangle
  \,.
$$


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
 
The original construction for [[C*-algebras]] and [[C*-representations]] is due to:

* {#GelfandNaimark43} [[Israel Gelfand]], [[Mark Naimark]], *On the imbedding of normed rings into the ring of operators on a Hilbert space*,  Matematicheskii Sbornik. 12 (2): 197&#8211;217 (1943) 

  reprinted in:

  Robert Doran (ed.), *$C^\ast$-Algebras: 1943–1993*, Contemporary Mathematics **167**, AMS 1994 ([doi:10.1090/conm/167](http://dx.doi.org/10.1090/conm/167))

* {#Segal47} [[Irving Segal]], _Irreducible representations of operator algebras_, Bull. Am. Math. Soc. 53: 73&#8211;88, (1947)  ([pdf](http://www.ams.org/journals/bull/1947-53-02/S0002-9904-1947-08742-5/S0002-9904-1947-08742-5.pdf), [euclid](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society-new-series/volume-53/issue-2/Irreducible-representations-of-operator-algebras/bams/1183510397.full))


Textbook accounts:

* [[Gerard Murphy]], Section 3.4 of: _$C^\ast$-algebras and Operator Theory_, Academic Press 1990 ([doi:10.1016/C2009-0-22289-6](https://doi.org/10.1016/C2009-0-22289-6))

* {#Schmuedgen90} [[Konrad Schmüdgen]], Section 8.3 of: _Unbounded  operator  algebras  and  representation  theory_, Operator  theory, advances and applications, vol. 37. Birkh&#228;user, Basel (1990) ([doi:10.1007/978-3-0348-7469-4](https://link.springer.com/book/10.1007/978-3-0348-7469-4))

* [[Kehe Zhu]], Section 14 of: *An Introduction to Operator Algebras*, CRC Press 1993 ([ISBN:9780849378751](https://www.routledge.com/An-Introduction-to-Operator-Algebras/Zhu/p/book/9780849378751))

* [[Richard V. Kadison]], [[John R. Ringrose]], Theorem 4.5.2 in: *Fundamentals of the theory of operator algebras -- Volume I: Elementary Theory*, Graduate Studies in Mathematics **15**, AMS 1997 ([ISBN:978-0-8218-0819-1](https://bookstore.ams.org/gsm-15), [ZMATH] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0888.46039&format=complete))

in the context of [[algebraic quantum field theory]]:

* {#Haag96} [[Rudolf Haag]], _Local  Quantum  Physics:  Fields,  Particles,  Algebras_,   Texts  and  Monographs  in Physics. Springer (1996).

* {#Moretti18} [[Valter Moretti]], _Spectral Theory and Quantum Mechanics :Mathematical Structure of Quantum Theories, Symmetries and introduction to the Algebraic Formulation_, 2nd ed.  Springer Verlag, Berlin (2018)

Review with an eye towards [[quantum probability]] and [[entropy]]:

* A. P. Balachandran, T. R. Govindarajan, Amilcar R. de Queiroz, A. F. Reyes-Lega, Section II of: _Algebraic approach to entanglement and entropy_, Phys. Rev. A 88, 022301 (2013) ([arXiv:1301.1300](http://arxiv.org/abs/1301.1300))

See also 

* Wikipedia, _[Gelfand-Naimark-Segal construction](https://en.wikipedia.org/wiki/Gelfand%E2%80%93Naimark%E2%80%93Segal_construction)_


For general unital [[star-algebras]]: 

* {#KhavkineMoretti15}  [[Igor Khavkine]], [[Valter Moretti]], _Algebraic QFT in Curved Spacetime and quasifree Hadamard states: an introduction_, Chapter 5 in [[Romeo Brunetti]] et al. (eds.) _Advances in Algebraic Quantum Field Theory_, , Springer, 2015

in relation with the classical moment problem and the notion of [[POVM]]

* {#DragoMoretti19} Nicolò Drago,  [[Valter Moretti]], *The notion of observable and the moment problem for $\ast$-algebras and their GNS representations*, Lett. Math. Phys. 2020 ([arXiv.org:1903.07496](https://arxiv.org/abs/1903.07496))

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

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

The _Gelfand-Naimark-Segal construction_ ("GNS construction") represents a [[state on a star-algebra]] over the [[complex numbers]] --- which *a priori* is defined purely algebraically as a non-degenerate positive linear function

$$
  \rho \;\colon\; \mathcal{A} \longrightarrow \mathbb{C}
  \,,
$$

--- by a [[vector]] $\psi \in \mathcal{H}$ in a [[complex numbers|complex]] [[Hilbert space]] $\mathcal{H}$ as the "[[expectation value]]"

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

of $\mathcal{A}$ on (a [[dense subspace]] of) $\mathcal{H}$; where $\langle -,-\rangle$ denotes the [[Hermitian form|Hermitian]] [[inner product]] on the [[Hilbert space]].

Originally and typically by default this is considered for [[C*-algebras]] and [[C*-representations]] ([Gelfand & Naimark 1943](#GelfandNaimark43), [Segal 1947](#Segal47)), see for instance ([Schmüdgen 1090](#Schmuedgen90)), but the construction applies to general [[unital algebra|unital]] [[star algebras]] $\mathcal{A}$ ([Khavkine& Moretti 2015](#KhavkineMoretti15)) as well as to other [[coefficient]] [[rings]], such as to  [[formal power series algebras]] over $\mathbb{C}[ [\hbar] ]$ ([Bordemann & Waldmann 1996](#BordemannWaldmann96)). 

The GNS-construction plays a central role in [[algebraic quantum field theory]] (cf. [Haag 1996](#Haag96), [Moretti 2017](#Moretti17), [Khavkine & Moretti 2015](#KhavkineMoretti15)), where $\mathcal{A}$ plays the role of an [[algebra of observables]] and $\rho \colon \mathcal{A} \to \mathbb{C}$ the role of an actual [[state]] of a [[physical system]] (whence the terminology) jointly constituting the "[[Heisenberg picture]]"-perspective of [[quantum physics]]; so that the GNS-construction serves to re-construct a corresponding [[Hilbert space|Hilbert]] [[space of states]] as in the [[Schrödinger picture]] of quantum physics. In this context the version for [[C*-algebras]] corresponds to [[non-perturbative quantum field theory]], while the generalization to [[formal power series algebras]] corresponds to [[perturbative quantum field theory]].

## Details

> under construction


### For $C^\ast$-algebras
  {#ForCStarAlgebras}

+-- {: .num_theorem}
###### Theorem

Given 

1. a [[C*-algebra]] $\mathcal{A}$;

1. a [[state on a star-algebra|state]] $\rho \;\colon\; \mathcal{A} \to \mathbb{C}$ in the sense of 

   1. a [[linear map]] on the [[underlying]] [[vector space]]

      \[
        \label{UnderlyingLinearMapOfStateExpectationValue}
        \rho \,\colon\, \mathcal{A} \to \mathbb{C}
        \,,
      \]

   1. which takes star-involution to [[complex conjugation]] 
  
      \[
        \label{StateRespectsStar}
        A \in \mathcal{A}
        \;\;\;
           \vdash
        \;\;\;
        \rho(A^\ast) = \overline{\rho(A)}
        \,,
      \]

   1. and satisfies "[positivity](state+on+a+star-algebra#PositivityCondition) in the sense that

      \[
        \label{StateSatisfiesPositivity}
        A \in \mathcal{A}
        \;\;\;
          \vdash
        \;\;\;
        \rho(A^\ast A) \in \mathbb{R}_{\geq 0} \subset \mathbb{C}
       \,,
      \]      

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

such that $\rho$ is the [[pure state]] corresponding to $\psi_\rho$, in that

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

\begin{proof}\label{ProofOfGNS}
Consider on the underlying [[complex vector space]] of $\mathcal{A}$ the [[sesquilinear form]] (inner product)

\[
  \label{InnerProductBeforeDevidingOutNullVectors}
  \langle A,B \rangle_\rho
  \;\coloneqq\;
  \rho
  \big(
    A^\ast B
  \big)
  \,.
\]

By the "[positivity](state+on+a+star-algebra#PositivityCondition)"-condition (eq:StateSatisfiesPositivity) on $\rho$, the pairing $\langle-,-\rangle$ is [positive semi-definite](sesquilinear+form#Definity), and therefore it satisfies the [[Cauchy-Schwarz inequality]]:

\[
  \label{CauchySchwarzBeforeDividingOutNullVectors}
  {\big\vert
    \rho\big( A^\ast B \big) 
  \big\vert}^2 
    \;\leq\; 
  \rho\big(A^\ast A\big)
  \,
  \rho(B^\ast B)
  \,.
\]

However, (eq:InnerProductBeforeDevidingOutNullVectors) will in general not be definite, in that there may be a non-trivial [[linear subspace]] of 0-norm elements:

\[
  \label{TheNullIdeal}
  \mathcal{N} 
    \;\coloneqq\; 
  \big\{
    A \in \mathcal{A}
    \,\vert\,
    \rho(A^\ast A) = 0
  \big\}
  \,,
\]

and hence we have to quotient out by this null-space in order to produce the desired Hilbert space.

Observe that this null space (eq:TheNullIdeal) is not just a [[linear subspace]] but a left [[ideal]] for the algebra structure, as follows by the [[Cauchy-Schwarz inequality]] (eq:CauchySchwarzBeforeDividingOutNullVectors):
 
\[
  \label{NullSpaceIsLeftIdeal}
  \left.
  \begin{array}{l}
    N \in \mathcal{N}
    \\
    A \in \mathcal{A}
  \end{array}
  \right\}
  \;\;\;
  \vdash
  \;\;\;
  \left\{
  \begin{array}{l}
    \big\vert
    \rho\big(
      (A N)^\ast
      A N
    \big)
    \big\vert^2
    \\
    \;=\;
    \big\vert
    \rho\big(
      (N^\ast A^\ast A) N
    \big)
    \big\vert^2
    \\
    \;\leq\;
    \rho\big(
      (N^\ast A^\ast A)
      (N^\ast A^\ast A)^\ast
    \big)
    \,
    \underset{
      = 0
    }{
    \underbrace{
    \rho\big(
      N^\ast N
    \big)
    \,.
    }
    }
  \end{array}
  \right.
\]

Similarly, the [[Cauchy-Schwarz inequality]] (eq:CauchySchwarzBeforeDividingOutNullVectors) implies that any inner product with a null vector vanishes:

\[
  \label{InnerProductWithNullVectorIsNullVector}
  \left.
  \begin{array}{l}
    N \in \mathcal{N}
    \\
    A \in \mathcal{A}
  \end{array}  
  \right\}
  \;\;
  \Rightarrow
  \;\;
  \rho\big(
    A^\ast N
  \big)
  \;=\;
  0
  \,.
\]

Therefore $\langle-,-\rangle$ first of all descends to the [[quotient vector space]] 

\[
  \label{HilbertSpaceAsQuotientOfStarAlgebraByNullSpace}
  \mathscr{H}
  \;\coloneqq\;
  \mathcal{A}/\mathcal{N}
  \,,
\]

because

$$
  \begin{array}{l}
    \big\langle
      A_1
      ,\,
      A_2 + N_2
    \big\rangle
    \\
    \;\equiv\;
    \rho\big(
      A_1^\ast
      (A_2 + N_2)
    \big)
    \\
    \;=\;
    \rho\big(
      A_1^\ast
      A_2
    \big)    
    +
    \rho\big(
      A_1^\ast
      N_2
    \big)    
    \\
    \;=\;
    \rho\big(
      A_1^\ast
      A_2
    \big)    
    \,,
  \end{array}
$$

where in the last step we used (eq:InnerProductWithNullVectorIsNullVector), and from this: 

$$
  \begin{array}{l}
    \big\langle
      A_1 + N_1
      ,\,
      A_2
    \big\rangle
    \\
    \;=\;
    \overline{
    \big\langle
      A_2
      ,\,
      A_1 + N_1
    \big\rangle
    }
    \\
    \;=\;
    \overline{
    \big\langle
      A_2
      ,\,
      A_1
    \big\rangle
    }
    \;=\;
    \big\langle
      A_1
      ,\,
      A_2
    \big\rangle
    \,,
  \end{array}
$$

where in the first and last step we used (eq:StateRespectsStar).

Now descended to the quotient, the pairing $\langle-,-\rangle$ becomes [positive definite](sesquilinear+form#Definity) by construction, so that it defines a [[Hermitian form|Hermitian]] -- by (eq:StateRespectsStar) -- [[inner product]] on $\mathscr{H}$, making it the desired [[Hilbert space]].

Finally, again by the left-ideal property (eq:NullSpaceIsLeftIdeal), the left multiplication [[action]] of $\mathcal{A}$ on itself also descends to an action on the quotient Hilbert space (eq:HilbertSpaceAsQuotientOfStarAlgebraByNullSpace):

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
    \,,
  }
$$

and so the cyclic vector in question is that represented by the [[unit element]] $1 \in \mathcal{A}$:

$$
  \psi_\rho 
    \;\coloneqq\;
  [1]
  \;\in\;
  \mathscr{H}
  \,.
$$

Hence on this Hilbert space $\mathscr{H}$, the original  operator-algebraic state $\rho$ is now represented by the tautological [[density matrix]] 

$$
  \left\vert 
    \psi_\rho 
  \right\rangle 
  \left\langle 
    \psi_\rho 
  \right\rangle
  \;=\;
  {\big\vert [1] \big\rangle} 
  {\big\langle [1] \big\vert}
  \,.
$$
\end{proof}

Notice in summary that this GNS construction constitutes a kind of [[operator-state correspondence]] modulo null operators:

$$
  \begin{array}{rcl}
    \mathcal{A}/\mathcal{N}
    &\xleftrightarrow{\phantom{---}}&
    \mathscr{H}
    \\
    [A] 
      &\mapsto&
    A \cdot \psi_\rho    
  \end{array}
$$


### For $C^\ast$-categories
 {#ForCStarCategories}

The GNS construction for $C^\ast$-algebras is a special case of a more general construction of [Ghez, Lina & Roberts 1985, Prop. 1.9](#GhezLinaRoberts85) applied to [[C*-categories]] ([[horizontal categorification]] of $C^\ast$-algebras):

+--{: .num_theorem}
###### Theorem

Let $\mathcal{C}$ be a [[C-star category|$C^\ast$-category]]. Fix an object $A \in \operatorname{Ob}\mathcal{C}$ and let $\sigma$ be a state on the $C^\ast$-algebra $\mathcal{C}(A,A)$. Then there exists a $*$-representation
$$
\rho_\sigma \colon \mathcal{C} \to \mathbf{Hilb}
$$
together with a cyclic vector $\xi \in \rho_\sigma(A)$ such that for all $x \in \mathcal{C}(A,A)$,
$$
\sigma(x) = \langle \xi, \rho_\sigma(x)\xi \rangle.
$$
=--


A [[C*-algebra]] $\mathcal{A}$ is a $C^\ast$-category with a single [[object]] $\bullet$, where we make the identification $A = \mathcal{A}(\bullet,\bullet)$. In this case the theorem reduces to the classical GNS construction.

## Functorial Aspects
See *[[Functorial Aspects of the GNS Representation]]*.

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

* {#Haag96} [[Rudolf Haag]], *[[Local  Quantum  Physics -- Fields,  Particles,  Algebras]]*,  Texts  and  Monographs  in Physics. Springer (1996).

* {#Moretti17} [[Valter Moretti]], _Spectral Theory and Quantum Mechanics -- Mathematical Foundations of Quantum Theories, Symmetries and Introduction to the Algebraic Formulation_, Springer (2017) &lbrack;[doi:10.1007/978-3-319-70706-8](https://doi.org/10.1007/978-3-319-70706-8)&rbrack;

Review with an eye towards [[quantum probability]] and [[entropy]]:

* A. P. Balachandran, T. R. Govindarajan, Amilcar R. de Queiroz, A. F. Reyes-Lega, Section II of: _Algebraic approach to entanglement and entropy_, Phys. Rev. A 88, 022301 (2013) ([arXiv:1301.1300](http://arxiv.org/abs/1301.1300))

See also 

* Wikipedia, _[Gelfand-Naimark-Segal construction](https://en.wikipedia.org/wiki/Gelfand%E2%80%93Naimark%E2%80%93Segal_construction)_

In the generality of [[C-star category|$C^\ast$-categories]] (and with an eye towards [[W-star category|$W^\ast$-categories]]):

* {#GhezLinaRoberts85} [[P. Ghez]], [[Ricardo Lima]], [[John E. Roberts]], Prop. 1.9 in: *$W^\ast$-categories*,  Pacific J. Math. **120** 1 (1985) 79-109 &lbrack;[euclid:pjm/1102703884](https://projecteuclid.org/journals/pacific-journal-of-mathematics/volume-120/issue-1/Wast-categories/pjm/1102703884.full)&rbrack;

For general unital [[star-algebras]]: 

* {#KhavkineMoretti15}  [[Igor Khavkine]], [[Valter Moretti]], *Algebraic QFT in Curved Spacetime and quasifree Hadamard states: an introduction*, Chapter 5 in: [[Romeo Brunetti]] et al. (eds.) *Advances in Algebraic Quantum Field Theory* Springer (2015) &lbrack;[doi:10.1007/978-3-319-21353-8](https://doi.org/10.1007/978-3-319-21353-8)&rbrack;

and in relation with the classical moment problem and the notion of [[POVM]]:

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
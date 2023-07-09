
> This entry describes a concrete formalization of the general notion of [[state]] in the context of [[quantum probability theory]] and [[algebraic quantum field theory]] and [[operator algebra]]. For other conceptualizations of [[states]] see there.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Algeraic Quantum Field Theory
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

The concept of _state on a star-algebra_ is the formalization of the general idea of *[[states]]* from the point of view of  [[quantum probability theory]] and [[AQFT|algebraic quantum theory]].

In order to motivate the definition from more traditional formulations in  [[physics]], recall that there a _[[state]]_ $\langle - \rangle$ is the information that allows to  assign to each [[observable]] $A$ the [[expectation value]] $\langle A\rangle$ that this observable has when the [[physical system]] is assumed to be in that state.

Often this is formalized in the [[Schrödinger picture]] where a [[Hilbert space|Hilbert]] [[space of states]] $\mathcal{H}$ is taken as primary, and the [[observables]] are [[representation|represented]] as suitable [[linear operators]] $A$ on $\mathcal{H}$. Then for $\psi \in \mathcal{H}$ a state ([[pure state]]) the [[expectation value]] of $A$ in this state is the [[inner product]] $\langle \psi \vert A \vert \psi \rangle \coloneqq (\psi, A \psi)$. This defines a [[linear function]]

$$
  \langle \psi \vert - \vert \psi \rangle
  \;\colon\;
  \mathcal{A}
  \longrightarrow
  \mathbb{C}
$$

on the [[algebra of observables]] $\mathcal{A}$, satisfying some extra properties.

Conversely, in the [[Heisenberg picture]] one may take the "abstract" [[associative algebra|algebra]] [[algebra of quantum observables|of observables]] as primary (i.e. not necessarily manifested as an [[operator algebra]]), and declare that a state is any linear functional

$$
  \langle - \rangle
  \;\colon\;
  \mathcal{A}
  \longrightarrow
  \mathbb{C}
$$

which is _positive_ in that $\langle A^\ast A\rangle \geq 0$ and _normalized_ in that $\langle 1\rangle = 1$.   Under suitable conditions a [[Hilbert space|Hilbert]] [[space of states]] may be (re-)constructed from this *a posteriori* via the _[[GNS construction]]_. 

Traditionally this definition is considered for [[algebras of observables]] which are [[C*-algebras]] (as usually required for [[non-perturbative quantum field theory]], see e.g. [Fredenhagen (2003) Sec. 2](#Fredenhagen03), [Landsman (2017) Def. 2.4](#Landsman17)), but the definition makes sense generally for plain [[star-algebras]] ([Meyer (1995), I.1.1](#Meyer95)), such as for instance for the [[formal power series algebras]] that appear in [[perturbative quantum field theory]] (e.g. [Bordemann-Waldmann (1996) Def. 1](#BordemannWaldmann96), [Fredenhagen & Rejzner (2012) Def. 2.4](#FredenhagenRejzner12), [Khavkine & Moretti (2015) Def. 6](#KhavkineMoretti15), [Dütsch (2018) Def. 2.11](#Duetsch18)).

{#AsPositiveLinearFunctionals} Of course, the notion of states depends only on the $\ast$-algebra's [[underlying]] [[partial order|partially ordered]] [[complex vector space]] (see [here](C-star-algebra#PartialOrderAndPositiveElements)) and hence makes sense in the generality of any [[partial order|partially ordered]] [[vector space]], in which case one refers to them also as *positive linear functionals* or similar (e.g. [Murphy (1990) §3.3](#Murphy90)).

The perspective that states are normalized positive linear functionals on the algebra of observables is implicit in traditional [[perturbative quantum field theory]], where it is encoded in the [[2-point function]] corresponding to a [[vacuum state]] or more generally a [[quasi-free quantum state]] (the _[[Hadamard propagator]]_).  The perspective is made explicit in [[algebraic quantum field theory]] (see e.g. [Fredenhagen 03, section 2](#Fredenhagen03)) and for [[star-algebras]] of observables that are not necessarily [[C*-algebras]] in [[perturbative algebraic quantum field theory]] (e.g. [Bordemann-Waldmann 96](#BordemannWaldmann96), [Fredenhagen-Rejzner 12, def. 2.4](#FredenhagenRejzner12), [Khavkine-Moretti 15, def. 6](#KhavkineMoretti15), [Dütsch 18, def. 2.11](#Duetsch18)).



## Definition

### For unital star algebras
 {#DefinitionForUnitalStarAlgebras}

+-- {: .num_defn #StateOnAStarAlgebra}
###### Definition
**([[state]] on a [[unital algebra|unital]] [[star algebra]])**

Let $\mathcal{A}$ be a [[unital]] [[star-algebra]] over the [[complex numbers]] $\mathbb{C}$. A _state_ on $\mathcal{A}$ is a [[linear function]]

$$
  \rho \;\colon\; \mathcal{A} \longrightarrow \mathbb{C}
$$

such that

1. {#PositivityCondition} (positivity) for all $A \in \mathcal{A}$ the value of $\rho$ on the product $A^\ast A$ is 

   1. [[real part|real]] $\,\rho(A^\ast A) \in \mathbb{R} \hookrightarrow \mathbb{C}$ 

   1. as such [[non-negative real number|non-negative]]: 

   \[
     \label{Positivity}
     \rho(A^\ast A) \geq 0
   \]

1. (normalization) 
   
   \[
     \label{Normalization}
     \rho(\mathbf{1}) = 1
   \]

   for $\mathbf{1} \in \mathcal{A}$ the [[unit]] in the algebra.

=--

(e.g. [Meyer 95, I.1.1](#Meyer95), [Bordemann-Waldmann 96](#BordemannWaldmann96), [Fredenhagen-Rejzner 12, def. 2.4](#FredenhagenRejzner12), [Khavkine-Moretti 15, def. 6](#KhavkineMoretti15), [Landsman 2017, Def. 2.4](#Landsman17))

+-- {: .num_remark}
###### Remark
**([[probability theory|probability theoretic]] interpretation of [[state on a star-algebra]])**

A [[star algebra]] $\mathcal{A}$ equipped with a [[state on a star-algebra|state]] is also called a _[[quantum probability space]]_, at least when $\mathcal{A}$ is in fact a [[von Neumann algebra]].

=--

+-- {: .num_remark #StatesFormAConvexSet}
###### Remark
**([[state on a star-algebra|states]] form a [[convex set]])**

For $\mathcal{A}$ a unital [[star-algebra]], the [[set]] of states on $\mathcal{A}$ according to def. \ref{StateOnAStarAlgebra} is naturally a [[convex set]]: For $\rho_1, \rho_2 \colon \mathcal{A} \to \mathbb{C}$ two states then for every $p \in [0,1] \subset \mathbb{R}$ also the [[linear combination]]

$$
  \array{
    \mathcal{A}
     &\overset{p \rho_1 + (1-p) \rho_2}{\longrightarrow}&
    \mathbb{C}
    \\
    A &\mapsto& p \rho_1(A) + (1-p) \rho_2(A)
  }
$$
 

is a state.

=--

+-- {: .num_defn #PureStateOnAStarAlgebra}
###### Definition
**([[pure state]])**

A state $\rho \colon \mathcal{A} \to \mathbb{C}$ on a unital [[star-algebra]] (def. \ref{StateOnAStarAlgebra}) is called a _[[pure state]]_ if it is extremal in the [[convex set]] of all states (remark \ref{StatesFormAConvexSet}) in that an identification

$$
  \rho = p \rho_1 + (1-p) \rho_2
$$

for $p \in (0,1)$ implies that $\rho_1 = \rho_2$ (hence $= \rho$).

=--


### For $C^\ast$-Algebras

The following discusses states specifically on [[C*-algebras]].

+-- {: .num_defn}
###### Definition

An element $A$ of an (abstract) $C^*$-algebra is called **[[positive operator|positive]]** if it is [[self-adjoint operator|self-adjoint]] and its [[spectrum of an operator|spectrum]] is contained in $[0, \infinity)$. We write $A \ge 0$ and say that the set of all [[positive operators]] is the positive cone (of a given $C^*$-algebra).
=--

+-- {: .num_remark}
###### Remark

This definition is motivated by the [[Hilbert space]] situation, where an operator $A \in \mathcal{B} (\mathcal{H})$ is called [[positive operator|positive]] if for every vector $x \in \mathcal{H}$ the inequality $ \langle x, A x \rangle \ge 0$ holds. If the abstract $C^*$-algebra of the definition above is represented on a Hilbert space, then we see that by [[functional calculus]] we can define a self adjoint operator $B$ by $B \coloneqq f(A)$ with $f(t) := t^{1/2}$ and get  $ \langle x, A x \rangle = \langle B x, B x \rangle \ge 0$. This shows that the positive elements of the abstract algebra, if represented on a Hilbert space, become positive operators as defined here in the Hilbert space setting.

=--

+-- {: .num_defn}
###### Definition

A [[linear functional]] $\rho$ on an $C^*$-algebra is **positive** if $A \ge 0$ implies that  $\rho(A) \ge 0$.

A **state** of a unital $C^*$-algebra is [[linear functional]] $\rho$ such that $\rho$ is positive and $\rho(1) = 1$.

=--

Though the mathematical notion of state is already close to what physicists have in mind, they usually restrict the set of states further and consider normal states only. We let $\mathcal{R}$ be an $C^*$-algebra and $\pi$ an representation of $\mathcal{R}$ on a Hilbert space $\mathcal{H}$.
 

+-- {: .num_theorem}
###### Definition/Theorem

A **normal state** $\rho$ is a state that satisfies one of the following equivalent conditions:

* $\rho$ is weak-operator continuous on the unit ball of $\pi(\mathcal{R})$.

* $\rho$ is strong-operator continuous on the unit ball $\pi(\mathcal{R})$.

* $\rho$ is ultra-weak continuous.

* There is an operator $A$ of [[trace class]] of $\mathcal{H}$ with $tr(A) = 1$ such that $\rho(\pi(R)) = tr(A \pi(R))$ for all $R \in \mathcal{R}$.

=--

This appears as [KadisonRingrose, def. 7.1.11, theorem 7.1.12](#KadisonRingrose)


+-- {: .num_remark}
###### Remark

This list is not complete, there are more commonly used equivalent characterizations of normal states.

The last one is most frequently used by physicists, in that context the operator $A$ is also called a [[density matrix]] or density operator.

=--



Sometimes the observables of a system are described by an abstract $C^*$-algebra, in this case an important notion is the folium:

+-- {: .num_defn}
###### Definition
The **folium** of a representation $\pi$ of an $C^*$-algebra  $\mathcal{R}$ on a Hilbert space is the set of normal states of $\pi(\mathcal{R})$.
=--

+-- {: .num_defn}
###### Definition
A state $\rho$ of a representation is called a **vector state** if there is a $x \in \mathcal{H}$ such that $\rho(\pi(R)) = \langle \pi(R)x, x \rangle$ for all $R \in \mathcal{R}$.
=--

+-- {: .num_theorem}
###### Theorem
Normal states are vector states if $\mathcal{R}$ is a [[von Neumann algebra]] with a separating vector. More precisely: Let $\mathcal{R}$ be a von Neumman algebra acting on a Hilbert space $\mathcal{H}$, let $\rho$ be a normal state of $\mathcal{R}$ and $x \in \mathcal{H}$ be a separating vector for $\mathcal{R}$, then there is a $y \in \mathcal{H}$ such that $\rho(R) = \langle Ry, y \rangle$ for all $R \in \mathcal{R}$.
=--

This appears as [KadisonRingrose, theorem 7.2.3](#KadisonRingrose).

The set of states of an $C^*$-algebra is sometimes called the **[[space of quantum states|state space]]**.

The state space is non-empty (define a state on the subalgebra $\mathbb{C} 1$ and extend it to the whole $C^*$-algebra via the [[Hahn-Banach theorem]]), convex and weak$^*$-compact, so it has extreme points. By the [[Krein-Milman theorem]] (see Wikipedia: [Krein-Milman theorem] (http://en.wikipedia.org/wiki/Krein%E2%80%93Milman_theorem)) it is the weak$^*$-closure of its extreme points.

+-- {: .num_defn}
###### Definition
A **pure state** is a state that is an extreme point of the state space.
=--

The term "pure" originates from the notion of [[entanglement]], a pure state is not a mixture of two distinct other states.


## Examples
 {#Examples}

\begin{example}\label{ClassicalProbabilityMeasureAsStateOnMeasurableFunctions}
**(classical [[probability measure]] as state on [[measurable functions]])**
\linebreak
For $\Omega$ a [[locally compact topological space|locally compact]] [[Hausdorff space]] equipped with a compatible structure of a classical [[probability space]], hence a [[measure space]] which normalized total measure $\int_\Omega d\mu = 1$, let $\mathcal{A} \coloneqq C_0(\Omega)$ be the algebra of [[continuous function]] with values in the [[complex numbers]] and [[vanishing at infinity]], regarded as a [[star algebra]] by pointwise [[complex conjugation]]. Then forming the [[expectation value]] with respect to $\mu$ defines a [[state on a star-algebra|state]] (def. \ref{StateOnAStarAlgebra}):

$$
  \array{
    C_0(\Omega) 
      &\overset{\langle - \rangle_\mu}{\longrightarrow}& 
    \mathbb{C}
    \\
    A &\mapsto& \int_\Omega A \, d\mu
  }
$$

\end{example}

(e.g. [Landsman 2017, p. 16-17](#Landsman17))



+-- {: .num_example #ElementsOfHilbertSpaceAsPureStates}
###### Example
**(elements of a [[Hilbert space]] as [[pure states]] on [[bounded operators]])**

Let $\mathcal{H}$ be a [[complex numbers|complex]] [[separable Hilbert space|separable]] [[Hilbert space]] with [[inner product]] $\langle -,-\rangle$ and let $\mathcal{A} \coloneqq \mathcal{B}(\mathcal{H})$ be the algebra of [[bounded operators]], regarded as a [[star algebra]] under forming [[adjoint operators]]. Then for every element $\psi \in \mathcal{H}$ of unit [[norm]] $\langle \psi,\psi\rangle = 1$ there is the [[state on a star-algebra|state]] (def. \ref{StateOnAStarAlgebra}) given by

$$
  \array{
    \mathcal{B}(\mathcal{H})
      &\overset{\langle -\rangle_\psi}{\longrightarrow}&
     \mathbb{C}
     \\
     A &\mapsto& \langle \psi \vert\, A \, \vert \psi \rangle &\coloneqq& \langle \psi, A \psi \rangle
  }
$$

These are [[pure states]] (def. \ref{PureStateOnAStarAlgebra}).

More general states in this case are given by [[density matrices]].

=--



\begin{example}
\label{StatesOnGroupAlgebrasAreUnitaryRepresentations}
**(states on group algebras are unitary representations)**
\linebreak
  Let $G$ be a [[discrete group]] and $\mathbb{C}[G]$ its [[group algebra]] regarded as a complex [[star-algebra]] under the combined operation of [[inverse element|inversion]] of group elements and [[complex conjugation]] of the [[coefficients]].

Then each state $\rho \,\colon\,\mathbb{C}[G] \longrightarrow \mathbb{C}$ arises from a [[unitary representation]] $\widehat{(\text{-})} \,\colon\, \longrightarrow U(\mathscr{H})$ on a [[Hilbert space]] $(\mathscr{H}, \langle -\vert-\rangle)$ with a [[cyclic vector]] $\psi \in \mathscr{H}$ as
$$
  \rho(g)
  \;=\;
  \big\langle 
    \psi 
   \big\vert 
    \widehat{g} \cdot \psi
  \big\rangle
  \,.
$$

The statement generalizes to [[topological groups]] in a suitable way.
\end{example} 

This is due to [Gelfand & Raikov (1943) (2)](#GelfandRaikov43), [Naimark (1956) §30 Thm. 1](#Naimark56) (reviewed at [eom](https://encyclopediaofmath.org/wiki/Positive-definite_function)) further generalization in [Saworotnow (1970)](#Saworotnow70), [(1972)](Saworotnow72), textbook account in in [Dixmier (1977) Thm. 13.4.5 (ii)](#Dixmier77).

## Properties

### Closure properties

\begin{example}\label{Mixtures}
**(mixtures, convex combinations)**

For $k \in \mathbb{N}_+$, let 

* $\big( \rho_i \colon \mathcal{A} \to \mathbb{C}  \big)_{i = 1}^k$

  be a $k$-[[tuple]] of states;

* $\big( p_i \in \mathbb{R}_{\geq 0} \big)_{i = 1}^k$, 
  $\underoverset{i = 1}{k}{\sum} p_i \;=\; 1$ 

  be a [[probability distribution]] on the [[finite set]] $\{1, \cdots, k\}$

then the [[convex combination]]

$$
  \underoverset{i = 1}{k}{\sum} p_i \cdot \rho_i
  \;\;\;
  \in
  \;
  \mathcal{A}^\ast
$$

is another state on the star-algebra $\mathcal{A}$.


\end{example}

\begin{prop}\label{OperatorStateCorrespondence}
**(operator-state correspondence)**

For $\rho \;\colon\; \mathcal{A} \to \mathbb{C}$ a state, with a non-null observable $O \in \mathcal{A}$, $\rho(O^\ast O) \neq 0$, then also

\[
  \label{OperatorImageOfState}
  \rho_O
  \;\colon\;
  A 
    \;\mapsto\; 
  \tfrac{1}{ \rho(O^\ast O) }
  \cdot
  \rho\big( O^\ast \cdot A \cdot O \big)
\]

is a state.

\end{prop}
\begin{proof}

To check positivity (eq:Positivity), we compute for any $A \in \mathcal{A}$ as follows:

$$
  \begin{aligned}
    \rho_O
    \big(
      A^\ast
      \cdot
      A
    \big)
    & =
    \tfrac{1}{\rho(O^\ast O)}
    \cdot
    \rho
    \big(
      O^\ast
      \cdot
      (
        A^\ast
        \cdot
        A
      )
      \cdot
      O
    \big)
    \\
    & =
    \tfrac{1}{\rho(O^\ast O)}
    \cdot
    \rho
    \big(
      (
        A \cdot O
      )^\ast
      \cdot
      (
        A
        \cdot
        O
      )
    \big)
    \\
    & \geq 0
    \,,
  \end{aligned}
$$

where the first step is the definition (eq:OperatorImageOfState) the second step uses the [[anti-homomorphisms]]-property of the star-involution, and the last step follows by the assumed positivivity of $\rho$.

To check normalization (eq:Normalization), we observe that:

$$
  \begin{aligned}
    \rho_O(\mathbf{1})
    & =
    \tfrac{1}{\rho(O^\ast O)}
    \cdot
    \rho
    \big(
      O^\ast \cdot \mathbf{1} \cdot O
    \big)
    \\
    & =
    \tfrac{1}{\rho(O^\ast O)}
    \cdot
    \rho
    \big(
      O^\ast \cdot O
    \big)
    \\
    & = 1
    \,.
  \end{aligned}
$$

\end{proof}

### Fell's theorem

See at *[[Fell's theorem]]*.

### Gleason's theorem

See at *[[Gleason's theorem]]*.




## Related concepts

* [[GNS construction]]

[[!include states and observables -- content]]


## References 

### Exposition

* {#Meyer95} [[Paul-André Meyer]], Section I.1.1 in: *Quantum Probability for Probabilists*,  Lecture Notes in Mathematics **1538**, Springer 1995 ([doi:10.1007/BFb0084701](https://link.springer.com/book/10.1007/BFb0084701))

* {#Gleason09} [[Jonathan Gleason]], *The $C^*$-algebraic formalism of quantum mechanics* (2009) &lbrack;[[Gleason09.pdf:file]], [[GleasonAlgebraic.pdf:file]]&rbrack;

* {#Gleason11} [[Jonathan Gleason]], *From Classical to Quantum: The $F^\ast$-Algebraic Approach*, contribution to *[VIGRE REU 2011](http://www.math.uchicago.edu/~may/VIGRE/VIGREREU2011.html)*, Chicago (2011) &lbrack;[pdf](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Gleason.pdf), [[GleasonFAlgebraic.pdf:file]]&rbrack;

Textbook account:

* {#BratteliRobinson79} [[Ola Bratteli]], [[Derek W. Robinson]], §2.3 in: *Operator Algebras and Quantum Statistical Mechanics* -- vol 1: *$C^\ast$- and $W^\ast$-Algebras. Symmetry Groups. Decomposition of States.*, Springer (1979, 1987, 2002) &lbrack;[doi:10.1007/978-3-662-02520-8](https://doi.org/10.1007/978-3-662-02520-8)&rbrack;

Discussion under the name "positive linear functionals":

* {#Steward76} [[James D. Steward]], *Positive definite functions and generalizations, an historical survey*, The Rocky Mountain Journal of Mathematics **6** 3 (1976) 409-434 &lbrack;[jstor:44236118](https://www.jstor.org/stable/44236118)&rbrack;

* {#Dixmier77} [[Jacques Dixmier]], §2 of: *$C^\ast$-algebras*, North Holland (1977)

* {#Murphy90} [[Gerard Murphy]], §3.3 in: _$C^\ast$-algebras and Operator Theory_, Academic Press (1990) &lbrack;[doi:10.1016/C2009-0-22289-6](https://doi.org/10.1016/C2009-0-22289-6)&rbrack;

* Wikipedia, *[Positive linear functional](https://en.wikipedia.org/wiki/Positive_linear_functional)*

* [[eom]], *[Positive-definite function](https://encyclopediaofmath.org/wiki/Positive-definite_function)*

With an eye towards [[density matrices]] and their [[entropy]]:

* Paolo Facchi, Giovanni Gramegna, Arturo Konderak, around (6) in: *Entropy of quantum states* ([arXiv:2104.12611](https://arxiv.org/abs/2104.12611), [spire:1860877](https://inspirehep.net/literature/1860877))

With an eye towards [[Gelfand-Tsetlin algebra|Gelfand-Tsetlin algebras]] and in the generality of [[conditional expectation values]]:

* [[Anatoly Vershik]], Def. 1 in: *Gel'fand-Tsetlin algebras, expectations, inverse limits, Fourier analysis*, pp. 619 in: [[Pavel Etingof]], [[Vladimir S. Retakh]], [[Isadore Singer]] (eds.) *The Unity of Mathematics* In Honor of the Ninetieth Birthday of [[I. M. Gelfand]], ([arXiv:math/0503140](https://arxiv.org/abs/math/0503140), [ISBN:978-0-8176-4467-3](https://www.springer.com/gp/book/9780817640767))


### Original articles

* {#KadisonRingrose} Richard Kadison, John Ringrose, _Fundamentals of the theory of operator algebras_, AMS (1991)

* {#BordemannWaldmann96} [[Martin Bordemann]], [[Stefan Waldmann]], _Formal GNS Construction and States in Deformation Quantization_, Commun. Math. Phys. (1998) 195: 549.  ([arXiv:q-alg/9607019](https://arxiv.org/abs/q-alg/9607019), [doi:10.1007/s002200050402](https://doi.org/10.1007/s002200050402))

* {#Fredenhagen03} [[Klaus Fredenhagen]], section 2 of _Algebraische Quantenfeldtheorie_, lecture notes, 2003 ([[FredenhagenAQFT2003.pdf:file]])

* {#HalvorsonMueger06} [[Hans Halvorson]], [[Michael Müger]], def. 1.11 in _Algebraic Quantum Field Theory_ ([arXiv:math-ph/0602036](https://arxiv.org/abs/math-ph/0602036))

* {#FredenhagenRejzner12} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], definition 2.4 in _Perturbative algebraic quantum field theory_, In _Mathematical Aspects of Quantum Field Theories_, Springer 2016 ([arXiv:1208.1428](https://arxiv.org/abs/1208.1428))

* {#KhavkineMoretti15}  [[Igor Khavkine]], [[Valter Moretti]], _Algebraic QFT in Curved Spacetime and quasifree Hadamard states: an introduction_, Chapter 5 in [[Romeo Brunetti]] et al. (eds.) _Advances in Algebraic Quantum Field Theory_, Springer, 2015 ([arXiv:1412.5945](https://arxiv.org/abs/1412.5945))

* {#Rejzner16} [[Katarzyna Rejzner]], section 2.1.2 of _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))

* {#FredenhagenLindner13} [[Klaus Fredenhagen]], Falk Lindner, _Construction of KMS States in Perturbative QFT and Renormalized Hamiltonian Dynamics_, Communications in Mathematical Physics Volume 332, Issue 3, pp 895-932, 2014-12-01 ([arXiv:1306.6519](https://arxiv.org/abs/1306.6519))

* {#Landsman17} [[Klaas Landsman]], around def. 2.4 in _Foundations of quantum theory -- From classical concepts to Operator algebras_, Springer Open 2017 ([doi:10.1007/978-3-319-51777-3](https://link.springer.com/book/10.1007/978-3-319-51777-3), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf))


* {#Duetsch18} [[Michael Dütsch]], section 2.5 of _[[From classical field theory to perturbative quantum field theory]]_, 2018

* Nicolò Drago, [[Valter Moretti]], _The notion of observable and the moment problem for $\ast$-algebras and their GNS representations_ ([doi:1903.07496](https://arxiv.org/abs/1903.07496), [spire:1725528](http://inspirehep.net/record/1725528))

For more references see at _[[operator algebra]]_.

### The case of group algebras

The characterization of states on [[group algebras]]:

* {#GelfandRaikov43} И. М. Гельфанд, Д. А. Райков, *Неприводимые унитарные представления локально бикомпактных групп*, Матем. сб., 13(55):2–3 (1943)  301–316 &lbrack;[mathnet pdf](https://www.mathnet.ru/links/728d630fdf2220b1ea8bdb2a5f6a5488/sm6181.pdf)&rbrack;

  \linebreak

  [[Israel Gelfand]], [[Dmitri Raikov]], *Irreducible unitary representations of locally bicompact groups*, Recueil Mathématique. N.S., 13(55) 2–3 (1943) 301–316 &lbrack;[mathnet:eng/sm6181](https://www.mathnet.ru/eng/sm6181)&rbrack;

* {#Naimark56} [[Mark A. Naimark]], *Normed Rings*, Moscow (1956)

* {#Saworotnow70} Parfeny P. Saworotnow, *Representation of a topological group on a Hilbert module*, Duke Math. J. **37** 1  (1970) 145-150 &lbrack;[doi:10.1215/S0012-7094-70-03720-8](https://projecteuclid.org/journals/duke-mathematical-journal/volume-37/issue-1/Representation-of-a-topological-group-on-a-Hilbert-module/10.1215/S0012-7094-70-03720-8.short)&rbrack;

* {#Saworotnow72} Parfeny P. Saworotnow, *Generalized Positive Linear Functionals on a Banach Algebra with an Involution*, Proceedings of the AMS, **31** 1 (1972) 299-304  &lbrack;[jstor:2038564](https://www.jstor.org/stable/2038564)&rbrack;

* [Steward (1976) §4](#Steward76)

* [Dixmier (1977) Thm. 13.4.6](#Dixmier77)

* [[eom]], *[Positive-definite function](https://encyclopediaofmath.org/wiki/Positive-definite_function)*

* Wikipedia, *[Positive-definite function on a group](https://en.wikipedia.org/wiki/Positive-definite_function_on_a_group)*

[[!redirects states on a star-algebra]]

[[!redirects states on star-algebras]]

[[!redirects state on a C-star algebra]]
[[!redirects states on a C-star algebra]]
[[!redirects state on a C* algebra]]
[[!redirects states on a C* algebra]]

[[!redirects state on an operator algebra]]
[[!redirects state of an operator algebra]]
[[!redirects states of an operator algebra]]
[[!redirects states of operator algebras]]
[[!redirects state on an operator algebra]]
[[!redirects states on an operator algebra]]
[[!redirects states on operator algebras]]
[[!redirects state in AQFT]]
[[!redirects states in AQFT]]
[[!redirects state in operator algebra]]
[[!redirects states in operator algebra]]
[[!redirects state in AQFT and operator algebra]]
[[!redirects states in AQFT and operator algebra]]
[[!redirects state of an algebra]]
[[!redirects states of an algebra]]
[[!redirects states of algebras]]
[[!redirects state on an algebra]]
[[!redirects states on an algebra]]
[[!redirects states on algebras]]

[[!redirects normal state]]
[[!redirects normal states]]

[[!redirects positive-definite function]]
[[!redirects positive-definite functions]]

[[!redirects positive linear functional]]
[[!redirects positive linear functionals]]


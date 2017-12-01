
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
#### AQFT
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

> This entry describes a concrete formalization of the general notion of [[state]] in the context of [[AQFT]] and [[operator algebra]].

# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

In [[physics]], a _[[state]]_ $\langle - \rangle$ is the information that allows to  assign to each [[observable]] $A$ the [[expectation value]] $\langle A\rangle$ that this observable has when the [[physical system]] is assumed to be in that state.

Often this is formalized in the [[Schrödinger picture]] where a [[Hilbert space|Hilbert]] [[space of states]] $\mathcal{H}$ is taken as primary, and the [[observables]] are [[representation|represented]] as suitable [[linear operators]] $A$ on $\mathcal{H}$. Then for $\psi \in \mathcal{H}$ a state ([[pure state]]) the [[expectation value]] of $A$ in this state is the [[inner product]] $\langle \psi \vert A \vert \psi \rangle \coloneqq (\psi, A \psi)$. This defines a [[linear function]]

$$
  \langle \psi \vert (-) \vert \psi \rangle
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
  \mathcal{C}
$$

which is _positive_ in that $\langle A^\ast A\rangle \geq 0$ and _normalized_ in that $\langle 1\rangle = 1$.   Under suitable conditions a [[Hilbert space|Hilbert]] [[space of states]] may be (re-)constructed from this a posteriori via the _[[GNS construction]]_. 

Tranditionally this definition is considered for [[algebras of observables]] which are [[C*-algebras]] (as usually required for [[non-perturbative quantum field theory]], see e.g. [Fredenhagen 03, section 2](#Fredenhagen03)), but the definition makes sense generally for plain [[star-algebras]], such as for instance for the [[formal power series algebras]] that appear in [[perturbative quantum field theory]] (e.g. [Fredenhagen-Rejzner 12, def. 2.4](#FredenhagenRejzner12)).

The perspective that states are normalized positive linear functionals on the algebra of observables is implicit in traditional [[perturbative quantum field theory]], where it is encoded in the [[2-point function]] corresponding to a [[vacuum state]] or more generally a [[quasi-free quantum state]] (the _[[Hadamard propagator]]_).  The perspective is made explicit in [[algebraic quantum field theory]] (see e.g. [Fredenhagen 03, section 2](#Fredenhagen03)) and for [[star-algebras]] of observables that are not necessarily [[C*-algebras]] in [[perturbative algebraic quantum field theory]] (e.g. [Fredenhagen-Rejzner 12, def. 2.4](#FredenhagenRejzner12)).



## Definition

The definition of a state relies on the notion of _positivity_ of the elements of an [[star-algebra]]. The following discusses this assuming [[C* algebra]] structure.

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

This apears as [KadisonRingrose, def. 7.1.11, theorem 7.1.12](#KadisonRingrose)


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

The state space is non-empty (define a state on the subalgebra $\mathbb{C} 1$ and extend it to the whole $C^*$-algebra via the [[Hahn-Banach theorem]]), convex and weak$^*$-compact, so it has extreme points. By the  [[Krein-Milman theorem]] (see Wikipedia: [Krein-Milman theorem] (http://en.wikipedia.org/wiki/Krein%E2%80%93Milman_theorem)) it is the weak$^*$-closure of its extreme points.

+-- {: .num_defn}
###### Definition
A **pure state** is a state that is an extreme point of the state space.
=--

The term "pure" originates from the notion of [[entanglement]], a pure state is not a mixture of two distinct other states.


## Properties

An important theorem for the physical interpretation of states is [[Fell's theorem]].


## Examples 

...


## Related concepts


* [[state]], [[quasi-state]]

* [[quasi-free state]]

* [[vacuum state]]
   
* [[Hadamard state]]

* [[Alfsen-Shultz theorem]]


## References 

* {#KadisonRingrose} Richard Kadison, John Ringrose, _Fundamentals of the theory of operator algebras_, AMS (1991)

* {#Fredenhagen03} [[Klaus Fredenhagen]], section 2 of _Algebraische Quantenfeldtheorie_, lecture notes, 2003 ([[FredenhagenAQFT2003.pdf:file]])

* {#HalvorsonMueger06} [[Hans Halvorson]], [[Michael Müger]], def. 1.11 in _Algebraic Quantum Field Theory_ ([arXiv:math-ph/0602036](https://arxiv.org/abs/math-ph/0602036))

* {#FredenhagenRejzner12} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], definition 2.4 in _Perturbative algebraic quantum field theory_, In _Mathematical Aspects of Quantum Field Theories_, Springer 2016 ([arXiv:1208.1428](https://arxiv.org/abs/1208.1428))

* {#Rejzner16} [[Katarzyna Rejzner]], section 2.1.2 of _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))

* {#FredenhagenLindner13} [[Klaus Fredenhagen]], Falk Lindner, _Construction of KMS States in Perturbative QFT and Renormalized Hamiltonian Dynamics_, Communications in Mathematical Physics Volume 332, Issue 3, pp 895-932, 2014-12-01 ([arXiv:1306.6519](https://arxiv.org/abs/1306.6519))


For more references see at _[[operator algebra]]_.

[[!redirects states on a star-algebra]]

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


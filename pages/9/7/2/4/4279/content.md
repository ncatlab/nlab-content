
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

This entry describes a concrete formalization of the general notion of [[state]] in the context of [[AQFT]] and [[operator algebra]].

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The [[AQFT|Heisenberg picture]] of [[quantum mechanics]] is sometimes formalized by describing the [[observables]] of a quantum system by an [[operator algebra]], and the [[state]] of the system as a state of the algebra. 

The first "state" in the preceding sentence is the state the described physical system is in, the second one is the mathematical counterpart we are about to define, that inherited it's name from the physical concept. 
This is the viewpoint of the [[AQFT]] approach to [[quantum field theory]], especially of the [[Haag-Kastler approach]].

We provide the definition of states and several associated properties and explain the physical interpretation and motivation of these concepts from the viewpoint of [[AQFT]].

## Definition ##

The definition of a state relies on the notion of positivity of the elements of an operator algebra, for which we need the structure of a [[C-star algebra]].  

+-- {: .un_def}
###### Definition
An element $A$ of an (abstract) $C^*$-algebra is called **positive** if it is [[self-adjoint operator|self-adjoint]] and its [[spectrum of an operator|spectrum]] is contained in $[0, \infinity)$. We write $A \ge 0$ and say that the set of all positive operators is the positive cone (of a given $C^*$-algebra).
=--

+-- {: .un_remark}
###### Remark

This defintion is motivated by the Hilbert space situation, where an operator $A \in \mathcal{B} (\mathcal{H})$ is called positive if for every vector $x \in \mathcal{H}$ the inequality $ \langle x, A x \rangle \ge 0$ holds. If the abstract $C^*$-algebra of the definition above is represented on a Hilbert space, then we see that by [[functional calculus]] we can define a self adjoint operator $B$ by $B \coloneqq f(A)$ with $f(t) := t^{1/2}$ and get  $ \langle x, A x \rangle = \langle B x, B x \rangle \ge 0$. This shows that the positive elements of the abstract algebra, if represented on a Hilbert space, become positive operators as defined here in the Hilbert space setting.

=--

+-- {: .un_def}
###### Definition

A [[linear functional]] $\rho$ on an $C^*$-algebra is **positive** if $A \ge 0$ implies that  $\rho(A) \ge 0$.

A **state** of a unital $C^*$-algebra is [[linear functional]] $\rho$ such that $\rho$ is positive and $\rho(\mathbb{1}) = 1$.

=--

Though the mathematical notion of state is already close to what physicists have in mind, they usually restrict the set of states further and consider normal states only. We let $\mathcal{R}$ be an $C^*$-algebra and $\pi$ an representation of $\mathcal{R}$ on a Hilbert space $\mathcal{H}$.
 

+-- {: .un_theorem}
###### Definition/Theorem

A **normal state** $\rho$ is a state that satisfies one of the following equivalent conditions:

* $\rho$ is weak-operator continuous on the unit ball of $\pi(\mathcal{R})$.

* $\rho$ is strong-operator continuous on the unit ball $\pi(\mathcal{R})$.

* $\rho$ is ultra-weak continuous.

* There is an operator $A$ of [[trace class]] of $\mathcal{H}$ with $tr(A) = 1$ such that $\rho(\pi(R)) = tr(A \pi(R))$ for all $R \in \mathcal{R}$.

=--

This apears as [KadisonRingrose, def. 7.1.11, theorem 7.1.12](#KadisonRingrose)


+-- {: .un_remark}
###### Remark

This list is not complete, there are more commonly used equivalent characterizations of normal states.

The last one is most frequently used by physicists, in that context the operator $A$ is also called a [[density matrix]] or density operator.

=--



Sometimes the observables of a system are described by an abstract $C^*$-algebra, in this case an important notion is the folium:

+-- {: .un_def}
###### Definition
The **folium** of a representation $\pi$ of an $C^*$-algebra  $\mathcal{R}$ on a Hilbert space is the set of normal states of $\pi(\mathcal{R})$.
=--

+-- {: .un_def}
###### Definition
A state $\rho$ of a representation is called a **vector state** if there is a $x \in \mathcal{H}$ such that $\rho(\pi(R)) = \langle \pi(R)x, x \rangle$ for all $R \in \mathcal{R}$.
=--

+-- {: .un_theorem}
###### Theorem
Normal states are vector states if $\mathcal{R}$ is a [[von Neumann algebra]] with a separating vector. More precisely: Let $\mathcal{R}$ be a von Neumman algebra acting on a Hilbert space $\mathcal{H}$, let $\rho$ be a normal state of $\mathcal{R}$ and $x \in \mathcal{H}$ be a separating vector for $\mathcal{R}$, then there is a $y \in \mathcal{H}$ such that $\rho(R) = \langle Ry, y \rangle$ for all $R \in \mathcal{R}$.
=--

This appeas as [KadisonRingrose, theorem 7.2.3](#KadisonRingrose).

The set of states of an $C^*$-algebra is sometimes called the **state space**.

The state space is non-empty (define a state on the subalgebra $\mathbb{C} \mathbb{1}$ and extend it to the whole $C^*$-algebra via the [[Hahn-Banach theorem]]), convex and weak$^*$-compact, so it has extreme points. By the  [[Krein-Milman theorem]] (see Wikipedia: [Krein-Milman theorem] (http://en.wikipedia.org/wiki/Krein%E2%80%93Milman_theorem)) it is the weak$^*$-closure of it's extreme points.

+-- {: .un_def}
###### Definition
A **pure state** is a state that is an extreme point of the state space.
=--

The term "pure" originates from the notion of [[entanglement]], a pure state is not a mixture of two distinct other states.

## Properties ##

An important theorem for the physical interpretation of states is [[Fell's theorem]].

## Examples 
...

## References 

* Richard Kadison, John Ringrose, _Fundamentals of the theory of operator algebras_ AMS (1991)
{#KadisonRingrose}


For more references see [[operator algebra]].


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

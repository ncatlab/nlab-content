


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Qunantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The "interaction picture" in [[quantum physics]] is a way to decompose solutions to the [[Schrödinger equation]] and more generally the construction of [[quantum field theories]] into a [[free field theory]]-part and the [[interaction]] part that acts as a [[perturbation]] of the free theory. Therefore the interaction picture lends itself to the construction of [[perturbative quantum field theory]], and in fact the only mathematically rigorous such construction scheme that is known, namely _[[causal perturbation theory]]_, proceeds this way.

[[dynamics|Dynamics]] in [[physics]] affects both [[observables]] and, dually, [[states]]; this is most well known in [[quantum physics]] but applies equally well to [[classical physics]]. The different "pictures" of physics differ in how the dynamics is explicitly formalized:

* In the [[Schrödinger picture]], states are propagated through [[time]], while observables are held fixed; the axiomatic formalization of this is given by [[cobordism category]] [[representation]]s in [[FQFT]].

* In the [[Heisenberg picture]], the dependence of observables on time (or more generally [[spacetime]]) is encoded, while the state is held fixed; the axiomatic formalization of this is given by the [[Haag–Kastler axioms]] of [[AQFT]].

* The __Dirac (interaction) picture__ is a mixture of these two approaches: dynamics is split into a free (or otherwise solvable) part and an [[interaction]] (often then treated as a [[perturbation theory|perturbation]]); one of these is taken to affect the states, the other the observables.

The pictures are named after those physicists who first used or popularised these approaches to quantum physics.


### In quantum mechanics
 {#InQuantumMechanics}


In [[quantum mechanics]], let $\mathcal{H}$ be some [[Hilbert space]] and let 

$$
  H = H_{free} + V
$$

be Hermitian operator, thought of as a [[Hamiltonian]], decomposed as the [[sum]] of a free part ([[kinetic energy]]) and an interaction part ([[potential energy]]).

For example for a  [[non-relativistic particle]] of [[mass]] $m$ propagating on the [[line]] subject to a [[potential energy]] $V_{pot} \colon \mathbb{R} \to \mathbb{R}$, then $\mathcal{H} = L^2(X)$ is the Hilbert space of [[square integrable functions]] and

$$
  H 
   =  
  \underset{H_{free}}{\underbrace{\tfrac{- \hbar^2}{2m} \frac{\partial^2}{\partial^2 x}}}
    + 
  V
  \,,
$$

where $V = V_{pot}(x)$ is the operator of multiplying square integrable functions with the given potential energy function.

Now for 

$$
  \array{
    \mathbb{R} &\overset{\vert \psi (-)\rangle }{\longrightarrow}& \mathcal{H}
   \\
   t &\mapsto& \vert \psi(t) \rangle 
  }
$$ 

a one-parameter family of [[quantum states]], the [[Schrödinger equation]] for this state reads

$$
  \frac{d}{d t} \vert \psi(t) \rangle
  \;=\;
  \tfrac{1}{i \hbar} H \vert \psi\rangle
  \,.
$$

It is easy to solve this [[differential equation]] formally via its [[Green function]]: for $\vert \psi \rangle \in \mathcal{H}$ any state, then the unique solution $\vert \psi(-) \rangle$ to the Schr&#246;dinger equation subject to $\vert \psi(0) \rangle = \vert \psi \rangle$ is 

$$
  \vert \psi(t)\rangle_S \coloneqq \exp( \tfrac{t}{i \hbar} H ) \vert \psi \rangle
  \,.
$$

(One says that this is the solution "in the [[Schrödinger picture]]", whence the subscript.)

However, if $H$ is sufficiently complicated, it may still be very hard to extract from this expression a more explicit formula for $\vert \psi(t) \rangle$, such as, in the example of the free particle on the line, its expression as a function ("[[wave function]]") of $x$ and $t$.

But assume that the analogous expression for $H_{free}$ alone is well understood, hence that the operator

$$
  U_{S,free}(t_1, t_2) \coloneqq \exp\left({\tfrac{t_2 - t_1}{i \hbar} H_{free}}\right)
$$

is sufficiently well understood. The "[[interaction picture]]" is a way to decompose the Schr&#246;dinger equation such that its dependence on $V$ gets separated from its dependence on $H_{free}$ in a way that admits to treat $H_{int}$ in [[perturbation theory]].

Namely define analogously

\[
  \label{StateInTheInteractionPicture}
  \begin{aligned}
    \vert \psi(t)\rangle_I
     &\coloneqq  
     \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right) \vert \psi(t)\rangle_S
    \\
    & = \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right) 
        \exp\left({ \tfrac{+ t}{i \hbar} H} \right)\vert \psi \rangle 
    \\
    & = \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right) 
        \exp\left({\tfrac{t}{i \hbar} H_{free} + \tfrac{t}{i \hbar} V} \right)\vert \psi \rangle   \end{aligned} 
  \,.
\]

This is called the solution of the Schr&#246;dinger equation "in the [[interaction picture]]", whence the subscript. Its definition may be read as the result of propagating the actual solution $\vert \psi(-)\rangle_S$ at time $t$ back to time $t = 0$, but using just the free Hamiltonian, hence with "the interaction switched off". 

Notice that if the operator $V$ were to commute with $H_{free}$ (which it does not in all relevant examples) then we would simply have $\vert \psi(t)\rangle_I = \exp( \tfrac{t}{i \hbar } V ) \vert \psi\rangle$, hence then the solution (eq:StateInTheInteractionPicture) in the interaction picture would be the result of "propagating" the initial conditions using _only_ the interaction. Now since $V$ may not be assumed to commute with $H_{free}$, the actual form of $\vert \psi(-) \rangle_{I}$ is more complicated. But _infinitesimally_ it remains true that $\vert \psi(-)\rangle_I$ is propagated this way, not by the plain operator $V$, though, but by $V$ viewed in the [[Heisenberg picture]] of the free theory. This is the content of the differential equation (eq:DifferentialEquationInInteractionPicture) below.

But first notice that this will indeed be useful: If an explicit expression for the "state in the [[interaction picture]]" (eq:StateInTheInteractionPicture) is known, then the assumption that also the operator $\exp\left({\tfrac{t}{i \hbar} H_{free}}\right)$ is sufficiently well understood implies that the actual solution

$$
  \vert \psi(t) \rangle_S = \exp\left({\tfrac{t}{i \hbar} H_{free}}\right) \vert \psi(t) \rangle_I
$$

is under control. Hence the question now is how to find $\vert \psi(-)\rangle_I$ given its value at some time $t$. (It is conventional to consider this for $t \to \pm \infty$, see (eq:SMatrixInQuantumMechanics) below.) 

Now it is clear from the construction and using the [[product law]] for [[differentiation]], that $\vert \psi(-)\rangle_S$ satisfies the following [[differential equation]]:

\[
  \label{DifferentialEquationInInteractionPicture}
  \frac{d}{d t} \vert \psi(t) \rangle
  \;=\;
  V_I(t) \vert \psi(t)\rangle_I
  \,,
\]

where

$$
  V_I(t)
    \coloneqq 
  \exp\left( -\tfrac{t}{i \hbar} H_{free} \right)
    V
  \exp\left( +\tfrac{t}{i \hbar} H_{free} \right)
$$

is known as the [[interaction]] term $V$ "viewed in the interaction picture". But in fact this is just $V$ "viewed in the [[Heisenberg picture]]", but for the _free_ theory. By our running assumption that the free theory is well understood, also $V_I(t)$ is well understood, and hence all that remains now is to find a sufficiently concrete solution to equation (eq:DifferentialEquationInInteractionPicture). This is the heart of working in the interaction picture.

Solutions to equations of the "[[parallel transport]]"-type such as (eq:DifferentialEquationInInteractionPicture) are given by [[time-ordered product|time-ordering]] of Heisenberg picture operators, denoted $T$, applied to the naive exponential solution as above. This is known as the _[[Dyson formula]]_:

$$
  \vert \psi(t)\rangle_I
  \;=\;
  T\left(
    \exp\left(
      \int_{t_0}^t
        V_I(t)
        \tfrac{d t}{i \hbar}
    \right)
  \right)
  \vert \psi(t_0)\rangle
  \,.
$$

Here [[time-ordered product|time-ordering]] means 

$$
  T( V_I(t_1) V_I(t_2) )
  \;\coloneqq\;
  \left\{
    \array{
      V_I(t_1) V_I(t_2) &\vert& t_1 \geq t_2
      \\
      V_I(t_2) V_I(t_1) &\vert& t_2 \geq t_2
    }
  \right.
  \,.
$$

(This is abuse of notation: Strictly speaking time ordering acts on the [[tensor algebra]] spanned by the $\{V_I(t)\}_{t \in \mathbb{R}}$ and has to be _followed_ by taking tensor products to actual products. )

In applications to [[scattering]] processes one is interested in prescribing the [[quantum state]]/[[wave function]] far in the past, hence for $t \to - \infty$, and computing its form far in the future, hence for $t \to \infty$.

The operator that sends such "asymptotic ingoing-states" $\vert \psi(-\infty) \rangle_I$ to "asymptotic outgoing states" $\vert \psi(+ \infty) \rangle_I$ is hence the [[limit of a sequence|limit]]

\[
  \label{SMatrixInQuantumMechanics}
  S 
  \;\coloneqq\;
  \underset{t \to \infty}{\lim}
  T\left(
    \exp\left(
      \int_{-t}^t
        V_I(t)
        \tfrac{d t}{i \hbar}
    \right)
  \right)  
  \,.
\]

This limit (if it exists) is called the _scattering matrix_ or _S-matrix_, for short.
 
### In quantum field theory

In [[perturbative quantum field theory]] the broad structure of the interaction picture in quantum mechanics ([above](#InQuantumMechanics)) remains a very good guide, but various technical details have to be generalized with due care:

1. The algebra of operators in the [[Heisenberg picture]] of the free theory becomes the _[[Wick algebra]]_ of the [[free field theory]] (taking into account "normal ordering" of field operators) defined on _[[microcausal functionals]]_ built from [[operator-valued distributions]] with constraints on their [[wave front set]]. 

1. The [[time-ordered products]] in the [[Dyson formula]] have to be refined to [[causal locality|causally ordered]] products and the resulting product at coincident points has to be defined by [[point-extension of distributions]] -- the freedom in making this choice is the [[renormalization]] freedom ("conter-terms").

1. The sharp interaction cutoff in the [[Dyson formula]] that is hidden in the integration over $[t_0,t]$ has to be smoothed out by [[adiabatic switching]] of the interaction (making the whole S-matrix an [[operator-valued distribution]]).

Together these three point are taken care of by the axiomatization of the "[[adiabatic switching|adiabatically switched]] [[S-matrix]]" according to **[[causal perturbation theory]]**.


The analogue of the limit $t \to \infty$ in the construction of the [[S-matrix]] (now: [[adiabatic limit]]) in general does not exist in field theory ("infrared divergencies"). But in fact it need not be taken: The field algebra in a bounded region of [[spacetime]] may be computed with any adiabatic switching that is constant on this region. Moreover, the algebras assigned to regions of spacetime this way satisfy [[causal locality]] by the causal ordering in the construction of the S-matrix. Therefore, even without taking the adiabatic limit in [[causal perturbation theory]] one obtains a field theory in the form of a _[[local net of observables]]_. This is the topic of **[[locally covariant perturbative quantum field theory]]**.




## Related concepts

* [[interaction]]

* [[interacting field algebra]]

* [[interacting field theory]]

* [[S-matrix]]

* [[Møller operator]]

## References

For instance 

* [[Eberhard Zeidler]], section 7.19.3 of _Quantum field theory. A bridge between mathematicians and physicists -- volume I_ Springer (2009) ([web](http://www.mis.mpg.de/zeidler/qft.html))


[[!redirects Dirac picture]]
[[!redirects interaction picture]]
[[!redirects Dirac interaction picture]]
[[!redirects Dirac (interaction) picture]]

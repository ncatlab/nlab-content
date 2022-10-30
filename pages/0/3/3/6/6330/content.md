
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### AQFT
+-- {: .hide}
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

[[dynamics|Dynamics]] in [[physics]] affects both [[observables]] and, dually, [[states]]; this is most well known in [[quantum physics]] but applies equally well to [[classical physics]]. The different "pictures" of physics differ in how the dynamics is explicitly formalized:

* In the [[Schrödinger picture]], states are propagated through [[time]], while observables are held fixed; the axiomatic formalization of this is given by [[cobordism category]] [[representation]]s in [[FQFT]].

* In the [[Heisenberg picture]], the dependence of observables on time (or more generally [[spacetime]]) is encoded, while the state is held fixed; the axiomatic formalization of this is given by the [[Haag–Kastler axioms]] of [[AQFT]].

* The __Dirac (interaction) picture__ is a mixture of these two approaches: dynamics is split into a free (or otherwise solvable) part and an [[interaction]] (often then treated as a [[perturbation theory|perturbation]]); one of these is take to affect the states, the other the observables.

The pictures are named after those physicists who first used or popularised these approaches to quantum physics.

## In quantum mechanics

In [[quantum mechanics]], let $\mathcal{H}$ be some [[Hilbert space]] and let 

$$
  H = H_{free} + V
$$

be Hermitian operator, thought of as a [[Hamiltonian]], decomposed as the [[sum]] of a free part ([[kinetic energy]]) and an interaction part ([[potential energy]]).

For exampled for a  [[non-relativistic particle]] of [[mass]] $m$ propagating on the [[line]] subject to a [[potential energy]] $V_{pot} \colon \mathbb{R} \to \mathbb{R}$, then $\mathcal{H} = L^2(X)$ is the Hilbert space space of [[square integrable functions]] and

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

However, if $H$ is sufficiently complicated, it may still be very hard to extract from this expression a more explicit formula for $\vert \psi(t) \rangle$, such as, in the example of the free particle on the line, it expression as a function ("[[wave function]]") of $x$ and $t$.

But assume that the analogous expression for $H_{free}$ alone is well understood, hence that the operator

$$
  U_{S,free}(t_1, t_2) \coloneqq \exp\left({\tfrac{i \hbar}{t_2 - t_1} H_{free}}\right)
$$

is sufficiently well understood. The "interaction picture" is a way to decompose the Schr&#246;dinger equation such that its dependence on $H_{int}$ gets separated from its dependence on $H_{free}$ in a way that admits to treat $H_{int}$ in [[perturbation theory]].

Namely define analogously

$$
  \begin{aligned}
    \vert \psi(t)\rangle_I
     &\coloneqq  
     \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right) \vert \psi(t)\rangle_S
    \\
    & = \exp\left({\tfrac{- t}{i \hbar} H_{free}}\right) \exp\left({+ \tfrac{t}{i \hbar} H} \right)\vert \psi \rangle 
  \end{aligned} 
  \,.
$$

If an explicit expression for this "state in the interaction picture" (whence the subscript) is known, then the assumption that also the operator $\exp\left({\tfrac{t}{i \hbar} H_{free}}\right)$ is sufficiently well understood implies that the actual solution

$$
  \vert \psi(t) \rangle_S = \exp\left({\tfrac{t}{i \hbar} H}\right) \vert \psi(t) \rangle_I
$$

is under control.

Hence the question now is how to find $\vert \psi(-)\rangle_I$ given its value at some time $t$. (It is conventional to consider this for $t \to \pm \infty$.) But it is clear from the construction and using the [[product law]] for [[differentiation]], that $\vert \psi(-)\rangle_S$ satisfies the following [[differential equation]]

$$
  \frac{d}{d t} \vert \psi(t) \rangle
  \;=\;
  V_I(t) \vert \psi(t)\rangle_I
  \,,
$$

where

$$
  V_I(t)
    \coloneqq 
  \exp\left( \tfrac{t}{i \hbar} H_{free} \right)
    V
  \exp\left( -\tfrac{t}{i \hbar} H_{free} \right)
   \,.
$$







## Related concepts

* [[S-matrix]]

* [[interacting field algebra]]

## References

For instance 

* [[Eberhard Zeidler]], section 7.19.3 of _Quantum field theory. A bridge between mathematicians and physicists -- volume I_ Springer (2009) ([web](http://www.mis.mpg.de/zeidler/qft.html))


[[!redirects Dirac picture]]
[[!redirects interaction picture]]
[[!redirects Dirac interaction picture]]
[[!redirects Dirac (interaction) picture]]

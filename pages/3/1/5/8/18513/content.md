
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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
 {#Idea}

A _Wick algebra_ is an [[algebra of quantum observables]] of [[free fields|free]] [[quantum field theory|quantum fields]].

In the [[quantum mechanics]] of [[harmonic oscillators]] or in [[quantum field theory]] of [[free fields]] on [[Minkowski spacetime]] one encounters [[linear operators]] $\{a_k, a^\ast_k\}_{k \in K}$ that satisfy the [[canonical commutation relation]] $[a_i, a^\ast_j] = diag((c_k))_{i j}$.
Then by a _normal ordered polynomial_ or _Wick polynomial_ ([Wick 50](#Wick50)) one means a [[polynomial]], denoted $:P:$, which is obtained from a polynomial $P((a_k, a^\ast_k))$ in these operators  by ordering all "creation operators" $a_k^\ast$ to the left of all "annihiliation operators". For example focusing on a single mode $k$ we have:

$$
  \array{
    :a^\ast: = a^\ast
    \\
    :a: = a
    \\
    :a^\ast a: = a^\ast a
    \\
    :a a^\ast: = a^\ast a
    \\
    :a a^\ast a: = a^\ast a a
    \\
    etc.
  }
  \,
$$

The intuitive idea is that these operators span a [[Hilbert space]] $\mathcal{H}$ of [[quantum states]] from a [[vacuum state]] $\vert vac \rangle \in \mathcal{H}$ characterized by the condition

$$
  a_k \vert vac \rangle = 0
  \phantom{AAA}
  \text{for all} \,\, k
$$

hence (if we think of $a_k$ as acting by "removing a quantum in mode $k$") by the condition that it contains no quanta. So the normal ordered Wick polynomials represent the [[quantum observables]] with vanishing [[vacuum expectation value]]. In [[quantum field theory]] they model [[scattering]] processes where quanta enter a reaction process (the modes corresponding to the "annihilation" operators $a_k$) and other particles come out of the reaction (the modes corresppnding to the "creation" operators $a^\ast_k$).

The product of two Wick polynomials, computed in the ambient operator algebra and 
then re-expressed as a Wick polynomial, is given by computing the relevant sequence of [[commutators]] by [[Wick's lemma]], for example

$$
  {:a^\ast a:} \, {:a^\ast a:}
  =
  :a^\ast a^\ast a a: + \hbar \, :a^\ast a:
  \,,
$$

where $\hbar = [a, a^\ast]$ is the value of the [[canonical commutation relations|canonical commutator]].

The [[associative algebra]] thus obtained is hence called the _algebra of normal ordered operators_ or _Wick polynomial algebra_ or just _Wick algebra_.

This plays a central role in [[perturbative quantum field theory]], where the [[quantization]] of [[quantum observables]] of [[free fields]] is traditionally _defined_ as the corresponding Wick algebra.

But the Wick algebra in [[quantum field theory]] may also be understood more systematically from first principles of [[quantization]]. It turns out that it is [[Moyal deformation quantization]] of the canonical [[Poisson bracket]] on the [[covariant phase space]] of the [[free field]], which is the [[Peierls bracket]] modified to an [[almost Kähler structure]] by the [[2-point function]] of a [[quasi-free Hadamard state]] ([Dito 90](#Dito90), [D&#252;tsch-Fredenhagen 01](#DutschFredenhagen01)). See example \ref{WickAlgebraOfASingleMode} and def. \ref{WickAlgebraOfFreeQuantumField} below.

Understood in this form the construction directly generalized to [[quantum field theory on curved spacetimes]] ([Brunetti-Fredenhagen 95](#BrunettiFredenhagen95), [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00), [Hollands-Wald 01](#HollandsWald01)).

Finally, the shift by the [[quasi-free Hadamard state]], which is the very source of the "normal ordering", was understood as an example of the almost-K&#228;hler version of the quantization recipe of [[Fedosov deformation quantization]] ([Collini 16](#Collini16)). For more on this see at _[[locally covariant perturbative quantum field theory]]_.

$\,$


[[!include Wick algebra -- table]]



## Definition


In [[free field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations]] of motion, then analog of (eq:InStarProductTensorInvertingHermitianForm)

$$
  \pi \;=\; \tfrac{i}{2}\omega^{-1} + \tfrac{1}{2}g^{-1}
$$

is the [[Wightman propagator]] according to [this equation](Hadamard+distribution#eq:DeompositionOfHadamardPropagatorOnMinkowkski)

$$
  \Delta_H
  \;=\;
  \tfrac{i}{2}\Delta_S + H
  \,.
$$



+-- {: .num_prop #MoyalStarProductOnMicrocausal}
###### Proposition
**(Hadamard-Moyal star product on [[microcausal observables]])

Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] and let $\Delta_H$ be a corresponding [[Hadamard distribution]] ([[Wightman propagator]]).

Then the [[star product]]

$$
  P_1 \star_{\Delta_H} P_2
  \;\coloneqq\;
  prod
   \circ
  \exp\left(
    \int_{X^2} \hbar \Delta_H^{a b}(x_1, x_2) \frac{\delta}{\delta \Phi^a(x_1)}
    \otimes \frac{\delta}{\delta \Phi^b(x_2)} dvol_g
  \right)
  (P_1 \otimes P_2)
$$

on [[microcausal observables]] $P_1, P_2 \in \mathcal{F}_{mc}$ is well defined in that the [[products of distributions]] that appear in expanding out the [[exponential]] are such that the sum of the [[wave front sets]] of the factors does not intersect the zero section.

=--

(e.g. [Collini 16, p. 25-26](#Collini16))

+-- {: .proof}
###### Proof

By definition of [[Hadamard distribution]], the [[wave front set]] of powers of $\pi$ has all cotangents on the first variables future pointing, and all those on the second variables past pointing. The first variables are integrated against those of $P_1$ and the second against $P_2$. By definition of microcausal functionals, the wave front sets of $P_1$ and $P_2$ are disjoint from the subsets where all components are future pointing or all components are past-pointing. Therefore the relevant sum of of the wave front covectors never vanishes.

=--

+-- {: .num_defn #WickAlgebraOfFreeQuantumField}
###### Definition
**(Wick algebra of free quantum field)**

Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] and let $\Delta_H$ be a corresponding [[Hadamard distribution]] ([[Wightman propagator]]).

Then the _Wick algebra_ of [[quantum observables]] of the [[free field|free]] [[scalar field]] on $(X,g)$ is the space of [[microcausal functionals]] $\mathcal{F}_{mc}$ equipped with the Hadamard-Moyal [[star product]] from prop. \ref{MoyalStarProductOnMicrocausal}:

$$
  \mathcal{W}(X,\Delta_H)
  \;\coloneqq\;
  \left(
    \mathcal{F}_{mc}, \star_{\Delta_H}
  \right)
  \,.
$$

> (this is [[off-shell]])

=--

## Hadamard vacuum states on Wick algebras

(...)

there is a [[state on a star-algebra|state]] on the [[Wick algebra]], given by evaluation on the zero [[field history]]

$$
  \array{
    \mathcal{W}
      &\overset{\langle -\rangle}{\longrightarrow}&
    \mathbb{C}
    \\
    A &\mapsto& A(\Phi = 0) 
  }
$$

(by positive semi-definiteness of [[Hadamard distributions]], [this condition](Hadamard+distribution#PositiveSemiDefiniteness)...)

With respect to this state, $\Delta_H(x,y)$ itself is the [[vacuum expectation value]] of the [[2-point function]]:

$$
  \langle \Phi(x) \star_{\Delta_F} \Phi(y) \rangle
  \;=\;
  \underset{ = 0 }{
  \underbrace{
    \left\langle 
       \mathbf{\Phi}(x) \mathbf{\Phi}(y)
    \right\rangle
  }}
  +
  \underset{ = \hbar \Delta_H(x,y) }{
  \underbrace{
    \left \langle 
      \hbar \Delta_H(x,y)
    \right\rangle
  }}
$$

or equivalently in physics notation

$$
  \langle \Phi(x) \Phi(y) \rangle
  \;=\;
  \underset{ = 0 }{
  \underbrace{
    \left\langle 
       :\mathbf{\Phi}(x) \mathbf{\Phi}(y):
    \right\rangle
  }}
  +
  \underset{ = \Delta_\hbar H(x,y) }{
  \underbrace{
    \left \langle 
      \hbar \Delta_H(x,y)
    \right\rangle
  }}
$$

(...)


## Examples

### On Minkowski spacetime

In [[Minkowski spacetime]] the [[Hadamard state]] is simply the usual [[vacuum state]] $\vert vac \rangle$, hence the [[Hadamard distribution]] is, as a [[generalized function]]

$$
  \pi(x,y) = \langle vac \vert \Phi(x) \Phi(y) \vert vac \rangle
  \,.
$$

[[!include propagators - table]]

Therefore the abstractly defined Wick algebra as in def. \ref{WickAlgebraOfFreeQuantumField} in this case satisfies the relation

$$
  \int_{X} f(x,y)  \;  :\Phi(x): \,  :\Phi(y): \; dvol_g
  \;=\;
  \int_X f(x,y) \left( :\Phi(x) \Phi(y): -  \langle vac \vert \Phi(x) \Phi(y) \vert vac \rangle \right)  \; dvol_g
  \,.
$$

This is the traditional expression for the normal ordered Wick product on Minkowski spacetime (e.g. [here](https://en.wikipedia.org/wiki/Normal_order#Free_fields)).

## Related concepts

[[!include products in pQFT -- table]]


## References

The construction goes back to

* {#Wick50} [[Gian-Carlo Wick]], _The evaluation of the collision matrix_, Phys. Rev. 80, 268-272 (1950)

Its realization as the [[Moyal deformation quantization]] of the [[Peierls bracket]] shifted by a [[quasi-free Hadamard state]] is due to

* {#Dito90} Joseph Dito, _Star-product approach to quantum field theory: The free scalar field_. Letters in Mathematical Physics, 20(2):125&#8211;134, 1990 ([spire](https://inspirehep.net/record/303898/))

further amplified in

* {#DuetshFredenhagen00} [[Michael Dütsch]], [[Klaus Fredenhagen]], section 5.1 of _Algebraic Quantum Field Theory, Perturbation Theory, and the Loop Expansion_, Commun.Math.Phys. 219 (2001) 5-30 ([arXiv:hep-th/0001129](https://arxiv.org/abs/hep-th/0001129))

* {#DutschFredenhagen01} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic field theory, and deformation quantization_, in [[Roberto Longo]] (ed.), _Mathematical Physics in Mathematics and Physics, Quantum and Operator Algebraic Aspects_, volume 30 of Fields Institute Communications, pages 151&#8211;160. American Mathematical Society, 2001 ([arXiv:hep-th/0101079](https://arxiv.org/abs/hep-th/0101079))


and the generalization to [[quantum field theory on curved spacetime]] is discussed in

* {#BrunettiFredenhagen95} [[Romeo Brunetti]], [[Klaus Fredenhagen]], M. K&#246;hler, _The microlocal spectrum condition and Wick polynomials on curved spacetimes_, Commun. Math. Phys. 180, 633-652, 1996 ([arXiv:gr-qc/9510056](https://arxiv.org/abs/gr-qc/9510056))


* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

* {#HollandsWald01} [[Stefan Hollands]], [[Robert Wald]], _Local Wick Polynomials and Time Ordered Products of Quantum Fields in Curved Spacetime_, Commun. Math. Phys. 223:289-326, 2001 ([arXiv:gr-qc/0103074](https://arxiv.org/abs/gr-qc/0103074))

The conceptual explanation of the shift by the Hadamard state as a step in the almost-K&#228;hler version of [[Fedosov deformation quantization]] is due to

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))


[[!redirects Wick algebras]]


[[!redirects Wick polynomial]]
[[!redirects Wick polynomials]]

[[!redirects normal ordering]]

[[!redirects normal-ordered product]]
[[!redirects normal-ordered products]]

[[!redirects normal ordered product]]
[[!redirects normal ordered products]]


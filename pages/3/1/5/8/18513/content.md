
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

In [[free field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations]] of motion, then analog of the star product tenstor ([this equation](star+product#eq:InStarProductTensorInvertingHermitianForm))

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


Understood in this form the construction directly generalized to [[quantum field theory on curved spacetimes]] ([Brunetti-Fredenhagen 95](#BrunettiFredenhagen95), [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00), [Hollands-Wald 01](#HollandsWald01)).

Finally, the shift by the [[quasi-free Hadamard state]], which is the very source of the "normal ordering", was understood as an example of the almost-K&#228;hler version of the quantization recipe of [[Fedosov deformation quantization]] ([Collini 16](#Collini16)). For more on this see at _[[locally covariant perturbative quantum field theory]]_.

$\,$


[[!include Wick algebra -- table]]



## Definition

### Abstract Wick algebra

+-- {: .num_defn #MicrocausalObservable}
###### Definition
**([[microcausal observable|microcausal]] [[polynomial observables]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]]. then the [[off-shell]] [[polynomial observables]] are those functions

$$
  A
    \;\colon\;
  \Gamma_{\Sigma,scp}(E)
    \longrightarrow
  \mathbb{C}
$$

which are given by graded-symmetric [[distribution|distributional]] [[coefficients]] 

$$
  \alpha^{(k)} \in \Gamma'_{\Sigma,cp}\left( E^{\boxtimes^k_{sym}} \right)
$$

as 

$$
  \begin{aligned}
    A(\Phi)
    & =
    \alpha^{(0)}
    \\
    & \phantom{=} +
    \int \alpha^{(1)}_{a}(x) \Phi^a(x)\, dvol_\Sigma(x)
    \\
    & \phantom{=} + 
    \int \int 
      \alpha^{(2)}_{a_1 a_2}(x_1, x_2) 
       \Phi^{a_1}(x_1) \Phi^{a_2}(x_2)
      \, dvol_\Sigma(x_1)
      \, dvol_\Sigma(x_2)
    \\
    & \phantom{=} + \cdots 
  \end{aligned}
$$

where we use [[generalized function]]-notation.

Moreover, if the [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]

$$
  P \Phi = 0
$$

are [[Green hyperbolic differential equations]], then the [[on-shell]] [[polynomial observables]] form the [[quotient space]] of that of off-shell polynomial observables by those with coefficients in the image of the [[differential operator]] $P$ corresponding to the [[equations of motion]]:

$$
  PolyObs(E,\mathbf{L})
  \simeq
  PolyObs(E)/im(P)
  \,.
$$

Finally a polynomial observable is a _[[microcausal observable]]_ if each [[coefficient]] $\alpha^{(k)}$ as above has [[wave front set]] away from those points where the $k$ [[wave vectors]] are all in the [[future cone]] or all in the [[past cone]]. We write

$$
  \array{
    PolyObs(E)_{mc}
     &\hookrightarrow&
    PolyObs(E)
    \\
    PolyObs(E,\mathbf{L})_{mc}
    \simeq
    PolyObs(E)_{mc}/im(P)
     &\hookrightarrow&
    PolyObs(E,\mathbf{L})
  }
$$

for the [[subspace]] of [[off-shell]]/[[on-shell]] [[microcausal observables]] insides all [[off-shell]]/[[on-shell]] [[polynomial observables]].


=--



+-- {: .num_prop #MoyalStarProductOnMicrocausal}
###### Proposition
**(Hadamard-Moyal star product on [[microcausal observables]])

Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] $P \Phi = 0$ with [[causal propagator]] $\Delta$ and let 

$$
  \Delta_H
  \;=\;
  \tfrac{i}{2}\Delta + H
$$ 

be a corresponding [[Wightman propagator]] ([[Hadamard 2-point function]]).

Then the [[star product]]

$$
  A \star_H A
  \;\coloneqq\;
  prod
   \circ
  \exp\left(
    \int_{X^2} \hbar \Delta_H^{a b}(x_1, x_2) \frac{\delta}{\delta \Phi^a(x_1)}
    \otimes \frac{\delta}{\delta \Phi^b(x_2)} dvol_g
  \right)
  (P_1 \otimes P_2)
$$

on [[off-shell]] [[microcausal observables]] $A_1, A_2 \in \mathcal{F}_{mc}$ (def. \ref{MicrocausalObservable}) is well defined in that the [[wave front sets]] involved in the [[products of distributions]] that appear in expanding out the [[exponential]] satisfy [[Hörmander's criterion]].

Hence by the general properties of [[star products]] ([this prop.](star+product#AssociativeAndUnitalStarProduct)) this yields a [[unital algebra|unital]] [[associative algebra]] [[structure]] on the space of [[off-shell]] [[microcausal observables]]

$$
  \left(
    PolyObs(E)_{mc} \,,\, \star_H
  \right)
  \,.
$$ 

This is the _[[off-shell]] [[Wick algebra]]_ corresponding to the choice of [[Wightman propagator]] $H$.

Moreover the image of $P$ is an ideal with respect to this algebra structure, so that it descends to the [[on-shell]] [[microcausal observables]] to yield the _[[on-shell]] [[Wick algebra]]_

$$
  \left(
    PolyObs(E,\mathbf{L})_{mc} \,,\, \star_H
  \right)
  \,.
$$ 


=--

(e.g. [Collini 16, p. 25-26](#Collini16))

+-- {: .proof}
###### Proof

By definition of [[Wightman propagator]], the [[wave front set]] of powers of $\Delta_H$ has all cotangents on the first variables future pointing, and all those on the second variables past pointing. The first variables are integrated against those of $A_1$ and the second against $A_2$. By definition of [[microcausal observables]] (def. \ref{MicrocausalObservable}), the wave front sets of $A_1$ and $A_2$ are disjoint from the subsets where all components are future pointing or all components are past-pointing. Therefore the relevant sum of of the wave front covectors never vanishes and hence [[Hörmander's criterion]] is met.

=--

+-- {: .num_remark #WickAlgebraIsFormalDeformationQuantization}
###### Remark
**([[Wick algebra]] is [[formal deformation quantization]] of [[Poisson-Peierls bracket|Poisson-Peierls algebra of observables]])**


Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] $P \Phi = 0$ with [[causal propagator]] $\Delta$ and let $\Delta_H \;=\; \tfrac{i}{2}\Delta + H$  be a corresponding [[Wightman propagator]] ([[Hadamard 2-point function]]).


Then the [[Wick algebra]]  $\left( PolyObs(E,\mathbf{L})_{mc} \,,\, \star_H \right)$ from prop. \ref{MoyalStarProductOnMicrocausal} is a [[formal deformation quantization]] of the [[Poisson algebra]] on the [[covariant phase space]] given by the [[on-shell]] [[polynomial observables]] equipped with the [[Poisson-Peierls bracket]] $\{-,-\} \;\colon\; PolyObs(E,\mathbf{L})_{mc} \otimes PolyObs(E,\mathbf{L})_{mc}  \to PolyObs(E,\mathbf{L})_{mc}$ in that for all $A_1, A_2 \in PolyObs(E,\mathbf{L})_{mc}$ we have

$$
  A_1 \star_H A_2
  \;=\;
  A_1 \cdot A_2
  \;mod\;
  \hbar
$$

and

$$
  A_1 \star_H A_2
  -
  A_2 \star_H a_1
  \;=\;
  i \hbar \{A_1, A_2\}
  \;mod\;
  \hbar^2
  \,.
$$



=--

([Dito 90](#Dito90), [Dütsch-Fredenhagen 01](#DutschFredenhagen01))

+-- {: .proof}
###### Proof

By prop. \ref{MoyalStarProductOnMicrocausal} this is immediate from the general properties of the [[star product]] ([this example](A+first+idea+of+quantum+field+theory+--+Quantization#MoyalStarProductIsFormalDeformationQuantization)). 

Explicitly, let, without restriction of generality, $A_1 = \int (\alpha_1)_a(x) \mathbf{\Phi}^a(x)\, dvol_\Sigma(x)$ and $A_2 = \int (\alpha_2)_a(x) \mathbf{\Phi}^a(x)\, dvol_\Sigma(x)$ be two linear observables. Then

$$
  \begin{aligned}
    A_1 \star_H A_2
    & =
    A_1 A_2 
    +
    \hbar 
    \int \left( \tfrac{i}{2} \Delta^{a_1 a_2}(x_1, x_2) + H^{a_1 a_2}(x_1,x_2)  
      \frac{\partial A_1}{\partial \mathbf{\Phi}^{a_1}(x_1)}
      \frac{\partial A_2}{\partial \mathbf{\Phi}^{a_2}(x_2)}
   \right) 
    \;mod\;
    \hbar^2  
   \\
   & = 
   A_1 A_2 
   + 
   \hbar 
   \left(
    \int 
      (\alpha_1)_{a_1}(x_1)
      \left(
       \tfrac{i}{2}\Delta^{a_1 a_2}(x_1, x_2)
       + H^{a_1 a_2}(x_1, x_2)
      \right)
      (\alpha_2)_{a_2}(x_2)
   \right)
   \;mod\;
   \hbar^2
  \end{aligned}
$$

Now since $\Delta$ is skew-symmetric, while $H$ is symmetric is follows that

$$
  A_1 \star_H A_2
  - 
  A_2 \star_H A_1
  =
  i \hbar 
  \left(
   \int 
     (\alpha_1)_{a_1}(x_1)
     \Delta^{a_1 a_2}(x_1, x_2)
     (\alpha_2)_{a_2}(x_2)
  \right)
  \;mod\;
  \hbar^2
  \,.
$$

The right hand side is the [[integral kernel]]-expression for the [[Poisson-Peierls bracket]].


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



>  under construction

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

The abstract [[Wick algebra]] of a [[free field theory]] with [[Green hyperbolic differential equation]] is directly analogous to the [[star product]]-algebra induced by a [[finite dimensional vector space|finite dimensional]] [[Kähler vector space]] ([this def.](star+product#WickAlgebraOfAlmostKaehlerVectorSpace))  under the following identification of the [[Wightman propagator]] with the [[Kähler space]]-[[structure]]:

+-- {: .num_remark #WightmanPropagatorAsKaehlerVectorSpaceStructure}
###### Remark
**([[Wightman propagator]] as [[Kähler vector space]]-[[structure]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] whose [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] is a [[Green hyperbolic differential equation]]. Then the corresponding [[Wightman propagator]] is analogous to the rank-2 tensor on a [[Kähler vector space]] as follows:

| [[covariant phase space]] <br/> of [[free field theory|free]] [[Green hyperbolic differential equation|Green hyperbolic]] <br/> [[Lagrangian field theory]] | [[finite dimensional vector space|finite dimensional]] <br/> [[Kähler vector space]] |
|-------------------|-------------------------|
| [[space of field histories]] <br/>  $\Gamma_\Sigma(E)$ |  $\mathbb{R}^{2n}$ |
| [[symplectic form]] <br/> $\tau_{\Sigma_p} \Omega_{BFV}$ | [[Kähler form]] $\omega$ |
| [[causal propagator]] $\Delta$ | $\omega^{-1}$ |
| [[Peierls-Poisson bracket]] <br/> $\{A_1,A_2\} = \int \Delta^{a_1 a_2}(x_1,x_2) \frac{\delta A_1}{\delta \mathbf{\Phi}^{a_1}(x_1)} \frac{\delta A_2}{\delta \mathbf{\Phi}^{a_2}(x_2)} dvol_\Sigma(x)$ | [[Poisson bracket]] |
| [[Wightman propagator]] <br/> $\Delta_H = \tfrac{i}{2} \Delta + H$  | [[Hermitian form]] <br/>  $\pi = \tfrac{i}{2}\omega^{-1} + \tfrac{1}{2}g^{-1}$ | 
 
=--

([Fredenhagen-Rejzner 15, section 3.6](pAQFT#FredenhagenRejzner15), [Collini 16, table 2.1](#pAQFT#Collini16))

+-- {: .num_defn #MicrocausalObservable}
###### Definition
**([[microcausal observable|microcausal]] [[polynomial observables]])**
Let $E \overset{fb}{\to}$ be [[field bundle]] which is a [[vector bundle]]. An [[off-shell]] _[[polynomial observable]]_ is a [[smooth function]]

$$
  A 
  \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow 
  \mathbb{C}
$$

on the [[on-shell]] [[space of sections]] of the [[field bundle]] $E \overset{fb}{\to} \Sigma$ (space of field histories) which may be expressed as

$$
  A(\Phi)
  \;=\;
  \alpha^{(0)}
  +
  \int_\Sigma
    \alpha^{(1)}_a(x) \Phi^a(x)
   \,
  dvol_\Sigma(x)
  +
  \int_\Sigma \int_\Sigma
   \alpha^{(2)}_{a_1 a_2}(x_1, x_2) \Phi^{a_1}(x_1) \Phi^{a_2}(x_2)
  \,dvol_\Sigma(x_1)
  \, dvol_\Sigma(x_2)
  +
  \cdots
  \,,
$$

where 

$$
  \alpha^{(k)} \in \Gamma'_{\Sigma^k}\left((E^\ast)^{\boxtimes^k_{sym}} \right)
$$

is a [[compactly supported distribution]] [[distribution of two variables|of k variables]] on the $k$-fold graded-symmetric [[external tensor product of vector bundles]] of the [[field bundle]] with itself.

Write 

$$
  PolyObs(E) \hookrightarrow Obs(E)
$$

for the [[subspace]] of off-shell polynomial observables onside all off-shell [[observables]].

Let moreover $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] whose [[equations of motion]] are [[Green hyperbolic differential equations]]. Then an _[[on-shell]] polynomial observable_ is the [[restriction]] of an off-shell polynomial observable along the inclusion of the [[on-shell]] [[space of field histories]] $\Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0} \hookrightarrow \Gamma_\Sigma(E)$. Write

$$
  PolyObs(E,\mathbf{L}) \hookrightarrow Obs(E,\mathbf{L})
$$

for the subspace of all on-shell polynomial observables inside all on-shell [[observables]].

By [this prop.](Green+hyperbolic+partial+differential+equation#DistributionsOnSolutionSpaceAreTheGeneralizedPDESolutions) restriction yields an [[isomorphism]] between polynomial on-shell observables and polynomial off-shell observables modulo the image of the [[differential operator]] $P$:

$$
  PolyObs(E,\mathbf{L})
    \underoverset{\simeq}{\text{restriction}}{\longleftarrow}
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
**([[Hadamard distribution|Hadamard]]-[[Moyal star product]] on [[microcausal observables]] -- [[abstract Wick algebra]])**

Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] $P \Phi = 0$. Write $\Delta$ for the [[causal propagator]] and let 

$$
  \Delta_H
  \;=\;
  \tfrac{i}{2}\Delta + H
$$ 

be a corresponding [[Wightman propagator]] ([[Hadamard 2-point function]]).

Then the [[star product]] induced by $\Delta_H$

$$
  A \star_H A
  \;\coloneqq\;
  prod
   \circ
  \exp\left(
    \int_{X^2} \hbar \Delta_H^{a b}(x_1, x_2) \frac{\delta}{\delta \mathbf{\Phi}^a(x_1)}
    \otimes \frac{\delta}{\delta \mathbf{\Phi}^b(x_2)} dvol_g
  \right)
  (P_1 \otimes P_2)
$$

on [[off-shell]] [[microcausal observables]] $A_1, A_2 \in \mathcal{F}_{mc}$ (def. \ref{MicrocausalObservable}) is well defined in that the [[wave front sets]] involved in the [[products of distributions]] that appear in expanding out the [[exponential]] satisfy [[Hörmander's criterion]].

Hence by the general properties of [[star products]] ([this prop.](star+product#AssociativeAndUnitalStarProduct)) this yields a [[unital algebra|unital]] [[associative algebra]] [[structure]] on the space of [[formal power series]] in $\hbar$ of [[off-shell]] [[microcausal observables]]

$$
  \left(
    PolyObs(E)_{mc}[ [\hbar] ] \,,\, \star_H
  \right)
  \,.
$$ 

This is the _[[off-shell]] [[Wick algebra]]_ corresponding to the choice of [[Wightman propagator]] $H$.

Moreover the image of $P$ is an ideal with respect to this algebra structure, so that it descends to the [[on-shell]] [[microcausal observables]] to yield the _[[on-shell]] [[Wick algebra]]_

$$
  \left(
    PolyObs(E,\mathbf{L})_{mc}[ [ \hbar ] ] \,,\, \star_H
  \right)
  \,.
$$ 

Finally, under [[complex conjugation]] $(-)^\ast$ these are [[star algebras]] in that 

$$
  \left(
    A_1 \star_H A_2
  \right)^\ast
  =
  A_2^\ast \star_H A_1^\ast
  \,.
$$

=--

([Dütsch-Fredenhagen 00](#DuetshFredenhagen00); see [Collini 16, p. 25-26](#Collini16))

+-- {: .proof}
###### Proof

By definition of [[Wightman propagator]], the [[wave front set]] of powers of $\Delta_H$ has all cotangents on the first variables future pointing, and all those on the second variables past pointing. The first variables are integrated against those of $A_1$ and the second against $A_2$. By definition of [[microcausal observables]] (def. \ref{MicrocausalObservable}), the wave front sets of $A_1$ and $A_2$ are disjoint from the subsets where all components are future pointing or all components are past-pointing. Therefore the relevant sum of of the wave front covectors never vanishes and hence [[Hörmander's criterion]] is met and the star product is well defined.

It remains to see that the star product $A_1 \star_H A_2$ is itself again a [[microcausal observable]]. It is clear that it is again a [[polynomial observable]] and that it respects the ideal generated by the equations of motion. That it still satisfies the condition on the [[wave front set]] follows directly from the fact that the wave front set of a [[product of distributions]] is inside the fiberwise sum of elements of the factor wave front sets ([this prop.](product+of+distributions#WaveFrontSetOfProductOfDistributionsInsideFiberProductOfFactorWaveFrontSets)).

Finally the [[star algebra]]-structure follows via remark \ref{WickAlgebraOfAlmostKaehlerVectorSpace} as in [this prop.](star+product#StarProductAlgebraOfKaehlerVectorSpaceIsStarAlgebra).

=--

+-- {: .num_remark #WickAlgebraIsFormalDeformationQuantization}
###### Remark
**([[Wick algebra]] is [[formal deformation quantization]] of [[Poisson-Peierls bracket|Poisson-Peierls algebra of observables]])**


Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] $P \Phi = 0$ with [[causal propagator]] $\Delta$ and let $\Delta_H \;=\; \tfrac{i}{2}\Delta + H$  be a corresponding [[Wightman propagator]] ([[Hadamard 2-point function]]).


Then the [[Wick algebra]]  $\left( PolyObs(E,\mathbf{L})_{mc}[ [\hbar] ] \,,\, \star_H \right)$ from prop. \ref{MoyalStarProductOnMicrocausal} is a [[formal deformation quantization]] of the [[Poisson algebra]] on the [[covariant phase space]] given by the [[on-shell]] [[polynomial observables]] equipped with the [[Poisson-Peierls bracket]] $\{-,-\} \;\colon\; PolyObs(E,\mathbf{L})_{mc} \otimes PolyObs(E,\mathbf{L})_{mc}  \to PolyObs(E,\mathbf{L})_{mc}$ in that for all $A_1, A_2 \in PolyObs(E,\mathbf{L})_{mc}$ we have

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

Explicitly, consider, without restriction of generality, $A_1 = \int (\alpha_1)_a(x) \mathbf{\Phi}^a(x)\, dvol_\Sigma(x)$ and $A_2 = \int (\alpha_2)_a(x) \mathbf{\Phi}^a(x)\, dvol_\Sigma(x)$ be two linear observables. Then

$$
  \begin{aligned}
    A_1 \star_H A_2
    & =
    A_1 A_2 
    +
    \hbar 
    \int 
    \left( 
      \tfrac{i}{2} \Delta^{a_1 a_2}(x_1, x_2) + H^{a_1 a_2}(x_1,x_2)  
     \right) 
      \frac{\partial A_1}{\partial \mathbf{\Phi}^{a_1}(x_1)}
      \frac{\partial A_2}{\partial \mathbf{\Phi}^{a_2}(x_2)}
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

Now since $\Delta$ is skew-symmetric while $H$ is symmetric is follows that

$$
  \begin{aligned}
    A_1 \star_H A_2
    - 
    A_2 \star_H A_1
    & =
    i \hbar 
    \left(
     \int 
       (\alpha_1)_{a_1}(x_1)
       \Delta^{a_1 a_2}(x_1, x_2)
       (\alpha_2)_{a_2}(x_2)
    \right)
    \;mod\;
    \hbar^2
    \\
    & =
    i \hbar \, \left\{ A_1, A_2\right\}
  \end{aligned}
  \,.
$$

The right hand side is the [[integral kernel]]-expression for the [[Poisson-Peierls bracket]], as shown in the second line.


=--


+-- {: .num_example}
###### Example
**([[Hadamard vacuum state]] [[2-point function]])**

Let 

$$
  A_i \in LinObs(E,\mathbf{L})_{mc} \hookrightarrow PolyObs(E,\mathbf{L})_{mc}
$$

for $i \in \{1,2\}$ be two [[linear observable|linear]] [[microcausal observables]] represented by [[distributions]] which in [[generalized function]]-notation are given by

$$
  A_i
  \;=\;
  \int (\alpha_i)_{a_i}(x_i) \mathbf{\Phi}^{a_i}(x_i) \, dvol_\Sigma(x_i)
  \,.
$$

Then their Hadamard-Moyal [[star product]] (prop. \ref{MoyalStarProductOnMicrocausal}) is the [[sum]] of their pointwise product with $\tfrac{1}{2} i \hbar$ times the evaluation 

$$
  \begin{aligned}
    \langle A_1 A_2\rangle
    & \coloneqq
    \int \int
      (\alpha_1)_{a_1}(x_1) 
      \,
      \left\langle \mathbf{\Phi}^{a_1}(x_1) \mathbf{\Phi}^{a_2}(x_2)\right\rangle
     \,  
     (\alpha_2)_{a_2}(x_2)
     \, dvol_\Sigma(x_1)
     \, dvol_\Sigma(x_2)
    \\
    & \coloneqq
      \tfrac{1}{2} 
     i \hbar \int \int 
     (\alpha_1)_{a_1}(x_1) \Delta_H^{a_1 a_2}(x_1,x_2) (\alpha_2)_{a_2}(x_2)
      \,dvol_\Sigma(x_1)
      \,dvol_\Sigma(x_2)
  \end{aligned}
$$

of the [[Wightman propagator]] $\Delta_H$:

$$
  \label{StarProductOfTwoLinearObservables}
  A_1 \star_H A_2
  =
  A_1 \cdot A_2
  +
  \langle A_1 A_2\rangle
$$

Further [below](#HadamardVacuumStatesOnWickAlgebras) we see that this evaluation is the [[2-point function]] of a [[state on a star-algebra|state]] on the [[Wick algebra]].

=--


+-- {: .num_example #WeylRelations}
###### Example
**([[Weyl relations]])**

Let $(E,\mathbf{L})$ a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green hyperbolic]] [[equations of motion]] and with [[Wightman propagator]] $\Delta_H$.

Then for 

$$
  A_1, A_2 
  \;\in\;
  LinObs(E,\mathbf{L})_{mc}
  \hookrightarrow
  PolyObs(E,\mathbf{L})_{mc}
$$

two [[linear observables|linear]] [[microcausal observables]], the Hadamard-Moyal star product (def. \ref{MoyalStarProductOnMicrocausal}) of their [[exponentials]] exhibits the [[Weyl relations]]:

$$
  e^{A_1}
  \star_H
  e^{A_2}
  \;=\;
  e^{A_1 + A_2} \; e^{\langle A_1 A_2\rangle}
$$

where on the right we have the [[exponential]] [[Wightman 2-point function]] (eq:StarProductOfTwoLinearObservables).

=--

(e.g. [Dütsch 18, exercise 2.3](#Duetsch18))

## Properties

### Hadamard vacuum states 
 {#HadamardVacuumStatesOnWickAlgebras}

+-- {: .num_prop #WickAlgebraCanonicalState}
###### Proposition
**(canonical [[state on a star algebras|state]] on abstract [[Wick algebra]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]; and let $\Delta_H$ be a compatible [[Wightman propagator]]. 

Consider the function

$$
  \array{
    PolyObs(E,\mathbf{L})_{mc}[ [[\hbar] ]
    &\overset{\langle -\rangle_H}{\longrightarrow}&
    \mathbb{C}[ [\hbar] ]
    \\
    \left.
    \begin{aligned}
      A & = \alpha^{(0)}
      \\ & \phantom{=} + \underset{\Sigma}{\int} \alpha^{(1)}_a(x) \mathbf{\Phi}^a(x) \, dvol_\Sigma(x)
      \\
      & \phantom{=} + \cdots
    \end{aligned}
    \right\}
    &\mapsto&
    A(0) = \alpha^{(0)}
  }
$$

which sends each ([[microcausal polynomial observables|microcausal]]) [[polynomial observable]] to its value $A(\Phi = 0)$ on the zero [[field history]], hence to the constant contribution $\alpha^{(0)}$ in its [[polynomial]] expansion.

This function $\langle -\rangle_H$ is a [[state on a star-algebra|state]] on the [[Wick algebra]] $\left( (PolyObs(E,\mathbf{L}))_{mc}[ [\hbar] ], \star_H\right)$ (prop. \ref{MoyalStarProductOnMicrocausal}) in that it is

1. [[linear function|linear]] over $\mathbb{C}[ [\hbar] ]$;

1. positive, in that for all $A \in PolyObs(E,\mathbf{L})_{mc}[ [\hbar] ]$ 

   $$
     \langle A^\ast \star_H A\rangle_H \geq 0
   $$

   in the sense that the first non-vanishing coefficient of a power of $\hbar$ (if any) is a [[positive real number]]

1. normalized, in that 

   $$
     \langle 1\rangle_H = 1
   $$

=--

(positivity follows by positive semi-definiteness of [[Hadamard distributions]], [this condition](Hadamard+distribution#PositiveSemiDefiniteness)...)

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

Review is in

* {#Duetsch18} [[Michael Dütsch]], section 2.1 of _[[From classical field theory to perturbative quantum field theory]]_, 2018


The conceptualization of the shift by the Hadamard state as a step in the almost-K&#228;hler version of [[Fedosov deformation quantization]] is due to

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))


[[!redirects Wick algebras]]


[[!redirects Wick polynomial]]
[[!redirects Wick polynomials]]

[[!redirects normal ordering]]

[[!redirects normal-ordered product]]
[[!redirects normal-ordered products]]

[[!redirects normal ordered product]]
[[!redirects normal ordered products]]

[[!redirects abstract Wick algebra]]
[[!redirects abstract Wick algebras]]

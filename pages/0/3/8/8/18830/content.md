## Free quantum fields
 {#FreeQuantumFields}

We discuss here the [[quantum observables]] for the special case of
[[free field theories]] (def. \ref{FreeFieldTheory}). In [[perturbative quantum field theory]] this is the
basis of the construction of all [[interaction|interacting]] theories in the [[infinitesimal neighbourhood]]
of the [[free field theories]].


$\,$

[[!include Wick algebra -- table]]

$\,$

We now discuss these topics

* _[Abstract Wick algebra](#WickAlgebraAbstact)_

* [Time-ordered product on regular polynomial observables](#TimeOrderedProuctOnRegularPolynomialObservables)




$\,$



$\,$

**abstract [[Wick algebra]]**
 {#WickAlgebraAbstract}

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


$\,$

$\,$

**[[time-ordered product]] on [[regular polynomial observables]]**
 {#TimeOrderedProuctOnRegularPolynomialObservables}

+-- {: .num_defn #OnRegularPolynomialObservablesTimeOrderedProduct}
###### Definition
**([[time-ordered product]] on [[regular polynomial observables]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] 
over a [[Lorentzian manifold|Lorentzian]] [[spacetime]] and with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[differential equations]]; write $\Delta_S = \Delta_+ - \Delta_-$ for the induced [[causal propagator]]. Let moreover $\Delta_H = \tfrac{i}{2}\Delta_S + H $ be a compatible [[Wightman propagator]] and write $\Delta_F = \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$ for the induced [[Feynman propagator]].

Then the _[[time-ordered product]]_ on the space of [[on-shell]] [[regular polynomial observable]] $PolyObs(E,\mathbf{L})_{reg}$ is the [[star product]] induced by the [[Feynman propagator]] (via [this prop.](star+product#PropagatorStarProduct)):

$$
  \array{
    PolyObs(E,\mathbf{L})_{reg}[ [\hbar] ]
    \otimes
    PolyObs(E,\mathbf{L})_{reg}[ [\hbar] ]
      &\overset{T((-)(-))}{\longrightarrow}&
    PolyObs(E,\mathbf{L})_{reg}[ [\hbar] ]
    \\
    (A_1, A_2)
    &\mapsto&
    \phantom{\coloneqq} A_1 \star_F A_2
  }
$$

hence

$$
  T(A_1 A_2)
  \coloneqq
  ((-)\cdot(-))
  \circ
  \exp\left(
    \underset{\Sigma \times \Sigma}{\int}
    \Delta_F^{a b}(x,y)
    \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
    \otimes
    \frac{\delta}{\delta \mathbf{\Phi}^b(y)}
    \,
    dvol_\Sigma(x)
    \,
    dvol_\Sigma(y)
  \right)
$$

=--

+-- {: .num_prop #CausalOrderingTimeOrderedProductOnRegular}
###### Proposition
**([[time-ordered product]] is indeed causally ordered [[Wick algebra]] product)**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] 
over a [[Lorentzian manifold|Lorentzian]] [[spacetime]] and with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[differential equations]]; write $\Delta_S = \Delta_+ - \Delta_-$ for the induced [[causal propagator]]. Let moreover $\Delta_H = \tfrac{i}{2}\Delta_S + H $ be a compatible [[Wightman propagator]] and write $\Delta_F = \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$ for the induced [[Feynman propagator]].

Then the [[time-ordered product]] on [[regular polynomial observables]] (def. \ref{OnRegularPolynomialObservablesTimeOrderedProduct}) is indeed a time-ordering of the [[Wick algebra]] product $\star_H$ in that for all [[pairs]] of [[regular polynomial observables]]

$$
  A_1, A_2 \in PolyObs(E,\mathbf{L})_{reg}[ [\hbar] ]
$$

with [[disjoint subset|disjoint]] [[spacetime]] [[support]] we have

$$  
  T(A_1 A_2)
  \;=\;
  \left\{
    \array{
      A_1 \star_H A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
      \\
      A_2 \star_H A_1 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)
    }
  \right.
  \,.
$$

Here $S_1 {\vee\!\!\!\wedge} S_2$ is the [[causal order]] relation ("$S_1$ does not intersect the [[past cone]] of $S_2$"). Beware that for general [[pairs]] $(S_1, S-2)$ of subsets neither $S_1 {\vee\!\!\!\wedge} S_2$ nor $S_2 {\vee\!\!\!\wedge} S_1$.

=--


+-- {: .proof}
###### Proof

The [[advanced and retarded propagators]] $\Delta_{pm}$ by definition are [[support|supported]] in the [[future cone]]/[[past cone]], respectively

$$
  supp(\Delta_{\pm}) \subset \overline{V}^{\pm}
$$

and since they turn into each other under exchange of their arguments ([this cor.](causal+propagator#CausalPropagatorIsSkewSymmetric)):

$$
  \Delta_\pm(y,x) = \Delta_{\mp}(x,y)
  \,.
$$

Using this we compute as follows:

$$
  \begin{aligned}
    A_1 \underset{\Delta_{F}}{\star} A_2
    & =
    A_1 \underset{\tfrac{i}{2}(\Delta_+ + \Delta_-) + H}{\star} A_2
    \\
    & =
    \left\{
      \array{
        A_1 \underset{\tfrac{i}{2}\Delta_+ + H}{\star} A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       \\
       A_1 \underset{\tfrac{i}{2}\Delta_- + H}{\star} A_2 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)    
      }
    \right.
    \\
    & = 
    \left\{
      \array{
        A_1 \underset{\tfrac{i}{2}\Delta_+ + H}{\star} A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       \\
       A_2 \underset{\tfrac{i}{2}\Delta_+ + H}{\star} A_1 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)    
      }
    \right.
    \\
    & =
    \left\{
      \array{
        A_1 \underset{\tfrac{i}{2}(\Delta_+ - \Delta_-) + H}{\star} A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       \\
       A_2 \underset{\tfrac{i}{2}(\Delta_+ - \Delta_-) + H}{\star} A_1 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)    
      }
    \right.
    \\
    & =
    \left\{
      \array{
        A_1 \underset{\Delta_H}{\star} A_2 &\vert& supp(A_1) {\vee\!\!\!\wedge} supp(A_2)
       \\
       A_2 \underset{\Delta_H}{\star} A_1 &\vert& supp(A_2) {\vee\!\!\!\wedge} supp(A_2)    
      }
    \right.
  \end{aligned}
$$


=--

## Free quantum fields
 {#FreeQuantumFields}

We discuss here the [[quantum observables]] for the special case of
[[free field theories]] (def. \ref{FreeFieldTheory}). In [[perturbative quantum field theory]] this is the
basis of the construction of all [[interaction|interacting]] theories in the [[infinitesimal neighbourhood]]
of the [[free field theories]].


$\,$


We now discuss these topics:

* _[Wick algebra](#WickAlgebraAbstract)_

* _[Time-ordered product](#AbstractTimeOrderedProduct)_

* _[Operator product notation](#OperatorProductAndNormalOrderedProduct)_

* _[Hadamard vacuum state](#HadamardVacuumStatesOnWickAlgebras)_

* _[Free quantum BV-differential](#FreeQuantumBVDifferential)_

* _[Schwinger-Dyson equation](#SchwingerDysonEquation)_

$\,$


**[[Wick algebra]]**
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
  \begin{aligned}
  A(\Phi)
  & =
  \phantom{+} \alpha^{(0)}
  \\
  & \phantom{=}
  +
  \int_\Sigma
    \alpha^{(1)}_a(x) \Phi^a(x)
   \,
  dvol_\Sigma(x)
  \\
  & \phantom{=}
  +
  \int_\Sigma \int_\Sigma
   \alpha^{(2)}_{a_1 a_2}(x_1, x_2)
   \Phi^{a_1}(x_1) \Phi^{a_2}(x_2)
  \,dvol_\Sigma(x_1)
  \, dvol_\Sigma(x_2)
  \\
  & \phantom{=}
  +
  \cdots
  \,,
  \end{aligned}
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

([Dito 90](deformation+quantization#Dito90), [Dütsch-Fredenhagen 00](deformation+quantization#DuetschFredenhagen00) [Dütsch-Fredenhagen 01](deformation+quantization#DuetschFredenhagen01), [Hirshfeld-Henselder 02](deformation+quantization#HirschfeldHenselder02), [Collini 16, p. 25-26](deformation+quantization#Collini16))


+-- {: .proof}
###### Proof

By definition of [[Wightman propagator]], the [[wave front set]] of powers of $\Delta_H$ has all cotangents on the first variables future pointing, and all those on the second variables past pointing. The first variables are integrated against those of $A_1$ and the second against $A_2$. By definition of [[microcausal observables]] (def. \ref{MicrocausalObservable}), the wave front sets of $A_1$ and $A_2$ are disjoint from the subsets where all components are future pointing or all components are past-pointing. Therefore the relevant sum of of the wave front covectors never vanishes and hence [[Hörmander's criterion]] is met and the star product is well defined.

It remains to see that the star product $A_1 \star_H A_2$ is itself again a [[microcausal observable]]. It is clear that it is again a [[polynomial observable]] and that it respects the ideal generated by the equations of motion. That it still satisfies the condition on the [[wave front set]] follows directly from the fact that the wave front set of a [[product of distributions]] is inside the fiberwise sum of elements of the factor wave front sets (prop. \ref{WaveFrontSetOfProductOfDistributionsInsideFiberProductOfFactorWaveFrontSets}).

Finally the [[star algebra]]-structure via [[complex conjugatioon]] follows via remark \ref{WightmanPropagatorAsKaehlerVectorSpaceStructure} as in prop. \ref{StarProductAlgebraOfKaehlerVectorSpaceIsStarAlgebra}.

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

$\,$

**[[time-ordered product]]**
 {#AbstractTimeOrderedProduct}

+-- {: .num_defn #OnRegularPolynomialObservablesTimeOrderedProduct}
###### Definition
**([[time-ordered product]] on [[regular polynomial observables]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]]
over a [[Lorentzian manifold|Lorentzian]] [[spacetime]] and with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[differential equations]]; write $\Delta_S = \Delta_+ - \Delta_-$ for the induced [[causal propagator]]. Let moreover $\Delta_H = \tfrac{i}{2}\Delta_S + H $ be a compatible [[Wightman propagator]] and write $\Delta_F = \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$ for the induced [[Feynman propagator]].

Then the _[[time-ordered product]]_ on the space of [[off-shell]] [[regular polynomial observable]] $PolyObs(E)_{reg}$ is the [[star product]] induced by the [[Feynman propagator]] (via [this prop.](star+product#PropagatorStarProduct)):

$$
  \array{
    PolyObs(E)_{reg}[ [\hbar] ]
    \otimes
    PolyObs(E)_{reg}[ [\hbar] ]
      &\overset{}{\longrightarrow}&
    PolyObs(E)_{reg}[ [\hbar] ]
    \\
    (A_1, A_2)
    &\mapsto&
    \phantom{\coloneqq} A_1 \star_F A_2
  }
$$

hence

$$
  A_1 \star_F A_2
  \;
  \coloneqq
  \;
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

(Notice that this does not descend to the [[on-shell]] observables, since the [[Feynman propagator]] is not a solution to the _homogeneous_ [[equations of motion]].)

=--

+-- {: .num_prop #CausalOrderingTimeOrderedProductOnRegular}
###### Proposition
**([[time-ordered product]] is indeed causally ordered [[Wick algebra]] product)**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]]
over a [[Lorentzian manifold|Lorentzian]] [[spacetime]] and with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[differential equations]]; write $\Delta_S = \Delta_+ - \Delta_-$ for the induced [[causal propagator]]. Let moreover $\Delta_H = \tfrac{i}{2}\Delta_S + H $ be a compatible [[Wightman propagator]] and write $\Delta_F = \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$ for the induced [[Feynman propagator]].

Then the [[time-ordered product]] on [[regular polynomial observables]] (def. \ref{OnRegularPolynomialObservablesTimeOrderedProduct}) is indeed a time-ordering of the [[Wick algebra]] product $\star_H$ in that for all [[pairs]] of [[regular polynomial observables]]

$$
  A_1, A_2 \in PolyObs(E)_{reg}[ [\hbar] ]
$$

with [[disjoint subset|disjoint]] [[spacetime]] [[support]] we have

$$
  A_1 \star_F A_2
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

Recall the following facts:

1. the [[advanced and retarded propagators]] $\Delta_{\pm}$ by definition are [[support|supported]] in the [[future cone]]/[[past cone]], respectively

   $$
     supp(\Delta_{\pm}) \subset \overline{V}^{\pm}
   $$

1. they turn into each other under exchange of their arguments ([this cor.](causal+propagator#CausalPropagatorIsSkewSymmetric)):

   $$
     \Delta_\pm(y,x) = \Delta_{\mp}(x,y)
     \,.
   $$

1. the real part $H$ of the [[Feynman propagator]], which by definition is the real part of the [[Wightman propagator]] is symmetric (by definition or else by [this prop.](Hadamard+distribution#SkewSymmetricPartOfHadmrdPropagatorIsCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetime)):

   $$
     H(x,y) = H(y,x)
   $$

Using this we compute as follows:

$$
  \begin{aligned}
    A_1 \underset{\Delta_{F}}{\star} A_2
    \;
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


+-- {: .num_prop #IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise}
###### Proposition
**([[time-ordered product]] on [[regular polynomial observables]] [[isomorphism|isomorphic]] to pointwise product)

The [[time-ordered product]] on [[regular polynomial observables]] (def. \ref{CausalOrderingTimeOrderedProductOnRegular}) is [[isomorphism|isomorphism]] to the pointwise product of [[observables]] ([this def.](A+first+idea+of+quantum+field+theory#Observable)) via the [[linear isomorphism]]

$$
  \mathcal{T}
  \;\colon\;
  PolyObs(E)_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E)_{reg}[ [\hbar] ]
$$

given by

$$
  \mathcal{T}A
  \;\coloneqq\;
  \exp\left(
    \tfrac{1}{2}
    \hbar 
    \underset{\Sigma}{\int} 
     \Delta_F(x,y)^{a b} 
     \frac{\delta^2}{\delta \mathbf{\Phi}^a(x) \delta \mathbf{\Phi}^b(y)}
  \right)
  A
$$

in that 

$$
  \begin{aligned}
    T(A_1 A_2)
    & \coloneqq
    A_1 \star_{F} A_2
    \\
    & =
    \mathcal{T}( \mathcal{T}^{-1}(A_1) \cdot \mathcal{T}^{-1}(A_2) )
  \end{aligned}
$$

hence

$$
  \array{
    PolyObs(E)_{reg}[ [\hbar] ]
      \otimes
    PolyObs(E)_{reg}[ [\hbar] ]
      &\overset{(-)\cdot (-)}{\longrightarrow}&   
    PolyObs(E)_{reg}[ [\hbar] ]
    \\
    {}^{\mathllap{\mathcal{T} \otimes \mathcal{T}}}_\simeq\Big\downarrow 
      && 
    \downarrow^{\mathrlap{\mathcal{T}}}_\simeq
    \\
    PolyObs(E)_{reg}[ [\hbar] ]
      \otimes
    PolyObs(E)_{reg}[ [\hbar] ]
      &\overset{(-) \star_F (-)}{\longrightarrow}&   
    PolyObs(E)_{reg}[ [\hbar] ]
  }
$$

=--


([Brunetti-Dütsch-Fredenhagen 09, (12)-(13)](time-ordered+product#BrunettiDuetschFredenhagen09), [Fredenhagen-Rejzner 11b, (14)](time-ordered+product#FredenhagenRejzner11b))

+-- {: .proof}
###### Proof

Since the [[Feynman propagator]] is symmetric ([this prop.](A+first+idea+of+quantum+field+theory#SymmetricFeynmanPropagator)), the statement is a special case of [this prop.](star+product#SymmetricContribution)).

=--


+-- {: .num_remark }
###### Remark
**([[renormalization]] of [[time-ordered product]])**


The [[time-ordered product]] on [[regular polynomial observables]] from prop. \ref{OnRegularPolynomialObservablesTimeOrderedProduct} extends to a product on [[polynomial observable|polynomial]] [[local observables]] (def. \ref{LocalObservables}), then taking values in [[microcausal observables]] (def. \ref{MicrocausalObservable}):

$$
  T
  \;\colon\;
  PolyLocObs(E)^{\otimes_n}[ [\hbar] ]
    \longrightarrow
  PolyObs(E)_{mc}[ [\hbar] ]
  \,.
$$

This extension is not unique. A choice of such an extension, satisfying some evident compatibility conditions, is a choice of _[[renormalization scheme]]_ for the given [[perturbative quantum field theory]]. Every such choice corresponds to a choice of [[perturbative S-matrix]] for the theory. This construction is called _[[causal perturbation theory]]_. 

This we discuss below in chapter _[Scattering](#Scattering)_ and chapter _[Renormalization](#Renormalization)_.

=--


$\,$

**operator product notation**
 {#OperatorProductAndNormalOrderedProduct}

+-- {: .num_defn #NormalOrderedProductNotation}
###### Definition
**(notation for [[operator product]] and [[normal-ordered product]])**

It is traditional to use the following alternative notation for the product structures on [[microcausal polynomial observables]]:


1. The [[Wick algebra]]-product, hence the [[star product]] $\star_H$ for the [[Wightman propagator]] (def. \ref{MoyalStarProductOnMicrocausal}), is rewritten as plain juxtaposition:

   $$
     \text{"operator product"}
     \phantom{AAA}
     A_1 A_2 \phantom{AA} \coloneqq \phantom{AA} A_1 \star_H A_1
     \phantom{AAAA}
     \array{
       \text{star product of}
       \\
       \text{Wightman propagator}
     }
     \,.
   $$

1. The pointwise product of observables ([this def.](A+first+idea+of+quantum+field+theory#Observable))  $A_1 \cdot A_2$
   is equivalently written as plain juxtaposition enclosed by colons:

   $$
     \array{
       \text{"normal-ordered}
       \\
       \text{product"}
     }
     \phantom{AAAA}
     :A_1 A_2:
      \phantom{AA}\coloneqq\phantom{AA}
     A_1 \cdot A_2
     \phantom{AAAA} \phantom{AAa}\text{pointwise product}\phantom{AAa}
   $$

1. The [[time-ordered product]], hence the [[star product]] for the [[Feynman propagator]] $\star_F$ (def. \ref{OnRegularPolynomialObservablesTimeOrderedProduct}) is equivalently written as plain juxtaposition prefixed by a "$T$"

   $$
     \array{
       \text{"time-ordered}
       \\
       \text{product"}
     }
     \phantom{AAAA}
     T(A_1 A_2)
      \phantom{AA}\coloneqq\phantom{AA}
     A_1 \star_F A_2
     \phantom{AAAA}
     \array{
       \text{star product of}
       \\
       \text{Feynman propagator}
     }
   $$

Under [[representation]] of the [[Wick algebra]] on a [[Fock space|Fock]] [[Hilbert space]] by [[linear operators]]
the first product become the _[[operator product]]_, while the second becomes the operator poduct applied after
suitable re-ordering, called "[[normal-ordered product|normal odering]]" of the factors.

Disregarding the [[Fock space]]-representation, which is [[faithful representation|faithful]], we may still
refer to these "abstract" products as the "operator product" and the "normal-ordered product", respectively.

=--


[[!include Wick algebra -- table]]





**[[Hadamard vacuum state]]**
 {#HadamardVacuumStatesOnWickAlgebras}

+-- {: .num_prop #WickAlgebraCanonicalState}
###### Proposition
**(canonical [[Hadamard vacuum state|vacuum]] [[state on a star-algebra|states]] on abstract [[Wick algebra]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]; and let $\Delta_H$ be a compatible [[Wightman propagator]].

For

$$
  \Phi_0 \in \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
$$

any [[on-shell]] [[field history]] (i.e. solving the [[equations of motion]]), consider the function from the [[Wick algebra]] to [[formal power series]] in $\hbar$ with [[coefficients]] in the [[complex numbers]]
which evaluates any [[microcausal polynomial observable]] on $\Phi_0$


$$
  \array{
    PolyObs(E,\mathbf{L})_{mc}[ [[\hbar] ]
    &\overset{\langle -\rangle_{\Phi_0}}{\longrightarrow}&
    \mathbb{C}[ [\hbar] ]
    \\
    A &\mapsto& A(\Phi_0)
  }
$$

Specifically for $\Phi_0 = 0$ (which is a solution of the [[equations of motion]] by the assumption that $(E,\mathbf{L})$ defines a [[free field theory]]) this is the function

$$
  \array{
    PolyObs(E,\mathbf{L})_{mc}[ [[\hbar] ]
    &\overset{\langle -\rangle_0}{\longrightarrow}&
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

which sends each [[microcausal polynomial observable]] to its value $A(\Phi = 0)$ on the zero [[field history]], hence to the constant contribution $\alpha^{(0)}$ in its [[polynomial]] expansion.

The function $\langle -\rangle_0$ is

1. [[linear function|linear]] over $\mathbb{C}[ [\hbar] ]$;

1. real, in that for all $A \in PolyObs(E,\mathbf{L})_{mc}[ [\hbar] ]$

   $$
     \langle A^\ast \rangle = \langle A \rangle^\ast
   $$

1. positive, in that for every $A \in PolyObs(E,\mathbf{L})_{mc}[ [\hbar] ]$ there exist a $c_A \in \mathbb{C}[ [\hbar] ]$ such that

   $$
     \langle A^\ast \star_H A\rangle_{\Phi_0} = c_A^\ast \cdot c_A
     \,,
   $$

1. normalized, in that

   $$
     \langle 1\rangle_H = 1
   $$

where $(-)^\ast$ denotes componet-wise [[complex conjugation]].


This means that $\langle -\rangle_{0}$ is a [[state on a star-algebra|states]] on the [[Wick algebra|Wick]] [[star-algebra]] $\left( (PolyObs(E,\mathbf{L}))_{mc}[ [\hbar] ], \star_H\right)$ (prop. \ref{MoyalStarProductOnMicrocausal}). One says that

* $\langle - \rangle_0$ is a _[[Hadamard vacuum state]]_;

and generally

* $\langle - \rangle_{\Phi_0}$ is called a _[[coherent state]]_.


=--

([Dütsch 18, def. 2.12, remark 2.20, def. 5.28, exercise 5.30 and equations (5.178)](#Duetsch18))


+-- {: .proof}
###### Proof

The properties of linearity, reality and normalization are obvious, what requires proof is positivity. This is proven by exhibiting a [[representation]] of the Wick algebra on a [[Fock space|Fock]] [[Hilbert space]] (this algebra [[homomorphism]] is _[[Wick's lemma]]_), with formal powers in $\hbar$ suitably taken care of, and showing that under this representation the function $\langle -\rangle_0$ is represented, degreewise in $\hbar$, by the [[inner product]] of the [[Hilbert space]].

=--

+-- {: .num_example #HadamardMoyalStarProductOfTwoLinearObservables}
###### Example
**([[operator product]] of two [[linear observables]])**

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

Then their Hadamard-Moyal [[star product]] (prop. \ref{MoyalStarProductOnMicrocausal}) is the [[sum]] of their pointwise product
with their value

$$
  \label{EvaluatingLinearObservablesInWightmanPropagator}
  \langle A_1 \star_H A_2 \rangle_0
  \;\coloneqq\;
  i \hbar \int \int
   (\alpha_1)_{a_1}(x_1) \Delta_H^{a_1 a_2}(x_1,x_2) (\alpha_2)_{a_2}(x_2)
   \,dvol_\Sigma(x_1)
   \,dvol_\Sigma(x_2)
$$

in the [[Wightman propagator]], which is the value of the [[Hadamard vacuum state]] from prop. \ref{WickAlgebraCanonicalState}

$$
  A_1 \star_H A_2
  \;=\;
  A_1 \cdot A_2
  \;+\;
  \langle A_1 \star_H A_2 \rangle_0
$$

In the [[operator product]]/[[normal-ordered product]]-notation of def. \ref{NormalOrderedProductNotation} this reads

$$
  A_1 A_2 \;=\; :A_1 A_2: \;+\; \langle A_1 A_2\rangle
  \,.
$$


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
  e^{A_1 + A_2} \; e^{\langle A_1 \star_H A_2\rangle_0}
$$

where on the right we have the [[exponential]] of the value of the [[Hadamard vacuum state]] (prop. \ref{WickAlgebraCanonicalState}) as in example \ref{HadamardMoyalStarProductOfTwoLinearObservables}.

=--

(e.g. [Dütsch 18, exercise 2.3](#Duetsch18))



+-- {: .num_example }
###### Example
**([[Wightman propagator]] is [[2-point function]] in the [[Hadamard vacuum state]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]; and let $\Delta_H$ be a compatible [[Wightman propagator]].


With respect to the induced [[Hadamard vacuum state]] $\langle - \rangle_0$ from prop. \ref{WickAlgebraCanonicalState}, the [[Wightman propagator]] $\Delta_H(x,y)$ itself is the _[[2-point function]]_, namely the [[distribution|distributional]] [[vacuum expectation value]] of the operator product of two [[field observables]]:

$$
  \left\langle
    \mathbf{\Phi}^a(x) \star_H \mathbf{\Phi}^b(y)
  \right\rangle_0
  \;=\;
  \underset{ = 0 }{
  \underbrace{
    \left\langle
       \mathbf{\Phi}(x) \cdot \mathbf{\Phi}(y)
    \right\rangle
  }}
  +
  \underset{ = \hbar \Delta^{a b}_H(x,y) }{
  \underbrace{
    \left \langle
      \hbar
      \underset{\Sigma \times \Sigma}{\int}
       \delta(x-x') \Delta^{a b}_H(x,y) \delta(y-y')
    \right\rangle
  }}
$$

by example \ref{HadamardMoyalStarProductOfTwoLinearObservables}.

Equivalently in the [[operator product]]-notation of def. \ref{NormalOrderedProductNotation} this reads:

$$
  \left\langle
    \mathbf{\Phi}^a(x)
    \mathbf{\Phi}^b(y)
  \right\rangle_0
  \;=\;
  \hbar \Delta_H(x,y)
  \,.
$$

=--

Similarly:

+-- {: .num_example }
###### Example
**([[Feynman propagator]] is time-ordered [[2-point function]] in the [[Hadamard vacuum state]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] with [[Green hyperbolic differential equation|Green-hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]; and let $\Delta_H$ be a compatible [[Wightman propagator]] with induced [[Feynman propagator]] $\Delta_F$.


With respect to the induced [[Hadamard vacuum state]] $\langle - \rangle_0$ from prop. \ref{WickAlgebraCanonicalState}, the [[Feynman propagator]] $\Delta_F(x,y)$ itself is the _time-ordered [[2-point function]]_, namely the [[distribution|distributional]] [[vacuum expectation value]] of the [[time-ordered product]] (def. \ref{OnRegularPolynomialObservablesTimeOrderedProduct}) of two [[field observables]]:

$$
  \left\langle
    T\left(
      \mathbf{\Phi}^a(x) \star_F \mathbf{\Phi}^b(y)
    \right)
  \right\rangle_0
  \;=\;
  \underset{ = 0 }{
  \underbrace{
    \left\langle
       \mathbf{\Phi}(x) \cdot \mathbf{\Phi}(y)
    \right\rangle
  }}
  +
  \underset{ = \hbar \Delta^{a b}_H(x,y) }{
  \underbrace{
    \left \langle
      \hbar
      \underset{\Sigma \times \Sigma}{\int}
       \delta(x-x') \Delta^{a b}_F(x,y) \delta(y-y')
    \right\rangle
  }}
$$

analogous to example \ref{HadamardMoyalStarProductOfTwoLinearObservables}.

Equivalently in the [[operator product]]-notation of def. \ref{NormalOrderedProductNotation} this reads:

$$
  \left\langle
    T\left(
     \mathbf{\Phi}^a(x)
     \mathbf{\Phi}^b(y)
    \right)
  \right\rangle_0
  \;=\;
  \hbar \Delta_F(x,y)
  \,.
$$

=--

[[!include propagators - table]]


$\,$

**[[BV-operator|free quantum BV-differential]]**
  {#FreeQuantumBVDifferential}

So far we have discussed the plain (graded-commutative) [[algebra of quantum observables]] of a [[gauge fixing|gauged fixed]] [[free field theory|free]] [[Lagrangian field theory]], [[deformation quantization|deforming]] the commutative pointwise product of [[observables]]. But after [[gauge fixing]], the algebra of observables is not just a (graded-commutative) algebra, but carries also a [[differential]] making it a [[differential graded-commutative superalgebra]]: the global [[BV-differential]] $\{-S' + S_{BRST}, -\}$ (def. \ref{ComplexBVBRSTGlobal}). The [[gauge invariance|gauge invariant]] [[on-shell]] [[observables]] are (only) the [[cochain cohomoloy]] of this differential. Here we discuss what becomes of this differential as we pass to the non-commutative [[Wick algebra|Wick]]-[[algebra of quantum observables]].


+-- {: .num_prop #OnMicrocausalObservablesGlobalBVDifferential}
###### Proposition
**(global [[BV-differential]] restricts to [[derivation]] on [[microcausal polynomial observables]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$ (remark \ref{FieldBundleBVBRST}). Let $\Delta_H$ be a compatible [[Wightman propagator]] (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}). 

Then the global [[BV-differential]] $\{-S',(-)\}$ (def. \ref{ComplexBVBRSTGlobal}) restricts from [[polynomial observables]] to a linear map on [[microcausal polynomial observables]] (def. \ref{MicrocausalObservable})

$$
  \{-S',(-)\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [\hbar] ]
$$

and as such is a [[derivation]] not only for the pointwise product, but also for the product in the [[Wick algebra]] (the [[star product]] induced by the [[Wightman propagator]]):

$$
  \{-S', A_1 \star_H A_2\}
  \;=\;
  \{-S', A_1\} \star_H A_2
  + 
  A_1 \star_H \{-S', A_2\}
$$

=--

+-- {: .proof}
###### Proof

By example \ref{BVDifferentialGlobal} the action of $\{-S',(-)\}$ on polyomial observables is to replace [[antifield]] [[field observables]] by 

$$
  \mathbf{\Phi}^\ddagger_a(x)
  \;\mapsto\;
  \pm
   (P_{A B}\mathbf{\Phi}^A)(x)
  \,,
$$

where $P$ is a [[differential operator]]. By [[partial integration]] this translates to $\{-S',(-)\}$ acting by the [[formally adjoint differential operator]] $P^\ast$ (def. \ref{FormallyAdjointDifferentialOperators}) via [[derivative of distributions|distributional derivative]] on the [[distribution|distributional]] [[coefficients]] of the given polynomial observable. 

Now by prop. \ref{RetainsOrShrinksWaveFrontSetDifferentialOperator} the application of $P^\ast$ retains or shrinks the [[wave front set]] of the distributional coefficient, hence it preserves the microcausality condition (def. \ref{MicrocausalObservable}). This makes $\{-S',(-)\}$ restrict to microcausal polynomial observables.

To see that $\{-S',(-)\}$ thus restricted is a [[derivation]] of the Wick algebra product, it is sufficient to see that its [[commutators]] with the [[Wightman propagator]] vanishes in each argument:

$$
  \left[
    \{-S',(-)\} \otimes id
    \;,\;
       \Delta_H
       \left( 
         \frac{\delta}{\delta \mathbf{\Phi}}  
           \otimes 
         \frac{\delta}{\delta \mathbf{\Phi}} 
       \right) 
  \right]
  \;=\;
  0
$$

and


$$
  \left[
    id \otimes \{-S',(-)\}
    \;,\;
       \Delta_H
       \left( 
         \frac{\delta}{\delta \mathbf{\Phi}}  
           \otimes 
         \frac{\delta}{\delta \mathbf{\Phi}} 
       \right) 
  \right]
  \;=\;
  0
  \,.
$$

Because with this we have:

$$
  \begin{aligned}
    \{-S', A_1 \star_H A_2\}
    & =
    \{-S',(-)\}
    \circ
     ((-)\cdot(-))
     \circ
     \exp\left( 
       \hbar
        \Delta_H\left( 
          \frac{\delta}{\delta \mathbf{\Phi}}
          \otimes
          \frac{\delta}{\delta \mathbf{\Phi}}
        \right)
     \right)
     (A_1 \otimes A_2)
     \\
     & =
     ((-)\cdot(-))
     \circ
     \left(
       \{-S',-\} \otimes it
       +
       id \otimes \{-S',(-)\}
     \right)
     \circ
     \exp\left( 
       \hbar
        \Delta_H\left( 
          \frac{\delta}{\delta \mathbf{\Phi}}
          \otimes
          \frac{\delta}{\delta \mathbf{\Phi}}
        \right)
     \right)
     (A_1 \otimes A_2)
     \\
     & =
     ((-)\cdot(-))
     \circ
     \exp\left( 
       \hbar
        \Delta_H\left( 
          \frac{\delta}{\delta \mathbf{\Phi}}
          \otimes
          \frac{\delta}{\delta \mathbf{\Phi}}
        \right)
     \right)
     \circ 
     \left(
       \{-S',-\} \otimes it
       +
       id \otimes \{-S',(-)\}
     \right)
     (A_1 \otimes A_2)
     \\
     & = 
     \{-S',A_1\} \star_H A_2
     +
     A_1 \star_H \{-S', A_2\}
  \end{aligned}
$$

Here in the first step we used that $\{-S',(-)\}$ is a derivation with respect to the pointwise product, by construction (def. \ref{ComplexBVBRSTGlobal}) and then we used the vanishing of the above commutators.

To see that these commutators indeed vanish

=--

+-- {: .num_defn #AntibracketTimeOrdered}
###### Definition
**([[time-ordered product|time-ordered]] [[antibracket]])


Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$ (remark \ref{FieldBundleBVBRST}).

Then the _time-ordered global [[antibracket]]_ on [[regular polynomial observables]] 

$$
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
   \otimes
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \overset{\{-,-\}_{\mathcal{T}}}{\longrightarrow}
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$

is the [[conjugation]] of the global [[antibracket]] ([this def. ](A+first+idea+of+quantum+field+theory#ComplexBVBRSTGlobal)) by the time-ordering operator $\mathcal{T}$ (from [this prop.](time-ordered+product#IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise)):

$$
  \{-,-\}_{\mathcal{T}}
  \;\coloneqq\;
  \mathcal{T}\left(\left\{ \mathcal{T}^{-1}(-), \mathcal{T}^{-1}(-)\right\}\right)
$$

hence

$$
  \array{
    PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
      \otimes
    PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
      &\overset{\{-,-\}}{\longrightarrow}&
    PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \\
    {}^{\mathllap{\mathcal{T}}}_{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\mathcal{T}}}_\simeq
    \\
    PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
      \otimes
    PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
      &\overset{ \{-,-\}_{\mathcal{T}} }{\longrightarrow}&
    PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
  }
$$

=--

([Fredenhagen-Rejzner 11, (27)](#FredenhagenRejzner11), [Rejzner 11, (5.14)](#Rejzner11))

+-- {: .num_prop #GaugeFixedActionFunctionalTimeOrderedAntibracket}
###### Proposition
**([[time-ordered product|time-ordered]] [[antibracket]] with [[gauge fixing|gauge fixed]] [[action functional]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$ (remark \ref{FieldBundleBVBRST}).

Then the [[time-ordered product|time-ordered]] [[antibracket]] (def. \ref{AntibracketTimeOrdered}) with the gauge fixed BV-[[action functional]] $-S'$ (def. \ref{ComplexBVBRSTGlobal}) equals the [[conjugation]] of the global [[BV-differential]] with the [[isomorphism]] $\mathcal{T}$ from the pointwise to the [[time-ordered product]] of [[observables]] (from [this prop.](time-ordered+product#IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise))

$$
  \{-S',-\}_{\mathcal{T}}
  \;=\;
  \mathcal{T} \circ \{-S',-\} \circ \mathcal{T}^{-1}
  \,,
$$

hence

$$
  \array{
    PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
     &\overset{ \{-S',-\} }{\longrightarrow}&
    PoyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \\
    {}^{\mathllap{\mathcal{T}}}\downarrow 
      &&
    \downarrow^{\mathrlap{\mathcal{T}}}
    \\
    PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
     &\overset{ \{-S',-\}_{\mathcal{T}} }{\longrightarrow}&
    PoyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
  }
$$

=--

+-- {: .proof}
###### Proof

By the assumption that $(E,\mathbf{L})$ is a [[free field theory]] its [[Euler-Lagrange equations]] are linear in the fields, and hence $S'$ is quadratic in the fields. This means that

$$
  \mathcal{T}^{-1}S' = S' + const
  \,,
$$

where the second term on the right is independent of the fields, and hence that

$$
  \{\mathcal{T}^{-1}(-S'),-\}
  = 
  \{-S', - \}
  \,.
$$

This implies the claim:

$$
  \begin{aligned}
    \{-S',-\}_{\mathcal{T}}
    & \coloneqq
    \mathcal{T}\left(\{ \mathcal{T}^{-1}(-S'), \mathcal{T}^{-1}(-) \}\right)
    \\
   & =
   \mathcal{T}\left(\{ -S', \mathcal{T}^{-1}(-) \}\right)
   \\
   & =
   \mathcal{T} \circ \{-S',-\} \circ \mathcal{T}^{-1}
   \,.
  \end{aligned}
$$


=--

+-- {: .num_defn #ForGaugeFixedFreeLagrangianFieldTheoryBVOperator}
###### Definition
**([[BV-operator]] for [[gauge fixing|gauge fixed]] [[free field theory|free]] [[Lagrangian field theory]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$ (remark \ref{FieldBundleBVBRST}) and with corresponding gauge-fixed global [[BV-BRST differential]] on graded [[regular polynomial observables]]

$$
  \{-S' + S'_{BRST}, -\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
  \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$ 

([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)).

Then the corresponding _[[BV-operator]]_ 

$$
  \Delta_{BV}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
  \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$ 

on [[regular polynomial observables]] is, up to a factor of $i \hbar$, the difference between the free component $\{-S',-\}$ of the gauge fixed global BV differential its time-ordered version (def. \ref{AntibracketTimeOrdered})

$$
  \Delta_{BV}
    \;\coloneqq\;
  \tfrac{1}{i \hbar}
  \left(
    \left\{
      -S',-
    \right\}_{\mathcal{T}}
    -
    \left\{ -S',(-) \right\}
  \right)
  \,,
$$

hence 

$$
  \label{BVOperatorDefiningRelation}
  \{-S',-\}_{\mathcal{T}}
  \;=\;
  \{-S',-\} + i \hbar \Delta_{BV}
  \,.
$$

=--


+-- {: .num_prop #ComponentsBVOperator}
###### Proposition
**([[BV-operator]] in components)**

If the [[field bundles]] of all [[field (physics)|fields]], [[ghost fields]] and [[auxiliary fields]] are [[trivial vector bundles]], with field/ghost-field/auxiliary-field coordinates collectively denoted $(\phi^A)$ then 
the [[BV-operator]] $\Delta_{BV}$ from prop. \ref{ForGaugeFixedFreeLagrangianFieldTheoryBVOperator} is given explicitly by

$$
  \Delta_{BV}
  \;=\;
  \underset{a}{\sum} (-1)^{deg(\Phi^A)}
  \underset{\Sigma}{\int} 
    \frac{\delta}{\delta \Phi^A(x)} 
    \frac{\delta}{\delta \Phi^{\ddagger}_A(y)}
  dvol_\Sigma
$$

=--

([Fredenhagen-Rejzner 11, (29)](#FredenhagenRejzner11), [Rejzner 11, (5.20)](#Rejzner11))

+-- {: .proof}
###### Proof

By prop. \ref{GaugeFixedActionFunctionalTimeOrderedAntibracket} we have equivalently

$$
  i \hbar \Delta_{BV}
  \;=\;
  \mathcal{T} \circ \{-S',-\} \circ \mathcal{T}^{-1}
  \,-\,
  \{-S',-\}
$$

and by [this example](A+first+idea+of+quantum+field+theory#BVDifferentialGlobal) the the second term on the right is

$$
  \begin{aligned}
    \left\{ -S', -\right\}
    & =
    \underset{\Sigma}{\int}
    j^{\infty}\left(\mathbf{\Phi}\right)^\ast
    \left(
      \frac{\overset{\leftarrow}{\delta}_{EL} L}{\delta \phi^a}
    \right)(x) 
    \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(x)} 
    \,
    dvol_\Sigma(x)
    \\
    & =
    \underset{a}{\sum}
      (-1)^{deg(\phi^a)}
    \underset{}{\int}
      (P\mathbf{\Phi})_a(x)
      \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(x)}
    \,
    dvol_\Sigma(x)
  \end{aligned}
$$

With this we compute as follows:

$$
  \label{AAA}
  \begin{aligned}
    \{-S',-\}_{\mathcal{T}}
    & =
    \mathcal{T} \circ \left\{ -S,-\right\} \circ \mathcal{T}^{-1}
    \\
    & = 
    \exp\left( 
     \left[
       \hbar \tfrac{1}{2} \Delta_F
       \left( 
         \frac{\delta}{\delta \mathbf{\Phi}}, 
         \frac{\delta}{\delta \mathbf{\Phi}}      
        \right)
        \,,\,
        -
      \right]
    \right)
    \left(
      \{-S',-\}
    \right)
    \\
    & = 
    \{-S',-\}
    +
    \left[
      \hbar \tfrac{1}{2}
      \Delta_F
      \left( 
        \frac{\delta}{\delta \mathbf{\Phi}}, 
        \frac{\delta}{\delta \mathbf{\Phi}}      
      \right)
      \,,
      \{-S',-\}
    \right]
    + \underset{ = 0 }{\underbrace{\hbar^2(...)}}
    \\
    & =
    \phantom{+}
    \left\{ -S' , -\right\}
    \\
    &
    \phantom{=}
    +
    \left[
      \tfrac{1}{2}\hbar 
      \underset{\Sigma \times \Sigma}{\int} 
      \Delta_F^{a b}(x,y)
      \frac{\delta^2}{\delta \mathbf{\Phi}^a(x) \delta \mathbf{\Phi}^b(y)}
      \, dvol_\Sigma(x)
      \, dvol_\Sigma(y)
      \;,\;
      \underset{a}{\sum}
      (-1)^{deg(\phi^a)}
      \underset{\Sigma}{\int}
        (P\mathbf{\Phi})_a(x)
        \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(x)}
      \,
      dvol_\Sigma(x)
    \right]
   \\
   & =
   \left\{ -S', -\right\}
   \\
   & \phantom{=}
   +
   \underset{a}{\sum} 
    (-1)^{deg(\phi^a)}
   \underset{\Sigma \times \Sigma}{\int} 
     \underset{ =  i \delta(x-y) }{\underbrace{P_x \Delta_F(x,y)}}
     \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
     \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(y)}
    \, dvol_\Sigma(x)
    \, dvol_\Sigma(y)
    \\
   & = \left\{ -S', -\right\} 
   + i \hbar 
   \underset{a}{\sum}
   (-1)^{deg(\phi^a)}
   \underset{\Sigma}{\int}
    \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
    \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(x)}
    \,
    dvol_\Sigma(x)
  \end{aligned}
$$

Here we used

1. under the first brace that by assumption of a [[free field theory]], $\{-S',-\}$ is linear in the fields, so that the first [[commutator]] with the [[Feynman propagator]] is independent of the fields, and hence all the higher commutators vanish;

1.  under the second brace that the [[Feynman propagator]] is $+i$ times the [[Green function]] for the [[Green hyperbolic differential equation|Green hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] ([this cor.](A+first+idea+of+quantum+field+theory#GreenFunctionFeynmanPropagator)).

=--

$\,$

**[[Schwinger-Dyson equation]]**
  {#SchwingerDysonEquation}

A special case of the general occurence of the [[BV-operator]] is the following important property of [[on-shell]] [[time-ordered products]]:

+-- {: .num_prop #DysonSchwinger}
###### Proposition
**([[Schwinger-Dyson equation]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$ (remark \ref{FieldBundleBVBRST}).

Let 

$$
  \label{SchwingerDysonTestObservable}
  A
  \;\coloneqq\;
  \underset{\Sigma}{\int}
    A^a(x) \cdot \mathbf{\Phi}^\ddagger_a(x)
  \, dvol_\Sigma(x)
  \;\in\;
  PolyObs_{reg}(E_{\text{BV-BRST}})
$$

be an [[off-shell]] [[regular polynomial observable]] which is [[linear map|linear]] in the [[antifield]] [[field observables]] $\mathbf{\Phi}^\ddagger$. Then 

$$
  \label{EquationSchwingerDyson}
  \mathcal{T}^{\pm 1}
  \left(
    \underset{\Sigma}{\int}
      \frac{\delta S'}{\delta \mathbf{\Phi}^a(x)}
      \cdot
      A^a(x)
      \, dvol_\Sigma(x)
  \right)
  \;=\;
  \pm i \hbar
  \,
  \mathcal{T}^{\pm}
  \left(
    \underset{\Sigma}{\int}
    \frac{\delta A^a(x)}{\delta \mathbf{\Phi}^a(x)}
    \,
    dvol_\Sigma(x)     
  \right)  
  \phantom{A}
  \in
  \underset{
    \text{on-shell}
  }{
  \underbrace{
    PolyObs_{reg}(E_{\text{BV-BRST}}, \mathbf{L'})
  }}
  \,.
$$

This is called the _[[Schwinger-Dyson equation]]_.

=--

The following proof is due to ([Rejzner 16, remark 7.7](#Rejzner16)) following the informal traditional argument ([Henneaux-Teitelboim 92, (15.108b)](#HenneauxTeitelboim92)).

+-- {: .proof}
###### Proof

Applying the inverse time-ordering map $\mathcal{T}^{-1}$ ([this prop.](time-ordered+product#IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise)) to equation (eq:BVOperatorDefiningRelation) applied to $A$ yields

$$
  \underset{
    \mathcal{T}^{-1}
    \underset{\Sigma}{\int}
      \frac{\delta S'}{\delta \mathbf{\Phi}^a(x)}
      \cdot
      A^a(x)
    dvol_\Sigma(x)
  }{
  \underbrace{
    \mathcal{T}^{-1}\left\{ -S', A\right\}
  }
  }
  \;=\;
  -
  \underset{
    i \hbar
    \mathcal{T}^{-1}
    \underset{\Sigma}{\int} 
      \frac{\delta A^a(x)}{\delta \mathbf{\Phi}^a(x)} 
    \, dvol_\Sigma
  }{
  \underbrace{
    i \hbar \mathcal{T}^{-1}\Delta_{BV}(A)
  }
  }
  +
  \underset{
    \{-S',\mathcal{T}^{-1}(A)\}
  }{
  \underbrace{
    \mathcal{T}^{-1}\left\{ -S',A\right\}_{\mathcal{T}}
  }
  }
$$

where we have identified the terms under the braces by 1) the component expression for the BV-differential $\{-S',-\}$ from [this prop](A+first+idea+of+quantum+field+theory#BVDifferentialGlobal), 2) prop. \ref{ComponentsBVOperator} and 3) prop. \ref{GaugeFixedActionFunctionalTimeOrderedAntibracket}.

The last term is manifestly in the [[image]] of the [[BV-differential]] $\{-S',-\}$ and hence vanishes when passing to [[on-shell]] observables along the [[isomorphism]] ([this equation](A+first+idea+of+quantum+field+theory#eq;OnShellPolynomialObservablesAsBVCohomology))

$$
  \underset{
    \text{on-shell}
  }{
  \underbrace{
    PolyObs(E_{\text{BV-BRST}}, \mathbf{L}')
  }}
  \;\simeq\;
  \underset{
    \text{off-shell}
  }{
  \underbrace{
    PolyObs(E_{\text{BV-BRST}})_{def(af = 0)}
  }}/im(\{-S',-\})
$$

(by [this example.](A+first+idea+of+quantum+field+theory#BVDifferentialGlobal)).

The same argument with the replacement $\mathcal{T} \leftrightarrow \mathcal{T}^{-1}$ throughout yields the other version of the equation (with time-ordering instead of reverse time ordering and the sign of the $\hbar$-term reversed).

=--

+-- {: .num_remark }
###### Remark
**("Schwinger-Dyson operator")**

The proof of the [[Schwinger-Dyson equation]] in prop. \ref{DysonSchwinger} shows that, up to [[time-ordered product|time-ordering]], the [[Schwinger-Dyson equation]] is the on-shell vanishing of the "quantized" [[BV-differential]] (eq:BVOperatorDefiningRelation)

$$
  \{-S',-\}_{\mathcal{T}}
  \;=\;
  \{-S', -\}
  \,+\,
  i \hbar \, \Delta_{BV}
  \,,
$$

where the [[BV-operator]] is the quantum correction of order $\hbar$. Therefore this is also called the _Schwinger-Dyson operator_ ([Henneaux-Teitelboim 92, (15.111)](#HenneauxTeitelboim92)).

=--

+-- {: .num_remark #SchwingerDysonDistributional}
###### Remark
**([[distribution|distributional]] [[Schwinger-Dyson equation]])**

Often the [[Schwinger-Dyson equation]] (prop. \ref{DysonSchwinger}) is displayed before spacetime-smearing of [[field observables]] in terms of [[operator products]] of [[operator-valued distributions]], taking the observable $A$ in (eq:SchwingerDysonTestObservable) to be

$$
  A^a(x) 
    \;\coloneqq\;
  \delta(x-x_0) \delta^a_{a_0} 
  \mathbf{\Phi}^{a_1}(x_1) \cdots \mathbf{\Phi}^{a_n}(x_n)
  \,.
$$

This choice makes (eq:EquationSchwingerDyson) become the [[distribution|distributional]] [[Schwinger-Dyson equation]]

$$
  \begin{aligned}
  & T
  \left(
    \frac{\delta S}{\delta \mathbf{\Phi}^{a_0}(x_0)}
      \cdot 
    \mathbf{\Phi}^{a_1}(x_1) \cdots \mathbf{\Phi}^{a_n}(x_n)
  \right)
  \\
  & 
  \underset{\text{on-shell}}{=}
  - i \hbar
  \underset{k}{\sum}
  T
  \left(
    \mathbf{\Phi}^{a_1}(x_1)
      \cdots
    \mathbf{\Phi}^{a_{k-1}}(x_{k-1})
      \cdot
    \delta(x_0 - x_k) \delta^{a_0}_{a_k}
      \cdot
    \mathbf{\Phi}^{a_{k+1}}(x_{k+1})
      \cdots
    \mathbf{\Phi}^{a_n}(x_m)
  \right)
  \end{aligned}
$$

(e.q. [Dermisek 09](Schwinger-Dyson+equation#Dermisek09)).

In particular this means that if $(x_0,a_0) \neq (x_k, a_k)$ for all $k \in \{1,\cdots ,n\}$ then

$$
  T
  \left(
    \frac{\delta S}{\delta \mathbf{\Phi}^{a_0}(x_0)}
      \cdot 
    \mathbf{\Phi}^{a_1}(x_1) \cdots \mathbf{\Phi}^{a_n}(x_n)
  \right)
  \;=\;
  0
  \phantom{AAA}
  \text{on-shell}
$$

Since by the [[principle of extremal action]] ([this prop.](A+first+idea+of+quantum+field+theory#PrincipleOfExtremalAction)) the equation 

$$
  \frac{\delta S}{\delta \mathbf{\Phi}^{a_0}(x_0)}
  \;=\;
  0
$$ 

is  the [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] (for the [[classical field theory]]) "at $x_0$", this may be interpreted as saying that the classical equations of motion for fields at $x_0$ still hold for [[time-ordered product|time-ordered]] [[quantum theory|quantum]] [[expectation values]], as long as all other observables are evaluated away from $x_0$; while if observables do coincide at $x_0$ then there is a correction measured by the [[BV-operator]].

=--

$\,$

This concludes our discussion of the [[algebra of quantum observables]] for [[free field theories]]. In the [next chapter](#Scattering) we introduce the [[perturbative quantum field theory|perturbative]] [[interaction]] in terms of the [[scattering matrix]]. This leads over to the discussion of the genuine perturbative [[algebra of quantum observables]] in the chapter _[Quantum observables](#QuantumObservables)_.


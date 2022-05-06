
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

The concept of _BV-operator_ has two different but (somewhat subtly) related meanings:

1. In [[perturbative quantum field theory]] (discussed [below](#InPerturbativeQuantumFieldTheory)) the _BV-operator_ or _BV-Laplacian_ ([Batalin-Vilkovisky 81](#BatalinVilkovisky81)) is essentially the difference between the action of the [[BV differential]] on the [[algebra of observables]] before and after [[quantization]] of the [[free field theory]] around which the [[perturbative quantum field theory|perturbative quantization]] is considered; it is a quantum correction $i \hbar \Delta_{BV}$ (of order of [[Planck's constant]] $\hbar$) to the [[BV differential]] $s_{BV} = \{-S',-.\}$. Where the condition $\left(\{-S',-\}\right)^2 = 0$ for the [[BV-differential]] to be a [[differential]] is called the "[[master equation]]" in [[BV-BRST theory]], the quantum corrected version $\left( \{-S',-\} + i \hbar \Delta\right)^2 = 0$ is called the _[[quantum master equation]]_.


1. In [[higher algebra]], under the identification of a [[BV-algebra]] with the [[chain homology]] of a [[little k-cubes operad|E2-algebra]], the _BV-operator_ corresponds to the operation of rotating a little disk around.

For the relation between the two see _[[relation between BV and BD]]_.

## In perturbative quantum field theory
 {#InPerturbativeQuantumFieldTheory}

In [[perturbative quantum field theory]] the BV-operator $i \hbar \Delta$ may be understood intuitively as reflecting the contribution of the [[Gaussian measure]] in the [[path integral]] of the [[free field theory]] around which the perturbative quantization takes place. This intuition may be made precise for finite-dimensional toy path integrals. This we discuss in:

* _[In finite-dimensional toy path integrals](#ForFiniteDimensionalToyPathIntegrals)_

In the rigorous construction of [[relativistic field theory|relativistic]] [[perturbative quantum field theory]] via [[causal perturbation theory]]/[[perturbative AQFT]] there is a rigorous incarnation of the BV-operator ([Fredenhagen-Rejzner 11b, section 2](#FredenhagenRejzner11b), [Rejzner 11, section 5.1.2](#Rejzner11)): The would-be path integral is reflected in the [[perturbative S-matrix]], hence in the [[time ordered products]], and the BV-operator on [[regular polynomial observables]] is the difference between the classical [[BV-differential]] and its [[conjugation]] into the [[time-ordered products]] (def. \ref{ForGaugeFixedFreeLagrangianFieldTheoryBVOperator} below). This we discuss in

* _[In causal perturbation theory](#InCausalPerturbationTheory)_


### For finite-dimensional toy path integrals
 {#ForFiniteDimensionalToyPathIntegrals}

If $X$ is a [[finite number|finite]] [[dimension|dimensional]] [[closed manifold|closed]] [[orientation|oriented]] [[smooth manifold]], then [[integration of differential forms]] of top degree over $X$ may be identified with sending such differential forms to their [[image]] in the [[de Rham cohomology]] of $X$.

This may be slightly reformulated: Fixing a [[volume form]] $\mu$ on $X$ it induces by contraction with [[vector fields]] degreewise a [[linear isomorphism]] 

$$
  \mu \;\colon\;
  \Gamma_X(\wedge^n T^\ast X)
   \overset{\simeq}{\longrightarrow}
  \Gamma_X(\wedge^{dim(X)-n} T X)
$$

between the spaces of [[differential n-forms]] on $X$ and the space of [[multivector fields]] on $X$ of degree $n-dim(X)$. Under this isomorphism the [[de Rham differential]] induces a differential on [[multivector fields]]:

$$
  \Delta_{BV}
  \;\coloneqq\;
  \mu \circ d_{dR} \circ \mu^{-1}
$$

This $\Delta_{BV}$ is the _BV-operator_ in this simple situation. 

The above statement about [[integration]] now translates into saying that for $f$ any [[smooth function]] on $X$, then its [[integration of differential forms]] $\int f \mu$ may be identified with the [[image]] of $f$ in the [[chain homology]] of the BV-operator $\Delta_{BV}$.

If one thinks of $X$ as a space of [[field configurations]] and of  $f = \exp(i \hbar S)$ as an exponentiated [[action functional]], the one may think of this integral $\int \exp(i \hbar S) \mu$ as the finite-dimensional toy version of a [[path integral]]. 

While this is in general not defined in the actual non-finite dimensional situations in [[field theory]], the above re-formulation in terms of the [[chain homology]] of a BV-operator does make sense whenever an appropriate kind of differential is given. One may then try to axiomatize which chain complexes qualify as BV-complex and try to interpret their chain homology as computing perturbative [[path integrals]].

For more on this perspective see at _[[BV-BRST formalism]]_ the section _[Quantum BV as homological (path-)integration](BV-BRST+formalism#HomologicalIntegration)_
 
### In causal perturbation theory
  {#InCausalPerturbationTheory}

For more context for the following see at _[[A first idea of quantum field theory]]_ the chapter _[Free quantum fields](A+first+idea+of+quantum+field+theory#FreeQuantumFields)_.

#### Background

Recall the following context

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] admitting a [[gauge fixing]], and let $\mathbf{L}' - \mathbf{L}'_{BRST}$ be its BV-BRST [[Lagrangian density]] after [[gauge fixing]] ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)), so that the gauge-fixed [[local BRST complex|local BV-BRST differential]] is given by the [[local antibracket]] as

$$
  s' 
    \;=\;
  \left\{ -\mathbf{L}' + \mathbf{L}'_{BRST}, - \right\}
$$

The corresponding global BV-BRST differential on [[regular polynomial observables]] is ([this def.](A+first+idea+of+quantum+field+theory#ComplexBVBRSTGlobal))

$$
  \label{GaugeFixedGlobalBVBRSTDifferentialRecalled}
  \left\{ -S' + S'_{BRST} \;,\; -\right\}
  \;\coloneqq\;
  \left\{ -\tau_\Sigma\mathbf{L}'(x) + \tau_\Sigma\mathbf{L}'_{BRST}(x), - \right\} 
  \;\colon\;
  PolyObs(E)_{reg} \longrightarrow PolyObs(E)_{reg}
  \,.
$$

By definition of [[gauge fixing]] ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)), the [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] for $\mathbf{L}'$ are [[Green hyperbolic differential equations|Green hyperbolic]] and hence have a [[causal propagator]] $\Deta = \Delta_+ - \Delta_-$ and admit a compatible _[[Wightman propagator]]_ $\Delta_H = \tfrac{i}{2}(\Delta_+ - \Delta_-) + H$ and the corresponding [[Feynman propagator]] $\Delta_F \coloneqq \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$.  The [[star products]] with respect to these ([this def.](star+product#PropagatorStarProduct)) on [[regular polynomial observables]] 

$$
  \star_H, \star_F
  \;\colon\;
  PolyObs(E)_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E)_{reg}[ [\hbar] ]
$$

are, respectively, the [[Wick algebra]] product ([[operator product]], see [this def.](Wick+algebra#NormalOrderedProductNotation))

$$
  A_1 A_2
  \;\coloneqq\;
  A_1 \star_H A_2 
  \;\coloneqq\;
  ((-) \cdot (-))
  \circ
  \exp\left(
    \hbar 
    \underset{\Sigma \times \Sigma}{\int}
      \Delta_{H}(x,y)^{a b} 
      \frac{\delta}{\delta \mathbf{\Phi}^a(x)} 
        \otimes 
      \frac{\delta}{\delta \mathbf{\Phi}^b(y)}
      \, dvol_\Sigma(x) \, dvol_\Sigma(y)
  \right)
  (A_1 \otimes A_2)
$$

and the [[time-ordered product]] (see again [this def.](Wick+algebra#NormalOrderedProductNotation))

$$
  T(A_1 A_2)
  \;\coloneqq\;
  A_1 \star_F A_2 
  \;\coloneqq\;
  ((-) \cdot (-))
  \circ
  \exp\left(
    \hbar 
    \underset{\Sigma \times \Sigma}{\int}
      \Delta_{F}(x,y)^{a b} 
      \frac{\delta}{\delta \mathbf{\Phi}^a(x)} 
        \otimes 
      \frac{\delta}{\delta \mathbf{\Phi}^b(y)}
      \, dvol_\Sigma(x)\, dvol_\Sigma(y)
  \right)
  (A_1 \otimes A_2)
  \,,
$$

Since the [[Feynman propagator]] is symmetric ([this prop.](A+first+idea+of+quantum+field+theory#SymmetricFeynmanPropagator)), the latter [[time ordered product]] on [[regular polynomial observables]] is [[isomorphism|isomorphic]] (via [this prop.](star+product#SymmetricContribution)) to the pointwise product, via

$$
  \label{RecallIsomorphsimTimeOrdering}
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

as 

$$
  A_1 \star_{F} A_2
  \;=\;
  \mathcal{T}( \mathcal{T}^{-1}A_1 \cdot \mathcal{T}^{-1}A_2 )
$$

([this prop.](time-ordered+product#IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise)).

#### The BV-Operator
 {#BVOperatorInCausalPerturbationTheory}

+-- {: .num_defn #AntibracketTimeOrdered}
###### Definition
**([[time-ordered product|time-ordered]] [[antibracket]])


Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$.

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

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$.

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

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$ and with corresponding gauge-fixed global [[BV-BRST differential]] on graded [[regular polynomial observables]]

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

on [[regular polynomial observables]] is, up to a factor of $i \hbar$, the difference between the free component $\{-S',-\}$ of the gauge fixed global BV differential and its time-ordered version (def. \ref{AntibracketTimeOrdered})

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

Since this formula exhibits a graded [[Laplace operator]], the BV-operator is also called the _BV-Laplace operator_ or _BV-Laplacian_, for short.

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

and by [this example](A+first+idea+of+quantum+field+theory#BVDifferentialGlobal) the second term on the right is

$$
  \begin{aligned}
    \left\{ -S', -\right\}
    & =
    \underset{\Sigma}{\int}
    j^{\infty}\left(\mathbf{\Phi}\right)^\ast
    \left(
      \frac{\overset{\leftarrow}{\delta}_{EL} L}{\delta \phi^A}
    \right)(x) 
    \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_A(x)} 
    \,
    dvol_\Sigma(x)
    \\
    & =
    \underset{a}{\sum}
      (-1)^{deg(\phi^A)}
    \underset{}{\int}
      (P\mathbf{\Phi})_A(x)
      \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_A(x)}
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
      \Delta_F^{A B}(x,y)
      \frac{\delta^2}{\delta \mathbf{\Phi}^A(x) \delta \mathbf{\Phi}^B(y)}
      \, dvol_\Sigma(x)
      \, dvol_\Sigma(y)
      \;,\;
      \underset{a}{\sum}
      (-1)^{deg(\phi^A)}
      \underset{\Sigma}{\int}
        (P\mathbf{\Phi})_A(x)
        \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_A(x)}
      \,
      dvol_\Sigma(x)
    \right]
   \\
   & =
   \left\{ -S', -\right\}
   \\
   & \phantom{=}
   +
   \underset{A}{\sum} 
    (-1)^{deg(\phi^A)}
   \underset{\Sigma \times \Sigma}{\int} 
     \underset{ =  i \delta(x-y) }{\underbrace{P_x \Delta_F(x,y)}}
     \frac{\delta}{\delta \mathbf{\Phi}^A(x)}
     \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_A(y)}
    \, dvol_\Sigma(x)
    \, dvol_\Sigma(y)
    \\
   & = \left\{ -S', -\right\} 
   + i \hbar 
   \underset{A}{\sum}
   (-1)^{deg(\phi^A)}
   \underset{\Sigma}{\int}
    \frac{\delta}{\delta \mathbf{\Phi}^A(x)}
    \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_A(x)}
    \,
    dvol_\Sigma(x)
  \end{aligned}
$$

Here we used

1. under the first brace that by assumption of a [[free field theory]], $\{-S',-\}$ is linear in the fields, so that the first [[commutator]] with the [[Feynman propagator]] is independent of the fields, and hence all the higher commutators vanish;

1.  under the second brace that the [[Feynman propagator]] is $+i$ times the [[Green function]] for the [[Green hyperbolic differential equation|Green hyperbolic]] [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] ([this cor.](A+first+idea+of+quantum+field+theory#GreenFunctionFeynmanPropagator)).

=--

#### Relation to time-ordered antibracket
 {#InCausalPerturbationTheoryRelationToTimeOrderedAntibracket}

+-- {: .num_prop #AntibracketBVOperatorRelation}
###### Proposition
**(global [[antibracket]] exhibits failure of [[BV-operator]] to be a [[derivation]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$

The [[BV-operator]] $\Delta_{BV}$ (def. \ref{ForGaugeFixedFreeLagrangianFieldTheoryBVOperator}) and the global [[antibracket]] $\{-,-\}$ ([this def.](A+first+idea+of+quantum+field+theory#ComplexBVBRSTGlobal)) satisfy for all [[polynomial observables]] ([this def.](A+first+idea+of+quantum+field+theory#PolynomialObservables)) $A_1, A_2 \in PolyObs(E_{\text{BV-BRST}})[ [\hbar] ]$ the relation 

$$
  \label{GlobalAntibracketInteractingWithBVOperator}
  \{A_1, A_2\}
  \;=\;
  (-1)^{deg(A_2)}
  \,
  \Delta_{BV}(A_1 \cdot A_2)
  - 
  (-1)^{deg(A_2)}
  \,
  \Delta_{BV}(A_1) \cdot A_2
  -
  A_1 \cdot \Delta_{BV}(A_2)  
$$

for $(-) \cdot (-)$ the pointwise product of observables (def. \ref{Observable}). 

Moreover, it commutes on [[regular polynomial observables]] with the [[time-ordered product|time-ordering operator]] $\mathcal{T}$ ([this prop.](time-ordered+product#IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise))

$$
  \Delta_{BV} \circ \mathcal{T}
  =
  \mathcal{T} \circ \Delta_{BV}
  \phantom{AAA}
  \text{on}
  \,\,
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$

and hence satisfies the analogue of relation (eq:GlobalAntibracketInteractingWithBVOperator) also for the time-ordered antibracket $\{-,-\}_{\mathcal{T}}$ (def. \ref{AntibracketTimeOrdered}) and the [[time-ordered product]] $\star_F$ on regular polynomial observables

$$
  \{A_1, A_2\}_{\mathcal{T}}
  \;=\;
  (-1)^{deg(A_2)}
  \,
  \Delta_{BV}(A_1 \star_F A_2)
  - 
  (-1)^{deg(A_2)}
  \Delta_{BV}(A_1) \star_F A_2
  -
  A_1 \star_F \Delta_{BV}(A_2)  
  \,.
$$

=--

(e.g. [Henneaux-Teitelboim 92, (15.105d)](antibracket#HenneauxTeitelboim92))

+-- {: .proof}
###### Proof

With prop. \ref{ComponentsBVOperator} the first statement is a graded version of the analogous relation for an ordinary [[Laplace operator]] $\Delta \coloneqq g^{a b} \partial_a \partial_b$ acting on [[smooth functions]] on [[Cartesian space]], which on [[smooth functions]] $f,g$ satisfies

$$
  \Delta(f \cdot g)
  \;=\;
  (\nabla f, \nabla g) - \Delta(f) g - f \Delta(g)
  \,,
$$

by the [[product law]] for [[differentiation]], where now $\nabla f \coloneqq (g^{a b} \partial_b f)$ is the [[gradient]] and $(v,w) \coloneqq g_{a b} v^a w b$ the [[inner product]]. Here one just needs to carefully record the relative signs that appear.

That the BV-operator commutes with the time-ordering operator is clear from the fact that both of these are given by [[partial derivative|partial]] [[functional derivatives]] with _[[constant function|constant]]_ [[coefficients]]. This immediately implies the last statement from the first.

=--

+-- {: .num_example #TimeOrderedExponentialBVOperator}
###### Example
**([[BV-operator]] on [[time-ordered product|time-ordered]] [[exponentials]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$.

Let moreover $V \in PolyObs(E_{\text{BV-BRST}})_{reg, deg = 0}[ [\hbar] ]$  be a [[regular polynomial observable]] (def. \ref{PolynomialObservables}) of degree zero. Then the application of the [[BV-operator]] $\Delta_{BV}$ (def. \ref{ForGaugeFixedFreeLagrangianFieldTheoryBVOperator}) to the [[time-ordered product|time-ordered]] [[exponential]] $\exp_{\mathcal{T}}(V)$ ([this example](time-ordered+product#RegularObservablesExponentialTimeOrdered)) is the [[time-ordered product]] of the time-ordered exponential with the sum of $\Delta_{BV}(V)$ and the global [[time-ordered product|time-ordered]] [[antibracket]] $\tfrac{1}{2}\{V,V\}_{\mathcal{T}}$ (def. \ref{AntibracketTimeOrdered}) of $V$ with itself:

$$
  \Delta_{BV}
  \left(
    \exp_{\mathcal{T}}(V)
  \right)
  \;=\;
  \left(
    \Delta_{BV}(V)
    +
    \tfrac{1}{2}\{V,V\}_{\mathcal{T}}
  \right)
   \star_F
  \exp_{\mathcal{T}}(V)
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{AntibracketBVOperatorRelation} $\Delta_{BV}$ acts as a [[derivation]] on the [[time-ordered product]] up to a correction given by the antibracket of the two factors. This yields the result by the usual combinatorics of [[exponentials]].

$$
  \begin{aligned}
    \Delta_{BV}
    \left(
      1 + V + \tfrac{1}{2}V \star_F V + \cdots
    \right)
    & =
    \Delta_{BV}(V) 
      + 
    \tfrac{1}{2}\left( \Delta_{BV}(V) \star_F V + V \star_F \Delta_{BV}(V) \right)
      +
    \tfrac{1}{2}\{V,V\}_{\mathcal{T}}
      +
    \cdots
    \\
    & = 
    \Delta_{BV}(V) +  \Delta_{BV}(V) \star_F V + \tfrac{1}{2}\{V,V\}_{\mathcal{T}}
    + \cdots
  \end{aligned}
$$ 

=--

#### Schwinger-Dyson equation
  {#SchwingerDysonEquation}

A special case of the general occurence of the [[BV-operator]] is the following important property of [[on-shell]] [[time-ordered products]]:

+-- {: .num_prop #DysonSchwinger}
###### Proposition
**([[Schwinger-Dyson equation]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] ([this def.](A+first+idea+of+quantum+field+theory#FreeFieldTheory)) with [[gauge fixing|gauge fixed]] BV-BRST [[Lagrangian density]] $-\mathbf{L}' + \mathbf{L}'_{BRST}$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) on a graded BV-BRST [[field bundle]] $E_{\text{BV-BRST}} \coloneqq T^\ast[-1]_{\Sigma,inf}(E \times_\Sigma \mathcal{G}[1] \times_{\Sigma} A \times_\Sigma A[-1])$.

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

The proof below is due to ([Rejzner 16, remark 7.7](#Rejzner16)), following the informal traditional argument ([Henneaux-Teitelboim 92, (15.108b)](#HenneauxTeitelboim92)).

+-- {: .proof}
###### Proof

Applying the inverse time-ordering map $\mathcal{T}^{-1}$ ([this prop.](time-ordered+product#IsomorphismOnRegularPolynomialObservablesTimeOrderedandPointwise)) to equation (eq:BVOperatorDefiningRelation) applied to $A$ yields

$$
  \label{BVDerivationOfSchwingerDyson}
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
  \label{OnShellObservablesAsQuotientOfOffShellObservablesRecalled}
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

+-- {: .num_remark #FreeFieldQuantumShell}
###### Remark
**(the "quantum shell")**

Beware that, superficially, it might seem that in equation (eq:BVDerivationOfSchwingerDyson) not only the term $\{-S',\mathcal{T}^{-1}(A)\}$ on the right vanishes [[on-shell]], but also the term $\mathcal{T}^{-1}\left\{ -S', A\right\}$ on the left, since the latter is the image under the linear map $\mathcal{T}^{-1}$ of an observable that vanishes on-shell.

To sort this out, notice that the isomorphism (eq:OnShellObservablesAsQuotientOfOffShellObservablesRecalled) tells us that the observables that vanish when passing from off-shell to on-shell observables are precisely those in the ideal generated by the image of $\{-S',(-)\}$. 
But while $\mathcal{T}^{-1}$ is an isomorphism on (regular off-shell observables), it need not (and in general does not) preserve this ideal! Hence $\mathcal{T}^{-1}(\{-S',A\})$ need not (and in general is not) an element of that ideal, and this is why it remains when passing to the algebra of on-shell observables and thus makes its crucial appearance in the [[Schwinger-Dyson equation]].


=--


#### Quantum master equation

Passing from [[free field theory]] to [[perturbative quantum field theory|perturbative]] [[quantization]] of [[interacting field theory]], the above BV-operator of the underying free field theory appears as a quantum correction to the "[[classical master equation]]" which expresses the nilpotency of the [[BV-differential]]. This "master equation" corrected by the BV-operator is called the _[[quantum master equation]]_. See [this prop.](quantum+master+equation#QuantumMasterEquation).


## References

The concept originates with

* {#BatalinVilkovisky81} [[Igor Batalin]], [[Grigori Vilkovisky]],  _Gauge Algebra and Quantization_, Phys. Lett. B 102 (1): 27&#8211;31, 1981 (<a href="https://doi.org/10.1016/0370-2693(81)90205-7">doi:10.1016/0370-2693(81)90205-7</a>) 

Traditional review includes

* {#HenneauxTeitelboim92} [[Marc Henneaux]], [[Claudio Teitelboim]], section 15.5.3  of _[[Quantization of Gauge Systems]]_, Princeton University Press, 1992

The understanding of the BV-operator in the rigorous formulation of [[relativistic field theory|relativistic]] [[perturbative quantum field theory]] via [[causal perturbation theory]]/[[perturbative AQFT]] is due to 

* {#FredenhagenRejzner11b} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], section 2 of _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. (2013) 317: 697 ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232), [doi:10.1007/s00220-012-1601-1](https://doi.org/10.1007/s00220-012-1601-1))

* {#Rejzner11} [[Katarzyna Rejzner]], section 5.1.2 of _Batalin-Vilkovisky formalism in locally covariant field theory_ ([arXiv:1111.5130](https://arxiv.org/abs/1111.5130))

surveyed in

* {#Rejzner16} [[Katarzyna Rejzner]], section 7.3 of _[[Perturbative Algebraic Quantum Field Theory]]_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))

See at _[[BV-formalism]]_ for more references.


[[!redirects BV-operators]]

[[!redirects BV-Laplacian]]
[[!redirects BV-Laplacians]]

[[!redirects BV-Laplace operator]]
[[!redirects BV-Laplace operators]]

[[!redirects Schwinger-Dyson operator]]
[[!redirects Schwinger-Dyson operators]]


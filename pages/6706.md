

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

In [[perturbative quantum field theory]] formulated in terms of [[BV-BRST formalism]], the _classical master equation_ expresses the nilpotency of the [[BV-differential]] before [[quantization]], with the latter regarded as a [[Hamiltonian vector field]] with respect to the _[[antibracket]]_ $\{-,-\}$, for "Hamiltonian" the BV-BRST-extended [[action functional]] "$S + S_{BRST}$":

$$
  \left( 
    s_{BV}
  \right)^2 = 0
  \phantom{AA}
  \Leftrightarrow
  \phantom{AA}
  \left( \{S + S_{BRST},(-)\}\right)^2 = 0
  \phantom{AA}
  \Leftrightarrow
  \phantom{AA}
  \{S + S_{BRST}, S + S_{BRST}\} = 0
  \,.
$$

The _quantum  master equation_ (prop. \ref{QuantumMasterEquation} below) is the version of this equation after [[quantization]], in which case the the [[BV-differential]] picks up a quantum correction of order $\hbar$ ([[Planck's constant]]) by the [[BV-operator]] $\Delta_{BV}$:

$$
  \left(\, \{S + S_{BRST},(-)\} + i \hbar \Delta_{BV} \, \right)^2 = 0
 \,.
$$


## In causal perturbation theory

We discuss the quantum master equation in the rigorous formulation of [[relativistic field theory|relativistic]] [[perturbative quantum field theory]] via [[causal perturbation theory]]/[[perturbative AQFT]] ([Fredenhagen-Rejzner 11b](#FredenhagenRejzner11b), [Rejzner 11](#Rejzner11)).


First we consider all structure just on [[regular polynomial observables]], hence excluding non-linear [[local observables]] such as the usual point-[[interaction]] [[action functionals]]. 

Then the [[extension]] of all structures from regular to [[local observables]] is the [[renormalization]] step, discussed [furthter below](#RenormalizationAndMasterWardIdentity).

### Background

Throughout, let $(E_{\text{BV-BST}},\mathbf{L}')$ be a [[gauge fixing|gauge fixed]] [[free field theory|free]] [[Lagrangian field theory]] with global [[BV-differential]] ([this def.](A+first+idea+of+quantum+field+theory#ComplexBVBRSTGlobal))

$$
  \{-S', -\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ] 
$$

Hence $S'$ denotes the gauge fixed free action functional.

Moreover, let $\Delta_H$ be a compatible choice of [[Wightman propagator]] with associated [[Feynman propagator]] $\Delta_F$. 

+-- {: .num_lemma #DerivationBVDifferentialForWickAlgebra}
###### Lemma
**(global [[BV-differential]] is [[derivation]] on [[Wick algebra]])**

The global [[BV-differential]] 

$$
  \{-S',-\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
   \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$

is a [[derivation]] also with respect to the [[Wick algebra]] [[star product]] $\star_H$:

$$
  \left\{
    -S', A_1 \star_H A_2
  \right\}
  \;=\;
  \left\{
    -S', A_1
  \right\}
    \star_H
  A_2
    \;+\;
  A_1
    \star_H
  \left\{
   -S', A_2
  \right\}
  \,.
$$

=--

([Fredenhagen-Rejzner 11b, below (37)](#FredenhagenRejzner11b), [Rejzner 11, below (5.28)](#Rejzner11)) For **proof** see [this prop](A+first+idea+of+quantum+field+theory#OnMicrocausalObservablesGlobalBVDifferential)



+-- {: .num_defn #OnRegularObservablesPerturbativeSMatrix}
###### Definition
**([[perturbative S-matrix]] on [[regular polynomial observables]])**

The _[[perturbative S-matrix]]_ on [[regular polynomial observables]]
is the [[exponential]] with respect to the [[time-ordered product]]

$$
  \mathcal{S} 
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))
$$

given by

$$
  \mathcal{S}(S_{int})
  =
  \exp_{\star_F}
  \left(
    \tfrac{1}{i \hbar} S_{int})
  \right)
  \coloneqq
  1 
    + 
  \tfrac{1}{\i \hbar} S_{int} 
    +
  \tfrac{1}{2}
  \tfrac{1}{(i \hbar)^2} 
  S_{int} \star_F S_{int}
  + 
  \cdots
  \,.
$$

We think of $S_{int}$ here as an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]].

We write $\mathcal{S}(S_{int})^{-1}$ for the [[inverse]] with respect to the [[Wick algebra|Wick product]] (which exists by [this remark](S-matrix#PerturbativeSMatrixInverse))

$$
  \mathcal{S}(S_{int})^{-1} \star_H \mathcal{S}(S_{int})
  = 
  1
  \,.
$$

Notice that this is in general different form the inverse with respect to the [[time-ordered product]] $\star_F$, which is $\mathcal{S}(-S_{int})$:

$$
  \mathcal{S}(-S_{int}) 
    \star_F
  \mathcal{S}(S_{int})
  =
  1
  \,. 
$$

=--


+-- {: .num_defn #MollerOperatorOnRegularPolynomialObservables}
###### Definition
**([[quantum Møller operator]] on [[regular polynomial observables]])**

Given an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]] in the form of a [[regular polynomial observable]] of degree 0

$$
  S_{int} 
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{{reg} \atop {deg = 0}}[ [\hbar] ]
$$

then the corresponding _[[quantum Møller operator]]_ on [[regular polynomial observables]]

$$
  \mathcal{R}^{-1}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$

is given by the [[derivative]] of [[Bogoliubov's formula]]

$$
  \mathcal{R}^{-1}
    \;\coloneqq\;
  \mathcal{S}(S_{int})^{-1} 
    \star_H 
  (\mathcal{S}(S_{int}) \star_F (-))
  \,,
$$

where $\mathcal{S}(S_{int}) = \exp_{\mathcal{T}}\left( \tfrac{-1}{i \hbar} S_{int} \right)$ is the [[perturbative S-matrix]] from  def. \ref{OnRegularObservablesPerturbativeSMatrix}.

This indeed lands in [[formal power series]] in [[Planck's constant]] $\hbar$ (by [this remark](Bogoliubov's+formula#PowersInPlancksConstant)),  instead of in more general [[Laurent series]] as the [[perturbative S-matrix]] does (def. \ref{OnRegularObservablesPerturbativeSMatrix}).

Hence the inverse map is

$$
  \mathcal{R}
   \;=\;
  \mathcal{S}(-S_{int}) \star_F ( \mathcal{S}(S_{int}) \star(-) )
  \,.
$$

=--

([Bogoliubov-Shirkov 59](Bogoliubov's+formula#BogoliubovShirkov59); the above terminology follows [Hawkins-Rejzner 16, below def. 5.1](Møller+operator#HawkinsRejzner16))

Notice that compared to Fredenhagen-Rejzner et. al. we have changed notation conventions $\mathcal{R} \leftrightarrow \mathcal{R}^{-1}$ in order to bring out the analogy to (the conventions for the) [[time-ordered product]]  $A_1 \star_F A_2 = \mathcal{T}(\mathcal{T}^{-1}(A_1) \cdot \mathcal{T}^{-1}(A_2))$ on regular polynomial observables.


notice the implicit dependencies

| [[endomorphism]] of <br/> [[regular polynomial observables]] | meaning | depends on choice of |
|--------|---------|----------------------|
| $\phantom{AA}\mathcal{T}$ | [[time-ordered product|time-ordering]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] |
| $\phantom{AA}\mathcal{S}$ | [[S-matrix]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] |
| $\phantom{AA}\mathcal{R}$ | [[quantum Møller operator]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] and [[interaction]] |



+-- {: .num_defn #FieldAlgebraObservablesInteracting}
###### Definition
**([[interacting field algebra]])**

Given an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]] in the form of a [[regular polynomial observable]] in degree 0

$$
  S_{int}
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{{reg} \atop {deg = 0}}[ [\hbar] ]
  \,,
$$

then the _[[interacting field algebra]]_ [[structure]] on [[regular polynomial observables]]

$$
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ] 
    \otimes 
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ] 
    \overset{ \star_{int} }{\longrightarrow}
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ] 
$$

is the [[conjugation]] of the [[Wick algebra]]-[[structure]] by the [[quantum Møller operator]] (def. \ref{MollerOperatorOnRegularPolynomialObservables}):

$$
  A_1 \star_{int} A_2
  \;\coloneqq\;
  \mathcal{R}
  \left(
    \mathcal{R}^{-1}(A_1) 
     \star_H 
    \mathcal{R}^{-1}(A_2)
  \right)
$$

=--

(e.g. [Fredenhagen-Rejzner 11b, (19)](#FredenhagenRejzner11b))



### Interacting quantum BV-differential

Recall how the global BV-differential 

$$
  \{S',-\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
$$ 

on [[regular polynomial observables]] ([this def.](A+first+idea+of+quantum+field+theory#BVDifferentialGlobal)) is conjugated into the [[time-ordered product]] via the time ordering operator
$\mathcal{T} \circ \{-S',-\} \circ \mathcal{T}^{-}$ ([this prop.](BV-operator#GaugeFixedActionFunctionalTimeOrderedAntibracket)).

In the same way we may use the [[quantum Møller operators]] to conjugate the BV-differential into the regular part of the [[interacting field algebra of observables]]:

+-- {: .num_defn #BVDifferentialInteractingQuantum}
###### Definition
**(interacting quantum [[BV-differential]])**

Given an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]] in the form of a [[regular polynomial observable]] $S_{int}$,
then the _interacting quantum BV-differential_ on the [[interacting field algebra]] (def. \ref{FieldAlgebraObservablesInteracting})
on [[regular polynomial observables]] is the [[conjugation]] of the plain [[BV-differential]] $\{-S',-\}$ by the [[quantum Møller operator]] induced by $S_{int}$ (def. \ref{MollerOperatorOnRegularPolynomialObservables}):

$$
  \mathcal{R} \circ \{-S', (-)\} \circ \mathcal{R}^{-1}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
  \,.
$$

=--

([Rejzner 11, (5.38)](#Rejzner11))


+-- {: .num_prop #QuantumMasterEquation}
###### Proposition
**([[quantum master equation]] and [[quantum master Ward identity]] on [[regular polynomial observables]])**

Consider an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]] in the form of a [[regular polynomial observable]] in degree 0

$$
  S_{int} 
  \;\in\;
  PolyObs(E_{\text{BV-BRST}})_{{reg} \atop {deg = 0}}[ [\hbar] ]
  \,,
$$

Then the following are equivalent:

1. The _[[quantum master equation]]_ (QME)

   $$
     \label{OnRegularObservablesQuantumMasterEquation}
      \tfrac{1}{2} \{ S' + S_{int}, S' + S_{int} \}_{\mathcal{T}}
      +
      i \hbar  \Delta_{BV}( S' + S_{int} )
     \;=\;
     0
     \,.
   $$


1. The  [[perturbative S-matrix]] (def. \ref{OnRegularObservablesPerturbativeSMatrix}) is $BV$-closed 

   $$
     \{-S', \mathcal{S}(S_{int})\} = 0
     \,.
   $$

1. The quantum _[[master Ward identity]]_ (MWI) on [[regular polynomial observables]] _in terms of [[retarded products]]_:

   $$
     \label{OnRegularObservablesQuantumMasterWardIdentity}
     \mathcal{R} \circ \{-S',(-)\} \circ \mathcal{R}^{-1}   
     \;=\;
     \left\{ -(S' + S_{int}) \,,\, (-) \right\}_{\mathcal{T}} 
     - 
     i \hbar   \Delta_{BV}
   $$

   ([Dütsch 18, (4.2)](Ward+identity#Duetsch18))

   expressing the interacting quantum [[BV-differential]] (def. \ref{BVDifferentialInteractingQuantum}) as the sum of the [[time-ordered product|time-ordered]] [[antibracket]] ([this def.](BV-operator#AntibracketTimeOrdered)) with the _total_ [[action functional]] $S' + S_{int}$ and $i \hbar$ times the [[BV-operator]] ([BV-operator](BV-operator#ForGaugeFixedFreeLagrangianFieldTheoryBVOperator)).

1. The quantum _[[master Ward identity]]_ (MWI) on [[regular polynomial observables]] _in terms of [[time-ordered products]]_:

   $$
     \label{OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered}
     \mathcal{S}(-S_{int}) 
       \star_F 
     \{-S', \mathcal{S}(S_{int}) \star_F  (-)\}
     \;=\;
     -
     \left(
       \left\{ S' + S_{int} \,,\, (-) \right\}_{\mathcal{T}} 
       + i \hbar   \Delta_{BV}
     \right)
   $$

   ([Dütsch 18, (4.8)](Ward+identity#Duetsch18))

=--

([Rejzner 11, (5.35) - (5.38)](#Rejzner11), following [Hollands 07, (342)-(345)](Ward+identity#Hollands07))


+-- {: .proof}
###### Proof

To see that the first two conditions are equivalent, we compute as follows

$$
  \label{QuantumMasterOnRegularObservablesBVDifferentialOfSMatrixInTerms}
  \begin{aligned}
    \left\{
      -S',  \mathcal{S}(S_{int})
    \right\}
    & =
    \left\{
      -S'
      , 
      \exp_{\mathcal{T}}
      \left(
        \tfrac{1}{i \hbar} S_{int}
      \right)
    \right\}
    \\
    & =  
    \underset{
      {
        \tfrac{-1}{i \hbar} \{S',S\}_{\mathcal{T}}
      }
      \atop
      {
        \star_F 
        \exp_{\mathcal{T}}
        \left(
          \tfrac{1}{i \hbar} S_{int}
        \right)
      }
    }{
    \underbrace{
    \left\{
      -S'
      , 
      \exp_{\mathcal{T}}
      \left(
        \tfrac{1}{i \hbar} S_{int}
      \right)
    \right\}_{\mathcal{T}}
    }
    }
    - 
    i \hbar 
    \underset{
      {
        \left( 
          \tfrac{1}{i \hbar}
          \Delta_{BV}(S_{int})
          +
          \tfrac{1}{2 (i \hbar)^2}
          \left\{
            S_{int}, S_{int}
          \right\}_{\mathcal{T}}
        \right)
      }
      \atop
      {
        \star_{F} 
        \exp_{\mathcal{T}}
        \left(
          \tfrac{1}{i \hbar}
          S_{int}
        \right)
      }
    }{
    \underbrace{
    \Delta_{BV}
    \left(
      \exp_{\mathcal{T}}
      \left(
        \tfrac{1}{i \hbar} S_{int}
      \right)
    \right)    
    }
    }
    \\
    & = 
    \tfrac{-1}{i \hbar}
    \underset{ \text{QME} }{
    \underbrace{
    \left(
      \{S',S_{int}\} 
      + 
      \tfrac{1}{2}\{S_{int}, S_{int}\}
      +
      i \hbar \Delta_{BV}(S_{int})
    \right)
    }
    }
      \star_F
    \exp_{\mathcal{T}}
    \left(
      \tfrac{1}{i \hbar}
      S_{int}
    \right)
  \end{aligned}
$$

Here in the first step we used the definition of the [[BV-operator]] ([this def.](ForGaugeFixedFreeLagrangianFieldTheoryBVOperator)) to rewrite the plain antibracket in terms of the time-ordered antibracket ([this def.](BV-operator#AntibracketTimeOrdered)), then under the second brace we used that the time-ordered antibracket is the failure of the BV-operator to be a derivation ([this prop](BV-operator#AntibracketBVOperatorRelation)) and under the first brace the consequence of this statement for application to exponentials ([this example](BV-operator#TimeOrderedExponentialBVOperator)). Finally we collected terms, and to "complete the square" we added the terms on the left of 

$$
  \frac{1}{2} \underset{= 0}{\underbrace{\{S', S'\}_{\mathcal{T}}}} 
  - 
  i \hbar \underset{ = 0}{\underbrace{ \Delta_{BV}(S')}} = 0
$$

which vanish because, by definition of [[gauge fixing]] ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)), the free gauge-fixed action functional $S'$ is independent of [[antifields]]. 

But since the operation $(-) \star_F \exp_{\mathcal{T}}\left( \tfrac{1}{i \hbar} S_{int} \right)$ has the [[inverse]] $(-) \star_F \exp_{\mathcal{T}}\left( \tfrac{-1}{i \hbar}  S_{int} \right)$, this implies the claim.

Next we show that the [[quantum master equation]] implies the [[quantum master Ward identities]].

We use that the BV-differential $\{-S',-\}$ is a [[derivation]] of the [[Wick algebra]] product $\star_H$ (lemma \ref{DerivationBVDifferentialForWickAlgebra}).

First of all this implies that with $\{-S', \mathcal{S}(S_{int})\} = 0$ also 
$\{-S', \mathcal{S}(S_{int})^{-1}\} = 0$. 

Thus we compute as follows:

$$
  \begin{aligned}
    \{-S', -\} \circ \mathcal{R}^{-1}(A)
    & =
    \{-S', \mathcal{R}^{-1}(A)\}
    \\
    & = 
    \left\{
      { \, \atop \, }
      -S', 
      \mathcal{S}(S_{int})^{-1} 
        \star_H 
      \left( \mathcal{S}(S_{int}) \star_F a \right)
      {\, \atop \,}
    \right\}
    \\
    & = \phantom{+}
    \underset{
      = 0
    }{ 
    \underbrace{
    \left\{
      -S', \mathcal{S}(S_{int})^{-1}
    \right\}
    }
    }
      \star_H
    \left(
      \mathcal{S}(S_{int}) \star_F A
    \right)    
    \\
    & \phantom{=}
    +
    \mathcal{S}(S_{int})^{-1}
      \star_H
    \left\{
      -S',
      \mathcal{S}(S_{int}) \star_F A
    \right\}
    \\
    & = 
    \mathcal{S}(S_{int})^{-1}
      \star_H
    \left(
      \underset{
        = 1
      }{
      \underbrace{
        \mathcal{S}(+ S_{int}) 
          \star_F 
        \mathcal{S}(- S_{int})
      }
      }
        \star_F
      \left\{
        -S',
        \mathcal{S}(S_{int}) \star_F A
      \right\}
   \right)
   \\
   & =
    \mathcal{S}(S_{int})^{-1}
      \star_H
    \left(
      \mathcal{S}(+ S_{int}) 
        \star_F 
      \underset{ (\ast) }{
      \underbrace{
        \mathcal{S}(- S_{int})
          \star_F
        \left\{
          -S',
          \mathcal{S}(S_{int}) \star_F A
        \right\}
     }
     }
   \right)
   \\
   & =
   \mathcal{R}^{-1}
   \left(
     \underset{ (\ast) }{
     \underbrace{
       \phantom{\, \atop \,}
       \mathcal{S}(-S_{int})
         \star_F
       \left\{
         -S',
         \mathcal{S}(S_{int}) \star_F A
       \right\}
       }
       }
   \right)
  \end{aligned}
$$

By applying $\mathcal{R}$ to both sides of this equation, this means 
first of all that the interacting quantum BV-differential 
is equivalently given by

$$
  \mathcal{R} \circ \{-S', (-)\} \circ \mathcal{R}^{-1}
  \;=\;
  \mathcal{S}(-S_{int}) \star_F \{-S', \mathcal{S}(S_{int}) \star_F  (-)\}
  \,,
$$

hence that if either version (eq:OnRegularObservablesQuantumMasterWardIdentity) or (eq:OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered)  of the [[master Ward identity]] holds, it implies the other.

Now expanding out the definition of $\mathcal{S}$ (def. \ref{OnRegularObservablesPerturbativeSMatrix}) and expressing $\{-S',-\}$ via the [[time-ordered product|time-ordered]] [[antibracket]] ([this def.](BV-operator#AntibracketTimeOrdered)) and the [[BV-operator]] $\Delta_{BV}$ ([this prop.](BV-operator#ForGaugeFixedFreeLagrangianFieldTheoryBVOperator)) as

$$
  \{-S',-\}  
  \;=\;
  \{-S',-\}_{\mathcal{T}} - i \hbar \Delta_{BV}
$$

(on [[regular polynomial observables]]), we continue computing as follows:

$$
  \label{QMESecondStep}
  \begin{aligned}
    & \mathcal{R} \circ \{-S', (-)\} \circ \mathcal{R}^{-1}( A )
    \\
    & =
   \exp_{\mathcal{T}}
    \left( 
      \tfrac{-1}{i \hbar} S_{int} 
    \right)
      \star_F 
    \left\{
      -S', 
      \exp_{\mathcal{T}}
      \left(
         \tfrac{1}{i \hbar} S_{int}
      \right) 
        \star_F  
      A 
    \right\}
    \\
    & =
    \exp_{\mathcal{T}}
    \left( 
      \tfrac{-1}{i \hbar} 
        S_{int}
    \right)
      \star_F
    \left(
      \left\{
        -S', 
        \exp_{\mathcal{T}}
        \left( 
          \tfrac{ 1 }{i \hbar} S_{int}
        \right) 
          \star_F  
        A 
      \right\}_{\mathcal{T}}
      - 
      i \hbar 
      \Delta_{BV}
      \left(
        \exp_{\mathcal{T}}
        \left( 
           \tfrac{ 1 }{i \hbar} S_{int}
        \right) 
          \star_F 
        A
      \right)
    \right)
    \\
    & 
    \phantom{+}
    = 
    \tfrac{1}{i \hbar} \{ -S', S_{int}  \}_{\mathcal{T}} \star_F   A
    + 
    \{-S', A\}_{\mathcal{T}}
    \\
    &
    \phantom{=}
    - 
    i \hbar
    \exp_{\mathcal{T}}\left( \tfrac{-1}{i \hbar} S_{int}\right)
    \star_F
    \left(
      \underset{
        {
          \left(
          \tfrac{1}{i \hbar}\Delta_{BV}(S_{int})
          +
          \tfrac{1}{2 (i \hbar)^2} \left\{ S_{int}, S_{int} \right\}
          \right)
        }
        \atop
        {
          \star_F \exp_{\mathcal{T}}\left( \tfrac{ 1 }{i \hbar} S_{int} \right)
        }
      }{
      \underbrace{
        \Delta_{BV}
        \left(
          \exp_{\mathcal{T}}
          \left(
            \tfrac{ 1}{i \hbar} S_{int}
          \right)
        \right)
      }
      }
      \star_F A
      \,+\,
       \exp_{\mathcal{T}}
       \left(
         \tfrac{ 1}{i \hbar} S_{int}
       \right)
       \star_F
       \Delta_{BV}(A)
       \,+\,
       \underset{
         {
           \exp_{\mathcal{T}}\left( \tfrac{1}{i \hbar} S_{int} \right)
         }
         \atop
         {
           \star_F
           \tfrac{ 1}{i \hbar}
           \{S_{int}, A\}
         }
       }{ 
       \underbrace{
         \left\{
           \exp_{\mathcal{T}}
           \left(
             \tfrac{ 1}{i \hbar} S_{int}
           \right)
           \,,\,
           A
         \right\}_{\mathcal{T}}
      }
      }
    \right)
    \\
    & =
    -
    \left(
      \{ S' + S_{int}\,,\, A\}_{\mathcal{T}} 
        +
      i \hbar \Delta_{BV}(A)
    \right)
    \\
    & \phantom{=}
    -
    \tfrac{1}{i \hbar}
    \underset{ \text{QME} }{
    \underbrace{
    \left(
      \tfrac{1}{2} \{ S' + S_{int}, S' + S_{int} \}_{\mathcal{T}}
      +
      i \hbar  \Delta_{BV}( S' + S_{int} )
    \right)
    }}
      \star_F A
    \\
    & =
    -
    \left(
      \{ S' + S_{int}\,,\, A\}_{\mathcal{T}} 
        +
      i \hbar \Delta_{BV}(A)
    \right)
  \end{aligned}
$$

Here in the line with the braces we used that the [[BV-operator]] is a [[derivation]] of the [[time-ordered product]] up to correction by the time-ordered [[antibracket]] ([this prop.](BV-operator#AntibracketBVOperatorRelation)), and under the first brace we used the effect of that property on time-ordered exponentials ([this example](BV-operator#TimeOrderedExponentialBVOperator)), while under the second brace we used that $\{(-),A\}_{\mathcal{T}}$ is a derivation of the time-ordered product. Finally we have collected terms, added $0 = \{S',S'\} + i \hbar \Delta_{BV}(S')$ as before, and then used the QME.

This shows that the quantum [[master Ward identities]] follow from the [[quantum master equation]]. To conclude, it is now sufficient to show that, conversely, the MWI in terms of, say, retarded products implies the QME.

To see this, observe that with the BV-differential being nilpotent, also its conjugation by $\mathcal{R}$ is, so that with the above we have:

$$
  \begin{aligned}
  & \left( \{-S',-\}\right)^2 = 0
  \\
  \Leftrightarrow
  \;
  &
  \left( \mathcal{R} \circ \{-S',(-)\} \circ \mathcal{R}^{-1} \right)^2 = 0
  \\
  \Leftrightarrow  
  \;
  &
  \underset{
    \left\{
      {\, \atop \,}
      \tfrac{1}{2}\{S' + S_{int}, S' + S_{int}\}_{\mathcal{T}} 
      + 
      i \hbar \Delta_{BV}(S' + S_{int})
      \,,\,
      (-)
    \right\}
  }{
  \underbrace{
    \left(
      \{S' + S_{int}, (-)\}_{\mathcal{T}} + i \hbar \Delta_{BV}
    \right)^2 
  }
  } = 0
  \end{aligned}
$$

Here under the brace we computed as follows:

$$
  \begin{aligned}
  \left(
    \{S' + S_{int}, (-)\}_{\mathcal{T}} + i \hbar \Delta_{BV}
  \right)^2 
  & =
  \phantom{+}
  \underset{
    \tfrac{1}{2} \{ \{S' + S, S'+ S\}_{\mathcal{T}}, (-) \}_{\mathcal{T}}
  }{
  \underbrace{
    \{S' + S_{int}, \{S' + S_{int}\}_{\mathcal{T}}, (-) \}_{\mathcal{T}}
  }}
  \\
  &
  \phantom{=}
  +
  i \hbar
  \underset{
    \{  \Delta_{BV}(S'+ S)\,,\, (-)  \}_{\mathcal{T}}
  }{
  \underbrace{
  \left(
    \{S' + S_{int}, (-)\}_{\mathcal{T}} \circ \Delta_{BV}
    + 
    \Delta_{BV} \circ \{S' + S_{int}, (-)\}_{\mathcal{T}}
  \right)
  }}
  \\
  &
  \phantom{=}
  +   
  (i \hbar)^2 
   \underset{= 0}
   {
     \underbrace{
       \Delta_{BV} \circ \Delta_{BV}
      }
    }
  \end{aligned}
  \,.
$$

where, in turn, the term under the first brace follows by the graded [[Jacobi identity]], the one under the second brace by Henneaux-Teitelboim (15.105c) and the one under the third brace by Henneaux-Teitelboim (15.105b).

=--

+-- {: .num_example #MasterWardIdentityClassical}
###### Example
**([[classical master Ward identity]])**

The [[classical limit]] $\hbar \to 0$ of the [[quantum master Ward identity]] (eq:OnRegularObservablesQuantumMasterWardIdentity) is 

$$
  \{-S',(-)\} \circ \mathcal{R}^{-1}   
  \;=\;
  -
  \mathcal{R}^{-1}
  \left(
    \left\{ S' + S_{int} \,,\, (-) \right\}
  \right)
  \,.
$$

Applied to an observable which is linear in the [[antifields]]

$$
  A 
    \;=\; 
  \underset{\Sigma}{\int}
    A^a(x) 
    \mathbf{\Phi}^\ddagger_a(x)
  \, 
  dvol_\Sigma(x)
$$

this becomes

$$
  \begin{aligned}
    0
    & =
    \{-S', \mathcal{R}^{-1}(A)\} 
    +
    \mathcal{R}^{-1}
    \left(
      \left\{ S' + S_{int} \,,\, A \right\}_{\mathcal{T}}
    \right)
    \\
    & = 
    \underset{\Sigma}{\int} 
      \frac{\delta S'}{\delta \mathbf{\Phi}^a(x)} \mathcal{R}^{-1}(A^a(x))
    \, dvol_\Sigma(x)
    +   
    \mathcal{R}^{-1}
    \left(
      \underset{\Sigma}{\int}
          A^a(x) \frac{\delta (S' + S_{int})}{\delta \mathbf{\Phi}^a(x)}
        \, dvol_\Sigma(x)
    \right)
  \end{aligned}
$$

In this form the _classical Master Ward identity_ was originally identified in ([Dütsch-Fredenhagen 02, (90)](master+Ward+identity#DuetschFredenhagen02), [Brennecke-Dütsch 07, (5.5)](master+Ward+identity#BrennecketDuetsch07), following [Dütsch-Boas 02](master+Ward+identity#DuetschBoas02)). 


=--



### Renormalization and Master ward identity
 {#RenormalizationAndMasterWardIdentity}

The quantum master equation in the form of prop. \ref{QuantumMasterEquation} is derived on [[regular polynomial observables]], in particular hence for non-point-[[interaction]] [[action functionals]] $S_{int}$. But the [[interaction]] terms of interest are point-interactions, hence are [[local observables]]. The [[extension]] of the [[time-ordered product]] and hence of the [[perturbative S-matrix]] from regular to local onservables exsists but involves choices, these are the _[[renormalization]]_ choices in the formulation of [[causal perturbation theory]].

Since for [[gauge fixing|gauged fixed]] [[gauge theories]] this physically relevant [[observables]] are not the plain ([[microcausal polynomial observables|mcirocausal]]) [[polynomial observables]], but the [[cochain cohomology]] of the [[BV-BRST differential]] on them, one needs to require for gauge theories that the [[quantum master equation]] still holds after [[renormalization]]. This is closely related to the [[renormalization condition]] called the _[[master Ward identity]]_ ([Rejzner 11 (prop. 5.3.1) and following paragraphs](#Rejzner11)). If the quantum master equation cannot be retained in [[renormalization]] one says that the field theory suffers from a _[[quantum anomaly]]_.

## Related concepts

* [[master Ward identity]]


## References

The concept originates with

* {#BatalinVilkovisky81} [[Igor Batalin]], [[Grigori Vilkovisky]],  _Gauge Algebra and Quantization_, Phys. Lett. B 102 (1): 27&#8211;31, 1981 (<a href="https://doi.org/10.1016/0370-2693(81)90205-7">doi:10.1016/0370-2693(81)90205-7</a>) 

Traditional review includes

* {#HenneauxTeitelboim92} [[Marc Henneaux]], [[Claudio Teitelboim]], section 15.5.3 of _[[Quantization of Gauge Systems]]_, Princeton University Press, 1992

Discussion in the rigorous context of [[relativistic field theory|relativistic]] [[perturbative QFT]] formulated in [[causal perturbation theory]]/[[perturbative AQFT]] is in:

* {#FredenhagenRejzner11a} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in the functional approach to classical field theory_, Commun. Math. Phys. 314(1), 93&#8211;127 (2012) ([arXiv:1101.5112](https://arxiv.org/abs/1101.5112))

* {#FredenhagenRejzner11b} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. 317(3), 697&#8211;725 (2012) ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232))

* {#Rejzner11} [[Katarzyna Rejzner]], _Batalin-Vilkovisky formalism in locally covariant field theory_ ([arXiv:1111.5130](https://arxiv.org/abs/1111.5130))

* {#Rejzner13} [[Katarzyna Rejzner]], _Remarks on local symmetry invariance in perturbative algebraic quantum field theory_ ([arXiv:1301.7037](https://arxiv.org/abs/1301.7037))

and surveyed in

* {#Rejzner16} [[Kasia Rejzner]], section 7 of _Perturbative algebraic quantum field theory_ Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


[[!redirects classical master equation]]

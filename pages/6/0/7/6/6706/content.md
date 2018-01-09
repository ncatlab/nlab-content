

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

In [[perturbative quantum field theory]] formulated in terms of [[BV-BRST formalism]], the _classical master equation_ expresses the nilpotency of the [[BV-differential]] before [[quantization]], with the latter regarded as a [[Hamiltonian vector field]] with respect to the _[[antibracket]]_ $\{-,-\}$, for "Hamiltonian" the BV-BRST-extended [[action functional]] "S + S_{BRST}":

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
  \{S + S_{BRST}, S + BRST\} = 0
  \,.
$$

The _quantum  master equation_ is the version of this equation after [[quantization]], in which case the the [[BV-differential]] picks up a quantum correction of order $\hbar$ ([[Planck's constant]]) by the [[BV-operator]] $\Delta_{BV}$:

$$
  \left(\, \{S + S_{BRST},(-)\} + i \hbar \Delta_{BV} \, \right)^2 = 0
 \,.
$$


## In causal perturbation theory

> under construction

We discuss the quantum master equation in the rigorous formulation of [[relativistic field theory|relativistic]] [[perturbative quantum field theory]] via [[causal perturbation theory]]/[[perturbative AQFT]] ([Fredenhagen-Rejzner 11b](#FredenhagenRejzner11b), [Rejzner 11](#Rejzner11)).

### Background

Let $(E_{\text{BV-BST}},\mathbf{L}')$ be a [[gauge fixing|gauge fixed]] [[free field theory|free]] [[Lagrangian field theory]] with global [[BV-differential]]

$$
  \{-S', -\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ] 
$$

and with [[Feynman propagator]] $\Delta_F$.

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

is a [[derivation]] also with respect to the [[Wick algebra]] structure:

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


the [[perturbative S-matrix]] on [[regular polynomial observables]]

$$
  \mathcal{S} 
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))
$$

is

$$
  \mathcal{S}(S_{int})
  =
  \exp_{\star_F}(\tfrac{1}{i \hbar} S_{int})
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
$$

[[quantum Møller operator]] from [[Bogoliubov's formula]]

$$
  \mathcal{R}
    \;\coloneqq\;
  \mathcal{S}(S_{int})^{-1} 
    \star_H 
  (\mathcal{S}(S_{int}) \star_F (-))
$$

its inverse:

$$
  \mathcal{R}^{-1}
  \;=\;
  \mathcal{S}(-S_{int}) \star_F ( \mathcal{S}(S_{int}) \star(-) )
$$

notice the implicit dependencies

| [[endomorphism]] of <br/> [[regular polynomial observables]] | meaning | depends on choice of |
|--------|---------|----------------------|
| $\phantom{AA}\mathcal{T}$ | [[time-ordered product|time-ordering]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] |
| $\phantom{AA}\mathcal{S}$ | [[S-matrix]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] |
| $\phantom{AA}\mathcal{R}$ | [[quantum Møller operator]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] and [[interaction]] |



+-- {: .num_defn #FieldAlgebraObservable}
###### Definition
**([[interacting field algebra]])**

The [[interacting field algebra]] [[structure]] on [[regular polynomial observables]]

$$
  PolyObs(E_{\text{BV-BRST}})[ [\hbar] ] 
    \otimes 
  PolyObs(E_{\text{BV-BRST}})[ [\hbar] ] 
    \overset{ \star_{int} }{\longrightarrow}
  PolyObs(E_{\text{BV-BRST}})[ [\hbar] ] 
$$

is the [[conjugation]] of with [[Wick algebra]]-[[structure]] by the [[quantum Møller operator]]:

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

+-- {: .num_defn #BVDifferentialInteractingQuantum}
###### Definition
**(interacting quantum [[BV-differential]])**

The _interacting quantum BV-differential_ on the [[interacting field algebra]]
on [[regular polynomial observables]]

$$
  \mathcal{R}_V \circ \{-S', (-)\} \circ \mathcal{R}^{-1}
$$

=--

([Rejzner 11, (5.38)](#Rejzner11))

+-- {: .num_prop }
###### Proposition

If the [[perturbative S-matrix]] for [[interaction]] $S_{int}$ is $BV$-closed 

$$
  \{-S', \mathcal{S}(S_{int})\} = 0
$$

then the interacting quantum BV-differential (def. \ref{BVDifferentialInteractingQuantum}) is equal to

$$
  \mathcal{S}(-S_{int}) \star_F \{-S', \mathcal{S}(S_{int}) \star_F  (-)\}
$$

=--

([Rejzner 11, (5.38)](#Rejzner11))

+-- {: .proof}
###### Proof


We use that the BV-differential $\{-S',-\}$ is a [[derivation]] also of the [[Wick algebra]] product $\star_H$ (lemma \ref{DerivationBVDifferentialForWickAlgebra}).

First this implies that with $\{-S', \mathcal{S}(S_{int})\} = 0$ also 
$\{-S', \mathcal{S}(S_{int})^{-1}\} = 0$, and then that

$$
  \begin{aligned}
    \{-S', \mathcal{R}(A)\}
    & \coloneqq
    \left\{
      -S', 
      \mathcal{S}(S_{int})^{-1} 
        \star_H 
      \left( \mathcal{S}(S_{int}) \star_F a \right)
    \right\}_H
    \\
    & = \phantom{+}
    \underset{
      = 0
    }{ 
    \underbrace{
    \left\{
      -S', \mathcal{S}(S_{int})^{-1}
    \right\}_H
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
      \underset{  }{
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
   \mathcal{R}
   \left(
     \mathcal{S}(-S_{int})
       \star_F
     \left\{
       -S',
       \mathcal{S}(S_{int}) \star_F A
     \right\}
   \right)
  \end{aligned}
$$

=--

### Quantum master equation

Let $\Delta_{BV}$ be the [[BV-operator]].

+-- {: .num_defn }
###### Definition
**([[quantum master equation]])**

$$
  \left(
    \left\{-S' - S_{int}, (-) \right\}
    + i \hbar \Delta_{BV}
  \right)^2
  \;=\;
  0
$$

=--

## Related concepts

* [[master Ward identity]]


## References

The concept originates with

* {#BatalinVilkovisky81} [[Igor Batalin]], [[Grigori Vilkovisky]],  _Gauge Algebra and Quantization_, Phys. Lett. B 102 (1): 27&#8211;31, 1981 (<a href="https://doi.org/10.1016/0370-2693(81)90205-7">doi:10.1016/0370-2693(81)90205-7</a>) 

Traditional review includes

* {#HenneauxTeitelboim92} [[Marc Henneaux]], [[Claudio Teitelboim]], section 15.5.3  of _[[Quantization of Gauge Systems]]_, Princeton University Press, 1992

Discussion in the rigorous context of [[relativistic field theory|relativistic]] [[perturbative QFT]] formulated in [[causal perturbation theory]]/[[perturbative AQFT]] is in:

* {#FredenhagenRejzner11a} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in the functional approach to classical field theory_, Commun. Math. Phys. 314(1), 93&#8211;127 (2012) ([arXiv:1101.5112](https://arxiv.org/abs/1101.5112))

* {#FredenhagenRejzner11b} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. 317(3), 697&#8211;725 (2012) ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232))

* {#Rejzner11} [[Katarzyna Rejzner]], _Batalin-Vilkovisky formalism in locally covariant field theory_ ([arXiv:1111.5130](https://arxiv.org/abs/1111.5130))

* {#Rejzner13} [[Katarzyna Rejzner]], _Remarks on local symmetry invariance in perturbative algebraic quantum field theory_ ([arXiv:1301.7037](https://arxiv.org/abs/1301.7037))

and surveyed in

* {#Rejzner16} [[Kasia Rejzner]], section 7 of _Perturbative algebraic quantum field theory_ Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


[[!redirects classical master equation]]

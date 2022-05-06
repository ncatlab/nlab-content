

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Vacua
+-- {: .hide}
[[!include vacua -- contents]]
=--
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

In [[quantum field theory]], a given [[vacuum state]] is called _stable_ if in a suitable sense it does not evolve into or from any orthogonal state.

In [[perturbative quantum field theory]] with specified [[S-matrix]] $\mathcal{S}(g S_{int})$ it makes sense to say that a vacuum state is stable if there is vanishing [[quantum probability]] for the vacuum state to scatter into a non-vacuum state, or for a non-vacuum state to scatter into the vacuum state. (e.g. [Nikolic 01, p. 6](#Nikolic01))

## Definition



+-- {: .num_defn #VacuumStability}
###### Definition
**([[vacuum stability]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to ([this def.](S-matrix#VacuumFree)), let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to ([this. def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering)), and let $g S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g] ]\langle g \rangle$ be a [[local observable]], regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

We say that the given [[Hadamard vacuum state|Hadamard]] [[vacuum state]] ([this prop.](Wick+algebra#WickAlgebraCanonicalState))

$$
  \langle - \rangle
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar , g, j ] ]
  \longrightarrow
  \mathbb{C}[ [ \hbar, g, j ] ]
$$

is _[[vacuum stability|stable]]_ with respect to the [[interaction]] $S_{int}$, if for all elements of the [[Wick algebra]]

$$
  A \in PolyObs(E_{\text{BV-BRST}})_{mc}[ [ \hbar, g] ] 
$$

we have

$$
  \left\langle
    A \mathcal{S}(g S_{int})
  \right\rangle
  \;=\;
  \left\langle
     \mathcal{S}(g S_{int})
  \right\rangle
  \,
  \left\langle
    A
  \right\rangle
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \left\langle
    \mathcal{S}(g S_{int})^{-1}
    A
  \right\rangle
  \;=\;
  \frac{1}
  {
    \left\langle
      \mathcal{S}(g S_{int})
    \right\rangle
   }
   \left\langle 
     A  
   \right\rangle
$$

=--

## Properties


+-- {: .num_example #ScatteringAmplitudeFromInteractingFieldObservables}
###### Example
**([[scattering amplitudes]] as [[vacuum expectation values]] of [[interacting field observables]])**

Let $(E_{\text{BV-BRST}}, \mathbf{L}', \Delta_H )$ be a [[relativistic field theory|relativistic]] [[free field theory|free]] [[vacuum]] according to [this def.](S-matrix#VacuumFree), let $\mathcal{S}$ be a corresponding [[S-matrix]] scheme according to [this def.](S-matrix#LagrangianFieldTheoryPerturbativeScattering), and let $g S_{int} \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g ] ]\langle g \rangle$ be a [[local observable]] regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]]-[[action functional|functional]],
such that the [[vacuum state]] is [[vacuum stability|stable]] with respect to $g S_{int}$ (def. \ref{VacuumStability}).

Consider [[local observables]]

$$
  \array{
    A_{in,1}, \cdots, A_{in , n_{in}},
    \\
    A_{out,1}, \cdots, A_{out, n_{out}}
  }
  \;\;\in\;\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g] ]
$$

whose spacetime support satisfies the following [[causal ordering]]:

$$
  A_{out, i_{out} }
  {\gt\!\!\!\!\lt}
  A_{out, j_{out}}
  \phantom{AAA}
  A_{out, i_{out} }
    {\vee\!\!\!\wedge}
  S_{int}
    {\vee\!\!\!\wedge}
  A_{in, i_{in}}
  \phantom{AAA}
  A_{in, i_{in} }
  {\gt\!\!\!\!\lt}
  A_{in, j_{in}}
$$

for all $1 \leq i_{out} \lt j_{out} \leq n_{out}$ and $1 \leq  i_{in} \lt j_{in} \leq n_{in}$.

Then the [[vacuum expectation value]] of the [[Wick algebra]]-product of the corresponding [[interacting field observables]] ([this def.](S-matrix#InteractingFieldObservables))
is



$$
  \begin{aligned}
   &
   \left\langle
     {\, \atop \,}
     (A_{out, 1})_{int}
     \cdots
     (A_{out,n_{out}})_{int}
     \,
     (A_{in, 1})_{int}
     \cdots
     (A_{in,n_{in}})_{int}
     {\, \atop \,}
   \right\rangle
   \\
   & =
   \left\langle
     {\, \atop \,}
       A_{out,1}
       \cdots
       A_{out,n_{out}}
    \right|
       \;
       \mathcal{S}(g S_{int})
       \;
    \left|
       A_{in,1}
       \cdots
       A_{in, n_{in}}
     {\, \atop \,}
   \right\rangle
   \\
   & \coloneqq
   \frac{1}{
     \left\langle \mathcal{S}(g S_{int}) \right\rangle
   }
   \left\langle
     {\, \atop \,}
       A_{out,1}
       \cdots
       A_{out,n_{out}}
       \;
       \mathcal{S}(g S_{int})
       \;
       A_{in,1}
       \cdots
       A_{in, n_{in}}
     {\, \atop \,}
   \right\rangle
   \,.
  \end{aligned}
$$

These [[vacuum expectation values]] are interpreted, in the [[adiabatic limit]] where $g_{sw} \to 1$, as _[[scattering amplitudes]]_ (see [this remark](S-matrix#FromAxiomaticSMatrixScatteringAmplitudes)).

=--

For **proof** see at _[[S-matrix]]_, [this prop.](S-matrix#ScatteringAmplitudeFromInteractingFieldObservables).

## Examples

* _[Higgs field -- Mass and Vacuum (in-)stability](Higgs+field#MassAndVacuumInstability)_



## Related concepts

[[!include states and observables -- content]]



## References
 
* {#Scharf96} [[Günter Scharf]], _Vacuum stability in quantum field theory_, Nuovo Cim. A109 (1996) 1605-1607 ([spire:432208](http://inspirehep.net/record/432208/))

Discussion for [[QED]]:

* {#Nikolic01} [[Hrvoje Nikolić]], _Physical stability of the QED vacuum_, 2001 ([arXiv:hep-ph/0105176](https://arxiv.org/abs/hep-ph/0105176))

Discussion for [[Higgs field]]:

* J.R. Espinosa, G. Giudice, A. Riotto, _Cosmological implications of the Higgs mass measurement_, JCAP 0805:002, 2008 ([arXiv:0710.2484](https://arxiv.org/abs/0710.2484))

* [[John Ellis]], J.R. Espinosa, G.F. Giudice, A. Hoecker, A. Riotto, _The Probable Fate of the Standard Model_, Phys. Lett. B679:369-375, 2009 ([arXiv:0906.0954](https://arxiv.org/abs/0906.0954))

* Dario Buttazzo, Giuseppe Degrassi, Pier Paolo Giardino, [[Gian Giudice]], Filippo Sala, Alberto Salvio, Alessandro Strumia, _Investigating the near-criticality of the Higgs boson_ ([arXiv:1307.3536](https://arxiv.org/abs/1307.3536))

* Anson Hook, John Kearney, Bibhushan Shakya, Kathryn M. Zurek, _Probable or Improbable Universe? Correlating Electroweak Vacuum Instability with the Scale of Inflation_, J. High Energ. Phys. (2015) 2015: 61 ([arXiv:1404.5953](https://arxiv.org/abs/1404.5953))

* Jose R. Espinosa, Gian F. Giudice, Enrico Morgante, Antonio Riotto, Leonardo Senatore, Alessandro Strumia, Nikolaos Tetradis, _The cosmological Higgstory of the vacuum instability_ ([arXiv:1505.04825](https://arxiv.org/abs/1505.04825))

* William E. East, John Kearney, Bibhushan Shakya, Hojin Yoo, Kathryn M. Zurek, _Spacetime Dynamics of a Higgs Vacuum Instability During Inflation_, Phys. Rev. D 95, 023526 (2017) ([arXiv:1607.00381](https://arxiv.org/abs/1607.00381))

* {#Kane18} [[Gordon Kane]], _Exciting Implications of LHC Higgs Boson Data_ ([arXiv:1802.05199](https://arxiv.org/abs/1802.05199))



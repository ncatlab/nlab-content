
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

In [[perturbative quantum field theory]] a _Ward identity_ expresses the invariance or equivariance of [[correlation functions]] under some given [[symmetry]].

For a [[Lagrangian field theory]], the _classical Ward identity_ is an [[on-shell]] [[equation]] satisfied by classical [[observables]] due to [[symmetries]] of the [[action functional]]. For quantum observables it is not automatic, but one may consider imposing it as a constraint on the choice of [[renormalization]]. As such it is called the _quantum master Ward identity_ (really a [[renormalization condition]]). It is a generalization of the [[Schwinger-Dyson equation]] to non-[[free field theory|free]] field theory: It may be understood as expressing the [[renormalization]] of the [[BV-differential]] with quantum correction by the [[BV-operator]], in fact it is equivalent to the _[[quantum master equation]]_ in [[BV-BRST formalism]] ([this prop.](quantum+master+equation#QuantumMasterEquation)).

## Details

### Before renormalization
 {#BeforeRenormalization}

Consider a [[free field theory|free]] [[gauge fixing|gauge fixed]] [[Lagrangian field theory]] $(E_{\text{BV-BRST}}, \mathbf{L}')$ ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)) with global [[BV-differential]] on [[regular polynomial observables]] 

$$
  \{-S',(-)\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]  
$$

([this def.](A+first+idea+of+quantum+field+theory#ComplexBVBRSTGlobal)).

Let moreover

$$
  g S_{int} 
   \;\in\; 
  PolyObs(E_{\text{BV-BRST}})_{{reg}\atop {deg = 0}}[ [ \hbar , g  ] ]
$$

be a [[regular polynomial observable]] in degree 0 (regarded as an [[adiabatic switching|adiabatically switched]] non-point-[[interaction]] [[action functional]]) such that the total action $S' + g S_{int}$ satisfies the [[quantum master equation]] ([this prop.](quantum+master+equation#QuantumMasterEquation)); and write

$$
  \mathcal{R}^{-1}(-)
  \;\coloneqq\;
  \mathcal{S}(g S_{int})^{-1} 
    \star_H 
  (\mathcal{S}(g S_{int}) \star_F (-))
$$

for the corresponding [[quantum Møller operator]] ([this def.](quantum+master+equation#MollerOperatorOnRegularPolynomialObservables)).

Then by [this prop.](quantum+master+equation#QuantumMasterEquation) we have

$$
  \label{OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered}
  \{-S',(-)\} \circ \mathcal{R}^{-1}   
  \;=\;
  \mathcal{R}^{1}
  \left(
    \left\{ -(S' + g S_{int}) \,,\, (-) \right\}_{\mathcal{T}} 
    - 
    i \hbar   \Delta_{BV}
  \right)
$$

This is the _quantum master Ward identity_ on [[regular polynomial observables]] (i.e. before [[renormalization]]) according to [Rejzner 13, (37)](#Rejzner13).

+-- {: .num_remark }
###### Remark
**([[quantum master Ward identity]] relates [[quantum field theory|quantum]] [[interacting field theory|interacting field]] [[equation of motion|EOMs]] to [[classical field theory|classical]] [[free field]] [[equation of motion|EOMs]])**

For $A \in PolyObs(E_{\text{BV-BRST}})_{reg}[ [ \hbar, g] ] $ the [[quantum master Ward identity]] on [[regular polynomial observables]] (eq:OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered) reads

$$
  \mathcal{R}^{-1}
  \left(
    \left\{ -(S' + g S_{int}) \,,\, A \right\}_{\mathcal{T}} 
    - 
    i \hbar   \Delta_{BV}(A)
  \right)
  \;=\;
  \{-S', \mathcal{R}^{-1}(A) \} 
$$

The term on the right is manifestly in the [[image]] of the global [[BV-differential]] $\{-S',-\}$ of the [[free field theory]] ([this def.](A+first+idea+of+quantum+field+theory#ComplexBVBRSTGlobal)) and hence vanishes when passing to [[on-shell]] observables along the [[isomorphism]] ([this equation](A+first+idea+of+quantum+field+theory#eq:OnShellPolynomialObservablesAsBVCohomology))

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

(by [this example](A+first+idea+of+quantum+field+theory#BVDifferentialGlobal)).

Hence

$$
  \mathcal{R}^{1}
  \left(
    \left\{ -(S' + g S_{int}) \,,\, A \right\}_{\mathcal{T}} 
    - 
    i \hbar   \Delta_{BV}(A)
  \right)
  \;=\;
  0
  \phantom{AAA}
  \text{on-shell}
$$

In contrast, the left hand side is the [[interacting field observable]] (via [this def.](S-matrix#MollerOperatorOnRegularPolynomialObservables)) of the [[antibracket]] with the [[action functional]] of the [[interacting field theory]] plus a quantum correction given by the [[BV-operator]].

Hence the [[quantum master Ward identity]] expresses a relation between the ideal spanned by the [[classical field theory|classical]] [[free field theory|free field]] [[equations of motion]] and the [[quantum field theory|quantum]] [[interacting field theory|interacting field]] equations of motion.  

=--

+-- {: .num_example}
###### Example
**([[free field]]-limit of [[master Ward identity]] is [[Schwinger-Dyson equation]])**

In the [[free field]]-limit $g \to 0$ the [[quantum master Ward identity]] (eq:OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered) reduces to

$$
  \left\{ -S'  \,,\, A \right\}_{\mathcal{T}} 
  - 
  i \hbar   \Delta_{BV}(A)
  \;=\;
  \{-S', A  \} 
$$

which is the defining equation for the [[BV-operator]] ([this equation](BV-operator#eq:BVOperatorDefiningRelation)), hence is isomorphic (under $\mathcal{T}$) to the [[Schwinger-Dyson equation]] ([this prop.](BV-operator#DysonSchwinger))

=--

+-- {: .num_example}
###### Example

In the [[classical limit]] $\hbar \to 0$ (noticing that the classical limit of $\{-,-\}_{\mathcal{T}}$ is $\{-,-\}$) the [[quantum master Ward identity]] (eq:OnRegularObservablesQuantumMasterWardIdentityViaTimeOrdered) reduces to

$$
  \mathcal{R}^{1}
  \left(
    \left\{ -(S' + g S_{int}) \,,\, A \right\} 
  \right)
  \;=\;
  \{-S', \mathcal{R}^{-1}(A) \} 
$$

This says that the [[interacting field observable]] corresponding to the global [[antibracket]] with the action functional of the [[interacting field theory]] vanishes on-shell, classically.

Applied to an observable which is [[linear map|linear]] in the [[antifields]]

$$
  A 
    \;=\; 
  \underset{\Sigma}{\int}
    A^a(x) 
    \mathbf{\Phi}^\ddagger_a(x)
  \, 
  dvol_\Sigma(x)
$$

this yields

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

This is the _classical Master Ward identity_ according to ([Dütsch-Fredenhagen 02](#DuetschFredenhagen02), [Brennecke-Dütsch 07, (5.5)](#BrennecketDuetsch07)), following ([Dütsch-Boas 02](#DuetschBoas02)).

=--


## Examples

* [[conformal blocks]]

## References

Named after _[[John Clive Ward]]_.

Discussion in the rigorous context of [[relativistic field theory|relativistic]] [[perturbative quantum field theory]] formulated via [[causal perturbation theory]]/[[perturbative AQFT]] is in

* {#DuetschBoas02} [[Michael Dütsch]], F.-M. Boas, _The Master Ward Identity_, Rev. Math. Phys 14, (2002) 977-1049 ([pdf](http://cds.cern.ch/record/526377/files/0111101.pdf))

* {#DuetschFredenhagen02} [[Michael Dütsch]], [[Klaus Fredenhagen]], equation (90) in _The Master Ward Identity and Generalized Schwinger-Dyson Equation in Classical Field Theory_, Commun.Math.Phys. 243 (2003) 275-314 ([arXiv:hep-th/0211242](https://arxiv.org/abs/hep-th/0211242))

* {#BrennecketDuetsch07} Ferdinand Brennecke, [[Michael Dütsch]], equation (5.5) in  _Removal of violations of the Master Ward Identity_, in perturbative QFT, Rev.Math.Phys. 20 (2008) 119-172 ([arXiv:https://arxiv.org/abs/0705.3160](https://arxiv.org/abs/0705.3160))

* {#Hollands07} [[Stefan Hollands]], around (322) and (333) and (345) of _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev. Math. Phys.20:1033-1172, 2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))

* {#Rejzner11} [[Katarzyna Rejzner]], section 5.3 of _Batalin-Vilkovisky formalism in locally covariant field theory_ ([arXiv:1111.5130](https://arxiv.org/abs/1111.5130))

* {#Rejzner13} [[Katarzyna Rejzner]], equation (37) of _Remarks on local symmetry invariance in perturbative algebraic quantum field theory_ ([arXiv:1301.7037](https://arxiv.org/abs/1301.7037))

* {#Duetsch18} [[Michael Dütsch]], equation (4.2) of _[[From classical field theory to perturbative quantum field theory]]_, 2018

See also

* Wikipedia, _[Ward-Takahashi identity](http://en.wikipedia.org/wiki/Ward%E2%80%93Takahashi_identity)_

[[!redirects Ward identities]]


[[!redirects Ward–Takahashi identity]]
[[!redirects Ward–Takahashi identities]]

[[!redirects classical master Ward identity]]
[[!redirects classical master Ward identities]]

[[!redirects quantum master Ward identity]]
[[!redirects quantum master Ward identities]]

[[!redirects master Ward identity]]
[[!redirects master Ward identities]]



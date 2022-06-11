
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

The _microcausal functionals_ on the space $C^\infty(X)$ of [[smooth functions]] on a [[globally hyperbolic spacetime]] $(X,e)$ are those which come from [[compactly supported distributions]] on some [[Cartesian product]] of copies of $X$ such that the [[wave front set]] of the distributions excludes those covectors to a point in $X^n$ all whose components are in the [[closed future cone]] or all whose components are in the [[closed past cone]]

These functionals underly the [[Wick algebra]] of [[free field theories]]. The condition on the wave front is such that the [[product of distributions]] with a [[Hadamard distribution]] is well defined, so that the coresponding [[Moyal star product]] is well defined, which gives the [[Wick algebra]]. At the same time the condition includes [[local observables]] and hence in particular the usual ([[adiabatic switching|adiabatically switched]]) point-[[interaction]] terms, such as of [[phi^4 theory]].

[[!include perturbative observables -- table]]

## Definition


+-- {: .num_defn #PolynomialObservable}
###### Definition
**([[polynomial observable]])**

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

=--


+-- {: .num_defn #MicrocausalObservable}
###### Definition
**([[microcausal observable]])**

For $\Sigma$ a [[spacetime]], hence a [[Lorentzian manifold]] with [[time orientation]], then a _[[microcausal observable]]_ is a [[polynomial observable]] (def. \ref{PolynomialObservable}) such that each [[coefficient]] $\alpha^{(k)}$ has [[wave front set]] excluding those points  where all $k$ [[wave vectors]] are in the [[closed future cone]] or all in the [[closed past cone]].

=--


## Examples

+-- {: .num_example }
###### Example
**([[non-singular distribution|non-singular observables]] are [[microcausal observables|microcausal]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]].

Then a [[regular observable]], hence a [[polynomial observable]] ([this def.](A+first+idea+of+quantum+field+theory+--+Observables#PolynomialObservables)) whose [[distribution|distributional]] [[coefficients]] $\alpha_{a_1 \cdots a_k}$ (eq:RecalledForWickAlgebraExpansionOfPolynomialObservables) are [[non-singular distributions]] is a [[microcausal observable]] (def. \ref{MicrocausalFunctionals}).

This is simply because the [[wave front set]] of [[non-singular distributions]] is [[empty set|empty]] (by definition, via the [[Paley-Wiener-Schwartz theorem]], [this prop.](Schwartz+theorem#DecayPropertyOfFourierTransformOfCompactlySupportedFunctions)).

=--

+-- {: .num_example}
###### Example
**(compactly averaged point evaluations are microcausal)**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]]. Assume the [[field bundle]] $E$ is a [[trivial vector bundle]] with linear [[fiber]] coordinates $(\phi^a)$.

Let $g \in C^\infty_c(X)$ be a [[bump function]], then for $n \in \mathbb{N}$ the polynomial observables ([this def.](A+first+idea+of+quantum+field+theory+--+Observables#PolynomialObservables)) of the form

$$
  \array{
    \Gamma_\Sigma(E) &\overset{}{\longrightarrow}& \mathbb{C}
    \\
    \Phi 
      &\mapsto& 
    \int_X g(x) 
      \tilde \alpha_{a_1 \cdots a_k}(x) 
      \Phi^{a_1}(x) \cdots \Phi^(a_k)\,  dvol_\Sigma(x)
  }
$$

are [[microcausal observable|microcausal]] (def. \ref{MicrocausalFunctionals}).

If here we think of $\phi(x)^n$ as a point-[[interaction]] term (as for instance in [[phi^4 theory]]) then $g$ is to be thought of as an "[[adiabatic switching|adiabatically switched]]" [[coupling constant]]. These are the relevant [[interaction terms]] to be quantized via [[causal perturbation theory]].

=--

+-- {: .proof}
###### Proof


For notational convenience, consider the case of the [[scalar field]] with $k = 2$; the general case is directly analogous. Then the [[local observable]] coming from $\phi^2$ (a [[phi^n interaction]]-term), has, regarded as a [[polynomial observable]], the [[delta distribution]] $\delta(x_1-x_2)$ as [[coefficient]] in degree 2:

$$
  \begin{aligned}
    A(\Phi)
    & =
    \underset{\Sigma}{\int} g(x) (\Phi(x))^2 \,dvol_\Sigma(x)
    \\
    & =
    \underset{\Sigma \times \Sigma}{\int} 
      \underset{ = \alpha^{(2)}}{
      \underbrace{
        g(x_1)
        \delta(x_1 - x_2)
      }}
      \, 
     \Phi(x_1) \Phi(x_2) \, dvol_\Sigma(x_1) \, dvol_\Sigma(x_2)
  \end{aligned}
  \,.
$$

Now for $(x_1, x_2) \in \Sigma \times \Sigma$ and $\mathbb{R}^{2n} \simeq U \subset X \times X$ a [[chart]] around this point,  the [[Fourier transform of distributions]] of $g \cdot \delta(-,-)$ restricted to this chart is proportional to the Fourier transform $\hat g$ of $g$ evaluated at the sum of the two covectors:

$$
  \begin{aligned}
    (k_1, k_2)
      & \mapsto
      \underset{\mathbb{R}^{2n}}{\int} 
      g(x_1) 
      \delta(x_1, x_2) 
      e^{i (k_1 \cdot x_1 + k_2 \cdot x_2 )} 
      \, dvol_\Sigma(x_1) \, dvol_\Sigma(x_2)
    \\
    & \propto \hat g(k_1 + k_2)
   \end{aligned}
  \,.
$$


Since $g$ is a plain [[bump function]], its [[Fourier transform]] $\hat g$ is quickly decaying (according to [this inequality](compactly+supported+distribution#eq:DecayEstimateForFourierTransformOfNonSingularDistribution))  along $k_1 + k_2$ ([this prop.](wavefront+set#EmptyWaveFronSetCorrespondsToOrdinaryFunction)), as long as $k_1 + k_2 \neq 0$. Only on the cone $k_1 + k_2 = 0$ the Fourier transform is constant, and hence in particular not decaying.


<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/WaveFrontSetOfDeltaDistributionInTwoVariables.png" width="200"/>
</div>

{#WaveFrontOfdeltaxy} This means that the wave front set consists of the elements of the form $(x, (k, -k))$ with $k \neq 0$. Since $k$ and $-k$ are both in the [[closed future cone]] or both in the [[closed past cone]] precisely if $k = 0$, this situation is excluded in the wave front set and hence the distribution $g \cdot \delta(-,-)$ is [[microcausal observable|microcausal]].

> (graphics grabbed from [Khavkine-Moretti 14, p. 45](#KhavkineMoretti14))

=--

This shows that microcausality in this case is related to conservation of momentum in the point interaction.

More generally:

+-- {: .num_example #CompactlySupportedPolynomialLocalDensities}
###### Example
**(polynomial [[local observables]] are microcausal)**

Write

$$
  \Omega_{poly}^{h,v}(E)
$$

for the space of differential forms on the [[jet bundle]] 
of the [[field bundle]] $E$ which locally are [[polynomials]]
in the field variables.

$$
  \mathcal{F}_{loc}
    \; \subset \;
  C^\infty_c(\Sigma) \underset{\Omega_{poly}^{0,0}(E)}{\otimes} \Omega_{poly}^{d,0}(E)
$$

for the subspace of [[horizontal differential forms]] of degree $d$ on the [[jet bundle]] ([[local Lagrangian densities]])
of those which are [[compact support|compactly supported]] with respect to $\Sigma$ ([[local observables]]) and [[polynomial]] with respect to the 
field variables.

Every $L \in \mathcal{F}_{loc}$ induces a functional

$$
   \Gamma_\Sigma(E) \longrightarrow \mathbb{R}
$$

by [[integration of differential forms|integration]] of the [[pullback of differential forms|pullback]]
of $L$ along the [[jet prolongation]] of a given [[section]]:

$$
  \phi \mapsto \int_{\Sigma} j^\infty(\phi)^\ast L 
  \,.
$$

These functionals happen to be [[microcausal functional|microcausal]], so that there is an inclusion

$$
  \mathcal{F}_{loc} \hookrightarrow \mathcal{F}_{mc}
$$

into the space of microcausal functionals (e.g. [Fredenhagen-Rejzner 12, p. 21](#FredenhagenRejzner12)). In fact this is a [[dense subspace]] inclusion (e.g. [Fredenhagen-Rejzner 12, p. 23](#FredenhagenRejzner12))

=--

## Properties

+-- {: .num_prop}
###### Proposition

Write $\mathcal{F}_{reg} \subset \mathcal{F}_{mc}$ for that subalgebra of the algebra of microcausal functionals whose [[coefficients]] are [[non-singular distributions]].

Let 

$$
  \langle -\rangle 
  \;\colon\;
  \mathcal{F}_{reg} 
  \longrightarrow 
  \mathbb{C}
$$

be a [[state on a star-algebra|state]] on regular observables which is [[quasi-free Hadamard state|quasi-free Hadamard]]. Then this uniquely [[extensions|extends]] to a state on microcausal functionsal

$$
  \array{
    \mathcal{F}_{reg} 
      &\overset{\langle -\rangle}{\longrightarrow}& 
    \mathbb{C}
    \\
    \downarrow & \nearrow_{\mathrlap{\exists ! \langle -\rangle}}
    \\
    \mathcal{F}_{mc}
  }
$$

=--

([Hollands-Ruan 01, remark 1 on p. 12](#HollandRuan01), implied by [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00), [Hollands-Wald 01](#HollandsWald01), a special case of [Hollands-Ruan 01, theorem III.1 (ii)](#HollandRuan01))

## Related concepts

[[!include states and observables -- content]]


## References

### Original articles

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

* {#DuetschFredenhagen01a} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Algebraic Quantum Field Theory, Perturbation Theory, and the Loop Expansion_, Commun.Math.Phys. 219 (2001) 5-30 ([arXiv:hep-th/0001129](https://arxiv.org/abs/hep-th/0001129))

* {#HollandsWald01} [[Stefan Hollands]], [[Robert Wald]], _Local Wick polynomials and time ordered products of quantum fields in curved spacetime_, Commun. Math. Phys., Commun.Math.Phys.223:289-326,2001 ([arXiv:gr-qc/0103074](https://arxiv.org/abs/gr-qc/0103074))

* {#DutschFredenhagen01b} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic field theory, and deformation quantization_, in [[Roberto Longo]] (ed.), _Mathematical Physics in Mathematics and Physics, Quantum and Operator Algebraic Aspects_, volume 30 of Fields Institute Communications, pages 151&#8211;160. American Mathematical Society, 2001
([arXiv:hep-th/0101079](https://arxiv.org/abs/hep-th/0101079))

* {#HollandRuan01} [[Stefan Hollands]], Weihua Ruan, _The State Space of Perturbative Quantum Field Theory in Curved Spacetimes_, Annales Henri Poincare 3 (2002) 635-657 ([arXiv:gr-qc/0108032](https://arxiv.org/abs/gr-qc/0108032))

* {#BrunettiFredenhagenRibeiro12} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Pedro Lauridsen Ribeiro]], section 4.1 of _Algebraic Structure of Classical Field Theory: Kinematics and Linearized Dynamics for Real Scalar Fields_ ([arXiv:1209.2148](https://arxiv.org/abs/1209.2148))

### Review

* {#FredenhagenRejzner12} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative algebraic quantum field theory_, In _Mathematical Aspects of Quantum Field Theories_, Springer 2016 ([arXiv:1208.1428](https://arxiv.org/abs/1208.1428))

* {#KhavkineMoretti14} [[Igor Khavkine]], [[Valter Moretti]], _Algebraic QFT in Curved Spacetime and quasifree Hadamard states: an introduction_, Chapter 5 in [[Romeo Brunetti]] et al. (eds.) _Advances in Algebraic Quantum Field Theory_, Springer, 2015 ([arXiv:1412.5945](https://arxiv.org/abs/1412.5945))

* [[Katarzyna Rejzner]], section 4.4.1 of _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))

* {#Duetsch18} [[Michael Dütsch]], def. 1.2 and equation (2.47) in _[[From classical field theory to perturbative quantum field theory]]_, 2018

[[!redirects microcausal polynomial observables]]

[[!redirects microcausal observable]]
[[!redirects microcausal observables]]

[[!redirects microcausal functional]]
[[!redirects microcausal functionals]]



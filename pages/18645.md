
<img src="https://ncatlab.org/schreiber/files/HamburgAnnouncement.jpg" width="850" >


These notes mean to give an expository but rigorous introduction to the basic concepts
of [[relativistic quantum field theory|relativistic]] [[perturbative quantum field theories]], specifically those
that arise as the [[perturbative quantum field theory|perturbative]] [[quantization]] of a _[[Lagrangian field theory]]_
-- such as [[quantum electrodynamics]], [[quantum chromodynamics]], and [[perturbative quantum gravity]]
appearing in the [[standard model of particle physics]].

For broad introduction of the idea of the topic of _[[perturbative quantum field theory]]_ see [[perturbative quantum field theory|there]] and see

* PhysicsForums-Insights: _[Introduction to Perturbative Quantum Field Theory](https://www.physicsforums.com/insights/paqft-idea-references/)_

Here, first we consider [[classical field theory]] (or rather [[pre-quantum field theory]]), complete with [[BV-BRST formalism]];
then its [[deformation quantization]] via [[causal perturbation theory]] to [[perturbative quantum field theory]].
This mathematically rigorous (i.e. clear and precise) formulation of the traditional informal lore
has come to be known as _[[perturbative algebraic quantum field theory]]_.

We aim to give a _fully [[local field theory|local]]_ discussion, where all structures arise
on the "[[jet bundle]] over the [[field bundle]]" (introduced [below](#FieldVariations)) and "[[transgression|transgress]]" from there to the [[spaces of field histories]] over [[spacetime]] (discussed [further below](#Observables)).
This "[[schreiber:Higher Prequantum Geometry]]" streamlines traditional constructions and serves the conceptualization in the theory.
This is joint work with [[Igor Khavkine]].


In full beauty these concepts are extremely general and powerful; but the aim here is to give a first precise idea of the subject, not
a fully general account.
Therefore we concentrate on the special case where [[spacetime]] is [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime} below), where the [[field bundle]] (def. \ref{FieldsAndFieldBundles} below) is an ordinary [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle} below) and hence the [[Lagrangian  density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below) is [[locally variational field theory|globally defined]].
Similarly, when considering [[gauge theory]] we consider just the special case that the [[gauge parameter]]-bundle
is a [[trivial vector bundle]]  and we concentrate on the case that the gauge symmetries are "closed irreducible" (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation} below).
But we aim to organize all concepts such that the _structure_ of their generalization to [[AQFT on curved spacetime|curved spacetime]]
and non-trivial [[field bundles]] is immediate.

This comparatively simple setup already subsumes what is considered in traditional texts on the subject; it captures the established [[perturbative quantum field theory|perturbative]] [[BV formalism|BRST-BV quantization]] of [[gauge fields]] coupled to [[fermions]] [[AQFT on curved spacetime|on curved spacetimes]]
-- which is the state of the art.
Further generalization, necessary for the discussion of global topological effects, such as [[instanton]] configurations
of [[gauge fields]], will be discussed elsewhere (see at _[[homotopical algebraic quantum field theory]]_).

Alongside the theory we develop the concrete examples of the [[real scalar field]], the [[electromagnetic field]] and the [[Dirac field]]:

**running examples**
{#RunningExamples}


| [[field (physics)|field]] |  [[field bundle]] |  [[Lagrangian density]] | [[equation of motion]] |
|---------------------------|------------------|-------------------------|------------------------|
| [[real scalar field]] |  expl. \ref{RealScalarFieldBundle} |  expl. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime} | expl. \ref{FreeScalarFieldEOM} |
| [[Dirac field]] | expl. \ref{DiracFieldBundle}  | expl. \ref{LagrangianDensityForDiracField}  |  expl. \ref{EquationOfMotionOfDiracFieldIsDiracEquation}  |
| [[electromagnetic field]] | expl. \ref{Electromagnetism} | expl. \ref{ElectromagnetismLagrangianDensity} | expl. \ref{ElectromagnetismEl}  |
| [[Yang-Mills field]] | expl. \ref{YangMillsFieldOverMinkowski}, <br/> expl. \ref{YangMillsFieldInInstantonSector} | expl. \ref{YangMillsLagrangian}  | expl. \ref{YangMillsOnMinkowskiEl} |
| [[B-field]] | expl. \ref{BField} | expl \ref{BFieldLagrangianDensity} | expl. \ref{EulerLagrangeFormBField} |

$\,$

| [[field (physics)|field]] | [[Poisson bracket]]  |  [[causal propagator]] | [[Hadamard propagator]] | [[Feynman propagator]] |
|---------------------------|----|----|-----|-----|
| [[real scalar field]] | expl. \ref{PeierlsBracketEistsForScalarFieldAndDiracField}, <br/> expl. \ref{PoissonBracketForRealScalarField} |  prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski} | def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} | def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}  |
| [[Dirac field]] | expl. \ref{PeierlsBracketEistsForScalarFieldAndDiracField}, <br/>  expl. \ref{PoissonBracketForDiracField}   |  prop. \ref{DiracEquationOnMinkowskiSpacetimeAdvancedAndRetardedPropagators} | def. \ref{HadamardPropagatorForDiracOperatorOnMinkowskiSpacetime} | def. \ref{FeynmanPropagatorForDiracOperatorOnMinkowskiSpacetime} |

$\,$

| [[field (physics)|field]] | [[gauge symmetry]] | [[local BRST complex]] | [[gauge fixing]] |
|---------------------------|--------------------|------------------------|------------------|
| [[electromagnetic field]] | expl. \ref{InfinitesimalGaugeSymmetryElectromagnetism}  | expl. \ref{LocalBRSTComplexForFreeElectromagneticFieldOnMinkowskiSpacetim} |  expl. \ref{NLGaugeFixingOfElectromagnetism}  |
| [[Yang-Mills field]]      |   expl. \ref{InfinitesimalGaugeSymmetryOfYangMillsTheory}      |  expl. \ref{YangMillsLocalBRSTComplex}   | ... |
| [[B-field]]    |   expl. \ref{InfinitesimalGaugeSymmetryOfTheBField} |  expl. \ref{LocalBRSTComplexBFieldMinkowskiSpacetime}  |  ... |

$\,$

The [[electromagnetic field]] and the [[Dirac field]] combined are the [[field (physics)|fields]] of _[[quantum electrodynamics]]_
which we turn to at the end [below](#QED).

$\,$

**Acknowledgement**

These notes profited greatly from discussions with [[Igor Khavkine]].

Thanks also to [[Marco Benini]], [[Klaus Fredenhagen]], [[Arnold Neumaier]], [[Kasia Rejzner]] for helpful discussion.


$\,$
$\,$

#A first idea of quantum field theory#
* table of contents
{:toc}

$\,$

[[!include A first idea of quantum field theory -- Geometry]]

[[!include A first idea of quantum field theory -- Spacetime]]

[[!include A first idea of quantum field theory -- Fields]]

[[!include A first idea of quantum field theory -- Field variations]]

[[!include A first idea of quantum field theory -- Lagrangians]]

[[!include A first idea of quantum field theory -- Symmetries]]

[[!include A first idea of quantum field theory -- Observables]]

[[!include A first idea of quantum field theory -- Phase space]]

[[!include A first idea of quantum field theory -- Propagators]]

[[!include A first idea of quantum field theory -- Gauge symmetries]]

[[!include A first idea of quantum field theory -- Reduced phase space]]

[[!include A first idea of quantum field theory -- Gauge fixing]]

[[!include A first idea of quantum field theory -- Quantization]]

[[!include A first idea of quantum field theory -- Free quantum fields]]

[[!include A first idea of quantum field theory -- Scattering]]

[[!include A first idea of quantum field theory -- Quantum observables]]

[[!include A first idea of quantum field theory -- Feynman diagrams]]

[[!include A first idea of quantum field theory -- Renormalization]]

[[!include A first idea of quantum field theory -- Quantum electrodynamics]]


[[!redirects A first idea of quantum field theory]]


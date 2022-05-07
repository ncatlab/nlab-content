[[!redirects geometry of physics -- A first idea of quantum field theory]]


<img src="https://ncatlab.org/schreiber/files/HamburgAnnouncement.jpg" width="850" >

These notes ([[Schreiber_pQFT20211103.pdf:file]], 323 pages) mean to give an expository but rigorous introduction to the basic concepts of [[relativistic quantum field theory|relativistic]] [[perturbative quantum field theories]], specifically those that arise as the [[perturbative quantum field theory|perturbative]] [[quantization]] of _[[Lagrangian field theories]]_ -- such as [[quantum electrodynamics]], [[quantum chromodynamics]], and [[perturbative quantum gravity]] appearing in the [[standard model of particle physics]].

$\,$

> This is one chapter of _[[geometry of physics]]_.

> Previous chapters: _[[geometry of physics -- smooth sets|smooth sets]]_, _[[geometry of physics -- supergeometry|supergeometry]]_.

$\,$

#Contents#
* table of contents
{:toc}

$\,$

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
Therefore we concentrate on the special case where [[spacetime]] is [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime} below), where the [[field bundle]] (def. \ref{FieldsAndFieldBundles} below) is an ordinary [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle} below) and hence the [[Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below) is [[locally variational field theory|globally defined]].
Similarly, when considering [[gauge theory]] we consider just the special case that the [[gauge parameter]]-bundle
is a [[trivial vector bundle]]  and we concentrate on the case that the gauge symmetries are "closed irreducible" (def. \ref{GaugeParametersClosed} below).
But we aim to organize all concepts such that the _structure_ of their generalization to [[AQFT on curved spacetime|curved spacetime]]
and non-trivial [[field bundles]] is immediate.

This comparatively simple setup already subsumes what is considered in traditional texts on the subject; it captures the established [[perturbative quantum field theory|perturbative]] [[BV formalism|BRST-BV quantization]] of [[gauge fields]] coupled to [[fermions]] [[AQFT on curved spacetime|on curved spacetimes]]
-- which is the state of the art.
Further generalization, necessary for the discussion of global topological effects, such as [[instanton]] configurations
of [[gauge fields]], will be discussed elsewhere (see at _[[homotopical algebraic quantum field theory]]_).

Alongside the theory we develop the concrete examples of the [[real scalar field]], the [[electromagnetic field]] and the [[Dirac field]]; eventually combining these to a disussion of [[quantum electrodynamics]].

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


| [[field (physics)|field]] | [[Poisson bracket]]  |  [[causal propagator]] | [[Wightman propagator]] | [[Feynman propagator]] |
|---------------------------|----|----|-----|-----|
| [[real scalar field]] | expl. \ref{PeierlsBracketEistsForScalarFieldAndDiracField}, <br/> expl. \ref{PoissonBracketForRealScalarField} |  prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski} | def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} | def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}  |
| [[Dirac field]] | expl. \ref{PeierlsBracketEistsForScalarFieldAndDiracField}, <br/>  expl. \ref{PoissonBracketForDiracField}   |  prop. \ref{DiracEquationOnMinkowskiSpacetimeAdvancedAndRetardedPropagators} | def. \ref{HadamardPropagatorForDiracOperatorOnMinkowskiSpacetime} | def. \ref{FeynmanPropagatorForDiracOperatorOnMinkowskiSpacetime} |
| [[electromagnetic field]]  |  | prop. \ref{PhotonPropagatorInGaussianAveragedLorenzGauge}  |   |  prop. \ref{PhotonPropagatorInGaussianAveragedLorenzGauge}  |


$\,$

| [[field (physics)|field]] | [[gauge symmetry]] | [[local BRST complex]] | [[gauge fixing]] |
|---------------------------|--------------------|------------------------|------------------|
| [[electromagnetic field]] | expl. \ref{InfinitesimalGaugeSymmetryElectromagnetism}  | expl. \ref{LocalBRSTComplexForFreeElectromagneticFieldOnMinkowskiSpacetim} |  expl. \ref{NLGaugeFixingOfElectromagnetism}  |
| [[Yang-Mills field]]      |   expl. \ref{InfinitesimalGaugeSymmetryOfYangMillsTheory}      |  expl. \ref{YangMillsLocalBRSTComplex}   | ... |
| [[B-field]]    |   expl. \ref{InfinitesimalGaugeSymmetryOfTheBField} |  expl. \ref{LocalBRSTComplexBFieldMinkowskiSpacetime}  |  ... |

$\,$

| [[interacting field theory]] | [[interaction]] [[Lagrangian density]] | [[interaction]] [[Wick algebra]]-element |
|------------------------------|------------------------|---------------|
| [[phi^n theory]] | exp. \ref{phintheoryLagrangian} | expl. \ref{InWickAlgebraphinInteraction} |
| [[quantum electrodynamics]] | expl. \ref{LagrangianQED} | expl. \ref{InWickAlgebraElectronPhotonInteraction} | 
$\,$

**References**
 {#References}

Pointers to the literature are given in each chapter, alongside the text. The following is a selection of these references.

The discussion of [[spinors]] in chapter _[2. Spacetime](#Spacetime)_ follows [Baez-Huerta 09](spin+representation#BaezHuerta09).

The [[functorial geometry]] of [[supergeometry|supergeometric]] [[spaces of field histories]] in _[3. Fields](#Fields)_ follows [Schreiber 13](higher+prequantum+geometry#Schreiber13). 

For the [[jet bundle]]-formulation of [[variational calculus]] of [[Lagrangian field theory]] in _[4. Field variations](#FieldVariations)_, and _[5. Lagrangians](#Lagrangians)_ we follow [Anderson 89](variational+bicomplex#Anderson89) and [Olver 86](#Olver86); for _[6. Symmetries](#Symmetries)_ augmented by [Fiorenza-Rogers-Schreiber 13b](#higher+prequantum+geometry#FRS13b).

The identification of [[polynomial observables]] with [[distributions]] in _[7. Observables](#Observables)_ was observed by [Paugam 12](distributions+are+the+smooth+linear+functionals#Paugam12).

The discussion of the [[Peierls-Poisson bracket]] in _[8. Phase space](#PhaseSpace)_ is based on [Khavkine 14](Peierls+bracket#Khavkine14).

The derivation of [[wave front sets]] of [[propagators]] in _[9. Propagators](#Propagators)_ takes clues from [Radzikowski 96](Hadamard+distribution#Radzikowski96) and uses results from [Gelfand-Shilov 66](Cauchy+principal+value#GelfandShilov66).

For the general idea of [[BV-BRST formalism]] a good review is [Henneaux 90](BV-BRST+formalism#Henneaux90).

The [[Lie algebroid]]-perspective on [[BRST complexes]] developed in chapter _[10. Gauge symmetries](#GaugeSymmetries)_, may be compared to [Barnich 10](BRST+complex#Barnich10).

For the [[local BV-BRST complexes|local BV-BRST theory]] laid out in chapter _[11. Reduced phase space](#ReducedPhaseSpace)_ we are following [Barnich-Brandt-Henneaux 00](local+BRST+cohomology#BarnichBrandtHenneaux00).

For the [[gauge fixing|BV-gauge fixing]] developed in _[12. Gauge fixing](#GaugeFixing)_ we take clues from [Fredenhagen-Rejzner 11a](BV-BRST+formalism#FredenhagenRejzner11a).

For the free quantum [[BV-operators]] in _[13. Free quantum fields](#FreeQuantumFields)_ and the interacting [[quantum master equation]] in _[15. Interacting quantum fields](#InteractingQuantumFields)_ we are following [Fredenhagen-Rejzner 11b](BV-BRST+formalism#FredenhagenRejzner11b), [Rejzner 11](BV-BRST+formalism#Rejzner11), which in turn is taking clues from [Hollands 07](BV-BRST+formalism#Hollands07).

The discussion of [[quantization]] in _[13. Quantization](#Quantization)_ takes clues from [Hawkins 04](geometric+quantization+of+symplectic+groupoids#EH), [Collini 16](star+product#Collini16) and spells out the derivation of the [[Moyal star product]] from [[geometric quantization of symplectic groupoids]] due to [Gracia-Bondia & Varilly 94](Moyal+deformation+quantization#GBV).

The perspective on the [[Wick algebra]] in _[14. Free quantum fields](#FreeQuantumFields)_ goes back to [Dito 90](Wick+algebra#Dito90) and was revived for [[pAQFT]] in [Dütsch-Fredenhagen 00](Wick+algebra#DuetschFredenhagen00). The proof of the folklore result that the perturbative [[Hadamard vacuum state]] on the [[Wick algebra]] is indeed a [[state on a star-algebra|state]] is cited from  [Dütsch 18](Wick#algebra#Duetsch18).

The discussion of [[causal perturbation theory]] in _[15. Interacting quantum fields](#InteractingQuantumFields)_ follows the original [Epstein-Glaser 73](causal+perturbation+theory#EpsteinGlaser73). The relevance here of the [[star product]] induced by the [[Feynman propagator]] was highlighted in [Fredenhagen-Rejzner 12](perturbative+algebraic+quantum+field+theory#FredenhagenRejzner12). The proof that the [[interacting field algebra of observables]] defined by [[Bogoliubov's formula]] is a [[causally local net]] in the sense of the [[Haag-Kastler axioms]] is that of [Brunetti-Fredenhagen 00](pAQFT#BrunettiFredenhagen00).  

Our derivation of [[Feynman diagrams|Feynman diagrammatics]] follows [Keller 10, chapter IV](Feynman+diagram#Keller10), our derivation of the [[quantum master equation]] follows [Rejzner 11, section 5.1.3](BV-BRST+formalism#Rejzner11), and our discussion of [[Ward identities]] is informed by [Dütsch 18, chapter 4](Ward+identity#Duetsch18).

In chapter _[16. Renormalization](#Renormalization)_ we take from [Brunetti-Fredenhagen 00](renormalization#BrunettiFredenhagen00) the perspective of [[Epstein-Glaser renormalization]] via [[extension of distributions]] and from [Brunetti-Dütsch-Fredenhagen 09](renormalization#BrunettiDuetschFredenhagen09) and [Dütsch 10](renormalization#Duetsch10) the rigorous formulation of [[Gell-Mann-Low renormalization cocycle|Gell-Mann & Low renormalization group flow]], [[UV-regularization]], [[effective quantum field theory]] and [[Polchinski's flow equation]].




$\,$

**Acknowledgement**

These notes profited greatly from discussions with [[Igor Khavkine]] and [[Michael Dütsch]].

Thanks also to [[Marco Benini]], [[Klaus Fredenhagen]], [[Arnold Neumaier]] and [[Kasia Rejzner]] for helpful discussion.


$\,$


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

[[!include A first idea of quantum field theory -- Interacting quantum fields]]

[[!include A first idea of quantum field theory -- Renormalization]]


[[!redirects A first idea of quantum field theory]]


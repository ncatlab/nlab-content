

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A theory of _quantum gravity_ (QG) is supposed to be a [[quantum field theory]] (QFT) -- or something similar -- that corresponds to the [[classical field theory]] of [[gravity]], possibly by [[quantization]].

The key technical problem with quantum gravity as a [[non-perturbative quantum field theory]] is that all known constructions of QFTs quantize [[field (physics)|fields]] defined _on_ a given [[spacetime]] [[background field|background]], while, in contrast, the field of [[gravity]] _is_ that spacetime. 

Since even for field theories that are defined on space-time backgrounds, such as [[Yang-Mills theory]], [[non-perturbative quantum field theory|non-perturbative]] quantization is a big open problem away from toy examples (for Yang-Mills theory it has been dubbed one of the _Millennium Problems_, see at _[[quantization of Yang-Mills theory]]_) this means that non-perturbative quantum gravity is an even wider open problem.

However, the [[Einstein-Hilbert action]] that defines gravity may be expanded around any of its solutions to the [[Einstein equations]] and the resulting [[perturbation]] of the field of gravity around this background behaves, to low order, like an ordinary [[field (physics)|field]] on a fixed spacetime background. This allows to treat _perturbative quantum gravity_ (pQG) as a [[perturbative quantum field theory]], see the references [below](#ReferencesAsAnEffectiveFieldTheory).


While the [[Einstein-Hilbert action]] (or any of its variants) that defines the dynamics of gravity makes perfect sense at low energies as the definition of an [[effective quantum field theory]] (see there for details), it is not expected to be a non-effective theory at arbitrary high energies, because it is [[renormalizable interaction|not renormalizable]]: all [[non-renormalizable QFTs]] that have appeared in practice turned out to be [[effective QFT]] approximations (see there) to renormalizable [[UV-completions]]. 

The idea has been explored that gravity is simply to be regarded as a [[classical field theory]], but trying to couple such a classical field theory to a [[stress-energy tensor]] of a matter [[quantum field theory]] leads to conceptual problems that break the very foundation of what is known about theoretical physics. The technical problem is this: the [[equations of motion]] of classical Einstein [[gravity]] ([[Einstein's equations]]) assert that the [[Einstein tensor]] of the [[field (physics)]] of [[gravity]] equals the [[energy-momentum tensor]] of all other [[force]] and [[matter]] [[field (physics)|fields]]. Here into the [[energy-momentum tensor]] enters the expression for [[energy]] and [[momentum]] of classical matter fields. However, according to the [[standard model of particle physics]], these matter fields are not described by [[classical field theory]]. This then is the technical problem: there is no consistent way in sight to modify [[Einstein's equations]] so as to have a quantum EM tensor in it. The simple idea of taking the [[expectation value]] of the quantum matter EM-tensor leads to all kinds of theoretical problems.

Thus, this idea seems to be very unlikely. At the same time, it is clear that present experiments cannot _directly_ probe the effects of that supposed [[UV-completion]] of Einstein-gravity.

Approaches to a full quantization of gravity therefore roughly fall into two different strategies

1. One assumes that the Einstein-Hilbert action is indeed the [[effective QFT]] that approximates a "[[UV-completion]]", a more fundamental theory valid at all energies. This is the approach taken for instance in [[string theory]].

1. One assumes that by some other fact that has been overlooked, one can make sense of a non-perturbative quantization of the EH action at arbitrary energies after all. This is for instance the case in speculations that EH-gravity has a [[UV fixed point]].

Accordingly, there are various proposals for what quantum gravity might be, but a comprehensive theory is missing to date. This is in stark contrast to the situation for the other fundamental [[force]]s of the [[standard model of particle physics]]: these are [[Yang-Mills field]]s, whose nature as QFTs is, while subtle, well understood. Indeed, the theoretical and experimental sucess of [[Yang-Mills theory]] is the main reason for the belief that QFT is the right framework for fundamental physics, and that also the field of gravity must have a description in this form. 

Indeed, a model of fundamental physics where Yang-Mills fields are quantized but gravity is not is incomplete and arguably even inconsistent. Central motivating examples for this come from [[black hole]]-physics:

1. The study of quantum fields on the classical gravitational background of a [[black hole]] [[spacetime]] suggest that in a full theory of quantum gravity black holes could be shown to emit radiation and to eventually even decay in some way or other. This expected decay process cannot be described without a theory of quantum gravity.

1. Related to black hole radiation is a whole series of observations in classical [[general relativity]] that seem to indicate that black holes need to be thought of as systems possessing physical microstates with an [[entropy]] that cannot be accounted for by classical general relativity. This has led to the expectation that these microstates are states in quantum theory of gravity and that their understanding is necessary for understanding the physics of black holes.

1. More generally, appearances of unphysical singularities in [[general relativity]], such as in [[black hole]]s or [[cosmology|cosmological]] singularities such as the [[big bang]], have been argued to be artefacts of a non-quantum description of gravity. Various toy models of quantum gravity have been proposed where notably the big-bang singularity is just a classical approximation to a non-singular and well-defined quantum dynamics.

An evident definition of quantum gravity would seem to simply be the [[quantization]] of the [[Einstein-Hilbert action]] by the rules [[perturbation theory]] and [[renormalization]]. This straightforward approach however fails, as it can be demonstrated that this [[action functional]] is not [[renormalization|renormalizable]]. 

More recently it has been argued that there is evidence that the EH-action has a nontrivial [[UV-fixed point]] after all. If true this would mean that a quantization of gravity in standard QFT is possible.

Another possibility is that this is only an apparent problem, and that standard gravity is nothing but an [[effective quantum field theory]]. (See there for references on gravity).

But most approaches to the problem have taken the non-renormalizability of classical gravity to be an indication that the standard concepts of QFT might need refinement in order to include gravity. 

A common idea is that the assumption that the space of configurations in gravity is really that of smooth [[spacetime]]s, i.e. of [[smooth manifold]]s, is wrong. A plethora of variants of the notion of smooth manifold have been proposed as ingredients for a theory of quantum gravity. Notably concepts in [[noncommutative geometry]]. For instance [[Alain Connes]]'s [[spectral action]] generalizes the [[Einstein-Hilbert action]] functional from [[Riemannian manifold]]s to [[spectral triple]]s. However, none of the modifications of the spaces of configuratations of gravity proposed so far have been shown to support action functionals that can actually be quantized, in one sense or another.

Accordingly there are suggestions to modify instead the principles of perturbative quantum field theory. In [[string theory]] the fundamental assumption is that the Feynman perturbation series over 1-dimensional graphs of traditional perturbative QFT is to be refined by a similar series over 2-dimensional surfaces. It has been shown that this _string perturbation series_ needs no renormalization and that it does describe Yang-Mills fields and a gravitational field. This led to huge hopes and large activity in the study of string theory as a theory of quantum gravity. But various central questions remain open and the state of the theory remains somewhat inconclusive.

While perturbative string theory did demonstrate that there is a variant of the perturbation series for gravity which is renormalized, it can, by definition of perturbation theory, be just an approximation to a more fundamental non-perturbatively defined theory. Various candidates for the non-perturbative theory to which the string perturbation series might be an approximation have been proposed. One that enjoyed a large popularity in the 1990s was called _matrix mechanics_ but the high hopes connected with it were supported mostly by toy example computations. More recently the [[AdS/CFT correspondence]] is widely thought of as providing a non-perturbative definition of string theory and of quantum gravity. This correspondence asserts that observables of a string theory on an asymptotically [[anti-de Sitter spacetime]] may be matched equivalently to certain observables in an auxiliary super [[Yang-Mills theory]]. If true, this would allow to take the well understood non-perturbative definition of Yang-Mills theory and deduce from it a theory of quantum gravity. 

Still another suggestion has been that ordinary quantum field theory might be seen to apply to the ordinary configuration space and action functional of general relativity, if only a suitably adapted parameterization of the configuration space is chosen. Notably one observes that [[Riemannian manifold]]s may be encoded in terms of [[connection on a bundle|connections on the tangent bundle]] -- the [[Levi-Civita connection]] -- this being manifestly analogous to the nature of the fields in [[Yang-Mills theory]]. (See [[first-order formulation of gravity]]).

It has been suggested that therefore quantum gravity may have a description in terms of the [[holonomy]]-observables of these connections,  their [[parallel transport]] around loops. Research in this direction has therefore become known as _loop quantum gravity_ . However, little progress has been made in understanding the configuration space of smooth connections in terms of loop observables. In most of the LQG-literature instead it is assumed from the outset that it makes sense to pass to _generalized connections_ : while a smooth connection is the same as a smooth [[parallel transport]]-[[functor]] on the [[path groupoid]] $\mathbf{P}_1(X) \to \mathbf{B}G$, the "generalized connections" in this context are taken to be non-smooth and non-continuous such functors on sub-categories of paths. It is is not clear how this configuration space relates to that of ordinary gravity.

A plethora of further suggestions has developed out of this, which in the literature often still go under the name "LQG", even though they may abandon the description of configuration spaces of metrics in terms of loop observables. There is for instance the approach of _spin foams_ or _[[causal dynamical triangulations]]_, and that of _[[causets]]_ , to name just a few.

The problem with discriminating between all these proposals is the combination of two problems.

1. There exist insufficient theoretical tools for analyzing in detail the consequences of the various proposals.

1. There are few to no experiments available that would be able to observe the phenomena that a theory of quantum gravity is supposed to describe.

As a result, the field of fundamental physics today finds itself in a somewhat awkward position where the need for theoretical progress concerning quantum gravity for conceptual reasons is widely appreciated, but where disagreements about the viability of various proposals finds no conclusive resolution and divides the community. 
 
## Effects

### First quantum correction to Newtonian $1/r$-potential
 {#FirstQuantumCorrectionToNewtonianPotential}

The first order quantum correction to the classical gravitational potential

$$
  V_{cl}(r) \;=\; - \frac{G m_1 m_2}{r} 
$$

between two bodies of [[mass]] $m_1$, $m_2$, respectively, may be computed unambiguously in [[perturbative quantum field theory|perturbative]] quantum gravity ([Donoghue 95, Section 9](#Donoghue95)):

The result is a term of the form

$$
  V_{qu}(r) 
  \;=\; 
  V_{cl}(r)
  \left( 
    1
    - \frac{135 + 2 N_\nu}{ 30 \pi^2}
    \frac{G \hbar}{r^2 c^2}
    +
    \text{higher order}
  \right)
$$

(where $N_\nu$ is the [[natural number|number]] of [[mass|massless]] [[neutrino]]-species, $G$ is the [[gravitational constant]], $c$ is the [[speed of light]] and $\hbar$ is [[Planck's constant]]).

([Donoghue 95, (65)](#Donoghue95)

Here for $r = 1$ [[fm]] we have that the quantum correction is by a tiny factor of order

$$
  \frac{G \hbar}{r^2 c^2}\vert_{r = 1 fm}
  \;\sim\;
  10^{-38}
  \,.
$$

### Vacuum energy and Cosmological constant

The [[renormalization]] freedom in [[perturbative QFT|perturbative]] [[quantization]] of gravity induces freedom in the choice of [[vacuum expectation value]] of the [[stress-energy tensor]] and hence in the [[cosmological constant]]. 

For details see [there](cosmological+constant#InPerturbativeQuantumGravity).

### Anomalous magnetic moment of the leptons
 {#CorrectionToAnomalousMagneticMomentOfTheLeptons}

The corrections of [[loop order|1-loop]] [[perturbative QFT|perturbative]] quantum gravity to the [[anomalous magnetic moment]] of the [[electron]] and the [[muon]] have been computed in ([Berends-Gastman 75](#BerendsGastman75)) and found to be finite, without need for [[renormalization]]. These [[Feynman diagrams]] contribute:

<img src="https://ncatlab.org/nlab/files/GravityVertexCorrectionsForQED.png" width="750">


## Special cases

* [[2d quantum gravity]]

* [[3d quantum gravity]]


## Related concepts

* [[soft graviton theorem]]:

* [[asymptotic safety]]

* [[weak gravity conjecture]]

* [[Witten conjecture]]

* [[piecewise flat spacetime]]

## References

### General

Some of the standard lore about necessity of and the problems of quantum gravity are discussed in reviews such as

* [[Steve Carlip]], _Quantum Gravity: a Progress Report_ ([arXiv:gr-qc/0108040](http://arxiv.org/abs/gr-qc/0108040))

* [[Richard Woodard]], _How Far Are We from the Quantum Theory of Gravity?_ ([arXiv:0907.4238](http://arxiv.org/abs/0907.4238))

* [[Hermann Nicolai]], _Quantum Gravity: the view from particle physics_ ([arXiv:1301.5481](http://arxiv.org/abs/1301.5481))

* [[Steven Carlip]], Dah-Wei Chiou, Wei-Tou Ni, Richard Woodard, _Quantum Gravity: A Brief History of Ideas and Some Prospects_, Int. J. Mod. Phys. D  ([arXiv:1507.08194](http://arxiv.org/abs/1507.08194))

Exposition from the point of view of [[worldline formalism]] is in

* {#Witten11} [[Edward Witten]], _Quantum Gravity_, Solomon Lefschetz Memorial Lecture Series, November 2011 ([video](https://www.youtube.com/watch?v=uRdCJMYc2Ds#t=15))

Textbook account:

* Claus Kiefer, _Quantum Gravity_, Oxford University Press 2007 ([doi:10.1093/acprof:oso/9780199585205.001.0001](https://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780199585205.001.0001/acprof-9780199585205))

### As a perturbative quantum field theory
 {#ReferencesAsAnEffectiveFieldTheory}

As a [[perturbative quantum field theory]], quantum gravity exists (usually thought of as an [[effective quantum field theory]]):

* {#Feynman63} [[Richard Feynman]], _Quantum theory of gravitation_, Acta Phys.Polon. 24 (1963) 697-722 ([spire:9148](http://inspirehep.net/record/9148/))

* [[Martinus Veltman]], _Quantum theory of Gravitation_, In Les Houches 1975, Proceedings, Methods In Field Theory, (Amsterdam 1976) 265-327 ([[VeltmanQuantumnGravity76.pdf:file]], [spire](http://inspirehep.net/record/105735?ln=en))

* {#Donoghue95} [[John Donoghue]], _Introduction to the Effective Field Theory Description of Gravity_ ([arXiv:gr-qc/9512024](http://arxiv.org/abs/gr-qc/9512024), [spire](http://inspirehep.net/record/403510))

* [[Zvi Bern]], _Perturbative Quantum Gravity and its Relation to Gauge Theory_, Living Rev Relativ. 2002; 5(1): 5. ([arXiv:gr-qc/0206071](https://arxiv.org/abs/gr-qc/0206071), [doi:10.12942/lrr-2002-5](https://dx.doi.org/10.12942%2Flrr-2002-5))

Review and outlook includes

* [[Richard Woodard]], _Perturbative Quantum Gravity Comes of Age_,  International Journal of Modern Physics DVol. 23, No. 09, 1430020 (2014) ([arXiv:1407.4748](https://arxiv.org/abs/1407.4748))

A brief survey of the relevant mathematical issues with more pointers to the literature is in

* [[Igor Khavkine]], _Gravity: an exercise in quantization_, talk at _Quantum Gravity in Perspective_, Munich, 31 May 2013 ([pdf slides](http://www.science.unitn.it/~khavkine/khavkine-munich.pdf), [video](https://www.youtube.com/watch?v=G5O9RKmXyfM#t=2444))
 
The rigorous construction via [[causal perturbation theory]] of quantum gravity  as a [[perturbative quantum field theory]] around [[Minkowski spacetime]] is spelled out in

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

The generalization of this to perturbation about [[AQFT on curved spacetimes|curved spacetimes]] is discussed via [[locally covariant perturbative algebraic quantum field theory]] in

* {#BrunettiFredenhagenRejzner13} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Quantum gravity from the point of view of locally covariant quantum field theory_, Communications in Mathematical Physics August 2016, Volume 345, Issue 3, pp 741–779 ([arXiv:1306.1058](http://arxiv.org/abs/1306.1058))

and with applications to [[cosmology]] in

* {#BFHPR16} [[Romeo Brunetti]], [[Klaus Fredenhagen]], Thomas-Paul Hack, [[Nicola Pinamonti]], [[Katarzyna Rejzner]], _Cosmological perturbation theory and quantum gravity_, Journal of High Energy Physics August 2016:32 ([arXiv:1605.02573](https://arxiv.org/abs/1605.02573))

Corrections at [[loop order|1-loop]] from [[quantum gravity]] to the [[anomalous magnetic moment]] of the [[leptons]] are discussed in

* {#BerendsGastman75} F. A. Berends, R. Gastmans, _Quantum gravity and the electron and muon anomalous magnetic moment_, Phys. Lett. B55 Issue 3 Feb 1975 311-312 (<a href="doi.org/10.1016/0370-2693(75)90608-5">doi:10.1016/0370-2693(75)90608-5</a>)

and adapted to [[supergravity]] in

* F. del Aguila, A. Culatti, R. Munoz-Tapia, M. Perez-Victoria, _Supergravity corrections to $(g-2)_l$ in differential renormalization_, Nuclear Physics  B  504  (1997)  532-550 ([arXiv:hep-ph/9702342](https://arxiv.org/abs/hep-ph/9702342))

Concrete discussion of [[graviton]] [[scattering amplitudes]]:

* S. Abreu, F. Febres Cordero, H. Ita, M. Jaquier, B. Page, M. S. Ruf, V. Sotnikov, _The Two-Loop Four-Graviton Scattering Amplitudes_ ([arXiv:2002.12374](https://arxiv.org/abs/2002.12374))

With an emphasis on the [[S-matrix]]-perspective:

* [[Pierre Vanhove]], *S-matrix approach to general gravity and beyond* ([arXiv:2104.10148](https://arxiv.org/abs/2104.10148))


For more discussion of perturbative [[supergravity]] see at 

* _[N=8 perturbative quantum gravity](4-dimensional+supergravity#PerturbativeQuantumSupergravityN8)_

* _[[KLT relations]]_

* _[[string theory results applied elsewhere]]_.

### Non-renormalizablity
 {#ReferencesNonRenormalizability}

That pure [[Einstein gravity]] is not perturbatively [[renormalizable interaction|renormalizable]] at [[loop order|2-loops]] was shown in 

* {#GoroffSagnotti85} M. H. Goroff, A. Sagnotti, _Quantum Gravity At Two Loops_, Phys. Lett. B 160 (1985) 81.

* {#vandeVen92} A. E. M. van de Ven, _Two loop quantum gravity_, Nucl. Phys. B 378 (1992) 309.

For generic matter couplings this applies already at [[loop order|1-loop]]:

* [[Gerard 't Hooft]], [[Martinus Veltman]], Annales Poincare Phys. Theor. A 20 , 69 (1974)

* [[Gerard 't Hooft]], Nucl. Phys. B 62, 444 (1973);

* [[Stanley Deser]], [[Peter van Nieuwenhuizen]], Phys. Rev. D 10, 401 (1974);

* [[Stanley Deser]], H. S. Tsao and [[Peter van Nieuwenhuizen]], Phys. Rev. D 10 , 3337 (1974)

If the matter coupling is such as to make the theory [[supersymmetry|supersymmetric]] ([[supergravity]]), the divergence appears only in higher [[loop order]].

That it appears earliest at 3-loops was established in

*  M. T. Grisaru, Phys. Lett. B 66, 75 (1977);

* E. T. Tomboulis, Phys. Lett. B67, 417 (1977);

* [[Stanley Deser]], J. H. Kay and [[Kellogg Stelle]], Phys. Rev. Lett. 38, 527 (1977);

* [[Renata Kallosh]], Phys. Lett. B99, 122 (1981);

* [[Paul Howe]], [[Kellogg Stelle]] and [[Paul Townsend]], Nucl. Phys. B 236, 125 (1984).

Specifically for [[N=8 d=4 supergravity]] there is evidence that it might be finite at all loops. See the references [there](4-dimensional+supergravity#PerturbativeQuantumSupergravityN8).

### From string field theory

Derivation of [[graviton]]-[[scattering amplitudes]] from [[string field theory]]:

* [[Taejin Lee]], _Gravitational Scattering Amplitudes and Closed String Field Theory in the Proper-Time Gauge_, EPJ Web of Conferences 168, 07004 (2018) ([doi:10.1051/epjconf/201816807004](https://doi.org/10.1051/epjconf/201816807004))

* [[Taejin Lee]], _Four-Graviton Scattering and String Path Integral in the Proper-time gauge_ ([arXiv:1806.02702](https://arxiv.org/abs/1806.02702))

### Local Gauging of global symmetries


It is being argued that after embedding into consistent [[quantum gravity]], all [[global symmetries]] must become [[local symmetries]].

A substantiation of this argument via [[AdS/CFT]] is given in

* [[Daniel Harlow]], [[Hirosi Ooguri]], _Symmetries in quantum field theory and quantum gravity_ ([arXiv:1810.05338](https://arxiv.org/abs/1810.05338))

* [[Daniel Harlow]], [[Hirosi Ooguri]], _Constraints on symmetry from holography_, Phys. Rev. Lett. 122, 191601 (2019) ([arXiv:1810.05337](https://arxiv.org/abs/1810.05337))

See also:


* Sylvain Fichet, Prashant Saraswat, _Approximate Symmetries and Gravity_ ([arXiv:1909.02002](https://arxiv.org/abs/1909.02002))


[[!redirects perturbative quantum gravity]]

[[!redirects pQG]]

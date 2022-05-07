
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Fields and quanta
+-- {: .hide}
[[!include fields and quanta - table]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[field (physics)|field]] of [[quantum field theory]] started out as a description of the [[fundamental particles]] that are observed in [[experiment]], such as [[electrons]] and [[photons]].

However, even so, abstractly the formalization of the concept of _particle_ within [[QFT]]s is somewhat subtle.

If the quantum field theory is on [[Minkowski space]] and comes with a [[Hilbert space|Hilbert]] [[space of states]] on which thus the  [[Poincare group]] of translations, rotations and boosts in Minkowski space acts, the massive _particle_ excitations of the theory can be found in the discrete spectrum of the time translation operator as the [[irreducible representation|irreducible]] [[unitary representations of the Poincare group]].
For QFTs on [[curved spacetime|curved]] [[spacetimes]] the situation is more subtle.

Often, however, QFTs are considered as [[quantizations]] of given [[Lagrangians]]. In these cases one often identifies their particle content with that explicitly encoded by the Lagrangian. Notably when that arises from [[second quantization]] of some 1-dimensional [[sigma-model]], the particles of the theory are those described by these sigma-models.

## What is a particle?
 {#WhatIsAParticle}

The fundamental concept of modern [[physics]] is that of [[quantum field theory]] (QFT); the concept of particle is derived from that, and need not make sense in every case. ("That's why it's called 'field theory'.")


 In the perspective of the [[Schrödinger picture]], a $(d+1)$-dimensional [[QFT]] is given by a [[functor]] $Z$ on a [[category of cobordisms]] (possibly with [[geometry|geometric]] structure, such as [[pseudo-Riemannian metric]] structure) between $d$-dimensional [[manifolds]] ("[[FQFT]]"). It is crucial to notice that one such QFT always has **two different interpretations**:

1. a [first quantized worldvolume perspective](#FirstQuantizedPerspective);

1. a [second quantized spacetime perspective](#SecondQuantizedSpacetimePerspective).

### First quantized worldvolume perspective
 {#FirstQuantizedPerspective}

If we think of a $d$-dimensional manifold as the shape of a some quantum object -- (as such commonly called a $d$-[[brane]]) -- then a [[cobordism]] between two such is thought of as a piece of [[worldvolume]], a way for parts of such an object to interact with other parts. From this perspective the functor $Z$ assigns to a manifold the [[space of quantum states]] that the [[brane]] of this shape may have, and to a [[cobordism]] the linear map which is the time evolution along the cobordism.

 Here if $d = 0$ then the [[brane]] is a "0-brane" and this is a "particle" (or [[D0-brane]]), the worldvolume is the "[[worldline]]" and the QFT encodes the [[worldline theory]] of the particle, its [[quantum mechanics]].

 If instead $d = 1$ then the brane is a 1-brane, for instance a [[string]] of [[D1-brane]], if $d = 2$ then the brane is a 2-brane also called a [[membrane]], and so on.

Given this, one may try to see if this data describes a brane propagating _in_ some [[spacetime]] (the "[[target space]]" of the brane). It is the topic of [[spectral geometry]] (in the sense of [[Alain Connes]]'s) to try to reconstruct from this data the would-be target spacetime that the brane is propagating in. For instance for $d = 0$ the data of a QFT in this sense here is a [[spectral triple]] and [[noncommutative geometry]] provides a general way to make sense of the target space of the particle. If $d =1$ the QFT data here is that of a [[2-spectral triple]], and so on.

### Second quantized perspective 
 {#SecondQuantizedSpacetimePerspective}

On the other hand, we may think of the $d+1$-dimensional [[cobordisms]] here themselves already as [[spacetimes]]. In this case the QFT describes [[field (physics)|fields]] on spacetime. In favorable circumstances this can arise from the previous case by a process of [[second quantization]], meaning that these fields may be thought of as [[condensates]] of branes/particles in the previous sense. Conversely one says that these particles are the _quanta_ of the fields that we start with.

But generally, given a QFT in this perspective, to extract from it the particle content that it comes from under [[second quantization]] is subtle. One of the common definitions of particle quanta only applies to non [[general covariance|generally-covariant]] [[free field theories]] (e.g. [Haag 92, section VI](#Haag92)). This means that already for quantum field theory on a fixed [[curved spacetime]] there is in general no longer any concept of particle-quanta of the fields. This situation would only become worse were one to think of the given QFT as incorporating also [[quantum gravity]]. The concept of [[field (physics)|field]] here is fundamental, that of particle quanta is not. 

### Mixed perspectives

Since the formalism of [[FQFT]] does not "know" whether we want to think of a given QFT as a [first-quantized worldvolume theory](#FirstQuantizedPerspective) or as a [second quantized spacetime theory](#SecondQuantizedSpacetimePerspective) in general both perspectives may be sensible at the same time. 

This is indeed so, but of course this mixing only becomes relevant once one really dares to consider higher-dimensional [[branes]] in the first place, hence in [[string theory]].

Indeed, [[perturbative string theory]] is all set up this way: one starts with a 2-dimensional QFT which one thinks of as the first-quantized [[worldsheet]] theory of a [[string]]. But this means that one may start to ask which "particles" propagate "on the worldvolume". Notably the "embedding fields" of the string [[sigma-model]] which describes how its worldsheet sits in [[spacetime]] look, from the perspective of the worldsheet theory, like [[scalar fields]]. Their [[superpartners]] look like [[fermion]] fields. If one considers the string worldsheet before gravitational [[gauge fixing]] then there is also a [[graviton]] on the worldsheet, and so on.

Hence in general one may want to/need to consider an intricate pattern of "branes withing branes". For instance the [[worldsheet]] [[gravity]] of the [[string]] may itself arises from quantizing other strings for which that worldsheet is target spacetime ([[world sheets for world sheets|Green 87]]).

## Examples

### Particles and non-particles in 3d TQFT
 {#ParticlesAndNonParticlesIn3dTQFT}

We consider a [[QFT]] which is a [[3d TQFT]] of [[Chern-Simons theory]] type and discuss some aspects of the notion of _particle_ in that context.

Assume for the sake of argument that we agree to think of the 3d TQFT here as a realization of [[3d quantum gravity]], as indicated there.  Then this means that as an [[FQFT]] the system assigns to every closed [[surface]] a [[space of quantum states]] to be thought of as the space of states of the [[observable universe]] in that 2+1-dimensional world. A state in here encodes the field of [[gravity]]. It would be somewhat subtle to extract from just the [[FQFT|functorial]] [[3d TQFT]] here the intrinsic notion of particle-quanta. In general, given an [[TQFT]] in the form of an [[FQFT]], there is essentially no established way to going about determining what the particle-quanta would be that an observer "in this universe" would see.

In fact, an argument due to ([Witten 92](A-model#Witten92)) says that if [[Chern-Simons theory]] [[3d TQFT]] is the [[second quantization]] of anything, then it is not of particles but of [[topological strings]] ([[A-model]]). See also ([Costello 06](A-model#Costello06)) and see at _[TCFT -- Worldsheet and effective background theories](TCFT#ActionFunctionals)_ for more on this.

Beware, again, that this concerns the quanta for the fields of the QFT regarded as a QFT on a 2+1-dimensional [[spacetime]]. However we may change perspective and instead think of the [[3d TQFT]] here as a first-quantized [[worldvolume]] [[theory (physics)|theory]]. As such it would be a [[membrane]] [[theory (physics)|theory]], often called the _[[topological membrane]]_, naturally.

Now if we allow [[boundaries]] of [[worldvolume]], hence consider an [[extended TQFT]] with its [[boundary field theory]], then the boundary theory is a 1+1-dimensional worldsheet theory, hence describes a [[string]]. This way of how a first quantized [[string]] can arise as the [[boundary field theory]] of a first-quantized [[topological membrane]] is an instance of the "[[holographic principle]]" known as _[[AdS3-CFT2 and CS-WZW correspondence]]_.

Moreover, going further up in [[codimension]], the [[3d TQFT]] may have [[defect field theory|defects]] of codimension 2, hence have inside it a 0+1-dimensional [[defect field theory]]. This hence may be thought of as a first-quantized particle. (Notice that it is a _first quantized_ particle, not a quantum of a field of the 3d theory regarded as a spacetime theory, for these particles-as-quanta do not have worldlines given by cobordisms,only their first quantized avatars do, but they are not the first quantized 1d defect theory considered now.)

Indeed, these first quantized codim-2-defects/0-branes/1d-particles in [[Chern-Simons theory]] are famous as having "[[Wilson line]] [[worldline theory]]". See at _[orbit method -- Nonabelian charged particle trajectories](orbit%20method#GaugeAndGravityWilsonLoops)_ for details on their incarnation as [[prequantum field theory]]. After [[quantization]] these first quantized 0-branes/1d-particles are famously represented in the [[Reshetikhin-Turaev construction]] as ribbon lines labeled by [[objects]] in a [[modular tensor category]].

In conclusion, given a [[3d TQFT]] regarded as [[quantum gravity]] of 2+1-dimensional [[spacetimes]], it is at best subtle to extract from it particles in the sense of "quanta of the fields of the spacetime field theory", while extracting from it first quantized codim-2 [[defect field theory|defect]] 0-[[branes]] is a famous step in [[Chern-Simons theory]].





## Related concepts

* [[sigma-model]]

* [[worldline]], [[worldline theory]]

* [[non-relativistic particle]]

* [[relativistic particle]], [[spinning particle]], [[superparticle]]

* [[virtual particle]], [[antiparticle]]

* [[fundamental particle]], [[standard model of particle physics]]

* [[matter]], [[force]]

* [[brane]], [[string]], [[membrane]]

* [[mechanics]]

* [[vacuum]]

## References
 {#References}

Chapter VI of 

* {#Haag92} [[Rudolf Haag]], _[[Local Quantum Physics]]_ (1992)
 

discusses how to extract notions of particles from a [[local net of observables]] satisfying the [[Haag-Kastler axioms]].

Further discussion of subtleties of the definition of particles _in_ (non-[[free field theory|free]]) [[quantum field theories]]:

* {#Bain00} [[Jonathan Bain]], _Against particle/field duality: Asymptotic particle states and interpolating fields in interacting QFT (or: Who's afraid of Haag's theorem)_, Erkenntnis 53: 375&#8211;406, 2000  ([pdf](http://faculty.poly.edu/~jbain/papers/lsz.pdf))
 
* Benjamin H. Feintzeig, Jonah Librande, Rory Soiffer, *Localizable Particles in the Classical Limit of Quantum Field Theory* ([arXiv:2104.06442](https://arxiv.org/abs/2104.06442))


[[!redirects particles]]

[[!redirects quantum]]
[[!redirects quanta]]
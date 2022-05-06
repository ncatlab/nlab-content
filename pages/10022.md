
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Holographic entanglement entropy refers to the expression of [[entanglement entropy]] of [[quantum field theories]] expressed "holographically" via a version of [[AdS-CFT duality]] in terms of the [[geometry]] of a higher-dimensional [[bulk]] [[spacetime]]

### Ryu-Takayanagi formula
 {#RyuTakayanagiFormula}

For [[quantum field theories]] that are exhibited as [[boundary field theories]] on the [[asymptotic boundary]] $A$ of an approximately [[anti de Sitter spacetime]] via some approximation to [[AdS-CFT duality]] (for instance for [[QCD]] via [[AdS-QCD duality]]) their [[entanglement entropy]] of a given [[bounded set|bounded domain]] $B\subset A$ turns out to be proportional to the [[area]] of the minimal-area [[surface]] inside the [[bulk]] spacetime that has the same [[boundary]] $\partial B$ (see [Nishioka-Ryu-Takayanagi 09 (3.3)](#NishiokaRyuTakayanagi09) for review of the formula and [Lewkowycz-Maldacena 13](#LewkowyczMaldacena13) for a conceptual explanation). 

<center>
<img src="https://ncatlab.org/nlab/files/RyuTakayanagiFormula.jpg" width="520"></a>
</center>

> graphics grabbed from [Nishioka-Ryu-Takayanagi 09](#NishiokaRyuTakayanagi09)

This relation is known as the _Ryu-Takayanagi formula_ ([Ryu-Takayanagi 06a](#RyuTakayanagi06a), [Ryu-Takayanagi 06b](#RyuTakayanagi06b)) for holographic computation of entanglement entropy, or _holographic entanglement entropy_, for short.

This is a generalization of the proportionality of [[black hole entropy]] to the area of its [[event horizon]]. Indeed, [[AdS-CFT duality]] applies to the [[near horizon geometry]] of [[black branes]], the higher-dimensional generalizations of [[black holes]] and reduces 4d black holes under suitable [[KK-compactification]] (see also at _[[black holes in string theory]]_)

<center>
<img src="https://ncatlab.org/nlab/files/RyuTakayanagiBlackHoleEntropy.jpg" width="500"></a>
</center>

> graphics grabbed from [Nishioka-Ryu-Takayanagi 09](#NishiokaRyuTakayanagi09)

In fact quantum corrections to the [[black hole entropy]] in the presence of matter fields is equal to the [[entanglement entropy]]. ([Ryu-Takayanagi 06a, p. 13](#RyuTakayanagi06a))

Various properties of [[entanglement entropy]] find immediate geometric interpretations this way, for instance subadditivity

<center>
<img src="https://ncatlab.org/nlab/files/RyuTakayanagiSubadditivity.jpg" width="500"></a>
</center>

> graphics grabbed from [Nishioka-Ryu-Takayanagi 09](#NishiokaRyuTakayanagi09)


### Emergence of bulk spacetime from boundary information theory

Further discussion of implications of the Ryu-Takayanagi formula in [van Raamsdonk 10](#vanRaamsdonk10) suggested that the logic may also be turned around: Instead of computing [[entanglement entropy]] of a given [[boundary field theory]] from known [[bulk]] [[geometry]], conversely the [[bulk]] [[spacetime]] may be reconstructed from knowledge of the [[entanglement entropy]] of a boundary field theory.

Talking this perspective to the extreme suggests a description of [[bulk]] [[spacetimes]] entirely in terms of [[information theory]]/[[entanglement]]-relations of a boundary [[QFT]] ("tensor networks", [Swingle 12](#Swingle12), and quantum error correction codes [ADH 14](#ADH14), [PYHP 15](#PYHP15), see [Harlow 18](#Harlow18) for review).


<center>
<img src="https://ncatlab.org/nlab/files/BlackHoleTensorNetwork.jpg" width="500"></a>
</center>

> graphics grabbed from [Harlow 18](#Harlow18)

<center>
<img src="https://ncatlab.org/nlab/files/AdSRindlerTensorNetwork.jpg" width="500"></a>
</center>

> graphics grabbed from [Harlow 18](#Harlow18)

In this context the Ryu-Takayanagi formula for holographic entanglement entropy ([above](#RyuTakayanagiFormula)) has an exact proof [PYHP 15, Theorem 2](#PYHP15).

## Related concepts

* gravitational entropy

  * [[Bekenstein-Hawking entropy]]

  * [[generalized second law of thermodynamics]]

  * [[black holes in string theory]]

* [[p-adic AdS-CFT]]


## References
 {#References}

The original article are

* {#RyuTakayanagi06a} [[Shinsei Ryu]], [[Tadashi Takayanagi]], _Holographic Derivation of Entanglement Entropy from AdS/CFT_, Phys. Rev. Lett. 96:181602, 2006 ([arXiv:hep-th/0603001](https://arxiv.org/abs/hep-th/0603001))

* {#RyuTakayanagi06a} [[Shinsei Ryu]], [[Tadashi Takayanagi]], _Aspects of Holographic Entanglement Entropy_, JHEP 0608:045, 2006 ([arXiv:hep-th/0605073](https://arxiv.org/abs/hep-th/0605073))

A proposal for a conceptual explanation is made in 

* {#LewkowyczMaldacena13} Aitor Lewkowycz, [[Juan Maldacena]], _Generalized gravitational entropy_, J. High Energ. Phys. (2013) 2013: 90 ([arXiv:1304.4926](https://arxiv.org/abs/1304.4926))

Review is in

* {#NishiokaRyuTakayanagi09} Tatsuma Nishioka, [[Shinsei Ryu]], [[Tadashi Takayanagi]], _Holographic Entanglement Entropy: An Overview_, J.Phys.A42:504008,2009 ([arXiv:0905.0932](https://arxiv.org/abs/0905.0932))

Survey talks include

* Meyers, _Holographic entanglement entropy_,  ([pdf slides](http://www.lpt.ens.fr/IMG/pdf/Myers.pdf))

* Shinsei Ryu, _Holographic geometry in Entanglement Renormalization_ ([pdf slides](http://icmt.illinois.edu/Workshops/JointWorkshopPerimeter/Ryu-PI-ICMT-2012.pdf))

* Juan Jottar, _(Entanglement) Entropy in three-dimensional higher spin theories_ ([pdf slides](http://www.hip.fi/holograv13/talk_folder/Jottar-HologravWorkshop-March2013.pdf))

* Matthew Headrick, _Entanglement entropies in holographic field theory_ ([pdf slides](http://www.ggi.fi.infn.it/talks/talk1853.pdf))

* Tadashi Takayanagi, _Entanglement Entropy and Holography (Introductory review)_ ([pdf slides](http://www.princeton.edu/~jmaciejk/entanglement2012/slides/TakayanagiPCTS2012.pdf))

An influential argument that this relation implies that [[entanglement]] in the boundary theory is what makes spacetime as such appear in the bulk theory is due to

* {#vanRaamsdonk10} [[Mark Van Raamsdonk]], _Building up spacetime with quantum entanglement_, Gen.Rel.Grav.42:2323-2329,2010; Int.J.Mod.Phys.D19:2429-2435,2010 ([arXiv:1005.3035](https://arxiv.org/abs/1005.3035)) 

* [[Mark Van Raamsdonk]], _Building up spacetime with quantum entanglement II: It from BC-bit_ ([arXiv:1809.01197](https://arxiv.org/abs/1809.01197))

Review is in 

* [[Mark Van Raamsdonk]], _Lectures on Gravity and Entanglement_, chapter 5 in  New Frontiers in Fields and Strings
TASI 2015 Proceedings of the 2015 Theoretical Advanced Study Institute in Elementary Particle Physics 2015 Theoretical Advanced Study Institute in Elementary Particle Physics ([arXiv:1609.00026](https://arxiv.org/abs/1609.00026))

Development of this idea in terms of [[tensor networks]] is due to 

* {#Swingle12} Brian Swingle, _Constructing holographic spacetimes using entanglement renormalization_ ([arXiv:1209.3304](https://arxiv.org/abs/1209.3304))

and further in terms of quantum error correcting codes due to 

* {#ADH14} Ahmed Almheiri, Xi Dong, Daniel Harlow, _Bulk Locality and Quantum Error Correction in AdS/CFT_, JHEP 1504:163,2015 ([arXiv:1411.7041](https://arxiv.org/abs/1411.7041))

* {#PYHP15} Fernando Pastawski, Beni Yoshida, [[Daniel Harlow]], John Preskill, _Holographic quantum error-correcting codes: Toy models for the bulk/boundary correspondence_, JHEP 06 (2015) 149 ([arXiv:1503.06237](https://arxiv.org/abs/1503.06237))

reviewed in

* {#Harlow18} [[Daniel Harlow]], _TASI Lectures on the Emergence of Bulk Physics in AdS/CFT_ ([arXiv:1802.01040](https://arxiv.org/abs/1802.01040))


Computation of [[black hole entropy]] in 4d via [[AdS4-CFT3 duality]] from [[holographic entanglement entropy]] in the [[ABJM theory]] for the [[M2-brane]] is discussed in

* Jun Nian, Xinyu Zhang, _Entanglement Entropy of ABJM Theory and Entropy of Topological Black Hole_ ([arXiv:1705.01896](https://arxiv.org/abs/1705.01896))


[[!redirects Ryu-Takayanagi formula]]

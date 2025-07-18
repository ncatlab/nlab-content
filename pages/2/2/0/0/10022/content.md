
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
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

The term *holographic entanglement entropy* refers to expressions of [[entanglement entropy]] in [[boundary field theory|boundary]] [[quantum field theories]], via a version of [[AdS-CFT duality]] ("holography"), in terms of the [[geometry]] of a higher-dimensional [[bulk]] [[spacetime]].

The essential idea is that the [[entanglement entropy]] of a region $U$ in the domain of a [[boundary field theory]] should be proportional to the [[volume]] ([[length]], [[area]], ...) of the [[hypersurface]] $\Sigma$ in the [[bulk]] [[spacetime]] which shares the same [[boundary]] $\partial U = \partial \Sigma$ and which has minimal volume with this property.
A more precise version of this idea is given by the *Ryu-Takayanagi formula*, see [below](#RyuTakayanagiFormula). 

This kind of relation between [[entropy]] of [[quantum systems]] and [[area]]/[[volumes]] of critical surfaces in a [[curved spacetime]] is akin to the [[Bekenstein-Hawking entropy]]-formula for [[black holes]], and indeed it is meant to *subsume* the [[black hole entropy]]-formula for black holes in [[anti de Sitter spacetimes]].

While in the original context of the [[AdS-CFT correspondence]] the Ryu-Takayanagi formula remains ill-defined, or at least intractable in detail (not the least because it is, ultimately, a statement about [[non-perturbative quantum field theory|non-perturbative]] [[string theory]], hence about [[M-theory]], which [remains elusive](M-theory#TheOpenProblem)), its general idea led to the discovery of fully well-defined discretized ("toy") models  of holography in terms of [[tensor networks]] that express ([[code subspaces]]) of [[quantum error correcting codes]] (such as the [[HaPPY code]] and [[Majorana dimer codes]]). In these holographic [[tensor network]] models the behaviour of holographic entanglement entropy, and of several other expected aspects of [[holography]], turn out to have a faithful reflection (up to lattice effects caused by the discretization) amenable to explicit analysis, by tools 

1. from [[quantum information theory]],

1. from [[condensed matter physics]] (see also at *[[AdS/CMT]]*).

The power of these [[quantum information theory]]-methods in making precise and detailed sense of [[quantum gravity]] in a [[holography|holographic]] [[bulk]] [[spacetime]] has re-inforced the earlier idea in [[AdS/CFT]] that notions of [[spacetime]] and of [[quantum gravity]] may be holographically defined and in fact *emerge* from non-gravitational [[quantum physics]], and here specifically from [[quantum entanglement]] -- an idea that has become known under the slogan "[It from Qbit](#SimonsFoundationItFromQBit)" (see also [Georgescu 19](#Georgescu19)). Just to keep in mind that, a priori, this applies "only" to the *extra* (higher) [[bulk]] [[dimension|dimensions]] of [[spacetime]], while the definition of the [[boundary field theory]] typically relies on some notion domain space(-time) already (maybe unless one considers bulk duals of [[D(-1)-branes]]...).



### Ryu-Takayanagi formula
 {#RyuTakayanagiFormula}

For [[quantum field theories]] that are exhibited as [[boundary field theories]] on the [[asymptotic boundary]] $A$ of an approximately [[anti de Sitter spacetime]] via some approximation to [[AdS-CFT duality]] (for instance for [[QCD]] via [[AdS-QCD duality]]) their [[entanglement entropy]] of a given [[bounded set|bounded domain]] $B\subset A$ turns out to be proportional to the [[volume]] ([[area]]) of the minimal-area [[codimension]]-2 [[hypersurface]] inside the [[bulk]] spacetime that has the same [[boundary]] $\partial B$ (see [Nishioka-Ryu-Takayanagi 09 (3.3)](#NishiokaRyuTakayanagi09) for review of the formula and [Lewkowycz-Maldacena 13](#LewkowyczMaldacena13) for a conceptual explanation). 

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


### Tensor network models
 {#TensorNetworkModels}

Further discussion of implications of the Ryu-Takayanagi formula in [van Raamsdonk 10](#vanRaamsdonk10) suggested that the logic may also be turned around: Instead of computing [[entanglement entropy]] of a given [[boundary field theory]] from known [[bulk]] [[geometry]], conversely the [[bulk]] [[spacetime]] may be reconstructed from knowledge of the [[entanglement entropy]] of a boundary field theory.

Talking this perspective to the extreme suggests a description of [[bulk]] [[spacetimes]] entirely in terms of [[quantum information theory]]/[[entanglement]]-relations of a boundary [[QFT]] ("[[tensor networks]]", [Swingle 09](#Swingle09), [Swingle 12](#Swingle12), and [[quantum error correction codes]] [ADH 14](#ADH14), [PYHP 15](#PYHP15), [HNQTWY 16](#HNQTWY16), see [Harlow 18](#Harlow18), [Jahn-Eisert 21](#JahnEisert21) for review).


Here a [[tensor network]] [[Poincaré duality|Poincaré dual]] to a finite-stage [[hyperbolic tesselation]] of the [[hyperbolic plane]] is interpreted as a discretized model for a [[bulk]] [[spacetime]] with holographic [[quantum state]] on its [[asymptotic boundary]] being given by the [[string diagram]]-evaluation of the [[tensor network]] as a [[linear map]] to the [[tensor product]] of spaces corresonding to the [[edges]] crossing the boundary of the [[tesselation]]. 

\begin{imagefromfile}
    "file_name": "HaPPYCodeTesselation.jpg",
    "float": "right",
    "width": 480,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 20
    },
    "caption": "from [Harlow 18](#Harlow18)"
\end{imagefromfile}


One shows ([ADH 14](#ADH14)) that this is a decent ("toy") model of expected properties of [[bulk]]/[[boundary field theory|boundary]] [[holography]] if this [[tensor network]] gives the [[code subspace]] of a [[quantum error correcting code]]. 

For example, the [[tensor network]] corresponding to the [[pentagon|pentagonal]] $\{5,4\}$ [[tesselation]] with a [[perfect tensor]] of rank $5+1$ assigned to each tile yields a [[quantum error correcting code]] now known as the [[HaPPY code]].

The idea is that the [[code subspace]] of this [[HaPPY code]] is that subspace of the boundary [[space of quantum states]] which holographically corresponds to all bulk states *without* a [[black hole]] in the bulk.

\begin{imagefromfile}
    "file_name": "BlackHoleInHaPPYCodeTensorNetworkII.jpg",
    "float": "right",
    "width": 360,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Jahn & Eisert 21](#JahnEisert21)"
\end{imagefromfile}



More generally, deleting any of the tiles in the interior of the [[tesselation]] is interpreted as the appearance of a bulk [[black hole]], whose [[Bekenstein-Hawking entropy]] is carried by the [[quantum states]] carried by the loose [[edges]] that cross over the "[[event horizon]]" to the now deleted tiles.

The extreme case that *all* tiles are deleted from the [[tensor network]], is thus interpreted describing a [[black hole]] that has swallowed up the entire [[bulk]] spacetime such that its [[horizon]] now coincides with the previous [[asymptotic boundary]], whence its quantum states and entropy now coincide with that of the holographic boundary theory.

\linebreak

In this discrete [[HaPPY code]] model for the [[AdS-CFT correspondence]] the Ryu-Takayanagi formula for holographic entanglement entropy ([above](#RyuTakayanagiFormula)) has an exact proof [PYHP 15, Theorem 2](#PYHP15).

### Chord diagram representation
 {#ChordDiagramRepresentation}

In fact, holographic entanglement entropy in the [[HaPPY code]] turns out to be entirely encoded by the *[[dimer]] network* in the underlying [[Majorana dimer code]] ([JGPE 19](#JGPE19)):

\begin{imagefromfile}
    "file_name": "HaPPYCodesAsDimerCode.jpg",
    "width": 680,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [JGPE 19](#JGPE19)"
\end{imagefromfile}

in that the entanglement entropy $S_A$ of any [[Majorana dimer code]]-[[tensor network]] [[quantum state|state]] turns out to count the number of [[dimers]] that cross between the ([[connected topological space|connected]]) subregion $A$ and its [[complement]]:

\begin{imagefromfile}
    "file_name": "ChordDiagramEntanglementEntropy.jpg",
    "width": 460,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [JGPE 19](#JGPE19)"
\end{imagefromfile}


\begin{imagefromfile}
    "file_name": "HanUniversalHolographicCode.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Yan 20](#Yan20)"
\end{imagefromfile}


In the case that the [[dimers]] correspond to the [[hyperbolic tesselation]] $\{5,4\}$ from the [[HaPPY code]], this entropy formula 

$$
  S_A
  \;=\;
  \tfrac{1}{2}
  \ln
  \big(
    2^{ \left\vert Chords(A, \bar A) \right\vert }
  \big)
$$

recovers the Ryu-Takayanagi formula ([JGPE 19 (78)](#JGPE19)), as here the number of chords crossing any hyperbolic [[geodesic]] grows linearly with the [[length]] of this geodesic. 

In the [[continuum limit]] this says that holographic entanglement entropy is exhibited by the [[geodesic]] [[flow]] out of the given subregion through its corresponding minimal bulk surface, an idea that was previously proposed in "bit-thread models" for holographic entanglement entropy ([Freedman & Headrick 16](#FreedmanHeadrick16)):

\begin{imagefromfile}
    "file_name": "HyperbolicGeodesicFlowAndEntanglementEntropy.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [Freedman & Headrick 16](#FreedmanHeadrick16)"
\end{imagefromfile}



\begin{imagefromfile}
    "file_name": "ChordDiagram.jpg",
    "float": "right",
    "width": 300,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [Sati & Schreiber 19c](#SatiSchreiber19c)"
\end{imagefromfile}

Following [Sati-Schreiber 19c](#SatiSchreiber19c) we recognize the above [[Majorana dimer]]/bit-thread networks from [JGPE 19](#JGPE19), [Yan 19](#Yan19) as *[[chord diagram]]*-encodings of holographic bulks ([p. 38](https://arxiv.org/pdf/1912.10425v3.pdf#page=38)).

Notice how each [[chord]] here reflects at the same time

1. one [[entanglement|entangled pair]] of [[qbits]] in the [[boundary field theory|boundary]] [[quantum system]];

1. a [[geodesic]] through the [[hyperbolic plane]] [[bulk]] spacetime.

This is a (rigorous) state of affairs reminiscent of the "[[ER = EPR]]" slogan.


\linebreak

## Related concepts

* [[holographic Renyi entropy]]

* gravitational entropy

  * [[Bekenstein-Hawking entropy]]

  * [[generalized second law of thermodynamics]]

  * [[black holes in string theory]]

  * [[ER = EPR]]

* [[p-adic AdS-CFT]]

* [[quantum error correcting code]]

  * [[HaPPY code]]

  * [[Majorana dimer code]]

## References
 {#References}


### General

The original articles are

* {#RyuTakayanagi06a} [[Shinsei Ryu]], [[Tadashi Takayanagi]], _Holographic Derivation of Entanglement Entropy from AdS/CFT_, Phys. Rev. Lett. 96:181602, 2006 ([arXiv:hep-th/0603001](https://arxiv.org/abs/hep-th/0603001))

* {#RyuTakayanagi06a} [[Shinsei Ryu]], [[Tadashi Takayanagi]], _Aspects of Holographic Entanglement Entropy_, JHEP 0608:045, 2006 ([arXiv:hep-th/0605073](https://arxiv.org/abs/hep-th/0605073))

A proposal for a conceptual explanation:

* {#LewkowyczMaldacena13} Aitor Lewkowycz, [[Juan Maldacena]], _Generalized gravitational entropy_, J. High Energ. Phys. (2013) 2013: 90 ([arXiv:1304.4926](https://arxiv.org/abs/1304.4926))

* [[Nele Callebaut]], *Entanglement in conformal field theory and holography* &lbrack;[arXiv:2303.16827](https://arxiv.org/abs/2303.16827)&rbrack;


Review:

* [[Jens Eisert]], M. Cramer, M.B. Plenio, _Area laws for the entanglement entropy - a review_, Rev. Mod. Phys. 82, 277 (2010) ([arXiv:0808.3773](https://arxiv.org/abs/0808.3773))

* {#NishiokaRyuTakayanagi09} Tatsuma Nishioka, [[Shinsei Ryu]], [[Tadashi Takayanagi]], *Holographic Entanglement Entropy: An Overview*, J. Phys. A **42** 504008 (2009) &lbrack;[arXiv:0905.0932](https://arxiv.org/abs/0905.0932), [doi:10.1088/1751-8113/42/50/504008](https://iopscience.iop.org/article/10.1088/1751-8113/42/50/504008)&rbrack;

* Matthew Headrick, _Lectures on entanglement entropy in field theory and holography_ ([arXiv:1907.08126](https://arxiv.org/abs/1907.08126))

* [[Bei Zeng]], [[Xie Chen]], [[Duan-Lu Zhou]], [[Xiao-Gang Wen]]: 

  Sec. 5 of: *[[Quantum Information Meets Quantum Matter]] -- From Quantum Entanglement to Topological Phases of Many-Body Systems*, Quantum Science and Technology (QST), Springer (2019) $[$[arXiv:1508.02595](https://arxiv.org/abs/1508.02595), [doi:10.1007/978-1-4939-9084-9](https://doi.org/10.1007/978-1-4939-9084-9)$]$


* Bin Chen, *Holographic Entanglement Entropy: A Topical Review*, Communications in Theoretical Physics, **71** (2019) 837 &lbrack;[doi:10.1088/0253-6102/71/7/837](https://iopscience.iop.org/article/10.1088/0253-6102/71/7/837)&rbrack;


* [[Bowen Chen]], [[Bartlomiej Czech]], [[Zi-zhi Wang]], *Quantum Information in Holographic Duality*, Rept. Prog. Phys. **85** (2022) 4, 046001 &lbrack;[arXiv:2108.09188](https://arxiv.org/abs/2108.09188), [doi:10.1088/1361-6633/ac51b5](https://doi.org/10.1088/1361-6633/ac51b5)&rbrack;


* [[Edward Witten]]  section 9 of: *Introduction to Black Hole Thermodynamics* &lbrack;[arXiv:2412.16795](https://arxiv.org/abs/2412.16795)&rbrack;



Textbook account:

* [[Mukund Rangamani]], [[Tadashi Takayanagi]], *Holographic Entanglement Entropy*, Lecture Notes in Physics **931**, Springer (2017) &lbrack;[doi:10.1007/978-3-319-52573-0](https://doi.org/10.1007/978-3-319-52573-0), [arXiv:1609.01287](https://arxiv.org/abs/1609.01287)&rbrack;



Survey talks:

* [[Robert Myers]], _Holographic entanglement entropy_,  ([pdf slides](http://www.lpt.ens.fr/IMG/pdf/Myers.pdf))

* Shinsei Ryu, _Holographic geometry in Entanglement Renormalization_ ([pdf slides](http://icmt.illinois.edu/Workshops/JointWorkshopPerimeter/Ryu-PI-ICMT-2012.pdf))

* Juan Jottar, _(Entanglement) Entropy in three-dimensional higher spin theories_ ([pdf slides](http://www.hip.fi/holograv13/talk_folder/Jottar-HologravWorkshop-March2013.pdf))

* Matthew Headrick, _Entanglement entropies in holographic field theory_ ([pdf slides](http://www.ggi.fi.infn.it/talks/talk1853.pdf))

* {#Hartmann14} Tom Hartmann, _Entanglement entropy and geometry_, talk slides, 2014 ([pdf](http://online.kitp.ucsb.edu/online/qft14/hartman/pdf/Hartman_QFT14_KITP.pdf))

An influential argument that this relation implies that [[entanglement]] in the boundary theory is what makes spacetime as such appear in the bulk theory is due to

* {#vanRaamsdonk10} [[Mark Van Raamsdonk]], _Building up spacetime with quantum entanglement_, Gen. Rel. Grav. **42** (2010) 2323-2329; Int. J. Mod. Phys. **D19** (2010) 2429-2435 ([arXiv:1005.3035](https://arxiv.org/abs/1005.3035)) 

* [[Mark Van Raamsdonk]], _Building up spacetime with quantum entanglement II: It from BC-bit_ ([arXiv:1809.01197](https://arxiv.org/abs/1809.01197))

reviewed in 

* [[Mark Van Raamsdonk]], _Lectures on Gravity and Entanglement_, chapter 5 in  New Frontiers in Fields and Strings
TASI 2015 Proceedings of the 2015 Theoretical Advanced Study Institute in Elementary Particle Physics 2015 Theoretical Advanced Study Institute in Elementary Particle Physics ([arXiv:1609.00026](https://arxiv.org/abs/1609.00026))

Discussion of the corresponding continuum theory, formulated via [[local nets of observables]] in [[algebraic quantum field theory]]:

* [[Edward Witten]], _Notes on Some Entanglement Properties of Quantum Field Theory_, Rev. Mod. Phys. 90, 45003 (2018) ([arXiv:1803.04993](https://arxiv.org/abs/1803.04993))


* {#Faulkner20} [[Thomas Faulkner]], _The holographic map as a conditional expectation_ ([arXiv:2008.04810](https://arxiv.org/abs/2008.04810))

See also:

* Matthew Headrick, Veronika E. Hubeny, *Covariant bit threads* &lbrack;[arXiv:2208.10507](https://arxiv.org/abs/2208.10507)&rbrack;

* Eugenia Colafranceschi, [[Xi Dong]], [[Donald Marolf]], Zhencheng Wang, *Algebras and Hilbert spaces from gravitational path integrals: Understanding Ryu-Takayanagi/HRT as entropy without invoking holography* &lbrack;[arXiv:2310.02189](https://arxiv.org/abs/2310.02189)&rbrack;


### Via holographic tensor networks and quantum codes

Relation to [[renormalization]] of [[entanglement]] and [[tensor networks]] is due to 

* {#Swingle09} [[Brian Swingle]], _Entanglement Renormalization and Holography_, Phys. Rev. D 86, 065007 (2012) ([arXiv:0905.1317](https://arxiv.org/abs/0905.1317))

* {#Swingle12} [[Brian Swingle]], _Constructing holographic spacetimes using entanglement renormalization_ ([arXiv:1209.3304](https://arxiv.org/abs/1209.3304), [spire:1185813](http://inspirehep.net/record/1185813))

and further in terms of [[quantum error correcting codes]] due to 

* {#ADH14} [[Ahmed Almheiri]], [[Xi Dong]], [[Daniel Harlow]], _Bulk Locality and Quantum Error Correction in AdS/CFT_, JHEP 1504:163,2015 ([arXiv:1411.7041](https://arxiv.org/abs/1411.7041))

* {#PYHP15} [[Fernando Pastawski]], [[Beni Yoshida]], [[Daniel Harlow]], [[John Preskill]], _Holographic quantum error-correcting codes: Toy models for the bulk/boundary correspondence_, JHEP 06 (2015) 149 ([arXiv:1503.06237](https://arxiv.org/abs/1503.06237))

* {#HNQTWY16} Patrick Hayden, Sepehr Nezami, Xiao-Liang Qi, Nathaniel Thomas, Michael Walter, Zhao Yang, _Holographic duality from random tensor networks_, JHEP 11 (2016) 009 ([arXiv:1601.01694](https://arxiv.org/abs/1601.01694))

* [[Daniel Harlow]], *The Ryu–Takayanagi Formula from Quantum Error Correction*, Comm. Math. Phys. **354** (2017) 865–912 &lbrack;[doi:10.1007/s00220-017-2904-z](https://doi.org/10.1007/s00220-017-2904-z), [arXiv:1607.03901](https://arxiv.org/abs/1607.03901)&rbrack;

* Helia Kamal, [[Geoffrey Penington]], _The Ryu-Takayanagi Formula from Quantum Error Correction: An Algebraic Treatment of the Boundary CFT_ ([arXiv:1912.02240](https://arxiv.org/abs/1912.02240))

reviewed in

* [[John Preskill]], *Is spacetime a quantum error-correcting code?*, talk at KITP 2015 ([pdf](http://theory.caltech.edu/~preskill/talks/Preskill-KITP-holographic-2015.pdf), [[Preskill_SpacetimeQEC.pdf:file]])

* {#Harlow18} [[Daniel Harlow]], _TASI Lectures on the Emergence of Bulk Physics in AdS/CFT_ ([arXiv:1802.01040](https://arxiv.org/abs/1802.01040))

* [[Pratik Rath]], *Aspects of Holography And Quantum Error Correction*, 2020 ([pdf](https://digitalassets.lib.berkeley.edu/etd/ucb/text/Rath_berkeley_0028E_19810.pdf), [[RathHolographyAndQEC.pdf:file]]) 

* {#Harlow20} [[Daniel Harlow]], *Computation and Holography*, talk at [Snowmass Computational Frontier Workshop 2020](https://indico.fnal.gov/event/43829/) ([pdf](https://indico.fnal.gov/event/43829/contributions/193566/attachments/132763/163346/snowmasscomp.pdf), [[HarlowComputationHolography.pdf:file]])

* Tanay Kibe, Prabha Mandayam, Ayan Mukhopadhyay, *Holographic spacetime, black holes and quantum error correcting codes: A review* ([arXiv:2110.14669](https://arxiv.org/abs/2110.14669))


See also

* [[Ahmed Almheiri]], _Holographic Quantum Error Correction and the Projected Black Hole Interior_ ([arXiv:1810.02055](https://arxiv.org/abs/1810.02055))


Further development of these tensor networks:

* Tamara Kohler, Toby Cubitt, *Toy Models of Holographic Duality between local Hamiltonians*, 	J. High Energy Phys. 2019:17 (2019) ([arXiv:1810.08992](https://arxiv.org/abs/1810.08992))



* {#BaoPeningtonSorceWall18} [[Ning Bao]], [[Geoffrey Penington]], [[Jonathan Sorce]], [[Aron C. Wall]], _Beyond Toy Models: Distilling Tensor Networks in Full AdS/CFT_,  JHEP 2019:69 ([arXiv:1812.01171](https://arxiv.org/abs/1812.01171))

* [[Ning Bao]], [[Geoffrey Penington]], [[Jonathan Sorce]], [[Aron C. Wall]], _Holographic Tensor Networks in Full AdS/CFT_ ([arXiv:1902.10157](https://arxiv.org/abs/1902.10157))

* Matthew Steinberg, Sebastian Feld, [[Alexander Jahn]], *Holographic Codes from Hyperinvariant Tensor Networks* &lbrack;[arXiv:2304.02732](https://arxiv.org/abs/2304.02732)&rbrack;


The bit-thread proposal for associating holographic entanglement entropy with [[geodesic]] [[flow]] in [[hyperbolic space]]:

* {#FreedmanHeadrick16} [[Michael Freedman]], [[Matthew Headrick]], *Bit threads and holographic entanglement*, Comm. Math. Phys. 352, 407 (2017) ([arXiv:1604.00354](https://arxiv.org/abs/1604.00354))

Embedding of the [[HaPPY code]] and the bit-thread models in more general [[Majorana dimer codes]]:

* {#JGPE19} [[Alexander Jahn]], [[Marek Gluza]], [[Fernando Pastawski]], [[Jens Eisert]], _Majorana dimers and holographic quantum error-correcting codes_, Phys. Rev. Research 1, 033079 (2019) ([arXiv:1905.03268](https://arxiv.org/abs/1905.03268))

* {#KahnZimborasEisert19} [[Alexander Jahn]], [[Zoltán Zimborás]], [[Jens Eisert]], _Central charges of aperiodic holographic tensor network models_, Phys. Rev. A 102, 042407 ([arXiv:1911.03485](https://arxiv.org/abs/1911.03485))


reviewed in:

* {#JahnEisert21} [[Alexander Jahn]], [[Jens Eisert]], _Holographic tensor network models and quantum error correction: A topical review_, Quantum Sci. Technol. 6 033002 ([arXiv:2102.02619](https://arxiv.org/abs/2102.02619), [doi:10.1088/2058-9565/ac0293](https://iopscience.iop.org/article/10.1088/2058-9565/ac0293))

* {#Yan19} [[Han Yan]], *Geodesic string condensation from symmetric tensor gauge theory: a unifying framework of holographic toy models*, Phys. Rev. B 102, 161119 (2020) ([arXiv:1911.01007](https://arxiv.org/abs/1911.01007))



See also:

* {#HMPSR19}  Felix M. Haehl, Eric Mintun, Jason Pollack, Antony J. Speranza, [[Mark Van Raamsdonk]], _Nonlocal multi-trace sources and bulk entanglement in holographic conformal field theories_, J. High Energ. Phys. (2019) 2019: 005 ([arxiv:1904.01584](https://arxiv.org/abs/1904.01584), [talk recording](https://youtu.be/kRCwzyliJ1M))

*  [[Han Yan]], _Hyperbolic Fracton Model, Subsystem Symmetry, and Holography_, Phys. Rev. B 99, 155126 (2019) ([arxiv:1807.05942](https://arxiv.org/abs/1807.05942))

* [[Chris Akers]], [[Geoff Penington]], *Quantum minimal surfaces from quantum error correction* ([arXiv:2109.14618](https://arxiv.org/abs/2109.14618))

* [[Alexander Jahn]], [[Marek Gluza]], Charlotte Verhoeven, Sukhbinder Singh, [[Jens Eisert]]. *Boundary theories of critical matchgate tensor networks* ([arXiv:2110.02972](https://arxiv.org/abs/2110.02972))

* Pablo Basteiro, Giuseppe Di Giulio, Johanna Erdmenger, Jonathan Karl, René Meyer, Zhuo-Yu Xian, *Towards Explicit Discrete Holography: Aperiodic Spin Chains from Hyperbolic Tilings* $[$[arXiv:2205.05693](https://arxiv.org/abs/2205.05693)$]$

* Lucas Daguerre, Matias Ginzburg, Gonzalo Torroba, *Holographic entanglement entropy inequalities beyond strong subadditivity* &lbrack;[arXiv:2208.03334](https://arxiv.org/abs/2208.03334)&rbrack;

* [[Scott Aaronson]], [[Jason Pollack]], *Discrete Bulk Reconstruction* &lbrack;[arXiv:2210.15601](https://arxiv.org/abs/2210.15601)&rbrack;



Computation of [[black hole entropy]] in 4d via [[AdS4-CFT3 duality]] from [[holographic entanglement entropy]] in the [[ABJM theory]] for the [[M2-brane]] is discussed in

* Jun Nian, Xinyu Zhang, _Entanglement Entropy of ABJM Theory and Entropy of Topological Black Hole_ ([arXiv:1705.01896](https://arxiv.org/abs/1705.01896))

Discussion in terms of [[DHR superselection theory]]:

* {#CHMP19} Horacio Casini, Marina Huerta, Javier M. Magan, Diego Pontello, _Entanglement entropy and superselection sectors I. Global symmetries_ ([arXiv:1905.10487](https://arxiv.org/abs/1905.10487))

Discussion of [[gauge symmetry]] of [[holographic tensor networks]] and their [[quantum error correcting codes]]:

* Kfir Dolev, Vladimir Calvera, Sam Cree, Dominic J. Williamson, 
*Gauging the bulk: generalized gauging maps and holographic codes* ([arXiv:2108.11402](https://arxiv.org/abs/2108.11402))

In relation to [[renormalization group flow]]:

* Keiichiro Furuya, Nima Lashkari, Mudassir Moosa, *Renormalization group and approximate error correction* ([arXiv:2112.05099](https://arxiv.org/abs/2112.05099))



Musings on possible implications on relations between [[quantum gravity]] and [[quantum information]] (specifically [[quantum entanglement]]):

* [[Brian Swingle]]: *Spacetime from Entanglement*, Annual Reviews **9** (2018) 345-358  &lbrack;[doi:10.1146/annurev-conmatphys-033117-054219](https://doi.org/10.1146/annurev-conmatphys-033117-054219)&rbrack;

* [[Mark Van Raamsdonk]]: *Spacetime from bits*, Science **370** 6513 (9 Oct 2020) 198-202 &lbrack;[doi:10.1126/science.aay9560](https://doi.org/10.1126/science.aay9560)&rbrack;
    
* [[Tadashi Takayanagi]]: *Emergent Holographic Spacetime from Quantum Information* &lbrack;[arXiv:2506.06595](https://arxiv.org/abs/2506.06595)&rbrack;

* {#SimonsFoundationItFromQBit} [[Simons Foundation]], *[It from Qubit: Simons Collaboration on Quantum Fields, Gravity and Information](https://www.simonsfoundation.org/mathematics-physical-sciences/it-from-qubit/)*

  Final meeting: *[It from QBit 2023](https://events.perimeterinstitute.ca/event/43/)*

* [[Tom Banks]], *Holographic Space-time and Quantum Information* &lbrack;[arXiv:2001.08205](https://arxiv.org/abs/2001.08205)&rbrack;

* {#Georgescu19} Iulia Georgescu: *Strings and qubits*, Nature Reviews Physics **1** (2019) 477 &lbrack;[doi:s42254-019-0087-6](https://www.nature.com/articles/s42254-019-0087-6)&rbrack;

* IAS Workshops on Quantum Information and Spacetime:

  * [Workshop on Quantum Information and Black Holes, December 5-6, 2017](https://www.ias.edu/sns/quantum-information-workshop-2017)

  * [Workshop on Quantum Information and the Structure of Spacetime, December 4-5, 2018](https://www.ias.edu/sns/quantum-information-workshop-2018)

  * [Workshop on Qubits and Spacetime, December 3 - 4, 2019](https://www.ias.edu/sns/quantum-information-workshop-2019)

  * [Online Workshop on Qubits and Black Holes, December 7-9, 2020](https://www.ias.edu/sns/quantum-information-workshop-2020)

  * [IAS Workshop on Quantum Information and Spacetime, December 6-8, 2021](https://www.ias.edu/sns/quantum-information-workshop-2021)


[[!include Chern-Simons Wilson lines in AdS3-CFT2 -- references]]


### Application to AdS/QCD

Application to [[AdS/QCD]]:

* Zhibin Li, Kun Xu, Mei Huang, _The entanglement properties of holographic QCD model with a critical end point_ ([arXiv:2002.08650](https://arxiv.org/abs/2002.08650))



[[!include entanglement island proposal for black hole paradox -- references]]


[[!include weight systems on chord diagrams in physics]]



[[!redirects Ryu-Takayanagi formula]]


[[!redirects bit thread]]
[[!redirects bit threads]]

[[!redirects holographic tensor network]]
[[!redirects holographic tensor networks]]




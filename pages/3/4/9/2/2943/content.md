
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

It is practically impossible to model a macroscopic [[physical system]] in terms of the microscopic kinematical and dynamical variables of all its [[particles]]. Thus one makes a hierarchical reduction in which this complexity is reduced to a small number of collective variables. The theoretical framework for such reductions for systems is [[statistical mechanics]] or statistical physics.

One special case of hierarchical reduction is the limit of large volumes $V$, in which the number of particles (of each species) per volume, $N/V$, stays constant. This is called the **[[thermodynamic limit]]** in statistical physics. Under some standard assumptions like homogeneity (spacial and possibly directional) and stability (no transitory effects), there is a small number of collective variables characterizing the system. Such a description can be (and historically was) postulated as an independent self-consistent phenomenological theory even without going into the details of statistical mechanics; such a description is called **[[equilibrium]] thermodynamics**, which is believed to be deducible from statistical mechanics, as has been partially proved for some classes of systems. Sometimes transitional finite-time phenomena are described either statistically by studying stochastic processes or by a more elaborate hierarchical form of thermodynamics, so-called **nonequilibrium thermodynamics**. 

One of the basic characteristics of a thermodynamical system is its [[temperature]], which has no analogue in fundamental non-statistical physics. Other common thermodynamical variables include pressure, volume, [[entropy]], enthalpy etc. 


## Related entries

* [[entropy]], [[relative entropy]], [[second law of thermodynamics]], [[generalized second law of thermodynamics|generalized second law]], [[KMS state]]

* [[intensive and extensive]]

* [[thermal quantum field theory]]

## References

### General

A formalization in terms of [[symplectic geometry]] is in chapter IV "Statistical mechanics" of

* [[Jean-Marie Souriau]], _Structure of dynamical systems. A symplectic view of physics_ . Translated from the French by C. H. Cushman-de Vries. Translation edited and with a preface by R. H. Cushman and G. M. Tuynman. Progress in Mathematics, 149. Birkh&#228;user Boston, Inc., Boston, MA, 1997

as well as in 

* [[Jean-Marie Souriau]], _Thermodynamique et g&#233;om&#233;trie_,  Lecture Notes in Math. 676 (1978), 369&#8211;397 ([scan](http://www-lib.kek.jp/cgi-bin/kiss_prepri.v8?KN=197810025))

The Souriau model of thermodynamics has been extented for "geometric science of information" (Koszul information geometry) with a general definition of [[Fisher metric]], Euler-Poincar&#233; equation and variational definition of Souriau thermodynamics, as in:

* Frederic Barbaresco, _Koszul information geometry and Souriau geometric, temperature_, Capacity of Lie Group Thermodynamics, MDPI Entropy, n&#176;16,  4521-4565 (2014) [pdf](http://www.mdpi.com/1099-4300/16/8/4521/pdf); _Symplectic structure of information geometry: Fisher metric and Euler-Poincar&#233; equation of Souriau Lie group thermodynamics_, GSI'15, Springer LCNS __9389__, 529-540 (2015) [doi](https://doi.org/10.1007/978-3-319-25040-3_57) 

See also

* wikipedia: [thermodynamics](http://en.wikipedia.org/wiki/Thermodynamics), [fundamental thermodynamic relation](http://en.wikipedia.org/wiki/Fundamental_thermodynamic_relation)

* Azimuth Project, _[Thermodynamics](http://www.azimuthproject.org/azimuth/show/Thermodynamics)_

* A. Bravetti, C. S. Lopez-Monsalvo, F. Nettel, _Contact symmetries and Hamiltonian thermodynamics_, [arxiv/1409.7340](http://arxiv.org/abs/1409.7340)

For an thorough introduction to common misconceptions at an elementary level:

* John Denker. _Modern Thermodynamics_. [web](http://www.av8n.com/physics/thermo), [pdf](http://www.av8n.com/physics/thermo-laws.pdf).

A survey of [[irreversible thermodynamics]] is in 

* Ivan Vavruch, _Conceptual problems of modern irreversible thermodynamics_, Chem. Listy 96 (2002) ([pdf](http://www.chemicke-listy.cz/docs/full/2002_05_01.pdf))

For more on this see also _[[rational thermodynamics]]_.

* &#193;lvaro M. Alhambra, Lluis Masanes, Jonathan Oppenheim, Christopher Perry, _Fluctuating work: from quantum thermodynamical identities to a second law equality_, Phys. Rev. X 6, 041017 [doi](http://dx.doi.org/10.1103/PhysRevX.6.041017)

### Relativistic thermodynamics
 {#ReferencesRelativisticThermodynamics}

Making sense of thermodynamics when taking into account [[special relativity]] and ultimately, possibly, [[general relativity]] ([[gravity]]) is notoriously subtle (even ignoring the issue of [[Bekenstein-Hawking entropy]]). 

> Shortly after the advent of the relativity theory, Planck, Hassenoerl, Einstein and others advanced separately a formulation of the thermodynamical laws in accordance with the special principle of relativity. This treatment was adopted unchanged including the first edition of this monograph. However it was shown by Ott and indepently by Arzelies, that the old formulation was not quite satisfactory, in particular because generalized forces were used instead of the true mechanical forces in the description of thermodynamical processes.

> The papers of Ott and Arzelies gave rise to many controversial discussions in the literature and at the present there is no generally accepted description of relativistic thermodynamics.

(quote from Moller, _[The theory of relativity](https://archive.org/details/theoryofrelativi029229mbp), 1952_)

A standard textbook has been 

* {#Tolman34} Richard Tolman, _Relativity, Thermodynamics and Cosmology_, Oxford 1934, reprinted by Dover 1987

but Tolman's approach has been called into question, see e.g. 

* Christian Fronsdal, _Relativistic thermodynamics_, 2014 ([pdf](http://fronsdal.physics.ucla.edu/system/files/Gen.Rel_.LMP_.pdf))

See also

* Nils Andersson, _General relativistic thermo-dynamics_, survey talk 2014 ([pdf](http://www.dpg-physik.de/dpg/pbh/aktuelles/pdf/Andersson.pdf))

* Sean A. Hayward, _Relativistic thermodynamics_ ([arXiv:gr-qc/9803007](https://arxiv.org/abs/gr-qc/9803007))

* Paul Frampton, Stephen D.H. Hsu, Thomas W. Kephart, David Reeb, _What is the entropy of the universe?_, Class. Quant. Grav.26:145005, 2009 ([arXiv:0801.1847](https://arxiv.org/abs/0801.1847))

### Further generalizations 

Some formal generalizations of thermodynamical formalism include mixing time and temperature in formalisms with complex time-temperature like Matsubara formalism in QFT. 

Mathematical analogies and generalizations include also 

* [[John Baez]], Mike Stay, _Algorithmic thermodynamics_, [pdf](http://math.ucr.edu/home/baez/thermo.pdf), [cafe](http://golem.ph.utexas.edu/category/2010/02/algorithmic_thermodynamics.html)
* [[M. Marcolli]], Ryan Thorngren, _Thermodynamical semirings_, [arXiv/1108.2874](http://arxiv.org/abs/1108.2874)
* M. Zinsmeister, _Thermodynamic formalism and holomorphic dynamical systems_, Amer. Math. Soc. 2000.
* I. Itenberg, G. Mikhalkin, _Geometry in the tropical limit_, [arXiv/1108.3111](http://arxiv.org/abs/1108.3111)



[[!redirects irreversible thermodynamics]]

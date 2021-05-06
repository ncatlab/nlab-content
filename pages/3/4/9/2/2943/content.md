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

One special case of hierarchical reduction is the limit of large volumes #$V$, in which the number of particles (of each species) per volume, $N/V$, stays constant. This is called the **[[thermodynamic limit]]** in statistical physics. Under some standard assumptions like homogeneity (spacial and possibly directional) and stability (no transitory effects), there is a small number of collective variables characterizing the system. Such a description can be (and historically was) postulated as an independent self-consistent phenomenological theory even without going into the details of statistical mechanics; such a description is called **[[equilibrium]] thermodynamics**, which is believed to be deducible from statistical mechanics, as has been partially proved for some classes of systems. Sometimes transitional finite-time phenomena are described either statistically by studying stochastic processes or by a more elaborate hierarchical form of thermodynamics, so-called **nonequilibrium thermodynamics**. 

One of the basic characteristics of a thermodynamical system is its [[temperature]], which has no analogue in fundamental non-statistical physics. Other common thermodynamical variables include pressure, volume, [[entropy]], enthalpy etc. 


## Related entries

* [[temperature]], [[inverse temperature]]

* [[Boltzmann constant]]

* [[Boltzmann distribution]]

* [[entropy]], [[relative entropy]], 

* [[second law of thermodynamics]], [[generalized second law of thermodynamics|generalized second law]], 

* [[KMS state]]

* [[intensive and extensive]]

* [[thermal quantum field theory]]

* [[eigenstate thermalization hypothesis]]

## References

### General


Introductions:

* John Denker, _Modern Thermodynamics_, ([web](http://www.av8n.com/physics/thermo), [pdf](http://www.av8n.com/physics/thermo-laws.pdf))

Mathematically rigorous treatments:

* Constantin Carathéodory, _Untersuchung über die Grundlagen der Thermodynamik_, Math. Annalen 67, 355-386


* Elliott H. Lieb, Jakob Yngvason, _The Physics and Mathematics of the Second Law of Thermodynamics_, Phys.Rept. 310 (1999) 1-96 ([arXiv:cond-mat/9708200](https://arxiv.org/abs/cond-mat/9708200))

* Elliott H. Lieb, Jakob Yngvason, _A Guide to Entropy and the Second Law of Thermodynamics_, Notices Amer. Math. Soc., 45, (1998) 571-581 ([arXiv:math-ph/9805005](https://arxiv.org/abs/math-ph/9805005))

See also

* Wikipedia: [thermodynamics](http://en.wikipedia.org/wiki/Thermodynamics), [fundamental thermodynamic relation](http://en.wikipedia.org/wiki/Fundamental_thermodynamic_relation)

* Azimuth Project, _[Thermodynamics](http://www.azimuthproject.org/azimuth/show/Thermodynamics)_


### In terms of symplectic geometry (Souriau)
 {#ReferencesSouriau}

A covariant formalization of thermodynamics in terms of [[moment maps]] in [[symplectic geometry]] is due to

* [[Jean-Marie Souriau]], _Thermodynamique et g&#233;om&#233;trie_,  Lecture Notes in Math. 676 (1978), 369&#8211;397 ([scan](http://www-lib.kek.jp/cgi-bin/kiss_prepri.v8?KN=197810025))

* {#IglesiasSouriau84} [[Patrick Iglesias-Zemmour]], [[Jean-Marie Souriau]] _Heat, cold and Geometry_, in: M. Cahen et al (eds.) Differential geometry and mathematical physics, 37-68, D. Reidel 1983 ([web](http://www.jmsouriau.com/Heat_Cold_And_Geometry_1983.htm), [pdf](http://www.jmsouriau.com/Publications/JMSouriau-PIglesias-HeatColdAndGeometry1983.pdf), [doi:978-94-009-7022-9_5](https://doi.org/10.1007/978-94-009-7022-9_5))

* [[Jean-Marie Souriau]], chapter IV "Statistical mechanics" of _Structure of dynamical systems. A symplectic view of physics_ . Translated from the French by C. H. Cushman-de Vries. Translation edited and with a preface by R. H. Cushman and G. M. Tuynman. Progress in Mathematics, 149. Birkh&#228;user Boston, Inc., Boston, MA, 1997

* [[Patrick Iglesias-Zemmour]], _Essai de «thermodynamique rationnelle» des milieux continus_, Annales de l'I.H.P. Physique théorique, Volume 34 (1981) no. 1,  p. 1-24 ([numdam:AIHPA_1981__34_1_1_0](http://www.numdam.org/item/AIHPA_1981__34_1_1_0))

* [[Jean-Marie Souriau]], J.-M. Mécanique statistique, groupes de Lie et cosmologie. In Colloques int. du CNRS; numéro 237; Aix-en-Provence, France, 1974; pp. 24–28, 59–113. English translation by F. Barbaresco, April, 2020. Available online: https://www.academia.edu/42630654/Statistical_Mechanics_Lie_Group_and_Cosmology_1_st_part_Symplectic_Model_of_Statistical_Mechanics(access on 20 April 2020)

Review includes

* {#Marle16} Charles-Michel Marle, _From tools in symplectic and Poisson geometry to Souriau's theories of statistical mechanics and thermodynamics_, Entropy 2016, 18(10), 370 ([arXiv:1608.00103](https://arxiv.org/abs/1608.00103))


The Souriau model of thermodynamics has been extented for "geometric science of information" (Koszul information geometry) with a general definition of [[Fisher metric]], Euler-Poincar&#233; equation and variational definition of Souriau thermodynamics, as in:

* Frederic Barbaresco, _Koszul information geometry and Souriau geometric, temperature_, Capacity of Lie Group Thermodynamics, MDPI Entropy, n&#176;16,  4521-4565 (2014) [pdf](http://www.mdpi.com/1099-4300/16/8/4521/pdf); _Symplectic structure of information geometry: Fisher metric and Euler-Poincar&#233; equation of Souriau Lie group thermodynamics_, GSI'15, Springer LCNS __9389__, 529-540 (2015) [doi](https://doi.org/10.1007/978-3-319-25040-3_57) 

* Barbaresco, F.; Gay-Balmaz, F. Lie Group Cohomology and (Multi)Symplectic Integrators: New Geometric Tools for Lie Group Machine Learning Based on Souriau Geometric Statistical Mechanics. Entropy 2020, 22, 498. https://www.mdpi.com/1099-4300/22/5/498

* {#Amari87} Shun-ichi Amari, Chapter 2: _Differential Geometrical Theory of Statistics_ in _Differential geometry in statistical inference_, Institute of Mathematical Statistics Lecture Notes - Monograph Series 1987, 19-94 ([euclid:1215467059](https://projecteuclid.org/euclid.lnms/1215467059))


* A. Bravetti, C. S. Lopez-Monsalvo, F. Nettel, _Contact symmetries and Hamiltonian thermodynamics_, [arxiv/1409.7340](http://arxiv.org/abs/1409.7340)


### Irreversible thermodynamics

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


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Exceptional structures
+-- {: .hide}
[[!include exceptional structures -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A hyperbolic [[Kac-Moody Lie algebra]] in the E-series 

* [[E₆]], [[E₇]], [[E₈]], [[E₉]], **E₁₀**, [[E₁₁]], $\cdots$


## Properties

### Maximal compact subalgebra
 {#MaximalCompactSubalgebra}

In contrast to $\mathfrak{e}_{10(10)}$ itself, its "[maximal compact subalgebra](Kac-Moody+algebra#OnMaximalCompactSubalgebra)" $\mathfrak{k}_{10(10)}$ has non-[[trivial representation|trivial]] [[finite-dimensional vector space|finite dimensional]] [[representations]] ([Kleinschmidt, Nicolai & Vigano 2020](#KleinschmidtNicolaiVigano20), [KKLN22](Kac-Moody+algebra#KKLN22)).


Among these is in particular a spinor representation $\mathbf{32}$ and a vector-spinor representation $\mathbf{320}$

$$
  \mathbf{32}
  ,\,
  \mathbf{320}
  \;\in\;
  Rep^{fdim}_{\mathbb{R}}\big(\mathfrak{k}_{10(10)}\big)
$$

akin to the familiar reps of $\mathfrak{so}(10)$ of the same name/dimension &lbrack;[deBuyl, Henneaux & Paulot 2005 §8](#deBuylHenneauxPaulot05), [Kleinschmidt & Nicolai 2006](#KleinschmidtNicolai06)&rbrack;.

Remarkably, the [[symmetric algebra|symmetrized]] [[tensor product of representations|tensor product]] of this spinorial $\mathbf{32}$ with itself decomposes as a 1-dimensional [[trivial representation]] with a 527-dimensional [[irrep]]:

$$
  \mathbf{32}
  \otimes_{sym}
  \mathbf{32}  
  \;\;
  \simeq
  \;\;
  \mathbf{1}
  \oplus
  \mathbf{527}
  \;\;\;\;\;
  \in
  \;\;
  Rep^{fdim}_{\mathbb{R}}\big(
    \mathfrak{k}_{10(10)}
  \big)
  \,.
$$

([Damour, Kleinschmidt & Nicolai 2006 p 37](#DamourKleinschmidtNicolai06)).




### As U-duality group of 1d M-theory
 {#AsUDualityOf1dMTheory}

$E_{10}$ is conjectured (e.g. [Nicolai 08](#Nicolai08)) to be the [[U-duality]] group (see there) of [[M-theory]] [[KK-compactification|compactified]] to 1 dimension (see also [[F/M-theory on elliptically fibered Calabi-Yau 5-folds]]).


[[!include U-duality -- table]]


## References


### General

Lecture notes:

* {#NicolaiSchlotterer09} [[Hermann Nicolai]] (notes by [[Oliver Schlotterer]]): _Infinite dimensional symmetries_, lecture at *Saalburg summer school* in Wolfersdorf, Thuringia (2009) &lbrack;[[NicolaiSchlotterer-InfinDimSymmetries.pdf:file]]&rbrack;


The fact that every simply laced hyperbolic Kac-Moody algebra is a sub Lie algebra of $E_{10}$:

* Sankaran Viswanath: *Embeddings of hyperbolic Kac-Moody algebras into $E_{10}$* &lbrack;[arXiv:0801.2586](https://arxiv.org/abs/0801.2586), [doi:10.1007/s11005-007-0214-7](https://doi.org/10.1007/s11005-007-0214-7), [doi:10.1007/s11005-007-0214-7](https://doi.org/10.1007/s11005-007-0214-7)&rbrack;

See also:

* {#NicolaiFischbacher03} [[Hermann Nicolai]], [[Thomas Fischbacher]]: _Low Level Representations for $E_{10}$ and $E_{11}$_, in *Kac-Moody Lie Algebras and Related Topics* &lbrack;[arXiv:hep-th/0301017](http://arxiv.org/abs/hep-th/0301017), [doi:10.1090/conm/343](https://doi.org/10.1090/conm/343)&rbrack;

* [[Thomas Fischbacher]]: *The structure of $E_{10}$ at higher $A_9$ levels -- a first algorithmic approach*, JHEP 0508:012 (2005) &lbrack;[arXiv:hep-th/0504230](https://arxiv.org/abs/hep-th/0504230), [doi:10.1088/1126-6708/2005/08/012](https://doi.org/10.1088/1126-6708/2005/08/012)&rbrack;



### Relation to supergravity
 {#ReferencesRelationToSupergravity}

Discussion of a 1d [[sigma-model]] on  $E_{10}/K(E_{10})$ as [[U-duality]]-covariant formuation of [[11D supergravity]]/[[M-theory]]:

For [[boson|bosonic]] degrees of freedom:

* [[Thibault Damour]], [[Marc Henneaux]], [[Hermann Nicolai]]: *$E(10)$ and a "small tension expansion" of M theory*, Phys. Rev. Lett. **89** 221601 (2002) &lbrack;[arXiv:hep-th/0207267](http://arxiv.org/abs/hep-th/0207267), [doi:10.1103/PhysRevLett.89.221601](https://doi.org/10.1103/PhysRevLett.89.221601)&rbrack;

* [[Axel Kleinschmidt]], [[Hermann Nicolai]]: _$E(10)$ and $SO(9,9)$ invariant supergravity_, JHEP 0407,
041 (2004) &lbrack;[arXiv:hep-th/0407101](http://arxiv.org/abs/hep-th/0407101), [doi:10.1088/1126-6708/2004/07/041](https://doi.org/10.1088/1126-6708/2004/07/041)&rbrack;

* [[Thibault Damour]], [[Hermann Nicolai]]: *Eleven dimensional supergravity and the $E_{10}/K(E_{10})$ sigma-model at low $A_9$ levels*, in Proceedings of the *XXV International Colloquium on Group Theoretical Methods in Physics, 2-6 August 2004, Cocoyoc, Mexico*, Routledge (2005) 93-111 &lbrack;[arXiv:hep-th/0410245](https://arxiv.org/abs/hep-th/0410245), [ISBN:9780750310086](https://www.routledge.com/Group-Theoretical-Methods-in-Physics-Proceedings-of-the-XXV-International-Colloqium-on-Group-Theoretical-Methods-in-Physics-Cocoyoc-Mexico-2/Pogosyan-Vincent-Wolf/p/book/9780750310086?srsltid=AfmBOopQu0UGWkX8-nMBU1xaKZdDXtl7Z9kUpqvWiOArkVvi_3k5qtHt)&rbrack;

* [[Axel Kleinschmidt]], [[Hermann Nicolai]]: *$E_{10}$ Cosmology*, JHEP 01 (2006) 137 &lbrack;[arXiv:hep-th/0511290](https://arxiv.org/abs/hep-th/0511290), [doi:10.1088/1126-6708/2006/01/137](https://iopscience.iop.org/article/10.1088/1126-6708/2006/01/137)&rbrack;
  > ([[cosmology|cosmological]] solutions)

* [[Marc Henneaux]], Mauricio Leston, Daniel Persson, Philippe Spindel: *Geometric Configurations, Regular Subalgebras of E10 and M-Theory Cosmology*, JHEP 0610:021 (2006) &lbrack;[arXiv:hep-th/0606123](https://arxiv.org/abs/hep-th/0606123), [doi:10.1088/1126-6708/2006/10/021](https://doi.org/10.1088/1126-6708/2006/10/021)&rbrack;
  > ([[cosmology|cosmological]] solutions)

* [[Marc Henneaux]], Ella Jamsin, [[Axel Kleinschmidt]], Daniel Persson: *On the $E_{10}$/Massive Type IIA Supergravity Correspondence*, Phys. Rev. D **79** (2009) 045008 &lbrack;[arXiv:0811.4358](https://arxiv.org/abs/0811.4358), [doi:10.1103/PhysRevD.79.045008](https://doi.org/10.1103/PhysRevD.79.045008)&rbrack;
  > (relation to [[massive type IIA string theory]])

* [[Thibault Damour]], [[Hermann Nicolai]]: *Higher order M theory corrections and the Kac-Moody algebra $E_{10}$*, Class. Quant. Grav. **22** (2005) 2849-2880 &lbrack;[arXiv:hep-th/0504153](https://arxiv.org/abs/hep-th/0504153), [doi:10.1088/0264-9381/22/14/003](https://doi.org/10.1088/0264-9381/22/14/003)&rbrack;
  > (relating to [[higher curvature corrections]])

* [[Thibault Damour]], [[Axel Kleinschmidt]], [[Hermann Nicolai]]: *Constraints and the $E_{10}$ Coset Model*, Class. Quant. Grav. **24** (2007) 6097-6120 &lbrack;[arXiv:0709.2691](https://arxiv.org/abs/0709.2691), [doi:10.1088/0264-9381/24/23/025](https://doi.org/10.1088/0264-9381/24/23/025)&rbrack;


* [[Eric A. Bergshoeff]], [[Olaf Hohm]], [[Axel Kleinschmidt]], [[Hermann Nicolai]], Teake A. Nutma, [[Jakob Palmkvist]]: *$E_{10}$ and Gauged Maximal Supergravity*, JHEP 0901:020 (2009) &lbrack;[doi:10.1088/1126-6708/2009/01/020](https://doi.org/10.1088/1126-6708/2009/01/020), [arXiv:0810.5767](https://arxiv.org/abs/0810.5767)&rbrack;
  > (relation to [[D=3 supergravity|D=3]] [[gauged supergravity]])

* [[Thibault Damour]], [[Axel Kleinschmidt]], [[Hermann Nicolai]]: *Sugawara-type constraints in hyperbolic coset models*, Commun. Math. Phys. **302** (2011) 755-788 &lbrack;[arXiv:0912.3491](https://arxiv.org/abs/0912.3491), [doi:10.1007/s00220-011-1188-y](https://doi.org/10.1007/s00220-011-1188-y)&rbrack;


* [[Axel Kleinschmidt]], [[Hermann Nicolai]]: *The $E_{10}$ Wheeler-DeWitt operator at low levels*, J. High Energ. Phys. **2022** 92 (2022) &lbrack;[arXiv:2202.12676](https://arxiv.org/abs/2202.12676), <a href="https://doi.org/10.1007/JHEP04(2022)092">doi:10.1007/JHEP04(2022)092</a>&rbrack;
  > (relation to the [[Wheeler-DeWitt equation]] for [[11D supergravity]])


and for [[fermion|fermionic]] degrees of freedom 

* S. de Buyl, [[Marc Henneaux]], L. Paulot: *Extended $E_8$ Invariance of 11-Dimensional Supergravity*, Journal of High Energy Physics **2006** JHEP02 (2006) &lbrack;[arXiv:hep-th/0512292](https://arxiv.org/abs/hep-th/0512292), [doi:10.1088/1126-6708/2006/02/056](https://doi.org/10.1088/1126-6708/2006/02/056)&rbrack;

* [[Axel Kleinschmidt]], [[Hermann Nicolai]]: *IIA and IIB spinors from $K(E_{10})$*, Phys. Lett.B **637** (2006) 107-112 &lbrack;[arXiv:hep-th/0603205](https://arxiv.org/abs/hep-th/0603205), [doi:10.1016/j.physletb.2006.04.007](https://doi.org/10.1016/j.physletb.2006.04.007)&rbrack;

* {#DamourKleinschmidtNicolai06} [[Thibault Damour]], [[Axel Kleinschmidt]], [[Hermann Nicolai]]: *$K(E_{10})$, Supergravity and Fermions*, JHEP 0608:046 (2006) &lbrack;[arXiv:hep-th/0606105](https://arxiv.org/abs/hep-th/0606105), [doi:10.1088/1126-6708/2006/08/046](https://doi.org/10.1088/1126-6708/2006/08/046)&rbrack;

* [[Axel Kleinschmidt]]: *Unifying R-symmetry in M-theory*, in *New Trends in Mathematical Physics*, Springer (2009) 389-401 &lbrack;[arXiv:hep-th/0703262](https://arxiv.org/abs/hep-th/0703262), [doi:10.1007/978-90-481-2810-5_26](https://doi.org/10.1007/978-90-481-2810-5_26)&rbrack;

and application to [[supersymmetric quantum mechanics|supersymmetric]] [[quantum cosmology]]: 

* {#Damour14} [[Thibault Damour]], _Quantum supersymmetric Bianchi IX  Cosmology and its hidden Kac-Moody Structure_, talk at [Gravitation, Solitons and Symmetries](http://www.lestudium-ias.com/#!registration-conference-21-may-gibbons/ci2z) &lbrack;[[DamourSQC14.pdf:file]]&rbrack;

See also:

* Jeffrey Brown, Surya Ganguli, [[Ori J. Ganor]], Craig Helfgott: *$E_{10}$ Orbifolds*, Journal of High Energy Physics **2005** JHEP06 (2005) &lbrack;[arXiv:hep-th/0409037](https://arxiv.org/abs/hep-th/0409037), [doi:10.1088/1126-6708/2005/06/057](https://doi.org/10.1088/1126-6708/2005/06/057)&rbrack;


Review:

* {#Carlevaro06} [[Luca Carlevaro]], part III of: *Three approaches to M-theory*, PhD thesis (2006) &lbrack;[hdl:123456789/16186](https://libra.unine.ch/handle/123456789/16186), [pdf](https://libra.unine.ch/server/api/core/bitstreams/b5eedf5f-8029-4700-83cb-806d0737a669/content), [spire:1253257](https://inspirehep.net/literature/1253257)&rbrack;

* [[Axel Kleinschmidt]], [[Hermann Nicolai]]: *Maximal supergravities and the $E_{10}$ model*,  International Journal of Modern Physics D **15** 10 (2006) 1619-1642 &lbrack;[doi:10.1142/S0218271806009005](https://doi.org/10.1142/S0218271806009005)&rbrack;

* {#Nicolai08} [[Hermann Nicolai]]: *Wonders of $E_{10}$ and $K(E_{10})$*, talk at *Wonders of Gauge Theory and Supergravity*, IHP Paris (2008) &lbrack;[[Nicolai-WondersOfE10.pdf:file]]&rbrack;

* {#Nicolai14} [[Hermann Nicolai]], _On Exceptional Geometry and Supergravity_, talk at *[Gravitation, Solitons and Symmetries](http://www.lestudium-ias.com/#!registration-conference-21-may-gibbons/ci2z)* &lbrack;[[NicolaiTalk14.pdf:file]]&rbrack;

* {#Nicolai24} [[Hermann Nicolai]]: *$\mathcal{N}=8$ Supergravity, and beyond* &lbrack;[arXiv:2409.18656](https://arxiv.org/abs/2409.18656)&rbrack;



### Maximal compact subalgebra

More on the [[maximal compact subalgebras]] of [[E9]] and [[E10]], respectively, and their [[finite-dimensional vector space|finite-dimensional]] [[linear representations]]:

* {#KleinschmidtNicolaiVigano20} [[Axel Kleinschmidt]], [[Hermann Nicolai]], Adriano Viganò: *On spinorial representations of involutory subalgebras of Kac-Moody algebras*, In: *Partition Functions and Automorphic Forms*, Moscow Lectures **5**, Springer  (2020) &lbrack;[arXiv:1811.11659](https://arxiv.org/abs/1811.11659), [doi:10.1007/978-3-030-42400-8_4](https://doi.org/10.1007/978-3-030-42400-8_4)&rbrack;


* {#deBuylHenneauxPaulot05} Sophie de Buyl, [[Marc Henneaux]], Louis Paulot: *Hidden Symmetries and Dirac Fermions*, Class. Quant. Grav. **22** (2005) 3595-3622 &lbrack;[arXiv:hep-th/0506009](https://arxiv.org/abs/hep-th/0506009), [doi:10.1088/0264-9381/22/17/018](https://doi.org/10.1088/0264-9381/22/17/018)&rbrack;


* {#KleinschmidtNicolai06} [[Axel Kleinschmidt]], [[Hermann Nicolai]]: *IIA and IIB spinors from $K(E_{10})$*, Phys. Lett. B **637** (2006) 107-112 &lbrack;[arXiv:hep-th/0603205](https://arxiv.org/abs/hep-th/0603205), [doi:10.1016/j.physletb.2006.04.007](https://doi.org/10.1016/j.physletb.2006.04.007)&rbrack;


* [[Axel Kleinschmidt]], [[Hermann Nicolai]], [[Jakob Palmkvist]]: *$K(E_9)$ from $K(E_{10})$*, Journal of High Energy Physics **2007** JHEP06 (2007) &lbrack;[arXiv:hep-th/0611314](https://arxiv.org/abs/hep-th/0611314), [doi:10.1088/1126-6708/2007/06/051](https://doi.org/10.1088/1126-6708/2007/06/051)&rbrack;

* [[Axel Kleinschmidt]], [[Hermann Nicolai]]: *On higher spin realizations of $K(E_{10})$*, J. High Energ. Phys. **2013** 41 (2013) &lbrack;[arXiv:1307.0413](https://arxiv.org/abs/1307.0413), <a href="https://doi.org/10.1007/JHEP08(2013)041">doi:10.1007/JHEP08(2013)041</a>&rbrack;



### Standard model pheonomenology
 {#StandardModelPhenomenology}


On the [[U-duality]] [[E10|$E_{10}$]] (or rather [$K(E_{10}) \subset E_{10}$](E10#MaximalCompactSubalgebra)) as a non-standard [[GUT]]-[[gauge group|group]], following the proposal at the end of

* {#GellMann83} [[Murray Gell-Mann]], introductory talk at _[Shelter Island II](https://en.wikipedia.org/wiki/Shelter_Island_Conference)_ (1983) ([[Gell-Mann_ShelterIslandII_1983.pdf:file]]) 

  in: _Shelter Island II: Proceedings of the 1983 Shelter Island Conference on Quantum Field Theory and the Fundamental Problems of Physics_. MIT Press (1985) 301-343 \[ISBN:0-262-10031-2\]

to identify the 48 spin 1/2 fermions of [[D=4 N=8 supergravity]], that remain after complete [[supersymmetry breaking|breaking]] of [[number of supersymmetries|$N=8$]] [[supersymmetry]], with the $3 \times 16$ [[quarks]] and [[leptons]] of the [[standard model of particle physics]]:

* [[Krzysztof A. Meissner]], [[Hermann Nicolai]]: *Standard Model Fermions and $N=8$ supergravity*, Phys. Rev. D **91** (2015) 065029 \[<a href="https://doi.org/10.1103/PhysRevD.91.065029">doi:10.1103/PhysRevD.91.065029</a>, [arXiv:1412.1715](https://arxiv.org/abs/1412.1715)\]

* [[Krzysztof A. Meissner]], [[Hermann Nicolai]]: *Standard Model Fermions and Infinite-Dimensional $R$-Symmetries*, Phys. Rev. Lett. **121** (2018) 091601 \[<a href="https://doi.org/10.1103/PhysRevLett.121.091601">doi:10.1103/PhysRevLett.121.091601</a>, [arXiv:1804.09606](https://arxiv.org/abs/1804.09606)\]

* [[Krzysztof A. Meissner]], [[Hermann Nicolai]]: *Standard Model Symmetries and $K(E_{10})$* \[<a href="https://arxiv.org/abs/2503.13155">arXiv:2503.13155</a>\]

For perspective see also [Nicolai 2024](#Nicolai24) and for the [[gravitino]] as a [[dark matter]] candidate in this context, see [there](gravitino#ViaE10AsDarkMatterCandidate).



[[!redirects E10]]



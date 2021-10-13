
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cosmology
+-- {: .hide}
[[!include cosmology -- contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In [[phenomenology]] of [[cosmology]], the _Starobinsky model_ of [[cosmic inflation]] takes into account -- and takes as the very source of the [[inflaton]] field -- [[higher curvature corrections]] to the [[Einstein-Hilbert action]] of [[gravity]], notably the term $R^2$ (square of the [[Ricci curvature]]).

The Starobinsky model stands out among models of inflation as predicting a low value of the scalar-to-tensor ratio $r$, specifically it predicts

$$
  r \sim \frac{12}{N^2}
$$

where $N$ is the number of $e$-foldings during inflation (see e.g. [Kehagias-Dizgah-Riotto 13 (2.6)](#KehagiasDizgahRiotto13)).


## Observational support
 {#ObservationalSupport}

Models of Starobinsky-type are favored by [[experiment|experimental]] results ([PlanckCollaboration 13](#PlanckCollaboration13), [BICEP2-Keck-Planck 15](#BICEPKeckPlanck15), [PlanckCollaboration 15](#PlanckCollaboration15), [BICEP3-Keck 18](#BICEPKeck21)) which give a low upper bound on $r$, well below $0.1$ (whereas other models like [[chaotic inflation]] are disfavored by these values), see ([PlanckCollaboration 13, page 12](#PlanckCollaboration13)).

{#Dat} With respect to this data, the Starobinsky model (or "$R^2$ inflation") is the model with the highest [[Bayesian reasoning|Bayesian evidence]] ([Rachen, Feb 15](#Rachen15), [PlanckCollaboration 15XX, table 6 on p. 18](#PlanckCollaboration15XX)) as it is right in the center of the likelihood peak, shown in dark blue in the following plots ([PlanckCollaboration 13, figure 1](#PlanckCollaboration13), also [Linde 14, figure 5](#Linde14)) and at the same time has the lowest number of free parameters : 

{#Figure1} <img src="https://ncatlab.org/nlab/files/PlanckData.jpg" width="800">


This remains true with the data of ([PlanckCollaboration 15](#PlanckCollaboration15)), see ([PlanckCollaboration 15 XIII, figure 22](#PlanckCollaboration15XIII)) and in the final analysis ([PlanckCollaboration 18X, Fig 8](#PlanckCollaboration18X)), which gives the following (from [here](http://resonaances.blogspot.se/2015/02/weekend-plot-inflation15.html)):

{#Figure2} <img src="https://ncatlab.org/nlab/files/InflationPlanck2015.jpg" width="800">

> $R^2$ inflation has the strongest evidence among the models considered here. However, care must be taken not to overinterpret small differences in likelihood lacking statistical significance. The models closest to $R^2$ in terms of evidence are brane inflation and exponential inflation, which have one more parameter
than $R^2$ ([PlanckCollaboration 15XX, p. 18](#PlanckCollaboration15XX))

{#KECKBICEPFurtherConfirmed} This picture is further confirmed by observations of the BICEP/Keck collaboration reported in [BICEP-Keck 2021](#BICEPKeck21), whose additional data singles out the dark blue area in the following (<a href="https://arxiv.org/pdf/2110.00483.pdf#page=8">Fig. 5</a>):

<center>
<a href="https://arxiv.org/pdf/2110.00483.pdf#page=8">
<img src="https://ncatlab.org/nlab/files/BICEPKeck-nr-plot-211006.jpg" width="430">
</a>
</center>

See also [Ellis 13](#Ellis13), [Ketov 13](#Ketov13), [Efstathiou 2019, 50:49](#Efstathiou2019) for brief survey of Starobinsky inflation in relation to observation, and see [Kehagias-Dizgah-Riotto 13](#KehagiasDizgahRiotto13) for more details. There it is argued that the other types of inflationary models which also reasonably fit the data are actually equivalent to the Starobinsky model during inflation.


## Embedding into supergravity
 {#EmbeddingIntoSupergravity}

Being concerned with pure [[gravity]] (the [[inflaton]] not being an extra [[matter]] field but part of the field of [[gravity]]) the Starobinsky model lends itself to embedding into [[supergravity]] (originally due to [Cecotti 87](#Cecotti87), see e.g. [Farakos-Kehagias-Riotto 13](#FKR13)). Such embedding has been argued to improve the model further (highlighted e.g. in [Ellis 13](#Ellis13)), for instance by 

* {#ShrinkingOfInitialHomogeneousPatch} shrinking the necessary initial homogeneous patch from $\sim 10^3$ [[Planck lengths]] (which would be in need of further explanation) down to just $\sim 10^1$ [[Planck lengths]] ([Dalianis-Farakos 15 equations (68), (72) in v1, equations (4.11), (4.17) in v3](#DalianisFarakos15), reviewed in [Dalianis 16](#Dalianis16));

* {#CompatibilityWithsusybreaking} naturally subsuming a mechanism for [[supersymmetry breaking]] ([Ferrar-Kehagias 14](#FerrarKehagias14), [DFKRU 14](#DFKRU14)) notably with a Starobisnky potential naturally induced from [[gravitino condensation]] ([Alexandre-Houston-Mavromatos 14](#AlexandreHoustonMavromatos14)).

<center>
<img src="https://ncatlab.org/nlab/files/DalianisDiagram.jpg" width="600">
</center>

> graphics grabbed from [Dalianis 16, p. 8](#Dalianis16)

{#HCCIn11dSugra} More concretely, in [Hiraga-Hyakutake 18](#HiragaHyakutake18) a simple model of [[11-dimensional supergravity]] with its $R^4$ [[higher curvature correction]] (see [there](11-dimensional+supergravity#HigherCurvatureCorrection)) is considered and claimed to yield inflation with "graceful exit" and dynamical [[KK-compactification]]:


<center>
<img src="https://ncatlab.org/nlab/files/W4Inflation.jpg" width="600">
</center>

> graphics from [Hiraga-Hyakutake 18, p. 8](#HiragaHyakutake18)


## References

### General

The model is due to

* {#Starobisnky80} [[Aleksei Starobinsky]], _A new type of isotropic cosmological models without singularity_, Phys. Lett. B 91, 99 (1980); (<a href="https://doi.org/10.1016/0370-2693(80)90670-X">doi:10.1016/0370-2693(80)90670-X</a>)

and the analysis of its predictions is due to

* [[Viatcheslav Mukhanov]] and G. V. Chibisov, JETP Lett. 33, 532 (1981) [Pisma Zh. Eksp. Teor. Fiz. 33, 549 (1981)]; 

* [[Aleksei Starobinsky]], Sov. Astron. Lett. 9, 302 (1983).

The experimental data supporting the model is due to 

* {#PlanckCollaboration13} [[Planck Collaboration]], _Planck 2013 results. XXII. Constraints on inflation_ ([arXiv:1303.5082](http://arxiv.org/abs/1303.5082))

* {#BICEPKeckPlanck15} [[Planck Collaboration]], [[BICEP2]] _A Joint Analysis of BICEP2/Keck Array and Planck Data_ ([arXiv:1502.00612](http://arxiv.org/abs/1502.00612))

* {#PlanckCollaboration15} [[Planck Collaboration]], _Planck 2015, Overview of results_ ([arXiv:1502.01582](http://xxx.lanl.gov/abs/1502.01582))

* {#PlanckCollaboration15XIII} [[Planck Collaboration]], _Planck 2015 results. XIII. Cosmological parameters_ ([arXiv:1502.01589](http://xxx.lanl.gov/abs/1502.01589))

* {#PlanckCollaboration15XX} [[Planck Collaboration]], _Planck 2015 results. XX. Constraints on inflation_ ([arXiv:1502.02114](http://arxiv.org/abs/1502.02114))

* {#PlanckCollaboration18X} [[Planck Collaboration]], _Planck 2018 results. X. Constraints on inflation_ ([arXiv:1807.06211](https://arxiv.org/abs/1807.06211))

* {#BICEPKeck21} BICEP/Keck Collaboration: *BICEP / Keck XIII: Improved Constraints on Primordial Gravitational Waves using Planck, WMAP, and BICEP/Keck Observations through the 2018 Observing Season*, Phys. Rev. Lett. 127, 151301 ([arXiv:2110.00483](https://arxiv.org/abs/2110.00483), [doi:10.1103/PhysRevLett.127.151301](https://doi.org/10.1103/PhysRevLett.127.151301))

See also

* Debika Chowdhury, Jerome Martin, Christophe Ringeval, Vincent Vennin, _Inflation after Planck: Judgment Day_ ([arxiv:1902.03951](https://arxiv.org/abs/1902.03951))


Review and exposition includes

* {#KehagiasDizgahRiotto13} [[Alex Kehagias]], Azadeh Moradinezhad Dizgah, Antonio Riotto, _Comments on the Starobinsky Model of Inflation and its Descendants_, Phys. Rev. D 89, 043527 (2014) ([arXiv:1312.1155](http://arxiv.org/abs/1312.1155))

* {#Ketov13} [[Sergei Ketov]], _PLANCK mission, Starobinsky inflation and its realization in old-minimal supergravity_, talk at _Kavli IPMU Workshop: SUSY Model Building and Phenomenology_, 2-4 December 2013 ([pdf](http://indico.ipmu.jp/indico/getFile.py/access?contribId=16&sessionId=7&resId=0&materialId=slides&confId=28))

* {#Ellis13} [[John Ellis]], _Planck-Compatible Inflationary Models_, talk 2013 ([pptx](http://londoncosmology.files.wordpress.com/2013/09/lcdm.pptx))

* {#Linde14} [[Andrei Linde]], _Inflationary Cosmology after Planck 2013_ ([arXiv:1402.0526](http://arxiv.org/abs/1402.0526))

* {#Rachen15} [[Jörg Rachen]], _The Planck 2015 Results: Cosmology and Fundamental Physics from the Polarised CMB and Other Probes_, IMAPP Special Seminar, Nijmegen, Feb.5, 2015

* {#Dalianis16} [[Ioannis Dalianis]],  _Features and implications of the plateau inflationary potentials_, Planck 2015 conference contribution ([arXiv:1602.05026](http://arxiv.org/abs/1602.05026))

* {#Efstathiou2019} George P. Efstathiou on behalf of the PLANCK mission, _The PLANCK legacy, inflation and the origin of structure in the universe_, talk at University of Cambridge, January 28, 2019 ([recording from 50:49](https://www.youtube.com/watch?v=16CkVzVK7Wk&feature=youtu.be&t=3049))

Discussion with more general [[higher curvature corrections]]:

* {#AEJ18} Gustavo Arciniega, Jose D. Edelstein, Luisa G. Jaime, _Towards purely geometric inflation and late time acceleration_ ([arXiv:1810.08166](https://arxiv.org/abs/1810.08166))

* Gustavo Arciniega, Pablo Bueno, Pablo A. Cano, Jose D. Edelstein, Robie A. Hennigar, Luisa G. Jaimem, _Geometric Inflation_ ([arXiv:1812.11187](https://arxiv.org/abs/1812.11187))

Discussion of [[eternal inflation]] in Starobinsky-type models

* {#BarenboimKinneyPark16} Gabriela Barenboim, [[William Kinney]], Wan-Il Park, _Eternal Hilltop Inflation_,  Journal of Cosmology and Astroparticle Physics, Volume 2016, May 2016 ([arXiv:1601.08140](https://arxiv.org/abs/1601.08140))

See also:

* Dhong Yeon Cheong, Hyun Min Lee, Seong Chan Park, _Beyond the Starobinsky model for inflation_ ([arXiv:2002.07981](https://arxiv.org/abs/2002.07981))



### Embedding into supergravity
 {#ReferencesEmbeddingIntoSupergravity}

Discussion of embedding of Starobinsky inflation in [[supergravity]] originates in 

* {#Cecotti87} S. Cecotti, _Higher derivative supergravity Is equivalent to standard supergravity coupled to matter_, Phys. Lett. B 190, 86 (1987).

* S. Cecotti, [[Sergio Ferrara]], M. Porrati and S. Sabharwal, Nucl. Phys. B 306, 160 (1988).

and is further developed in the following articles:

* [[Sergei Ketov]], _Supergravity and Early Universe: the Meeting Point of Cosmology and High-Energy Physics_, Int.J.Mod.Phys. A28 (2013) 1330021 ([arXiv:1201.2239](http://arxiv.org/abs/arXiv:1201.2239))

* [[John Ellis]], [[Dimitri Nanopoulos]], [[Keith Olive]], _No-Scale Supergravity Realization of the Starobinsky Model of Inflation_ Phys. Rev. Lett. 111, 111301 (2013) ([arXiv:1305.1247](http://arxiv.org/abs/1305.1247))

* [[Renata Kallosh]], [[Andrei Linde]], _Superconformal generalizations of the Starobinsky model_ JCAP 1306, 028 (2013) ([arXiv:1306.3214](http://arxiv.org/abs/1306.3214))


* [[John Ellis]], [[Dimitri Nanopoulos]], [[Keith Olive]], _Starobinsky-like Inflationary Models as Avatars of No-Scale Supergravity_ JCAP 1310, 009 (2013) ([arXiv:1307.3537](http://arxiv.org/abs/1307.3537))


* {#FKR13} [[Fotis Farakos]], [[Alex Kehagias]], A. Riotto, _On the Starobinsky Model of Inflation from Supergravity_, Nucl. Phys. B 876, 187 (2013) ([arXiv:1307.1137](http://arxiv.org/abs/1307.1137))


* [[Sergio Ferrara]], [[Renata Kallosh]], [[Andrei Linde]] and M. Porrati, _Minimal Supergravity Models of Inflation_ ([arXiv:1307.7696](http://arxiv.org/abs/1307.7696))


* [[Andrei Linde]] and M. Porrati, _Higher Order Corrections in Minimal Supergravity Models of Inflation_ ([arXiv:1309.1085](http://arxiv.org/abs/1309.1085))

* [[Sergio Ferrara]], [[Renata Kallosh]], [[Antoine Van Proeyen]], _On the Supersymmetric Completion of R+R2 Gravity and Cosmology_ JHEP 1311, 134 (2013) ([arXiv:1309.4052](http://arxiv.org/abs/1309.4052))

* [[Sergei Ketov]], Takahiro Terada, _Old-minimal supergravity models of inflation_, JHEP12(2013)040 ([arXiv:1309.7494](https://arxiv.org/abs/1309.7494))

* [[Sergio Ferrara]]], [[Pietro Fre]] and A. S. Sorin, _On the Topology of the Inflaton Field in Minimal Supergravity Models_ ([arXiv:1311.5059](http://arxiv.org/abs/1311.5059))

* {#AlexandreHoustonMavromatos14} Jean Alexandre, Nick Houston, Nick E. Mavromatos, _Starobinsky-type Inflation in Dynamical Supergravity Breaking Scenarios_, Phys. Rev. D 89, 027703 (2014) ([arXiv:1312.5197](https://arxiv.org/abs/1312.5197))

  via [[gravitino condensation]], based on

  * Jean Alexandre, Nick Houston, Nick E. Mavromatos, _Dynamical Supergravity Breaking via the Super-Higgs Effect Revisited_, Phys. Rev. D 88, 125017 (2013) ([arXiv:1310.4122](https://arxiv.org/abs/1310.4122))

  * Jean Alexandre, Nick Houston, Nick E. Mavromatos, _Inflation via Gravitino Condensation in Dynamically Broken Supergravity_,  International Journal of Modern Physics D, Volume 24, Issue 04, April 2015 ([arXiv:1409.3183](https://arxiv.org/abs/1409.3183))

* [[Sergei Ketov]], [[Aleksei Starobinsky]], _Inflation and non-minimal scalar-curvature coupling in gravity and supergravity_, JCAP 1208, 022 (2012) ([arXiv:1203.0805](https://arxiv.org/abs/1203.0805))

* [[Sergei Ketov]], S. Tsujikawa, _Consistency of inflation and preheating in $F(R)$ supergravity_, Phys. Rev. D 86, 023529 (2012) ([arXiv:1205.2918](https://arxiv.org/abs/1205.2918)) 

* [[Sergei Ketov]], _On the supersymmetrization of inflation in $f(R)$ gravity_,Prog. Theor. Exp. Phys. 2013, 123B04 ([arXiv:1309.0293](https://arxiv.org/abs/1309.0293))


* [[Sergio Ferrara]], [[Alex Kehagias]], Antonio Riotto, _The Imaginary Starobinsky Model and Higher Curvature Corrections_ ([arXiv:1405.2353](http://arxiv.org/abs/1405.2353))

* {#FerrarKehagias14} [[Sergio Ferrara]], [[Alex Kehagias]], _Higher Curvature Supergravity, Supersymmetry Breaking and Inflation_ ([arXiv:1407.5187](http://arxiv.org/abs/1407.5187))

* {#DFKRU14} [[Ioannis Dalianis]], [[Fotis Farakos]], [[Alex Kehagias]], A. Riotto, [[Rikard von Unge]], _Supersymmetry Breaking and Inflation from Higher Curvature Supergravity_ ([arXiv:1409.8299](http://arxiv.org/abs/1409.8299))


* {#DalianisFarakos15} [[Ioannis Dalianis]], [[Fotis Farakos]], _On the initial conditions for inflation with plateau potentials: the $R + R^2$ (super)gravity case_, [Journal of Cosmology and Astroparticle Physics, Volume 2015, July 2015 ](http://iopscience.iop.org/article/10.1088/1475-7516/2015/07/044/meta), ([arXiv:1502.01246](http://arxiv.org/abs/1502.01246))

* Spyros Basilakos, Nick E. Mavromatos, Joan Sola, _Starobinsky-like inflation and running vacuum in the context of Supergravity_ ([arXiv:1505.04434](https://arxiv.org/abs/1505.04434))

  > In this paper we have shown that SUGRA models with a dynamically induced massive gravitino phase lead to the RVM behavior and therefore provide a strong support for a fundamental description of the cosmic history.

* Andrea Addazi, [[Sergei Ketov]], _Energy conditions in Starobinsky supergravity_ ([arXiv:1701.02450](https://arxiv.org/abs/1701.02450))

* [[John Ellis]], Dimitri V. Nanopoulos, [[Keith Olive]], _From $R^2$ Gravity to No-Scale Supergravity_, Phys. Rev. D 97, 043530 (2018) ([arXiv:1711.11051](https://arxiv.org/abs/1711.11051))

* Hiroyuki Abe, Yermek Aldabergenov, Shuntaro Aoki, [[Sergei Ketov]], _Massive vector multiplet with Dirac-Born-Infeld and new Fayet-Iliopoulos terms in supergravity_ ([arXiv:1808.00669](https://arxiv.org/abs/1808.00669))

* Sergey Ketov, Maxim Khlopov, _Extending Starobinsky inflationary model in gravity and supergravity_ ([arXiv:1809.09975](https://arxiv.org/abs/1809.09975))

* {#ENOV19} [[John Ellis]], [[Dimitri Nanopoulos]], [[Keith Olive]], Sarunas Verner, _A Unified No-Scale Model of Modulus Fixing, Inflation, Supersymmetry Breaking and Dark Energy_, Phys. Rev. D 100, 025009 (2019) ([arXiv:1903.05267](https://arxiv.org/abs/1903.05267), [doi:10.1103/PhysRevD.100.025009](https://doi.org/10.1103/PhysRevD.100.025009))

* Yermek Aldabergenov, Shuntaro Aoki, [[Sergei Ketov]], _Minimal Starobinsky supergravity coupled to dilaton-axion superfield_ ([arXiv:2001.09574](https://arxiv.org/abs/2001.09574))


* [[John Ellis]], Marcos A. G. Garcia, Natsumi Nagata, [[Dimitri Nanopoulos]], [[Keith Olive]], Sarunas Verner, _Building Models of Inflation in No-Scale Supergravity_ ([arXiv:2009.01709](https://arxiv.org/abs/2009.01709))

* N. E. Martínez-Pérez, C. Ramírez, V. Vázquez-Báez, *FRW supersymmetric model of Starobinsky* ([arXiv:2110.00556](https://arxiv.org/abs/2110.00556))


### Embedding into 11d supergravity
 {#ReferencesEmbeddingInto11dSupergravity}

Discussion of Starobinsky inflation in [[11-dimensional supergravity]] with its [[higher curvature corrections]] included (see [there](11-dimensional+supergravity#HigherCurvatureCorrection)):

* [[Katrin Becker]], [[Melanie Becker]], _Supersymmetry Breaking, M-Theory and Fluxes_, JHEP 0107:038,2001 ([arXiv:hep-th/0107044](https://arxiv.org/abs/hep-th/0107044))

* {#HiragaHyakutake18} Kazuho Hiraga, Yoshifumi Hyakutake, _Inflationary Cosmology via Quantum Corrections in M-theory_ ([arXiv:1809.04724](https://arxiv.org/abs/1809.04724))

* Kazuho Hiraga, Yoshifumi Hyakutake, _Scalar Cosmological Perturbations in M-theory with Higher Derivative Corrections_ ([arxiv:1910.12483](https://arxiv.org/abs/1910.12483))


### Embedding into superstring theory
 {#ReferencesEmbeddingIntoStringTheory}

Embedding of Starobinsky inflation into [[superstring theory]] is discussed in

* [[Costas Kounnas]], [[Dieter Luest]], Nicolaos Toumbas, _$\mathcal{R}^2$ inflation from scale invariant supergravity and anomaly free superstrings with fluxes_ ([arXiv:1409.7076](http://arxiv.org/abs/1409.7076))

* [[Ralph Blumenhagen]], Anamaria Font, Michael Fuchs, Daniela Herschmann, Erik Plauschinn, _Towards Axionic Starobinsky-like Inflation in String Theory_, Physics Letters B Volume 746, 30 June 2015, Pages 217&#8211;222 ([arXiv:1503.01607](https://arxiv.org/abs/1503.01607))

* {#EllisCarciaNanopoulosOlive15} [[John Ellis]], Marcos A. G. Garcia, [[Dimitri Nanopoulos]], [[Keith Olive]], _Phenomenological Aspects of No-Scale Inflation Models_ ([arXiv:1503.08867](http://arxiv.org/abs/1503.08867))

* [[Luis Alvarez-Gaume]], [[Alex Kehagias]], [[Costas Kounnas]], [[Dieter Luest]], Antonio Riotto, _Aspects of Quadratic Gravity_ ([arXiv:1505.07657](http://arxiv.org/abs/1505.07657))

* Benedict Broy, David Ciupke, FranciscoG. Pedro, Alexander Westphal, _Starobinsky-Type Inflation from $\alpha'$-Corrections_, JCAP01(2016)001 ([arXiv:1509.00024](https://arxiv.org/abs/1509.00024))

* K. Sravan Kumar, _Inflaton candidates: from string theory to particle physics_, PhD thesis ([arXiv:1808.03701](https://arxiv.org/abs/1808.03701))

[[!redirects Starobinsky inflation]]
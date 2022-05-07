

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

According to the [classification of superconformal symmetry](supersymmetry#ClassificationSuperconformal), there should exist [[superconformal field theories]] in 6 dimensions...

[[!include superconformal symmetry -- table]]

...with $(2,0)$-[[supersymmetry]], that contain a [[self-dual higher gauge theory]] whose field configurations are [[connections on a 2-bundle]] (a [[circle n-bundle with connection|circle 2-bundle with connection]] in the abelian case).

In ([Claus-Kallosh-Proeyen 97](#ClausKalloshProeyen97)) such has been derived, in the abelian case and to low order, as the small fluctuations of the [[Green-Schwarz sigma-model]] of the [[M5-brane]] around the embedding in the [[asymptotic boundary]] of the [[AdS-spacetime]] that is the [[near-horizon geometry]] of the [[black brane|black]] M5-brane.

In accord with this the [AdS7-CFT6](AdS-CFT#AdS7CFT6) correspondence predicts that the nonabelian 6d theory is the corresponding theory for $N$ coincident M5-branes.

In the non-abelian case it is expected ([Witten 07](#Witten07)) that the compactification of such theories are at the heart of the phenomenon that leads to [[S-duality]] in [[super Yang-Mills theory]] and further to [[geometric Langlands duality]] ([Witten 09](#Witten09)).

Due to the [[self-dual higher gauge theory|self-duality]] a characterization of these theories by an [[action functional]] is subtle. Therefore more direct descriptions are still under investigation (for instance [SSW11](#SSW11)). Review includes ([Moore11](#Moore11), [Moore 12](#Moore12)).

## Properties

### Geometric engineering
  {#GeometricEngineering}

For [[geometric engineering]] of the [[6d (2,0)-superconformal QFT]], see at _[duality between M-theory on Z2-orbifolds and type IIB string theory on K3-fibrations -- Geometric engineering of 6d (2,0)-SCFT](duality+between+M-theory+on+Z2-orbifolds+and+type+IIB+string+theory+on+K3-fibrations#GeometricEngineeringOfThe6d2SuperconformalQFT)_.


### Holographic dual

Under [[AdS-CFT|AdS7/CFT6]] the 6d $(2,0)$-superconformal QFT is supposed to be dual to [[11-dimensional supergravity|M-theory]] on [[anti de Sitter spacetime]] $AdS_7 \times S^4$.  

See [[AdS/CFT correspondence]] for more on this.


### Realization of quantum chromodynamics

See at _[[AdS-QCD correspondence]]_.

### Solitonic 1-branes

The 5d $(2,0)$-[[SCFT]] has tensionless 1-[[brane]] configurations. From the point of view of the ambient [[11-dimensional supergravity]] these are the boundaries of [[M2-branes]] ending on the [[M5-branes]]. ([GGT](#GGT))

### Compactification on a Riemann surface and AGT correspondence
 {#CompactificationOnARiemannSurface}

\begin{imagefromfile}
  "file_name": "6d_qft_graph.gif",
  "width": 600,
  "float": "right",
  "margin": {
    "top": 0,
    "right": 20,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  },
  "alt": "Compactification diagram"
\end{imagefromfile}


> (graphics taken from ([Workshop 14](#Workshop14)))


The [[Kaluza-Klein mechanism|compactification]] of the 5-brane on a [[Riemann surface]] yields as [[worldvolume]] [[theory (physics)|theory]] [[N=2 D=4 super Yang-Mills theory]]. See at _[N=2 D=4 SYM -- Construction by compactification of 5-branes](N%3D2+D%3D4+super+Yang-Mills+theory#ConstructionByCompactificationOf5Branes)_.

The _[[AGT correspondence]]_ relates  the [[partition function]] of $SU(2)^{n+3g-3}$-[[N=2 D=4 super Yang-Mills theory]] obtained by [[Kaluza-Klein mechanism|compactifying]] the $6d$ M5-brane theory on a [[Riemann surface]] $C_{g,n}$ of [[genus]] $g$ with $n$ punctures to 2d [[Liouville theory]] on $C_{g,n}$. 

More generally, this kind of construction allows to describe the 6d (2,0)-theory as a "[[2d SCFT]] with values in [[super Yang-Mills theory|4d SYM]]". See at _[[AGT correspondence]]_ for more on this.


### Twistor space description

Famously the solutions to [[self-dual Yang-Mills theory]] in [[dimension]] 4 can be obtained as images of degree-2 cohomology classes under the [[Penrose-Ward twistor transform]]. Since the 6d QFT on the [[M5-brane]] contains a 2-form [[self-dual higher gauge field]] it seems natural to expect that it can be described by a higher analogy of the twistor transform. For references exploring this idea see at _[twistor space -- References -- Application to the self-dual 2-form field in 6d](twistor+space#ReferencesApplicationToSelfDual2FormField)_.

## Related entries

* [[little string theory]]

* [[D=6 N=(1,0) SCFT]]

* [[D=6 supergravity]]

* [[D=2 N=(2,0) SCFT]]

* [[D=5 super Yang-Mills theory]]

* [[M5-brane elliptic genus]]

[[!include gauge theory from AdS-CFT -- table]]

[[!include superconformal symmetry -- table]]


## References

### General

The first indication of a 6d theory with a self-dual 2-form field appears in  

* {#Witten95} [[Edward Witten]], section 1 of _Some comments on string dynamics_ ([hepth/9507121](http://arxiv.org/abs/hep-th/9507121))

Derivation of the abelian 6d theory to low order as the small fluctuations of the [[Green-Schwarz sigma-model]] of the [[M5-brane]] around a solution embedding as the asymptotic boundary of the [[AdS-spacetime]] [[near-horizon geometry]] of a [[black brane|black]] 5-brane is due to 

* {#ClausKalloshProeyen97} P. Claus, [[Renata Kallosh]], [[Antoine Van Proeyen]], _M 5-brane and superconformal $(0,2)$ tensor multiplet in 6 dimensions_, Nucl.Phys. B518 (1998) 117-150 ([arXiv:hep-th/9711161](http://arxiv.org/abs/hep-th/9711161))


General survey includes

* {#Moore11} [[Greg Moore]], _On the role of six&#8208;dimensional $(2,0)$-theories in recent developments in Physical Mathematics_, talk at [Strings 2011](http://www2.physics.uu.se/external/strings2011/) ([pdf slides](http://www.physics.rutgers.edu/~gmoore/Strings2011FinalPDF.pdf))
  
* {#Moore12} [[Greg Moore]], _Applications of the six-dimensional (2,0) theories to Physical Mathematics_, [Felix Klein lectures Bonn (2012)](http://www.hcm.uni-bonn.de/events/eventpages/felix-klein-lectures/applications-of-the-six-dimensional-20-theories-to-physical-mathematics/) ([pdf](http://www.physics.rutgers.edu/~gmoore/FelixKleinLectureNotes.pdf), [[MooreKleinLectures12.pdf:file]])


* {#Workshop14}  [[Qiaochu Yuan]]: _[lecture notes](https://math.berkeley.edu/~qchu/Notes/6d/)_ for _[Mathematical Aspects of Six-Dimensional Quantum Field Theories](http://www.math.northwestern.edu/~celliott/workshop/)_, Berkeley, December 8th-12th, 2014 at the University of California, Berkeley

Discussion of [[anomaly cancellation]]:

* [[Kantaro Ohmori]], [[Hiroyuki Shimizu]], [[Yuji Tachikawa]], Kazuya Yonekura, _Anomaly polynomial of general 6d SCFTs_, Progress of Theoretical and Experimental Physics, Volume 2014, Issue 10, October 2014, 103B07 ([arXiv:1408.5572](https://arxiv.org/abs/1408.5572))

* [[Hiroyuki Shimizu]], _Aspects of anomalies in 6d superconformal field theories_, Tokyo 2018 ([spire:1802462](https://inspirehep.net/literature/1802462), [[ShimizuAnomaliesIn6dSCFT.pdf:file]])

Construction from [[F-theory]] [[KK-compactification]] is reviewed in 

* {#HeckmanRudelius18} [[Jonathan Heckman]], [[Tom Rudelius]], _Top Down Approach to 6D SCFTs_, J. Phys. A: Math. Theor. 52 093001 2018 ([arXiv:1805.06467](https://arxiv.org/abs/1805.06467), [doi:10.1088/1751-8121/aafc81](https://doi.org/10.1088/1751-8121/aafc81))

New approach to construction of candidate [[Lagrangian densities]] for [[D=6 N=(2,0) SCFTs]]:


* [[Neil Lambert]], _$(2,0)$ Lagrangian Structures_, Physics Letters B Volume 798, 10 November 2019, 134948 ([arXiv:1908.10752](https://arxiv.org/abs/1908.10752))


 
See also the references and discussion at _[[M5-brane]]_.

### Compactification to 5d super-Yang-Mills

[[KK-compactification]] on [[circle]] [[fibers]] to [[D=5 super Yang-Mills theory]] is discussed in (see also at [[Perry-Schwarz Lagrangian]]):

* [[Nathan Seiberg]], Sec. 7 of _Notes on Theories with 16 Supercharges_, Nucl. Phys. Proc. Suppl. 67:158-171, 1998 ([arXiv:hep-th/9705117](https://arxiv.org/abs/hep-th/9705117))

* {#Douglas11} [[Michael Douglas]], _On D=5 super Yang-Mills theory and (2,0) theory_, JHEP 1102:011, 2011 ([arXiv:1012.2880](https://arxiv.org/abs/1012.2880))

* [[Neil Lambert]], Constantinos Papageorgakis, Maximilian Schmidt-Sommerfeld, _M5-Branes, D4-Branes and Quantum 5D super-Yang-Mills_, JHEP 1101:083, 2011 ([arXiv:1012.2882](https://arxiv.org/abs/1012.2882))

* {#Witten11} [[Edward Witten]], Sections 4 and 5 of _Fivebranes and Knots_ ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216)) 

* {#Hu13} Shan Hu, _6D $(2,0)$ theory and M5 branes: A KK mode approach_, 2013 ([hdl:1969.1/151094](http://hdl.handle.net/1969.1/151094))


* [[Chris Hull]], [[Neil Lambert]], _Emergent Time and the M5-Brane_, JHEP06(2014)016 ([arXiv:1403.4532](https://arxiv.org/abs/1403.4532))

* [[Andreas Gustavsson]], _Five-dimensional Super-Yang-Mills and its Kaluza-Klein tower_. JHEP01(2019)222 ([arXiv:1812.01897](https://arxiv.org/abs/1812.01897))

* {#Lambert19} [[Neil Lambert]], Sec. 3.1 and 3.4.3. of _Lessons from M2's and Hopes for M5's_, _Proceedings of the [LMS-EPSRC Durham Symposium](http://www.maths.dur.ac.uk/lms/):_ _[Higher Structures in M-Theory](http://www.maths.dur.ac.uk/lms/109/index.html), August 2018_ Fortschritte der Physik Volume 67, Issue 8-9 2019 ([arXiv:1903.02825](https://arxiv.org/abs/1903.02825), [doi:10.1002/prop.201910011]( https://doi.org/10.1002/prop.201910011), [slides pdf](http://www.maths.dur.ac.uk/lms/109/talks/1877lambert.pdf), [video recording](http://www.maths.dur.ac.uk/lms/109/movies/1877lamb.mp4))


### Compactification to 4d super-Yang-Mills

[[KK-compactification]] on [[torus]] [[fibers]] to [[D=4 super Yang-Mills theory]] and the related [[electric-magnetic duality]]/[[S-duality]] in 4-dimensions is discussed in

* {#Witten07} [[Edward Witten]], _[[Conformal field theory in four and six dimensions]]_ in [[Ulrike Tillmann]] (ed.) _Topology, geometry and quantum field theory_ LMS Lecture Note Series (2004) ([arXiv:0712.0157](http://arxiv.org/abs/0712.0157))
 

and the resulting relation to the [[geometric Langlands correspondence]] is disucssed in 

* {#Witten09} [[Edward Witten]], _Geometric Langlands From Six Dimensions_, in Peter Kotiuga (ed.) _A Celebration of the Mathematical Legacy of Raoul Bott_, CRM Proceedings & Lecture Notes Volume: 50, AMS 2010 ([arXiv:0905.2720](http://arxiv.org/abs/0905.2720), [ISBN:978-0-8218-4777-0](https://bookstore.ams.org/crmp-50))
 

For more references on this see at _[[N=2 D=4 super Yang-Mills theory]]_ the section _[References - Constructions from 5-branes](N%3D2+D%3D4+super+Yang-Mills+theory#ConstructionByCompactificationOf5Branes)_.

Relation to [[BFSS matrix model]] on [[tori]]:

* [[Micha Berkooz]], [[Moshe Rozali]], [[Nathan Seiberg]], _Matrix Description of M-theory on $T^3$ and $T^5$_ ([arXiv:hep-th/9704089](http://arxiv.org/abs/hep-th/9704089))

The [[KK-compactification]] specifically of the [[D=6 N=(1,0) SCFT]] to [[D=4 N=1 super Yang-Mills]]:

* Ibrahima Bah, Christopher Beem, Nikolay Bobev, Brian Wecht, _Four-Dimensional SCFTs from M5-Branes_ ([arXiv:1203.0303](http://arxiv.org/abs/1203.0303))

* Shlomo S. Razamat, [[Cumrun Vafa]], Gabi Zafrir, _$4d$ $\mathcal{N} = 1$ from $6d (1,0)$_, J. High Energ. Phys. (2017) 2017: 64 ([arXiv:1610.09178](https://arxiv.org/abs/1610.09178))

* Ibrahima Bah, [[Amihay Hanany]], Kazunobu Maruyoshi, Shlomo S. Razamat, Yuji Tachikawa, Gabi Zafrir, _$4d$ $\mathcal{N}=1$ from $6d$ $\mathcal{N}=(1,0)$ on a torus with fluxes_ ([arXiv:1702.04740](https://arxiv.org/abs/1702.04740))

* Hee-Cheol Kim, Shlomo S. Razamat, [[Cumrun Vafa]], Gabi Zafrir, _E-String Theory on Riemann Surfaces_, Fortsch. Phys. ([arXiv:1709.02496](https://arxiv.org/abs/1709.02496))

* Hee-Cheol Kim, Shlomo S. Razamat, [[Cumrun Vafa]], Gabi Zafrir, _D-type Conformal Matter and SU/USp Quivers_, JHEP06(2018)058 ([arXiv:1802.00620](https://arxiv.org/abs/1802.00620))

* Hee-Cheol Kim, Shlomo S. Razamat, [[Cumrun Vafa]], Gabi Zafrir, _Compactifications of ADE conformal matter on a torus_, JHEP09(2018)110 ([arXiv:1806.07620](https://arxiv.org/abs/1806.07620))

* Shlomo S. Razamat, Gabi Zafrir, _Compactification of 6d minimal SCFTs on Riemann surfaces_, Phys. Rev. D 98, 066006 (2018) ([arXiv:1806.09196](https://arxiv.org/abs/1806.09196))

* Jin Chen, Babak Haghighat, Shuwei Liu, [[Marcus Sperling]], _4d N=1 from 6d D-type N=(1,0)_ ([arXiv:1907.00536](https://arxiv.org/abs/1907.00536))


### ADE classification

Discussion of the [[ADE classification]] of the 6d theories includes, after ([Witten95](#Witten95))

* Julie D. Blum, [[Kenneth Intriligator]], _New Phases of String Theory and 6d RG Fixed Points via Branes at Orbifold Singularities_, Nucl.Phys.B506:199-222,1997 ([arXiv:hep-th/9705044](http://arxiv.org/abs/hep-th/9705044))

* {#HeckmannMorrisonVafa13} [[Jonathan Heckman]], [[David Morrison]], [[Cumrun Vafa]], _On the Classification of 6D SCFTs and Generalized ADE Orbifolds_ ([arXiv:1312.5746](http://arxiv.org/abs/1312.5746))


### Models and special properties
 {#ModelsAndSpecialProperties}

Realization of the 6d theory in [[F-theory]] is discussed in ([Heckmann-Morrison-Vafa 13](#HeckmannMorrisonVafa13)).

A proposal for related higher nonabelian differential form data is made in 


* {#SSW11} [[Henning Samtleben]], Ergin Sezgin, Robert Wimmer, _(1,0) superconformal models in six dimensions_ ([arXiv:1108.4060](http://arxiv.org/abs/1108.4060))
 

Since by [[transgression]] every nonabelian [[principal 2-bundle]]/[[gerbe]] gives rise to some kind of nonabelian 1-bundle on [[loop space]] it is clear that some parts (but not all) of the nonabelian gerbe theory on the 5-brane has an equivalent reformulation in terms of ordinary gauge theory on the [[loop space]] of the 5-brane and possibly for gauge group the [[loop group]] of the original gauge group. 

Comments along these lines have been made in 

* [[Andreas Gustavsson]], _Selfdual strings and loop space Nahm equations_ ([arXiv:0802.3456](http://arxiv.org/abs/0802.3456)).

In fact, via the [[strict 2-group]] version of the [[string 2-group]] there is a local gauge in which the loop group variables appear already before transgression of the 5-brane gerbe to loop space. This is discussed from a [[holographic principle|holographic]] point of view in

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane]]_ 

### On the holographic dual 
 {#ReferencesOnTheHolographicDual}

The basics of the relation of the 6d theory to a 7d theory under [[AdS-CFT]] is reviewed [[holographic principle|holographic duality]]


* {#Maldacena} [[Juan Maldacena]], _The Large N limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys. 2:231, 1998, [hep-th/9711200](http://arxiv.org/abs/hep-th/9711200); _Wilson loops in Large N field theories_, Phys. Rev. Lett. __80__ (1998) 4859, [hep-th/9803002](http://arxiv.org/abs/hep-th/9803002)
 

The argument that the abelian [[7d Chern-Simons theory]] of a [[circle n-bundle with connection|3-connection]] yields this way the [[conformal blocks]] of the abelian [[self-dual higher gauge theory]] of the 6d theory on a _single_ brane is due to

* {#WittenI} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ J. Geom. Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 

* {#Witten98} [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ JHEP 9812:012,1998 ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012)) 
 

The nonabelian generalization of this 7d action functional that follows from taking the quantum corrections ([[Green-Schwarz mechanism]] and flux quantization) of the [[supergravity C-field]] into account is discussed in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane]]_

See also

* {#HEGK} [[Eric D'Hoker]], John Estes, Michael Gutperle, Darya Krym, 

  _Exact Half-BPS Flux Solutions in M-theory I
Local Solutions_ ([arXiv:0806.0605](http://arxiv.org/abs/0806.0605))

   _Exact Half-BPS Flux Solutions in M-theory II: Global solutions asymptotic to $AdS_7 \times S^4$ ([arXiv:0810.4647](http://arxiv.org/abs/0810.4647))
  

### Solitonic 1-brane excitations

* {#GGT} [[Jerome Gauntlett]], [[Joaquim Gomis]], [[Paul Townsend]], _BPS Bounds for Worldvolume Branes_ ([arXiv:hep-th/9711205](http://arxiv.org/abs/hep-th/9711205))
 

* [[Paul Howe]], [[Neil Lambert]], [[Peter West]], _The Threebrane Soliton of the M-Fivebrane_ ([arXiv:hep-th/9710033](http://arxiv.org/abs/hep-th/9710033))





[[!include D=6 N=(2,0) SCFT as an extended functorial field theory -- references]]






[[!redirects 6d (2,0)-susy QFT]]
[[!redirects 6d (2,0)-superconformal QFT]]

[[!redirects 6d (2,0)-superconformal field theory]]
[[!redirects 6d (2,0)-superconformal field theories]]

[[!redirects 6d (2,0)-superconformal SCFT]]
[[!redirects 6d (2,0)-superconformal SCFTs]]

[[!redirects 6d superconformal gauge field theory]]
[[!redirects 6d superconformal gauge field theories]]

[[!redirects D=6 N=(2,0) SCFT]]
[[!redirects D=6 N=(2,0) SCFTs]]

[[!redirects D=6 N=(1,1) SCFT]]

[[!redirects 6d (2,0)-supersymmetric QFT]]

[[!redirects 6dN20SCFT]]



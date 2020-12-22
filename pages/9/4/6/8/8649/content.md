
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

### For monopole charges in electromagnetism

If the field of [[electromagnetism]] serves as a [[background gauge field]] for electrically charged [[quantum mechanics|quantum]] [[particles]] it is subject to a _quantization condition_: Outside the locus of any [[magnetic charge]] -- for instance a magnetic [[monopole]] [[topological defect]] -- the [[electromagnetic field]] must be a [[circle bundle with connection|connection on a principal U(1) bundle]] whose [[first Chern class]] is the discrete measure for the units of magnetic charge. Equivalently this means that the [[electromagnetic field]] is a [[cocycle]] in [[ordinary differential cohomology]] of degree 2.

In the underlying topological sector ("[[monopole]]"/"[[instantons]]"-sector) this is [[integral cohomology]] in degree-2, whose [[classifying space]] is equivalently the [[infinite complex projective space]] $B U(1) \simeq \mathbb{C}P^\infty$:

{#Illustration} $\,$

<center>
<img src="https://ncatlab.org/nlab/files/DiracChargeQuantizationII.jpg" width="640">
</center>

This goes back to an insight due to [Dirac 31](#Dirac31). See [Heras 18](#Heras18) for traditional elementary review, but see [Alvarez 85](#Alvarez85),  [Frankel](#Frankel) and [Mangiarotti-Sardanashvily 00](#MangiarottiSardanashvily00) for exposition of the modern picture in terms of [[fiber bundles in physics]]. See [Freed 00, Section 2](#Freed00) for review in terms of [[differential cohomology]] with outlook to generalization to [[higher gauge fields]] in [[string theory]] (more on which in the references [below](#ReferencesForBFieldAndRRFields)).

A closely related phenomenon is the magnetic flux quantization in [[type II superconductors]], see [there](superconductivity#MagneticFluxQuantizationInTypeIISuperconductors).

On the locus of the magnetic charge itself the situation is more complex. There the [[magnetic current]] is given by a cocycle in [[ordinary differential cohomology]] of degree 3 (with compact support) and now the electromagnetic field is a connection on a [[twisted bundle]] ([Freed 00, Section 2](#Freed00)).

\linebreak

### For monopole charges in non-abelian Yang-Mills theory

A similar charge quantization condition govers [[monopoles]] in [[SU(2)]]-[[Yang-Mills theory]], see at _[[moduli space of monopoles]]_. Here the [[Atiyah-Hitchin charge quantization]] ([Atiyah-Hitchin 88, Theorem 2.10](#AtiyahHitchin88)) says that the [[moduli space]] of [[monopoles]] is the [[holomorphic function|complex]]-[[rational function|rational]] 2-[[Cohomotopy]] of an asymptotic 2-sphere enclosing the monopoles:

{#IllustrationAtiyahHitchinQuantization} $\,$


<center>
<img src="https://ncatlab.org/nlab/files/AtiyahHitchinChargeQuantizationII.jpg" width="640">
</center>


### For RR-field D-brane charges in K-theory

See at _[[K-theory classification of D-brane charge]]_

### For the C-field in J-twisted Cohomotopy

See at _[supergravity C-field -- shifted flux quantization condition](supergravity+C-field#ShiftedCFieldFluxQuantizationCondition)_

## Related concepts

* [[fiber bundles in physics]]

* [[monopole]]

  * [[Dirac monopole]], [[Yang monopole]]

* [[moduli space of monopoles]]

\linebreak



## Reference

See also the references at _[[fiber bundles in physics]]_.

### For the electromagnetic field

The original argument for charge quantization of the [[electromagnetic field]] is due to

* {#Dirac31} [[P.A.M. Dirac]], _Quantized Singularities in the Electromagnetic Field_,  Proceedings of the Royal Society, A133 (1931) pp 60--72 ([doi:10.1098/rspa.1931.0130](http://rspa.royalsocietypublishing.org/content/133/821/60.short))

Review:

* {#Alvarez85} [[Orlando Alvarez]], Section 2 of: _Topological quantization and cohomology_, Comm. Math. Phys. Volume 100, Number 2 (1985), 279-309 ([euclid:cmp/1103943448](https://projecteuclid.org/euclid.cmp/1103943448))

* {#Frankel} [[Theodore Frankel]], section 16.4e of _[[The Geometry of Physics - An Introduction]]_, Cambridge University Press 2011 ([doi:10.1017/CBO9781139061377](https://doi.org/10.1017/CBO9781139061377))

* [Freed 00, Section 2](#Freed00)

* {#MangiarottiSardanashvily00} L. Mangiarotti, [[Gennadi Sardanashvily]], _Connections in Classical and Quantum Field Theory_, World Scientific, 2000 ([doi:10.1142/2524](https://doi.org/10.1142/2524))

* {#Heras18} Ricardo Heras, _Dirac quantisation condition: a comprehensive review_, Contemp. Phys. 59, 331 (2018) ([arXiv:1810.13403](https://arxiv.org/abs/1810.13403))

See also 

* Wikipedia, _[Dirac's quantization](https://en.wikipedia.org/wiki/Magnetic_monopole#Dirac%27s_quantization)_

### For the weak nuclear force field

Discussion of the [[moduli space of monopoles]] for [[SU(2)]]-[[Yang-Mills theory]] ([[weak nuclear force]]):

* {#AtiyahHitchin88} [[Michael Atiyah]], [[Nigel Hitchin]], _The geometry and dynamics of magnetic monopoles_  M. B. Porter Lectures. Princeton University Press, Princeton, NJ, 1988 ([jstor:j.ctt7zv206](https://www.jstor.org/stable/j.ctt7zv206))

* {#Segal79} [[Graeme Segal]], _The topology of spaces of rational functions_, Acta Math. Volume 143 (1979), 39-72 ([euclid:1485890033](https://projecteuclid.org/euclid.acta/1485890033))



### For the B-field and RR-field in string theory
 {#ReferencesForBFieldAndRRFields}

Discussion in the broader context of the [[higher gauge fields]] in [[string theory]] ([[B-field]], [[RR-field]]) charge-quantized in [[generalized cohomology theories]] ([[twisted K-theory|twisted]] [[topological K-theory]]):

* {#Freed00} [[Daniel Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_, Surveys in Differential Geometry, Int. Press, Somerville, MA, 2000, pp. 129&#8211;194 ([arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220))

For a comprehensive list of literature in this case see at _[D-brane -- Charge quantization in K-theory](D-brane#ReferencesKTheoryDescription)_.

The idea that [[D-brane charge]] should be quantized in [[topological K-theory]] originates with these articles:

* [[Ruben Minasian]], [[Gregory Moore]], _K-theory and Ramond-Ramond charge_, JHEP9711:002,1997 ([arXiv:hep-th/9710230](http://arxiv.org/abs/hep-th/9710230))

* {#Witten98} [[Edward Witten]], _D-Branes And K-Theory_, JHEP 9812:019,1998 ([arXiv:hep-th/9810188](http://arxiv.org/abs/hep-th/9810188))

* {#FreedHopkins00} [[Daniel Freed]], [[Michael Hopkins]], _On Ramond-Ramond fields and K-theory_, JHEP 0005 (2000) 044 ([arXiv:hep-th/0002027](http://arxiv.org/abs/hep-th/0002027))

See also at _[[anti-D-brane]]_.

Review of the conjecture:

* [[Jarah Evslin]], _What Does(n't) K-theory Classify?_ ([arXiv:hep-th/0610328](https://arxiv.org/abs/hep-th/0610328))

* [[Stefan Fredenhagen]], _Physical Background to the K-Theory Classification of D-Branes: Introduction and References_ ([doi:10.1007/978-3-540-74956-1_1](https://doi.org/10.1007/978-3-540-74956-1_1)), chapter in: [[Dale Husemoeller]], [[Michael Joachim]], [[Branislav Jurčo]], [[Martin Schottenloher]],  _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Lecture Notes in Physics, Springer 2008 ([doi:10.1007/978-3-540-74956-1](https://doi.org/10.1007/978-3-540-74956-1), [pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726corr1.pdf))


Discussion of full-blown [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type II string theory]] 

* {#GradySati19a} Daniel Grady, [[Hisham Sati]], _Ramond-Ramond fields and twisted differential K-theory_ ([arXiv:1903.08843](https://arxiv.org/abs/1903.08843))

Discussion of full-blown [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[KO-theory|orthogonal]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type I string theory]] (on [[orientifolds]]):

* {#GradySati19b} Daniel Grady, [[Hisham Sati]], _Twisted differential KO-theory_ ([arXiv:1905.09085](https://arxiv.org/abs/1905.09085))



{#KTheorySubtleties} But there remain conceptual issues with the proposal that D-brane  charge is in K-theory, as highlighted for in

* {#BDHKMMS01} [[Jan de Boer]], [[Robbert Dijkgraaf]], [[Kentaro Hori]], [[Arjan Keurentjes]], [[John Morgan]], [[David Morrison]], [[Savdeep Sethi]], section 4.5 and 4.6.5 of  _Triples, Fluxes, and Strings_, Adv.Theor.Math.Phys. 4 (2002) 995-1186 ([arXiv:hep-th/0103170](https://arxiv.org/abs/hep-th/0103170))

* {#Evslin06} [[Jarah Evslin]], section 8 of _What Does(n't) K-theory Classify?_, Second Modave Summer School in Mathematical Physics ([arXiv:hep-th/0610328](https://arxiv.org/abs/hep-th/0610328))

In particular, actual checks of the proposal that D-brane charge is given by K-theory, via concrete computation in [[boundary conformal field theory]], have revealed some subtleties:

* [[Stefan Fredenhagen]], [[Thomas Quella]], _Generalised permutation branes_, JHEP0511:004, 2005 ([arXiv:hep-th/0509153](https://arxiv.org/abs/hep-th/0509153))

  > It might surprise that despite all the progress that has been made in understanding branes on group manifolds, there are usually not enough D-branes known to explain the whole charge group predicted by (twisted) K-theory.

Further review and discussion of D-brane charge in K-theory includes the following

* {#OlsenSzabo00} Kasper Olsen, [[Richard Szabo]], _Brane Descent Relations in K-theory_, Nucl.Phys. B566 (2000) 562-598 ([arXiv:hep-th/9904153](https://arxiv.org/abs/hep-th/9904153))

* Kasper Olsen, [[Richard Szabo]], _Constructing D-Branes from K-Theory_, Adv.Theor.Math.Phys. 3 (1999) 889-1025 ([arXiv:hep-th/9907140](https://arxiv.org/abs/hep-th/9907140))

* [[John Schwarz]], _TASI Lectures on Non-BPS D-Brane Systems_ ([arXiv:hep-th/9908144](https://arxiv.org/abs/hep-th/9908144))

* {#Witten00} [[Edward Witten]], _Overview Of K-Theory Applied To Strings_, Int.J.Mod.Phys.A16:693-706,2001 ([arXiv:hep-th/0007175](https://arxiv.org/abs/hep-th/0007175))

* [[Greg Moore]], _K-Theory from a physical perspective_ ([arXiv:hep-th/0304018](http://arxiv.org/abs/hep-th/0304018))

* [[Juan José Manjarín]], _Topics on D-brane charges with B-fields_, Int.J.Geom.Meth.Mod.Phys. 1 (2004) ([arXiv:hep-th/0405074](http://arxiv.org/abs/hep-th/0405074))

A textbook account of D-brane charge in ([[twisted K-theory|twisted]]) [[topological K-theory]] is 

* [[Dale Husemoeller]], [[Michael Joachim]], [[Branislav Jurco]], [[Martin Schottenloher]], _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Lecture Notes in Physics, Springer 2008  ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726corr1.pdf))

See also for instance

* [[Ilka Brunner]], [[Jacques Distler]], _Torsion D-Branes in Nongeometrical Phases_ ([arXiv:hep-th/0102018](https://arxiv.org/abs/hep-th/0102018))

Discussion of D-branes in [[KK-theory]] is reviewed in

* {#Szabo} [[Richard Szabo]], _D-branes and bivariant K-theory_, Noncommutative Geometry and Physics 3 1 (2013): 131. ([arXiv:0809.3029](http://arxiv.org/abs/0809.3029))
 

based on

* {#ReisSzabo05} Rui Reis, [[Richard Szabo]], _Geometric K-Homology of Flat D-Branes_ ,Commun.Math.Phys. 266 (2006) 71-122 ([arXiv:hep-th/0507043](https://arxiv.org/abs/hep-th/0507043))

* [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_, Commun. Math. Phys. 277:643-706,2008 ([arXiv:hep-th/0607020](http://arxiv.org/abs/hep-th/0607020))

* {#BMRS2} [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]],  _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))
 

* [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]],  _D-branes, KK-theory and duality on noncommutative spaces_, J. Phys. Conf. Ser. 103:012004,2008 ([arXiv:0709.2128](http://arxiv.org/abs/0709.2128))

In particular ([BMRS2](#BMRS2)) discusses the definition and construction of D-brane charge as a generalized [[index]] in [[KK-theory]]. The discussion there focuses on the untwisted case. Comments on the generalization of this to topologicall non-trivial [[B-field]] and hence [[twisted K-theory]] is in

* [[Richard Szabo]], _D-Branes, Tachyons and K-Homology_,  	Mod. Phys. Lett. A17 (2002) 2297-2316 ([arXiv:hep-th/0209210](http://arxiv.org/abs/hep-th/0209210))


Specifically for D-branes in [[WZW models]] see

* [[Peter Bouwknegt]], _A note on equality of algebraic and geometric D-brane charges in WZW models_ ([pdf](http://people.physics.anu.edu.au/~drt105/papers/BR0312259.pdf))

More on this, with more explicit relation to [[noncommutative motives]], is in 

* {#Mahanta09} [[Snigdhayan Mahanta]], _Noncommutative correspondence categories, simplicial sets and pro $C^\ast$-algebras_ ([arXiv:0906.5400](http://arxiv.org/abs/0906.5400))
 

* {#Mahanta11} [[Snigdhayan Mahanta]], _Higher nonunital Quillen $K'$-theory, KK-dualities and applications to topological $\mathbb{T}$-duality_, Journal of Geometry and Physics, Volume 61, Issue 5 2011, p. 875-889.   ([pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf))
 
Discussion of D-brane [[matrix models]] taking these K-theoretic effects into account ([[K-matrix model]]) is in

* {#AsakawaSugimotoTerashima01} T. Asakawa, S. Sugimoto, S. Terashima, _D-branes, Matrix Theory and K-homology_, JHEP 0203 (2002) 034 ([arXiv:hep-th/0108085](https://arxiv.org/abs/hep-th/0108085))

{#ChargeInEquivariantKTheory} The proposal that D-brane charge on [[orbifolds]] is measured in [[equivariant K-theory]] goes back to 

* [Witten 98, section 5.1](#Witten98) 

but it was pointed out that only a subgroup of equivariant K-theory can be physically relevant in

* {#BDHKMMS01} [[Jan de Boer]], [[Robbert Dijkgraaf]], [[Kentaro Hori]], [[Arjan Keurentjes]], [[John Morgan]], [[David Morrison]], [[Savdeep Sethi]], around (137) of  _Triples, Fluxes, and Strings_, Adv.Theor.Math.Phys. 4 (2002) 995-1186 ([arXiv:hep-th/0103170](https://arxiv.org/abs/hep-th/0103170))

Further discussion of [[equivariant K-theory]] for D-branes on [[orbifolds]] includes the following:

* Hugo García-Compeán, _D-branes in orbifold singularities and equivariant K-theory_, Nucl.Phys. B557 (1999) 480-504 ([arXiv:hep-th/9812226](https://arxiv.org/abs/hep-th/9812226))

* [[Matthias Gaberdiel]], [[Bogdan Stefanski]], _Dirichlet Branes on Orbifolds_, Nucl.Phys.B578:58-84, 2000 ([arXiv:hep-th/9910109](https://arxiv.org/abs/hep-th/9910109))

* [[Igor Kriz]], Leopoldo A. Pando Zayas, Norma Quiroz, _Comments on D-branes on Orbifolds and K-theory_, Int.J.Mod.Phys.A23:933-974, 2008 ([arXiv:hep-th/0703122](https://arxiv.org/abs/hep-th/0703122))

* [[Richard Szabo]], [[Alessandro Valentino]], _Ramond-Ramond Fields, Fractional Branes and Orbifold Differential K-Theory_, Commun.Math.Phys.294:647-702, 2010 ([arXiv:0710.2773](https://arxiv.org/abs/0710.2773))

Discussion of [[real K-theory]] for D-branes on [[orientifolds]] includes the following:

The original observation that [[D-brane charge]] for [[orientifolds]] should be in [[KR-theory]] is due to

* [Witten 98, section 5](#Witten98)

and was then re-amplified in

* {#Gukov99} [[Sergei Gukov]], _K-Theory, Reality, and Orientifolds_, Commun.Math.Phys. 210 (2000) 621-639 ([arXiv:hep-th/9901042](https://arxiv.org/abs/hep-th/9901042))

* {#BergmanGimonSugimoto01} [[Oren Bergman]], E. Gimon, [[Shigeki Sugimoto]], _Orientifolds, RR Torsion, and K-theory_, JHEP 0105:047, 2001 ([arXiv:hep-th/0103183](https://arxiv.org/abs/hep-th/0103183))

With further developments in 

* [[Varghese Mathai]], [[Michael Murray]], [[Daniel Stevenson]], _Type I D-branes in an H-flux and twisted KO-theory_, JHEP 0311 (2003) 053 ([arXiv:hep-th/0310164](https://arxiv.org/abs/hep-th/0310164))

Discussion of orbi-orienti-folds using [[equivariant K-theory|equivariant]] [[KO-theory]] is in

* N. Quiroz, [[Bogdan Stefanski]], _Dirichlet Branes on Orientifolds_, Phys.Rev. D66 (2002) 026002 ([arXiv:hep-th/0110041](https://arxiv.org/abs/hep-th/0110041))

* [[Volker Braun]], [[Bogdan Stefanski]], _Orientifolds and K-theory_ ([arXiv:hep-th/0206158](https://arxiv.org/abs/hep-th/0206158))

* H. Garcia-Compean, W. Herrera-Suarez, B. A. Itza-Ortiz, O. Loaiza-Brito, _D-Branes in Orientifolds and Orbifolds and Kasparov KK-Theory_, JHEP 0812:007, 2008 ([arXiv:0809.4238](https://arxiv.org/abs/0809.4238))

An elaborate proposal for the correct flavour of real equivariant K-theory needed for [[orientifolds]] is sketched in

* {#Precis} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))

Discussion of the alleged K-theory classification of D-brane charge in relation to the [[M-theory]] [[supergravity C-field]] is in

* {#DMW00} D. Diaconescu, [[Gregory Moore]], [[Edward Witten]], _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv.Theor.Math.Phys.6:1031-1134,2003 ([arXiv:hep-th/0005090](http://arxiv.org/abs/hep-th/0005090)), summarised in _A Derivation of K-Theory from M-Theory_ ([arXiv:hep-th/0005091](http://arxiv.org/abs/hep-th/0005091))

See also

* {#GarciaUranga05} Inaki Garcia-Etxebarria, [[Angel Uranga]], _From F/M-theory to K-theory and back_, JHEP 0602:008,2006 ([arXiv:hep-th/0510073](https://arxiv.org/abs/hep-th/0510073))


For more on this perspective as 10d type II as a [[self-dual higher gauge theory]] in the boudnary of a kind of [[higher dimensional Chern-Simons theory|11-d Chern-Simons theory]] is in

* {#BelovMooreII} Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv:hep-th/0611020](http://arxiv.org/abs/hep-th/0611020))

More complete discussion of the decomposition of the [[supergravity C-field]] as one passes from 11d to 10d is in 

* {#MathaiSati03} [[Varghese Mathai]], [[Hisham Sati]], _Some Relations between Twisted K-theory and E8 Gauge Theory_, JHEP0403:016,2004 ([arXiv:hep-th/0312033](http://arxiv.org/abs/hep-th/0312033))


### For the C-field in M-theory

Discussion of [[shifted C-field flux quantization]] of the [[C-field]] in [[D=11 supergravity]]/[[M-theory]]:


* {#DFM} E. Diaconescu, [[Dan Freed]], [[Greg Moore]],  _The $M$-theory 3-form and $E_8$-gauge theory_, chapter in [[Haynes Miller]], [[Douglas Ravenel]] (eds.) _Elliptic Cohomology Geometry, Applications, and Higher Chromatic Analogues_, Cambridge University Press 2007 ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069), [doi:10.1017/CBO9780511721489](https:
//doi.org/10.1017/CBO9780511721489))

* {#FreedMoore04} [[Dan Freed]], [[Greg Moore]], _Setting the [[quantum integrand]] of M-theory_, Communications in Mathematical Physics, Volume 263, Number 1, 89-132, ([arXiv:hep-th/0409135](http://arxiv.org/abs/hep-th/0409135), [doi:10.1007/s00220-005-1482-7](https://doi.org/10.1007/s00220-005-1482-7))

* [[Greg Moore]], _Anomalies, Gauss laws, and Page charges in M-theory_ ([arXiv:hep-th/0409158](http://arxiv.org/abs/hep-th/0409158))

* {#FSS12} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]],  _[[schreiber:The moduli 3-stack of the C-field]]_, Communications in Mathematical Physics, Volume 333, Issue 1 (2015), Page 117-151, ([arXiv:1202.2455](http://arxiv.org/abs/1202.2455), [DOI 10.1007/s00220-014-2228-1](http://link.springer.com/article/10.1007%2Fs00220-014-2228-1))

* {#FiSaSc} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane|M5-branes, String 2-connections, and 7d nonabelian Chern-Simons theory]]_ Advances in Theoretical and Mathematical Physics, Volume 18, Number 2 (2014) p. 229?321   ([arXiv:1201.5277](http://arxiv.org/abs/1201.5277), [doi:10.4310/ATMP.2014.v18.n2.a1](https://dx.doi.org/10.4310/ATMP.2014.v18.n2.a1))

Discussion in [[twisted Cohomotopy]] ("[[schreiber:Hypothesis H]]"):

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization]]_ ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))

and in [[equivariant Cohomotopy]]:

* [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[schreiber:Equivariant Cohomotopy implies orientifold tadpole cancellation]]_ ([arXiv:1909.12277](https://arxiv.org/abs/1909.12277))
 


[[!redirects Dirac's charge quantization]]

[[!redirects charge quantization]]
[[!redirects charge quantizations]]


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

See at _[[D-brane charge quantization in K-theory]]_

### For the C-field in J-twisted Cohomotopy

See at _[supergravity C-field -- shifted flux quantization condition](supergravity+C-field#ShiftedCFieldFluxQuantizationCondition)_


## Related entries

* [[flux]], [[flux tube]], [[flux compactification]], [[uncertainty of fluxes]]

* [[higher flux quantization]]

* [[fiber bundles in physics]]

* [[non-perturbative quantum field theory]]

* [[monopole]]

  * [[Dirac monopole]], [[Yang monopole]]

* [[moduli space of monopoles]]

\linebreak



## References

See also the references at *[[fiber bundles in physics]]*.

### For the electromagnetic field

The original argument for charge quantization of the [[electromagnetic field]]:

* {#Dirac31} [[P.A.M. Dirac]], _Quantized Singularities in the Electromagnetic Field_,  Proceedings of the Royal Society A **133** (1931) 60-72 &lbrack;[doi:10.1098/rspa.1931.0130](http://rspa.royalsocietypublishing.org/content/133/821/60.short)&rbrack;

Further early discussion

* [[Julian Schwinger]], *Magnetic Charge and Quantum Field Theory*, Phys. Rev. **144** (1966) 1087 &lbrack;[doi:10.1103/PhysRev.144.1087](https://doi.org/10.1103/PhysRev.144.1087)&rbrack;

* [[Daniel Zwanziger]], *Quantum Field Theory of Particles with Both Electric and Magnetic Charges*, Phys. Rev. **176** (1968) 1489 &lbrack;[doi:10.1103/PhysRev.176.1489](https://doi.org/10.1103/PhysRev.176.1489)&rbrack;

Understanding of charge quantization in terms of [[Čech cohomology]]:

* {#Alvarez85a} [[Orlando Alvarez]], *Cohomology and Field Theory*, talk at: *Symposium on Anomalies, Geometry, Topology*, Argonne IL (28-30 March 1985) &lbrack;[inspire:965785](https://inspirehep.net/conferences/965785), [pdf](https://lib-extopc.kek.jp/preprints/PDF/1985/8507/8507262.pdf), [[Alvarez-CohomologyAndFieldTheory.pdf:file]]&rbrack;

* {#Alvarez85} [[Orlando Alvarez]], _Topological quantization and cohomology_, Comm. Math. Phys. **100** 2 (1985) 279-309 &lbrack[euclid:cmp/1103943448](https://projecteuclid.org/euclid.cmp/1103943448)&rbrack;

reviewed in:

* Guillermo A. González, *Cohomologa de Cĕch y Cuantización Topológica de Parámetros Físicos*, Revista de la Academia Colombiana de Ciencias Exactas, Físicas y Naturales **47** 182 (2023) 51-71 &lbrack;[doi:10.18257/raccefyn.1782](https://doi.org/10.18257/raccefyn.1782), [[Gonzales-TopologicalQuantization.pdf:file]]&rbrack;

General review and further discussion:

* {#Frankel} [[Theodore Frankel]], section 16.4e of _[[The Geometry of Physics - An Introduction]]_, Cambridge University Press (2011) &lbrack;[doi:10.1017/CBO9781139061377](https://doi.org/10.1017/CBO9781139061377)&rbrack;

* [[Luis Alvarez-Gaumé]], Frederic Zamora, Section II in:  *Duality in Quantum Field Theory (and String Theory)*, AIP Conference Proceedings **423** (1998) 46–83 &lbrack;[arXiv:hep-th/9709180](https://arxiv.org/abs/hep-th/9709180), [doi:10.1063/1.55087](https://doi.org/10.1063/1.55087)&rbrack;

* {#Freed00} [[Daniel Freed]], Section 2 of: *[[Dirac charge quantization and generalized differential cohomology]]*, Surveys in Differential Geometry **7**, Int. Press (2000) 129-194 &lbrack;[arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220), [doi:10.4310/SDG.2002.v7.n1.a6](https://dx.doi.org/10.4310/SDG.2002.v7.n1.a6), [spire:537392](https://inspirehep.net/literature/537392)&rbrack;

* {#MangiarottiSardanashvily00} L. Mangiarotti, [[Gennadi Sardanashvily]], _Connections in Classical and Quantum Field Theory_, World Scientific, 2000 ([doi:10.1142/2524](https://doi.org/10.1142/2524))

* [[Yakov Shnir]], Section 2.1 of: *Magnetic Monopoles*, Springer 2005 ([ISBN:978-3-540-29082-7](https://www.springer.com/gp/book/9783540252771))

* [[Daniel S. Freed]], [[Gregory W. Moore]], [[Graeme Segal]], p. 7 of: *The Uncertainty of Fluxes*, Commun. Math. Phys. 271:247-274, 2007 ([arXiv:hep-th/0605198](https://arxiv.org/abs/hep-th/0605198), [doi:10.1007/s00220-006-0181-3](https://doi.org/10.1007/s00220-006-0181-3))

* {#Heras18} Ricardo Heras, _Dirac quantisation condition: a comprehensive review_, Contemp. Phys. 59, 331 (2018) ([arXiv:1810.13403](https://arxiv.org/abs/1810.13403))

See also 

* Wikipedia, _[Dirac's quantization](https://en.wikipedia.org/wiki/Magnetic_monopole#Dirac%27s_quantization)_

Arguments for electric charge quantization from [[anomaly cancellation]] in the [[standard model of particle physics]]:

* K. S. Babu and Rabindra N. Mohapatra, *Quantization of electric charge from anomaly constraints and a Majorana neutrino*, Phys. Rev. D **41** (1990) 271 &lbrack;[doi:10.1103/PhysRevD.41.271](https://doi.org/10.1103/PhysRevD.41.271)&rbrack;


### For the weak nuclear force field

Discussion of the [[moduli space of monopoles]] for [[SU(2)]]-[[Yang-Mills theory]] ([[weak nuclear force]]):

* {#AtiyahHitchin88} [[Michael Atiyah]], [[Nigel Hitchin]], _The geometry and dynamics of magnetic monopoles_  M. B. Porter Lectures. Princeton University Press, Princeton, NJ, 1988 ([jstor:j.ctt7zv206](https://www.jstor.org/stable/j.ctt7zv206))

* {#Segal79} [[Graeme Segal]], _The topology of spaces of rational functions_, Acta Math. Volume 143 (1979), 39-72 ([euclid:1485890033](https://projecteuclid.org/euclid.acta/1485890033))


[[!include D-brane charge quantization in topological K-theory -- references]]



### For the C-field in F-theory

Discussion of [[shifted C-field flux quantization]] of the [[C-field]]  in [[F-theory]]:

* [[Andres Collinucci]], [[Raffaele Savelli]], *On Flux Quantization in F-Theory*,  J. High Energ. Phys. **2012** 15 (2012)   &lbrack;[arXiv:1011.6388](https://arxiv.org/abs/1011.6388), <a href="https://doi.org/10.1007/JHEP02(2012)015">doi:10.1007/JHEP02(2012)015</a>&rbrack;

* [[Andres Collinucci]], [[Raffaele Savelli]], *On Flux Quantization in F-Theory II: Unitary and Symplectic Gauge Groups*,  J. High Energ. Phys. **2012** 94 (2012) &lbrack;[arXiv:1203.4542](https://arxiv.org/abs/1203.4542), <a href="https://doi.org/10.1007/JHEP08(2012)094">doi:10.1007/JHEP08(2012)094</a>&rbrack;

* [[Raffaele Savelli]], *Flux Quantization in F-theory and Freed-Witten anomaly*, talk at StringMath (2012) &lbrack;[pdf](https://www.hcm.uni-bonn.de/fileadmin/stringmath2012/parallel_talks/savelli.pdf), [[Savelli-FTheoryFluxQuantization.pdf:file]]&rbrack;




### For the C-field in M-theory

Discussion of [[shifted C-field flux quantization]] of the [[C-field]] in [[D=11 supergravity]]/[[M-theory]]:


* {#DFM} E. Diaconescu, [[Dan Freed]], [[Greg Moore]],  _The $M$-theory 3-form and $E_8$-gauge theory_, chapter in [[Haynes Miller]], [[Douglas Ravenel]] (eds.) _Elliptic Cohomology Geometry, Applications, and Higher Chromatic Analogues_, Cambridge University Press 2007 ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069), [doi:10.1017/CBO9780511721489](https:
//doi.org/10.1017/CBO9780511721489))

* {#FreedMoore04} [[Dan Freed]], [[Greg Moore]], _Setting the [[quantum integrand]] of M-theory_, Communications in Mathematical Physics, Volume 263, Number 1, 89-132, ([arXiv:hep-th/0409135](http://arxiv.org/abs/hep-th/0409135), [doi:10.1007/s00220-005-1482-7](https://doi.org/10.1007/s00220-005-1482-7))

* [[Greg Moore]], _Anomalies, Gauss laws, and Page charges in M-theory_ ([arXiv:hep-th/0409158](http://arxiv.org/abs/hep-th/0409158))

* {#FSS12} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]],  _[[schreiber:The moduli 3-stack of the C-field]]_, Communications in Mathematical Physics, Volume 333, Issue 1 (2015), Page 117-151, ([arXiv:1202.2455](http://arxiv.org/abs/1202.2455), [DOI 10.1007/s00220-014-2228-1](http://link.springer.com/article/10.1007%2Fs00220-014-2228-1))

* {#FiSaSc} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane|M5-branes, String 2-connections, and 7d nonabelian Chern-Simons theory]]_ Advances in Theoretical and Mathematical Physics, Volume 18, Number 2 (2014) p. 229?321   ([arXiv:1201.5277](http://arxiv.org/abs/1201.5277), [doi:10.4310/ATMP.2014.v18.n2.a1](https://dx.doi.org/10.4310/ATMP.2014.v18.n2.a1))

Discussion in [[twisted Cohomotopy]] ("[[Hypothesis H]]"):

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization]]_ ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))

and in [[equivariant Cohomotopy]]:

* [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[schreiber:Equivariant Cohomotopy implies orientifold tadpole cancellation]]_ ([arXiv:1909.12277](https://arxiv.org/abs/1909.12277))
 


[[!redirects Dirac's charge quantization]]

[[!redirects charge quantization]]
[[!redirects charge quantizations]]

[[!redirects flux quantization]]
[[!redirects flux quantizations]]

[[!redirects flux quantization law]]
[[!redirects flux quantization laws]]

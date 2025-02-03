
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

Certain [[topological string theories]] (2d [[topological field theory|topological]] [[sigma-models]] &lbrack;[Witten 1988](#Witten88)&rbrack;), with [[target space]] a suitable [[symplectic manifold]] $X$, have as [[spaces of quantum states]] the [[ordinary cohomology]] ([[real cohomology|real]]/[[complex cohomology|complex]]/[[de Rham cohomology]]) $H^\bullet(X)$ of the target manifold, but such that the [[genus of a surface|genus]]$=0$ [[worldsheet]] [[3-point function]] (a [[Gromov-Ruan-Witten invariant]]) equips the [[underlying]] [[vector space]] of the [[cohomology groups]] with a new product $H^\bullet(X) \otimes H^\bullet(X) \to H^\bullet(X)$ that [[deformation|deforms]] ("[[quantization|quantizes]]") the ordinary [[cup product]]/[[wedge product]]-[[cohomology ring]] to a non-commutative ring &lbrack;[Witten (1990), §3](#Witten90)&rbrack;, whence called a *quantum cohomology ring* &lbrack;[Vafa (1992)](#Vafa92)&rbrack;.

Beware that later authors often abbreviate the term from *quantum cohomology ring* to just *quantum cohomology*, which is however a misnomer since it is not the underlying notion of ([[ordinary cohomology|ordinary]]) [[cohomology]] that is being deformed/quantized here (just the [[coefficients]] are typically enlarged), but the multiplicative *[[ring]]-[[structure]]* [[cohomology ring|on cohomology]] is deformed -- indeed the title of [Vafa (1992)](#Vafa92) speaks more properly of *quantum rings*.


## Examples

\begin{example}
\label{QuantumCohomologyOfComplexProjectiveSpace}
**(quantum cohomology ring of complex projective space)**
\linebreak
The (small) quantum cohomology ring of [[complex projective space]] $\mathbb{C}P^{N-1}$, $N \geq 2$, should be
$$
  QH^\bullet\big(
    \mathbb{C}P^{N-1}
    ;\,
    \mathbb{C}
  \big)
  \;\simeq\;
  \mathbb{C}\big[
    a_2,\, b_{2N}
  \big]/(a_2^N - b_{2N})
  \,.
$$
and as such a "[[deformation]]" of the ordinary [[cohomology ring]], which is (see [there](complex+projective+space#eq:CohomologyRing)):
$$
  H^\bullet\big(
    \mathbb{C}P^{N-1}
    ;\,
    \mathbb{C}
  \big)
  \;\simeq\;
  \mathbb{C}\big[
    a_2
  \big]/(a_2^N)
  \,.
$$
\end{example}
([Witten 1990, p. 275](#Witten90); [Cecotti & Vafa 1992, p. 3](#CecottiVafa92); [Cecotti & Vafa 1993 p. 89](#CecottiVafa93); [Bourdeau & Douglas 1994 3.4](#BourdeauDouglas94); see also [Dorfmeister, Guest & Rossman 2010, p .1](#DorfmeisterGuestRossman10))



## Related concepts

* Quantum cohomology arises as [[chiral rings]] in [[super Yang-Mills theory]].

* [[Pontryagin ring]]



## References

### Quantum cohomology rings

The notion of quantum cohomology originates as a model for certain [[topological string]] [[n-point functions]] in:

* {#Vafa92} [[Cumrun Vafa]], §4 in: *Topological mirrors and quantum rings*, in [[Shing-Tung Yau]] (ed.) *Essays on mirror manifolds*, International Press (1992), republished in *Mirror Symmetry I*, AMS/IP Studies in Advanced Mathematics **9** (1998) &lbrack;[arXiv:hep-th/9111017](https://arxiv.org/abs/hep-th/9111017), [doi:10.1090/amsip/009](https://doi.org/10.1090/amsip/009)&rbrack;

* {#Witten90} [[Edward Witten]],  §3 in: *Two-dimensional gravity and intersection theory on moduli space*,  Surveys in Differential Geometry **1** (1990) 243-310 &lbrack;[doi:10.4310/SDG.1990.v1.n1.a5](https://dx.doi.org/10.4310/SDG.1990.v1.n1.a5), [inspire:307956](https://inspirehep.net/literature/307956), [SemanticScholar](https://www.semanticscholar.org/paper/Two-dimensional-gravity-and-intersection-theory-on-Witten/e5935bb91e79d8247468b19c310a201b8e41e808)&rbrack;

motivated by

* {#Witten88} [[Edward Witten]], *Topological sigma models*,  Comm. Math. Phys. **118** 3 (1988) 411-449 &lbrack;[euclid:cmp/1104162092](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-118/issue-3/Topological-sigma-models/cmp/1104162092.full)&rbrack;

See also:

* [[Eric Zaslow]], *Topological Orbifold Models and Quantum Cohomology Rings*, Commun. Math. Phys. **156** (1993) 301-331 &lbrack;[arXiv:hep-th/9211119](https://arxiv.org/abs/hep-th/9211119), [doi:10.1007/BF02098485](https://doi.org/10.1007/BF02098485)&rbrack;

  > (targets [[orbifolds]] of [[Riemann sphere|$\mathbb{C}P^1$]])

The rigorous mathematical formulation in [[differential geometry|differential]] [[symplectic geometry]] via [[Gromov-Ruan-Witten invariants]] is due to:

* [[Yongbin Ruan]], [[Gang Tian]], _A mathematical theory of quantum cohomology_, Mathematical Research Letters **1** 2 (1994) 269-278 &lbrack;[doi:10.4310/MRL.1994.v1.n2.a15](https://doi.org/10.4310/MRL.1994.v1.n2.a15), [pdf](https://www.intlpress.com/site/pub/files/_fulltext/journals/mrl/1994/0001/0002/MRL-1994-0001-0002-a015.pdf)&rbrack;

* [[Yongbin Ruan]], [[Gang Tian]], _A mathematical theory of quantum cohomology_, J. Diff. Geometry __42__ 2 (1995) 259-367 &lbrack;[doi:10.4310/jdg/1214457234](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-42/issue-2/A-mathematical-theory-of-quantum-cohomology/10.4310/jdg/1214457234.full)&rbrack;

with early computations in

* [[Bernd Siebert]], [[Gang Tian]], *On Quantum Cohomology Rings of Fano Manifolds and a Formula of Vafa and Intriligator*,  Asian Journal of Mathematics **1** 4 (1997) 679 – 695 &lbrack;[arXiv:alg-geom/9403010](https://arxiv.org/abs/alg-geom/9403010), [doi:10.4310/AJM.1997.v1.n4.a2](https://dx.doi.org/10.4310/AJM.1997.v1.n4.a2)&rbrack;

and in terms of [[algebraic geometry]] and via [[Frobenius manifolds]] due to:

* [[Maxim Kontsevich]], [[Yuri Manin]], *Gromov-Witten classes, quantum cohomology, and enumerative geometry*, Commun. Math. Phys. __164__ (1994) 525-562 &lbrack;[doi:10.1007/BF02101490](https://doi.org/10.1007/BF02101490), [hep-th/9402147](https://arxiv.org/pdf/hep-th/9402147)&rbrack;

* [[Maxim Kontsevich]], [[Yuri Manin]], [[Ralph Kaufmann]], _Quantum cohomology of a product_,  Invent. Math. __124__ (1996) 313-339 &lbrack;[doi:10.1007/s002220050055](https://doi.org/10.1007/s002220050055) arXiv:[q-alg/9502009](https://arxiv.org/abs/q-alg/9502009)&rbrack;

* [[Yuri I. Manin]], *Frobenius Manifolds, Quantum Cohomology, and Moduli Spaces*, Colloquium Publications **47** (1999) &lbrack;[ISBN:978-0-8218-1917-3](https://bookstore.ams.org/coll-47), [mpim-eprint:1598](https://archive.mpim-bonn.mpg.de/id/eprint/1598)&rbrack;

See also:

* [[Boris Dubrovin]], *Geometry and Analytic Theory of Frobenius Manifolds*, Extra Volume ICM II (1998) 315–326 &lbrack;[arXiv:math/9807034](https://arxiv.org/abs/math/9807034)&rbrack;

* [[Ron Donagi]], [[Josh Guffin]], [[Sheldon Katz]], [[Eric Sharpe]], *A Mathematical Theory of Quantum Sheaf Cohomology*, Asian J. Math. **18** (2014) 387-418 &lbrack;[arXiv:1110.3751](https://arxiv.org/abs/1110.3751), [doi:10.4310/AJM.2014.v18.n3.a1](https://doi.org/10.4310/AJM.2014.v18.n3.a1)&rbrack;

More on the history:

* [[Maxim Kontsevich]], *On the History of quantum cohomology and homological mirror symmetry* (2021) &lbrack;video:[YT](https://youtu.be/Ml2x5NnEQ1I)&rbrack;


Introduction and review:

* [[Martin A. Guest]], *Introduction to Quantum Cohomology*, Vietnam Journal of Mathematics **33** SI (2005) 29–59 &lbrack;[pdf](http://www.math.ac.vn/publications/vjm/VJM_33/Pdf_files_DB_2005/Bai3_Guest.pdf)&rbrack;

* [[Joachim Kock]], [[Israel Vainsencher]], *An Invitation to Quantum Cohomology -- Kontsevich's Formula for Rational Plane Curves*, Birkh&auml;ser (2007) &lbrack;[doi:10.1007/978-0-8176-4495-6](https://doi.org/10.1007/978-0-8176-4495-6)&rbrack;

* [[Martin A. Guest]], *Quantum cohomology: is it still relevant?* &lbrack;[arXiv:2210.05413](https://arxiv.org/abs/2210.05413)&rbrack;


* Josh Guffin, _Quantum sheaf cohomology, a pr&#233;cis_, Matemática Contemporânea **41** (2012) 17-26 &lbrack;[arxiv:1101.1305](https://arxiv.org/abs/1101.1305)&rbrack;

* Tom Coates, *An Introduction to Quantum Cohomology* &lbrack;[pdf](https://homepages.abdn.ac.uk/kedra/pages/lms/tom.pdf), [[Coates-QuantumCohomology.pdf:file]]&rbrack;

* [[Alexander Givental]], *A tutorial on Quantum Cohomology* &lbrack;[pdf](https://math.berkeley.edu/~giventh/papers/lqc.pdf), [[Givental-QuantumCohomologyTutorial.pdf:file]]&rbrack;

See also:

* Wikipedia, *[Quantum cohomology](https://en.wikipedia.org/wiki/Quantum_cohomology)*

Relation to [[chiral algebras]]:

* [[Fyodor Malikov]], [[Vadim Schechtman]], *Deformations of chiral algebras and quantum cohomology of toric varieties* &lbrack;[arXiv:math/0001170](https://arxiv.org/abs/math/0001170)&rbrack;


Slides of a talk for an audience of mathematical [[string theory|string theorists]]:

* [[Eric Sharpe]]: 

  _Quantum sheaf cohomology_ &lbrack;[pdf](http://www.phys.vt.edu/~ersharpe/brandeis-mar10-2.pdf)&rbrack; Brandeis university (2010)

  _Quantum sheaf cohomology I_ &lbrack;[pdf](http://www.phys.vt.edu/~ersharpe/banff-mar10.pdf)&rbrack;

On the [[equivariant cohomology|ewuivariant]] case:

* Hiroshi Iritani: *Fourier analysis of equivariant quantum cohomology* &lbrack;[arXiv:2501.18849](https://arxiv.org/abs/2501.18849)&rbrack;




### Of flag varieties

On quantum cohomology rings of [[flag varieties]] --- "quantum [[Schubert calculus]]":

* [[Dale H. Peterson]] (notes by [[Arun Ram]]), *Quantum Cohomology of $G/H$*, MIT (1997) &lbrack;[web](http://math.soimeme.org/~arunram/Resources/QuantumCohomologyOfGPL1-5.html), [pdf](http://math.soimeme.org/~arunram/Resources/PetersonGmodBcourse1997.pdf), [[Peterson-QuantumCohomology.pdf:file]]&rbrack;


* {#LeungLi14} [[Naichung Conan Leung]], [[Changzheng Li]], *An update of quantum cohomology of homogeneous varieties* &lbrack;[arXiv:1407.5905](https://arxiv.org/abs/1407.5905)&rbrack;

> (e.g. for $\mathbb{C}P^1 = SL(2,\mathbb{C})/P$)

Specifically the case of [[complex projective space|$\mathbb{C}P^N$]] ([[CP^N sigma-model|$\mathbb{C}P^N$ sigma-model]]):

* {#Witten90} [[Edward Witten]], *On the structure of the topological phase of two-dimensional gravity*, Nuclear Physics B **340** 2–3 (1990) 281-332 &lbrack;<a href="https://doi.org/10.1016/0550-3213(90)90449-N">doi:10.1016/0550-3213(90)90449-N</a>&rbrack;

* {#CecottiVafa92} [[Sergio Cecotti]], [[Cumrun Vafa]], *Exact Results for Supersymmetric Sigma Models*, Phys. Rev. Lett. **68** (1992) 903-906 &lbrack;[arXiv:hep-th/9111016](https://arxiv.org/abs/hep-th/9111016), [doi:10.1103/PhysRevLett.68.903](https://doi.org/10.1103/PhysRevLett.68.903)&rbrack;

* {#CecottiVafa93} [[Sergio Cecotti]], [[Cumrun Vafa]], *On Classification of $N=2$ Supersymmetric Theories*, Comm. Math. Phys. **158** (1993) 569-644 &lbrack;[arXiv:hep-th/9211097](https://arxiv.org/abs/hep-th/9211097), [doi:10.1007/BF02096804](https://doi.org/10.1007/BF02096804)&rbrack;

* {#BourdeauDouglas94} [[M. F. Bourdeau]], [[Michael R. Douglas]], *Topological-Antitopological Fusion and the Large $N$ $\mathbb{C}P^N$ Model*, Nucl. Phys. B **420** (1994) 243-267 &lbrack;[doi:hep-th/9312095](https://arxiv.org/abs/hep-th/9312095), <a href="https://doi.org/10.1016/0550-3213(94)90380-8">doi:10.1016/0550-3213(94)90380-8</a>&rbrack;


And specifically the case of [[Riemann sphere|$\mathbb{C}P^1$]]:

* {#DorfmeisterGuestRossman10} Josef F. Dorfmeister, [[Martin A. Guest]], Wayne Rossman, *The $t t^\ast$ Structure of the Quantum Cohomology of $\mathbb{C}P^1$ from the Viewpoint of Differential Geometry*, Asian Journal of Mathematics **14** 3 (2010) 417-438 &lbrack;[doi:10.4310/AJM.2010.v14.n3.a7](https://dx.doi.org/10.4310/AJM.2010.v14.n3.a7)&rbrack;


### Quantum K-cohomology rings
 {#ReferencesQuantumKTheoryRings}

The idea of an analogous quantum deformation of [[topological K-theory]]-rings originates around:

* [[Alexander B. Givental]], *On the WDVV-equation in quantum K-theory*, Michigan Math. J. **48** 1 (2000) 295-304 &lbrack;[arXiv:math/0003158](https://arxiv.org/abs/math/0003158), [doi:10.1307/mmj/1030132720](https://projecteuclid.org/journals/michigan-mathematical-journal/volume-48/issue-1/On-the-WDVV-equation-in-quantum-K-theory/10.1307/mmj/1030132720.full)&rbrack;

* Y.-P. Lee, *Quantum K-Theory I: Foundations*, Duke Math. J. **121** 3 (2004) 389-424 &lbrack;[arXiv:math/0105014](https://arxiv.org/abs/math/0105014), [doi:10.1215/S0012-7094-04-12131-1](https://projecteuclid.org/journals/duke-mathematical-journal/volume-121/issue-3/Quantum-K--theory-I-Foundations/10.1215/S0012-7094-04-12131-1.short)&rbrack;

and for some form of [[equivariant K-theory]] in:

* [[Alexander B. Givental]], *Permutation-equivariant quantum K-theory* &lbrack;[webpage](https://math.berkeley.edu/~giventh/perm/perm.html)&rbrack;

  *I. Definitions. Elementary K-theory of $\overline{\mathcal{M}}_{0,n}/S_n$* &lbrack;[arXiv:1508.02690](https://arxiv.org/abs/1508.02690)&rbrack;

  *II. Fixed point localization* &lbrack;[arXiv:1508.04374](https://arxiv.org/abs/1508.04374)&rbrack;

  *III. Lefschetz' formula on $\overline{\mathcal{M}}_{0,n}/S_n$ and adelic characterization* &lbrack;[arXiv:1508.06697](https://arxiv.org/abs/1508.06697)&rbrack;

  *IV. $D_q$-modules* &lbrack;[arXiv:1508.06697](https://arxiv.org/abs/1508.06697)&rbrack;

  *V. Toric $q$-hypergeometric functions* &lbrack;[arXiv:1509.03903](https://arxiv.org/abs/1509.03903)&rbrack;

  *VI. Mirrors* &lbrack;[arXiv:1509.07852](https://arxiv.org/abs/1509.07852)&rbrack;

  *VII. General theory* &lbrack;[arXiv:1510.03076](https://arxiv.org/abs/1510.03076)&rbrack;

  *VIII. Explicit reconstruction* &lbrack;[arXiv:1510.06116](https://arxiv.org/abs/1510.06116)&rbrack;

  *IX. Quantum Hirzebruch-Riemann-Roch in all genera* &lbrack;[arXiv:1709.03180](https://arxiv.org/abs/1709.03180)&rbrack;

  *X. Quantum Hirzebruch-Riemann-Roch in genus 0*, SIGMA **16** 031 (2020) &lbrack;[arXiv:1710.02376](https://arxiv.org/abs/1710.02376), [doi:10.3842/SIGMA.2020.031](https://doi.org/10.3842/SIGMA.2020.031)&rbrack;

  *XI. Quantum Adams-Riemann-Roch* &lbrack;[arXiv:1711.04201](https://arxiv.org/abs/1711.04201)&rbrack;

See also:

* [[Anders S. Buch]], [[Leonardo C. Mihalcea]], *Quantum K-theory of Grassmannians*, Duke Math. J. **156** 3 (2011) 501-538 &lbrack;[arXiv:0810.0981](https://arxiv.org/abs/0810.0981), [doi:10.1215/00127094-2010-218](https://doi.org/10.1215/00127094-2010-218)&rbrack;

Relation to [[D=3 N=2 super Yang-Mills theory]]:

* [[Hans Jockers]], [[Peter Mayr]], *Quantum K-Theory of Calabi-Yau Manifolds*, J. High Energ. Phys. **2019** 11 (2019) &lbrack;[arXiv:1905.03548](https://arxiv.org/abs/1905.03548), <a href="https://doi.org/10.1007/JHEP11(2019)011">doi:10.1007/JHEP11(2019)011</a>&rbrack;

* [[Hans Jockers]], [[Peter Mayr]], *A 3d Gauge Theory/Quantum K-Theory Correspondence*, Advances in Theoretical and Mathematical Physics **24** 2 (2020) &lbrack;[arXiv:1808.02040](https://arxiv.org/abs/1808.02040), [doi:10.4310/ATMP.2020.v24.n2.a4](https://dx.doi.org/10.4310/ATMP.2020.v24.n2.a4)&rbrack;

* Cyril Closset, Osama Khlaif, *Grothendieck lines in 3d $\mathcal{N}=2$ SQCD and the quantum K-theory of the Grassmannian* &lbrack;[arXiv:2309.06980](https://arxiv.org/abs/2309.06980)&rbrack;

Relation to [[D=4 N=1 super Yang-Mills theory]]:

* M. Nouman Muteeb, Leopoldo A. Pando Zayas: *A Four-dimensional Gauge Theory Perspective on Quantum K-theory* &lbrack;[arXiv:2501.02394](https://arxiv.org/abs/2501.02394)&rbrack;



More references are listed in:

* W. Gu, [[Leonardo C. Mihalcea]], [[Eric Sharpe]], H. Zou, *Quantum K theory of symplectic Grassmannians* &lbrack;[arXiv:2008.04909](https://arxiv.org/abs/2008.04909)

See also:

* Wei Gu, Jirui Guo, Leonardo Mihalcea, Yaoxiong Wen, Xiaohan Yan, *A correspondence between the quantum K theory and quantum cohomology of Grassmannians* &lbrack;[arXiv:2406.13739](https://arxiv.org/abs/2406.13739)&rbrack;

* Peter Koroteev, Andrey Smirnov: *On the Quantum K-theory of Quiver Varieties at Roots of Unity* &lbrack;[arXiv:2412.19383](https://arxiv.org/abs/2412.19383)&rbrack;





[[!include quantum cohomology as Pontrjagin rings -- references]]



[[!redirects quantum cohomology rings]]


[[!redirects quantum cohomology]]
[[!redirects quantum sheaf cohomology]]

[[!redirects quantum Schubert calculus]]

[[!redirects quantum K-theory]]
[[!redirects quantum K-theory ring]]
[[!redirects quantum K-theory rings]]


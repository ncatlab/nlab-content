
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

What is called the "BRST complex" in the [[physics]] literature is the [[Lie infinity-algebroid|qDGCA]] which is the [[Chevalley-Eilenberg algebra]] of the $L_\infty$-[[Lie infinity-algebroid|algebroid]] which is the differential version in [[Lie theory]] of the $\infty$-groupoid 

 * whose space of objects is the space of configurations/histories of a given physical system;

 * whose morphisms describe the gauge transformations between these configurations/histories;

 * whose $k$-morphisms describe the $k$-fold gauge-of-gauge transformations.

The generators of the BRST complex are called

 * in degree 0: **fields**;

 * in degree 1: **[[ghost field]]**;

 * in degree 2: **[[ghost-of-ghost fields]]**;

 * etc.

The [[cochain cohomology]] of the BRST complex is called, of course, _BRST cohomology_.

## Details

For details see at 

* _[[A first idea of quantum field theory]]_ the chapter _[Gauge symmetries](A+first+idea+of+quantum+field+theory#Gauge+symmetries)_.

## Related concepts

The BRST complex described a homotopical [[quotient]] of a space by an infinitesimal [[action]]. Combined with a homotopical intersection, it is part of the [[BRST-BV complex]].

* [[gauge transformation]], [[higher gauge transformation]]

* [[ghost field]], [[ghost-of-ghost field]]

* [[antifield]], [[antighost field]]

* [[local BRST complex]]

* [[variational BRST-bicomplex]]

* [[equivariant de Rham cohomology]]



[[!include gauge field - table]]



## References

### General

The idea of "ghost" fields was introduced in 

* [[Richard Feynman]], _Quantum theory of gravitation_ In: Acta physica polonica. vol 24, 1963, S. 697 

and expanded on in

* [[Richard Feynman]] in [[John Wheeler]], Klauder (eds.), _Magic without Magic_, Wheeler-Festschrift (1972)

The BRST formalism originates around

* [[Carlo Becchi]], A. Rouet, [[Raymond Stora]]: *Renormalization of gauge theories*, Ann. Phys. **98** 287 (1976)

 * [[I. V. Tyutin]], (1975), _Gauge Invariance in Field Theory and Statistical Physics in Operator Formalism_, [arXiv:0812.0580](https://arxiv.org/abs/0812.0580).

see also the references at _[[BRST]]_.

A classical standard references for the Lagrangian formalism is

* {#Henneaux90} [[Marc Henneaux]], _Lectures on the Antifield-BRST formalism for gauge theories_, Nuclear Physics B (Proceedings Supplement) 18A (1990) 47-106 (<a href="https://doi.org/10.1016/0920-5632(90)90647-D">doi</a> [pdf](http://www.math.uni-hamburg.de/home/schweigert/ws07/henneaux2.pdf))

Similarly the bulk of the textbook

* [[Marc Henneaux]], [[Claudio Teitelboim]], _[[Quantization of Gauge Systems]]_

considers the Hamiltonian formulation. Chapters 17 and 18 are about the Lagrangian ("antifield") formulation, with section 18.4 devoted to the relation between the two.

Review includes:

* {#Jiang95} [[Shuhan Jiang]], *BRST cohomology*, Section 3 in: *Mathematical Structures of Cohomological Field Theories*, PhD thesis (1995) &lbrack;[urn:nbn:de:bsz:15-qucosa2-869402](https://nbn-resolving.org//urn:nbn:de:bsz:15-qucosa2-869402), [spire:2701230](https://inspirehep.net/literature/2701230), [pdf](https://inspirehep.net/files/183359de739dfbf2a8118cd6e5d44700)&rbrack;


The [[L-infinity algebroid|$L_\infty$-algebroid]]-structure of the [[local BRST complex]] on the [[jet bundle]] is made manifest in

* {#Barnich10} [[Glenn Barnich]], _A note on gauge systems from the point of view of Lie algebroids_, in: *XXIX Workshop on Geometric Methods in Physics*, AIP Conference Proceedings, **1307** 7 (2010) &lbrack;[arXiv:1010.0899](https://arxiv.org/abs/1010.0899), [doi:/10.1063/1.3527427]( https://doi.org/10.1063/1.3527427)&rbrack;

Lecture notes from this perspective:

* [[Urs Schreiber]]: around [Ex. 10.28](https://ncatlab.org/nlab/show/geometry+of+physics+--+perturbative+quantum+field+theory#LocalOffShellBRSTComplex) in *[[geometry of physics -- perturbative quantum field theory]]* (2018)


Discussion with more emphasis on the applications to quantum field theory of interest: 

* [[Edward Witten]], in lecture 3 of: _Dynamics of Quantum Field Theory_ in vol II, starting page 1119, of [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey,  [[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. 

The [[perturbative quantum field theory|perturbative quantization]] of [[gauge theories]] ([[Yang-Mills theory]]) in [[causal perturbation theory]]/[[perturbative AQFT]] is discussed (for trivial [[principal bundles]] and restricted to [[gauge invariant observables]]) via [[BRST-complex]]/[[BV-formalism]] in

* {#Hollands07} [[Stefan Hollands]], _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev. Math. Phys.20:1033-1172, 2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))

* {#FredenhagenRejzner11a} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in the functional approach to classical field theory_, Commun. Math. Phys. 314(1), 93&#8211;127 (2012) ([arXiv:1101.5112](https://arxiv.org/abs/1101.5112))

* {#FredenhagenRejzner11b} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. 317(3), 697&#8211;725 (2012) ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232))

* {#Rejzner13} [[Katarzyna Rejzner]], _Remarks on local symmetry invariance in perturbative algebraic quantum field theory_ ([arXiv:1301.7037](https://arxiv.org/abs/1301.7037))

* {#Rejzner13} [[Katarzyna Rejzner]], _Remarks on local symmetry invariance in perturbative algebraic quantum field theory_ ([arXiv:1301.7037](https://arxiv.org/abs/1301.7037))

* Mojtaba Taslimi Tehrani, _Quantum BRST charge in gauge theories in curved space-time_ ([arXiv:1703.04148](https://arxiv.org/abs/1703.04148))

and surveyed in

* {#Rejzner16} [[Kasia Rejzner]], section 7 of _Perturbative algebraic quantum field theory_ Springer 2016

With focus on the [[cochain cohomology]]:

* [[José Figueroa-O'Farrill]], [[Takashi Kimura]], *The cohomology of BRST complexes* (1988) &lbrack;[pdf](https://www.maths.ed.ac.uk/~jmf/Research/PVBLICATIONS/homol.pdf), [[FigueroaKimuar-BRSTCohomology.pdf:file]]&rbrack;

Discussion of the BRST complex of the [[bosonic string]]/for [[2d CFT]] includes

* [[Graeme Segal]], p.114 and following of _The definition of conformal field theory_ , preprint, 1988; also in [[Ulrike Tillmann]] (ed.) _Topology, geometry and quantum field theory_ , London Math. Soc. Lect. Note Ser., Vol. 308. Cambridge University Press, Cambridge (2004) 421-577. ([pdf](https://people.maths.ox.ac.uk/segalg/0521540496txt.pdf)) 


Discussion of the BRST complex for the [[superstring]] (hence with the corresponding [[Lie algebroid]] being actually a [[super Lie algebroid]]) is for instance in 

* [[José Figueroa-O'Farrill]], [[Takashi Kimura]], _The BRST cohomology of the NSR string: vanishing and ``no-ghost'' theorems_, Comm. Math. Phys. **124** 1 (1989) 105-132. &lbrack;[euclid:cmp/1104179078](http://projecteuclid.org/euclid.cmp/1104179078)&rbrack;

* [[Alexander Belopolsky]], _De Rham Cohomology of the Supermanifolds and Superstring BRST Cohomology_, Phys.Lett. B403 (1997) 47-50 ([arXiv:hep-th/9609220](http://arxiv.org/abs/hep-th/9609220))

The perspective on the BRST complex as a formal dual to a space in [[dg-geometry]] is relatively clearly stated in section 2 of

* [[Kevin Costello]], _Renormalisation and the Batalin-Vilkovisky formalism_ ([arXiv](http://arxiv.org/abs/0706.1533)).

For more along these lines see [[BV-BRST formalism]].

In relation to [[equivariant de Rham cohomology]]:

* {#Kalkman93} [[Jaap Kalkman]], _BRST model applied to symplectic geometry_, Ph.D. Thesis, Utrecht, 1993 ([arXiv:hep-th/9308132 (broken)](https://arxiv.org/abs/hep-th/9308132), [cds:9308132](http://cds.cern.ch/record/568522), [pdf](http://cds.cern.ch/record/568522/files/9308132.pdf))

* [[Jaap Kalkman]], _BRST Model for Equivariant Cohomology and  Representatives for the Equivariant Thom Class_, Comm. Math. Phys. Volume 153, Number 3 (1993), 447-463. ([euclid:1104252784](http://projecteuclid.org/euclid.cmp/1104252784))

Making explicit that general observables constitute the functions on the BRST complex regarded as a [[dg-manifold]]:

* [[Anton Kapustin]], Yi Li: *Open String BRST Cohomology for Generalized Complex Branes*, Adv. Theor. Math. Phys. **9** (2005) 559-574 &lbrack;[arXiv:hep-th/0501071](https://arxiv.org/abs/hep-th/0501071), [euclid](https://projecteuclid.org/journals/advances-in-theoretical-and-mathematical-physics/volume-9/issue-4)&rbrack;

* {#Jiang23} Shuhan Jiang, Def. 4.3 in: *Mathematical Structures of Cohomological Field Theories*, Journal of Geometry and Physics **185** (2023) 104744 &lbrack;[doi:10.1016/j.geomphys.2022.104744](https://doi.org/10.1016/j.geomphys.2022.104744), [arXiv:2202.12425](https://arxiv.org/abs/2202.12425)&rbrack;




### History

* [[Carlo Becchi]], _BRS "Symmetry", prehistory and history_ ([arXiv:1107.1070](https://arxiv.org/abs/1107.1070))


[[!redirects BRST complexes]]

[[!redirects BRST-complex]]
[[!redirects BRST-complexes]]

[[!redirects BRST differential]]
[[!redirects BRST differentials]]

[[!redirects BRST cohomology]]

[[!redirects BRST operator]]
[[!redirects BRST operators]]

[[!redirects BRST Lagrangian]]



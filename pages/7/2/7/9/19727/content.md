

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
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

The study of [[conformal field theory]] on [[manifolds with boundary]], hence conformal [[boundary field theory]], is known as _boundary conformal field theory_ (often abbreviated as BCFT).



For the special case of [[2d CFT]] understood as the [[quantum field theory]] on the [[worldsheet]] of [[strings]], boundary conformal field theory is the key ingredient of [[perturbative string theory]] with prescribed [[boundary conditions]] for the [[open strings]]. From the [[target spacetime]]-perspective these [[boundary conditions]] are interpreted as the [[D-branes]] that the [[open strings]] may "end on".

In this way 2d BCFT can serve to give an [[algebra|algebraic]] definition of [[D-branes]], independent of or complementary to their incarnation in the [[target space|target]]-[[spacetime]] [[geometry]]. In particular [[fractional D-branes]] may be described this way as boundary conditions for the [[2d CFTs]] describing [[open strings]] propagating in [[orbifolds]].

A key tool of BCFT is the _boundary state_ formalism, where one interprets [[boundary conditions]] for the [[open string]] as [[coherent states]] of the corresponding [[closed string]] [[2d CFT]]. The physical interpretation of this algebraic fact is that the [[D-brane]], being [[mass|massive]] (see also at _[[black brane]]_) emits and absorbs [[gravitons]], which, in [[string theory]], are excitations of the [[closed string]].

It has been argued that, therefore, for [[sigma-model]] [[2d CFT]]s the classification of [[equivalence classes]] of BCFT boundary states under [[renormalization group flow]] should reproduce the expected classification of [[D-branes]] by the ([[equivariant K-theory|equivariant]], [[twisted K-theory]]) [[topological K-theory]] of the [[target spacetime]] ([Moore 03, section 3](#Moore03)).

While this gives, in principle, a precise algebraic definition of [[D-brane charge]] from the [[worldsheet]]-perspective, in practice it is hard to follow the [[renormalization group flow]] of the boundary states.
The proposal has been checked in some special cases (e.g. [Braun & Schaefer-Nameki 05](#BraunSchaeferNameki05)). Other authors reported some discrepancies ([Quiroz-Stefanski 01](#QuirozStefanski01))

Specifically for [[fractional D-branes]] at $G$-[[orbifold]] [[singularities]] the relevant boundary states are [[sums]] of boundary states for each "$g$-twisted sector" of the [[closed string]] [[2d CFT]], consisting of those string configurations that are closed in the [[covering space]] up to the [[action]] of the element $g \in G$:

<center>
<img src="https://ncatlab.org/nlab/files/TwistedSector.jpg" width="300"/>
</center>

> graphics grabbed from [BCR 00](#BCR00)

Here the [[coefficient]] of the $g$-twisted sector in the total boundary state is proprotional to the value $\chi_V(g)$ of the [[character]] $\chi_V$ of some $G$-[[representation]] $V \in R_{\mathbb{C}}(G) = KU_G(\ast)$ (e.g. [Recknagel-Schomerus 13 (4.102)](#RecknagelSchomerus13)). This makes it plausible that the [[RG-flow]]-[[equivalence classes]] of the boundary states for [[fractional D-branes]] do coincide with the [[equivariant K-theory]] $KU_G(\ast) = R_{\mathbb{C}}(G)$ of the [[orbifold]] singularity (the [[representation ring]] of $G$). 

> But maybe this has not yet been actually proven? 


## Related concepts

* [[boundary field theory]]

* [[fractional brane]], [[permutation brane]]

[[!include field theory with boundaries and defects - table]]


## References

### General

The boundary state formalism in BCFT is due to 

* C. G. Callan, C. Lovelace, C. R. Nappi and S. A. Yost, _Adding holes and crosscaps to the superstring_, Nucl. Phys. B 293 (1987) 83 (<a href="https://doi.org/10.1016/0550-3213(87)90065-4">doi:10.1016/0550-3213(87)90065-4</a>)

* C. G.  Callan, C. Lovelace, C. R. Nappi and S. A. Yost, _Loop corrections to superstring equations of motion_, Nucl. Phys. B308 (1988) 221 ([pdf](https://www.researchgate.net/profile/Scott_Yost/publication/222468211_Loop_Corrections_to_Superstring_Equations_of_Motion/links/5a54d5eda6fdccd72f5b4583/Loop-Corrections-to-Superstring-Equations-of-Motion.pdf))

* N. Ishibashi, _Boundary and Crosscap States in Conformal Field Theories_,  Mod. Phys. Lett. A4(1989) 251 ([pdf](https://inis.iaea.org/collection/NCLCollectionStore/_Public/20/072/20072844.pdf#page=125))

* N. Ishibashi and T. Onogi, _Open string model building_,  Nucl. Phys. B318(1989) 239 (<a href="https://doi.org/10.1016/0550-3213(89)90054-0">doi:10.1016/0550-3213(89)90054-0</a>)

* [Dixon-Friedan-Martinec-Shenker 87](#DixonFriedanMartinecShenker87)

See also

* {#RecknagelSchomerus99} [[Andreas Recknagel]], [[Volker Schomerus]], _Boundary Deformation Theory and Moduli Spaces of D-Branes_, Nucl.Phys. B545 (1999) 233-282 ([arXiv:hep-th/9811237](https://arxiv.org/abs/hep-th/9811237))

A textbook account is in


* {#RecknagelSchomerus13} [[Andreas Recknagel]], [[Volker Schomerus]], _Boundary Conformal Field Theory and the Worldsheet Approach to D-branes_, Cambridge 2013 ([spire:1308990](http://inspirehep.net/record/1308990))



### Relation to K-theory

The suggestion that [[renormalization group flow]]-[[equivalence classes]] of boundary states in 2d BCFT should realize the expected classification of [[D-brane charge]] in ([[equivariant K-theory|equivariant]]) [[topological K-theory]] apparntly goes back to

* {#Moore03} [[Gregory Moore]], section 3 of _K-Theory from a physical perspective_ ([arXiv:hep-th/0304018](https://arxiv.org/abs/hep-th/0304018))

This has been checked in examples in

* {#BraunSchaeferNameki05} [[Volker Braun]], Sakura Schafer-Nameki, _D-Brane Charges in Gepner Models_, J.Math.Phys. 47 (2006) 092304 ([arXiv:hep-th/0511100](https://arxiv.org/abs/hep-th/0511100))

A mismatch was claimed in 

* [Quiroz-Stefanski 01](#QuirozStefanski01)

### For rational CFT, WZW models and Gepner models

For [[rational CFT]]

* Sergei E. Parkhomenko, _Free Field Construction of D-Branes in Rational Models of CFT and Gepner Models_ ([arXiv:0802.3445](https://arxiv.org/abs/0802.3445))

Specifically for [[WZW models]]:

* [[Giovanni Felder]], [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Christoph Schweigert]], _The geometry of WZW branes_ ([arXiv:hep-th/9909030](https://arxiv.org/abs/hep-th/9909030))


For [[Gepner models]]:

* [[Jürgen Fuchs]], [[Christoph Schweigert]], J. Walcher, _Projections in string theory and boundary states for Gepner models_, Nucl.Phys. B588 (2000) 110-148 ([arXiv:hep-th/0003298](https://arxiv.org/abs/hep-th/0003298))

* [Braun & Schaefer-Nameki 05](#BraunSchaeferNameki05)

### On orbifolds

Discussion specifically concerning [[fractional D-branes]] on [[orbifolds]] includes

* {#DixonFriedanMartinecShenker87} [[Lance Dixon]], [[Daniel Friedan]], [[Emil Martinec]], [[Stephen Shenker]], _The conformal field theory of orbifolds_, Nucl. Phys. B 282 (1987) 13. (<a href="https://doi.org/10.1016/0550-3213(87)90676-6">doi:10.1016/0550-3213(87)90676-6</a>)

* {#DiaconescuGomis99} Diaconescu, [[Jaume Gomis]], _Fractional Branes and Boundary States in Orbifold Theories_, JHEP 0010 (2000) 001 ([arXiv:hep-th/9906242](https://arxiv.org/abs/hep-th/9906242))

* {#BCR00} M. Billo', B. Craps, F. Roose, _Orbifold boundary states from Cardy's condition_, JHEP 0101:038, 2001 ([arXiv:hep-th/0011060](https://arxiv.org/abs/hep-th/0011060))

* {#QuirozStefanski01} N. Quiroz, B. Stefanski Jr, _Dirichlet Branes on Orientifolds_, Phys.Rev. D66 (2002) 026002 ([arXiv:hep-th/0110041](https://arxiv.org/abs/hep-th/0110041))

* {#MMR06} Jaydeep Majumder, Subir Mukhopadhyay, Koushik Ray, _Fractional Branes in Non-compact Type IIA Orientifolds_, JHEP0611:008, 2006 ([arXiv:hep-th/0602135](https://arxiv.org/abs/hep-th/0602135))


[[!redirects boundary conformal field theories]]


[[!redirects boundary CFT]]
[[!redirects boundary CFTs]]

[[!redirects BCFT]]
[[!redirects BCFTs]]

[[!redirects boundary state]]
[[!redirects boundary states]]

[[!redirects twisted sector]]
[[!redirects twisted sectors]]

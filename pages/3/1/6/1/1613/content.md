

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

What might be called the _FRS construction/theorem_ after [[Jürgen Fuchs|Fuchs]], [[Ingo Runkel|Runkel]] and [[Christoph Schweigert|Schweigert]], also [[Jürg Fröhlich|Fröhlich]] and [[Jens Fjelstad|Fjelstad]] ([FRS 02](#FuchsRunkelSchweigert02), [FRS 04a](#FuchsRunkelSchweigert04a), [FRS 04b](#FuchsRunkelSchweigert04b), [FRS 05](#FuchsRunkelSchweigert05), [FFRS 06](#FjeldstadFuchsRunkelSchweigert06), [FFRS 08](#FjeldstadFuchsRunkelSchweigert06)) is a rigorous construction and classification of all [[rational CFT|rational]] _full_ [[2-dimensional conformal field theories]], where "full" means that these theories are defined "at all [[genus of a surface|genera]]", namely on all 2-dimensional [[cobordisms]] (instead of just on [[tori]], which is a simple special case that much of the other literature traditionally concentrates on ("modular invariance")).

It is (was earlier) well known that the construction of [[2d CFTs]] may be decomposed into 

1. a "local geometric" aspect which describes the behaviour of the theory on infinitesimal conformal cobordisms and is controled by [[vertex operator algebras]] and related structures, which in particular may be used to construct the spaces of [[conformal blocks]] of the theory, which are the spaces of _potential_ [[correlator]] functions with the right dependence of the [[conformal structure]];

1. a "global topological" aspects which consists of picking in these spaces of [[conformal blocks]] over each surface one element (one correlation function depending on conformal structure) in such a way that these choices globally fit together under gluing of 2-dimensional [[cobordisms]], a condition known as the _[[sewing constraint]]_.

What the FRS theorem effectively observes/shows is that the [[sewing constraints]] may be solved by appealing to a [[holography|holographic principle]] in form of the [[AdS3-CFT2 and CS-WZW correspondence]]. Indeed the FRS formalism may be seen as providing a mathematically precise realization of this correspondence. (That is clear from the construction in the FFRS articles, but the relation to holography was made explicit in various web posts by Urs Schreiber and then later in ([Kapustin-Saulina 11](#KapustinSaulina11))).

Namely given the [[vertex operator algebra]] that controls the CFT locally, then in the case of [[rational CFT]] (hence for a [[rational vertex operator algebra]]) its [[representation category]]  is a [[modular tensor category]] (which may alternatively be obtained from suitable representations of [[Hopf algebras]] or of [[loop groups]], but for the full construction one needs in the end an equivalence to reps of a specified VOA) and by the [[Reshetikhin-Turaev construction]] or [[Turaev-Viro construction]] this defines a [[3d TQFT]], which is essentially known to be the [[quantization of 3d Chern-Simons theory]]. 

The way that the FFRS construction now works is that given a [[surface]] with field insertions, then the [[CFT]] [[correlator]] of that is computed by 

1. first [[triangulation|triangulating]] the surface suitably, labelling the triangulation with a [[Frobenius algebra]] object internal to the [[modular tensor category]];

1. passing to the [[orientation double cover]] of the surface, filling that with a 3d [[cobordism]] with "[[Wilson loop]]" ribbons running through it and piercing the surface at the prescribed field insertions, where the ribbons are labeled by the [[objects]] of the representation category correpsonding to the field insertions (this makes one label for boundary field insertions and two for bulk field insertions, corresponding to the two "chiral" pieces of [[closed string]] CFT)

1. applying the [[3d TQFT]] [[FQFT|functor]] to this labeled cobordism with ribbons inside to produce an element in its [[hom-object|hom-space]];

1. identifying that hom space with the space of [[conformal blocks]] and hence finally producing an actual CFT correlator.

[[FFRSStbl.gif:pic]]

Previous to the FRS construction (and still) much of the literature on classification of [[2d CFTs]] concentrated on [[modular invariance|modular invariant]] [[partition functions]], hence on CFTs evaluated on a surface which is a [[torus]]. One interesting aspect of the FRS classification of _full_ CFTs that are defined not just on the torus but on all surfaces is that it showed examples of modular invariant partition functions in the literature which had all of: one, none, or several extensions to full CFTs. 

Since full [[2d CFTs]] are what is relevant in [[string theory]], where these correspond to the [[vacua]] that the [[string perturbation series]] is perturbing about (while in [[statistical physics]] often just the torus is in fact sufficient) this means that the FRS classification is part of the mathematical identification of the [[landscape of string theory vacua]]. Now, [[rational CFTs]] are known to constitute but a tiny part of that landscape, indeed a [[discrete space|discrete subset]] since any [[deformation]] of a rational CFT is non-rational. Nevertheless, rational 2d CFTs (the [[WZW model]]!) play an important roles as the "internal" parts of string theory [[KK-compactifications]]. Also, even a tiny space is infinitely more than the empty space, which is presently the part of the rest of the "landscape" that is understood rigorously.

## Related entries

* [[CFT]]

* [[holographic principle]]

* [[local-global principle]]

* [[cobordism hypothesis]]

## References

The construction and the proof of the classification result is originally described in the series of articles

* {#FuchsRunkelSchweigert02} [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _TFT construction of RCFT correlators I: Partition functions_, Nucl. Phys. B **646**  (2002) 353-497 &lbrack;[arXiv:hep-th/0204148](http://arxiv.org/abs/hep-th/0204148), <a href="https://doi.org/10.1016/S0550-3213(02)00744-7">doi:10.1016/S0550-3213(02)00744-7</a>&rbrack;

* {#FuchsRunkelSchweigert04a} [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _TFT construction of RCFT correlators II: Unoriented world sheets_, Nucl.Phys. B678 (2004) 511-637 ([arXiv:hep-th/0306164](http://arxiv.org/abs/hep-th/0306164))

* {#FuchsRunkelSchweigert04b} [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _TFT construction of RCFT correlators III: Simple currents_, Nucl.Phys. B694 (2004) 277-353 ([arXiv:hep-th/0403157](http://arxiv.org/abs/hep-th/0403157))

* {#FuchsRunkelSchweigert05} [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _TFT construction of RCFT correlators IV: Structure constants and correlation functions_, Nucl.Phys.B715:539-638 (2005) ([arXiv:hep-th/0412290](http://arxiv.org/abs/hep-th/0412290))

* {#FjeldstadFuchsRunkelSchweigert06} [[Jens Fjelstad]], [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _TFT construction of RCFT correlators V: Proof of modular invariance and factorisation_, Theor.Appl.Categor.16:342-433 (2006) ([arXiv:hep-th/0503194](http://arxiv.org/abs/hep-th/0503194))

* {#FjeldstadFuchsRunkelSchweigert08} [[Jens Fjelstad]], [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _Uniqueness of open/closed rational CFT with given algebra of open states_, Adv.Theor.Math.Phys.12:1283-1375 (2008) ([hep-th/0612306](http://arxiv.org/abs/hep-th/0612306))

Review:

* [[Ingo Runkel]], [[Jens Fjelstad]], [[Jürgen Fuchs]], [[Christoph Schweigert]], *Topological and conformal field theory as Frobenius algebras*, in: *Categories in Algebra, Geometry and Mathematical Physics* Contemp. Math. **431** (2007) 225-248 $[$[doi:10.1090/conm/431](http://dx.doi.org/10.1090/conm/431), [arXiv:math/0512076](https://arxiv.org/abs/math/0512076)$]$

*  [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _Open strings and 3d topological field theory_ ([pdf](http://www.mth.kcl.ac.uk/staff/i_runkel/PDF/ost.pdf))

* [[Liang Kong]], _Conformal field theory and a new geometry_, in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings in Symposia in Pure Mathematics, AMS, (2011) ([arXiv:1107.3649](http://arxiv.org/abs/1107.3649))

* [[Jürgen Fuchs]], [[Christoph Schweigert]], [[Simon Wood]], [[Yang Yang]], p. 13 of: *Algebraic structures in two-dimensional conformal field theory*, Encyclopedia of Mathematical Physics &lbrack;[arXiv:2305.02773](https://arxiv.org/abs/2305.02773)&rbrack;


An explicit amplification of how the FRS formalism follows from 3-dimensional [[Chern-Simons theory]] regarded as an [[extended topological quantum field theory]] [[QFT with defects|with defects]] and the [[holographic principle]] is in 

* {#KapustinSaulina11} [[Anton Kapustin]], [[Natalia Saulina]], _Surface operators in 3d TFT and 2d Rational CFT_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings in Symposia in Pure Mathematics, AMS, (2011)


Some more online discussion is here:

For a list of references see

* Urs Schreiber, [FRS reviews](http://golem.ph.utexas.edu/string/archives/000747.html)

A survey of the central theorem that the FRS construction solves the [[sewing constraints]] is at

* Urs Schreiber, [The FRS theorem on CFT](http://golem.ph.utexas.edu/string/archives/000813.html)

and a discussion of the converse, that every rarional 2-d CT is obtained this way is at

* Urs Schreiber, [FFRS on uniqueness of conformal field theory](http://golem.ph.utexas.edu/category/2007/01/ffrs_on_uniqueness_of_conforma.html)

On potential generalization from [[rational 2d CFT]] to [[logarithmic CFT]]:

* [[Jürgen Fuchs]], [[Christoph Schweigert]], *Full Logarithmic Conformal Field theory - an Attempt at a Status Report*, Proc. of *[[Higher Structures in M-Theory 2018]]*, Fortschr. Phys.  **67** 8-9 (2019)  $[$[arXiv:1903.02838](https://arxiv.org/abs/1903.02838), [doi:10.1002/prop.201910018](https://doi.org/10.1002/prop.201910018)$]$


[[!redirects FRS theorem on rational 2d CFT]]

[[!redirects FFRS formalism]]

[[!redirects Fuchs-Runkel-Schweigert construction]]

[[!redirects FRS formalism]]

[[!redirects FRS theorem on 2d rational CFT]]

[[!redirects FFRS-formalism]]
[[!redirects FFRS-formalism]]

[[!redirects FRS-formalism]]

[[!redirects FRS-theorem]]
[[!redirects FRS theorem]]



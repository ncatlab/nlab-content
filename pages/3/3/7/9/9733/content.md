
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of [[tensor triangulated category]] may be thought of as a [[categorification]] of the concept of a [[ring]] in that the [[monoidal category]] structure refines the [[monoid]] structure of a ring, and the fact that it is a [[triangulated category]] and hence [[stable (infinity,1)-category|stable]] makes it the [[homotopy theory]] analog of a monoid in [[abelian groups]], hence of a ring.

Accordingly, one may consider the [[prime spectrum]] of a tensor triangulated category in direct analogy: the [[prime ideals]] are taken to be the [[thick subcategories]] which behave as prime ideals under the [[tensor product]], in the obvious way.  ([Thomason 97](#Thomason97), [Balmer 02](#Balmer02)).

In terms of modern [[stable (∞,1)-category]] theory this may be understood as being the shadow on [[homotopy categories]] of the  _[[prime spectrum of a symmetric monoidal stable (∞,1)-category]]_.

A typical application of the spectrum construction for tensor triangulated categories is to the [[derived categories]] of [[quasicoherent sheaves]] of [[algebraic varieties]]. If one restricts to [[perfect complexes]] then often the variety may be reconstructed from the spectrum of its category of coherent sheaves. More generally this reconstruction theory applies to [[geometric stacks]], see at _[[Tannaka duality for geometric stacks]]_.

In some good cases such reconstruction works even when forgetting the monoidal structure ([Bondal-Orlov 03](#BondalOrlov03)):
The reconstruction theorems of nice classes of schemes from the abelian categories of (quasi)coherent sheaves have versions from weaker data of the corresponding derived categories, viewed as [[triangulated category|triangulated]] or [[enhanced triangulated categories]] (see [[triangulated categories of sheaves]]). This is important for study of deformations, [[homological mirror symmetry]] and noncommutative generalizations.

## Related concepts

* [[spectrum of an abelian category]]

* [[prime spectrum of a symmetric monoidal stable (∞,1)-category]]

## References

An important theorem of reconstruction using the triangulated category (but not the monoidal structure) is the [[Bondal-Orlov reconstruction theorem]]:

* {#BondalOrlov03} [[Aleksei Bondal]], [[Dmitri Orlov]], _Reconstruction of a variety from the derived category and groups of autoequivalences_, Compositio Mathematica __125__ (03), 327-344 [doi](http://dx.doi.org/10.1023/A:1002470302976), [pdf](http://www.mi.ras.ru/~orlov/papers/Compositio2001.pdf)

Several spectra for triangulated categories were systematically studied by Rosenberg:

* [[A. L. Rosenberg]], _Geometry of Noncommutative 'Spaces' and Schemes_, [pdf](http://www.mpim-bonn.mpg.de/preblob/5148)

Along the lines of the general [[spectral cookbook]], these spectra are obtained considering certain preorders on objects of the triangulated category. The preorders can be easily modified to respect additional structure, say a monoidal product, if there. 


In this vein, Thomason, Balmer, Garkusha and others considered instead tensor triangulated categories and corresponding [[spectral theory]], as well as stronger reconstruction theorems of schemes from derived categories of coherent sheaves (or, in some cases, perfect complexes) taking into account the monoidal structures:

* {#Thomason97} [[R. W. Thomason]], _The classification of triangulated subcategories_, Compositio Math. __105__(1):1&#8211;27, 1997 [MR98b:18017](http://www.ams.org/mathscinet-getitem?mr=1436741) [doi](http://dx.doi.org/10.1023/A:1017932514274)

* {#Balmer02} [[Paul Balmer]], _Presheaves of triangulated categories and reconstruction of schemes_, Mathematische Annalen __324__:3 (2002), 557-580 [dvi](https://www.math.ucla.edu/~balmer/Pubfile/Reconstr.dvi), [pdf](https://www.math.ucla.edu/~balmer/Pubfile/Reconstr.pdf) [ps](https://www.math.ucla.edu/~balmer/Pubfile/Reconstr.ps); _The spectrum of prime ideals in tensor triangulated categories_, J. Reine Angew. Math. __588__:149&#8211;168, 2005 [](http://www.math.ucla.edu/~balmer/Pubfile/Spectrum.dvi) [pdf](http://www.math.ucla.edu/~balmer/Pubfile/Spectrum.pdf) [ps](http://www.math.ucla.edu/~balmer/Pubfile/Spectrum.ps); _Spectra, spectra, spectra - Tensor triangular spectra versus Zariski spectra of endomorphism rings_, Alg. and Geom. Topology __10__:3 (2010) 1521-1563 [dvi](http://www.math.ucla.edu/~balmer/Pubfile/SSS.dvi) [pdf](http://www.math.ucla.edu/~balmer/Pubfile/SSS.pdf) [ps](http://www.math.ucla.edu/~balmer/Pubfile/SSS.ps)
* [[Grigory Garkusha]], M. Prest, _Reconstructing projective schemes from Serre subcategories_, J. Algebra __319__(3) (2008), 1132-1153, [pdf](http://www.swansea.ac.uk/media/garkpr44.pdf); _Triangulated categories and the Ziegler spectrum_, Algebras Repr. Theory 8 (2005), 499-523 [pdf](http://www.swansea.ac.uk/media/gark-pr2.pdf)

* {#Balmer04} [[Paul Balmer]], _The spectrum of prime ideals in tensor triangulated categories_. J. Reine Angew. Math., 588:149&#8211;168, 2005 ([arXiv:math/0409360](http://arxiv.org/abs/math/0409360))

* {#Balmer10} [[Paul Balmer]], _Spectra, spectra, spectra&#8212;tensor triangular spectra versus Zariski spectra of endomorphism rings_, Algebr. Geom. Topol., 10(3):1521&#8211;1563, 2010 ([pdf](http://www.math.ucla.edu/~balmer/research/Pubfile/SSS.pdf))



* [[Greg Stevenson]], _Tensor actions and locally complete intersection_ PhD thesis 2011 ([pdf](http://www.math.uni-bielefeld.de/~gstevens/Stevenson_thesis.pdf))


This line has been enhanced by exploring the theory of [[locales]] (for the case of quasicompact quasiseparated (i.e. coherent) schemes and derived category of [[perfect complexes]]) in 

* [[Joachim Kock]], Wolfgang Pitsch, _Hochster duality in derived categories and point-free reconstruction of schemes_, [arxiv/1305.1503](http://arxiv.org/abs/1305.1503)
 
Further discussion in the context of [[2-algebraic geometry]] is in 

* {#Brandenburg14} [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](http://arxiv.org/abs/1410.1716))

For the [[equivariant stable homotopy theory|equivariant stable homotopy category]]:

* [[Paul Balmer]], [[Beren Sanders]], _The spectrum of the equivariant stable homotopy category of a finite group_ ([arXiv:1508.03969](http://arxiv.org/abs/1508.03969))

In relation to [[Drinfeld centers]]:

* Kent B. Vashaw, _Balmer spectra and Drinfeld centers_ ([arXiv:2010.11287](https://arxiv.org/abs/2010.11287))


[[!redirects spectra of tensor triangulated categories]]

[[!redirects spectrum of a triangulated category]]
[[!redirects spectra of triangulated categories]]


category: geometry, noncommutative geometry, triangulated categories
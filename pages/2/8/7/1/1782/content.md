
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


Algebraic K-theory is about natural constructions of [[cohomology theories]]/[[spectra]] from [[algebra|algebraic]] data such as [[commutative rings]], [[symmetric monoidal categories]] and various [[homotopy theory|homotopy theoretic]] refinements of these. 

The _algebraic K-theory_ of a [[commutative ring]] $R$ was originally defined to be the [[Grothendieck group]] of its [[category]] of [[projective modules]]. Under the [relation between modules and vector bundles](module#RelationToVectorBundlesInIntroduction) this is directly analogous to the basic definition of [[topological K-theory]] and hence the common term.

More generally, following the axiomatics of _[[generalized (Eilenberg-Steenrod) cohomology]]_ any _algebraic K-theory_ should be given by a sequence of [[functors]] $K_i$ from some suitable class of [[categories]] of "algebraic nature" to [[abelian groups]], satisfying some natural conditions. Moreover, following the [[Brown representability theorem]] thesse groups should arise as the [[homotopy groups]] of a [[spectrum]], the algebraic _[[K-theory spectrum]]_. Classical constructions producing this by combinatorial means are known as the _[[Quillen Q-construction]]_ defined on _[[Quillen exact categories]]_ and more generally the _[[Waldhausen S-construction]]_ defined on _[[Waldhausen categories]]_.

For more on the history of the subject see ([Arlettaz 04](#Arlettaz04)) and see at at _[[Algebraic K-theory, a historical perspective]]_.

There are two ways to think of the traditional algebraic K-theory of a commutative ring more conceptually: on the one hand this construction is the [[group completion]] of the [[direct sum]] [[symmetric monoidal category|symmetric monoidal]]-structure on the [[category of modules]], on the other hand it is the group completion of the addition operation expressed by [[short exact sequences]] in that category. This leads to the two modern ways of expresing and viewing algebraic K-theory:

1. **monoidal.** The [[core]] of a [[symmetric monoidal category]] or more generally of a [[symmetric monoidal (∞,1)-category]] has a [[universal construction|universal]] completion to an [[abelian ∞-group]]/[[connective spectrum]] optained by universally adjoining [[inverses]] to the symmetric monoidal operation. This yields the concept of [[K-theory of a permutative category|algebraic K-theory of a symmetric monoidal category]] and more generally that of [[algebraic K-theory of a symmetric monoidal (∞,1)-category]];

1. **exact/stable.** Analogously, inverting the addition operation expressed by the [[exact sequences]] in an [[abelian category]] or more generally in a [[stable (∞,1)-category]] yields the [[algebraic K-theory of a stable (∞,1)-category]]. Explicit ways to express this are known as the  _[[Waldhausen S-construction]]_ and the _[[Quillen Q-construction]]_. This turns out to be a universal construction in the context of [[non-commutative motives]].

Both of these constructions produce a [[spectrum]] (hence [[Brown representability theorem|representing]] a [[generalized (Eilenberg-Steenrod) cohomology theory]]) -- called the _[[K-theory spectrum]]_ -- and the algebraic K-theory groups are the [[homotopy groups]] of that spectrum.

Typically the first construction here contains more information but is harder to compute, and vice versa (see also MO-discussion [here](http://mathoverflow.net/a/98602/381) and [here](http://mathoverflow.net/a/102583/381)).


The classical case of the algebraic K-theory of a commutative ring $R$ is a special case of this general concept of algebraic K-theory by either forming the [[symmetric monoidal category]] $(Mod(R), \oplus)$ and applying the [[abelian ∞-group]]-completion to that, or else forming the [[stable (∞,1)-category of chain complexes]] of $R$-modules and applyong the [[Waldhausen S-construction]] to that. In both cases the result is a [[spectrum]] whose degree-0 [[homotopy group]] is the ordinary algebraic K-theory of $R$ as given by the [[Grothendieck group]] and whose higher homotopy groups are its _higher algebraic K-theory_ groups.





## More Details


### Classical constructions

See at 

* [[Quillen Q-construction]]

* [[Waldhausen S-construction]]


### Via stable $(\infty,1)$-categories

There is a universal characterization of the construction of the K-theory spectrum $K(A)$ of a stable $(\infty,1)$-category $A$:

there is an $(\infty,1)$-functor

$$
  U : (\infty,1)StabCat \to N
$$

to a stable $(\infty,1)$-category which is universal with the property that it respects colimits and exact sequences in a suitable way. Given any stable $(\infty,1)$-category $A$, its (connective or non-connective, depending on details) algebraic K-theory spectrum is the hom-object

$$
  K(A) \simeq Hom(U(Sp), U(A))
  \,,
$$

where $Sp$ denotes the stable $(\infty,1)$-category of compact [[spectra]]. 

See ([Blumberg-Gepner-Tabuada 10](#BlumbergGepnerTabuada10)).

### Via symmetric monoidal $(\infty,1)$-categories

See at 

* [[K-theory of a permutative category]]

* [[K-theory of a bipermutative category]]

* [[K-theory of a symmetric monoidal (∞,1)-category]]

## Properties

### Regulators (relation to ordinary cohomology)

See at _[[Beilinson regulator]]_.

### Relation to topological K-theory

* [[comparison map between algebraic and topological K-theory]]


### Red-shift conjecture

* [[red-shift conjecture]]

[[!include chromatic tower examples - table]]


## Related concepts

Types of categories for which a theory of algebraic K-theory exist include notably the notions

* [[Quillen exact category]], 

* [[abelian category]],

* [[Waldhausen category]], 

* [[triangulated category]].

Concrete examples of interest include for instance


* the category of finitely generated [[projective object]]s over a unital $k$-[[associative unital algebra|algebra]], 

* the category of [[coherent sheaf|coherent sheaves]] over a [[noetherian ring|noetherian]] [[scheme]],

* the category of locally free sheaves over a scheme, 


* [[Milnor's K2]]([[Steinberg group]],[[universal central extension]])

* [[higher algebraic K-theory]] [[Quillen exact category]], [[Quillen's Q-construction]], [[Waldhausen S-construction]], [[Volodin spaces]];

* [[topological cyclic homology]], [[algebraic K-theory of operator algebras]]

* [[Beilinson regulator]]

* [[differential algebraic K-theory]]

* [[non-connective algebraic K-theory]]

* [[real algebraic K-theory]]


* [[bivariant algebraic K-theory]]

* [[K-motive]]

* [[red-shift conjecture]]


[[!include noncommutative motives - table]]


## References 

### Introductions

A survey is in 

* {#Arlettaz04} Dominique Arlettaz, _Algebraic K-theory of rings from a topological viewpoint_ ([pdf](http://www.math.uiuc.edu/K-theory/0420/Arlettaz-survey.pdf))

An introductory textbook account is in 

* {#Weibel} [[Charles Weibel]], _The K-Book: An introduction to algebraic K-theory_ ([web](http://www.math.rutgers.edu/~weibel/Kbook.html))

### Classical

Original articles include

* [[R. W. Thomason]], Thomas Trobaugh, _Higher algebraic K-theory of schemes and of derived categories_, _The Grothendieck Festschrift_, 1990, 247-435.

* [[Daniel Quillen]], _Higher algebraic K-theory_, in Higher K-theories, pp. 85&#8211;147, Proc. Seattle 1972, Lec. Notes Math. 341, Springer 1973.
A reference for classical constructions is

For discussion of stable phenomena in algebraic K-theory, see section 4 of 

* {#Cohen} [[Ralph Cohen]], _Stability phenomena in the topology of moduli spaces_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0908/0908.1938v2.pdf))

Discussion of the [[comparison map between algebraic and topological K-theory]] includes

* [[Jonathan Rosenberg]], _Comparison between algebraic and topological K-theory for Banach algebras and $C^\ast$-algebras_   ([pdf](http://www2.math.umd.edu/~jmr/algtopK.pdf))


 
### Via stable $(\infty,1)$-categories

The [[stable (∞,1)-category]] theory picture is discussed in

* {#BlumbergGepnerTabuada10} [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _A universal characterization of higher algebraic K-theory_ ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282)).
 

(in terms of [[noncommutative motives]]) and in

* [[Clark Barwick]], _On the algebraic K-theory of higher categories, I. The universal property of Waldhausen K-theory_ ([arXiv:1204.3607](http://de.arxiv.org/abs/1204.3607))

 
### Via symmetric monoidal $(\infty,1)$-categories

The perspective of [[algebraic K-theory of a symmetric monoidal (∞,1)-category]] is developed in

* {#BunkeTamme12} [[Ulrich Bunke]], [[Georg Tamme]], section 2.1 of _Regulators and cycle maps in higher-dimensional differential algebraic K-theory_ ([arXiv:1209.6451](http://arxiv.org/abs/1209.6451))

* {#Nikolaus13} [[Thomas Nikolaus]] _Algebraic K-Theory of $\infty$-Operads_ ([arXiv:1303.2198](http://arxiv.org/abs/1303.2198))

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], def. 6.1 in  _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))



[[!redirects algebraic K-theory of a stable (∞,1)-category]]
[[!redirects algebraic K-theory of a stable (infinity,1)-category]]
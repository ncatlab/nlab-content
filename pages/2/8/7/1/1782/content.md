

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
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

From a modern perspective, the algebraic K-theory [[spectrum]] $\mathbf{K}(R)$ of a [[commutative ring]] is simply the [[K-theory of a symmetric monoidal (∞,1)-category|∞-group completion]] of [[algebraic vector bundles]] on $Spec(R)$; this will be discussed in more detail [below](#AsTheKTheoryOfAlgebraicVectorBundles). In particular there is a natural concept of algebraic K-theory of "[[brave new rings]]", i.e. of [[ring spectra]]/[[E-∞ rings]].

Historically, the _algebraic K-theory_ of a [[commutative ring]] $R$ (what today is the "0th" algebraic K-theory group) was originally defined to be the [[Grothendieck group]] of its [[symmetric monoidal category]] of [[projective modules]] (under [[tensor product]] of modules). Under the [relation between modules and vector bundles](module#RelationToVectorBundlesInIntroduction), this is directly analogous to the basic definition of [[topological K-theory]], whence the common term. (In fact when applied to the _[[stack]]_ of [[vector bundles]] then algebraic K-theory subsumes [[topological K-theory]] and also [[differential K-theory]], see [below](#OnMonoidalStacks)).

There are canonical maps $K_0(R)\to Pic(R)$ from the 0th algebraic K-theory of a ring to its [[Picard group]] and $K_1(R)\to GL_1(R)$ from the first algebraic K-theory group of $R$ to its [[group of units]] which are given in components by the [[determinant]] functor. This fact is sometimes used to motivate algebraic K-theory as a "generalization of [[linear algebra]]" (see e.g. [this MO discussion](http://mathoverflow.net/a/171369/381)). This is also how the traditional [[regulator of a number field]] relates to [[Beilinson regulators]] of algebraic K-theory.

More generally, following the axiomatics of _[[Whitehead-generalized cohomology]]_ any _algebraic K-theory_ should be given by a sequence of [[functors]] $K_i$ from some suitable class of [[categories]] of "algebraic nature" to [[abelian groups]], satisfying some natural conditions. Moreover, following the [[Brown representability theorem]] these groups should arise as the [[homotopy groups]] of a [[spectrum]], the algebraic _[[K-theory spectrum]]_. Classical constructions producing this by combinatorial means are known as the _[[Quillen Q-construction]]_ defined on _[[Quillen exact categories]]_ and more generally the _[[Waldhausen S-construction]]_ defined on _[[Waldhausen categories]]_.

For more on the history of the subject see ([Arlettaz 04](#Arlettaz04), [Grayson 13](#Grayson13)) and see at at _[[Algebraic K-theory, a historical perspective]]_.

There are two ways to think of the traditional algebraic K-theory of a commutative ring more conceptually: on the one hand this construction is the [[group completion]] of the [[direct sum]] [[symmetric monoidal category|symmetric monoidal]]-structure on the [[category of modules]], on the other hand it is the group completion of the addition operation expressed by [[short exact sequences]] in that category. This leads to the two modern ways of expressing and viewing algebraic K-theory:

1. **monoidal.** The [[core]] of a [[symmetric monoidal category]] or more generally of a [[symmetric monoidal (∞,1)-category]] has a [[universal construction|universal]] completion to an [[abelian ∞-group]]/[[connective spectrum]] optained by universally adjoining [[inverses]] to the symmetric monoidal operation -- the [[K-theory of a symmetric monoidal (∞,1)-category|∞-group completion]]. This yields the concept of [[K-theory of a permutative category|algebraic K-theory of a symmetric monoidal category]] and more generally that of [[algebraic K-theory of a symmetric monoidal (∞,1)-category]];

1. **exact/stable.** Analogously, inverting the addition operation expressed by the [[exact sequences]] in an [[abelian category]] or more generally in a [[stable (∞,1)-category]] yields the [[algebraic K-theory of a stable (∞,1)-category]]. Explicit ways to express this are known as the  _[[Quillen Q-construction]]_ and the _[[Waldhausen S-construction]]_. This turns out to be a universal construction in the context of [[non-commutative motives]].

Here the second construction may be understood as first [[split exact sequence|splitting]] the [[exact sequences]] and then applying the first construction to the resulting [[direct sum]] monoidal structure. Typically the first construction here contains more information but is harder to compute, and vice versa (see also MO-discussion [here](http://mathoverflow.net/a/98602/381) and [here](http://mathoverflow.net/a/102583/381)).


Both of these constructions produce a [[spectrum]] (hence [[Brown representability theorem|representing]] a [[Whitehead-generalized cohomology theory]]) -- called the _[[K-theory spectrum]]_ -- and the algebraic K-theory groups are the [[homotopy groups]] of that spectrum.



The classical case of the algebraic K-theory of a commutative ring $R$ is a special case of this general concept of algebraic K-theory by either forming the [[symmetric monoidal category]] $(Mod(R), \oplus)$ and applying the [[abelian ∞-group]]-completion to that, or else forming the [[stable (∞,1)-category of chain complexes]] of $R$-modules and applyong the [[Waldhausen S-construction]] to that. In both cases the result is a [[spectrum]] whose degree-0 [[homotopy group]] is the ordinary algebraic K-theory of $R$ as given by the [[Grothendieck group]] and whose higher homotopy groups are its _higher algebraic K-theory_ groups.





## Constructions

### Symmetric monoidal K-theory

For a [[symmetric monoidal category]] $C$, K-theory may be defined by taking

* the [[maximal subgroupoid]] $i C \subset C$,
* the [[classifying space]] $B(i C)$ (a [[topological monoid]]),
* the [[group completion]] $\Omega B B (i C)$.

See at

* [[K-theory of a symmetric monoidal (∞,1)-category]]

* [[K-theory of a permutative category]]

* [[K-theory of a bipermutative category]]

### Quillen Q-construction (for exact categories)

Given an [[Quillen exact category]] $E$, one defines $K(E)$ by applying

* the [[Quillen Q-construction]] $Q(E)$,
* the [[group completion]] $\Omega B Q(E)$.

See at 

* [[Quillen Q-construction]]

### Waldhausen $S_\bullet$-construction (for Waldhausen categories)

Given a [[Waldhausen category]] $(C, w C)$, one defines its $K$-theory by applying

* the [[Waldhausen S-construction]] $w S_\bullet C$ (a [[simplicial category]]),
* the [[nerve]] (a [[bisimplicial set]]),
* the [[colimit]] (a [[simplicial set]]),
* the [[geometric realization]] (a [[space]]).

There is also a [[Waldhausen S-construction]] for [[stable (infinity,1)-categories]] and, most generally, for [[Waldhausen (infinity,1)-categories]].

See at

* [[Waldhausen S-construction]]
* [[K-theory of a stable (infinity,1)-category]]

## Examples

### For rings

We recall several constructions of the [[algebraic K-theory]] of a [[ring]].
See ([Weibel, IV.4.8, IV.4.11.1](#Weibel)) for details.


#### Plus construction

Given an associative unital [[ring]] $R$, one may define the algebraic K-theory [[space]] $K(R) = BGL(R)^+$ by taking

* the [[general linear groups]] $GL_n(R)$ for $n \ge 0$,
* their [[classifying spaces]],
* the [[colimit]] $BGL(R) = colim_n BGL_n(R)$,
* the [[Quillen plus construction]].

#### Direct sum K-theory

Consider the category $P(X)$ of [[finitely generated]] [[projective]] (right) $R$-modules.
It has a [[symmetric monoidal structure]] given by [[direct sum]].
The algebraic K-theory $K(R)$ may be described as the [[K-theory of a symmetric monoidal (infinity,1)-category]] of $P(R)$.
That is, it is the [[group completion]]
  $K(R) = \Omega B B (i P(X))$
where $i P(X)$ denotes the [[maximal subgroupoid]].
See ([Weibel, IV.4.8, IV.4.11.1](#Weibel)).

#### Exact K-theory

Consider the category $P(X)$ of [[finitely generated]] [[projective module|projective]] (right) $R$-modules.
This is an [[exact category]] and the K-theory $K(R)$ may be described via the [[Quillen Q-construction]]:
  $$ K(R) = \Omega B (Q(P(R)). $$


### For schemes

For [[schemes]], there are two constructions which do not agree in full generality.
See [Thomason-Trobaugh 90](#ThomasonTrobaugh90).

#### Quillen K-theory

The Quillen K-theory of a [[scheme]] $X$ is defined as the algebraic K-theory of the [[exact category]] $Vect(X)$ of [[vector bundles]] on $X$ (using the [[Quillen Q-construction]]).

#### Thomason-Trobaugh K-theory

Let $Perf(X)$ be the category of [[perfect complexes]] on $X$.
This admits the structure of a [[Waldhausen category]], and the Thomason-Trobaugh K-theory of $X$ is defined via the [[Waldhausen S-construction]].

It may also be defined as the [[K-theory of a stable (infinity,1)-category]] of $Perf(X)$ viewed as a [[stable (infinity,1)-category]].

Thomason-Trobaugh K-theory coincides with Quillen K-theory for schemes that admit an ample family of [[line bundles]], but has the advantage of better global descent properties.

### For smooth manifolds

Discussion of algebraic K-theory as a [[smooth spectrum]] $SmoothMfd^{op} \longrightarrow Spectra$ via $X \mapsto K(C^\infty(X))$ is in ([Bunke-Nikolaus-Voelkl 13](#BunkeNikolausVoelkl13), [Bunke 14](#Bunke14)).

For more on this see at 

* [[algebraic K-theory of smooth manifolds]]

* [[differential cohomology hexagon]], section _[Algebraic K-theory of smooth manifolds and the e-invariant](differential+cohomology+diagram#SoothVectorBundlesWithConnectionAndEInvariant)_

## Properties

### Chern characters

#### Regulators and relation to ordinary cohomology

See at _[[Beilinson regulator]]_.


#### Cyclotomic trace and relation to topological Hochschild homology

Given a ring $R$, then there is a natural morphism of [[spectra]]

\begin{tikzcd}
& TC(R) \arrow[d]\\
K(R) \arrow[ru] \arrow[r] & THH(R)\\
\end{tikzcd}

from the algebraic K-theory spectrum to the [[topological Hochschild homology]] spectrum and factoring through the [[topological cyclic homology]] spectrum called the _[[cyclotomic trace]]_ which much like a [[Chern character]] map for algebraic K-theory.

### Comparison map and Relation to topological K-theory

* [[comparison map between algebraic and topological K-theory]]



### Descent
 {#Descent}

See also

* Moritz Kerz, Florian Strunk, [[Georg Tamme]], _Algebraic K-theory and descent for blow-ups_ ([arXiv:1611.08466](https://arxiv.org/abs/1611.08466))

#### Zariski and Nisnevich descent

The algebraic K-theory spectrum $\mathbf{K}$ satisfies [[descent]] to give a [[sheaf]] of [[connective spectra]] on the [[Zariski site]].  For regular noetherian schemes this statement is due to ([Brown Gersten 73](#BrownGersten73)). The generalization to finite dimensional noetherian schemes is due to ([Thomason-Trobaugh 90](#ThomasonTrobaugh90)).

Moreover, $\mathbf{K}$ satisfies descent with respect to the [[Nisnevich site|Nisnevich topology]] (which lies between Zariski and &#233;tale).  This is due to ([Nisnevich 89](#Nisnevich89)) and was generalized in turn to finite dimensional noetherian schemes in the same paper of Thomason.

Further generalization of the descent result to finite dimensional quasi-compact quasi-separated schemes is due to ([Rosenschon 06](#Rosenschon06)).

#### Etale descent

The question of descent of $\mathbf{K}$ over the [[étale site]] is closely related to the [[Lichtenbaum-Quillen conjecture]], see also ([Thomason 85](#Thomason85)).  This is now a theorem of Rost and Voevodsky and it implies that K-theory does satisfy etale descent in sufficient large degrees.  

> [MO comment](http://mathoverflow.net/a/180265/381)

#### Description of the K-theory sheaf via algebraic vector bundles
 {#AsTheKTheoryOfAlgebraicVectorBundles}

Let $Sch$ denote the gros [[Zariski site]] of regular, separated, noetherian schemes.
It is explained in ([Bunke-Tamme 12, section 3.3](#BunkeTamme12) that the presheaf of [[spectra]] on $Sch$ defined by algebraic K-theory admits the following description.

Regard the [[stack]] $\mathbf{Vect}^\oplus$ of [[algebraic vector bundles]]
on $Sch$ as taking values in [[symmetric monoidal (∞,1)-categories]], via the [[direct sum]] of vector bundles. Then apply the [[K-theory of a symmetric monoidal (∞,1)-category]]-construction $\mathcal{K}$ to this, yielding a [[sheaf of spectra]].
This identifies with the usual Thomason-Trobaugh K-theory sheaf,a fact that follows from

1. Zariski descent for Thomason-Trobaugh K-theory,

1. the Zariski-local equivalence between Thomason-Trobaugh K-theory, Quillen K-theory, and direct sum K-theory.

### Relation to non-commutative topology and non-commutative motives
 {#RelationToKKAndMotives}

[[!include noncommutative motives - table]]




### Red-shift conjecture

* [[red-shift conjecture]]

[[!include chromatic tower examples - table]]


## Examples

### On monoidal stacks
 {#OnMonoidalStacks}

Algebraic K-theory is traditionally applied to single [[symmetric monoidal (∞,1)-categories|symmetric monoidal]]/[[stable (∞,1)-category|stable]] [[(∞,1)-categories]], but to the extent that it is [[(∞,1)-functor|functorial]] it may just as well be applied to [[(∞,1)-sheaves]] with values in these.

Notably, applied to the monoidal [[stack]] of [[vector bundles]] (with [[connection on a bundle|connection]]) on the [[site]] of [[smooth manifolds]], the [[K-theory of a symmetric monoidal (∞,1)-category|K-theory of a monoidal category]]-functor produces a [[sheaf of spectra]] which is a form of [[differential K-theory]] and whose [[geometric realization]] is the [[topological K-theory]] spectrum. For more on this see at _[differential cohomology hexagon -- Differential K-theory](differential%20cohomology%20diagram#DifferentialKTheory)_.


## Related concepts

* [[Eilenberg swindle]]

* [[equivariant algebraic K-theory]]

* [[iterated algebraic K-theory]]

Types of categories for which a theory of algebraic K-theory exist include notably the notions

* [[Quillen exact category]], 

* [[abelian category]],

* [[Waldhausen category]], 

* [[triangulated category]].

Concrete examples of interest include for instance


* the category of finitely generated [[projective object]]s over a unital $k$-[[associative unital algebra|algebra]], 

* the category of [[coherent sheaf|coherent sheaves]] over a [[noetherian ring|noetherian]] [[scheme]],

* the category of locally free sheaves over a scheme, 

* [[Gersten resolution]]

* [[Milnor's K2]] ([[Steinberg group]], [[universal central extension]])

* [[higher algebraic K-theory]] [[Quillen exact category]], [[Quillen's Q-construction]], [[Waldhausen S-construction]], [[Volodin spaces]];

* [[topological cyclic homology]], [[algebraic K-theory of operator algebras]]

* [[Beilinson regulator]]

* [[differential algebraic K-theory]]

* [[non-connective algebraic K-theory]]

* [[real algebraic K-theory]]


* [[bivariant algebraic K-theory]]

* [[K-motive]]

* [[red-shift conjecture]]

* [[filtrations on algebraic K-theory]]

[[!include noncommutative motives - table]]


## References 

### Introductions

Surveys with accounts of the historical development include

* {#Arlettaz04} [[Dominique Arlettaz]], _Algebraic K-theory of rings from a topological viewpoint_ ([pdf](http://www.math.uiuc.edu/K-theory/0420/Arlettaz-survey.pdf))

* {#Grayson13} [[Daniel Grayson]], _Quillen's work in algebraic K-theory_, J. K-Theory 11 (2013), 527&#8211;547 [pdf](http://www.math.uiuc.edu/~dan/Papers/qs-published-final.pdf)

An introductory textbook account is in 

* {#Weibel} [[Charles Weibel]], _The K-Book: An introduction to algebraic K-theory_ ([web](http://www.math.rutgers.edu/~weibel/Kbook.html))


Further review includes

* {#Isely05} Olivier Isely, _Algebraic $K$-theory_, 2005-06 ([[IselyKTheory.pdf:file]])

* {#Gerhardt14} [[Teena Gerhardt]], _Computations in algebraic K-theory_, talk at [CUNY Workshop on differential cohomologies 2014](http://qcpages.qc.cuny.edu/~swilson/cunyworkshop14.html) ([video recording](http://videostreaming.gc.cuny.edu/videos/video/1800/in/channel/55/))

Review of the relation to [[Dennis trace]], [[topological cyclic homology]] and [[topological Hochschild homology]] is in

* {#DundasGoodwillieMcCarthy13} [[Bjørn Dundas]], [[Thomas Goodwillie]], [[Randy McCarthy]], *The local structure of algebraic K-theory*, Springer (2013) &lbrack;[doi:10.1007/978-1-4471-4393-2](https://doi.org/10.1007/978-1-4471-4393-2)&rbrack;


### Classical

Original articles include

* {#Quillen73} [[Daniel Quillen]], _Higher algebraic K-theory_, in Higher K-theories, pp. 85&#8211;147, Proc. Seattle 1972, Lec. Notes Math. 341, Springer 1973.
([pdf](http://math.mit.edu/~hrm/kansem/quillen-higher-algebraic-k-theory.pdf))

  also: [[Daniel Grayson]], _Higher algebraic K-theory II, [after Daniel Quillen]_ ([pdf](http://www.math.illinois.edu/~dan/Papers/HigherAlgKThyII.pdf))

* {#BrownGersten73} [[Kenneth Brown]], Stephen M. Gersten, _Algebraic K-theory as generalized sheaf cohomology_, Higher K-Theories, Lecture Notes in Mathematics Volume 341, 1973, pp 266-292.

* {#Waldhausen85} [[F. Waldhausen]], _Algebraic K-theory of spaces_, Alg. and Geo. Top., Springer Lect. Notes Math. 1126 (1985), 318-419, [pdf](http://www.maths.ed.ac.uk/~aar/surgery/rutgers/wald.pdf).

* {#Thomason85} [[R. W. Thomason]], _Algebraic K-theory and &#233;tale cohomology_, Ann. Sci. Ecole Norm. Sup. 18 (4), 1985, pp. 437&#8211;552.


* {#Nisnevich89} [[Yevsey Nisnevich]], _The completely decomposed topology on schemes and associated descent spectral sequences in algebraic K-theory_, Algebraic K-theory: connections with geometry and topology, 1989, pp 241-341.


* {#ThomasonTrobaugh90} [[R. W. Thomason]], Thomas Trobaugh, _Higher algebraic K-theory of schemes and of derived categories_, _The Grothendieck Festschrift_, 1990, 247-435.


* {#Rosenschon06} Andreas Rosenschon, P.A. Ostv&#230;r, _Descent for K-theories_, Journal of Pure and Applied Algebra 206, 2006, pp 141&#8211;152.


For [[complex varieties]]:

* {#PedriniWeibel01} Claudio Pedrini, [[Charles Weibel]],  _The higher K-theory of complex varieties_, K-theory 21 (2001), 367-385 ([web](http://www.math.uiuc.edu/K-theory/0403/))

* Michael Paluch, _Algebraic K-theory and topological spaces_ ([pdf](http://www.math.uiuc.edu/K-theory/0471/alg-top.pdf))



For discussion of stable phenomena in algebraic K-theory, see section 4 of 

* {#Cohen} [[Ralph Cohen]], _Stability phenomena in the topology of moduli spaces_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0908/0908.1938v2.pdf))

Discussion of the [[comparison map between algebraic and topological K-theory]] includes

* [[Jonathan Rosenberg]], _Comparison between algebraic and topological K-theory for Banach algebras and $C^\ast$-algebras_   ([pdf](http://www2.math.umd.edu/~jmr/algtopK.pdf))

For [[smooth manifolds]]:

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_, Journal of Homotopy and Related Structures October 2014 ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

* {#Bunke14} [[Ulrich Bunke]], _A regulator for smooth manifolds and an index theorem_ ([arXiv:1407.1379](http://arxiv.org/abs/1407.1379))



### Algebraic K-theory of quotient stacks
 {#ReferencesAlgebraicKTheoryForQuotientStacks}

Discussion of algebraic K-theory for [[algebraic stacks]] (generalizing algebraic [[equivariant K-theory]]) is in

* [[Robert Thomason]], _Algebraic K-theory of group scheme actions_, Algebraic Topology and Algebraic K-theory, Ann. Math. Stud., Princeton, 113, (1987), 539-563.

* [[Amalendu Krishna]], Charanya Ravi, _On the K-theory of schemes with group scheme actions_ ([arXiv:1509.05147](http://arxiv.org/abs/1509.05147))

See also at _[universal Chern-Simons 3-bundle -- For reductive groups](universal+Chern-Simons+line+3-bundle#ForReductiveAlgebraicGroups)_.

### Algebraic K-theory of ring spectra

The [[algebraic K-theory]] of [[ring spectra]]:

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], chapter VI of _[[Rings, modules and algebras in stable homotopy theory]]_, AMS Mathematical Surveys and Monographs Volume 47 (1997) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/EKMM.pdf))

* {#BlumbergGepnerTabuada10} [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], Section 9.5 of: _A universal characterization of higher algebraic K-theory_, Geom. Topol. 17 (2013) 733-838 ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282), [doi:10.2140/gt.2013.17.733](http://dx.doi.org/10.2140/gt.2013.17.733))

* [[Jacob Lurie]], _Algebraic K-Theory of Ring Spectra_, Lecture 19 of _[Algebraic K-Theory and Manifold Topology](https://www.math.ias.edu/~lurie/281.html)_, 2014 ([pdf](http://people.math.harvard.edu/~lurie/281notes/Lecture19-Rings.pdf))

The  algebraic K-theory of specifically of [[suspension spectra]] of [[loop spaces]] (Waldhausen's _[[A-theory]]_) is originally due to

* [[Friedhelm Waldhausen]], _Algebraic K-theory of spaces_, In: A. Ranicki N.,  Levitt, F. Quinn (eds.), Algebraic and Geometric Topology, Lecture Notes in Mathematics, vol 1126. Springer, Berlin, Heidelberg (1985) ([doi:10.1007/BFb0074449](https://doi.org/10.1007/BFb0074449))

See also:

([Thomason-Trobaugh 90](#ThomasonTrobaugh90))



 
### Via stable $(\infty,1)$-categories

The [[stable (∞,1)-category]] theory picture is discussed in

* {#BlumbergGepnerTabuada10} [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _A universal characterization of higher algebraic K-theory_, Geom. Topol. 17 (2013) 733-838 ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282), [doi:10.2140/gt.2013.17.733](http://dx.doi.org/10.2140/gt.2013.17.733))
 

(in terms of [[noncommutative motives]]) and in

* [[Clark Barwick]], _On the algebraic K-theory of higher categories, I. The universal property of Waldhausen K-theory_ ([arXiv:1204.3607](http://de.arxiv.org/abs/1204.3607))

 
### Via symmetric monoidal $(\infty,1)$-categories

The perspective of [[algebraic K-theory of a symmetric monoidal (∞,1)-category]] is developed in

* {#BunkeTamme12} [[Ulrich Bunke]], [[Georg Tamme]], section 2.1 of _Regulators and cycle maps in higher-dimensional differential algebraic K-theory_ ([arXiv:1209.6451](http://arxiv.org/abs/1209.6451))

* {#Nikolaus13} [[Thomas Nikolaus]] _Algebraic K-Theory of $\infty$-Operads_ ([arXiv:1303.2198](http://arxiv.org/abs/1303.2198))


* {#BunkeTamme13} [[Ulrich Bunke]], [[Georg Tamme]], _Multiplicative differential algebraic K-theory and applications_ ([arXiv:1311.1421](http://arxiv.org/abs/1311.1421))


* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], def. 6.1 in  _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

* {#GepnerGrothNikolaus13} [[David Gepner]], [[Moritz Groth]], [[Thomas Nikolaus]], _Universality of multiplicative infinite loop space machines_, [arXiv:1305.4550](http://arxiv.org/abs/1305.4550).

### K-theory stacks

The system of [[infinite loop spaces]] of the algebraic K-theory spectrum regarded as an [[∞-stack]] on the [[Nisnevich site]] and the [[principal ∞-bundles]] over it is considered in

* {#Saito14} [[Sho Saito]], _Higher Tate central extensions via K-theory and infinity-topos theory_ ([arXiv:1405.0923](http://arxiv.org/abs/1405.0923))

implementing a suggestion stated in 

* {#Drinfeld03} [[Vladimir Drinfeld]], _Infinite-dimensional vector bundles in algebraic geometry (an introduction)_ ([arXiv:math/0309155](http://arxiv.org/abs/math/0309155))

### Equivariant versions

Refinement to [[global equivariant stable homotopy theory]]:

* [[Stefan Schwede]], _Global algebraic K-theory_ ([arXiv:1912.08872](https://arxiv.org/abs/1912.08872))

### Examples

* {#Ananyevskiy} Alexey Ananyevskiy, _On the algebraic $K$-theory of some homogeneous varieties_ ([pdf](http://www.math.uni-bielefeld.de/lag/man/431.pdf))


[[!redirects algebraic K-theory of a stable (∞,1)-category]]
[[!redirects algebraic K-theory of a stable (infinity,1)-category]]
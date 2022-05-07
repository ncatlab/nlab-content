
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

__Noncommutative algebraic geometry__  is the study of  'spaces' represented or defined in terms of algebras, or categories. Commutative [[algebraic geometry]], restricts attention to spaces whose local description is via _commutative_ [[ring]]s and [[algebra]]s, while noncommutative algebraic geometry allows for more general local (or affine) models. The categories are viewed as categories of [[quasicoherent sheaf|quasicoherent modules]] on noncommutative locally affine space, and by affine one can think of many algebraic models, e.g. $A_\infty$-algebras; the algebra and its category of modules are in the two descriptions viewed as representing the same space (Morita equivalence should not change the space). Categories are needed as the global "algebra of functions" is usually an incomplete global description while it may be  good enough locally. The categories are typically [[abelian category|abelian]], [[triangulated category|triangulated]], [[dg-category|dg-categories]] or [[A-infinity-category|A-infinity-catgories]].

Noncommutative algebraic geometry extends the [[algebraic geometry|algebraic geometric]] methods ([[local ring]]s, intersection theory etc.) to study noncommutative algebras, and conversely, uses noncommutative algebras in the study of commutative [[algebraic variety|algebraic varieties]] ([[Brauer group]]s, noncommutative desingularizations, [[stack]]s etc.). But some features, phenomena and methods do not have commutative analogues. 

## Relation to other kinds of geometry

### Relation to ordinary algebraic geometry
 {#RelationToOrdinaryAlgebraicGeometry}

The direct "naive" generalization of Grothendieck-style [[algebraic geometry]] via [[sheaves]] on a [[site]] ([[Zariski site]], [[etale site]] etc.) of [[commutative rings]]-[[opposite category|op]] to non-commutative rings does not work, for reasons discussed in some detail in ([Reyes 12](#Reyes12)). This is the reason why non-commutative algebraic geometry is phrased in other terms, mostly in terms of [[monoidal categories]] "of ([[quasicoherent sheaf|quasicoherent]]) [[abelian sheaves]]" ("[[2-rings]]"). See at _[[2-algebraic geometry]]_ for more.

### Relation to noncommutative geometry a la Connes 

Noncommutative algebraic geometry may be considered a subfield of general [[noncommutative geometry]]. Among prominent other subfields, the most influential is the direction lead by [[Alain Connes]].
In Connes' noncommutative geometry the algebras in question are [[operator algebras]] viewed as algebras of continuous, smooth or measurable functions or more general continuous global sections. There it is customary and sufficient to describe a space globally by a single algebra: smooth and continuous context allow for partition of unity so there is no need for sheaves and gluing local descriptions, to define the very spaces.


## History 

The subject is older than mainstream [[noncommutative geometry]] and it is very much implicit in Pierre Gabriel's thesis "Des cat&#233;gories Ab&#233;liennes" (Bull. Soc. Math. France 1962). The [[Gabriel spectrum]] (consisting of isomorphism classes of injective indecomposables) amounts to a reconstruction of a [[noetherian scheme|noetherian]] [[quasiseparated scheme|quasiseparated]] [[quasicompact scheme|quasicompact]] [[scheme]] from its category of [[quasicoherent sheaf|quasicoherent]] $\mathcal{O}$-[[module]]s (now generalized to all schemes, as the [[Gabriel-Rosenberg theorem]]). He looked at [[localization]] functors, and corresponding subcategories ([[reflective subcategory|reflective]] and coreflective), and proved some theorems on localization of [[quasicoherent sheaf|quasicoherent sheaves]]. At the same time, [[Alexander Grothendieck|Grothendieck]] taught us that _to study a space it is enough to have a [[category of sheaves]] -- a [[Grothendieck topos]] -- on this would-be space_. 

Together with two Auslander-Goldman papers " _Maximal orders_ " and " _The Brauer group of a commutative ring_ " -- both in Trans. AMS 1960 -- Gabriel's paper is a precursor of a more articulated development starting with Mike Artin's " _On Azumaya algebras and finte dimensional representations of rings_ " (J. Alg. 1969). Artin's 1969 paper characterizes [[Azumaya algebra]]s via their identities and paved the way to generalize [[algebraic geometry]] to [[ring]]s satisfying polynomial identities, via their [[representation]]s and invariant theory. Subsequent major contributions were made by Claudio Procesi with his book " _Rings with polynomial identities_ " (Marcel Dekker 1973) and his paper " _The invariant theory of $n\times n$ matrices_" (Adv. Math. 1976) and by Mike Artin and Bill Schelter's " _A version of Zariski's main theorem for PI rings_ " (Amer. J. Math. 1979). The link with [[representation theory]], using seminal work by Paul Cohn and [[George Bergman]], was clarified by Claus Ringel " _The simple Artinian spectrum of a finite dimensional algebra_ " (in Dekker Lect. Notes 51, 1979) and culminated in Aidan Schofield's book " _Representations of rings over skew fields_ " (1985). These developments have been influential for recent work in '[[formal scheme|formal]]' noncommutative geometry, such as [[Maxim Kontsevich]]'s "_Formal (non)commutative symplectic geometry" (1993), [[Joachim Cuntz]] and [[Daniel Quillen]]'s "Algebra extensions and nonsingularity" (JAMS 1995) and Kontsevich-Rosenberg's "Noncommutative smooth spaces" (cf. bibl. and [[quasi-free algebra]]). 

In the 70ties, [[localization]] theory was popular among ring theorists, and, several people tried to generalize [[structure sheaf|structure sheaves]] to noncommutative algebras. Gabriel-like localizations via alternative formalism of "kernel functors" (Goldman 1969) led to the books by Jonathan Golan " _Localization of noncommutative rings_ " (Marcel Dekker 1975) and [[Fred Van Oystaeyen]] " _Prime spectra in noncommutative algebra_ " (Springer LNM 444, 1975), and making the link with the Artin-Procesi approach, the book 

* [[Fred Van Oystaeyen]], [[Alain Verschoren]], _Non-commutative algebraic geometry_, Springer LNM 887, 1981. 

Localizations were viewed as analogues of open sets. However, the [[lattice of torsion theories]] is not [[distributive lattice|distributive]], what presented major difficulties at the time. Around 1995, a major [[descent]] theorem was proved by van Oystaeyen and Willaert and independently in a work of A. Rosenberg in Stockholm (1988). It is sort of generalized [[sheaf]] condition for quasicoherent modules, with respect to [[cover]]s by Gabriel localizations. This fact is now seen almost obvious; namely it is the comonadic descent for a [[comonad]] induced by a conservative family of flat localizationshaving right adjoint, which in the Gabriel localization clearly satisfy the conditions for Beck's [[comonadicity theorem]].

Cohn's universal localizations were used by Paul Cohn in " _The affine scheme of a general ring_ " (in Springer LNM 753, 1979) and later by Claus Ringel and Aidan Schofield as mentioned before. In England, Goldie's localization theory led to the theory of 'cliques' and 'clans' of prime ideals (Jategaonkar, Hajarnavis and others) which may in retrospect be viewed as influential to present local description via [[quiver]]s and [[A-infinity-category|A-infinity structures]].

Around 1980, the Leningrad school of [[integrable system]]s (Sklyanin, Fadeev, Takhtajan) created examples of [[quantum groups]], and soon after that were joined by Drinfel'd, Novikov, Jimbo, and independently, Manin and Woronowicz; these in turn give good examples in __affine noncommutative geometry__ (spaces represented by a single nongraded ring), moreover the actions of group-like objects are considered starting the subject of [[equivariant noncommutative algebraic geometry]].

In the early 80ties maximal orders were revisited as noncommutative versions of normal [[variety|varieties]]. In particular their local structure was investigated. Extending prior work by Mark Ramras, Mike Artin succeeded in describing the etale local structure of maximal orders over surfaces. In trying to generalize this to higher dimensions, one was quickly led to impose strong homological properties on the orders (and later, more general algebras). This led to the investigation of homological homogeneous rings (work by Ken Brown and others), Artin-Schelter regular algebras and, finally, Auslander-regular rings.

In this vein, around 1989, the [[noncommutative projective geometry]]  was developed by Artin, Zhang and collaborators, where Serre's theorem on $Proj$ of a graded ring is taken as a definition in the noncommutative case: [[quasicoherent sheaf|quasicoherent sheaves]] over a $Proj$ of a graded ring is the category of graded modules modulo the modules of finite length. They assume strong regularity properties on graded rings, limiting to the geometry which is very close to commutative projective geometry. Using [[Ore localization]], [[F. van Oystaeyen]] has defined another version of noncommutative projective geometry, based on his notion of a [[schematic algebra]].

A huge project started, trying to classify Auslander-regular algebras, graded-connected and generated in degree one (that is, noncommutative analogons of projective n-space) for small dimensions n. In dimension 3, the initial work was done by Artin and Schelter, culminating in the influential papers (ATV1), (ATV2) by Mike Artin, John Tate and [[Michel Van den Bergh]] (see bibl.). In this classification a class of algebras re-appeared which were initially discovered by Odeskii and Feigin, the so called Sklyanin algebras. Ring-theoretic investigations of the Sklyanin algebras were done by Tate and Van den Bergh (Noetherianity for all dimensions n) and in dimension 4 a geometric study via 'point' and 'line' modules was carried out by Thierry Levasseur, Toby Stafford and Paul Smith. Further classifications in dimension 3 (dropping the degree one generator condition) and 4 were done by these people and their students. In the ungraded case, maximal orders with excellent homological properties were recently used in connection with quotient-singularities and their desingularizations as in the noncommutative crepant resolution by Michel Van den Bergh (Abel symposium 2002).


## Approaches 

### Spectrum of an abelian category

When one is serious about the point of view that every space is represented by some [[abelian category]] and that every [[abelian category]] represents a (noncommutative) space this way, one wants to find the _spectrum_ of an abelian category in the way that one forms the [[spectrum (geometry)]] of a [[ring]]. In particular since in the noncommutative case the classical spectra from ring theory (like primitive spectrum and Gabriel's spectrum are usually too small to represent noncommutative spaces) 

Motivated by this, [[A. L. Rosenberg]] has developed many spectral constructions extending from the left spectrum of a ring to various spectra of [[abelian category|abelian categories]], [[triangulated category|triangulated categories]] and [[exact category|right exact categories]] (in his sense) and created a categorical version of a notion of (quasicompact relative) [[noncommutative scheme]] $X$ over a base category $C$ (viewed as category of sheaves on $Spec k$). Many other variants of spectra of abelian categories can be constructed; there is a general pattern though, cf. [[spectral cookbook]]. 

### Sheaves of sets on a $Q$-category

A space in the sense of a Grothendieck school is a sheaf $F$ of sets on the category of affine schemes $Aff$ equipped with some subcanonical Grothendieck topology and which is locally affine, i.e. there is a cover of $F$ (in the sense of induced Grothendieck topology on the category of presheaves) by representables. The noncommutative analogue of $Aff$ is the opposite to the category of noncommutative unital rings $NAff = Ring^{op}$. The problem is that the natural candidates for covers in $NAff$ are not making classes which satisfy the axioms for [[Grothendieck topology]], namely, the crucial stability under pullback fails. However $A$ can be equipped with a structure of a [[Q-category]], and then one can consider the sheaves of sets on a Q-category and define in an analogous way when they are locally affine. Similar approach works for noncommutative stacks.   

### Derived noncommutative geometry
  {#DerivedNonCommutativeGeometry}

[[derived noncommutative geometry|Derived noncommutative geometry]] is a subject related to the commutative [[derived algebraic geometry]] of [[Carlos Simpson|C. Simpson]]'s school. Cyclic and [[Hochschild homology]] play a major role. 

Here one thinks of [[dg-categories]], [[A-infinity categories]], [[Spectra]]-[[enriched categories]] and ultimately of [[stable (∞,1)-categories]] as [[formal duals]] to non-commutative derived spaces:

Any [[locally presentable (∞,1)-category|locally presentable]] [[stable (∞,1)-category]] may be regarded as a stable [[(∞,1)-topos]] (the "stable Giraud theorem", see [there](stable+infinity-category#StabGiraud)).
Therefore, thinking of a non-commutative space as the [[formal dual]] to a  [[triangulated category]] or rather to a [[stable (∞,1)-category]] is directly analogous to the way  [[topos theory]] and in particular [[higher topos theory]] characterizes generalized spaces as formal duals of [[toposes]].

More in detail, every [[stable (∞,1)-category]] with a set of generators is [[equivalence of (infinity,1)-categories|equivalently]] the $\infty$-category of [[(∞,1)-modules]] over an [[A-∞ algebra]] (or rather $A_\infty$-algebroid, in general, due to [Schwede-Shipley 01](stable+infinity-category#SchwedeShipley)) and in this sense manifestly the formal dual to a non-commutative derived variety (see [there](stable+infinity-category#AsCategoriesOfModules) for more).

The notion of [[noncommutative motive]] as localizations of stable $\infty$-categories (see [there](noncommutative+motive#AsUniversalAditiveInvariant)), due to [Blumberg-Gepner-Tabuada 10](noncommutative+motive#BlumbergGepnerTabuada10), directly ties into this.

The most nontrivial result seem to be a noncommutative 
version of the [[degeneration of Hodge-to-de-Rham spectral sequence]], conjectured by Kontsevich and, in one version, [proved](http://front.math.ucdavis.edu/0611.5623) by [[D. Kaledin]]. 

#### Homological mirror symmetry 

[Homological mirror symmetry](http://en.wikipedia.org/wiki/Homological_mirror_symmetry) by [[Maxim Kontsevich]] is a source of many *examples* of spaces of [[derived algebraic geometry]], which are represented by [[triangulated category|triangulated categories]] or their [[dg-category|dg-]] or $A_\infty$-[[enhanced triangulated category|enhancements]]; this has been enhanced by the insight in the structure of [[derived category|derived categories]] of [[coherent sheaf|coherent sheaves]] and their deformations like Landau-Ginzburg models, by [Beilinson](http://en.wikipedia.org/wiki/Alexander_Beilinson)(1977/8), Kapranov (1985-), Orlov, Bondal, van den Bergh, Polishchuk, Bridgeland and others.  

### Other motivations

Another big source of examples is deformation quantization and related topics involving usage of $A_\infty$ and $L_\infty$-algebras. Understanding of the role of quivers in noncommutative geometry has also being stimulated by independent and original works of Lieven le Bruyn and [[Arfinn Laudal]]. Laudal was also  motivated by deformation theory.

## Related concepts

[[!include Isbell duality - table]]

$\,$

[[!include noncommutative motives - table]]

## References 

* the entries on the subject include: [[noncommutative scheme]], [[sheaf on a noncommutative space]], [[noncommutative projective geometry]], [[localization]], [[schematic algebra]], [[Q-category]], [[quasicoherent sheaf]], [[spectrum of an abelian category]], [[spectral cookbook]], [[quantum group]], [[noncommutative principal bundle]], [[quantum homogeneous space]], [[equivariant noncommutative geometry]]
* list of pages with the tag [noncommutative geometry](/nlab/list/noncommutative+geometry)
* related subjects include: [[noncommutative geometry]], [[Hopf algebra]], [[gebra]], [[bialgebroid]], [[quantization]], [[deformation theory]]

* M. Artin, J. J. Zhang, _Noncommutative projective schemes_, Adv. Math. __109__ (1994), no. 2, 228--287, [doi](http://dx.doi.org/10.1006/aima.1994.1087)

* A. Bondal, M. van den Bergh, _Generators and representability of functors in commutative and noncommutative geometry_, Moscow MJ 2003

* M. Kontsevich, A. Rosenberg, _Noncommutative smooth spaces_,  The Gelfand Mathematical Seminars, 1996--1999,  85--108, Birkh&#228;user 2000; [arXiv:math/9812158](http://arxiv.org/abs/math/9812158)

* [[M. Kontsevich]], A. Rosenberg, _Noncommutative spaces_, preprint MPI-2004-35 ([dvi](http://www.mpim-bonn.mpg.de/preblob/2303),[ps](http://www.mpim-bonn.mpg.de/preblob/2331)), _Noncommutative spaces and flat descent_, MPI-2004-36 [dvi](http://www.mpim-bonn.mpg.de/preblob/2304),[ps](http://www.mpim-bonn.mpg.de/preblob/2332), _Noncommutative stacks_, MPI-2004-37 [dvi](http://www.mpim-bonn.mpg.de/preblob/2305),[ps](http://www.mpim-bonn.mpg.de/preblob/2333)

* [[A. L. Rosenberg]], _Noncommutative schemes_, Compos. Math. __112__ (1998) 93--125, [MR99h:14002](http://www.ams.org/mathscinet-getitem?mr=1622759), [doi](http://dx.doi.org/10.1023/A:1000479824211)

* O. A. Laudal, _Noncommutative algebraic geometry_, Rev. Mat. Iberoamericana __19__, n. 2 (2003), 509--580; ([euclid](http://projecteuclid.org/euclid.rmi/1063050166)).

* (ATV2) M. Artin, J. Tate, [[M. Van den Bergh]], _Modules over regular algebras of dimension $3$_, Invent. Math. __106__ (1991), no. 2, 335&#8211;388, [MR93e:16055](http://www.ams.org/mathscinet-getitem?mr=1128218), [doi](http://dx.doi.org/10.1007/BF01243916) 


* (ATV1) Michael Artin, John Tate, [[Michel Van den Bergh]], _Some algebras associated to automorphisms of elliptic curves_, The [[Grothendieck Festschrift]], Vol. I, 33&#8211;85, Progr. Math. __86__, Birkh&#228;user 1990.

* the n-geometry cafe, _the NAG canon_ ([blog](http://www.noncommutative.org/index.php/the-nag-canon.html))

* [[F. van Oystaeyen]], _Algebraic geometry for associative algebras_, Marcel Dekker 2000. vi+287 pp.

* S. Mahanta, _On some approaches towards non-commutative algebraic geometry_, [math.QA/0501166](http://arxiv.org/abs/math/0501166)

* [[L. Katzarkov]], [[Maxim Kontsevich|M. Kontsevich]], T. Pantev, _Hodge theoretic aspects of mirror symmetry_, [arxiv/0806.0107](http://arxiv.org/abs/0806.0107)

* [[D. Kaledin]], _Tokyo lectures "Homological methods in non-commutative geometry"_, [pdf](http://imperium.lenin.ru/~kaledin/tokyo/final.pdf), [TeX](http://imperium.lenin.ru/~kaledin/tokyo/final.tex)

* [[Zoran Skoda]], _Some equivariant constructions in noncommutative algebraic geometry_, Georgian Mathematical Journal 16 (2009), No. 1, 183&#8211;202, [arXiv:0811.4770](http://arxiv.org/abs/0811.4770); preprint MPIM2009-3.

* MathOverflow, [Theories of Noncommutative Geometry](http://mathoverflow.net/questions/10512/theories-
of-noncommutative-geometry)

* {#Reyes12} Reyes, _Sheaves that fail to represent matrix rings_ ([arXiv:1211.4005](http://arxiv.org/abs/1211.4005))


Discussion of noncommutative [[formal geometry]] 
of infinitesimal neighborhood of commutative schemes within noncommutative
ambient schemes is in 

* {#Kapranov98} [[Mikhail Kapranov]], _Noncommutative geometry based on commutator expansions_ ([arXiv:9802041](http://arxiv.org/abs/math/9802041))

For more on this see at _[[Kapranov's noncommutative geometry]]_.
See also the references at _[[derived noncommutative geometry]]_


category: algebraic geometry, noncommutative geometry
[[!redirects non-commutative algebraic geometry]]
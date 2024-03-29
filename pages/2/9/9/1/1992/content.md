+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents
{:toc}


## Idea

Sometimes for [[categories]] having some fixed [[extra property]] and/or [[extra structure]], one can produce a recipe which gives (up to suitable equivalence) all the examples (and nothing else). 

There are several typical classes of such *reconstruction theorems* (which are all to some extent related).

## Tannakian reconstruction theorems 

These theorems reconstruct an algebraic symmetry object ([[group]], [[groupoid]], [[gerbe]], [[Hopf algebra]], Hopf algebroid) from the [[monoidal category]] of [[representation]]s of that object (typically rigid and [[symmetric monoidal category|symmetric]] or [[braided monoidal category|braided]]). The correspondence between the symmetry object and the corresponding [[category of representations]] is called **[[Tannaka duality]]**.

Examples include the classical Tannaka theorem and Krein theorem, [[Doplicher-Roberts reconstruction theorem]] in physics, [[Deligne's theorem on tensor categories]], Woronowicz's Tannaka duality for compact matrix pseudogroups, Saavedra-Rivano and Deligne reconstruction theorems for neutral and mixed Tannakian categories, Ulrich's reconstruction theorem, reconstruction theorems of Majid, Nori Tannakian theorem, Grothendieck's version of Galois group in algebraic geometry and so on. The notion of the [[fiber functor]] (due to Grothendieck) is central to these considerations. 

## Reconstruction theorems for schemes

These theorems for schemes (or varieties only) reconstruct a [[scheme]] (variety) out of the category of quasicoherent or only coherent sheaves (or a [[derived category]] version of them). In that class one can find the Gabriel--Rosenberg theorem, the [[Bondal-Orlov reconstruction theorem]], the reconstruction theorems of [P. Balmer](http://www.math.ucla.edu/~balmer) and of [G. Garkusha](http://www-maths.swan.ac.uk/staff/gg), and so on. There is also a class of reconstructions where for some derived categories a realization as derived categories of representation of quivers can be reconstructed.

There is a large class of __abelian reconstruction theorems__, for example the [[Gabriel-Popescu theorem]]. In _topos theory_ the __[[Giraud theorem]]__ is also a reconstruction theorem (of a [[site]] out of a [[topos]], though a nonuniqueness of the resulting site is involved, not affecting cohomology, hence, according to Grothendieck, nonessential).

Examples:

- [[Freyd-Mitchell embedding theorem]]
- [[Gabriel-Popescu embedding theorem]]
- [[Quillen-Gabriel embedding theorem]]

## Gabriel-Ulmer duality

[[Gabriel-Ulmer duality]] is an equivalence of 2-categories LFP of locally finitely presentable categories and Lex of finitely complete categories. It is related to syntax-semantics adjunction and to Tannaka type reconstruction for coalgebra-like objects, with which has a common generalization (enriched Tannaka duality of Day).  

Gabriel–Ulmer duality has a generalisation to [[sound doctrines]]. For [[sifted colimits]] rather than [[filtered colimits]], this gives [[Lawvere's reconstruction theorem]].

## Heuristics

Typically in the proofs of most reconstruction theorems an implicit use of the  Yoneda lemma is involved. Various embedding theorems of classes of categories (as well as theorems on realization as quotient categories) are closely related, e.g. [[Barr embedding theorem]] and [[Freyd-Mitchell embedding theorem]].

Many of these examples are corollaries of the theory of _lex colimits_.


## References

* [[André Joyal]], [[Ross Street]], [An introduction to Tannaka duality and quantum groups](http://www.maths.mq.edu.au/~street/CT90Como.pdf), in Part II of _Category Theory, Proceedings, Como 1990_, eds. A. Carboni, M. C. Pedicchio and G. Rosolini,  Lec. Notes in Mathematics __1488__, Springer, Berlin, 1991, pp. 411&#8211;492 [doi:10.1007/BFb0084207](http://dx.doi.org/10.1007/BFb0084207).

* P. Deligne, [[Catégories Tannakiennes]], [[Grothendieck Festschrift]], vol. II,  Birkh&#228;user Progress in Math. 87 (1990) pp.111--195.

* Alexander L. Rosenberg, _The existence of fiber functors_, in 'The Gelfand Mathematical Seminars 1996--1999', pp. 145--154. Birkh&#228;user, Boston, MA, 2000.

* A. L. Rosenberg, [[Reconstruction of groups]], Selecta Math. N.S. 9:1 (2003) [doi](http://dx.doi.org/10.1007/s00029-003-0322-x)

* N. Saavedra Rivano, _Cat&#233;gories Tannakiennes_, Springer LNM 265, 1972 

* Bodo Pareigis, [Quantum groups and noncommutative geometry](http://www.mathematik.uni-muenchen.de/~pareigis/pa_schft.html), WS 1999, chapter 3, online notes.

* S. Majid, _Foundations of quantum group theory_, chapter 9, Camb. Univ. Press 1995, 2002.

* S. Majid, _Tannaka--Krein theorem for quasiHopf algebras and other results_, Contemp. Math. 134 (1992) 219--232.

* A. L. Rosenberg, _Reconstruction of groups_, Selecta Math. N.S. __9__:1 (2003)[doi:10.1007/s00029-003-0322-x](http://dx.doi.org/10.1007/s00029-003-0322-x) (nlab remark: this paper is on a generalization of Tannaka--Krein and not of the Gabriel--Rosenberg kind of reconstruction)

* A. Rosenberg, _The spectrum of abelian categories and reconstructions of schemes_, in Rings, Hopf Algebras, and Brauer groups, Lectures Notes in Pure and Appl. Math. __197__, Marcel Dekker, New York, 257--274, 1998; MR99d:18011; and Max Planck Bonn preprint _Reconstruction of Schemes_, [MPIM1996-108](http://www.mpim-bonn.mpg.de/preprints/send?bid=3948) (1996). 

* [[A. L. Rosenberg]], _Spectra of noncommutative spaces_, MPIM2003-110 [ps](http://www.mpim-bonn.mpg.de/preblob/1946) [dvi](http://www.mpim-bonn.mpg.de/preblob/1945), _Underlying spaces of noncommutative schemes_, MPIM2003-111, [dvi](http://www.mpim-bonn.mpg.de/preblob/1947), [ps](http://www.mpim-bonn.mpg.de/preblob/1948)

* [[P. Gabriel]], [[Des catégories abéliennes]], Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __90__ (1962), 323--448, [numdam](http://www.numdam.org/item?id=BSMF_1962__90__323_0)

* A. I. Bondal, [[D. O. Orlov]], _Reconstruction of a variety from the derived category and groups of autoequivalences_, Compos. Math. 125 (2001), 327&#8211;344 [doi:10.1023/A:1002470302976](http://dx.doi.org/10.1023/A:1002470302976)

*  [[K. Szlachányi]], _Fiber functors, monoidal sites and Tannaka duality for bialgebroids_ [arxiv:0907.1578](http://arxiv.org/abs/0907.1578)

*  Ph&#249;ng H&#244; Hai, _Tannaka--Krein duality for Hopf algebroids_, [arxiv:math.QA/0206113](http://arxiv.org/abs/math/0206113)

* H&#233;l&#232;ne Esnault, Ph&#249;ng H&#244; Hai, _Gau&#223;--Manin connection and Tannaka duality_, [math.AG/0509111](http://arxiv.org/abs/math/0509111)

* H. Pfeiffer, _Tannaka--Krein reconstruction and a characterization of modular tensor categories_, [arxiv:math.QA/0711.1402](http://arxiv.org/abs/0711.1402)

* [[S. L. Woronowicz]], _Tannaka--Kre&#301;n duality for compact matrix pseudogroups. Twisted $SU(N)$ groups_, Invent. Math. __93__ (1988), no. 1, 35&#8211;76

* [[Michael Müger]], _Abstract duality for symmetric tensor $*$-categories_ (App. to Hans Halvorson: 'Algebraic Quantum Field Theory'.) In: J. Butterfield and J. Earman (eds.): "Handbook of the Philosophy of Physics", p. 865--922. North Holland, 2007; [arxiv:math-ph/0602036](http://arxiv.org/abs/math-ph/0602036); cf. The String Coffee Table, [M&#252;ger on Doplicher--Roberts](http://golem.ph.utexas.edu/string/archives/000711.html)  

* [[S. Doplicher]], J. E. Roberts, _A new duality theory for compact groups_, Inventiones Math., 98(1):157--218, 1989.

* [[P. Balmer]], _The spectrum of prime ideals in tensor triangulated categories_, J. Reine Angew. Math. __588__ (2005), pp. 149--168 [dvi](http://www.math.ucla.edu/~balmer/research/Pubfile/Spectrum.dvi) [pdf](http://www.math.ucla.edu/~balmer/research/Pubfile/Spectrum.pdf) [ps](http://www.math.ucla.edu/~balmer/research/Pubfile/Spectrum.ps).

* [M. Prest](http://www.maths.man.ac.uk/~mprest), [[G. Garkusha]], _Reconstructing projective schemes from Serre subcategories_, J. Algebra __319__ (3) (2008), 1132--1153 ([pdf](http://www-maths.swan.ac.uk/staff/gg/papers/garkpr44.pdf)).

* [[P. Deligne]], J. S. Milne, _Tannakian categories_, Lect. notes in math. 900, 101&#8211;228, Springer 1982.

* A. Brugui&#232;res, _On a tannakian theorem due to Nori_, [pdf](http://imag.umontpellier.fr/~bruguieres/docs/ntan.pdf); _Th&#233;orie tannakienne non commutative_, Comm. Algebra __22__, 5817&#8211;5860, 1994 

Lex colimits are discussed in:

* [[Richard Garner]] and [[Stephen Lack]]. _Lex colimits_. Journal of Pure and Applied Algebra 216.6 (2012): 1372-1396.


[[!redirects reconstruction theorems]]
[[!redirects reconstruction]]

[[!redirects Tannakian reconstruction]]
[[!redirects Tannakian reconstruction theorem]]
[[!redirects Tannakian reconstruction theorems]]

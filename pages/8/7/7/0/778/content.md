A _differential graded category_ is a category enriched
over complexes of modules for some commutative ring $k$.
Given a differential graded category $D$, one can form
a $k$-linear category $H^{0}(D)$ with the same objects as $D$
but with morphisms between two objects $X$ and $Y$ defined to be the $0$th cohomology group of the complex of morphisms
between $X$ and $Y$ in $D$.

The derived category of an abelian category $\mathcal{A}$
having enough injectives (or projectives) can be constructed
as $H^{0}$ of the differential graded category consisting
of complexes of injective (or projective) objects in $\mathcal{A}$ with morphisms between two complex $X$ and $Y$ being the Hom-complex from $X$ to $Y$. One can check that
$H^{0}$ of the Hom-complex between $X$ and $Y$ is precisely
homotopy classes of chain maps from $X$ to $Y$. 

# Definition #

A **dg-category** or **differential graded category** is a category [[enriched category|enriched]] over a [[symmetric monoidal category]] of [[category of chain complexes|chain complexes]], usually taken to be that of [[chain complex]]es of $k$-vector spaces for some field $k$: $dgCat := Ch(Mod_k)\Cat$.

Notice that a dg-category $\mathbf{B}A$ with a single object is a _differential graded algebra_ (see [[dg-algebra]]), $A$.

+--{.query}

[[Tim Porter|Tim]] : Would it be better to say cochain complexes as both Keller and Toen use the cochain convention?  This can be confusing. (In other words I am confused!) Things related to this seem central to several questions elsewhere. Perhaps a word here would be a good idea.

To get from a simplicially enriched category to a chain enriched one is easy (it is linearisation plus Dold-Kan, looked at by Tabuada in arXiv:0711.3845) but to get to a dg-category in the sense of Keller or Toen  (i.e. cochain enriched) is more interesting and complicated.
=--
Therefore, following the terminology for [[horizontal categorification]] a dg-category might more descriptively be addressed as a **differential graded algebroid**. (A similar comment applies for instance to [[C-star-category|C*-category]], which is a $C^*$-algebroid.)

A **left dg-module** over a dg-category $C$ is a dg-functor $L : C\to \mathrm{Com}_k$ where $\mathrm{Com}_k$ is the dg-category of complexes of $k$-vector spaces (that is Ch(Mod_k) with inner hom); similarly a right dg-module is a contravariant right dg-module. Morphisms between left dg-modules $L$ and $L'$ are elements of $Z^0\mathbf{Hom}(L,L')$ where the inner hom $\mathbf{Hom}$ is the complex of graded morphisms. Left dg-modules and their morphisms make a category $dgMod C$
which has a natural structure of [[Quillen exact category]],
which is in fact [[Frobenius category|Frobenius]].
There is a *Yoneda functor* $Z^0(C)\to dgMod C$ given by $X\mapsto C(-,X)$. 

+--{: .query}
[[Zoran Škoda]]: If one talks about left modules then we have category dgMod-C, and if talk about right modules then C-dgMod. When it is all the time clear which one we talk about than one can use either notation, but as long as we talk about left and right, then we should use A-Mod for left and Mod-A for right as it is usual in noncommutative algebra. 

_Toby_:  Good system, but there shouldn\'t be a minus sign in either version!  (You can get a hyphen, if you really need one, either by moving out of the dollar signs (the quick and dirty way) or (more properly) by using the Unicode hyphen: $dgMod$-$C$ or $dgMod&#8208;C$.)
=--

# Pre-triangulated dg-categories #

Intuitively, a dg-category is **pre-triangulated** if its homotopy category is a [[triangulated category]]. More precisely, it is pre-triangulated if the image of the Yoneda functor is closed under translations (in both directions) and extensions. 

Pre-triangulated dg-categories linear over field $k$ of characteristic 0 are equivalent to $k$-linear [[A-infinity-category|A-infinity-categories]] and both are models for [[stable (infinity,1)-category|stable (infinity,1)-categories]].

+--{: .query}
[[Hanno Becker]]: Hello! Maybe one could add that in a pretriangulated dg-category $C$, the Frobenius-structure on dg-mod(C) pulls back to a Frobenius-structure on $Z^0(C)$ via the Yoneda-functor, and that dividing out its injective-projective objects turns out to be equivalent to passing to the homotopy category. Thus, the stable category of $Z^0(C)$ equals the homotopy category, which is then triangulated. 

Do you assume the existence of a zero-object in a pretriangulated dg-category (there are interesting examples of dg-categories not possessing a zero object, e.g. the dg-categories of matrix-factorizations)?
=--

#References#

*  A. I. Bondal, M. M. Kapranov, _Enhanced triangulated categories_, &#1052;&#1072;&#1090;&#1077;&#1084;. &#1057;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1058;&#1086;&#1084; 181 (1990), No.5, 669--683 (Russian); transl. in USSR Math. USSR Sbornik, vol. 70 (1991), No. 1, pp. 93--107, (MR91g:18010) ([[bondalKaprEnhTRiangCat.pdf:file]])

* Bernhard Keller, _On differential graded categories_  International Congress of Mathematicians. Vol. II,  151--190, Eur. Math. Soc., Z&#252;rich, 2006. ([arXiv](http://arxiv.org/abs/math/0601185))

* Bertrand To&#235;n, _Lectures on dg-categories_ ([pdf](http://www.math.univ-toulouse.fr/~toen/swisk.pdf))

* B. Keller, _Deriving DG categories_,  Ann. Sci. &#201;cole Norm. Sup. (4)  27  (1994),  no. 1, 63--102 (<a href="http://www.numdam.org/item?id=ASENS_1994_4_27_1_63_0">numdam</a>)

* B. Keller, _A remark on tilting theory and DG algebras_,  Manuscripta Math.  79  (1993),  no. 3-4, 247--252.

* S. Mahanta, _Noncommutative geometry in the framework of differential graded categories_ (<a href="http://arxiv.org/abs/0805.1628">arXiv:0805.1628</a>)

* Dmitry Tamarkin, _What do dg-categories form?_,
Compos. Math. 143 (2007), no. 5, 1335--1358. 

* M. Batanin, _What do dg-categories form_ (after Tamarkin), talks at Paris 7 and Australian category seminar (<a href="http://www.maths.usyd.edu.au/u/AusCat/abstracts/060726mb.html">abstract</a>)

* Gon&#231;alo Tabuada, _Invariants additifs de DG-cat&#233;gories_, Int. Math. Res. Not.  2005,  no. 53, 3309--3339; Addendum in Int. Math. Res. Not.  2006, Art. ID 75853, 3 pp. ; Erratum in Int. Math. Res. Not. IMRN  2007,  no. 24, Art. ID rnm149, 17 pp.; Une structure de cat&#233;gorie de mod&#232;les de Quillen sur la cat&#233;gorie des dg-cat&#233;gories,  C. R. Math. Acad. Sci. Paris  340  (2005),  no. 1, 15--19.

* G. Tabuada, _Homotopy theory of DG categories_, Thesis, Paris, 2007, <a href="http://people.math.jussieu.fr/~keller/TabuadaThese.pdf">pdf</a> (some chapters in English and some in French)

* A. I. Bondal, M. Larsen, V. A. Lunts, _Grothendieck ring of pretriangulated categories_ (<a href="http://front.math.ucdavis.edu/0401.5009">arXiv</a>)

See also [[motives and dg-categories]].

+--{.query}

[[Tim Porter|Tim]] : Is there an nLab policy on the meaning of chain complexes and dg-algebras?  Are the differentials of degree +1 or -1?

[[Urs Schreiber|Urs]]: to me it seems that one should stick to

$$
  \array{
    & \mathbf{name of differential} & \mathbf{degree of differential}
    \\
    chain complex & boundary operator & -1
    \\
    cochain complex & coboundary operator & +1
  }
$$

if one runs into a differential that feels like it 
ought to be called
a "boundary operator" but which still raises degree 
instead of lowering it one should be prepared to 
admit that one should choose the other overall sign
convention for the grading.

[[Tim Porter|Tim]] : That would be my choice as well.  I believe the Toen convention is with cochain complexes however. All the dgas tend to have cochain complexes underlying them, so perhaps we should provide some new entries to set up a suitable set of notation and terminology. We will need it if we start talking about infinity algebras whether Lie or otherwise.

[[Urs Schreiber|Urs]]: okay, let's choose here the above convention by default and add remarks where usage in the literature differs from ours. (on the other hand everyone reading anything differential graded will have to develop a certain tolerance for the inevitable mess of sign and grading conventions that haunts the literature)

[[Tim Porter|Tim]] : There is a fail-safe convention and that is to say $dg^-$ if chain enriched and $dg^+$ if cochain enriched.  What gets very confusing is, for instance, in Tabuada's thesis 

arXiv:0710.4303,

he is probably using $dg^+$ but in the comparison paper of dg-cat wih $SSet$-cat (arXiv:0711.3845) explicitly states 

'Let $Ch$ denote the category of complexes
over $k$ and $Ch\geq 0$ the full subcategory of positive graded complexes. Throughout
this article we consider homological notation (the differential decreases the degree).'

To go from $SSet$-cat to $dg^+$-cat you need a bar /  cobar construction it seems.

=--


[[!redirects differential graded category]]
[[!redirects dg-categories]]
[[!redirects differential graded categories]]
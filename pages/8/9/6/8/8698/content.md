
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

### Several notions of formal geometry

Formal geometry is a highly overloaded term in mathematics, used in number of conceptually similar ways, usually meaning that we work in setup in which some crucial details of geometry or analysis are not present or satisfied, e.g.

* we work with functions on "manifolds" but the functions do not necessarily converge, the geometry is rather based on topological algebras of [[formal power series]]; this is the formal geometry of Grothendieck school and the main notion is that of a [[formal scheme]] (or more general ind-schemes). There are also noncommutative versions like [[Kapranov's noncommutative geometry]].

* Gelfand's formal geometry: study infinite dimensional manifolds of [[jet bundles]] and related objects coming from usual differential geometry, geometry of formal differential operators, study of related objects from homological algebra, including 
Gelfand's [[formal manifold]] (homological vector field)

* we talk about neighborhoods,or localizations, morphisms of spaces, but not about spectra and points (a part of noncommutative geometry is done in such style) -- this is sometimes called "pseudogeometry"

* in [[algebraic geometry]]: [[formal spectrum]] of an [[adic noetherian ring]]

### Gelfand's formal geometry


See MathOverflow: [formal-geometry](http://mathoverflow.net/questions/6057/formal-geometry), [how-do-i-describe-the-gl-n-torsor-attached-to-a-smooth-morphism-of-relative-dimen](http://mathoverflow.net/questions/27531/how-do-i-describe-the-gl-n-torsor-attached-to-a-smooth-morphism-of-relative-dimen), []()

* [[Israel Gelfand]], [[David Kazhdan]], _Certain questions of differential geometry and the computation of the cohomologies of the Lie algebras of vector fields_, Soviet Math. Doklady __12__, 1367-1370 (1971)

For characteristic $p\gt 0$ case see

* Fedosov quantization in positive characteristics [arXiv](http://front.math.ucdavis.edu/0501.5247)

In a similar formal context Gelfand and collaborators introduced $(\mathfrak{A},\mathcal{D})$-systems

* I. M. Gel&#697;fand, Yu. L. Daletski&#301;, _Lie superalgebras and Hamiltonian operators_, Rep. No. 16 Sem. Supermanifolds, Dept. Math. Univ. Stockholm, 1987, 26 p.
* I. M. Gel&#697;fand, Yu. L. Daletski&#301;, B. L. Tsygan, _On a variant of noncommutative differential geometry_, Dokl. Akad. Nauk SSSR 308 (1989), no. 6, 1293--1297; translation in Soviet Math. Dokl. __40__ (1990), no. 2, 422&#8211;426 [MR91j:58015](http://www.ams.org/mathscinet-getitem?mr=1039918)

The $(\mathfrak{A},\mathcal{D})$-systems were partly motivated by the [[calculus of variations]], formalizing further the setting of works of Gelfand and Dorfman.

* &#1048;. &#1052;. &#1043;&#1077;&#1083;&#1100;&#1092;&#1072;&#1085;&#1076;, &#1048;. &#1071;. &#1044;&#1086;&#1088;&#1092;&#1084;&#1072;&#1085;, _&#1043;&#1072;&#1084;&#1080;&#1083;&#1100;&#1090;&#1086;&#1085;&#1086;&#1074;&#1099; &#1086;&#1087;&#1077;&#1088;&#1072;&#1090;&#1086;&#1088;&#1099; &#1080; &#1073;&#1077;&#1089;&#1082;&#1086;&#1085;&#1077;&#1095;&#1085;&#1086;&#1084;&#1077;&#1088;&#1085;&#1099;&#1077; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1099; &#1051;&#1080;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;., 15:3 (1981), 23&#8211;40, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1729&what=fullt&option_lang=rus); _&#1043;&#1072;&#1084;&#1080;&#1083;&#1100;&#1090;&#1086;&#1085;&#1086;&#1074;&#1099; &#1086;&#1087;&#1077;&#1088;&#1072;&#1090;&#1086;&#1088;&#1099; &#1080; &#1082;&#1083;&#1072;&#1089;&#1089;&#1080;&#1095;&#1077;&#1089;&#1082;&#1086;&#1077; &#1091;&#1088;&#1072;&#1074;&#1085;&#1077;&#1085;&#1080;&#1077; &#1071;&#1085;&#1075;&#1072;&#8211;&#1041;&#1072;&#1082;&#1089;&#1090;&#1077;&#1088;&#1072;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;. __16__:4 (1982), 1&#8211;9 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1663&what=fullt&option_lang=rus); _&#1057;&#1082;&#1086;&#1073;&#1082;&#1072; &#1057;&#1093;&#1086;&#1091;&#1090;&#1077;&#1085;&#1072; &#1080; &#1075;&#1072;&#1084;&#1080;&#1083;&#1100;&#1090;&#1086;&#1085;&#1086;&#1074;&#1099; &#1086;&#1087;&#1077;&#1088;&#1072;&#1090;&#1086;&#1088;&#1099;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;., 14:3 (1980), 71&#8211;74 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1836&what=fullt&option_lang=rus)
* &#1070;. &#1051;. &#1044;&#1072;&#1083;&#1077;&#1094;&#1082;&#1080;&#1081;, _&#1043;&#1072;&#1084;&#1080;&#1083;&#1100;&#1090;&#1086;&#1085;&#1086;&#1074;&#1099; &#1086;&#1087;&#1077;&#1088;&#1072;&#1090;&#1086;&#1088;&#1099; &#1074; &#1075;&#1088;&#1072;&#1076;&#1091;&#1080;&#1088;&#1086;&#1074;&#1072;&#1085;&#1085;&#1086;&#1084; &#1092;&#1086;&#1088;&#1084;&#1072;&#1083;&#1100;&#1085;&#1086;&#1084; &#1074;&#1072;&#1088;&#1080;&#1072;&#1094;&#1080;&#1086;&#1085;&#1085;&#1086;&#1084; &#1080;&#1089;&#1095;&#1080;&#1089;&#1083;&#1077;&#1085;&#1080;&#1080;_, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1277&what=fullt&option_lang=rus), transl. Yu. L. Daletskii, _Hamiltonian operators in graded formal calculus of variations_, Funct. Anal. Appl. __20__:2, 1986, 136-138

See also

* Bernstein, Rozenfeld, Homogeneous spaces of infinite-dimensional lie algebras and characteristic classes of foliations, Uspehi Mat. Nauk, [English pdf](http://www.math.tau.ac.il/~bernstei/Publication_list/publication_texts/B-Rosen-Foliations-Usp.pdf)

	
### Formal noncommutative symplectic geometry of Kontsevich

* [[Maxim Kontsevich]], _Formal (non)-commutative symplectic geometry_, The Gelfand Mathematical. Seminars, 1990-1992, Ed. L.Corwin, I.Gelfand, J.Lepowsky, Birkhauser 1993, 173-187, [pdf](http://www.ihes.fr/~maxim/TEXTS/Formal%20non-commutative%20symplectic%20geometry.pdf)

## Related concepts

* [[formal dg-algebra]]

* [[formal neighbourhood]], [[formal disk]]

* [[Hasse local-global principle]]

* [[formal Picard group]], [[formal Brauer group]]

* [[Kapranov's noncommutative geometry]]

[[!include infinitesimal and local - table]]


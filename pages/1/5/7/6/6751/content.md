
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Geometric quantization
+-- {: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Orbit method_ (or _Kirillov's method_, or _method of coadjoint orbits_) is concerned with identifying [[unitary representations]] of [[Lie groups]] with the canonical $G$-[[actions]] on spaces of [[sections]] of certain [[line bundles]] over [[coadjoint orbits]] of the Lie group.

More in detail, the dual $\mathfrak{g}^*$ of a (say finite-dimensional real) [[Lie algebra]] has a canonical structure of a [[Poisson manifold]] (with the Poisson structure due to [[Alexandre Kirillov]] and [[Jean-Marie Souriau]]), namely for any $a\in \mathfrak{g}^*$, 

$$
\{ f, g\}(a) := \langle [d f_a, d g_a],a\rangle
 \,.
$$

This Poisson manifold [[foliation|foliates]] into [[symplectic leaves]] which are the [[coadjoint orbits]]. The [[line bundles]] in question are the _[[prequantum line bundles]]_ of these [[symplectic manifolds]].

Hence, in the language of [[quantum physics]], the orbit methods identifies unitary representations of Lie groups $G$ with the $G$-action on [[spaces of states]] of the [[geometric quantization]] of a [[classical mechanical system]] with a global $G$-[[symmetry]].

Many important classes of unitary representations are obtained by that method. 

Notably in the case of [[compact Lie groups]], co-adjoint orbits are [[flag manifolds]] and the _[[Borel-Weil theorem]]_ says that under certain further conditions the expected unitary representations are obtained.

The case of non-compact Lie groups is much less well understood, see for instance ([Graham-Vogan](#GrahamVogan), [Vogan 99](#Vogan99)).


## References

Introductions and survey include

* [[Alexandre Kirillov]], _Lectures on the orbit method_ (2004)

  [[David Vogan]], _Review of: Lectures on the orbit method_ ([pdf](http://www.ams.org/journals/bull/2005-42-04/S0273-0979-05-01065-7/S0273-0979-05-01065-7.pdf))

* [[David Vogan]], _Geometry and representations of reductive gorups_ (2007) ([pdf](http://www-math.mit.edu/~dav/rittC.pdf))

* J. Maes, _An introduction to the orbit method_ Master thesis (2011) ([web](http://igitur-archive.library.uu.nl/student-theses/2011-0622-200341/UUindex.html))

* Craig Jackson, _Symplectic manifolds, geometric quantization, and unitary representations of Lie groups_ ([pdf](http://go.owu.edu/~chjackso/Papers/topic.pdf))

* Reyer Sjamaar, _Notes on the orbit method and quantization_ (1997) ([[SjamaarOrbitMethod.pdf:file]])

Original references include

* &#1042;. &#1040;. &#1043;&#1080;&#1085;&#1079;&#1073;&#1091;&#1088;&#1075;, _&#1052;&#1077;&#1090;&#1086;&#1076; &#1086;&#1088;&#1073;&#1080;&#1090; &#1074; &#1090;&#1077;&#1086;&#1088;&#1080;&#1080; &#1087;&#1088;&#1077;&#1076;&#1089;&#1090;&#1072;&#1074;&#1083;&#1077;&#1085;&#1080;&#1081; &#1082;&#1086;&#1084;&#1087;&#1083;&#1077;&#1082;&#1089;&#1085;&#1099;&#1093; &#1075;&#1088;&#1091;&#1087;&#1087; &#1051;&#1080;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;., 1981, &#1090;&#1086;&#1084; 15, &#1074;. 1, &#1089;&#1090;&#1088;. 23&#8211;37,  [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1690&what=fullt&option_lang=rus); transl. V. A. Ginzburg, _Method of orbits in the representation theory of complex Lie groups_, Funct. Analysis and Its Appl. __1981__, 15:1, 18&#8211;28, [doi](http://dx.doi.org/10.1007/BF01082375)

* [[Bertram Kostant]], _Orbits and quantization theory_, Proc. ICM Nice 1970, 395-406, [djvu:597 K](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0395.0406.ocr.djvu), [pdf:1.1 M](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0395.0406.ocr.pdf)

* [[Bertram Kostant]], _Quantization and unitary representations. I. Prequantization_, in: Lectures in Modern Analysis and Applications III, Lec. Notes in Math. __170__, 87&#8211;208, [MR294568](http://www.ams.org/mathscinet-getitem?mr=294568); Russ. transl. by A. Kirillov: Uspehi Mat. Nauk __28__ (1973), no. 1(169), 163&#8211;225, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=4837&volume=28&year=1973&issue=1&fpage=163&what=fullt&option_lang=eng)

* [[Alexandre Kirillov]], _&#1059;&#1085;&#1080;&#1090;&#1072;&#1088;&#1085;&#1099;&#1077; &#1087;&#1088;&#1077;&#1076;&#1089;&#1090;&#1072;&#1074;&#1083;&#1077;&#1085;&#1080;&#1103; &#1085;&#1080;&#1083;&#1100;&#1087;&#1086;&#1090;&#1077;&#1085;&#1090;&#1085;&#1099;&#1093; &#1075;&#1088;&#1091;&#1087;&#1087; &#1051;&#1080;_, , Uspehi. Mat. Nauk. 17 (1962), 57-110, [Rus. pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=6513&what=fullt&option_lang=rus); transl. _Unitary representations of nilpotent Lie groups_, Russian Math. Surveys, 1962, 17:4, 53&#8211;104, [doi](http://dx.doi.org/10.1070%2FRM1962v017n04ABEH004118), [MR142001](http://www.ams.org/mathscinet-getitem?mr=142001)

* L. Auslander, [[Bertram Kostant]], _Quantization and representations of solvable Lie groups_, Bull. Amer. Math. Soc. __73__, 1967, 692&#8211;695, [pdf](http://www.ams.org/journals/bull/1967-73-05/S0002-9904-1967-11829-9/S0002-9904-1967-11829-9.pdf); _Polarization and unitary representations of
solvable Lie groups_, Invent. Math. __14__ (1971), 255&#8211;354, [MR293012](http://www.ams.org/mathscinet-getitem?mr=293012), [doi](http://dx.doi.org/10.1007/BF01389744)

* W. Graham, [[David Vogan]], _Geometric quantization for nilpotent coadjoint orbits_, in Geometry and Representation Theory of real and p-adic groups.
Birkh&#228;user, Boston-Basel-Berlin (1998)
 {#GrahamVogan}

* [[David Vogan]], _The method of coadjoint orbits for real reductive groups_, in Representation Theory of Lie Groups. IAS/Park City Mathematics Series 8 (1999), 179&#8211;238
 {#Vogan99}

Generalizations to [[supergeometry]] are discussed in

* Gijs M. Tuynman, _Geometric Quantization of Superorbits: a Case Study_ ([arXiv:0901.1811](http://arxiv.org/abs/0901.1811))

A generalization to [[higher geometry]] and [[2-group]] [[2-representations]] is proposed in 

* [[Bruce Bartlett]], _On unitary 2-representations of finite groups and topological quantum field theory_ ([arXiv:0901.3975](http://arxiv.org/abs/0901.3975))

See also

* wikipedia, _[orbit method](http://en.wikipedia.org/wiki/Orbit_method)_

[[!redirects method of coadjoint orbits]]
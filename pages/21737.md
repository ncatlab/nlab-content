
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Chern-Dold character_ is the natural generalization of the [[Chern character]] from [[topological K-theory]] to any [[generalized (Eilenberg-Steenrod) cohomology theory]]. It is given essentially by [[rationalization]] of [[Brown representability theorem|coefficient spectra]].


## Definition


For $E$ a [[spectrum]] and $E^\bullet$ the [[generalized (Eilenberg-Steenrod) cohomology theory|generalized cohomology theory]] it [[Brown representability theorem|represents]]

$$
  E^\bullet(X) \;\simeq\; \pi_{-\bullet} Maps(X,E)
$$

the _[[Chern-Dold character]] for $E$_ ([Buchstaber 70](#Buchstaber70)) is the map induced by [[rationalization]] over the [[real numbers]]

$$
  E \overset{L_{\mathbb{R}}}{\longrightarrow} E_{\mathbb{R}}
$$

i.e. is

\[
  \label{ChernDoldCharacter}
  chd
  \;\colon\;
  E^\bullet(X)
  \;\simeq\;
  \pi_{-\bullet}Maps(X,E)
  \overset{
    \pi_{-\bullet}Maps(X,L_{\mathbb{R}})
  }{\longrightarrow}
  \pi_{-\bullet}Maps(X,E_{\mathbb{R}})
  \;\simeq\;
  E^\bullet_{\mathbb{E}}(X)
  \;\simeq\;
  H^\bullet(X, \pi_{\bullet}(E)\otimes_{\mathbb{Z}}\mathbb{R})
  \,.
\]

The very last equivalence in (eq:ChernDoldCharacter) is due to [Dold 56, Cor. 4](#Dold56) (reviewed in detail in [Rudyak 98, II.3.17](#Rudyak98), see also  [Gross 19, Def. 2.5](#Gross19)).

One place where this neat state of affairs (eq:ChernDoldCharacter) is made fully explicit is [Lind-Sati-Westerland 16, Def. 2.1](#LindSatiWesterland16). Many other references leave this statement somewhat in between the lines (e.g. [Buchstaber 70](#Buchstaber70), [Upmeier 14](#Upmeier14)) and, in addition, often without reference to Dold (e.g. [Hopkins-Singer 02, Sec. 4.8](#HopkinsSinger02), [Bunke 12, Def. 4.45](#Bunke12), [Bunke-Gepner 13, Def. 2.1](#BunkeGepner13), [Bunke-Nikolaus 14, p. 17](#BunkeNikolaus14)).

Beware that some authors say _[[Chern-Dold character]]_ for the full map in (eq:ChernDoldCharacter) (e.g. 
[Buchstaber 70](#Buchstaber70), 
[Upmeier 14](#Upmeier14), [Lind-Sati-Westerland 16, Def. 2.1](#LindSatiWesterland16)), while other authors mean by this only that last equivalence in (eq:ChernDoldCharacter) (e.g. [Rudyak 98, II.3.17](#Rudyak98), [Gross 19, Def. 2.5](#Gross19)).

## Exanples

Examples of [[Chern-Dold characters]]: 

* [[Chern character]] on [[KU]];

* [[Pontrjagin character]] on [[KO]].

Further examples listed in [FSS 20](#FSS20)

## References

The identification of rational [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]] as [[ordinary cohomology]] with [[coefficients]] in the rationalized [[stable homotopy groups]] is due to

* {#Dold56} [[Albrecht Dold]], _Relations between ordinary and extraordinary homology_, Matematika, 9:2 (1965), 8–14; Colloq. algebr. Topology, Aarhus Universitet, 1962, 2–9 ([mathnet:mat350](http://mi.mathnet.ru/eng/mat350)), reprinted in: J. Adams & G. Shepherd (Authors), _Algebraic Topology: A Student's Guide_ (London Mathematical Society Lecture Note Series, pp. 166-177). Cambridge: Cambridge University Press 1972 ([doi:10.1017/CBO9780511662584.015](https://doi.org/10.1017/CBO9780511662584.015)) 

reviewed in

* [Hilton 71, Theorem 3.18](#Hilton71)

* {#Rudyak98} [[Yuli Rudyak]], II.7.13 in: _On Thom Spectra, Orientability, and Cobordism_, Springer 1998 ([doi:10.1007/978-3-540-77751-9](https://doi.org/10.1007/978-3-540-77751-9))


* {#Gross19} Jacob Gross, _The homology of moduli stacks of complexes_ ([arXiv:1907.03269](https://arxiv.org/abs/1907.03269))


The combination of [Dold 56](#Dold56) to the [[Chern-Dold character]] on [[generalized (Eilenberg-Steenrod) cohomology theory]] is due (for [[complex cobordism cohomology]]) to

* {#Buchstaber70} [[Victor Buchstaber]], _The Chern–Dold character in cobordisms. I_, 

  Russian original: Mat. Sb. (N.S.), 1970 Volume 83(125), Number 4(12), Pages 575–595 ([mathnet:3530](http://m.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=sm&paperid=3530&option_lang=eng))

  English translation: Mathematics of the USSR-Sbornik, Volume 12, Number 4, AMS 1970 ([doi:10.1070/SM1970v012n04ABEH000939](https://iopscience.iop.org/article/10.1070/SM1970v012n04ABEH000939))

Review in 

* [Hilton 71, p. 50](#Hilton71)

That the Chern-Dold character reduces to the original Chern character on K-theory is

* [Hilton 71, Theorem 5.8](#Hilton71).


That the Chern-Dold character is given by rationalization of representing spectra is made fully explicit in 

* {#LindSatiWesterland16} [[John Lind]], [[Hisham Sati]], [[Craig Westerland]], Section 2.1: _Twisted iterated algebraic K-theory and topological T-duality for sphere bundles_, Ann. K-Th. 5 (2020) 1-42 ([arXiv:1601.06285](https://arxiv.org/abs/1601.06285))

This rationalization construction appears also (without attribution to [#Hilton 71](#Hilton71) or [Buchstaber 70](#Buchstaber70) or [Dold 56](#Dold56)) in the following articles (all in the context of [[differential cohomology]]):

* {#HopkinsSinger02} [[Mike Hopkins]], [[Isadore Singer]], Section [4.8, page 47](http://arxiv.org/PS_cache/math/pdf/0211/0211216v2.pdf#page=47) of _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_, ([math.AT/0211216](http://arxiv.org/abs/math.AT/0211216)).

* {#Bunke12} [[Ulrich Bunke]], _Differential cohomology_ ([arXiv:1208.3961](http://arxiv.org/abs/1208.3961))

* {#BunkeGepner13} [[Ulrich Bunke]], [[David Gepner]], around def. 2.1 of: _Differential function spectra, the differential Becker-Gottlieb transfer, and applications to differential algebraic K-theory_ ([arXiv:1306.0247](http://arxiv.org/abs/1306.0247))

* {#Upmeier14} Markus Upmeier, _Refinements of the Chern-Dold Character: Cocycle Additions in Differential Cohomology_,  J. Homotopy Relat. Struct. 11, 291–307 (2016). ([arXiv:1404.2027](https://arxiv.org/abs/1404.2027), [doi:10.1007/s40062-015-0106-y](https://doi.org/10.1007/s40062-015-0106-y))

* {#BunkeNikolaus14} [[Ulrich Bunke]], [[Thomas Nikolaus]], _Twisted differential cohomology_, Algebr. Geom. Topol. Volume 19, Number 4 (2019), 1631-1710. ([arXiv:1406.3231](http://arxiv.org/abs/1406.3231), [euclid:euclid.agt/1566439272](https://projecteuclid.org/euclid.agt/1566439272))

More on the [[Chern-Dold character]] on [[complex cobordism cohomology]]:

* [[Victor Buchstaber]], A. P. Veselov, _Chern-Dold character in complex cobordisms and abelian varieties_ ([arXiv:2007.05782](https://arxiv.org/abs/2007.05782))

The observation putting this into the general context of [[differential cohomology diagrams]] (see there) of [[stable homotopy types]] in [[cohesion]] is due to

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], section 4.4. of _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

based on [Bunke-Gepner 13](#BunkeGepner13).

Further generalization of the [[Chern-Dold character]] to [[non-abelian cohomology]]:

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The character map in (twisted differential) non-abelian cohomology]]_ ([arXiv:2009.11909](https://arxiv.org/abs/2009.11909))


The [[equivariant Chern-Dold character]] in [[equivariant cohomology]]:

* [[Wolfgang Lück]], _Chern characters for proper equivariant homology theories and applications to K- and L-theory_, Journal für die reine und angewandte Mathematik, Volume 2002: Issue 543 ([doi:10.1515/crll.2002.015](https://doi.org/10.1515/crll.2002.015), [pdf](https://www.him.uni-bonn.de/lueck/data/eh.pdf))

* [[Wolfgang Lück]], _Equivariant Cohomological Chern Characters_, International Journal of Algebra and Computation, Vol. 15, No. 05n06, pp. 1025-1052 (2005) ([arXiv:math/0401047](https://arxiv.org/abs/math/0401047), [doi:10.1142/S0218196705002773](https://doi.org/10.1142/S0218196705002773))


* [[Wolfgang Lück]], _Equivariant Chern characters_, 2006 ([pdf](https://www.him.uni-bonn.de/lueck/data/goettingen_equi_Chern061130trans.pdf), [[LuckEquivariantChernCharacters.pdf:file]])




[[!redirects Dold-Chern characters]]


[[!redirects Chern character map]]
[[!redirects Chern character maps]]

[[!redirects Chern-Dold character]]
[[!redirects Chern-Dold characters]]

[[!redirects Chern-Dold character map]]
[[!redirects Chern-Dold character maps]]



[[!redirects Dold-Chern character map]]
[[!redirects Dold-Chern character maps]]



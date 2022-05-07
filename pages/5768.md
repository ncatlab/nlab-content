
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Tropical geometry is often thought of as the [[algebraic geometry]] over the [[tropical semiring]]. Many central results are combinatorial in nature, with relations to the (geometry and combinatorics of) polyhedra, [[matroid]]s, [[cluster algebra]]s and toric geometry. Recently it found applications in explaining [[mirror symmetry]] at a more fundamental level (see e.g. [Gross 11](#Gross11)). 


Tropical algebraic geometry establishes and studies some very general principles to translate algebro-geometric problems into purely combinatorial ones.

*Example*
In algebraic geometry one often work with polynomials. In tropical geometry, these polynomials are
"tropicalized"  and this turns them into piecewise linear functions. 


For instance: $f (x, y) = x^2 + y^2-1$. 

This tropicalizes to $trop(f ) = x^2 \oplus y^2 \oplus 0 = 
min(2x, 2y, 0)$, and this is a piecewise linear curve.

(To see this remember that in the [[tropical semiring]], the sum of two numbers is their minimum, and their product is their sum. $x^2 = x\oplus x$, $y^2 = y\oplus y$ and so $x^2+y^2$  converts to $min(2x,2y)$. The 0 will remain mysterious for the moment.  (If you cannot wait look at the AARMS notes listed below.))

## Related concepts

 * [[tropical semiring]]

##References

###Books and Lecture Notes

Textbook accounts/lecture notes include

*  [[Diane Maclagan]], [[Bernd Sturmfels]] _Introduction to tropical geometry_, [draft book](http://homepages.warwick.ac.uk/staff/D.Maclagan/papers/TropicalBook.pdf)

* {#Gross11} [[Mark Gross]], _Tropical geometry and mirror symmetry_, CBMS regional conf. ser. 114 (2011), based on the CBMS course in Kansas, [AMS book page](http://www.ams.org/bookstore-getitem/item=CBMS-114), [pdf](http://www.math.ucsd.edu/~mgross/kansas.pdf)

* G. Mikhalkin, _Tropical geometry_, book, early draft, [scribd](http://www.scribd.com/doc/47771116/Tropical-geometry-Grigory-Mikhalkin); _Tropical geometry and its applications_, Proc. Intern. Congr. Math.,
V. 2 (Madrid, 2006), Eur. Math. Soc., Z&#252;rich, 2006, 827&#8211;852 [djvu](http://www.mathunion.org/ICM/ICM2006.2/Main/icm2006.2.0827.0852.ocr.djvu) [pdf](http://www.mathunion.org/ICM/ICM2006.2/Main/icm2006.2.0827.0852.ocr.pdf)

* [[Diane Maclagan]], [AARMS Tropical Geometry](http://homepages.warwick.ac.uk/staff/D.Maclagan/AARMS/AARMSTropical.pdf):lecture notes from a four week graduate summer school on Tropical Geometry held at the University of New Brunswick in July/August 2008 under the auspices of the Atlantic Association for Research in the Mathematical Sciences (AARMS).

* MSRI introductory workshop on tropical geometry [page](http://www.msri.org/web/msri/scientific/workshops/show/-/event/Wm483), Aug 24-28, 2009 (with videos of the lectures)
* Erwan Brugall&#233;, Kristin Shaw, _A bit of tropical geometry _, [arxiv/1311.2360](http://arxiv.org/abs/1311.2360)

### Collections of articles

* (CM580) Tropical geometry and integrable systems, [Contemp. Math. __580__](http://www.ams.org/bookstore-getitem/item=CONM-580), Amer. Math. Soc., Providence, RI, 2012 
* _Tropical and idempotent mathematics_, [pdf](http://www.mccme.ru/tropical12/Tropics2012final.pdf), proceedings conf. Moscow 2012

###Papers and Preprints

* [[Dan Abramovich]], _Moduli of algebraic and tropical curves_, [arxiv/1301.0474](http://arxiv.org/abs/1301.0474)
* [[Dan Abramovich]], Lucia Caporaso, Sam Payne, _The tropicalization of the moduli space of curves_, [arxiv/1212.0373](http://arxiv.org/abs/1212.0373)

* I. Itenberg, G. Mikhalkin, _Geometry in the tropical limit_, [arXiv:
1108.3111](http://arxiv.org/abs/1108.3111)

* M. Einsiedler, [[M. Kapranov]], D. Lind, _Non-archimedean amoebas and tropical varieties_, [math.AG/0408311](http://arxiv.org/abs/math/0408311)
* [[Mikhail Kapranov]], _Thermodynamics and the moment map_, [arxiv/1108.3472](http://arxiv.org/abs/1108.3472)
* Walter Gubler, _A guide to tropicalizations_, [arxiv/1108.6126](http://arxiv.org/abs/1108.6126)
* E. Katz, _A tropical toolkit_, [math.AG/0610878](http://arxiv.org/abs/math/0610878) (Expo. Math. 27 (2009), No. 1, 1-36)
* Oleg Viro, _Hyperfields for tropical geometry I. hyperfields and dequantization_, [arxiv/1006.3034](http://arxiv.org/abs/1006.3034); _Tropical geometry and hyperfields_, talk at Mathematics - XXI century. PDMI 70th anniversary, [video](http://www.mathnet.ru/php/presentation.phtml?option_lang=eng&presentid=1286); _On basic concepts of tropical geometry_, Trudy Mat. Inst. Steklova __273__ (2011),  271&#8211;303
* Patrick Popescu-Pampu, Dmitry Stepanov, _Local tropicalization_, [arxiv/1204.6154](http://arxiv.org/abs/1204.6154) 
* W. Gubler, _Tropical varieties for non-Archimedean analytic spaces_, Invent. Math. __169__ (2007), 321&#8211;376.
* David Speyer, [[Bernd Sturmfels]], _Tropical mathematics_, [math.CO/0408099](http://arxiv.org/abs/math/0408099); _The tropical Grassmannian_, Adv. Geom. 4 (2004) 389–411 [math.AG/0304218](https://arxiv.org/abs/math/0304218) [emis](http://emis.ams.org/journals/AG/4-3/4_389.pdf)
* Andreas Gathmann, _Tropical algebraic geometry_, [math.AG/0601322](http://arxiv.org/abs/math/0601322)
* [[Diane Maclagan]], _Polyhedral structures on tropical varieties_, [arXiv:1302.5372](http://arxiv.org/abs/1302.5372)
* Paul Johnson, _Hurwitz numbers, ribbon graphs, and tropicalization_, [arxiv/1303.1543](http://arxiv.org/abs/1303.1543) (pages 55-72 in CM580)  
* Brugalle Erwan, Markwig Hannah, _Deformation of tropical Hirzebruch surfaces and enumerative geometry_, [arxiv/1303.1340](http://arxiv.org/abs/1303.1340)
* Qingchun Ren, Steven V Sam, Bernd Sturmfels, _Tropicalization of classical moduli spaces_, [arxiv/1303.1132](http://arxiv.org/abs/1303.1132)

* Martin Ulirsch, _Functorial tropicalization of logarithmic schemes: The case of constant coefficients_, [arxiv/1310.6269](http://arxiv.org/abs/1310.6269)
* Luis Felipe Tabera, _On real tropical bases and real tropical discriminants_, [arxiv/1311.2211](http://arxiv.org/abs/1311.2211)

* Simon Hampe, _Tropical linear spaces and tropical convexity_, [arxiv/1505.02045](http://arxiv.org/abs/1505.02045)

* Tyler Foster, _Introduction to adic tropicalization_, [arxiv/1506.00726](http://arxiv.org/abs/1506.00726)

* G. Mikhalkin, _Quantum indices of real plane curves and refined enumerative geometry _, [arxiv/1505.04338](http://arxiv.org/abs/1505.04338)

> We associate a half-integer number, called the quantum index, to algebraic curves in the real plane satisfying to certain conditions. The area encompassed by the logarithmic image of such curves is equal to $\pi^2$ times the quantum index of the curve. We use the quantum index to refine real enumerative geometry in a way consistent with the Block-G\"ottsche invariants from tropical enumerative geometry.

*  Diane Maclagan, Felipe Rinc&#243;n, _Tropical ideals_, [arxiv/1609.03838](http://arxiv.org/abs/1609.03838)

* Kiumars Kaveh, Christopher Manon, _Khovanskii bases, Newton-Okounkov polytopes and tropical geometry of projective varieties_, [arxiv/1610.00298](https://arxiv.org/abs/1610.00298)

*  [[Alain Connes]], [[Caterina Consani]], _Geometry of the scaling site_, [arxiv/1603.03191](https://arxiv.org/abs/1603.03191) 

* Keyvan Yaghmayi, _Geometry over the tropical dual numbers_, [arxiv/1611.05508](https://arxiv.org/abs/1611.05508)

An alternative algebraic framework for tropical mathematics (not based on semirings), "more compatible with valuation theory" has been proposed in

* Zur Izhakian, Manfred Knebusch, Louis Rowen, _Algebraic structures of tropical mathematics_, [arxiv/1305.3906](http://arxiv.org/abs/1305.3906) 

Connections to diophantine integration (involving p-adic integration):

* Eric Katz, Joseph Rabinoff, David Zureick-Brown, _Diophantine and tropical geometry, and uniformity of rational points on curves_, [arxiv/1606.09618](http://arxiv.org/abs/1606.09618)

###Miscellaneous: MO questions, discussions, etc.

* MathOverflow : [Mikhalkin's tropical schemes versus Durov's tropical schemes](http://mathoverflow.net/questions/72613/mikhalkins-tropical-schemes-versus-durovs-tropical-schemes), [learning-tropical-geometry](http://mathoverflow.net/questions/84629/learning-tropical-geometry)

* [wikipedia page](http://en.wikipedia.org/wiki/Tropical_geometry)

* $n$Cafe: [Tight spans, Isbell completions and semi-tropical modules](http://golem.ph.utexas.edu/category/2013/01/tight_spans_isbell_completions.html) 

category: geometry
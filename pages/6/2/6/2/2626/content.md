
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Knots
* table of contents
{: toc}

The theory of knots is very visual. It can provide a link between the concrete and abstract.  Some of the arguments are quite elementary, others very deep, and there are numerous connections with other parts of mathematics.


## Definition

A __knot__ is a [[smooth map|smooth]] (or piecewise-affine) [[embedding]] of the [[circle]] $S^1$ into $\mathbb{R}^3$, or equivalently into the $3$-[[sphere]] $S^3$ (one can also consider knots in other [[3-manifold]]s).

Sometimes, higher dimensional knots are also considered. An $n$-dimensional knot (or simply an $n$-knot) is a smooth embedding of an $n$-dimensional closed manifold (usually an $n$-sphere) into the $(n+2)$-dimensional sphere $\mathbb{S}^n$.  

Typically, knots are considered up to [[ambient isotopy]] (or [[smooth isotopy]]).

Knots that are ambient isotopic are often said to have the *same knot type* or to be *in the same isotopy class*.

## Example

The [[trefoil knot]] is the simplest non-trivial knot.  In its simplest representation, it has three crossings.  It is a [[torus knot]], that is it can be embedded on the surface of a solid torus, itself embedded in $S^3$. Here is a picture.

+--{: style="text-align:center"}
[[!include trefoil knot - SVG]]
=--

Classifying knots up to isotopy is usually done using [[knot invariants]]. Some of these are simple to define (these tend to be geometric and also tend to be hard to calculate) others are harder to define and to show they are invariants but are easier to calculate. A few are reasonably easy to define and to calculate... Yippee!

It is often useful to consider the domain circle of a knot as being oriented.  This is then represented by putting a directional arrow on diagrams of the knot. Such oriented knots are usually considered up to [[ambient isotopy]] in which the isotopy is orientation preserving. This leads to the idea of [[invertible knot|invertible knots]].  It is also possible to take the [[mirror reflection]] of  knots and thus to introduce the concept of [[knot chirality]], a [[knot invariant]]; Knots that remain equivalent to their mirror images possess a certain symmetry called [[achiral knot|achiral knots]] or equivalently, [[amphicheiral]]. An alternative definition of this notion is the following: 
A knot $K$ is [[amphicheiral]] if there exists an orientation-reversing [[homeomorphism]] of $R^3$ mapping $K$ to itself. 


## Relevant nLab Pages

### Knots, Links, and other Variants

The theory of knots can be extended to include various similar things:

* [[links]]
* [[braids]]
* [[strings]]
* [[tangles]]
* [[singular knots]]

### Invariants

A major line in the study of knots is to look for [[knot invariants]] (see also [[link invariants]]).

### Ancillary pages

There are various pages related to knot theory that are linked from the main articles.

* [[Vassiliev skein relations]]
* [[Reidemeister moves]]

### Images

The study of knots is very pictorial.  There are various knot-related SVGs that can be included in to nLab pages.

* [[SVG images]]

## Related concepts

* [[space of knots]]

* [[knot complement]]

* [[knot diagram]]

* [[isotopy]], [[smooth isotopy]]

* [[Kirby calculus]]

* [[torus knot]]

* [[hyperbolic knot]]

* [[surface knot]]

* [[slice knot]]

* [[boxed knot]], [[knot sum]]

* [[MKR dictionary]] in [[arithmetic topology]]

* [[chord diagram]]

* [[Wilson loop]]

* [[knots-quivers correspondence]]

* [[quantum topology]]

[[!include chord diagrams and weight systems -- table]]



## References

### General

Historically, a motivation for [[Peter Tait]] to start thinking about classification of [[knots]] was the book 

* [[Lord Kelvin]], _[[On Vortex Atoms]]_

which presented the speculation in [[physics]] that  [[atoms]]/[[elementary particles]] are fundamentally [[vortices]] in a [[spacetime]]-filling fluid-like substance.

Expositions of modern knot theory:

* J. Hoste, M. Thistlethwaite, J. Weeks: _The First 1,701,936 Knots_, The Mathematical Intelligencer **20** (1998) 33–48 &lbrack;[doi:10.1007/BF03025227](https://doi.org/10.1007/BF03025227)&rbrack;

* Sam Nelson: *The Combinatorial Revolution in Knot Theory*, Notices of the AMS **58** 11 (2011) &lbrack;[pdf](https://math.mit.edu/~ormsby/nelson-combinatorial-revolution.pdf), full issue: [pdf](https://www.ams.org/notices/201111/201111FullIssue.pdf)&rbrack;

* [[Aaron Lauda]], _Knot theory explained_, (1:24 min lightning idea), USC Dornsife College of Letters, Arts and Sciences (2015) &lbrack;video: [YT](https://youtu.be/kxaWqKM5JyQ)&rbrack;

* [[Abhijit Champanerkar]], _The geometry of knot complements_ &lbrack;[pdf](https://www.math.csi.cuny.edu/~abhijit/talks/knot-geometry-h.pdf), [[ChampanerkarKnotComplements.pdf:file]]&rbrack;

* Roland van der Veen: *A smooth introduction to knots*, lecture notes (2016) &lbrack;[pdf](https://www.julianlyczak.nl/seminar/knots2016-files/KnotesJan18.pdf), [[vdVeen-SmoothKnots.pdf:file]]&rbrack;


Monographs:

* [[Richard H. Crowell]], [[R. H. Fox]], _Introduction to knot theory_, Graduate Texts in Mathematics **57**, Springer (1963) &lbrack;[doi:10.1007/978-1-4612-9935-6](https://doi.org/10.1007/978-1-4612-9935-6)&rbrack;

* G. Burde, H. Zieschang, _Knots_, De Gruyter (1989).

* [[Michael Atiyah]], _The Geometry and Physics of Knots_,  Cambridge University Press (1990) &lbrack;[doi:10.1017/CBO9780511623868](https://doi.org/10.1017/CBO9780511623868)&rbrack;

* [[Vladimir Turaev]]: *Quantum invariants of knots and 3-manifolds*, de Gruyter Studies in Mathematics **18**, de Gruyter & Co. (1994) &lbrack;[doi:10.1515/9783110435221](https://doi.org/10.1515/9783110435221), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/turaev5.pdf)&rbrack;


* Colin C. Adams, *The Knot Book -- An elementary Introduction to the Mathematical Theory of Knots*,  W. H. Freedman and Co. (1994) &lbrack;[ISBN:978-0-8218-3678-1](https://bookstore.ams.org/KNOT)&rbrack;


* [[Nick Gilbert]], [[Tim Porter]], *Knots and surfaces*, Oxford University Press (1994) &lbrack;[ISBN:9780198514909](https://global.oup.com/academic/product/knots-and-surfaces-9780198514909?cc=de&lang=en&)&rbrack;

* [[Tomotada Ohtsuki]]: *Quantum Invariants -- A Study of Knots, 3-Manifolds, and Their Sets*, World Scientific (2001) &lbrack;[doi:10.1142/4746](https://doi.org/10.1142/4746)&rbrack;

* [[Seiichi Kamada]]: *Classical Braids and Links*, Part 1 of: *Braid and Knot Theory in Dimension Four*, Mathematical Surveys and Monographs **95**, AMS (2002) &lbrack;[ISBN:978-0-8218-2969-1](https://bookstore.ams.org/view?ProductCode=SURV/95)&rbrack;


* [[Dale Rolfsen]], _Knots and links_, AMS Chelsea __346__ (2003) &lbrack;[ams:chel-346-h](https://bookstore.ams.org/chel-346-h), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/rolfsen.pdf)&rbrack;

* {#Sossinsky23} [[Alexei B. Sossinsky]], *Knots, Links and Their Invariants: An Elementary Course in Contemporary Knot Theory*, The Student Mathematical Library **101**, AMS (2023) &lbrack;[doi:10.1090/stml/101](https://doi.org/10.1090/stml/101)&rbrack;

In higher dimensions:

* [[Andrew Ranicki]]: *High-dimensional knot theory -- Algebraic Surgery in Codimension 2*, Monographs in Mathematics, Springer (1998, 2009) &lbrack;[doi:10.1007/978-3-662-12011-8](https://doi.org/10.1007/978-3-662-12011-8), [pdf](https://www.maths.ed.ac.uk/~v1ranick/knot.pdf)&rbrack;
  > (via [[surgery]] and [[algebraic K-theory]] and [[L-theory]])




### Relation to physics

Relation of knot theory to [[physics]]/[[quantum field theory]]:

* [[Louis Kauffman]], _Knots and physics_, Series on _Knots and Everything_, Volume 1,  World Scientific, 1991 ([doi:10.1142/1116](https://doi.org/10.1142/1116))

* [[Louis Kauffman]] (ed.) _The Interface of Knots and Physics_, Proceedings of Symposia in Applied Mathematics
Volume 51 (1996) ([pdf](http://www.csee.umbc.edu/~lomonaco/kelvin/kelvin23.pdf), [doi:10.1090/psapm/051](https://doi.org/10.1090/psapm/051))

and with emphasis on [[TQFT]]:

* [[Dmitry Melnikov]]: *A Tutorial on Knots and Quantum Mechanics* &lbrack;[arXiv:2503.08846](https://arxiv.org/abs/2503.08846)&rbrack;


In [[string theory]] ([[NS5-branes]]/[[M5-branes]]):

* [[Edward Witten]], _Fivebranes and Knots_, Quantum Topology, Volume 3, Issue 1, 2012, pp. 1-137 ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216), [doi:10.4171/QT/26](https://www.ems-ph.org/journals/show_abstract.php?issn=1663-487X&vol=3&iss=1&rank=1))



### Higher dimensional knots

* D. Roseman, _Reidemeister-type moves for surfaces in four dimensional space_, Banach Center Publication, __42__ (1998), 347-380 [pdf](http://matwbn.icm.edu.pl/ksiazki/bcp/bcp42/bcp42124.pdf) [doi](https://doi.org/10.4064/-42-1-347-380)

* J. S. Carter, M. Saito, _Knotted surfaces and their diagrams_, Mathematical Surveys and Monographs __55__, Amer. Math. Soc., Providence, RI, 1998

* V. A. Rohlin, _The embedding of non-orientable three-manifolds into five-dimensional Euclidean space_, Dokl. Akad. Nauk SSSR __160__ (1965) 549–551 (in Russian; English transl.: Soviet Math. Dokl. 6 (1965), 153–156)

* I.G. Korepanov, G.I. Sharygin, D.V. Talalaev, _Cohomology of the tetrahedral complex and quasi-invariants of 2-knots_, [arxiv/1510.03015](https://arxiv.org/abs/1510.03015)

* J. E. Fischer, Jr. _2-Categories and 2-knots_, Duke Math. J. 75 (1994), 493–596.

category: knot theory

[[!redirects knot]]
[[!redirects knots]]
[[!redirects Knot]]
[[!redirects Knots]]

[[!redirects Knot Theory]]
[[!redirects knot theory]]
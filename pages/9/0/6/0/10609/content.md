
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

> To speak of points of space, as if they constituted the positive element of space, is inadmissible ([PdN&#167;254b](Science+of+Logic#PN254b))

> That the line does not consist of points, nor the plane of lines, follows from their concepts ([PdN&#167;256b](Science+of+Logic#PN256b))


_Synthetic geometry_ is about formalization of [[geometry]] by [[axioms]] that directly speak about the fundamental concepts of geometry -- such as points and lines -- instead of about a backdrop for such objects -- such as [[Cartesian spaces]].

In the 19th century, after [[noneuclidean geometries]] were found (Lobachevski, Bolya, Gauss), mathematicians reexamined the [[foundations]] of [[geometry]]. Some schools concentrated on the [[axiom|axiomatic]] construction of geometry,  independent from the tools which were offered by the [[models]] with concrete [[coordinate]] [[algebra of functions|algebras]]. Synthetic geometry in this sense referred to doing geometry without recourse to [[algebras of functions]] and analytic computations. This was especially successful in [[projective geometry]], see _[[synthetic projective geometry]]_.

The main part of synthetic geometry is the study of incidence structures in geometry, sometimes also called [[incidence geometry]]. A modern point of view on incidence geometry is through the theory of [[buildings]]. 

## Comparison to synthetic differential geometry
 {#ComparisonToSDG}

This perspective of synthetic geometry is somewhat different from the more modern subject called _[[synthetic differential geometry]]_, although the terminology has the same origin. Indeed, in view of the fact that in the axiomatic approach the emphasis is on the relationship between the elements of geometry ([[points]], [[lines]], [[curves]]) and that in modern geometry these are viewed as subvarieties, hence [[subobjects]], in his original axiomatization of _[[synthetic differential geometry]]_ [[William Lawvere]] has reinterpreted the meaning of synthetic geometry as being concerned with the categorical relationship between geometrical objects. However, he was not concerned with working without analytic and algebraic calculations (which do appear in his axioms for [[infinitesimally thickened points]], the _[[Kock-Lawvere axioms]]_); he just wanted to introduce the foundations internally. (But this is different for his later development of [[cohesion|cohesive geometry]] which includes the original synthetic differential geometry via _[[differential cohesion]]_. Here no analysis enters the [[axioms]].)


Lawvere also notes the  failure (for physical applications) of the correspondence between evolution paths and corresponding maps in differential geometry, and wanted to work in [[closed monoidal categories]] (having the [[exponential law]] for [[mapping spaces]]). In [[synthetic differential geometry]], which he created with Kock, Dubuc and others, this enabled also intuitive, pre-Cauchy reasoning with [[differentials]], what also reminded him of 19th century mathematics what probably also influenced on choosing the name. But still, the subject of synthetic differential geometry is non-synthetic in the sense of traditional 
synthetic geometry. A genuinely synthetic axiomatization of differential geometry is [[cohesion]].


## Related concepts

| [[synthetic geometry]]  |
|-------------------------|
| [[Euclidean geometry]]  |
| [[hyperbolic geometry]] |
| [[elliptic geometry]]   |

* [[parallel postulate]]

* [[synthetic mathematics]]

* [[geometric homotopy type]]

* [[cohesive homotopy type]]

## References

* Wikipedia, _[Synthetic geometry](http://en.wikipedia.org/wiki/Synthetic_geometry)_

* {#Tarski} [[Alfred Tarski]], _What is elementary geometry?_, in _The axiomatic method. With special reference to geometry and physics_ Proceedings of an International Symposium held at the Univ. of Calif., Berkeley, Dec. 26, 1957-Jan. 4, 1958 (ed. L. Henkin, P. Suppes, and A. Tarski), Studies in Logic and the Foundations of Mathematics, Amsterdam: North-Holland (1959), pp. 16&#8211;29. ([pdf](http://www.geographicknowledge.de/SeminarLFG/Tarski_Whatiselementarygeometry.pdf))

A textbook account of the axiomatization of [[Euclidean geometry]] is

* [[Wolfram Schwabhäuser]], [[Wanda Szmielew]], [[Alfred Tarski]], _Mathematische Methoden in der Geometrie_, Springer 1983

Full formalization of this book in [[Coq]] (as synthetic geometry but following Tarski's work) is discussed at 

*  [[Gabriel Brau]], [[Pierre Boutry]], [[Julien Narboux]], _[GeoCoq](http://geocoq.github.io/GeoCoq/)_, _[La g&#233;om&#233;trie de Tarski en Coq](http://gabrielbraun.free.fr/Geometry/Tarski/)_
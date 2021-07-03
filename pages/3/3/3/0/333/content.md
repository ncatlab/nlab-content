
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Spaces can be characterized by their [[algebra|algebras]] of functions (see at [[Isbell duality - table]]).

Using this [[duality]] between [[space and quantity]] one can define generalized spaces in terms of generalizations of their algebras of functions.

The idea of noncommutative geometry is to encode everything about the geometry of a space algebraically and then allow all commutative function algebras to be generalized to possibly non-commutative algebras. 

More generally, __noncommutative geometry__ means replacing the space by some structure carried by an entity (or a collection of entities) living on that would-be space. The entity may be for example a function, vector bundle, coherent sheaf, a complex of sheaves and KK-theory class. Objects organize into [[associative algebras]], [[operator algebras]],
[[categories]], higher categories ($k$-linear or not) and so on; and sometimes such a collection represents a space.  [[reconstruction|Reconstruction]] theorems are theorems on construction of a genuine (say topological) "underlying" space of such an entity or collection.  Spectral theories are procedures (sometimes functors, often not) which recover some form of underlying space called [[spectrum (geometry)|spectrum]], often just partially or under strong assumptions on (the data determining) the noncommutative space.

Under the process of forming [[groupoid convolution algebras]] a good bit of commutative but [[higher geometry]] translates into noncommutative geometry. This is for instance the origin of the role of noncommutative geometry in [[twisted K-theory]].

## Definitions

### Connes' noncommutative geometry 

A particular and most prominent realization of the program of noncommutative geometry has been lead by [[Alain Connes]]. This is really "[[spectrak geometry|spectral]]" and possibly non-commutative [[Riemannian geometry]], where the metric structure on a possibly noncommutative "[[algebra of functions]]" is encoded by a structure called a _[[spectral triple]]_ (see there for more). 

The central ingredients in Connes' noncommutative geometry are

* the idea to characterize a (noncommutative) space by a [[C-star algebra]] $A$, to be thought of as the $C^*$-[[algebra of functins|algebra of global functions]] on that space; this approach has been occasionally considered earlier e.g. in the book of Semadeni on Banach algebras. 

* There is a refined, quantized differential calculus where the differential is given by a commutator formula involving a Fredholm operator; the setup in which this is taken place involves cyclic cocycles discovered by Tsygan and Connes.

* the noncommutative analog of the structure of a [[Riemannian manifold]] with a spin structure in terms of generalized [[Dirac operator]]s $D$ acting on a representation space of the algebra $A$. Metric information on the space is then encoded in the spectrum of $D$.

For that reason [[Alain Connes|Connes]]' noncommutative manifolds are well described as **spectral geometry**. The Dirac operator is, of course, very much related to the quantized differential calculus of Connes. 

* Noncommutative measure spaces are represented by noncommutative von Neumann algebras. 

In noncommutative geometry various homotopical and (co)homological invariants were introduced by large amount of improvisation, similar to the beginnings of algebraic topology, but more recently there are few systematic approaches to homotopy theory emerging. See [[model structure on operator algebras]].


## Related concepts

* [[noncommutative topology]], [[noncommutative measure theory]], [[noncommutative probability theory]]

* [[groupoid algebra]]

* [[noncommutative torus]], [[fuzzy sphere]]

* [[noncommutative topology of quasiperiodicity]]

* [[noncommutative scheme]]

* [[non-commutative analytic space]]

* [[QFT on non-commutative spacetime]]

* [[noncommutative motive]]

* [[Riemann hypothesis and physics]]

* [[D-brane geometry]]

* [[noncommutative algebraic geometry]]

* [[derived noncommutative geometry]]

[[!include Isbell duality - table]]


## References

### General


* [[Alain Connes]], _[[Noncommutative Geometry]]_, Academic Press, San Diego, CA, 1994 ([ISBN:9780080571751](https://www.elsevier.com/books/noncommutative-geometry/connes/978-0-08-057175-1), [pdf](http://www.alainconnes.org/docs/book94bigpdf.pdf))

* [[José Gracia-Bondia]], [[Joseph Varilly]], H&#233;ctor Figueroa, _Elements of noncommutative geometry_, Birkh&#228;user 2001. xviii+685 pp. ([doi:10.1007/978-1-4612-0005-5](https://link.springer.com/book/10.1007/978-1-4612-0005-5), [gBooks](http://books.google.hr/books?id=2yJIwWbh1isC&lpg=PP1&ots=ex0Xfmh_UU&dq=Varilly%20noncommutative&hl=en&pg=PP1#v=onepage&q=Varilly%20noncommutative&f=false))



Exposition:

* {#Lupercio20} [[Ernesto Lupercio]], _Non-commutative Geometry Indomitable_ ([arXiv:2008.08529](https://arxiv.org/abs/2008.08529))

See also:

* {#Connes95} [[Alain Connes]], _Noncommutative geometry and reality_, J. Math. Phys. 36 (11), 1995 ([pdf](http://www.alainconnes.org/docs/reality.pdf))


* [[Alain Connes]], _A walk in the non-commutative garden_ ([arXiv:math/0601054](http://arxiv.org/abs/math/0601054))


With a view towards [[motives in physics]]:

* [[Alain Connes]], [[Matilde Marcolli]], _[[Noncommutative Geometry, Quantum Fields and Motives]]_


### Very early sources and schools

There are many sources of noncommutative spaces, e.g. [[quantization]] in [[physics]] (Snyder studied an interesting noncommutative space in the late 1940s). It has been often noticed, since Gel'fand--Neimark's work (see [[Gelfand spectrum]]), that many geometric notions for commutative [[Banach algebra]]s are interesting in the noncommutative case; among early enthusiasts one could mention [[Irving Segal]]; Semadeni's monograph on Banach spaces of continuous maps also predates the sudden expansion of the field in the late 1970s when [[Alain Connes]] ([web site](http://www.alainconnes.org/)) brought about a whole revolution in mathematics using the framework of noncommutative geometry based on [[operator algebra]]s, and boosted by the discovery of cyclic (co)homology by Connes and Boris Tsygan and its connection to [[K-theory]]. 

In [[ring theory]], there were many efforts at building [[spectrum (geometry)|spectra]] of noncommutative rings or [[abelian category|abelian categories]] (the spectrum of indecomposable injectives of Gabriel, the affine spectrum of P. M. Cohn
and so on) and stronger results in special cases like P. I. rings (polynomial identities rings) by M. Artin, F. van Oystaeyen and others in the 1970s. Golan and van Oystaeyen took noncommutative localization seriously in the mid 1970s with very promising results; [[Alexander Rosenberg|A. Rosenberg]] found in 1982 the so-called [[left spectrum]] of a noncommutative ring, straightforwardly later generalized to a spectrum of an [[abelian category]]. All these efforts belong to an early phase of [[noncommutative algebraic geometry]]. In the late 1980s, the study of [[derived categories]] of (quasi)coherent sheaves complemented that effort ([[Mikhail Kapranov|Kapranov]], Bondal, Orlov, ...). Though the effort was rather disconnected (from ring-theoretic mainstream noncommutative algebraic geometry) at the beginning, it can be now more easily judged as closely related; this is also the time of birth of the influential school of noncommutative [[projective geometry]] (Artin, Smith, Zhang, ...). 

The quantization program and the study of [[integrable systems]] brought about a number of interesting examples (in the early phase by G. Kac, Sklyanin, Fadeev, Drinfel'd, Woronowicz, Jimbo, [[Yuri Manin|Manin]], Reshetikin, Lusztig, Majid and others) with group-like flavour, the study of [[quantum groups]] which were studied in a number of formalisms from operator algebraic to algebro-geometric and purely categorical. [[action|Actions]] are very important in noncommutative geometry, and are some of the main examples in Connes' school like group(oid) $C^*$-algebras, crossed product operator algebras and the study of functions on orbifolds and foliations. They also play an important role in [[equivariant noncommutative algebraic geometry]]; cf. the central notions like [[Hopf–Galois extension]] and entwining structure. 

Noncommutative formal geometry, concerned with objects like infinitesimal neighborhoods of subvariaties, power series in noncommutative variables and so on, has been appearing more sporadically than the operator algebraic and algebro-geometric frameworks. Among pioneering works, there are [[Kontsevich]]'s (formal) noncommutative symplectic geometry (1992) and [[Kapranov's noncommutative geometry]] "based on commutator expansions". Noncommutative [[analytic geometry]] is even now only vaguely outlined in existing works. 

[[!redirects noncommutative geometries]]

[[!redirects non-commutative geometry]]
[[!redirects non-commutative geometries]]


[[!redirects noncommutative space]]
[[!redirects noncommutative spaces]]

[[!redirects non-commutative space]]
[[!redirects non-commutative spaces]]

[[!redirects Connes noncommutative geometry]]



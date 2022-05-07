
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *strict (2,1)-category* is a [[2-category]] which is both a *[[strict 2-category]]* as well as a [[(2,1)-category]], hence which is a [[Grpd]]-[[enriched category]], referred to as a *g.e. category* in original articles ([Fantham & Moore 1983](#FanthamMoore83)).

## Examples

\begin{example}\label{Homotopy2CategoryOfTopologicalSpaces}
**(homotopy 2-category of topological spaces)**
\linebreak
  There is a strict $(2,1)$-category whose underlying [[1-category]] is that of [[TopologicalSpaces]] and whose [[2-morphisms]] are the [[higher homotopy]]-classes of [[homotopies]] between [[continuous functions]].

If one restricts to topological spaces which admit the structure of [[CW-complexes]], then this is [[equivalence of 2-categories|equivalently]] the [[homotopy 2-category]] of the [[(infinity,1)-category|$(\infty,1)$-category]] of the [[simplicial localization]] of [[TopologicalSpaces]] at the [[weak homotopy equivalences]] ([[equivalence of (infinity,1)-categories|equivalently]] that of [[infinity-groupoids|$\infty$-groupoids]]), hence is the [[(2,1)-category]]-enhancement of the [[classical homotopy category]].

Since higher homotopy-classes of homotopies were also known as "tracks", some authors (following [Baues 1991, p. 300](#Baues91))
say "track category", not just for this example, but for $Grpd$-enriched categories generally.
\end{example}

## References
 {#References}

Original discussion of $Grpd$-enriched categories motivated from the [[homotopy 2-category]] of [[topological spaces]]:

* {#FanthamMoore83} [[Peter H. H. Fantham]], [[Eric J. Moore]], *Groupoid Enriched Categories and Homotopy Theory*, Canadian Journal of Mathematics **35** 3 (1983) 385-416 ([doi:10.4153/CJM-1983-022-8](https://doi.org/10.4153/CJM-1983-022-8))

In this context, some authors use the term "track category" for "$Grpd$-enriched category" (referring to their [[2-morphisms]], since "track" is a term for relative [[higher homotopy]]-classes of [[homotopies]]), following:

* {#Baues91} Chapter VI of: [[Hans-Joachim Baues]], *Combinatorial Homotopy and 4-Dimensional Complexes*, Expositions in Mathematics, De Gruyter 1991 ([doi:10.1515/9783110854480](https://doi.org/10.1515/9783110854480))

see also

* [[Klaus Heiner Kamps]], [[Tim Porter]], Sec. IV.1 of: _Abstract Homotopy and Simple Homotopy Theory_, World Scientific 1997 ([doi:10.1142/2215](https://doi.org/10.1142/2215), [GoogleBooks](http://books.google.de/books?id=7JYKxInRMdAC&dq=Porter+Kamps&printsec=frontcover&source=bl&ots=uuyl_tIjs4&sig=Lt8I92xQBZ4DNKVXD0x76WkcxCE&hl=de&sa=X&oi=book_result&resnum=3&ct=result#PPP1,M1))


For example, [[Toda brackets]] have a neat desciption in the [[homotopy 2-category]] of topological spaces regarded (Ex. \ref{Homotopy2CategoryOfTopologicalSpaces}) as a strict (2,1)-category (hence: "track category"):

* {#HardieKampsKieboom99} [[Keith Hardie]], [[Klaus Heiner Kamps]], [[Rudger  Kieboom]], _Higher homotopy groupoids and Toda brackets_, Homology Homotopy Appl. Volume 1, Number 1 (1999), 117-134 ([euclid:hha/1139840198](https://projecteuclid.org/euclid.hha/1139840198))

* {#HardieMarcumOda01} [[Keith Hardie]], [[Howard Marcum]], [[Nobuyuki Oda]], _Bracket operations in the homotopy theory of a 2-category_, Rend. Ist. Mat. Univ. Trieste 33, 19–70 (2001) ([rendiconti:33/02](https://rendiconti.dmi.units.it/volumi/33/02.pdf))

* {#HardieKampsMarcum02} [[Keith Hardie]], [[Klaus Heiner Kamps]], [[Howard Marcum]], _The Toda bracket in the homotopy category of a track bicategory_, Journal of Pure and Applied Algebra Volume 175, Issues 1–3, 8 November 2002, Pages 109-133 (<a href="https://doi.org/10.1016/S0022-4049(02)00131-7">doi:10.1016/S0022-4049(02)00131-7</a>)

* [[Howard Marcum]], [[Nobuyuki Oda]], _Long Box Bracket Operations in Homotopy Theory_, Appl Categor Struct 19, 137–173 ([doi:10.1007/s10485-009-9186-3](https://doi.org/10.1007/s10485-009-9186-3))



Often strict (2,1)-categories are discussed in the broader context of [[strict 2-categories]], i.e. [[Cat]]-[[enriched categories]], and not explicitly identified as the special case that they are, e.g. in:

* [[Susan B. Niefield]], [[Dorette A. Pronk]], *Internal groupoids and exponentiability*, Cahiers de topologie et géométrie différentielle catégoriques, [**LX** 4 (2019)](http://cahierstgdc.com/index.php/volume-lx/) ([pdf](http://cahierstgdc.com/wp-content/uploads/2019/10/Niefield-Pronk-LX-4.pdf))

  

[[!redirects strict (2,1)-categories]]

[[!redirects Grpd-enriched category]]
[[!redirects Grpd-enriched categories]]

[[!redirects g.e. category]]
[[!redirects g.e. categories]]

[[!redirects ge category]]
[[!redirects ge categories]]

[[!redirects ge-category]]
[[!redirects ge-categories]]

[[!redirects track category]]
[[!redirects track categories]]




+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Two [[polygons]] $P,P'$ in the [[Euclidean space|Euclidean plane]] have the same [[area]] iff they are __scissors congruent__ in the sense that they can be subdivided into _finitely_ many pieces such that the pieces of $P$ are congruent to the pieces of $P'$. 

__Hilbert's third problem__ (see _[[Hilbert's problems]]_) was to decide whether the analogue of this elementary fact holds for [[polyhedra]] in 3-[[dimension|dimensional]] space. Dehn solved this problem using what is now called the Dehn invariant. In modern language, it assigns to a polyhedron $P$ an element in $\mathbf{R}\otimes_{\mathbf{Z}} \mathbf{R}/\mathbf{Z}$. If both the Dehn invariant and volume of two (3-dimensional finite) polyhedra in Euclidean space are equal then they are scissors congruent. 

The __generalized Hilbert's third problem__  asks whether two finite $n$-[[polytopes]] in Euclidean, spherical or hyperbolic $n$-space must be scissors equivalent if they have the same volume and generalized invariants. 

The __scissors congruence group__  $\mathcal{P}(X,G)$ where $G$ is a subgroup of the group of isometries of $X$, is the free abelian group on symbols $[P]$, for all polytopes in $X$ modulo the relations

(i) $[P]-[P']-[P'']$ when $P = P'\coprod P''$,

(ii) $[g P]-[P]$.

In the book 

* J.L. Dupont, <a href="http://home.imf.au.dk/dupont/scissors.ps">Scissors congruences, group homology and characteristic classes (.ps) </a>, Lecture notes from Nankai Institute of Mathematics, 1998, Manuscript, University of Aarhus, Department of Math., Aarhus, 1999, 122 pp., and in: Nankai Tracts in Mathematics 1, World Scientific, Singapore, 2001. 

Dupont explains the relations of dilogarithms, Reidemeister torsion, Dehn invariant (which is from 1900) and their role in understanding the 19th century scissors congruence...The subject is very active now. After physicist Anatole Kirillov found the [[quantum dilogarithm]] and L. D. Fadeeev and Kashaev published a paper about it (and discovered the pentagon relation), this became an important topic in quantization (Fadeev's modular double, quantization of Teichmuller spaces, work of A. Fock, L. Takhdajan, Aldrovandi etc.) of hyperbolic spaces and generally the hyperbolic geometry and with relations, together with classical [[dilogarithm]] to many other subjects (e.g. to the work of Reznikov and theory or regulators, specially Borel regulator in higher algebraic K-theory, important for study of motives (Goncharov et al.) and, as W. Nahm shown, also relevant for understanding some phenomena in CFT).


## References

### Scissor congruence

* C. H. Sah, _Hilbert's third problem: scissors congruence_, Research Notes in Mathematics __33__, Pitman 1979.

* Inna Zakharevich, _Scissors congruence as K-theory_, [arxiv/1101.3833](http://arxiv.org/abs/1101.3833)

* J.-P. Sydler, _Conditions n&#233;cessaires et suffisantes pour l'&#233;quivalence des poly&#232;dres de l'espace euclidean &#224; trois dimensions_, Comment. Math. Helv. 40, 43-80, 1965. 

See also:

* Wikipedia, *[Hilbert's third problem](https://en.wikipedia.org/wiki/Hilbert%27s_third_problem)*

Via [[K-theory]]:

* [[Mona Merling]], [[Ming Ng]], [[Julia Semikina]], [[Alba Sendón Blanco]], [[Lucas Williams]]: *Scissors congruence K-theory for equivariant manifolds* &lbrack;[arXiv:2501.06928](https://arxiv.org/abs/2501.06928)&rbrack;


### Cut-and-paste of manifolds
 {#CutAndPasteOfManifolds}

Generalization to cut-and-paste of [[smooth manifolds]] (SK-groups, D: *Schneiden-und-Kleben Gruppen*):

* {#KarrasKreckNeumannOssa73} U. Karras, [[Matthias Kreck]], [[Walter D. Neumann]], E. Ossa, *Cutting and Pasting of Manifolds; SK-Groups*, Publish or Perish (1973) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/skbook.pdf), [[Karras-Kreck-Neumann-Ossa_CutNPaste.pdf:file]]&rbrack;

* [[Walter D. Neumann]], *Manifold cutting and pasting groups*, Topology **14** 3 (1975) 237-244 &lbrack;<a href="https://doi.org/10.1016/0040-9383(75)90004-X">doi:10.1016/0040-9383(75)90004-X</a>&rbrack;

Relation to [[TQFTs]]:

* [[Carmen Rovi]], Matthew Schoenbauer, *Relating Cut and Paste Invariants and TQFTs*, The Quarterly Journal of Mathematics **73** 2 (2022) 579–607 &lbrack;[arXiv:1803.02939](https://arxiv.org/abs/1803.02939), [doi:10.1093/qmath/haab044](https://doi.org/10.1093/qmath/haab044)&rbrack;

Survey:

* [[Carmen Rovi]], *Relating cut and paste invariants and TQFTS*, [talk](Center+for+Quantum+and+Topological+Systems#RoviArp2023) at [[CQTS]] (Apr. 2023) &lbrack;video: [YT](https://www.youtube.com/watch?v=lD8wQhwyrdg)&rbrack;

[[!redirects scissor congruences]]

[[!redirects Hilbert's third problem]]


[[!redirects cutting and pasting of manifolds]]
[[!redirects cut-and-paste of manifolds]]

[[!redirects SK-group]]
[[!redirects SK-groups]]

[[!redirects SK invariant]]
[[!redirects SK invariants]]

[[!redirects SK-invariant]]
[[!redirects SK-invariants]]

[[!redirects SKK invariant]]
[[!redirects SKK invariants]]

[[!redirects SKK-invariant]]
[[!redirects SKK-invariants]]




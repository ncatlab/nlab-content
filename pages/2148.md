The subject of [[cohomology]] with local coefficients ([[twisted cohomology]]) begins with [[Reidemeister]] in his study of lens spaces in 1938 in the article _Topologie der Polyeder und kombinatorischen Topologie der Komplexe_. He considered the cohomology of a polyhedron (there called a manifold -- such terminology hadn't yet settled down and so is probably best considered as a combinatorial manifold) $M$ in terms of cochains of the universal covering space $U$ together with the action of the fundamental group of $M$ as deck transformations. His terminology was _&#220;berdeckung_ (covering space). Interestingly, this approach underlies the [[crossed complex|crossed complexes]] studied extensively by Ronnie Brown, Phil Higgins and others in the past four decades.

+--{.query}
[[Zoran Škoda]] J. Nielsen, _&#220;ber die Minimalzahl der Fixpunkte bei den Abbildungstypen der Ringfl&#228;chen_, Math. Ann. __82__(1-2):83&#8211;93, 1920. is probably the reference responsible for so called Nielsen invariant. Nielsen invariant and Reidemeister torsion are rather related (there are many article now on this relation, for example by A. Felshtyn); there are also some precursors like dilogarithm functions from the end of 19th century, closely related to the subject. Finally the first article having homological algebra by Cayley from 1840-s is claimed by Gelfand-Kapranov-Zelevinsky to use at one point an invariant which is in the calculations with Koszul complexes the analogue of the Whitehead torsion, but I was not able to do the comparison. There is a book 

* J.L. Dupont, <a href="http://home.imf.au.dk/dupont/scissors.ps">Scissors congruences, group homology and characteristic classes (.ps) </a>, Lecture notes from Nankai Institute of Mathematics, 1998, Manuscript, University of Aarhus, Department of Math., Aarhus, 1999, 122 pp., and in: Nankai Tracts in Mathematics 1, World Scientific, Singapore, 2001. 

 which explains the relations of dilogarithms, [[Reidemeister torsion]], Dehn invariant (which is from 1900) and its role in understanding the 19th century scissors congruence...The subject is very active now. After physicist Anatole Kirillov found the [[quantum dilogarithm]] and L. D. Fadeeev and Kashaev published a paper about it (and discovered the pentagon relation), this became an important topic in quantization (Fadeev's modular double, quantization of Teichmuller spaces, work of A. Fock, L. Takhdajan, Aldrovandi etc.) of hyperbolic spaces and generally the hyperbolic geometry and with relations, together with classical [[dilogarithm]] to many other subjects (e.g. to the work of Reznikov and theory or regulators, specially Borel regulator in higher algebraic K-theory, important for study of motives (Goncharov et al.) and, as W. Nahm shown, also relevant for understanding some phenomena in CFT).
=--

[[Norman Steenrod|Steenrod]] in 1942 independently generalized the concept of ordinary cohomology to *cohomology with coefficients in a local system of groups*, later known as *cohomology with local coefficients*. In 1943, he acknowledged Reidemeister's precedence  showing that (after a suitable interpretation) the theory includes Reidemeister's concept of &#220;berdeckung.

In 1947, [[Eilenberg]] showed that the cohomology theory with a local system of groups is naturally equivalent to a theory of equivariants with respect to the [[deck transformation]]s of cohomology with ordinary coefficients on the corresponding universal [[covering space]].

In 1950, Olum extended Eilenberg's [[obstruction]] theory to the non-simple case, i.e. when the [[fundamental group]] acts non-trivially on the higher [[homotopy group]]s involved.

* _Obstructions to extensions and homotopies_, Annals 52 (1950) 1--52

In the 1960s and early 1970s, there were several papers addressing operations on cohomology with local coefficients:

* 1963, [[Sam Gitler]] (Steenrod mod $p$), _Cohomology operations with twisted coefficients_, AJM 85 (1963)156--188

* 1966, McClendon, thesis -- summarized in

* 1967, Emery Thomas, tc ops

* 1967, Larmore, tc ops

* 1969, McClendon, _Higher order twisted cohomology operations_, Invent. Math. 7 (1969) 183--214

* 1969, Larmore, tc

* 1970, Peterson, tc ops

* 1971, McClendon, tc ops

In 1972, the phrase _twisted cohomology_ was  used by Larmore to describe 
$H(-; \mathcal{E})$, cohomology with coefficients in a special kind of [[spectrum]] $\mathcal{E}$  related to a [[fibration]] $p:E\to B.$ The result is what May and Sigurdsson call a parameterized spectrum,
the _parameters_ being the points of $B$, which might also be called, in the older topological terminology, an _ex-spectrum_.

In recent years, especially after  the invention of [[twisted K-theory]], 'twisted cohomology' has become the generic term, including not only twisted [[Whitehead-generalized cohomology]] but even what is known as twisted _[[nonabelian cohomology|non-abelian]]_ cohomology. Among other things, non-abelian refers to the fact 
that no spectrum need be involved, but only a single target space, preferably at least a [[loop space]].

Also in 1972 Robinson constructed Moore--[[Postnikov system]]s for non-simple fibrations. In particular, he
provided twisted $K(\pi,n)$s corresponding to cohomology with local coefficients.

##Comments## 

It is useful to show that  the work of Reidemeister was extended in another way by [[J.H.C. Whitehead]] in his paper [CHII] referenced below. [[Graham Ellis]] writes in his paper (E) as follows: 

.... J.H.C. Whitehead showed in
(CHII)  that, for connected $CW$-complexes $X, Y$ with
dim $X \leq n$ and $\pi_i Y = 0$ for $2\leq i \leq  n - 1$, the
homotopy classification of maps $X \to  Y$ can be reduced to a
purely algebraic problem of classifying, up to an appropriate
notion of homotopy, the $\pi_1$-equivariant chain homomorphisms $C_*
\widetilde{X} \to  C_* \widetilde{Y}$ between the cellular chain complexes of the
universal  covers. The classification of homotopy equivalences $Y
\simeq Y$ can similarly be reduced to a purely algebraic problem.
Moreover, the algebra of the cellular chains of the universal
covers closely reflects the topology, and provides pleasant and
interesting exercises.

These results ought to be a standard piece of elementary algebraic
topology. Yet, perhaps because of the somewhat esoteric exposition given in (CHII), and perhaps because of a lack of
worked examples, they have remained largely ignored. The purpose
of the present paper is to rectify this situation.  We shall show
the utility of Whitehead's results by using them to give new and
clearer treatments of various known classifications.

In fact this work includes that of Olum referenced above. 

(End of quote)

Whitehead introduced what he called _homotopy systems_ which we now call free, reduced [[crossed complex]]es, and these were a major tool in his work. He related these to chain complexes with a group of operators, and, for CW-complexes, to the chains of the universal cover. 

However Whitehead remarks that the homotopy systems have better realisation properties than the chain complexes with operators, and this we can now see is reflected in the classifying space $BC$ of a crossed complex $C$ defined in (BH). By choosing the crossed complex $C$ to be a group $G$ in dimension 1 and a $G$-module $A$ in dimension $n$ we easily get the classifying space for local coefficients defined by various authors. This is discussed in more generality in Section 7 of (BH). 
 
##References##

* (E) [[G.J.Ellis]],  Homotopy classification the J.H.C. Whitehead way.
_Exposition. Math._ 6 (1988) 97--110.


* (BH) Brown, R. and Higgins, P.J.
The classifying space of a crossed complex.
_Math. Proc. Cambridge Philos. Soc._ 110 (1991)
  95--120.

* (CHII) Whitehead, J. H.C.
Combinatorial homotopy. II.
_Bull. Amer. Math. Soc._ 55 (1949) 453--496.

[[!redirects History of cohomology with local coefficients]]
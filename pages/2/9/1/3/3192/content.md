
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}


## Definition


\begin{definition}\label{FredholmOperator}
A [[continuous function|continuous]] [[linear operator]] $F \colon B_1\to B_2$ between [[Banach spaces]] is **Fredholm** if it has [[finite set|finite]] [[dimension|dimensional]] [[kernel]] and finite dimensional [[cokernel]]. 
\end{definition}


\begin{definition}\label{FredholmIndex}
The difference between the [[dimension of a vector space|dimensions]] of the kernel and the cokernel of a Fredholm operator $F$ is called its *[[index]]* (the *[[Fredholm index]]*) 

$$
  ind F \coloneqq dim (ker F) - dim (coker F) = dim (ker F) - codim (im F)
  \,.
$$

\end{definition}

An equivalent characterization of Fredholm operators is the following:

\begin{definition}\label{Parametrix}
A **parametrix** of a [[bounded operator|bounded]] [[linear operator]] $F \colon \mathcal{H}_1 \to \mathcal{H}_2$ is a reverse operator $P \colon \mathcal{H}_2 \to \mathcal{H}_1$ which is an "[[inverse]] up to [[compact operators]]", i.e. such that $F \circ P - id_{\mathcal{H}_2}$ and $P \circ F - id_{\mathcal{H}_1}$ are both [[compact operators]].
\end{definition}

\begin{proposition}\label{FredholmViaParametrix}
**([[Atkinson's theorem]])**
\linebreak
A [[bounded operator|bounded]] [[linear operator]] $ F \colon B_1\to B_2$ between [[Banach spaces]] is Fredholm, def. \ref{FredholmOperator} precisely it is has a parametrix, def. \ref{Parametrix}.
\end{proposition}


## Examples

* [[elliptic operator|Elliptic operators]] on [[compact topological space|compact]] [[manifolds]] are naturally Fredholm, when understood between the appropriate [[Sobolev spaces]].

* [charged vacua of free Dirac field in Coulomb background](Dirac+field#FreeDiracFieldInCoulombBackground) are characterized by Fredholm operators



## Properties


### General 

+-- {: .num_prop }
###### Proposition

The [[image]] (range) of a Fredholm operator is closed. 

=--

+-- {: .num_prop }
###### Proposition

The [[subspace]] $Fred(B_1,B_2)\subset B(B_1,B_2)$ of Fredholm operators in the space of bounded linear operators with the [[norm topology]] is [[open subset|open]]. 

=--

  In other words, given a Fredholm operator $F$, there exists $\epsilon\gt 0$ such that every bounded linear operator $G$ satisfying $\| G-F\|\lt \epsilon$ is Fredholm. Fredholm operators on a fixed separable Hilbert space $H = B_1 = B_2$ form a [[semigroup]] with respect to the composition and the index is a [homomorphism]] of semigroups: $ind F G = ind F + ind G$. 


### Relation to topological K-theory

\begin{proposition}
**([[Atiyah-Jänich theorem]])**
\linebreak
The space of [[Fredholm operators]] $Fred(\mathscr{H})$ on a (countably infinite-dimensional, [[separable Hilbert space|separable]], [[complex vector space|complex]]) [[Hilbert space]] $\mathscr{H}$ is a [[classifying space]] for [[topological K-theory]] $K(-)$:

For $X$ a [[compact Hausdorff space]], the [[homotopy classes]] of [[continuous maps]] from $X$ to $Fred(\mathscr{H})$ are in [[natural bijection]] with $K(X)$

$$
  \pi_0 \, 
  Map\big(
    X,
    \,
    Fred(\mathscr{H})
  \big)
  \xrightarrow[\sim]{ind_X}
  K(X)
  \,,
$$

where $ind_X$ is an $X$-parameterized enhancement of the [[Fredholm index]].
\end{proposition}


{#VariantsForTwistedKTheory}Several variants of the ordinary space of Fredholm operators retain the same [[homotopy type]] and hence all serves as [[classifying spaces]] for [[topological K-theory]], but differ in further properties they have, cf. [Atiyah & Segal 2004 §3](#AtiyahSegal04).

A definition which makes a good classifying space also for [[twisted K-theory]] and [[equivariant K-theory]] is the following:

\begin{definition}\label{FredZero}
  Given any [[cyclic group of order 2|$C_2$]]-[[graded vector space|graded]] infinite-dimensional ([[separable Hilbert space|separable]] [[complex vector space|complex]]) [[Hilbert space]] $\mathscr{H} \simeq \mathscr{H}_+ \oplus \mathscr{H}_i$, 
write $Fred^{(0)}(\mathscr{H})$ for the set of [[bounded linear operators]] $F \,\colon\, \mathscr{H} \to \mathscr{H}$ which are

1. [[self-adjoint operator|self-adjoint]]: $F^\dagger = F$

1. odd-graded: $F(\mathscr{H}_{\pm}) \subset \mathscr{H}_{\mp}$,

1. idempotent up to [[compact operators]]: $F^2 - Id \,\in\, \mathcal{K}(\mathscr{H})$,

equipped with the [[topological space|topology]] of the [[topological subspace]], via

$$
  F \,\mapsto\, \big(F ,\, F^2 - id\big)
  \,,
$$

of the [[product space]] of the spaces of 

1. [[bounded linear operators]], $\mathcal{B}$, equipped with the [[compact-open topology]] and 

1. [[compact operators]], $\mathcal{K}$, equipped with the [[norm topology]]:

\begin{imagefromfile}
    "file_name": "Fred0.png",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}


\end{definition}
(This is due to [Atiyah & Segal 2004 Def. 3.2](#AtiyahSegal04), following [Atiyah & Singer 1969 p 7](#AtiyahSinger69), see also [Freed, Hopkins & Teleman 2011 Def. A.39](#FreedHopkinsTeleman11).)

\begin{remark}
  In view of Def. \ref{Parametrix} and Prop. \ref{FredholmViaParametrix}, the condition $F^2 - id \in \mathcal{K}$ in Def. \ref{FredZero} asserts that $F$ not just has a [[parametrix]], but is its *own* parametrix. Or rather, together with the condition that $F$ is odd, hence $F = F_+ + F_-$ with $F_\pm \colon \mathscr{H}_{\pm} \to \mathscr{H}_{\mp}$, it says that $F_+$ and $F_-$ are parametrices of each other. 

Indeed the Fredholm index map on $Fred^{(0)}(\mathscr{H})$ assigns the Fredholm index (Def. \ref{FredholmIndex}) of one of these components (say $F_+$). (This follows by tracing through the equivalences indicated in [AS04 §3](#AtiyahSegal04).)

Finally, together with the grading, the condition $F^\ast = F$ implies that in fact $F_\pm = (F_\mp)^\ast$, whence the index is actually just (the dimension of) the [[kernel]] of $F$, but regarded as (the dimension of) a [[virtual vector bundle|virtual vector space]].
\end{remark}

\linebreak


## Generalizations

Fredholm operators generalize to Fredholm complexes. A finite [[chain complex]]

$$
0 \to C_0 \stackrel{d_0}\to C_1\stackrel{d_1}\to C_2 \ldots C_n\to 0
$$

of [[Banach spaces]] and bounded operators is said to be a **Fredholm complex** if the images $d_i$ are closed and the [[chain homology]] of the complex is finite dimensional. The [[Euler characteristic]] (the alternative sum of the dimensions of the homology groups) is then called the __index__ of the Fredholm complex. Each Fredholm operator can be considered as a Fredholm complex concentrated at zero. Each Fredholm complex produces a Fredholm operator from the sum of the even- to the sum of the odd-numbered spaces in the complex. 

One can consider *Fredholm almost complexes*, where $d_i \circ d_{i-1}$ is not zero but the image of that operator is compact. Out of every Fredholm almost complex one can make a complex by correcting the differentials by compact perturbation terms. [[elliptic complex|Elliptic complexes]] give examples of Fredholm complexes. 


## Related concepts


* [[Fredholm module]], 

* [[Fredholm determinant]], 

* [[Dirac operator]], 

* [[Toeplitz operator]]

* [[K-theory]], [[KK-theory]]

* [[index theory]] 



## References

Textbook accounts:

* [[William Arveson]], §3.3 of: *A Short Course on Spectral Theory*, Graduate Texts in Mathematics **209**, Springer (2002) &lbrack;[doi:10.1007/b97227](https://link.springer.com/book/10.1007/b97227)&rbrack;

Review:

* [[Martin Schechter]]: *Basic theory of Fredholm operators*, Annali della Scuola Normale Superiore di Pisa - Scienze Fisiche e Matematiche, Serie 3, **21** 2 (1967) 261-280 &lbrack;[numdam:ASNSP_1967_3_21_2_261_0](https://www.numdam.org/item/ASNSP_1967_3_21_2_261_0)&rbrack;

Discussion of the space of Fredholm operators as a [[classifying space]] for [[topological K-theory]]:

* {#Atiyah67}  [[Michael Atiyah]], Appendix of: _K-theory_, Harvard Lecture 1964 (notes by D. W. Anderson), Benjamin (1967) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahk.pdf), [[AtiyahKTheory.pdf:file]]&rbrack;

and variants that serve as classifying spaces also for [[twisted K-theory]] and [[equivariant K-theory]]:

* {#AtiyahSinger69} [[Michael Atiyah]], [[Isadore Singer]]: *Index theory for skew-adjoint Fredholm operators*,  Publications Mathématiques de l’Institut des Hautes Scientifiques **37** 1 (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [pdf](http://www.maths.ed.ac.uk/~aar/papers/askew.pdf)&rbrack;

* {#AtiyahSegal04} [[Michael Atiyah]], [[Graeme Segal]], §3 in: _Twisted K-theory_, Ukrainian Math. Bull. **1** 3 (2004) &lbrack;[arXiv:math/0407054](http://arxiv.org/abs/math/0407054), [journal page](http://iamm.su/en/journals/j879/?VID=10), [published pdf](http://iamm.su/upload/iblock/45e/t1-n3-287-330.pdf)&rbrack;

* {#FreedHopkinsTeleman11} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], §A.5 in: *[[Loop Groups and Twisted K-Theory]] I*, J. Topology **4 (2011) 737-789  &lbrack;[arXiv:0711.1906](http://arxiv.org/abs/0711.1906), [doi:10.1112/jtopol/jtr019](https://doi.org/10.1112/jtopol/jtr019)&rbrack;



See also:

* Wikipedia, *[Fredholm operator](http://en.wikipedia.org/wiki/Fredholm_operator)*

* A. S. Mishchenko, &#1042;&#1077;&#1082;&#1090;&#1086;&#1088;&#1085;&#1099;&#1077; &#1088;&#1072;&#1089;&#1089;&#1083;&#1086;&#1077;&#1085;&#1080;&#1103; &#1080; &#1080;&#1093; &#1087;&#1088;&#1080;&#1084;&#1077;&#1085;&#1077;&#1085;&#1080;&#1103; (Vector bundles and their applications), Nauka, Moscow, 1984. 208 pp. MR87f:55010  

* S. Rempel, B-W. Schulze, _Index theory of elliptic boundary problems_, Akademie--Verlag, Berlin, 1982.

* [[Lars Hörmander]], _The analysis of linear partial differential operators. III. Pseudo-differential operators_, 1994, reprinted 2007. 

* Pietro Aiena, _Fredholm and local spectral theory, with applications to multipliers_, [book page](http://www.springer.com/mathematics/analysis/book/978-1-4020-1830-5)

* [[Otgonbayar Uuye]], _A simple proof of the Fredholm Alternative_, [arxiv/1011.2933](http://arxiv.org/abs/1011.2933)

* [[Alexander Grothendieck]], _La th&#233;orie de Fredholm_, Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __84__ (1956), p. 319-384, [numdam](http://www.numdam.org/item?id=BSMF_1956__84__319_0) 

* Marina Prokhorova, _Spectral Sections_, [arXiv:2008.04672](https://arxiv.org/abs/2008.04672).

* Marina Prokhorova, _Spaces of unbounded Fredholm operators. I. Homotopy equivalences_, [arXiv:2110.14359](https://arxiv.org/abs/2110.14359).

* Marina Prokhorova, _The continuity properties of discrete-spectrum families of Fredholm operators_, [arXiv:2201.09869](https://arxiv.org/abs/2201.09869).

* Marina Prokhorova, _From graph to Riesz continuity_, [arXiv:2202.03337](https://arxiv.org/abs/2202.03337).

For Fredholm complexes, see

* [[Graeme Segal]], _Fredholm complexes_, Quarterly Journal of Mathematics 21:4 (1970), 385–402.  [doi](http://dx.doi.org/10.1093/qmath/21.4.385).


category: analysis

[[!redirects Fredholm complex]]
[[!redirects Fredholm operators]]
[[!redirects parametrix]]


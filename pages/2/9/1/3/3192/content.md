
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
A [[bounded linear operator|bounded]] [[linear operator]] $F \colon B_1\to B_2$ between [[Banach spaces]] is **Fredholm** if it has [[finite set|finite]] [[dimension|dimensional]] [[kernel]] and finite dimensional [[cokernel]]. 
\end{definition}
(e.g. [Murphy 1990 p. 23](#Murphy90))

\begin{remark}
  Some (older) text may also require that the [[image]] of $F$ be [[closed subspace|closed]], but that is in fact implied by the cokernel of $F$ having finite dimension (cf. Prop. \ref{ImageIsClosed} below).
Moreover, some (older) texts do not require $F$ to be bounded, but just ask that it be [[closed operator|closed]] with [[dense subset|dense]] [[domain]] of definition (e.g. [Schechter 1967 §1](#Schechter1967)). 
\end{remark}

\begin{definition}\label{FredholmIndex}
The difference between the [[dimension of a vector space|dimensions]] of the kernel and the cokernel of a Fredholm operator $F$ is called its *[[index]]* (the *[[Fredholm index]]*) 

$$
  \begin{array}{ccl}
  ind F 
    &\coloneqq&
  dim (ker F) - dim (coker F) 
  \\
    &=&
  dim (ker F) - codim (im F)
  \mathrlap{\,.}
  \end{array}
$$

\end{definition}



## Examples

* [[elliptic operator|Elliptic operators]] on [[compact topological space|compact]] [[manifolds]] are naturally Fredholm, when understood between the appropriate [[Sobolev spaces]].

* [charged vacua of free Dirac field in Coulomb background](Dirac+field#FreeDiracFieldInCoulombBackground) are characterized by Fredholm operators



## Properties


### General 

\begin{proposition}\label{ImageIsClosed}
The [[image]] (range) of a Fredholm operator is [[closed subspace|closed]]. 
\end{proposition}
(cf. [Atiyah 1967 p. 153-4](#Atiyah67), [Murphy 1990 Thm. 1.4.7](#Murphy90))


\begin{proposition}\label{SubspaceOfFredholmInNormTopology}
The [[topological subspace]] $Fred(B_1,B_2)\subset B(B_1,B_2)$ of Fredholm operators (in the space of [[bounded linear operators]] equipped with the [[norm topology]]) is [[open subset|open]]. 

On this subspace with its [[subspace topology]], the Fredholm index (Def. \ref{FredholmIndex}) is a [[continuous map]].
\end{proposition}
([Murphy 1990 Thm. 1.4.17](#Murphy90))

\begin{remark}
In other words, Prop. \ref{SubspaceOfFredholmInNormTopology} says that given a Fredholm operator $F$ then there exists a [[real number]] $\epsilon \gt 0$ such that every [[bounded linear operator]] $G$ with [[operator norm]] ${\Vert G - F \Vert} \lt \epsilon$ is itself Fredholm of the same index.
\end{remark}


\begin{proposition}\label{ClosureUnderComposition}
For [[Banach spaces]] $B_1$, $B_2$, $B_3$ and Fredholm operators $F_1 \colon B_1 \longrightarrow B_2$ and $F_2 \colon B_2 \longrightarrow B_3$ 

1. the [[composition|composite]] $F_2 \,\circ\, F_1 \colon B_1 \longrightarrow B_3$ is Fredholm

1. with index (Def. \ref{FredholmIndex}) the sum of the indices of the factors:

   $$
     ind(F_2\circ F_1) 
       \;=\;
     ind(F_1) + ind(F_2)
     \,.
   $$

\end{proposition}
([Murphy 1990 Thm. 1.4.8](#Murphy90))

\begin{remark}
In other words, Prop. \ref{ClosureUnderComposition} says that Banach spaces with Fredholm operators between them form a [[category]] on which the Fredholm index is a [[functor]] to the [[delooping groupoid]] of the [[integers]]; hence the [[endomorphism|endomorphic]] Fredholm operators $F \colon B \longrightarrow B$ form a [[monoid]] with the Fredholm index being a [[homomorphism]] of monoids.
\end{remark}


### Via parametrices
 {#ViaParametrices}


An equivalent characterization of Fredholm operators is the following:

\begin{definition}\label{Parametrix}
A **parametrix** of a [[bounded operator|bounded]] [[linear operator]] $F \colon \mathcal{H}_1 \to \mathcal{H}_2$ is a reverse bounded operator $P \colon \mathcal{H}_2 \to \mathcal{H}_1$ which is an "[[inverse]] up to [[compact operators]]", i.e. such that $F \circ P - id_{\mathcal{H}_2}$ and $P \circ F - id_{\mathcal{H}_1}$ are both [[compact operators]].
\end{definition}

\begin{proposition}\label{FredholmViaParametrix}
**([[Atkinson's theorem]])**
\linebreak
A [[bounded operator|bounded]] [[linear operator]] $ F \colon B_1\to B_2$ between [[Banach spaces]] is Fredholm, def. \ref{FredholmOperator}, precisely if it admits a parametrix, def. \ref{Parametrix}.
\end{proposition}
(cf. [Murphy 1990 Thm. 1.4.16](#Murphy90))



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

### Self-adjoint Fredholm operators
 {#PropertiesSelfAdjointFredholmOperators}

The following is a digest of [Booß-Bavnbek & Wojciechowski 1993](#BooßBavnbekWojciechowski1993).

All [[linear operators]] in the following act on a given [[separable Hilbert space|separable]] countably infinite-dimensional [[complex numbers|complex]] [[Hilbert space]].

Consider and denote:

* $\mathcal{B}$ --- the space of [[bounded operators]],

* $\mathcal{K} \subset \mathcal{B}$ --- the subspace of [[compact operators]],

* $\mathcal{C} \coloneqq \mathcal{B}/\mathcal{K}$  --- the [[Calkin algebra]] regarded as a [[C*-algebra|$C^\ast$-algebra]],

* $\mathbf{p} \colon \mathcal{B} \twoheadrightarrow \mathcal{C}$  --- the [[quotient]] [[coprojection]],

* $\mathcal{G} \coloneqq \mathcal{C}^\times = GL(\mathcal{C})$  --- the [[group of units]] of the [[Calkin algebra]],

* $\widehat{\mathcal{G}} \subset \mathcal{G}$  --- the subgroup of [[self-adjoint elements]],

* $\widehat{\mathcal{G}}_{\pm} \subset \widehat{\mathcal{G}}$   --- the subgroup of elements with purely positibe/negative [[essential spectrum]], 

* $\widehat{\mathcal{G}}_{\ast} \subset \widehat{\mathcal{G}}$   --- the remaining subspace, of elements whose essential spectrum is both positive and negative,

* $G \coloneqq \mathrm{U}(\mathcal{C}) \subset GL(\mathcal{C})$ --- the [[unitary group]] of the Calkin algebra, 

* $\widehat{G} \coloneqq \widehat{\mathcal{G}} \cap G$ --- the group of self-adjoint unitary elements of the Calkin algebra

* $\widehat{G}_{\pm} \coloneqq \widehat{\mathcal{G}}_{\pm} \cap G$ --- the group of self-adjoint unitary elements of the Calkin algebra with purely positive/negative essential spectrum,

* $\widehat{G}_{\ast} \coloneqq \widehat{\mathcal{G}}_{\ast} \cap G$ --- the group of self-adjoint unitary elements of the Calkin algebra with both positive and negative essential spectrum,

* $\mathcal{F} \simeq \mathbf{p}^{-1}(\mathcal{G})$  --- the space of [[Fredholm operators]],

* $\widehat{\mathcal{F}} \subset \mathcal{F}$  --- the subspace of self-adjoint Fredholm operators,

* $\widehat{\mathcal{F}}_{\pm} \subset \widehat{\mathcal{F}}$  --- the subspace of operators with purely positive/negative [[essential spectrum]],
  
* $\widehat{\mathcal{F}}_{\ast} \subset \widehat{\mathcal{F}}$  --- the remaining subspace, that of operators with both positive and negative [[essential spectrum]],


\begin{proposition}

We have [[homeomorphisms]]:

\[
  \begin{aligned}
     \widehat{\mathcal{G}} 
     & \;\simeq\; 
     \widehat{\mathcal{G}}_+ 
       \sqcup 
     \widehat{\mathcal{G}}_- 
       \sqcup 
     \widehat{\mathcal{G}}_\ast
     \\
     \widehat{\mathcal{F}} 
     & \;\simeq\; 
     \widehat{\mathcal{F}}_+ 
       \sqcup 
     \widehat{\mathcal{F}}_- 
       \sqcup 
     \widehat{\mathcal{F}}_\ast
     \\
     \widehat{G}_\pm 
     & \;\simeq\; 
     \{ \pm id \}
     \\
     \widehat{G}_\ast
     & \;\simeq\; 
     \big\{
       g \in \mathcal{C}
       \;\Big\vert\;
       g^\ast = g
       ,\;
       g^2 = id
       ,\;
       g \neq \pm id
     \big\}
     \\
     & \;\simeq\; 
     \big\{
       g \in \mathcal{C}
       \;\Big\vert\;
       g^\ast = g
       ,\;
       spec(g) = \{+1, -1\}
     \big\}
     \\
     & \;\simeq\;
     \underset{
       Gr(\mathcal{C})
     }{
     \underbrace{
       \big\{ 
          p \in \mathcal{C} 
       \,\big\vert\, 
          p^2 = p = p^\ast \neq 0, id 
       \big\} 
     }}
  \end{aligned}
\]

and [[homotopy equivalences]]:

\[
  \begin{aligned}
    \widehat{\mathcal{G}}_{\pm} 
     & \;\sim\; 
    \widehat{G}_{\pm} \;\sim\; \ast
    \\
    \widehat{\mathcal{F}}_{\pm} 
    & \;\sim\; 
    \mathbf{p}^{-1}\big(\widehat{\mathcal{G}}_{\pm}\big)
      \;\sim\; 
      \ast
    \\
    \widehat{\mathcal{F}}_{\ast} 
    & \;\sim\; 
    \mathbf{p}^{-1}\big(\widehat{\mathcal{G}}_{\ast}\big)
    \\
    \mathbf{p} 
      \;\colon\; 
    \widehat{\mathcal{F}}_\ast 
     & \;\sim\; 
    \widehat{\mathcal{G}}_\ast  
       \;\sim\;
    \widehat{G}_\ast  
  \end{aligned}
\]

For $j_0 \in \widehat{G}_\ast$ any [[base point]], the [[conjugation action]] map

$$
  \begin{array}{c}
     G 
     &\overset{}{\longrightarrow}&
     \widehat{G}_\ast
     \\
     u &\mapsto& u \circ j_0 \circ u^{-1}
  \end{array}
$$

is a [[fiber bundle]] (in fact a [[principal bundle]]) with [[typical fiber]] $G \times G$.

\end{proposition}

([Booß-Bavnbek & Wojciechowski 1993](#BooßBavnbekWojciechowski1993), following [Atiyah & Singer 1969](#AtiyahSinger69))

\begin{proposition}
  The [[exponential map]]
  $$
    \exp\big(\pi \mathrm{i} (-) \big)
    \;\colon\;
    \widehat{\mathcal{F}}_\ast
    \longrightarrow
    \Big\{
      U \in \mathrm{U}(\mathscr{H})
      \,\Big\vert\,
      U + id \in \mathcal{K}(\mathscr{H})
    \Big\}
  $$
  (to the *Fredholm unitary group*) is a [[homotopy equivalence]].
\end{proposition}
([Atiyah & Singer 1969 Prop. 3.3](#AtiyahSinger69))


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

* [[topological K-theory]], [[KK-theory]]

* [[Atiyah-Jänich theorem]]

* [[index theory]] 



## References
 {#References}

### General

The concept of Fredholm operators originates with and is named after:

* [[Ivar Fredholm]]: *Sur une classe d’équations fonctionnelles*,  Acta Math. **27** (1903) &lbrack;[doi:10.1007/BF02421317](https://doi.org/10.1007/BF02421317), [euclid:10.1007/BF02421317](https://projecteuclid.org/journals/acta-mathematica/volume-27/issue-none/Sur-une-classe-d%C3%A9quations-fonctionnelles/10.1007/BF02421317.full)&rbrack;


Textbook accounts:

* Ronald G. Douglas: *Compact Operators, Fredholm Operators, and Index Theory*, chapter 5 in *Banach Algebra Techniques in Operator Theory*, Pure and Applied Mathematics **49** (1972) 121-148 \[<a href="https://doi.org/10.1016/S0079-8169(08)60364-5">doi:10.1016/S0079-8169(08)60364-5</a>\]

* {#Murphy90} [[Gerard Murphy]]: §1.4 in: *$C^\ast$-algebras and Operator Theory*, Academic Press (1990) &lbrack;[doi:10.1016/C2009-0-22289-6](https://doi.org/10.1016/C2009-0-22289-6)&rbrack;

* [[William Arveson]], §3.3 of: *A Short Course on Spectral Theory*, Graduate Texts in Mathematics **209**, Springer (2002) &lbrack;[doi:10.1007/b97227](https://link.springer.com/book/10.1007/b97227)&rbrack;

* Nora Doll, [[Hermann Schulz-Baldes]], [[Nils Waterstraat]]: *Bounded Fredholm Operators*, Chapter 3 in: *Spectral Flow --- A Functional Analytic and Index-Theoretic Approach*, Studies in Mathematics **94**, De Gruyter (2023) &lbrack;[doi:10.1515/9783111172477](https://doi.org/10.1515/9783111172477)&rbrack;

Review:

* {#Schechter1965} [[Martin Schechter]]: *Fredholm Operators and the Essential Spectrum*, New York University Courant Institute (1965) &lbrack;[pdf](https://ia801803.us.archive.org/17/items/fredholmoperator00sche/fredholmoperator00sche.pdf)&rbrack;
  > (focus on their [[essential spectrum]])

* {#Schechter1967} [[Martin Schechter]]: *Basic theory of Fredholm operators*, Annali della Scuola Normale Superiore di Pisa - Scienze Fisiche e Matematiche, Serie 3, **21** 2 (1967) 261-280 &lbrack;[numdam:ASNSP_1967_3_21_2_261_0](https://www.numdam.org/item/ASNSP_1967_3_21_2_261_0)&rbrack;

* {#Jaffe} Ethan Y. Jaffe: *Atkinson’s Theorem* &lbrack;[pdf](https://r-grande.github.io/Expository/Atkinson%27s%20Theorem.pdf)&rbrack;
  > (focus on [[Atkinson's theorem]])



Discussion of the space of Fredholm operators as a [[classifying space]] for [[topological K-theory]]:

* {#Atiyah67}  [[Michael Atiyah]], Appendix of: _K-theory_, Harvard Lecture 1964 (notes by D. W. Anderson), Benjamin (1967) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahk.pdf), [[AtiyahKTheory.pdf:file]]&rbrack;

and variants that serve as classifying spaces also for [[twisted K-theory]] and [[equivariant K-theory]]:

* {#AtiyahSinger69} [[Michael Atiyah]], [[Isadore Singer]]: *Index theory for skew-adjoint Fredholm operators*,  Publications Mathématiques de l’Institut des Hautes Scientifiques **37** 1 (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [pdf](http://www.maths.ed.ac.uk/~aar/papers/askew.pdf)&rbrack;

* {#AtiyahSegal04} [[Michael Atiyah]], [[Graeme Segal]], §3 in: _Twisted K-theory_, Ukrainian Math. Bull. **1** 3 (2004) &lbrack;[arXiv:math/0407054](http://arxiv.org/abs/math/0407054), [journal page](http://iamm.su/en/journals/j879/?VID=10), [published pdf](http://iamm.su/upload/iblock/45e/t1-n3-287-330.pdf)&rbrack;

* {#FreedHopkinsTeleman11} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], §A.5 in: *[[Loop Groups and Twisted K-Theory]] I*, J. Topology **4** (2011) 737-789  &lbrack;[arXiv:0711.1906](http://arxiv.org/abs/0711.1906), [doi:10.1112/jtopol/jtr019](https://doi.org/10.1112/jtopol/jtr019)&rbrack;



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

On Fredholm complexes:

* [[Graeme Segal]], _Fredholm complexes_, Quarterly Journal of Mathematics 21:4 (1970), 385–402.  [doi](http://dx.doi.org/10.1093/qmath/21.4.385).

### Self-adjoint

On (the space of) [[self-adjoint operators|self-adjoint]] Fredholm operators:

* Nora Doll, [[Hermann Schulz-Baldes]], [[Nils Waterstraat]]:  *Bounded Self-Adjoint Fredholm Operators*, Section 3.6 in: *Spectral Flow --- A Functional Analytic and Index-Theoretic Approach*, Studies in Mathematics **94**, De Gruyter (2023) &lbrack;[doi:10.1515/9783111172477](https://doi.org/10.1515/9783111172477)&rbrack;


As a [[classifying space]] for [[topological K-theory]] $KU^1$, $KO^1$ and $KSp^1$ (see at *[[Atiyah-Jänich theorem]]*):

* {#AtiyahSinger1969} [[Michael F. Atiyah]], [[Isadore M. Singer]]: *Index theory for skew-adjoint Fredholm operators*, Publications Mathématiques de l'IHÉS **37** (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [numdam:PMIHES_1969__37__5_0](https://www.numdam.org/item/PMIHES_1969__37__5_0), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/askew.pdf)&rbrack;

* {#Karoubi1970} [[Max Karoubi]]: *Espaces Classifiants en K-Théorie*, Trans. Amer. Math. Soc. **147** (1970) 75-115 &lbrack;[doi:10.2307/1995218](https://doi.org/10.2307/1995218), [jstor:1995218](https://www.jstor.org/stable/1995218), Engl. transl: [[Karoubi-EspacesClassifiants-English-251105.pdf:file]]&rbrack;
 
More on the [[homotopy groups]] of this space:

* {#BooßBavnbekWojciechowski1993} [[Bernhelm Booß-Bavnbek]], Krzysztof P. Wojciechowski: *The Homotopy Groups of the Space of Self-Adjoint Fredholm Operators*, §16 in: *Elliptic Boundary Problems for Dirac Operators* Mathematics: Theory & Applications, Birkhäuser (1993) 127-137  &lbrack;[doi:10.1007/978-1-4612-0337-7_16](https://doi.org/10.1007/978-1-4612-0337-7_16), [pdf](https://link.springer.com/content/pdf/10.1007/978-1-4612-0337-7_16)&rbrack;

Specifically regarding their [[spectral flow]]:

* [[Michael F. Atiyah]], [[Vijay K. Patodi]], [[Isadore M. Singer]]: *Spectral asymmetry and Riemannian Geometry. I*, Mathematical Proceedings of the Cambridge Philosophical Society **77** 1 (1975) 43-69 &lbrack;[doi:10.1017/S0305004100049410](https://doi.org/10.1017/S0305004100049410)&rbrack; 
  > (original mentioning, on p. 47-48, in the context of introducing the [[eta-invariant]])

* [[John Phillips]]: *Self-Adjoint Fredholm Operators And Spectral Flow*, Canadian Mathematical Bulletin **39** 4 (1996) 460-467 &lbrack;[doi:10.4153/CMB-1996-054-4](https://doi.org/10.4153/CMB-1996-054-4)&rbrack; 

* {#CareyPhilips98} [[Alan Carey]], [[John Phillips]]: _Fredholm modules and spectral flow_  J. Canadian Math. Soc. **50** (1998) 673-718 &lbrack;[cms:10.4153/CJM-1998-038-x](https://cms.math.ca/10.4153/CJM-1998-038-x)&rbrack;

* [[Bernhelm Booß-Bavnbek]], Matthias Lesch, [[John Phillips]]: *Unbounded Fredholm Operators and Spectral Flow*, Canadian Journal of Mathematics **57** 2 (2005) 225-250 &lbrack;[doi:10.4153/CJM-2005-010-1](https://doi.org/10.4153/CJM-2005-010-1), [arXiv:math/0108014](https://arxiv.org/abs/math/0108014)&rbrack;

* [[Nils Waterstraat]]: *Fredholm Operators and Spectral Flow* &lbrack;[arXiv:1603.02009](https://arxiv.org/abs/1603.02009)&rbrack;

* Robert Skiba, Nils Waterstraat: *The Index Bundle for Selfadjoint Fredholm Operators and Multiparameter Bifurcation for Hamiltonian Systems* &lbrack;[arXiv:2012.05691](https://arxiv.org/abs/2012.05691)&rbrack;

* Nora Doll, [[Hermann Schulz-Baldes]], [[Nils Waterstraat]]: *Spectral Flow for Bounded Fredholm Operators*, Chapter 4 in: *Spectral Flow --- A Functional Analytic and Index-Theoretic Approach*, Studies in Mathematics **94**, De Gruyter (2023) &lbrack;[doi:10.1515/9783111172477](https://doi.org/10.1515/9783111172477)&rbrack;



category: analysis

[[!redirects Fredholm complex]]
[[!redirects Fredholm operators]]
[[!redirects parametrix]]


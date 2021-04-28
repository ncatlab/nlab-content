

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given a [[finite group]] $G$ with a set of generators $S$, its [[Cayley graph]] is, just as any [[undirected graph]], encoded by its adjacency matrix

\[
  \label{AdjacencyMatrix}
  \left(
    \left\{
    \array{
       1 &if \; g_1 g_2^{-1} \in S
       \\
       0 & otherwise
    }
    \right.
  \right)_{g_1, g_2 \in G}
\]

and the [[eigenvalues]] of this matrix are referred to as the *spectrum* of the Cayley graph.

More generally, any *coloring function* 

\[
  \label{ColoringFunction}
  c \;\colon\; G \longrightarrow \mathbb{C}
  \,,
\]

namely a [[function]] from the underlying [[set]] of $G$ to the [[complex numbers]] (for definiteness), induces the matrix

\[
  \label{ColoredMatrix}
  M_c 
  \;\coloneqq\;
  \big( c(g_1 g_2^{-1}) \big)_{g_1, g_2 \in G}
\]

and the [[eigenvalues]] of this matrix are the *Cayley graph spectrum* for coloring $c$.

For example:

* if $c$ is the [[characteristic function]] of the given set of generators of $G$, then $M_c$ (eq:ColoredMatrix) reduces to the adjacency matrix (eq:AdjacencyMatrix).

* if $c(g) = d(g,e)$ is the [[minimum|minimal]] number of generators needed to express $g$, then $M_c$ (eq:ColoredMatrix) is the [[graph distance]]-matrix of the Cayley graph -- specifically the original [[Cayley distance]] matrix if $G = Sym(n)$ is a [[symmetric group]] and $S$ its subset of [[transpositions]];

* if $c(g) = e^{- \beta d(g,e)}$ is the [[exponential|exponentiated]] [[graph distance]], then $M_c$ (eq:ColoredMatrix) is the [[kernel method|kernel matrix]] corresponding to the Cayley graph -- specifically the [[Cayley distance kernel]] if $G = Sym(n)$ is a [[symmetric group]] and $S$ its subset of [[transpositions]].

## Properties

### Character formula

\begin{prop}\label{CharacterFormula}
**(character formula for Cayley graph spectra)** \linebreak
  If the coloring function $c$ (eq:ColoringFunction) is a [[class function]], then the [[eigenvalues]] $EV$ of the color matrix (eq:ColoredMatrix) are 

* indexed by the [[irreducible representation|irreducible]] [[character of a linear representation|characters]] $\chi$ of $G$,

* given by the formula

  $$
    EV_\chi
    \;=\;
    \frac{1}{\chi(1)}
    \underset{
      g \in G
    }{\sum}
    c(g) \, \chi(g)
    \,,
  $$

* appear with multiplicity $(\chi(1))^2$;

* the corresponding [[eigenvectors]] are the component functions 

  $$
    \big(\rho_{i j}(g)\big)_{g \in G}
    \;\;
      \in
    \;\;
    \mathbb{C}[G]
  $$ 

  of the complex [[irreducible representations]] $\rho$ whose [[character of a linear representation|characters]] are the $\chi$, regarded for each $g \in G$ as [[unitary matrices]] $(\rho(g))_{i,j \in \{1, \chi(1)\}} \;\in\; Mat_{\chi(1) \times \chi(1)}(\mathbb{C})$.



\end{prop}

([Diaconis & Shahshahani 81, Cor. 3](#DiaconisShahshahani81), [Rockmore, Kostelec, Hordijk & Stadler 02, Thm. 1.1](#RockmoreKostelecHordijkStadler02),  [Kaski 02, Cor. 5.4](#Kaski02), [Foster-Greenwood & Kriloff 16, Thm. 4.3](#FosterGreenwoodKriloff16), see also [Liu & Zhou 18, Thm. 2.6](#LiuZhou18); in the special case that$G$ is an [[abelian group]] the result is due to [Lovász 1975](#Lovasz75)) 


## References

* {#Lovasz75} [[László Lovász]], *Spectra of graphs with transitive groups*, Period. Math. Hungar., 6(2):191–195, 1975 ([doi:10.1007/BF02018821](https://doi.org/10.1007/BF02018821), [pdf](https://web.cs.elte.hu/~lovasz/scans/spectra-of-graphs.pdf))

* [[László Babai]], *Spectra of Cayley graphs*, Journal of Combinatorial Theory, Series B Volume 27, Issue 2, October 1979, Pages 180-189 (<a href="https://doi.org/10.1016/0095-8956(79)90079-0">doi:10.1016/0095-8956(79)90079-0</a>)

* {#DiaconisShahshahani81} [[Persi Diaconis]], [[Mehrdad Shahshahani]], *Generating a random permutation with random transpositions*, Z. Wahrscheinlichkeitstheorie verw Gebiete 57, 159–179 (1981) ([doi:10.1007/BF00535487](https://doi.org/10.1007/BF00535487))

* {#RockmoreKostelecHordijkStadler02} Dan Rockmore, Peter Kostelec, Wim Hordijk, Peter F. Stadler, *Fast Fourier Transform for Fitness Landscapes*, Applied and Computational Harmonic Analysis Volume 12, Issue 1, January 2002, Pages 57-76 ([doi:10.1006/acha.2001.0346](https://doi.org/10.1006/acha.2001.0346))
 
* {#Kaski02} [[Petteri Kaski]], *Eigenvectors and spectra of Cayley graphs*, 2002 ([pdf](http://www.tcs.hut.fi/Studies/T-79.300/2002S/esitelmat/kaski_paper_020506.pdf), [[KaskiSpectraOfCayleyGraphs.pdf:file]])

* {#FosterGreenwoodKriloff16} [[Briana Foster-Greenwood]], [[Cathy Kriloff]], *Spectra of Cayley graphs of complex reflection groups*, J. Algebraic Combin., 44(1):33–57, 2016 ([arXiv:1502.07392](https://arxiv.org/abs/1502.07392), [doi:10.1007/s10801-015-0652-8](https://doi.org/10.1007/s10801-015-0652-8))

* {#LiuZhou18} Xiaogang Liu, Sanming Zhou, *Eigenvalues of Cayley graphs* ([arXiv:1809.09829](https://arxiv.org/abs/1809.09829))

* Farzaneh Nowroozi, Modjtaba Ghorbani, *On the spectrum of Cayley graphs via character table*, Journal of Mathematical NanoScience, Volume 4, 1-2 (2014) ([doi:10.22061/jmns.2014.477](https://dx.doi.org/10.22061/jmns.2014.477) [pdf](https://journals.sru.ac.ir/article_477_166922038b274bc7128566c1e2ce4b98.pdf))


[[!redirects Cayley graph spectra]]

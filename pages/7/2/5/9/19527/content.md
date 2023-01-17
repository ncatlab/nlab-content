

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[geometric group theory]], the _Cayley graph_ (also: _Cayley [[quiver]]_) of a [[group]], $G$, equipped with a [[set]] of [[generators]], $X$, encodes how the chosen generating elements operate (by multiplication)  on the [[elements]] of the group.


## Definition

Given a [[group]], $G$, and a [[set]] of [[generators]], $X$ (e.g. a [[finitely generated group]] if $X$ is a [[finite set]]), which we regard as a [[subset]] of the underlying set $|G|$ of $G$, we can form a [[directed graph]] with the [[elements]] of $G$ as the [[vertices]] and with its [[edges]] labelled (some people say 'coloured')  by the elements of $X$ with an edge joining a vertex, $g$, to the vertex $g x$ labelled by $x$

$$
  g \overset{x}{\longrightarrow} g x
$$


This graph is called the _Cayley graph_ of the group, $G$, relative to the set of generators.

The [[metric]] induced from corresponding [[graph distance]] is also called the *word metric* on the group $G$ with respect to its generators $X$.


## Examples 

### For the symmetric group

\begin{example}
The [[symmetric group]] $Sym(n)$ may be [[finitely generated group|generated]] from, in particular:

* all [[transposition permutations]] -- the corresponding Cayley [[graph distance]] is the original *[[Cayley distance]]*;

* the *adjacent* [[transpositions]] -- the corresponding Cayley [[graph distance]] is known as the *[[Kendall tau distance]]*.

\end{example}

Specifically:

\begin{example}\label{CayleyGraphForSym3}
**([[Cayley graph of Sym(3)]])**\linebreak
The following is the [[Cayley graph]] of the [[symmetric groups]] on 3 elements, $Sym(3)$, with [[edges]] corresponding to any [[transposition]] (not necessarily adjacent), hence whose [[graph distance]] is the [[Cayley distance]]:

\begin{tikzcd}[row sep=-6pt, column sep=14pt]
  123
  \ar[rrrr,-]
  \ar[ddddd,-]
  \ar[ddrrr,-]
  &&
  &&
  132
  \ar[ddddd,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  &&&
  \scalebox{.8}{$321$}
  \ar[dddr,-]
  \\
  &
  \scalebox{1.2}{231}
  \ar[ddl,-]
  \ar[uuurrr,-, crossing over]
  \ar[urr,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  213
  \ar[rrrr,-]
  &&&&
  312
\end{tikzcd}
\end{example}

\begin{example}\label{CayleyGraphOfSym4}
  
The Cayley graph of the [[symmetric group]] $Sym(4)$ with edges for [[transpositions]] looks as follows:

<center>
<img src="https://ncatlab.org/nlab/files/CayleyGraphOfSym4.jpg" width="400">
</center>

> graphics from [Kaski 02, p. 17](#Kaski02)

\end{example}

\begin{example}
Consider one of the standard presentations of the [[symmetric group]] $S_3$, $ (a,b  :  a^3, b^2, (a b)^2)$. Write $ r = a^3$, $s = b^2$, $t = (a b)^2$.  

The Cayley graph is easy to draw.  There are two triangles corresponding to $1 \to a \to a^2$ and to its translate by $b$, $b \to a b \to a^2 b$, flipping the orientation of the second, and three 2-cycles, $1\to b\to 1$, $a\to a b\to a$ and $a^2\to a^2b\to a^2$.

To understand the geometric significance of this graph we compare the algebraic information in the presentation with the homotopical information in the graph (considered as a CW-complex).

Looking at the presentation it leads to a free group, $F$, on the generators, $a$ and $b$, so $F$ is free of rank 2, but the normal closure of the relations $N(R)$ is a subgroup of $F$, so it must be
free as well, by the [[Nielsen-Schreier theorem]].  Its rank will be 7, given by the [[Nielsen-Schreier theorem|Schreier index formula]].

Looked at geometrically, this will be the [[fundamental group]] of the   Cayley graph, of the presentation.  This group is free on generators corresponding to edges outside  a maximal tree, and, of course, there are 7 of these.
\end{example}


## Related entries

* [[graph distance]]

  * [[Cayley distance]], [[Kendall distance]]

* [[identity among the relations]]



## References

### General

Textbooks accounts:

* [[Clara Löh]], Section II.3 of : *Geometric Group Theory*, Springer 2017 ([doi:10.1007/978-3-319-72254-2](https://link.springer.com/book/10.1007/978-3-319-72254-2), [pdf](http://www.mathematik.uni-regensburg.de/loeh/teaching/ggt_ws1011/lecture_notes_old.pdf))

* [[Cornelia Druţu]], [[Michael Kapovich]], Section 7.9 of: *Geometric group theory*, Colloquium Publications **63**, AMS 2018 ([ISBN:978-1-4704-1104-6](https://bookstore.ams.org/coll-63/), [pdf](https://courses.maths.ox.ac.uk/node/view_material/35649))



Review:

* [[Elena Konstantinova]], *Some problems on Cayley graphs*, Linear Algebra and its Applications Volume 429, Issues 11–12, 1 December 2008, Pages 2754-2769 ([doi:10.1016/j.laa.2008.05.010](https://doi.org/10.1016/j.laa.2008.05.010))

See also:

* Wikipedia, _[Cayley graph ](https://en.wikipedia.org/wiki/Cayley_graph)_

Discussion in [[homotopy type theory]]/[[univalent foundations of mathematics]]:

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]]: Def. 6.3.4 in: *[[Symmetry]]* (2021) &lbrack;[pdf](https://unimath.github.io/SymmetryBook/book.pdf)&rbrack;

### Spectra
 {#ReferencesSpectra}

Discussion of [[Cayley graph spectrum|Cayley graph spectra]]:

* [[László Lovász]], *Spectra of graphs with transitive groups*, Period. Math. Hungar., 6(2):191–195,1975 ([doi:10.1007/BF02018821](https://doi.org/10.1007/BF02018821), [pdf](https://web.cs.elte.hu/~lovasz/scans/spectra-of-graphs.pdf))

* [[László Babai]], *Spectra of Cayley graphs*, Journal of Combinatorial Theory, Series B Volume 27, Issue 2, October 1979, Pages 180-189 (<a href="https://doi.org/10.1016/0095-8956(79)90079-0">doi:10.1016/0095-8956(79)90079-0</a>)
 
* {#Kaski02} Petteri Kaski, *Eigenvectors and spectra of Cayley graphs*, 2002 ([pdf](http://www.tcs.hut.fi/Studies/T-79.300/2002S/esitelmat/kaski_paper_020506.pdf), [[KaskiSpectraOfCayleyGraphs.jpg:file]])

* [[Briana Foster-Greenwood]], [[Cathy Kriloff]], *Spectra of Cayley graphs of complex reflection groups*, J. Algebraic Combin., 44(1):33–57, 2016 ([arXiv:1502.07392](https://arxiv.org/abs/1502.07392), [doi:10.1007/s10801-015-0652-8](https://doi.org/10.1007/s10801-015-0652-8))

* Xiaogang Liu, Sanming Zhou, *Eigenvalues of Cayley graphs* ([arXiv:1809.09829](https://arxiv.org/abs/1809.09829))

* Farzaneh Nowroozi, Modjtaba Ghorbani, *On the spectrum of Cayley graphs via character table*, Journal of Mathematical NanoScience, Volume 4, 1-2 (2014) ([doi:10.22061/jmns.2014.477](https://dx.doi.org/10.22061/jmns.2014.477) [pdf](https://journals.sru.ac.ir/article_477_166922038b274bc7128566c1e2ce4b98.pdf))

### Distance on Cayley graphs 

On [[graph distances]] in Cayley graphs (generalizing the [[Cayley distance]] for the [[symmetric group]]):


For [[symmetric groups]] ([[permutations]]):

* Farzad Farnoud (Hassanzadeh), Lili Su, Gregory J. Puleo, Olgica Milenkovic, *Computing Similarity Distances Between Rankings*, Discrete Applied Mathematics Volume 232, 11 December 2017, Pages 157-175 ([doi:10.1016/j.dam.2017.07.038](https://doi.org/10.1016/j.dam.2017.07.038),  [pdf](https://arxiv.org/abs/1307.4339), [pdf](http://www.people.virginia.edu/~ffh8x/d/p/1-s2.0-S0166218X17303608-main.pdf))

* Mohammad Hossein Ghaffri, Zohreh Mostaghim, _Distance in Cayley graphs on permutations generated by $k m$ cycles_, Transactions on Combinatorics, Vol 6 No. 3 (2017) ([[GhaffriMostaghim17.pdf:file]])

[[!redirects Cayley graphs]]

[[!redirects Cayley quiver]]
[[!redirects Cayley quivers]]

[[!redirects word metric]]
[[!redirects word metrics]]

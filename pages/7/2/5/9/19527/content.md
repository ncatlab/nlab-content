

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

Textbooks:

* [[Cornelia Druţu]], [[Michael Kapovich]], Section 7.9 of: *Geometric group theory*, Colloquium Publications **63**, AMS 2018 ([ISBN:978-1-4704-1104-6](https://bookstore.ams.org/coll-63/), [pdf](https://courses.maths.ox.ac.uk/node/view_material/35649))

Review:

* [[Elena Konstantinova]], *Some problems on Cayley graphs*, Linear Algebra and its Applications Volume 429, Issues 11–12, 1 December 2008, Pages 2754-2769 ([doi:10.1016/j.laa.2008.05.010](https://doi.org/10.1016/j.laa.2008.05.010))

See also:

* Wikipedia, _[Cayley graph ](https://en.wikipedia.org/wiki/Cayley_graph)_

### Distance on Cayley graph 

On [[graph distances]] in Cayley graphs (generalizing the [[Cayley distance]] for the [[symmetric group]]):

For [[symmetric groups]] ([[permutations]]):

* Farzad Farnoud (Hassanzadeh), Lili Su, Gregory J. Puleo, Olgica Milenkovic, *Computing Similarity Distances Between Rankings*, Discrete Applied Mathematics Volume 232, 11 December 2017, Pages 157-175 ([doi:10.1016/j.dam.2017.07.038](https://doi.org/10.1016/j.dam.2017.07.038),  [pdf](https://arxiv.org/abs/1307.4339), [pdf](http://www.people.virginia.edu/~ffh8x/d/p/1-s2.0-S0166218X17303608-main.pdf))

* Mohammad Hossein Ghaffri, Zohreh Mostaghim, _Distance in Cayley graphs on permutations generated by $k m$ cycles_, Transactions on Combinatorics, Vol 6 No. 3 (2017) ([[GhaffriMostaghim17.pdf:file]])

[[!redirects Cayley graphs]]

[[!redirects Cayley quiver]]
[[!redirects Cayley quivers]]

[[!redirects word metric]]
[[!redirects word metrics]]

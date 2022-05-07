
> This page is about the notion in [[combinatorics]]. For other notions of the same name see at _[[graph of a function]]_ and _[[graph of a functor]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

##  Idea

A __graph__ is a collection of _[[vertices]]_ and _[[edges]]_; each [[edge]] links a pair of [[vertices]], defining a relationship of _incidence_ between vertices and edges.  There are several variations on the idea, described below.

This is the sense of graph in [[combinatorics]]; the other sense in high-school algebra, which interprets a [[morphism]] $f: A \to B$ as a [[subobject]] of the [[product]] $A \times B$, is unrelated; see _[[graph of a function]]_ for more on this.


##  Definitions

Let $V$ and $E$ be [[sets]]; call an element of $V$ a __vertex__ and an element of $E$ an __edge__.  A __graph__ is given by $V$, $E$, and a mapping $d$ that interprets edges as pairs of vertices.  Exactly what this means depends on how one defines 'mapping that interprets' and 'pair'; the possibilities are given below.  We will need the following notation:

*  $V^2$ is the [[cartesian product]] of $V$ with itself, the set of ordered pairs $(x,y)$ of vertices;
*  $\Delta_V$ is the [[diagonal subset]] of $V$, the set of pairs $(x,x)$, so that its [[complement]] $V^2 \setminus \Delta_V$ is the set of pairs as above where $x \neq y$;
*  $\left\langle{V \atop 2}\right\rangle$ is the [[quotient set]] of $V^2$ in which $(x,y)$ is identified with $(y,x)$, the set of unordered pairs $\{x,y\}$ of vertices;
*  $\left({V \atop 2}\right)$ is the quotient set of $V^2 \setminus \Delta_V$ in which $(x,y)$ is identified with $(y,x)$, the set of unordered pairs where $x \neq y$.

### Undirected graphs

We are now ready for the first batch of definitions.

*  For a __simple graph__, a pair of vertices is a [[subset]] of $V$ of [[cardinality]] $2$, and we interpret edges as unordered pairs of vertices in a one-to-one way.  Thus a simple graph is given by $V$, $E$, and an [[injective function]] $d: E \hookrightarrow \left({V \atop 2}\right)$.  Among graph theorists, this is often the default meaning of 'graph' unless another is specified. The category of simple graphs is called [[category of simple graphs|SimpGph]]

*  For a __[[multigraph]]__, a pair of vertices is the same as above, but we interpret edges as pairs of vertices in a many-to-one way.  Thus a multigraph is given by $V$, $E$, and an arbitrary [[function]] $d: E \to \left({V \atop 2}\right)$.

*  For a __loop graph__, a pair of vertices is any subset of the form $\{x,y\}$, where $x = y$ is allowed, and we interpret edges as pairs of vertices in a one-to-one way again.  Thus a loop-graph is given by $V$, $E$, and an injective function $d: E \hookrightarrow \left\langle{V \atop 2}\right\rangle$.

*  For a __[[pseudograph]]__, a pair of vertices is as in a loop graph, while edges are interpreted as pairs of vertices as in a multigraph.  Thus a pseudograph is given by $V$, $E$, and a function $d: E \to \left\langle{V \atop 2}\right\rangle$.

Note:  While 'simple graph' is unambiguous, the other terms above are not.  In particular, 'multigraph' sometimes means a pseudograph, 'pseudograph' sometimes means a loop graph, and 'loop graph' sometimes means a pseudograph.  These could be made unambiguous by saying 'simple multigraph', 'simple loop graph', and 'multipseudograph', respectively, but we will try to keep our terminology short. 
An oldfashioned (e.g. [p. 142](#Harary1953)) term for 'simple graph' is 'linear graph', traces of which remain in the usual term 'linear hypergraph' in combinatorics (i.e. hypergraph any two edges of which intersect in at most one element of the ground set).

### Directed graphs

In all four of the above, edges are interpreted as *unordered* pairs.  If we instead interpret edges as *ordered* pairs, then we get four new concepts:

*  A __directed graph__ consists of $V$, $E$, and an injective function $d: E \hookrightarrow V^2 \setminus \Delta_V$;
*  a __directed multigraph__ consists of $V$, $E$, and a function $d: E \to V^2 \setminus \Delta_V$;
*  a __directed loop graph__ consists of $V$, $E$, and an injective function $d: E \hookrightarrow V^2$;
*  a __[[directed pseudograph]]__ consists of $V$, $E$, and a function $d: E \to V^2$.

Directed pseudographs are commonly used in [[category theory]], where they are often called 'directed graphs', 'digraphs', or (less ambiguously) '[[quivers]]'.


The same terminological ambiguities as above apply here as well, and they can be resolved in the same way, including using 'simple directed graph' for a directed graph if necessary.  One can also use 'undirected' in place of 'directed' to emphasise that the previous definitions apply instead of these.


It is always possible to interpret any kind of graph as a directed pseudograph (a quiver), in which there happens to be at most one edge between a given pair of vertices, or there happen to be no loops (or alternatively exactly one of every possible kind of loop), or in which there is an edge from $x$ to $y$ if and only if there is an edge from $y$ to $x$, or some mixture of these.

### Undirected graphs as directed graphs with an involution

There is an alternative definition of an undirected graph allowing loops and multiple edges (cf. [Serre 1977](#Serre1977)), that begins with the structure of a quiver $s,t : E \rightrightarrows V$ and then asks in addition for a [[fixed point]] free [[involution]] on edges $i : E \to E$ swapping source and target, i.e., such that
$$
i(i(e)) = e
\quad
i(e) \ne e
\quad
s(i(e)) = t(e)
\quad
t(i(e)) = s(e)
$$
Of course, since the source $s : E \to V$ and target $t : E \to V$ functions determine each other in the presence of the involution $i : E \to E$, it is enough to give, say, $s$ and $i$ to define an undirected graph.
In that case, one might alternatively view $E$ as a set of "half-edges" or "flags" (with $i$ the involution swapping the two halves of an edge), and even lift the condition that $i$ has no fixed points to allow for the possibility of undirected graphs with "dangling" or "open" edges (i.e., with only one side attached to a vertex).

Although this definition of undirected graphs with open edges is standard (cf. [[ribbon graph]]), [Kock (2016b)](#Kock2016BM) remarks that "it does not naturally lead to good notions of morphisms, beyond isomorphisms". A slight variation of this definition with a more natural notion of morphism was introduced by [Joyal and Kock (2009)](#JoyalKockQPL): they define a "Feynman graph" as a triple of [[finite sets]] $V, E, H$ together with a triple of a function $t : H \to V$, an injection $s : H \to E$, and a fixed point free involution $i : E \to E$. (See also [Kock (2016a)](#Kock2016GHP) for further discussion.)

### Orientations

An **orientation** of an undirected graph is the choice of a direction for every edge.
Formally, if we define undirected graphs as above to be quivers $E \rightrightarrows V$ equipped with a fixed point free involution $i : E \to E$, then an orientation corresponds to the choice of a subset $E^+ \subseteq E$ such that $E$ is the [[disjoint union]] $E = E^+ \uplus i(E^+)$.

Any orientation of an undirected graph induces a corresponding directed graph $E^+ \rightrightarrows V$.
In many situations, though, it is useful to consider a given undirected graph equipped with one of many possible orientations.
For example, various [[graph invariants]] (such as the [[flow polynomial]], or [[W. T. Tutte|Tutte]]'s original definition of the [[Tutte polynomial]]) can be defined for an arbitrary orientation of a graph, but are independent of the choice of orientation.

## Auxiliary definitions

The term __arc__ is often used for an *ordered* edge, while __line__ is sometimes used for an *unordered* edge.  We say that an arc $e$ with $d(e) = (x,y)$ is an arc __from $x$ to $y$__, while a line $e$ such that $d(e) = \{x,y\}$ is a line __between $x$ and $y$__.  In either case, a __loop__ is an edge from a vertex to itself or between a vertex and itself; only (possibly directed) loop graphs and pseudographs can have loops.

Given any sort of graph, we can define a [[binary relation]] on $V$; say that $x$ and $y$ are __adjacent__, written $x \sim y$, if there exists an edge $e$ such that $d(e) = (x,y)$ or $d(e) = \{x,y\}$.  A directed loop graph is determined entirely by this relation; we may say that it *is* $V$ equipped with a binary relation.  Then a simple directed graph is $V$ equipped with an [[irreflexive relation]] (or equivalently a [[reflexive relation]]), and an undirected loop graph is $V$ equipped with a [[symmetric relation]].

A graph is __[[finite graph|finite]]__ if $V$ and $E$ are both [[finite sets]].  Given a [[linear ordering]] of the [[vertices]] of a [[finite graph]], its __adjacency matrix__ is a square [[matrix]] whose $(i,j)$th entry gives the number of edges $e$ between the $i$th and $j$th vertices or from the $i$th vertex to the $j$th vertex.  In the examples above where a graph is determined by a binary relation on $V$, then matrix multiplication gives composition of relations.


##  Morphisms of graphs

An __[[isomorphism]]__ from $G = (V,E,d)$ to $G' = (V',E',d')$ consists of a bijection $f: V \to V'$, together with a bijection from $E$ to $E'$ (also denoted $f$) such that $f$ commutes with $d$; that is, $d(f(e)) = (f(x),f(y))$ or $d(f(e)) = \{f(x),f(y)\}$ whenever $d(e) = (x,y)$ or $d(e) = \{x,y\}$ (as appropriate).  Two graphs $G$ and $G'$ are __isomorphic__ if there exists such an isomorphism.  Then [[finite graphs]] $G$ and $G'$ are isomorphic if and only if they have the same number of vertices and, for some ordering of their vertices, they have the same adjacency matrix.

A __[[morphism]]__ from $G$ to $G'$ should consist of functions $f: V \to V'$ and $f: E \to E'$ such that $f$ commutes with $d$.  However, some authors allow $f(e)$ to be undefined if $d(e) = (x,y)$ or $d(e) = \{x,y\}$ but $f(x) = f(y)$ when using a notion of graph where loops are forbidden.  The difference amounts to whether one interprets a simple graph as a special kind of loop graph in which no loops exist (the first kind of morphism) or in which each vertex has a unique loop (the second kind of morphism).  Either way, an isomorphism (as defined above) is precisely an invertible morphism.

+--{: .query}
[[Mike Shulman]]: Isn't there something backwards about defining "isomorphic" and _then_ "isomorphism" and _then_ "morphism"?  Doesn't the logic generally flow in the other direction (especially around here)?

[[David Roberts]]: well at least there's a historical precedent: this is how Bourbaki would have done it via structures :)

_Toby_:  That, and it\'s simpler to state the definition of 'isomorphic' than 'isomorphism'.  Not to mention that graph theorists, in my experience, tend to care much more about the property of being isomorphic than the structure of having an isomorphism.  As for 'morphism', there\'s even disagreement about what that should be; I think that my definition is the obvious correct one, but it disagrees with the one at, for example, [Wikipedia](http://en.wikipedia.org/wiki/graph) (although they had my definition in the past); both versions give the same notion of isomorphism, however.

[[Mike Shulman]]: Well, but we aren't graph theorists here, are we?  Isn't it okay for us to rephrase their definitions in the more categorically sensible order?

_Toby_:  I disagree that 'morphism' before 'isomorphism' is more categorially sensible.  That\'s like defining $\leq$ before $=$; sometimes useful, sometimes not.  Since I am getting ambiguity about morphisms in what I find online, I\'d prefer to do isomorphisms first.  With luck, I\'ll find some terminology to distinguish the two kinds of morphisms, or we can make up our own.

[[Mike Shulman]]: Okay, I'll accept that sometimes it makes sense to have isomorphisms before morphisms.  Certainly there are other situations in which the notion of isomorphism is more obvious, or less subject to debate, than the notion of morphism.  But I am happy that now "isomorphism" comes before "isomorphic."

[[RonnieBrown]]: I hope it is helpful to add the reference below, which also contains quite a few references to categorical treatments of graphs. 

=--

Under the second notion of morphism (where simple graphs are identified with sets equipped with a symmetric reflexive relation), the [[category of simple graphs]] has many desirable properties (q.v.). 

## Notions of subgraphs from the nPOV

A usual definition of _subgraph_ in combinatorics is, roughly: _subset_. 
More precisely, if _undirected simple graph_ means _pair $(V,E)$ of two sets, with $E\subseteq[V]^2$ any subset of the set of all two-element subsets of $V$_, then a usual meaning of _subgraph_ of $(V,E)$ is (cf. e.g. [p. 3](#DiestelGraphTheoryFourthEd)): any pair $(W,F)$ with $W\subseteq V$, $F\subseteq E$, and[^1] $F\subseteq [W]^2$. 

[^1]: The last condition is to ensure that $(W,F)$ is itself again a graph, which would not be guaranteed if we defined subgraph to be just any pair of subsets of the respective sets $V$ and $E$. 


In particular, such a subgraph $(W,F)$ may have isolated vertices which are not isolated in the ambient graph $G$, and $(W,F)$ need not be an _induced_ subgraph, which by definition is a subgraph in the above sense for which $F = [W]^2\cap E$. In words: the edge-set of an _induced_ subgraph must contain all edges _induced_ within the ambient graph by the vertex set of the subgraph.[^2] 

[^2]: This happens to be the usual notion of substructure in model theory, for any relational structure.

Another usual notion of subgraph in combinatorics is[^3] _spanning_ subgraph: 


[^3]: Somewhat counterintuitively (with regard to connotations of the words _spanning_ and _induced_), a _spanning_ subgraph need not be _induced_, and in fact it never is, _except_ if the subgraph is the graph itself. 


this means just any subgraph $(W,F)$ in the above sense with $W=V$. There are three kinds of spanning subgraphs which are the most studied: [[Hamilton circuit]]s[^4], [[perfect matching]]s and [[spanning tree]]s.

[^4]: We here follow A. Bondy's choice of words in [p. 20](#HandbookOfCombinatoricsVol1), both in the decision whether to use _hamiltonian_ or _Hamilton_, and whether to use _cycle_ or _circuit_. 
The term _circuit_ is less usual than _cycle_ in combinatorics, but less ambiguous, not longer, and more clearly signalling that the combinatorial notion is meant (not one of the many other meanings of _cycle_).
One argument in favor of _Hamilton_ is that _any_ circuit, by itself, is _hamiltonian_.

From the [[nPOV]], it is often possible to describe notions of subgraph in terms of types of monomorphisms in categories of graphs; for example, 

* _subgraphs_ are [[monos]], and 

* _induced subgraphs_ are [[regular monos]] 

in the [[category of simple graphs]], and similarly for suitable categories of other types of graph. 

One synonym, in the nLab[^5] for _induced subgraph_ is *full subgraph*, for brevity, and for harmony with other uses of _full_ in category theory (but also for more precise reasons).

[^5]: Incidentally, the term _full_ was in use in mid-twentieth century graph theory, then seems to have fallen out of favor.

The precise meaning of _subgraph_ depends on the chosen formalization of *graph*, needless to say.

## Undirected graphs as 1-complexes, barycentric subdivision

Recall that a [[simplicial complex]] of dimension one consists of the data of a set $V$ together with a set $S$ of non-empty subsets of $V$ of cardinality at most $2$, that contains all of the [[singleton]] subsets.
In other words, a 1-dimensional simplicial complex is essentially the same thing as a simple graph, with the set of edges being determined by the set of simplices and vice versa:
$$
E = \{\{x,y\} \mid \{x,y\} \in S, x \ne y\}
\qquad
S = \{\{x\} \mid x \in V\} \cup E
$$
For this reason, simple graphs are sometimes referred to as **simplicial graphs** [(Gross & Tucker 1987)](#GrossTucker).
On the other hand, an undirected graph $G$ with loops or multiple edges can more generally be seen as a 1-dimensional [[CW-complex]] (or more precisely, it has a [[geometric realization]] $|G|$ as a CW-complex in which 0-cells correspond to vertices and 1-cells to edges).

Given a general undirected graph, it is always possible to obtain a simple graph through the process of _[[barycentric subdivision]]_.
Let $G$ be a graph with vertex set $V$ and edge set $E$.
The **barycentric subdivision** of $G$ is the graph $G'$ with vertex set $V \cup E$, and with an edge joining $v \in V$ to $e \in E$ just in case $v$ is incident to (i.e., at either end of) $e$ in $G$.
It is easy to check that $G'$ contains no loops, while the two-fold barycentric subdivision $G''$ contains no loops or multiple edges, in other words is a simple graph.
(More generally, the $n$-fold barycentric subdivision contains no circuit of length $\le n$).
Part of the reason for the importance of simple graphs is that many "topological" properties of a graph $G$ (such as [[planar graph|planarity]], first [[Betti number]], etc., which can be defined in terms of the geometric realization of $G$) are preserved under barycentric subdivision.
(Although obviously, not all _graph-theoretic_ properties are preserved. For example, barycentric subdivision always produces a [[bipartite graph]]).

## Flavors of graphs

* [[reflexive graph]]

* [[directed graph]]

## Lawvere's remarks on graph theory 


At the [[Como]] conference in 1990, [[William Lawvere]] gave a videotaped lecture including the following remarks:


> {#LawvreOnGraphTheory} I have great problems reading books on graph theory, books and papers on graph theory, because they never tell you exactly what they are talking about. Sometimes the graphs are [word inaudible, even when played slower], sometimes they are absolutely reflexive, sometimes they are not. 
Even if they go so far as talking about homomorphisms, I still don't know exactly what that is, i.e., which category are we in? 
What they should do is admit that they are working in three or four *different* categories and they don't know how to pass from one to the other, and so on, and [inaudible words] to simplify.  
But no, they prefer to talk in a vague way and smushing these together. [inaudible] tried to understand some of the problems of graph theorists and get [bogged? locked?] in the first page. 
Does anybody actually know what a graph minor is? 
[some interjection from the audience] Graph minor. Big problem. 
(..) you see, this famous [inaudible works] problem on graph minors. 
Looks like that that might be interesting. 
But I can't determine *exactly* what it is, because, if you read the first parts of the paper, they waffle, you see, they don't give you a *property* (...)
([William Lawvere] in his 1990 lecture at [[Como]], Italy, Villa Olmo)



## Related concepts

* **graph**

* [[omega-graph]]

* [[planar graph]], [[connected graph]]

* [[empty graph]]

* [[ribbon graph]]

* [[hypergraph]]

* [[quiver]], [[McKay quiver]]

* [[n-quiver]]

* [[distance (graph theory)]]

* [[relation]]

* [[category]], [[free category]]

* [[Feynman diagram]]

* [[graph complex]], [[formality of the little n-disk operad]]

* [[graph of groups]]

* [[semi-graph]]

## References

Textbooks:

* Frank Harary (1969), _Graph Theory_, Addison-Wesley.



* Frank Harary and E.M. Palmer (1973), _Graphical Enumeration_, Academic Press.

* {#Serre1977} [[Jean-Pierre Serre]] (1977), _Trees_, Springer.

* [[W. T. Tutte]] (1984), _Graph Theory_, Addison-Wesley.

* {#GrossTucker} Jonathan L. Gross and Thomas W. Tucker (1987), _Topological Graph Theory_, Wiley.

* Gunther Schmidt and Thomas Str&#246;hlein (1993), _Relations and Graphs: Discrete Mathematics for Computer Scientists_, EATCS Monographs on Theoretical Computer Science, Springer.

* {#HandbookOfCombinatoricsVol1} A. Bondy. Basic Graph Theory: Paths and Circuits. Elsevier Amsterdam, 1995, Vol. 1, pp. 1--110

* Chris Godsil and Gordon Royle (2001), _Algebraic Graph Theory_, Springer.

* {#DiestelGraphTheoryFourthEd} R. Diestel, Graph Theory, 4. ed., Springer 2010

Other references:

* [[Bill Lawvere]] (1989), _Qualitative distinctions between some toposes of generalized graphs_, in Categories in computer science and logic (Boulder, CO,   1987), volume 92 of _Contemporary Mathematics_, 261--299. American Mathematical Society, Providence, RI.

* E. Babson, H. Barcelo, M. de Longueville, R. Laubenbacher, A Homotopy Theory for Graphs, [arXiv:math/0403146 ](http://arxiv.org/abs/math/0403146)

* [[Ronnie Brown]], I. Morris, J. Shrimpton, and C.D. Wensley (2008), _Graphs of Morphisms of Graphs_, Electronic Journal of Combinatorics, A1 of Volume 15(1), 1--28.


* {#Harary1953} [[Frank Harary]]: _On the notion of balance of a signed graph_. The   Michigan Mathemathical Journal, Volume 2, Issue 2 (1953), 143-146.

* {#JoyalKockQPL} [[André Joyal]] and [[Joachim Kock]], Feynman graphs, and nerve theorem for compact symmetric multicategories (extended abstract), in _Proceedings of the 6th International Workshop on Quantum Physics and Logic_(Oxford 2009), Electronic Notes in Theoretical Computer Science 270 (2) (2011), 105-113. [arXiv:0908.2675](https://arxiv.org/abs/0908.2675)

* {#Kock2016GHP} [[Joachim Kock]], Graphs, hypergraphs, and properads, _Collect. Math._ 67 (2016), 155-190. [arXiv:1407.3744](https://arxiv.org/abs/1407.3744)

* {#Kock2016BM} [[Joachim Kock]], Cospan construction of the graph category of Borisov and Manin, [arXiv:1611.10342](https://arxiv.org/abs/1611.10342)

* Martin Schmidt, _Functorial Approach to Graph and Hypergraph Theory_, ([arXiv:1907.02574](https://arxiv.org/abs/1907.02574))

See also [[quiver#references|quiver - references]].

Discussion of use of [[simplicial complexes]] in graph theory:

* MO, _[What have simplicial complexes ever done for graph theory?](http://mathoverflow.net/questions/161586/what-have-simplicial-complexes-ever-done-for-graph-theory)_


[[!redirects linear graph]]
[[!redirects graph]]
[[!redirects graphs]]
[[!redirects undirected graph]]
[[!redirects undirected graphs]]
[[!redirects simple directed graph]]
[[!redirects simple directed graphs]]
[[!redirects graph theory]]

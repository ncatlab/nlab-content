##  Idea

A __graph__ is a collection of _vertices_ and _edges_, each edge links a pair of vertices.  There are several variations on the idea, described below.

This is the sense of graph in combinatorics; the sense in high-school algebra, which interprets a [[morphism]] $f: A \to B$ as a [[subobject]] of the [[product]] $A \times B$, is not particularly related; see [[graph of a function]] if we ever write about that.

We have a separate article on [[directed graphs]] (in the sense of directed multipseudographs below), since these are closely related to [[categories]].


##  Definitions

Let $V$ and $E$ be [[sets]]; call an element of $V$ a __vertex__ and an element of $E$ an __edge__ or __arc__.  A __graph__ is given by $V$, $E$, and a [[function]] $d$ from $E$ to $V^2$; we say that $a$ is an edge __between__ $x$ and $y$, or __from__ $x$ __to__ $y$, if $d(a) = (x,y)$.  The function $d$ is often subject to the conditions below:

*  By default, we require that the function $d: E \to V^2$ be an [[injection]]; if we do not make this requirement, then we have a __multigraph__.
*  By default, we require that that, for every vertex $x$, there is exactly one edge over $(x,x)$; if we do not make this requirement, then we have a __pseudograph__.  (In a pseudograph, such an edge is called a __loop__.)
*  By default, we require that the graph be __undirected__: the [[fibre]] over $(x,y)$ should be isomorphic (same [[cardinality]]) as the fibre over $(y,x)$.
A graph satisfying this condition is __undirected__; if we do not make this requirement, then we have a __directed graph__.  (One usually speaks of _edges_ _between_ vertices in an undirected graph but _arcs_ _from_ one vertex _to_ another in a directed one.)

A graph that satisfies all of the above conditions may be called a __simple graph__ to be more clear, especially in a context where one of more of these defaults is *not* being assumed.  One can also mix 'simple' with 'multi&#8209;', 'pseudo&#8209;', or 'directed' to clarify that *only* the indicated relaxation is being made; but 'undirected' is usually used to indicate that the graph is not allowed to be directed.  Note that the terms 'multi&#8209;', 'pseudo&#8209;', and 'directed' are examples of the [[red herring principle]]; a simple graph is an example of a directed multipseudograph, but not every directed multipseudograph is simple.

The above definition shows all of the possibilities, but it is unnecessarily complicated if one is interested in applying any of the usual restrictions; then the definition can be simplified as follows:
*  If the graph is required to be undirected, then we may replace $V^2$ with $\left[{V \atop 2}\right]$, the set of all subsets of $V$ of the form $\{x,y\}$; we replace $E$ with a [[quotient set]] where an edge over $(x,y)$ is identified with the corresponding edge over $(y,x)$.
*  If the graph is not allowed to be a pseudograph, then we may replace $V^2$ with $V^2 \setminus \{(x,x) \;|\; x \in V\}$; that is, we ignore all of the loops.
*  If both of the above apply, then we may replace $V^2$ with $\left({V \atop 2}\right)$, the set of all subsets of $V$ of cardinality $2$; again, we replace $E$ with a quotient set, which now has exactly half the cardinality of the original.
*  If the graph is not allowed to be a multigraph, then we may take $E$ to be explicitly a [[subset]] of $V^2$ (rather than an arbitrary set equipped with an injection to $V^2$).  If the graph is also undirected, then we may take $E$ to be a subset of $\left[{V \atop 2}\right]$ or $\left({V \atop 2}\right)$.

Given any sort of graph, we can define a [[binary relation]] on $V$; say that $x$ and $y$ are __adjacent__, written $x \sim y$, if there exists an edge over $(x,y)$ (or over $\{x,y\}$, or an edge that *is* one of these).  A simple directed pseudograph is determined entirely by this relation; we may say that it *is* $V$ equipped with such a relation.  Then a simple directed graph is $V$ equipped with a [[reflexive relation]], and a simple undirected pseudograph is $V$ equipped with a [[symmetric relation]].

Often in combinatorics, one requires that $V$ and $E$ be [[finite sets]].  Sometimes one also requires $V$ to be [[inhabited set|inhabited]], (but surely that\'s silly).  For example, Harary defines the concept (and related terms) in the following manner (page 9):
> A _graph_ $G$ consists of a finite nonempty set $V = V(G)$ of $p$ _points_ together with a prescribed set $X$ of $q$ unordered pairs of distinct points of $V$.  Each pair $x = \{u, v\}$ of points in $X$ is a _line_ of $G$, and $x$ is said to _join_ $u$ and $v$.  We write $x = u v$ and say that $u$ and $v$ are _adjacent points_ (sometimes denoted $u adj v$);  point $u$ and line $x$ are _incident_ with each other, as are $v$ and $x$.  If two distinct lines $x$ and $y$ are incident with a common point, then they are _adjacent lines_.  A graph with $p$ points and $q$ lines is called a $(p, q)$ _graph_.  The $(1, 0)$ graph is _trivial_.

+-- {: .query}
sorry to be a pain, inserting adjectives like that, but here at the Lab you'll likely be confronted with graphs with a proper class (or large set, depending on the flavour of your foundations) of vertices. Or at least any set of vertices whatever.  ---Anon

I\'ve now clarified that this is just one example of how the term might be defined, so I\'ve restored the original text in the quotation.  ---Toby

I'm more of a "stepwise refinement" than a "most general definition first" sort of guy, and nobody knows the trouble I've seen when folks get to fightin' over terminology in this area.  So I started with a conception that is widely used among some of the larger schools of practicing graph theorists ... ---JA

=--


##  Morphisms of graphs

Two graphs $G = (V,E,d)$ and $G' = (V',E',d')$ are __[[isomorphism|isomorphic]]__ if there exists a [[bijection]] $f: V \to V'$ such that the fibre (in $G$) over $(x,y)$ (or $\{x,y\}$) always has the same cardinality as the fibre over $(f(x),f(y))$ (or $\{f(x),f(y)\}$); if $G, G'$ are not allowed to be multigraphs, then we can simply say that $x \sim y$ if and only if $f(x) \sim f(y)$.

An __isomorphism__ from $G$ to $G'$ is such a bijection, together with a family of bijections for each fibre above; if $G, G'$ are not allowed to be multigraphs, then the bijection $f$ is sufficient (if it satisfies the condition that $x \sim y$ if and only if $f(x) \sim f(y)$).

A __[[morphism]]__ from $G$ to $G'$ is any function $f: V \to V'$ together with, for each pair $x,y$ of vertices, a function from the fibre over $(x,y)$ (or $\{x,y\}$) to the fibre over $(f(x),f(y)$ (or $\{f(x),f(y)\}$); if $G, G'$ are not allowed to be multigraphs, then the function $f$ is sufficient, as long as $x \sim y$ only if $f(x) \sim f(y)$.

When $G$ and $G'$ are not allowed to be pseudographs, note that there may be a morphism from $G$ to $G'$ in which $f(x) = f(y)$, even when there is a (non-loop) edge from $x$ to $y$.  This is why simple graphs should be interpreted as pseudographs in which $x \sim x$ always instead of $x \sim x$ never.
+-- {: .query}
Actually, I\'m getting conflicting reports on this from different sources, but this seems to most sensible way to me.  For example, then the category of graphs has a [[terminal object]], which may be identified with the [[point]].  ---Toby
=--


## References ##

* Harary, Frank (1969), _Graph Theory_, Addison-Wesley.
* Harary, Frank and Palmer, E.M. (1973), _Graphical Enumeration_, Academic Press.
* Lambek, J. and Scott, P.J. (1986), _Introduction to Higher Order Categorical Logic_, Cambridge University Press.
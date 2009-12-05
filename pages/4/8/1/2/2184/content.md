#Contents##

* automatic table of contents goes here
{:toc}

##  Idea

A __graph__ is a collection of _vertices_ and _edges_; each edge links a pair of vertices.  There are several variations on the idea, described below.

This is the sense of graph in combinatorics; the sense in high-school algebra, which interprets a [[morphism]] $f: A \to B$ as a [[subobject]] of the [[product]] $A \times B$, is not particularly related; see [[graph of a function]] for more on this.


##  Definitions

Let $V$ and $E$ be [[sets]]; call an element of $V$ a __vertex__ and an element of $E$ an __edge__.  A __graph__ is given by $V$, $E$, and a mapping $d$ that interprets edges as pairs of vertices.  Exactly what this means depends on how one defines 'mapping that interprets' and 'pair'; the possibilities are given below.  We will need the following notation:

*  $V^2$ is the [[cartesian product]] of $V$ with itself, the set of ordered pairs $(x,y)$ of vertices;
*  $\Delta_V$ is the [[diagonal subset]] of $V$, the set of pairs $(x,x)$, so that its [[complement]] $V^2 \setminus \Delta_V$ is the set of pairs as above where $x \neq y$;
*  $\left\langle{V \atop 2}\right\rangle$ is the [[quotient set]] of $V^2$ in which $(x,y)$ is identified with $(y,x)$, the set of unordered pairs $\{x,y\}$ of vertices;
*  $\left({V \atop 2}\right)$ is the quotient set of $V^2 \setminus \Delta_V$ in which $(x,y)$ is identified with $(y,x)$, the set of unordered pairs where $x \neq y$.


We are now ready for the first batch of definitions.

*  For a __simple graph__, a pair of vertices is a [[subset]] of $V$ of [[cardinality]] $2$, and we interpret edges as unordered pairs of vertices in a one-to-one way.  Thus a simple graph is given by $V$, $E$, and an [[injective function]] $d: E \hookrightarrow \left({V \atop 2}\right)$.  Among graph theorists, this is the standard meaning of 'graph' unless another is specified.

*  For a __multigraph__, a pair of vertices is the same as above, but we interpret edges as pairs of vertices in a many-to-one way.  Thus a multigraph is given by $V$, $E$, and an arbitrary [[function]] $d: E \to \left({V \atop 2}\right)$.

*  For a __loop graph__, a pair of vertices is any subset of the form $\{x,y\}$, where $x = y$ is allowed, and we interpret edges as pairs of vertices in a one-to-one way again.  Thus a loop-graph is given by $V$, $E$, and an injective function $d: E \hookrightarrow \left\langle{V \atop 2}\right\rangle$.

*  For a __pseudograph__, a pair of vertices is as in a loop graph, while edges are interpreted as pairs of vertices as in a multigraph.  Thus a pseudograph is given by $V$, $E$, and a function $d: E \to \left\langle{V \atop 2}\right\rangle$.

Note:  While 'simple graph' is unambiguous, the other terms above are not.  In particular, 'multigraph' sometimes means a pseudograph, 'pseudograph' sometimes means a loop graph, and 'loop graph' sometimes means a pseudograph.  These could be made unambiguous by saying 'simple multigraph', 'simple loop graph', and 'multipseudograph', respectively, but we will try to keep our terminology short.


In all four of the above, edges are interpreted as *unordered* pairs.  If we instead interpret edges as *ordered* pairs, then we get four new concepts:

*  A __directed graph__ consists of $V$, $E$, and an injective function $d: E \hookrightarrow V^2 \setminus \Delta_V$;
*  a __directed multigraph__ consists of $V$, $E$, and a function $d: E \to V^2 \setminus \Delta_V$;
*  a __directed loop graph__ consists of $V$, $E$, and an injective function $d: E \hookrightarrow V^2$;
*  a __directed pseudograph__ consists of $V$, $E$, and a function $d: E \to V^2$.  These are commonly used in [[category theory]]; see [[digraph]] and [[quiver]].

The same terminological ambiguities as above apply here as well, and they can be resolved in the same way, including using 'simple directed graph' for a directed graph if necessary.  One can also use 'undirected' in place of 'directed' to emphasise that the previous definitions apply instead of these.

It is always possible to interpret any kind of graph as a directed pseudograph, in which there happens to be at most one edge between a given pair of vertices, or there happen to be no loops (or alternatively exactly one of every possible kind of loop), or in which there is an edge from $x$ to $y$ if and only if there is an edge from $y$ to $x$, or some mixture of these.


## Auxiliarly definitions

The term __arc__ is often used for an *ordered* edge, while __line__ is sometimes used for an *unordered* edge.  We say that an arc $e$ with $d(e) = (x,y)$ is an arc __from $x$ to $y$__, while a line $e$ such that $d(e) = \{x,y\}$ is a line __between $x$ and $y$__.  In either case, a __loop__ is an edge from a vertex to itself or between a vertex and itself; only (possibly directed) loop graphs and pseudographs can have loops.

Given any sort of graph, we can define a [[binary relation]] on $V$; say that $x$ and $y$ are __adjacent__, written $x \sim y$, if there exists an edge $e$ such that $d(e) = (x,y)$ or $d(e) = \{x,y\}$.  A directed loop graph is determined entirely by this relation; we may say that it *is* $V$ equipped with a binary relation.  Then a simple directed graph is $V$ equipped with an [[irreflexive relation]] (or equivalently a [[reflexive relation]]), and an undirected loop graph is $V$ equipped with a [[symmetric relation]].

A graph is __finite__ if $V$ and $E$ are both [[finite sets]].  Given a [[linear ordering]] of the vertices of a finite graph, its __adjacency matrix__ is a square [[matrix]] whose $(i,j)$th entry gives the number of edges $e$ between the $i$th and $j$th vertices or from the $i$th vertex to the $j$th vertex.  In the examples above where a graph is determined by a binary relation on $V$, then matrix multiplication gives composition of relations.


##  Morphisms of graphs

An __[[isomorphism]]__ from $G = (V,E,d)$ to $G' = (V',E',d')$ consists of a bijection $f: V \to V'$, together with a bijection from $E$ to $E'$ (also denoted $f$) such that $f$ commutes with $d$; that is, $d(f(e)) = (f(x),f(y))$ or $d(f(e)) = \{f(x),f(y)\}$ whenever $d(e) = (x,y)$ or $d(e) = \{x,y\}$ (as appropriate).  Two graphs $G$ and $G'$ are __isomorphic__ if there exists such an isomorphism.  Then finite graphs $G$ and $G'$ are isomorphic if and only if they have the same number of vertices and, for some ordering of their vertices, they have the same adjacency matrix.

A __[[morphism]]__ from $G$ to $G'$ should consist of functions $f: V \to V'$ and $f: E \to E'$ such that $f$ commutes with $d$.  However, some authors allow $f(e)$ to be undefined if $d(e) = (x,y)$ or $d(e) = \{x,y\}$ but $f(x) = f(y)$ when using a notion of graph where loops are forbidden.  The difference amounts to whether one interprets a simple graph as a special kind of loop graph in which no loops exist (the first kind of morphism) or in which each vertex has a unique loop (the second kind of morphism).  Either way, an isomorphism (as defined above) is precisely an invertible morphism.

+--{: .query}
[[Mike Shulman]]: Isn't there something backwards about defining "isomorphic" and _then_ "isomorphism" and _then_ "morphism"?  Doesn't the logic generally flow in the other direction (especially around here)?

[[David Roberts]]: well at least there's a historical precedent: this is how Bourbaki would have done it via structures :)

_Toby_:  That, and it\'s simpler to state the definition of 'isomorphic' than 'isomorphism'.  Not to mention that graph theorists, in my experience, tend to care much more about the property of being isomorphic than the structure of having an isomorphism.  As for 'morphism', there\'s even disagreement about what that should be; I think that my definition is the obvious correct one, but it disagrees with the one at, for example, [Wikipedia](http://en.wikipedia.org/wiki/graph) (although they had my definition in the past); both versions give the same notion of isomorphism, however.

[[Mike Shulman]]: Well, but we aren't graph theorists here, are we?  Isn't it okay for us to rephrase their definitions in the more categorically sensible order?

_Toby_:  I disagree that 'morphism' before 'isomorphism' is more categorially sensible.  That\'s like defining $\leq$ before $=$; sometimes useful, sometimes not.  Since I am getting ambiguity about morphisms in what I find online, I\'d prefer to do isomorphisms first.  With luck, I\'ll find some terminology to distinguish the two kinds of morphisms, or we can make up our own.

[[Mike Shulman]]: Okay, I'll accept that sometimes it makes sense to have isomorphisms before morphisms.  Certainly there are other situations in which the notion of isomorphism is more obvious, or less subject to debate, than the notion of morphism.  But I am happy that now "isomorphism" comes before "isomorphic."
=--

## References ##

* Harary, Frank (1969), _Graph Theory_, Addison-Wesley.
* Harary, Frank and Palmer, E.M. (1973), _Graphical Enumeration_, Academic Press.
* Lambek, J. and Scott, P.J. (1986), _Introduction to Higher Order Categorical Logic_, Cambridge University Press.


## Discussion ## {#talk}

Obsolete discussion may also be found in the History at [Version 24](http://ncatlab.org/nlab/revision/graph/24).

_Toby_:  OK, I\'ve completely redone the page above; [this](http://ncatlab.org/nlab/revision/graph/24) is how it looked before.  In particular, I am defining things case by case, rather than choice by choice ($8$ cases, rather than $3$ choices with $2$ options each).  Feedback please!

(One obvious possibility is that the best style of definition is a mixture of the two previous styles: doing undirected and directed graphs separately, but in each case listing the two choices ---loops or no loops, multiple edges or no multiple edges--- as I had done before.)

[[Eric]]: Ugh. I see that quite some discussion went on here and I'm late to the party. This page is not beautiful nor remotely $n$-categorical in my opinion. We already had a page that I was very happy with on [[directed graphs]].

Isn't there some way to state very simply:

>A **graph** is a functor...

Here is a humble attempt...

+-- {: .un_defn}
###### Definition

An **abstract graph** $X$ is a [[category]] with

* one object $X_0$, called the object of _vertices_;

* one object $X_1$, called the object of _edges_;

* one morphism $e : X_1 \to ???$, called
the _???_;

* together with identity morphisms.

A **graph** is a [[functor]] $G: X\to$ [[Set]].

More generally, a **graph [[internalization|in]] a category $C$** is a [[functor]] $G : X \to C$.
=--

_Toby_:  First, it depends on what kind of 'graph' you mean.

Let\'s take a simple undirected graph.  Then the answer is no, since the definition of a simple graph is not (despite the name) as simple as the definition of digraph (directed pseudograph).  Whereas a digraph consists of just $V$, $E$, and $d: E \to V^2$, a simple graph consists of $V$, $E$, and an injection $d: E \to \left({V \atop 2}\right)$.  The two problems here are: how do you say that $d$ is an injection? and how do you describe a function $E \to \left({V \atop 2}\right)$ in terms of functions among $V$ and $E$?  (A map $E \to V^2$ can be done; that\'s the same as two maps $E \to V$.)  You can describe these things more internally, of course (say by replacing 'injective function' with '[[monomorphism]]'), but there\'s no category $X$ such that a simple graph is precisely a functor from $X$ to $Set$.

In fact, the *only* kind of graph above that can be defined as a functor from $X$ to $Set$ for some fixed 'abstract general' category $X$ is directed pseudograph, the kind of graph discussed at [[digraph]].  Between that, and the fact that every strict category has an underlying digraph, it\'s no surprise that this is the sort of graph that category theorists like.  But it\'s not the sort of graph that graph theorists like so much!

It would be worth discussing what sort of graphs can be internalised in what sort of categories.  Those graphs that allow loops are easier; I think that I can do them!  For the graphs without loops, I haven\'t even decided what\'s the best way to phrase the definition in [[constructive mathematics]].  (Luckily it doesn\'t matter for finite graphs.)

_Roger Witte_ says

A looped directed graph is a set with a set with a binary relation.
A looped graph is a set with symmetric binary relation.
A directed graph is a set with an irreflexive binary relation.
A graph is a set with a symmetric irreflexive binary relation.

In each case this yields the correct definition of morphism and isomorphism

_Toby_:  But what is the definition of morphism for a set equipped with an irreflexive relation?  In many more structured examples (such as [[linear orders]] and [[apartness relations]]), at least, it is a function that *reflects* the relation instead of one that *preserves* the relation.

_Long time lurker, first time writer_: I don't think of a graph as a set with binary relation so much as I think of it as a "set with an adjacency structure." If one views graphs as adjacency lists, as a computer scientist would say, then the correct definition of morphism becomes obvious. (That said, I don't know how well this generalizes to multigraphs -- I tend to do actual graph theory and therefore work with simple graphs 99.9% of the time.)

All this makes me wonder if an approach along the following lines is possible: Define directed graphs in the broadest sense, as functors from the two-object, two-nontrivial-morphism category to the category of sets. As combinatorial objects, the obvious functor from the category of digraphs to the category of graphs is in fact a functor. Is there some analogous operation on the functor category of digraphs? (Apologies if some of the above doesn't make much sense, I'm writing this on way too little sleep.)

_Toby_:  I don\'t know the difference between 'a set with a (certain kind of) binary relation' and 'a set with an adjacency structure', at least not if an adjacency structure is a certain kind of binary relation.  (Although it might be a good idea to say something like that in the Idea section.)  Which defintion of morphism is obviously correct to you?

_Long time lurker_: I'm talking about the definition of graph homomorphism that graph theorists use, which I think agrees with the one given here at least for simple undirected graphs. And as for "binary relation" vs. "adjacency structure," I don't think there's any real mathematical difference, but it can pay off to think of a (directed loop) graph as a function $V \rightarrow 2^V$ rather than a subset of $V \times V$.

Obviously there are some issues with this; for one thing, I don't see an obvious way to abstract this in a category that doesn't have a subobject classifier. But philosophically, I'd like to propose that the key property of graphs is that their edges don't carry any information except for incidence -- so, e.g., when we take a category and forget about how arrows compose, we get a digraph. And this suggests that we should have some way of defining a graph without any reference to edges. 

[[!redirects undirected graph]]
[[!redirects graph theory]]
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

*  For a __simple graph__, a pair of vertices is a [[subset]] of $V$ of [[cardinality]] $2$, and we interpret edges as unordered pairs of vertices in a one-to-one way.  Thus a simple graph is given by $V$, $E$, and an [[injective function]] $d: E \hookrightarrow \left({V \atop 2}\right)$.  Among [[graph theory|graph theorists]], this is the standard meaning of 'graph' unless another is specified.

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

This is about on old version of the page, although much of it still applies.  Obsolete discussion may also be found in the History at Version 24.

+-- {: .query}
[[Mike Shulman]]: At [[latest changes]] Jon Awbrey said

> The page on graph has become too baroque to fix, but there needs to be a place to record the basic definitions of graph theory that are actually used by the larger schools of math folks who actually dare to call themselves graph theorists.

I propose that we try to fix this page, instead of replacing it.  Let's discuss what exactly may be wrong with it.  Keep in mind that, as has been pointed out elsewhere, the nLab is not Wikipedia.  We are not obligated to present a view of a given subject which is in line with those of the "larger schools of math folks" who practice that subject, and frequently we don't.  Our attitude towards [[foundations]] and [[set theory]], for instance, are quite different from those of many or most mathematicians who study those fields; everything we do is colored by our especial interest in, and focus on, category theory, higher category theory, and higher algebraic structures.

That being said, I do think it is important to be careful with *definitions*.  We may take a different approach than other people, but in general we shouldn't redefine their words---instead we should use different words.  (Our use of [[n-category]] to mean "weak $n$-category" is, I believe, a justified exception to this general principle.)  So if there are definitions on this page that are different from those commonly accepted in most of mathematics, there may be a good argument to fix them.

I do also agree that the exposition could use some work.  In particular, I don't like definitions of the form "An X is a Y such that Z.  By default, we also require that W, otherwise we call it a not-quite X."  I much prefer definitions of the form "An X is a Y such that Z and W.  If a Y satisfies Z but not W, we call it a not-quite X."  I suppose that other people may feel differently, though.

_Toby_:  Part of the problem with 'graph' is that, like 'ring', different schools take the default in different ways.  I find directed pseudomultigraphs much more interesting than simple graphs, which are simply sets equipped with one (ir)reflexive symmetric relation each.  We categorially minded people have (in an example dual to this one) mostly gotten everybody else to assume that rings are unital (although Zoran does not go along with this), although the algebraic geometers have so far not gotten the world at large to assume that rings are commutative.  (I don\'t even know who got people to assume that rings are associative; that may be lost in the mists of time.)  We may yet get people to allow graphs to be, by default, directed pseudomultigraphs.  Whether or not this ever happens, it\'s true that 'graph' among category theorists most often means that, not the more restrictive default meaning used by graph theorists.

I like [[graph theory]] as a place to discuss what 'graph theorists' actually talk about; I would also like to see it more like [[topology]], but that could come with time, and with additional pages to discuss the defined terms.  (So far only very basic terms appear, and that may be all that we need for now, but there are plenty that could be added.)

[[Mike Shulman]]: Why not use this page to discuss all the possible variations, along with information and links regarding who uses the terminology in which way?  I think that could be really useful.  Graph theorists and category theorists aren't the only ones; for instance, people writing about [[locally presentable categories]] often use "graph" to mean a set equipped with a binary relation, since the category of such graphs has a "universality" property among lp categories.  

[[Todd Trimble]]: Jon, would you like your own personal web at the nLab? I'm sure someone would be glad to set it up for you, and then you can define your terms just the way you like without outside interference. (By the way, I'm looking at some of your other entries. We seem to have a mutual interest in C.S. Peirce.) But I'm not sure you can expect to set up your private moorings on a public space like this. 

While I don't agree with some of the aesthetic choices on this page, I think we need to recognize and record the different senses of "graph" (but I personally don't feel a need to make one sense pre-eminent and make that fit other cases). The elaborate terminology I could do without, frankly; it would be enough to list the different senses in the spirit people use them, and just be very clear on other pages which sense is meant, with plain terminology like "directed graph", "undirected graph", and so on. 

[[Mike Shulman]]: "Fairly standard definitions" is not enough at the nLab.  We are not Wikipedia; we are a place for collaborative research, with a special place in our hearts for (higher) category theory.  Moreover just because you initiate a page, you can't expect to continue to "own" it; a wiki is all about building on other people's work.  But I still don't understand why you felt the need to retreat from this page at all; it still contains the same information, only now it is more explanatory and helps people to understand that terminology is used by different people in different ways.  Why is that something you want to avoid?  Why not join the rest of us and help clarify it and make it even better?

Todd, I assume by "elaborate terminology" you mean things like "directed pseudo multi graph"?  That is a bit of a mouthful.  I can see wanting to avoid that, but if it is terminology that graph theorists actually use (is it?) then it might be useful to include--although perhaps not quite so prominently. 

[[Todd Trimble]]: Yes, that's the kind of thing I meant. That particular phrase is not familiar to me, although if some (hopefully few!) graph theorists use it, perhaps the usage could be noted with more of a hint of ridicule or tongue in cheek -- these are very basic objects after all. 

From a logical point of view I think I see what Toby's after, but I'm against the idea of proliferating such fancy terms. I'd prefer keeping it real simple: say something like "graph can mean any of the following things", maybe qualified by a single adjective like 'simple', 'directed', 'undirected', etc., and more sociological discussion on which subcommunity uses what. Not pseudomultiwhatever, that sounds almost like a parody of math-talk. 

I'll join you in reiterating that no page here should be considered exempt from being edited by people after the first author, including for example [[graph theory]]. My own recommendation is that if some other page makes reference to one of the fairly standard notions of graph, then say just enough on which notion is meant to avoid any _likely_ confusions. (It's hard to spell this out legalistically, but I don't think confusion is very likely if for example someone writes "categories are monadic over graphs".) 

_Toby_:  I don\'t think that anybody says 'directed pseudomultigraph' if they can avoid it; category theorists, for example, usually just say 'graph' (or maybe 'directed graph' or 'digraph') for that, since it is their default notion.  But if you say those words to ordinary graph theorists, then they will *not* know what you mean; if you say 'directed pseudograph', then a lot of people will know what you mean, but not necessarily everybody.  The *only* unambiguous phrase that I know of is 'directed pseudomultigraph', but you would use this in the same way (or rather, a dual way) as Zoran uses 'commutative unital ring', which is to say that this is the kind of graph that you\'re discussing and that you will simply say 'graph' from now on.

Another way to say this, probably more common but also more wordy, is 'Our graphs will be directed, and they may have multiple edges and loops.'.  Personally, I would say just that if I were not including a definition of 'graph' myself, although I\'d probably add 'That is, they are _directed pseudomultigraphs_.'.  If I were giving my own definition, then I\'d probably say something like 'A __graph__ (more precisely, a _directed pseudomultigraph_) is ...'; in fact, I think that I have done this somewhere here, although maybe I only did that for 'tree' (by which I meant a directed rooted [[tree]]) at [[pure set]].

[[Todd Trimble]]: Sure, I already got that point, but _if I were_ talking to graph theorists, I'd just preface with that wordier expression, with full confidence that it's clear and everyone understands it. Anyway, we're not talking to graph theorists; we're really (so far) just itemizing different senses in which people use the word 'graph', and I'd rather not promote ugly jargon of somewhat limited usefulness. (I wonder whether most graph theorists even understand what it means, whereas 'commutative unital' and 'directed rooted' are good honest expressions everyone understands. But I'm prepared to be convinced that it is in fact widely understood by graph theorists, and if so, then there's a good chance my stance will soften.) 

Picking a nit perhaps: is 'multigraph' completely unambiguous? There's another sense I think where multigraphs are things that generate multicategories (i.e., spans from $X^*$ to $X$). 

To Jon: I'm sorry if something I said upset you, but I don't think anyone here is putting words in your mouth. You said: "I initiated this page with a particular purpose in mind, which was simply to anchor the fairly standard definitions that I'll be using throughout my other entries on site." But looking to the needs of _other_ users of the nLab, the fact that this entry has expanded its scope seems entirely fitting. I wouldn't say it was "appropriated" particularly; Toby was just being helpful and addressing community needs. Similarly, people may perceive a need to expand the entry on [[graph theory]] (I hope someone will!), and in ways no one anticipates yet. Anyway, my feeling is that the present page should serve your anchoring needs; are your graphs just "simple graphs" as defined above? 

_Toby_:  I don\'t disagree with rewriting this page to use more longer sentences composed of shorter words, or something like that.  (See also my reply to Mike\'s query about (un)directed graphs in the definition.)  I just think that we should also introduce the long words at some point too.  As for 'multigraph', since we\'ve already bowed to the graph theorists\' default by using 'digraph' at [[digraph]], how about 'multidigraph'? (not to be confused with 'directed multigraph', of course).

_Todd_: Ha ha! Well, I guess you can anticipate my reaction. While my own preference is just to disambiguate as local occasions may demand, I guess there's no harm in throwing it against the wall and seeing whether it sticks. Go for it, sez I. 

[[Mike Shulman]]: I think I like the idea of mostly using more words, and then just have a single list, towards the end maybe, of all the fancy terminology.  Especially since I gather from Toby's responses to my queries above that existing graph-theorists terminology is, IMHO, extremely haphazard.

_Toby_:  That discussion helps to make it clear that the terminology is inconsistent.  I\'m not sure what 'gobbleygeek' you mean that isn\'t used by graph theorists.  The author of your glossary is one of those who use 'pseudograph' to mean pseudomultigraph (I can\'t see what term they use for a simple pseudograph, which is not a concept that one wants to ignore, since they correspond to symmetric relations); otherwise, they use every term above.

_Toby_:  Then I really am throughly confused about what 'gobbleygeek' you are referring to!  *Nobody* here has suggested anything like 'FUUGSLOME'.  I use 'graph' almost exactly as you use it, but unfortunately this is not consistent, so I offer 'simple graph' as a way to make it precise.  (The only difference is that you want your graphs to be finite and ---if I am to believe your quotation--- inhabited.  Since those necessarily complicate the definition, I\'m not sure why, although I see the value of focussing on finite objects in combinatorics.)  The complicated terminology that others here object to are terms like 'directed pseudomultigraph'; your glossary uses merely 'directed pseudograph' for that, but that also is not consistent.  (I admit that 'pseudomultigraph' is very rare, since most people say either 'multigraph' or 'pseudograph', but these are ambiguous; using each of those for their simpler meanings gives a nice logical form of language.  I do like 'loop-graph' from your bibliography, although that would seem to work best to mean a simple pseudograph rather than a pseudomultigraph as the bibliography states.)  So yes, it is graph theorists who use inconsistent and complicated terminology, although I understand how this came about and offer my sympathies rather than my condemnation.
=--

+-- {: .standout}
_Toby_:  OK, I\'ve completely redone the page above; [this](http://ncatlab.org/nlab/revision/graph/24) is how it looked before.  In particular, I am defining things case by case, rather than choice by choice ($8$ cases, rather than $3$ choices with $2$ options each).  Feedback please!

(One obvious possibility is that the best style of definition is a mixture of the two previous styles: doing undirected and directed graphs separately, but in each case listing the two choices ---loops or no loops, multiple edges or no multiple edges--- as I had done before.)
=--

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


[[!redirects undirected graph]]
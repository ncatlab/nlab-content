#Idea#

A (directed) graph is a collection of edges which may stretch between (ordered) pairs of "points", called _vertices_.

A directed graph is like a [[category]] with units and composition forgotten. Indeed, a [[category]] is a directed graph with extra structure.  To formalize this idea, we say there is a [[forgetful functor]] 

$$U : Cat \to DiGraph$$

where [[DiGraph]] is the category of directed graphs and [[Cat]] is the category of small categories.  Moreover, this forgetful functor has a [[adjoint functor|left adjoint]] 

$$F : DiGraph \to Cat $$

sending each directed graph to the [[free functor|free]] category on that graph.  A free category on a graph is called a [[quiver]].

Compare also [[graph]].


#Definition#

The **walking directed graph** $X$ is the [[category]] with

* one object $X_0$, called the object of _vertices_;

* one object $X_1$, called the object of _edges_;

* two morphisms $s,t : X_1 \to X_0$, called
the _source_ and _target_;

* together with identity morphisms.

A **directed graph** is a [[functor]] $G: X\to$ [[Set]].

More generally, a **directed graph [[internalization|in]] a category $C$** is a [[functor]] $G : X \to C$.

The category of directed graphs in $C$, [[DiGraph]], is the [[functor category]] $C^{X}$, where:

* objects are functors $G: X \to C$,

* morphisms are [[natural transformation|natural transformations]] between such functors.

In the basic case $C = Set$, we call this category the category of [[presheaf|presheaves]] on $X^{op}$.  So: the category of directed graphs, [[DiGraph]], is the category of presheaves on the category $X^{op}$.


#Remarks#

Let $G_0 = G(X_0)$ and $G_1 = G(X_1)$.

* A directed graph in $C$ is a [[presheaf]] on $X^{op}$ with values in $C$.

* A directed graph is a [[globular set]] which is concentrated in the first two degrees.

* Directed graphs includes multigraphs, i.e. graphs with distinct edges $e,e'\in G_1$ such that $s(e) = s(e')$ and $t(e) = t(e')$, as well as loops, i.e. edges with $s(e) = t(e)$.

* A directed graph is **complete** if for any pair of vertices $v,v'\in G_0$, there are directed edges $e,e'\in G_1$ with $s(e) = v, t(e) = v'$ and $s(e') = v', t(e') = v$.


#See also#

* [[directed n-graph|Directed n-graph]]


#Discussion#

_[[Eric Forgy|Eric]] asks_: Given a small [[category]] $C$ whose set of objects is countable, I'm interested in finding the smallest [[directed graph]] $G$ such that its free category/quiver $F(G)$ is equivalent to $C$. Is that a standard construction? If so, what would it be called? Does that even make any sense?

[[John Baez]]: If I hand you a small category $C$, there's usually _no_ directed graph $G$ such that $F(G)$ is equivalent to $C$!  For example: suppose $C$ has one object and two morphisms.  (There are two categories of this sort; pick your favorite.)  Quivers are very special categories.

[[Eric Forgy|Eric]] continues: Here is one idea I had...

Consider the nerve $N(C)$ and set $G_0 = N(C)_0$.

Next, note that each non-degenerate $2$-simplex $\sigma\in N(C)_2$ is bounded by two distinct (non-identity) morphisms $f:x\to y$, $g:y\to z$ and the composite morphism $gf:x\to z$.

The set of directed edges $G_1$ can then be thought of as the subset of $N(C)_1$ consisting of only those morphisms that are not identities and are not composites.

Then, unless I'm mistaken, $C$ can be recovered from $G = (G_0,G_1)$ by

1. Inserting identity morphisms over each node and
1. Inserting composite morphisms into each path of length 2

In the language of [our paper](http://arxiv.org/abs/math-ph/0407005), I would say that $G$ has no loops and no intermediate edges. These kinds of graphs have some nice properties when you put a discrete calculus on them. 

I suspect that given a small (countable) category $C$ the smallest directed graph $G$ that can reproduce it has an interesting discrete calculus that should have something interesting to say about $C$.

_[[Urs Schreiber|Urs]] says_: You are effectively asking for
_free resolutions_ aka _cofibrant replacements_ of categories. There is not in general a 1-graph whose free category is equivalent to a given 1-category. But there may be "higher dimensional graphs" in a sense, such that this is true.

I'd like to reply to this in detail, because it is an interesting and important construction, but right now I need to do something else. But you can maybe get an impression by looking at the blog entry [Freely generated omega-Categories](http://golem.ph.utexas.edu/category/2008/10/freely_generated_categories.html).

_[[Eric Forgy|Eric]] says_: Great! Thanks for the references. I would find it to be very neat (and surprising) if any general category can be recovered this way, which is why I was specifically considering "countable" categories, where the set of objects does not form a continuum. In the continuum, you could imagine being able to sneak two infinitesimal composable morphisms onto any morphism so that all morphisms are effectively composites. When the objects do not form a continuum, you can imagine a set of "primordial" morphisms that cannot be written as composites of other morphisms.

It seems that when every morphism is a composite of other morphisms, i.e. there are no primordial morphisms, it would be difficult to find the directed graph I'm looking for. If higher degree edges somehow provide the magic ingredient, that would be neat.

_[[Eric Forgy|Eric]] says_: It seems what I was talking about might also be related to a [covering relation](http://en.wikipedia.org/wiki/Covering_relation). 

[[Eric]]: Oh! I see John Baez is (likely with the help of the Wizard) playing with the space time continuum again. Ok! So the example with one object and two morphisms is a good one. Thanks! Now I can ask a related question, given a [[preorder]] $C$, I'd like to find the smallest directed graph $G$ such that $F(G)\equiv C$. But this reminds me of a [Hasse diagram](http://en.wikipedia.org/wiki/Hasse_diagram). Hmm... (Edit: While John freely travels back and forth through time, I tend to relive past experience with no recollection. There is a discussion of Hasse diagrams at [[preorder]]. John suggests (if I understood correctly) _defining_ a Hasse diagram to be the smallest graph whose quiver reproduces the proset.

[[John Baez]]: Sorry, I was just trying to go back in time and nip that hope of yours in the bud.  Yes: I believe for a [[poset]] $C$ to have a Hasse diagram is the same as for it to have a directed graph $G$ with $F(G)\equiv C$, and then this directed graph is its Hasse diagram!  I think the Wikipedia article more or less says this, calling $C$ the 'transitive reduction' of $G$.

I've never heard of Hasse diagrams for preorders that aren't posets, so let's not worry about those.   Not all posets have Hasse diagram, either --- do they?  For example, the rational numbers with their usual ordering doesn't seem to have a Hasse diagram --- and they are, by the way, countable. 

The Wikipedia article seems content to discuss Hasse diagrams for finite posets; probably some sort of 'local finiteness' condition will suffice.  The rationals have infinitely many guys between any two different guys, so they're not 'locally finite'.

[[Eric]]: Ok. So this 'locally finite' restriction seems to put us into [[causets]], which is kind of neat. So maybe we should create a page [[Hasse diagram]]. A [[Hasse diagram]] of a [[causet]] $C$ is the smallest [[directed graph]] $G$ such that its [[quiver]] $F(G)$ is equivalent to $C$ (?)

_Toby_:  You don\'t need 'smallest' here; adding to $G$ will either add objects to $C$ or destroy that $C$ is a preorder.  (Along those lines, note that the only prosets that are ---up to isomorphism--- quivers are posets.  That explains why one mostly only talks about Hasse diagrams for posets.)  But note that 'Hasse diagram' is a fairly informal notion; I have had occasion to draw a Hasse diagram for the (non-antisymmetric, non-locally finite) proset of integers under divisibility, by cheating just slightly (doubling up the labels on the vertices to handle the lack of antisymmetry, some fudging with ellipses to handle the one breakdown of local finiteness, which is at $0$).


[[!redirects digraph]]
[[!redirects directed graphs]]
[[!redirects directed pseudograph]]
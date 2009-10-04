<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


#Idea#

* A category consists of a collection of things and binary relationships (or transitions) between them, such that these relationships can be combined and include the "identity" relationship "is the same as."

* A category is a [[directed graph]] with a rule saying how to _compose_ two edges that fit together to get a new edge.  Furthermore, each vertex has an edge starting and ending at that vertex, which acts as an identity for this composition.

* A category is a combinatorial model for a [[directed space]] -- a "directed [[homotopy 1-type]]" in some sense.  It has "points", called _objects_, and also directed "paths", or "processes" connecting these points, called _morphisms_.  There is a rule for how to compose paths; and for each object there is an identity path that starts and ends there.

* More precisely, a category consists of a collections of [[object|objects]] and
a collection of [[morphism|morphisms]].  Every morphism 
has a [[source]] object and a [[target]] object.  If $f$ is a morphism with $x$ as its source and $y$ as its target,
we write
$$f : x \to y$$
and we say that $f$ is a morphism from $x$ to $y$.  In a category, we can [[composition|compose]] a morphism $g : x \to y$ and a morphism $f : y \to z$ to get a morphism $f \circ g : x \to z$.  Composition is associative and satisfies the left and right unit laws.

The example to keep in mind is the category [[Set]], in which the objects are sets and a morphism $f : x \to y$ is a function from the set $x$ to the set $y$.  Here composition is the usual composition of functions.

For more background on and context for categories see

* [[category theory]].

#Definition#

A _category_ $C$ consists of 

* a [[collection]] $C_0$ of _objects_;

* a collection $C_1$ of _morphisms_ (or _arrows_);

* two maps $s, t : C_1 \to C_0$ called _source_ (or _domain_) and _target_ (or _codomain_);

  * one writes $f : x \to y$ if $s(f) = x$ and $t(f) = y$;

* a rule which assigns to any pair of morphisms $f$, $g$ such that $t(f) = s(g)$ their _composite_ morphism $g \circ f \in C_1$ (also  written $g f$ or sometimes $f;g$);

* a rule which assigns to each object $x$ a morphism $1_x$, the _identity_ morphism on $x$;

* such that the following properties are satisfied:

  * source and target are respected by composition: $s(g \circ f) = s(f)$ and $t(g\circ f) = t(g)$;

  * source and target are respected by identities: $s(1_x) = x$, $t(1_x) = x$;

  * composition is _associative_: $(h \circ g)\circ f = h\circ (g \circ f)$ whenever $t(f) = s(g)$ and $t(g) = s(h)$;

  * composition satisfies the _left and right unit laws_:
    given any morphism $f: x \to y$ we have $1_y \circ f = f = f \circ 1_x$. 

People often write $hom(x,y)$, $hom_C(x,y)$, or $C(x,y)$ for the collection of morphisms $f : x \to y$; the latter two have the advantage of making clear which category is being discussed.  People also often write $x \in C$ instead of $x \in C_0$ as a short way to indicate that $x$ is an object of $C$.  Also, some people write $Ob(C)$ and $Mor(C)$ instead of $C_0$ and $C_1$.

#Examples#

The classic example is [[Set]], the category with sets as objects and functions as morphisms, and the usual composition of functions as composition.  Here are some other famous examples, which arise as variations on this theme:

* [[Vect]] - [[vector space]]s as objects, linear maps as morphisms.

* [[Grp]] - [[group]]s as objects, homomorphisms as morphisms.

* [[Top]] - [[topological space]]s as objects, continuous functions as morphisms.

* [[Diff]] - smooth [[manifold]]s as objects, smooth maps as morphisms.

* [[Ring]] - [[ring]]s as objects, ring homomorphisms as morphisms.

Note that in all these cases the morphisms are actually special sorts of functions.  That need not be the case in general!

These classic examples are the original motivation for the term "category": all of the above categories encapsulate one "kind of mathematical structure".  These are often called "concrete" categories (that term also has a [[concrete category|technical definition]] that these examples all satisfy).  But just as widespread in applications as these categorization examples of categories are are other categories (often "[[small category|small]]" ones) which, roughly, model something like _states_ and _processes_ of some system.

* **Poset** A [[partial order|poset]] can be thought of as a category with its elements as objects and one morphism in each $hom(x,y)$ if $x$ is less than or equal to $y$, but none otherwise.  

* **Group** A [[group]] is just a category where there's one object and all the morphisms have inverses - we call the morphisms "elements" of the group.  This may seem weird, but it's actually a very useful viewpoint. Here's another way to say it: _A group is a [[groupoid]] with a single object_.

* **Monoid** More generally, a [[monoid]] is a category with a single object. In fact, this is one way to motivate the concept of categories: categories are the [[horizontal categorification|many object version]] of monoids.

* **Quiver** A [[quiver]] is a free category on a [[directed graph]].  Given a directed graph $G$ with collection of vertices $G_0$ and collection of edges $G_1$, there is the _[[free functor|free]] category_ $F(G)$ on the graph whose collection of objects coincides with the collection of vertices, and whose collection of morphisms consists of finite sequences of edges in $G_1$ that fit together head-to-tail. The composition operation in this free category is the concatenation of sequences of edges.

#Size Issues#

The attentive reader will note that we said a category has a 'collection' of objects and a 'collection' of morphisms.  A category is said to be [[small category|small]] if these collections are sets &mdash; as opposed to [[proper class|proper classes]], for example.  (The alternatives depend on ones [[foundations|foundations for mathematics]].)

Similarly, a category is [[locally small category|locally small]] if $hom(x,y)$ is a set for every pair of objects $x,y$ in that category.  The above examples of "concrete" categories are all locally small but not small (unless one restricts their objects in some way).

#Alternate Definitions#

The definition of a category can be rephrased in different mostly-equivalent ways.  For example, instead of taking as given a collection $C_0$ of objects and a collection $C_1$ of morphisms, one can take as given a collection $C_0$ of objects, together with for each pair $x,y$ of objects a collection $hom_C(x,y)$ of morphisms from $x$ to $y$.  (If each collection $hom_C(x,y)$ is a _set_, then this latter version defines only a "locally small category," as above.)  The first definition generalizes naturally to [[internal categories]], while the second generalizes naturally to [[enriched categories]].

It is also possible to define a category in terms of only _one_ collection (the collection of arrows); see [[single-sorted definition of a category]].  This is sometimes convenient for technical reasons.

#Database# 

We will build a [[database of categories]] listing well-known categories (with links to articles on these categories, if such articles) and some of their properties.  Right now this is just beginning.

#Literature#

Let's include a lot of nice online introductions. Here is a start:

* Jaap van Oosten, [Basic category theory] (http://www.math.uu.nl/people/jvoosten/syllabi/catsmoeder.pdf).

* Andrea Schalk and H. Simmons, [An introduction to category theory in four easy movements](http://www.cs.man.ac.uk/~hsimmons/BOOKS/CatTheory.pdf), notes for a course offered as part of the MSc. in Mathematical Logic, Manchester University.

* Daniele Turim, [Category theory lecture notes](http://www.dcs.ed.ac.uk/home/dt/CT/categories.pdf), 1996-2001.  Based on Mac Lane's book (1998).

* A. Martini, H. Ehrig, and D. Nunes, [Elements of basic category theory](http://citeseer.ist.psu.edu/martini96element.html), Technical Report 96-5, Technical University Berlin.

[[!redirects categories]]
[[!redirects Category]]
[[!redirects Categories]]
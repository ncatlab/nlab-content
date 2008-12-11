#Idea#

* A (small) category is a [[directed graph]] with a rule for how to _compose_ two edges that fit together to get a new edge and for each vertex an edge starting and ending there which behaves as an identity under this composition.

* A category is a combinatorial model for a directed space: there are "points", called _objects_, and there are directed "paths", or "processes" connecting these points: called _morphisms_; and there is a rule for how to compose morphisms that end and start at a given object; and for each object there is the trivial process, which does nothing.

* More precisely, a category consists of a collections of [[object]]s and
a collection of [[morphism|morphisms]].  Every morphism 
has a [[source]] object and a [[target]] object.  If $f$ is a morphism with $x$ as its source and $y$ as its target,
we write

$$f : x \to y$$

and we say that $f$ is a morphism from $x$ to $y$.  In a category, we can [[composition|compose]] a morphism $g : x \to y$ and a morphism $f : x \to y$ to get a morphism $f g : x \to z$.  Composition is associative and satisfies the left and right unit laws.

The example to keep in mind is the category [[Set]], in which the objects are sets and a morphism $f : x \to y$ is a function from the set $x$ to the set $y$.  Here composition is the usual composition of functions.

#Definition#

A _category_ $C$ consist of 

* a collection $C_0$ of _objects_;

* a collection $C_1$ of _morphisms_;

* two maps $s, t : C_1 \to C_0$ called _source_ and _target_;

  * one writes $f : x \to y$ if $s(f) = x$ and $t(f) = y$;

* a rule which assigns to any pair of morphisms $f$, $g$ such that $t(f) = s(g)$ their _composite_ morphism
$g \circ f \in C_1$;

* a rule which assigns to each object $x$ a morphism $1_x$, the _identity_ morphism on $x$;

* such that the following properties are satisfied:

  * source and target are respected by composition: $s(g \circ f) = s(f)$ and $t(g\circ f) = t(g)$;

  * source and target are respected by identities: $s(1_x) = x$, $t(1_x) = x$;

  * composition is _associative_: $(f \circ g)\circ h = f\circ (g \circ h)$ whenever either side is defined;

* composition satisfies the _left and right unit laws_:
given any morphism $f: x \to y$ we have $1_y \circ f = f = f \circ 1_y$. 


#Examples#

The classic example is [[Set]], the category with sets as objects and functions as morphisms, and the usual composition of functions as composition.  Here are some other famous examples, which arise as variations on this theme:

* [[Vect]] - vector spaces as objects, linear maps as morphisms.

* [[Grp]] - groups as objects, homomorphisms as morphisms.

* [[Top]] - topological spaces as objects, continuous functions as morphisms.

* [[Diff]] - smooth manifolds as objects, smooth maps as morphisms.

* [[Ring]] - rings as objects, ring homomorphisms as morphisms.

Note that in all these cases the morphisms are actually  special sorts of functions.  That need not be the case in general!  

These classic examples are the original motivation for the term "category": all of the above categories encapsulate one "kind of mathematical structure". But just as widespread in applications as these categorization examples of categories are are other categories (often "[[internalization|small]]" ones) which, roughly, model something like _states_ and _processes_ of some system.

* **Free category on a directed graph**. Given a [[directed graph]] $G$ with collection of vertices $G_0$ and collection of egdes $G_1$, there is the _free category_ $F(G)$ on the graph whose collection of objects coincides with the collection of vertices, and whose collection of morphisms consists of finite sequences of edges in $G_1$ that fit together head-to-tail. The composition operation in this free category is the concatenation of sequences of edges.

* **Poset** A [[poset]] can be thought of as a category with its elements as objects and one morphism in each $hom(x,y)$ if $x$ is less than or equal to $y$, but none otherwise.  

* **Group** A [[group]] is just a category where there's one object and all the morphisms have inverses - we call the morphisms "elements" of the group.  This may seem weird, but it's actually a very useful viewpoint. One can think of this as: _A group if a [[groupoid]] with a single object_.

* **Monoid.** More generally, a [[monoid]] is a category with a single object. In fact, this is one way to motivate the concept of categories: categories are the [[horizontal categorification|many object version]] of monoids.



There is much more to say... it might not be terrible to copy the Wikipedia article on categories and rework it to suit our purposes.

#Literature#

Let's include a lot of nice online introductions. Here is a start:

* Jaap van Oosten, _Basic category theory_ ([pdf](http://www.math.uu.nl/people/jvoosten/syllabi/catsmoeder.pdf))


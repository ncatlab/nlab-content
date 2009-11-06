# Definition

A **double category** is an [[n-fold category]] for $n=2$, i.e., an [[internal category]] in [[Cat]].  Similarly, a **double groupoid** is an internal [[groupoid]] in [[Grpd]].

However, these definitions obscure the essential symmetry of the definition.  We think of a double category $D_1 \rightrightarrows D_0$ as having

* *objects*: the objects  of $D_0$
* *vertical arrows*: the morphisms of $D_0$
* *horizontal arrows*: the objects of $D_1$
* *squares* or *2-cells*: the morphisms of $D_0$.

The vertical and horizontal arrows both form categories (the "edge categories"), and the squares have two category structures which respect the edge category structures.  In particular, the *transpose* of a double category, which switches the vertical and horizontal arrows, is again a double category.


# Examples

* If $C$ is a 2-category, we have a double category $Sq(C)$ whose objects are those of $C$, both of whose types of morphisms are the morphisms in $C$, and whose squares are 2-cells in $C$ with their source and target both decomposed as a composite of two morphisms.  (These squares are sometimes called *quintets* $(\alpha,f,g,h,k)$ where $\alpha\colon f g \to h k$.)

  (In this example, the two edge categories coincide.  Double categories with this property are called **edge-symmetric**.)

* Since any 1-category can be regarded as a 2-category with only identity 2-cells, for any 1-category $C$ we have a double category $Sq(C)$ whose squares are the commutative squares in $C$.  

* Any 2-category can also be made into a double category in two more ways, by defining the vertical or horizontal morphisms to consist only of identities.  In this way 2-categories can be considered as a special case of double categories.

  In the other direction, any double category has two underlying 2-categories, consisting of the objects, the vertical (resp. horizontal) arrows, and the squares whose horizontal-arrow (resp. vertical-arrow) source and target are identities.  We call these its **vertical 2-category** and **horizontal 2-category**.

* Finally, we can also make a 2-category $C$ into a double category with the same objects, whose horizontal arrows are the morphisms of $C$, whose vertical arrows are the [[adjunctions]] in $C$, and whose 2-cells are [[mate]]-pairs of 2-cells in $C$.  Naturality properties of the mate correspondence are concisely expressed by the existence of this double category.

* There is a double category $Prof$ whose objects are (small) categories, whose vertical arrows are functors, whose horizontal arrows are [[profunctors]], and whose squares are natural transformations.  This double category is in fact an [[equipment]], as are many other similar ones (such as for [[enriched categories]]).

* Any topological space has a "homotopy double groupoid" whose objects are points, whose morphisms of both types are paths (so it is edge-symmetric), and whose 2-cells are homotopies.

* There is a double category $MonCat$ whose objects are [[monoidal categories]], whose horizontal arrows are [[lax monoidal functors]], whose vertical arrows are [[colax monoidal functors]], and whose 2-cells are generalized [[monoidal transformations]].  An analogous double category can be constructed involving the algebras for any [[2-monad]].

* There is a double category $Model$ whose objects are [[model categories]], whose horizontal arrows are right [[Quillen functors]], whose vertical arrows are left Quillen functors, and whose 2-cells are arbitrary natural transformations.  Passage to [[derived functors]] is a functor on this double category.


# Weakenings

An internal category in the 1-category $Cat$ is a *strict* double category, all of whose composition operations are strictly associative and unital.  However, since a double category is a 2-dimensional structure, it makes sense to allow these compositions to be weak as well.

A **pseudo double category** is a weakly internal category in the 2-category $Cat$.  Here "weakly internal category" in a 2-category is interpreted as being associative and unital up to coherent isomorphism, just as a [[bicategory]] is a "weakly enriched category."  This makes the composition in one direction weak, but the composition in the other direction remains strict (it is the composition in the objects of $Cat$ that make up the pseudo double category).  Many naturally occurring examples, such as $Prof$, are pseudo double categories.

Finally, a **[[double bicategory]]** is one way to define a double category which is "weak in both directions."


#References#

* R. Brown and C.B. Spencer, Double groupoids and crossed
modules, Cah.  Top. G\'{e}om. Diff. 17 (1976) 343--362.

* Jeffrey C. Morton, [Double Bicategories and Double Cospans](http://arxiv.org/abs/math/0611930)

* Tom Fiore, [Double Categories and
Pseudo Algebras](http://www.math.uchicago.edu/~fiore/1/fiorefolding.pdf) 

* John C. Baez, [An Introduction to n-Categories](http://arxiv.org/abs/q-alg/9705009)

* Catsters, Double Categories ([YouTube](http://www.youtube.com/watch?v=kiCZiSA2W3Q&feature=channel_page))

[[!redirects double categories]]
[[!redirects double groupoid]]
[[!redirects double groupoids]]

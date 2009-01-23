#Idea#

Intuitively speaking, a braided monoidal category is a category with a tensor product and an isomorphism called the 'braiding' which lets us 'switch' two objects in a tensor product like $x \otimes y$.

#Definition#

A **braided monoidal category** is a [[monoidal category]] equipped with a natural isomorphism
$$ B_{x,y} : x \otimes y \to y \otimes x $$
called the _braiding_, which must satisfy two axioms called the 'hexagon identities'.  

+--{.query}
Someone please put these diagrams in here!
=--

More tersely, we could define a braided monoidal category to be a [[tricategory]] with one object and one 1-cell.  However, unlike the definition of a monoidal category as a [[bicategory]] with one object, this identification is not trivial; a doubly-degenerate tricategory is literally a category with two monoidal structures that interchange up to isomorphism.  It requires the [[Eckmann-Hilton argument]] to deduce an equivalence with braided monoidal categories.

#Basic Facts#

There is a [[strict 2-category]] BrMonCat with:

* braided monoidal categories as objects,
* [[braided monoidal functor|braided monoidal functors]] as morphisms, 
* [[braided monoidal natural transformation|braided monoidal natural transformations]] as 2-morphisms.

For definitions of all these concepts, see:

* John Baez, [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

For an elementary introduction to braided monoidal categories using string diagrams, see:

* John Baez and Mike Stay, [Physics, topology, logic and computation: a Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf).

+--{.query}
Eventually we should include all these diagrams here!  Can anyone help out?
=--
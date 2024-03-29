# Intercategories

* table of contents
{:toc}

## Idea

An *intercategory* is a particular sort of [[triple category]] that is pseudo in some ways and lax in others.  Many different kinds of higher-categorical structures can be viewed as, or give rise to, intercategories.  In particular, an intercategory can be viewed as a [[double category]] with "extra strictness/weakness information" given by the third direction.

## Definition

The data of an intercategory is like that of a triple category: it has

* objects
* three kinds of arrows, called *transversal*, *vertical*, and *horizontal*
* three kinds of square 2-cells, called *vertical* (those having transversal and vertical arrows on their boundaries), *horizontal* (those having transversal and horizontal arrows on their boundaries), and *basic* (those having horizontal and vertical arrows on their boundaries)
* cubes

All three kinds of arrows can be composed in the obvious way, all three kinds of 2-cell can be composed like in a double category, and cubes can be composed like in a triple category.  Composition of transversal arrows, and transversal composition of horizontal and vertical squares and cubes, is strictly associative and unital.  Horizontal and vertical composition is associative and unital up to coherent transversal isomorphism, as in a bicategory.  In particular, the vertical cells and the horizontal cells each form the cells in a pseudo double category of the usual sort.  Finally, composition of basic cells in the vertical and horizontal directions only satisfies the "interchange law" laxly (up to a not-necessarily-invertible comparison cell).

For a precise definition, see the references.

## Examples

* Of course, any strict [[triple category]] can be regarded as an intercategory.

* A Verity [[double bicategory]] can be regarded as an intercategory in which the only transversal arrows are identities, and the horizontal and vertical cells have basic [[companions]] and [[conjoints]].  This includes in particular the case of [[quintets]] in a [[bicategory]].

* A [[locally cubical bicategory]] (a bicategory enriched over pseudo double categories) can be regarded as an intercategory with only identity transversal arrows, vertical arrows, and vertical cells.  The horizontal arrows are the objects of the hom-double-categories, the horizontal and basic cells are their arrows, and the cubes are their squares.  This includes in particular [[monoidal double categories]] as the special case where there is only one object.

* A [[duoidal category]] can be regarded as an intercategory with one object, one arrow of each sort, and one vertical and one horizontal cell.  The objects of the duoidal category are the basic cells and its morphisms are the cubes; the two tensor products are the horizontal and vertical compositions.

* A [[Gray-category]] gives rise to an intercategory of [[quintets]], whose objects are the objects of the Gray-category, only identity transversal arrows, vertical cells, and horizontal cells, whose horizontal *and* vertical arrows are those of the Gray-category, whose basic cells are "quintet" 2-cells in the Gray-category, and whose cubes are the 3-cells.  Because interchange is lax, this includes even categories enriched over Gray's lax" tensor product, in addition to the "pseudo" one that is usually used to define Gray-categories.

## References

* [[Marco Grandis]], [[Robert Paré]], *Intercategories*, [arXiv](http://arxiv.org/abs/1412.0144), [TAC](http://tac.mta.ca/tac/volumes/30/38/30-38abs.html)

* [[Marco Grandis]], [[Robert Paré]], *Intercategories: A framework for three-dimensional category theory*, [doi](https://doi.org/10.1016/j.jpaa.2016.08.002), [arXiv](http://arxiv.org/abs/1412.0212)

[[!redirects intercategories]]

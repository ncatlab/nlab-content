#Idea#

A concept of a _2-vector space_ is supposed to be a [[vertical categorification|categorification]] of the concept of a vector space. As usual, there are various different concepts of 2-vector spaces, all of them useful and relevant in different contexts.

Most definitions of 2-vector spaces used in the literature are special cases of the idea that in analogy to how a vector space can be regarded as a [[module]] over the ground field $k$, a 2-vector space $W$ should be a [[category]] which is a [[monoidal category module]] with some nice properties (such as being an abelian category) over a suitable [[monoidal category]] $C$ which plays the role of the categorified ground field. There is then an obvious [[bicategory]] of such module categories.


#Examples

## $C = $ [[closed monoidal category]]

## $C = Disc(k)$

The ground field itself may be regarded as a [[discrete category]] which is then clearly a [[monoidal category]]. A $Disc(k)$-module category is a category whose space of objects and space of morphisms are both $k$-modules -- ordinary vector spaces! -- such that all structure morphisms (source, target, identity, composition) respect the $k$-action -- hence are linear maps. This are categories [[internal category|internal to]] [[Vect]]_k which are equivalent to chain complexes of vector spaces concentrated in degree 0 and 1.

Categories internal to [[Vect]] were explicitly described from the perspective of 2-vector spaces in 

* John C. Baez and Alissa S. Crans, _Higher-Dimensional Algebra VI: Lie 2-Algebras_ ([tac](http://www.tac.mta.ca/tac/volumes/12/15/12-15abs.html)).


## $C = Vect_k$

General [[monoidal category modules]] over $C = Vect$ are hard to get under control, but various more well-behaved  sub-[[bicategory|bicategories]] of all $Vect$-module categories are well studied and have found many applications.



## $C = $ modular tensor category


#Remark on the different notions of 2-vector spaces#

As the above list shows, there are 2-vector spaces of very different kind. There is not <em>the</em> notion of 2-vector space which is the universal right answer. Different notions of vector spaces are applicable and useful in different situations. 
This can be regarded as nothing but a more pronounced incarnation of the fact that already ordinary vector space appear in different flavors which are useful in different situations (real vector spaces, complex vector spaces, etc.)

For instance $Disc(k)$-module categories are crucial for higher [[Lie theory]] but 2-bundles with fibers $Disc(k)$-module categories are comparatively boring as far as general 2-bundles go, as they are essentially complexes of ordinary vector bundles.


#Idea#

An **fc-multicategory** is a common generalization of a [[monoidal category]], a [[bicategory]], a [[double category]], and a [[multicategory]].  It contains:

* objects
* vertical arrows, which form a category
* horizontal arrows, which do not have identities or composites, and
* 2-cells which have
  * a horizontal source and target, which are vertical arrows,
  * a vertical target, which is a horizontal arrow, and
  * a vertical source, which is a composable string of horizontal arrows.

fc-multicategories are related to double categories precisely as ordinary multicategories are related to monoidal categories (see [[tensor product]]).  They can be viewed as "the natural place in which to enrich categories."

#Definition#

An fc-multicategory is a $T$-multicategory, in the sense of Leinster, for the monad $T$ on [[directed graph|directed graphs]] whose algebras are categories.  The "fc" is a name for this monad $T$ which stands for "free-category."

#References#

* Tom Leinster, _Higher Operads, Higher Categories_

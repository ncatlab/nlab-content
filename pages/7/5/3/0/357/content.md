#Idea#

An **fc-multicategory** is a common generalization of a [[monoidal category]], a [[bicategory]], a [[double category]], and a [[multicategory]].  It contains:

* objects
* vertical arrows, which form a category
* horizontal arrows, which do not have identities or composites, and
* 2-cells which have
  * a horizontal source and target, which are vertical arrows,
  * a vertical target, which is a horizontal arrow, and
  * a vertical source, which is a composable string of horizontal arrows.

fc-multicategories are related to double categories precisely as ordinary multicategories are related to monoidal categories (see [[tensor product]]).  For this reason, [[Mike Shulman]] and [[Geoff Cruttwell]] have proposed to call them instead **virtual double categories**.

#Definition#

An fc-multicategory is a $T$-[[generalized multicategory|multicategory]], in the sense of Leinster, for the monad $T$ on [[directed graph|directed graphs]] whose algebras are categories.  The "fc" is a name for this monad $T$ which stands for "free-category."

# Enriching categories #

fc-multicategories can be viewed as "the natural place in which to enrich categories."  Specifically, for any set $A$, there is an fc-multicategory $A_{ch}$ which has $A$ as its objects, only identity vertical arrows, exactly one horizontal arrow from every object to every other object, and exactly one 2-cell in every possible niche.  For any other fc-multicategory $W$, a functor $A_{ch}\to W$ of fc-multicategories is the same as a $W$-enriched category with object set $A$.

#References#

* [[Tom Leinster]], _Higher Operads, Higher Categories_
* [[Mike Shulman]] and [[Geoff Cruttwell]], _A unified framework for generalized multicategories_, [arXiv:0907.2460](http://arxiv.org/abs/0907.2460)

[[!redirects virtual double category]]
[[!redirects fc-multicategories]]
[[!redirects virtual double categories]]

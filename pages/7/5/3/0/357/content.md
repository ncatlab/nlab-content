#Idea#

A **virtual double category** is a common generalization of a [[monoidal category]], a [[bicategory]], a [[double category]], and a [[multicategory]].  It contains:

* objects
* vertical arrows, which form a category
* horizontal arrows, which do not have identities or composites, and
* 2-cells which have
  * a horizontal source and target, which are vertical arrows,
  * a vertical target, which is a horizontal arrow, and
  * a vertical source, which is a composable string of horizontal arrows.

Virtual double categories are related to double categories precisely as ordinary multicategories are related to monoidal categories (see [[tensor product]]).

# Definition #

A virtual double category can be defined in two equivalent ways:

* It is a $T$-[[generalized multicategory|multicategory]], in the sense of Leinster, relative to the monad $T$ on [[directed graph|directed graphs]] whose algebras are categories.  For this reason, Leinster originally called them **fc-multicategories**, where "fc" is a name for this monad $T$ which stands for "free-category."

* It is a generalized multicategory, in the sense of Hermida, Cruttwell-Shulman, and others, relative to the monad $T$ on graphs-internal-to-Cat whose algebras are double categories.  This is the origin of the name "virtual double category," in line with the general terminology "virtual $T$-algebra" of Cruttwell-Shulman for such generalized multicategories.


# Enriching categories #

Virtual double categories can be viewed as "the natural place in which to enrich categories."  Specifically, for any set $A$, there is a virtual double category $A_{ch}$ which has $A$ as its objects, only identity vertical arrows, exactly one horizontal arrow from every object to every other object, and exactly one 2-cell in every possible niche.  For any other virtual double category $W$, a functor $A_{ch}\to W$ of virtual double categories is the same as a $W$-enriched category with object set $A$.

#References#

* [[Tom Leinster]], _Higher Operads, Higher Categories_
* [[Geoff Cruttwell]] and [[Mike Shulman]], _A unified framework for generalized multicategories_, [arXiv:0907.2460](http://arxiv.org/abs/0907.2460)

[[!redirects virtual double categories]]
[[!redirects fc-multicategory]]
[[!redirects fc-multicategories]]

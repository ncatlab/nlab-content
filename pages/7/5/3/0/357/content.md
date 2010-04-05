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

There are notions of **functor**, **transformation**, and **profunctor** between virtual double categories.  The neatest way to define all of these notions at once is to use the general framework of [[generalized multicategories]]: from the monad $fc$ on the [[virtual equipment]] $Span = Span(Set)$ we can construct a new virtual equipment $vDblProf = KMod(Span,fc)$ whose objects are virtual double categories, whose arrows are functors between them, whose proarrows are profunctors between them, and whose cells are transformations.

The notion of functor is also easy to define explictly, as is the notion of transformation once you realize that its components must consist of a vertical arrow (those that can be composed) for each object, and a cell for each horizontal arrow (just as in a vertical transformation between [[double categories]]).  The profunctors between virtual double categories are a similar "virtualization" of the notion of [[double profunctor]] between double categories.


# Enriching categories #

Virtual double categories can be viewed as "the natural place in which to enrich categories."  Specifically, for any set $A$, there is a virtual double category $A_{ch}$ which has $A$ as its objects, only identity vertical arrows, exactly one horizontal arrow from every object to every other object, and exactly one 2-cell in every possible niche.  For any other virtual double category $W$, a functor $A_{ch}\to W$ of virtual double categories is the same as a $W$-enriched category with object set $A$.


# Monoids and modules #

...


#References#

* [[Tom Leinster]], _Higher Operads, Higher Categories_, [link](http://www.maths.gla.ac.uk/~tl/book.html), [arXiv:0305049](http://arxiv.org/abs/math/0305049)
* [[Geoff Cruttwell]] and [[Mike Shulman]], _A unified framework for generalized multicategories_, [arXiv:0907.2460](http://arxiv.org/abs/0907.2460)

[[!redirects virtual double categories]]
[[!redirects fc-multicategory]]
[[!redirects fc-multicategories]]


# Contents
* tic
{:toc}

## Idea

A **double profunctor** is an appropriate notion of [[profunctor]] between [[double categories]].

## Definition

A double profunctor can be defined in several equivalent ways.  In each case, however, we must choose whether to regard the "vertical" or the "horizontal" direction as primary; applying transposes results in a different notion of double profunctor.

### As internal profunctors in Cat

Since a (strict) double category is an [[internal category]] in [[Cat]], it makes sense to define a **double profunctor** to be an internal profunctor in $Cat$.  Thus, if $C$ and $D$ are double categories, a double profunctor $C &#8696; D$ consists of a span $C_0 \leftarrow H \to D_0$ in $Cat$, together with actions $C_1 \times_{C_0} H \to H$ and $H\times_{D_0} D \to H$ which are associative and commute with each other.

### As collages in DblCat

Another natural way to define a double profunctor is in terms of its [[collage]].  From this perspective, a double profunctor $C &#8696; D$ consists of a double category $H$, together with double functors $C\to H$ and $D\to H$ such that:

1. The images of $C$ and $D$ in $H$ are disjoint.
1. The induced functor $C\sqcup D\to H$ is bijective on objects and vertical arrows.
1. Each functor $C\to H$ and $D\to H$ is fully faithful on horizontal arrows and squares.
1. There are no horizontal arrows in $H$ from an object of $C$ to an object of $D$, and therefore also no squares whose horizontal source is a vertical arrow in $C$ and whose horizontal target is a vertical arrow in $D$.


### Explicit definition

Each of these definitions can be unraveled to give a more explicit definition, and thereby shown to be the same.

(it would be nice to do this)


## Composites

Composition of double profunctors can (maybe?) be defined, but it is not in general associative.  From the internal-category point of view, this is because [[pullbacks]] in $Cat$ do not preserve [[coequalizers]].  Thus, double categories and double profunctors do not form a [[bicategory]].  They do, however, form a [[virtual double category]], as do internal categories in any category with pullbacks.

[[!redirects double profunctors]]


# Contravariant functors
* table of contents
{: toc}

## Idea

A contravariant functor is like a [[functor]] but it reverses the directions of the [[morphisms]].  (Between [[groupoids]], contravariant functors are essentially the same as functors.)


## Between categories

A **contravariant functor** $F$ from a [[category]] $C$ to a category $D$ is simply a [[functor]] from the [[opposite category]] $C^op$ to $D$.


To emphasize that one means a functor $C \to D$ as stated and _not_ as a functor $C^{op} \to D$ one sometimes says **covariant functor** when referring to non-contravariant functors, for emphasis. 

Equivalently, a contravariant functor from $C$ to $D$ may be thought of as a functor from $C$ to $D^op$, but the version above generalises better to functors of many variables. 

Also notice that while the objects of the [[functor category]] $[C^{op}, D]$ are in canonical bijection with those in the functor category $[C, D^{op}]$ (both are contravariant functors from $C$ to $D$), the morphisms in the two functor categories are in general different, as

$$
  [C^{op}, D] \simeq [C, D^{op}]^{op}
  \,.
$$

This matters when discussing a [[natural transformation]] from one contravariant functor to another.

## Between higher categories

Since [[n-categories]] (and also [[(infinity,n)-categories]]) have $2^n$ different kinds of [[opposite category]] depending on which of the $k$-morphisms are reversed for $1\le k\le n$ (see for instance [[opposite 2-category]]), they also have $2^n$ different kinds of "contravariant functor".

## Abstractly

Categories, covariant functors, and [[natural transformations]] form a [[2-category]] [[Cat]].  To include the contravariant functors as well, we can equip $Cat$ with a [[duality involution]], or we can generalize to a [[2-category with contravariance]], or some more general structure that also includes [[extranatural transformations]] or [[dinatural transformations]].  There could also be higher-categorical versions, such as a [[3-category with contravariance]].

## Related concepts

[[!include notions of pullback -- contents]]


[[!redirects contravariant functor]]
[[!redirects contravariant functors]]

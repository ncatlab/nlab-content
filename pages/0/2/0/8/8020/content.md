
# Concrete and abstract structures
* table of contents
{: toc}

## Idea

Many concepts from ordinary mathematics originally develop in the course of a particular application, such that the original definition of the concept is tied to that application.  The modern definition (typically some kind of [[structured set]]) is then obtained by a process of abstraction.  Sometimes this history is remembered in the terminology, with the original notion being called _concrete_ and the later notion called _abstract_.

It then becomes possible to define the concrete notion in terms of the abstract one (so giving an *abstract* definition of the original *concrete* concept); usually, a concrete structure is then an abstract structure equipped with some [[extra stuff]].  Sometimes there is also a [[representation theorem]] showing that every abstract structure arises from some concrete structure (but sometimes this is false).


## Examples

### Groups

Given a [[set]] $X$, a __permutation group__ on $X$ is a [[subset]] of the set of [[permutations]] of $X$ that includes the [[identity function]] and is closed under [[composition]] and taking [[inverse functions]].  This is the original notion of __concrete group__ due to [[Évariste Galois]].  Abstracting from this, we get the modern notion of __abstract [[group]]__ as a set equipped with an appropriate operation (taking the place of composition of permutations).

Much of the early work on group theory dealt with symmetry groups in [[geometry]], giving a geometric notion of concrete group in which $X$ is a [[space]] instead of a [[set]], although (except perhaps in [[constructive mathematics]] without the [[fan theorem]]) the relevant spaces form a [[concrete category]] and so the elements of the group can still be viewed as permutations of an [[underlying set]].

We can now give an *abstract* definition of the notion of *concrete* group:  An abstract group $G$ becomes a __concrete group__ on the set $X$ once it is given a [[free action]] of $G$ on $X$.  The [[Cayley theorem]] shows that every group may be made into a concrete group.


### Categories

Unlike groups, [[categories]] were first defined in full modern abstraction.  (At least, modern for the 20th century; by the end of the 21st century, it may seem old-fashioned not to start with weak $(\infty,1)$-[[(infinity,1)-category|categories]].)  But in light of the motivating examples and [[Bourbaki]]\'s prior theory of structures, we can anachronistically define a __concrete category__ as any category of [[structured sets]] (as defined there).

Of course, an __abstract category__ is the usual notion of [[category]].  Then the abstract definition of a __[[concrete category]]__ is a category equipped with a [[faithful functor]] to [[Set]]; see [[structured set]] again for the equivalence.


### Boolean algebras

...


### Vector spaces

...


### Hilbert spaces

...


### Operator algebras

...


### Manifolds

...


### Sets

...


### Points

...


## Concrete objects

...


[[!redirects concrete structure]]
[[!redirects concrete structures]]

[[!redirects abstract structure]]
[[!redirects abstract structures]]

[[!redirects concrete group]]
[[!redirects concrete groups]]

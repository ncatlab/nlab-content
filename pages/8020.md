
# Concrete and abstract structures
* table of contents
{: toc}

## Idea

Many concepts from ordinary mathematics were originally developed in the course of a particular application, such that the original definition of the concept is tied to that application.  The modern definition (typically some kind of [[structured set]]) is then obtained by a process of abstraction.  Sometimes this history is remembered in the terminology, often with the original notion being called _concrete_ and the later notion called _abstract_.

It then becomes possible to define the concrete notion in terms of the abstract one (so giving an *abstract* definition of the original *concrete* concept); usually, a concrete structure is then an abstract structure equipped with some [[extra stuff]].  Sometimes there is also a [[representation theorem]] showing that every abstract structure arises from some concrete structure (but sometimes this is false).


## Examples

We list here only examples where the concrete meaning has historically been the default meaning for at least some authors or where at least one of the adjectives 'concrete' or 'abstract' have been used.


### Groups

Given a [[set]] $X$, the [[permutation group]] on $X$ is the set of [[permutations]] on $X$; consider a [[subset]] of this that includes the [[identity function]] and is closed under [[composition]] and taking [[inverse functions]].  This is the original notion of __concrete group__ due to [[Évariste Galois]].  Abstracting from this, we get the modern notion of __abstract [[group]]__ as a set equipped with an appropriate operation (taking the place of composition of permutations).

Much of the early work on group theory dealt with symmetry groups in [[geometry]], giving a geometric notion of concrete group in which $X$ is a [[space]] instead of a [[set]], although (except perhaps in [[constructive mathematics]] without the [[fan theorem]]) the relevant spaces form a [[concrete category]] and so the elements of the group can still be viewed as permutations of an [[underlying set]].

We can now give an *abstract* definition of the notion of *concrete* group:  An abstract group $G$ becomes a __concrete group__ on the set $X$ once it is given a [[free action]] of $G$ on $X$.  The [[Cayley theorem]] shows that every group may be made into a concrete group.  Of course, if we generalise from [[Set]] to an arbitrary [[category]] (whether thought of as a category of spaces or not), then every group is *already* a concrete group, identifying a group with the [[automorphism group]] of a [[pointed category|pointed]] [[connected category|connected]] [[groupoid]].


### Categories

Unlike groups, [[categories]] were first defined in full modern abstraction.  (At least, modern for the 20th century; by the end of the 21st century, it may seem old-fashioned not to start with weak $(\infty,1)$-[[(infinity,1)-category|categories]].)  But in light of the motivating examples and [[Bourbaki]]\'s prior theory of structures, we can anachronistically define a __concrete category__ as any category of [[structured sets]] (as defined there).

Of course, an __abstract category__ is the usual notion of [[category]].  Then the abstract definition of a __[[concrete category]]__ is a category equipped with a [[faithful functor]] to [[Set]]; see [[structured set]] again for the equivalence.


### Vector spaces

The original [[vector spaces]] were [[Cartesian spaces]]: $\mathbb{R}^n$, where $\mathbb{R}$ is the [[real line]] and $n$ is a [[natural number]].  This generalises easily to $K^c$, where $K$ is any [[field]] and $c$ is any [[cardinal number]]; we may call such a __concrete vector space__.  Unlike with groups, there is no need (in [[classical mathematics]]) to consider [[subspaces]] of $K^c$ closed under [[linear combinations]], since these are all isomorphic to $K^d$ for $d \leq c$.

Then an __abstract vector space__, which came later, is a [[module]] over $K$ thought of as a [[commutative ring]].  The abstract definition of a __concrete vector space__ is an abstract vector space equipped with a [[basis]].  Using the [[axiom of choice]], we may prove that every abstract vector space has such a concrete structure.


### Hilbert spaces

The original notion of [[Hilbert space]] (the one used by [[David Hilbert]]) was $L^2(\mathbb{R})$, the [[Lebesgue space]] on the [[real line]] (with [[Lebesgue measure]]) of exponent $2$.  This immediately generalises to $L^2(X)$, where $X$ is any [[measure space]].  As a special case, if $X$ is a [[discrete space|discrete]] measure space (a [[set]] equipped with [[counting measure]]), then we have a topological version of the concrete vector space $K^c$.

Either of these (any measure space or only a discrete measure space) may be taken as a __concrete Hilbert space__, while the modern notion is an __abstract Hilbert space__.  An [[orthonormal basis]] on an abstract Hilbert space gives it the structure of a __concrete Hilbert space__ (in the stricter sense).


### Operator algebras

With [[operator algebras]], we have the curious situation that special names may still be found in the literature to distinguish the concrete and abstract structures.

Let $H$ be a [[Hilbert space]] over the [[complex numbers]] and consider the $*$-[[star-algebra|algebra]] $B(H)$ of [[bounded linear operators]] from $H$ to itself.  A __$C^*$-[[C-star-algebra|algebra]]__ is a sub-$*$-algebra of $B(H)$ that is [[closed subspace|closed]] in the [[norm topology]]; a __[[von Neumann algebra]]__ is a sub-$*$-algebra of $B(H)$ that is closed in the [[weak operator topology]] (a stronger condition).

On the abstract side, a __$B^*$-[[B-star-algebra|algebra]]__ is a [[Banach algebra|Banach]] $*$-algebra such that ${\|x^* x\|} = {\|x\|}^2$ always holds, while a __$W^*$-[[W-star-algebra|algebra]]__ is a $B^*$-algebra with a [[predual]] as a [[Banach space]].  It is then a theorem that (as defined above) every $C^*$-algebra is a $B^*$-algebra, and every von Neumann algebra is a $W^*$-algebra, so we may abstractly define a __$C^*$-algebra__ to be a $B^*$-algebra with a [[faithful representation|faithful]] [[representation]] on a Hilbert space, and similarly define a __von Neumann algebra__ to be a $W^*$-algebra with a free action on a Hilbert space.

The representation theorem here is that every $B^*$-algebra may be given the structure of a $C^*$-algebra, and in fact the term '$B^*$-algebra' is nearly obsolete.  Similarly, every $W^*$-algebra may be given the structure of a von Neumann algebra, but here both terms may yet be found (and even distinguished such that a von Neumann algebra comes with a representation on a Hilbert space but a $W^*$-algebra does not).


### Manifolds and varieties

The original [[algebraic varieties]] were [[subspaces]] of [[affine spaces]] or [[projective spaces]] given as the [[zero set]]s of [[algebraic function]]s; these are __concrete varieties__.  The modern notion of varieties as certain [[schemes]], the __abstract varieties__, is much more general.

Similarly, [[manifolds]] can be viewed as [[subspaces]] of [[Cartesian spaces]] with locally invertible local parametrisations ---**concrete manifolds**--- or as abstract sets of points equipped with an [[atlas]] of locally invertible local charts ---**abstract manifolds**.  Both concepts were used from the earliest days; the [[Whitney embedding theorem]] shows their equivalence (at least if the abstract manifolds are assumed to be [[second-countable space|second-countable]] and [[Hausdorff space|Hausdorff]], as is common).


### Sets

One might view the [[sets]] of [[material set theory]] as __concrete sets__ and the sets of [[structural set theory]] as __abstract sets__ (a term used at least by [[Lawvere]]).  The abstract definition of a concrete set is then that given at [[pure set]].  There is also a more na&#239;ve version of a __concrete set__ as a [[subset]] of a given [[ambient set]]; these were the first sets studied, predating [[set theory]] as such.


### Points

A __concrete [[point]]__ in a [[set]] $X$ is an [[element]] of $X$, an __abstract point__ is a [[singleton]], and the abstract definition of __concrete point__ in $X$ is a [[function]] to $X$ from an abstract point.  The concrete definition of concrete point doesn\'t generalise from [[Set]] to arbitrary [[categories]], but the others do: an __abstract point__ is a [[terminal object]], and a __concrete point__ is a [[global element]].


## Concrete objects

Since all of these concrete and abstract objects literally are [[objects]] in various [[categories]], it would be nice to use the terms 'concrete object' and 'abstract object' to refer to them collectively.  However, there is another meaning of '[[concrete object]]', so I have gone for the vaguer term 'structure' instead (justified since they are all objects in [[concrete categories]] and so are sets with [[extra structure]] ... with the exception of the concrete and abstract categories themselves!).

There is a relationship: concrete objects generalise [[concrete sheaves]], which are concrete in the sense of having an [[underlying set]] of points, similar to how a concrete variety has a set of points from an affine or projective space.  However, it\'s not really an example of the concept on this page, as far as I can tell.


[[!redirects concrete structure]]
[[!redirects concrete structures]]
[[!redirects abstract structure]]
[[!redirects abstract structures]]
[[!redirects concrete or abstract structure]]
[[!redirects concrete or abstract structures]]
[[!redirects concrete and abstract structure]]
[[!redirects concrete and abstract structures]]

[[!redirects concrete group]]
[[!redirects concrete groups]]

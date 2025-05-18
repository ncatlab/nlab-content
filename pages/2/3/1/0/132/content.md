
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea

The term _discrete category_ (or _discrete groupoid_) is used in two different ways:

1. A category is _discrete_ if it is [[equivalence of categories|equivalent]] to (or, sometimes, isomorphic to) a category whose only morphisms are identities; i.e., if [[small]], to a [[set#AsCategory|set]].  In other words, this is a [[truncated object|0-truncated]] object of [[Cat]]; see also [[discrete object in a 2-category]].  This meaning is discussed below in [Categorical meaning](#CategoricalMeaning).
   
1. A category with additional "topological" or "cohesive" structure is _discrete_ if that topological structure consists only of [[discrete spaces]].  This meaning is discussed below in [Topological meaning](#TopologicalMeaning).

See also the related discussion at [[discrete space]].


## Categorical meaning
{#CategoricalMeaning}

A [[category]] is **discrete** if it is both a [[groupoid]] and a [[preorder]].  That is, every morphism should be invertible, any two [[parallel morphisms]] should be equal.  The idea is that in a discrete category, no two distinct (nonisomorphic) objects are connectable by any path (morphism), and an object connects to itself only through its [[identity morphism]].

Often one also assumes that a discrete category is [[skeletal category|skeletal]]; a category is both discrete and skeletal if and only if it contains only identity morphisms.  However, this definition violates the [[principle of equivalence]], because it states that objects (the source and target of the identity morphism in question) are equal; it is cleaner to separate the discreteness from the skeletality.

A ([[small category|small]]) discrete category may be identified with its [[set]] of isomorphism classes.  Conversely, given a [[collection]] $S$ of objects, the __discrete category over $S$__ is the category with $S$ as its collection of objects and only identity morphisms.


## Topological meaning
{#TopologicalMeaning}

If $C$ is a category [[enriched category|enriched]] or [[internal category|internal]] to [[topological space|topological spaces]], then there is another completely different meaning of **discrete**: that the _topology_ on the arrows (and the objects, in the internal case) is the 
[[discrete topology]]. In this sense a _discrete category_ is an [[internal category]] in [[discrete spaces]] sitting inside a more general kind of spaces.  This usage can be applied more generally for internal or enriched categories in any context with a notion of [[discrete space]].

This is especially confusing if one extends the use of "discrete category over $S$" to the case of internal categories, when $S$ is an object of some ambient category.  With this usage, if $S$ is a topological space, then the "discrete internal category over $S$" in [[Top]] will not be discrete in the topological sense: it still remembers the topology on that space.

Because of potential confusion, in cases when topology or cohesion is present it is perhaps better to use *0-truncated* for categorically-discrete categories and groupoids, reserving *discrete* for those which are topologically-discrete.

## Adjoints

The discrete category construction extends to a [[fully faithful functor]] $Set \to Cat$. It has a [[left adjoint]] given by taking connected components and a [[right adjoint]] given by the underlying set of objects functor (which itself has a right adjoint given by the [[indiscrete category]] construction).


## Related concepts

* [[discrete space]]

* [[discrete group]] 

* **discrete groupoid**, [[discrete object in a 2-category]]

* [[discrete ∞-groupoid]]


[[!redirects discrete category]]
[[!redirects discrete categories]]

[[!redirects discrete groupoid]]
[[!redirects discrete groupoids]]

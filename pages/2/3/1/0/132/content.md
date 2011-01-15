
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Cohesive $\infty$-Toposes
+-- {: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

The term _discrete groupoid_ is used in two different ways:

1. as a synonym for 0-[[truncated]] [[groupoid]];

   this is discussed below in [Categorical meaning](#CategoricalMeaning)

1. as a synonym for 1-[[truncated]] [[discrete ∞-groupoid]].

   this is discussed below in [Topological meaning](#TopologicalMeaning).

Although the truncation terminology is not really established for $\infty$-[[infinity-categories]] that are not $\infty$-[[infinity-groupoids]], these particular meanings can easily be generalised to _discrete category_.


## Categorical meaning
{#CategoricalMeaning}

A [[category]] is **discrete** if it is both a [[groupoid]] and a [[preorder]].  That is, every morphism should be invertible, any two [[parallel morphisms]] should be equal.  The idea is that in a discrete category, no two distinct (nonisomorphic) objects are connectable by any path (morphism), and an object connects to itself only through its [[identity morphism]].

Often one also assumes that a discrete category is [[skeletal category|skeletal]]; a category is both discrete and skeletal if and only if it contains only identity morphisms.  However, this definition is [[evil]], because it states that objects (the source and target of the identity morphism in question) are equal; it is cleaner to separate the discreteness from the skeletality.

A ([[small category|small]]) discrete category may be identified with its [[set]] of isomorphism classes.  Conversely, given a [[collection]] $S$ of objects, the __discrete category over $S$__ is the category with $S$ as its collection of objects and only identity morphisms.


## Topological meaning
{#TopologicalMeaning}

If $C$ is a category [[enriched category|enriched]] or [[internal category|internal]] to [[topological space|topological spaces]], then there is another completely different meaning of **discrete**: that the _topology_ on the arrows (and the objects, in the internal case) is the 
[[discrete topology]]. In this sense a _discrete category_ is an [[internal category]] in [[discrete spaces]] sitting inside a more general kind of spaces.

This is especially confusing if one extends the use of "discrete category over $S$" to the case of internal categories, when $S$ is an object of some ambient category.  With this usage, if $S$ is a topological space, then the "discrete internal category over $S$" in [[Top]] will not be discrete in the topological sense: it still remembers the topology on that space.


## Related concepts

* [[discrete space]]

* [[discrete group]] 

* **discrete groupoid**

* [[discrete ∞-groupoid]]


[[!redirects discrete category]]
[[!redirects discrete categories]]

[[!redirects discrete groupoid]]
[[!redirects discrete groupoids]]

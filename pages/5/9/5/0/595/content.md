
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An **intersection** is a [[meet]] of [[subset]]s or (more generally) [[subobject]]s. Dually, a **cointersection** is a [[union]]/[[join]] of cosubobjects.

This includes the traditional [[set theory|set-theoretic]] intersection of subsets of some ambient set, as well as intersections of completely which can be constructed as  arbitrary sets (which are subsets of the [[universe]]) in [[material set theory]].

## Definition

### In material set theory

In [[material set theory]] such as [[ZFC]], the **intersection** of two sets $A$ and $B$ is

$$ A\cap B = \{ x \mid x\in A \;\text{ and }\; x\in B \}.$$

This makes sense for any two sets, but in practice it is usually used when $A$ and $B$ are both subsets of some ambient set $X$.

### In category theory

In a [[finitely complete category]], the **intersection** of two [[monomorphism]]s $A\hookrightarrow X$ and $B\hookrightarrow X$ is the [[pullback]] of the [[cospan]] $A\to X \leftarrow B$.  This is, in particular, also a [[meet]] in the poset of [[subobjects]] of $X$.

In a category that lacks all pullbacks, there is some question as to whether an intersection of subobjects should be defined as a pullback or as a meet in the poset of subobjects; the former implies the latter but not in general conversely.

Dually, the cointersection of two [[epimorphisms]] is their [[pushout]].

### Other arities

The __nullary intersection__ of the subsets of $X$ is $X$ itself.  Note that this does not make sense in material set theory until we fix an ambient set, since "the universe" is not a set.

A __binary intersection__ is the intersection of two sets or subobjects, as defined above, and a __finitary intersection__ is the intersection of [[finite set|finitely]] many sets or subobjects.  By induction, intersections may be built out of binary and nullary intersections.

One can also define infinitary intersections, which can be constructed categorically as [[wide pullbacks]].

## Properties

* [[interactions of images and pre-images with unions and intersections]]

  * [[the image of an intersection is contained in the intersection of the images]]

  * [[pre-images preserve intersections]], 

## Related concepts

* [[product]]

* [[union]]

* [[intersection product]], [[intersection theory]]

* [[brane intersection]]

[[!redirects intersection]]
[[!redirects intersections]]

[[!redirects cointersection]]
[[!redirects cointersections]]

[[!redirects nullary intersection]]
[[!redirects nullary intersections]]

[[!redirects binary intersection]]
[[!redirects binary intersections]]

[[!redirects finitary intersection]]
[[!redirects finitary intersections]]

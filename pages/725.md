
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In a [[preordered set]] or [[partially ordered set]] $P$, the _meet_ (or _infimum_, abbreviated _inf_, or _greatest lower bound_, abbreviated _glb_) of a [[subset]] $S$ of $P$ is, if it exists, the largest element of $P$ which is smaller or equal to all the elements in $S$. If this element is itself member of $S$, then it is also called the _[[minimum]]_ of that subset.

If we think of the pre-ordered set as a [[category]] (a [[(0,1)-category]]) then the meet is the [[limit]] over the given subset, if it exists, regarded as a [[diagram]]. Thus in a [[partially ordered set]] this is unique if it exists, otherwise it is unique up to [[isomorphism]].


## Definition

If $x$ and $y$ are elements of a [[partial order|poset]], then their **meet** is an element $x \wedge y$ of the poset such that:

* $x \wedge y \leq x$ and $x \wedge y \leq y$;
* if $a \leq x$ and $a \leq y$, then $a \leq x \wedge y$.

Such a meet may not exist; if it does, then it is unique.

In a [[preorder|proset]], a meet may be defined similarly, but it need not be unique.  (However, it is still unique up to the natural [[equivalence]] in the proset.)

The above definition is for the meet of two elements of a poset, but it can easily be generalised to any number of elements.  It may be more common to use 'meet' for a meet of finitely many elements and 'infimum' for a meet of (possibly) infinitely many elements, but they are the same concept.  The meet may also be called the **minimum** if it equals one of the original elements.

A poset that has all finite meets is a **meet-[[semilattice]]**.  A poset that has all infima is an **[[inflattice]]**.

A meet of [[subsets]] or [[subobjects]] is called an [[intersection]].


## Examples

### General

* A meet of no elements is a [[top]] element.  

* Any element $a$ is a meet of that one element.


### Infimum of real numbers

Often one considers infima of subsets of the [[real numbers]] $\mathbb{R}$, regarded with their canonical [[preordering]], which in this case is in fact a [[total order]].

For $S \subset \mathbb{R}$ a subset, say that a _lower bound_ is an element $b \in \mathbb{R}$ such that $\underset{s \in S \subset \mathbb{R}}{\forall}( b \leq s )$.

Then the infimum of $S$ is, if it exists, that lower bound $inf(S)$ of $S$ such that for $b$ any other lower bound of $S$ then $b \leq inf(S)$.

See [[join#constructive]] for the case in [[constructive analysis]].


## Properties

As a poset is a special kind of [[category]], a meet is simply a [[product]] in that category.


## Related concepts

* [[join]]

* **meet**


[[!redirects meet]]
[[!redirects meets]]
[[!redirects infimum]]
[[!redirects infimums]]
[[!redirects infima]]
[[!redirects inf]]
[[!redirects infs]] 
[[!redirects greatest lower bound]]
[[!redirects greatest lower bounds]]
[[!redirects glb]]
[[!redirects glbs]]
[[!redirects (0,1)-limit]]
[[!redirects (0,1)-limits]]


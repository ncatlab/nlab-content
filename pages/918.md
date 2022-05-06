
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Definition

A [[function]] $f$ (of sets) from $A$ to $B$ is __surjective__ if, given any element $y$ of $B$, $y = f(x)$ for some $x$.  A surjective function is also called __onto__ or a __surjection__; it is the same as an [[epimorphism]] in [[Set|the category of sets]]. 

A _[[bijection]]_ is a function that is both [[surjection|surjective]] and [[injection|injective]].

## The surjection preorder

In [[classical mathematics|classical]] [[set theory]], one writes $|B| \leq^* |A|$ to mean that either there is a surjection $A \to B$ *or* $B=\empty$. The relation $\leq^*$ is a [[preorder]] on the class of all sets, and its restriction to [[inhabited]] sets is the preorder reflection of the category $Surj_{inh}$ of inhabited sets and surjections.

To make this definition less piecemeal and more constructive, one can define $|B| \leq^* |A|$ to mean $B$ is a [[subquotient]] of $A$, in other words one has a surjection $B' \to B$ and an injection $B' \to A$. For $B$ inhabited and a subquotient of $A$, [[excluded middle]] implies there is a surjection from $A$ to $B$, so in [[classical mathematics]] this coincides with the piecemeal definition.

Contrast with the notation $|B| \leq |A|$ if there is an [[injection]] $B\to A$.  Since subobjects are subquotients (e.g. we can take $B'=B$ above), $|B| \leq |A|$ implies $|B| \leq^* |A|$.  (If we wanted to prove this using the piecemeal definition, we would require excluded middle.)

## Axioms of choice

The [[axiom of choice]] states precisely that every surjection in the category of sets has a [[section]]. Thus in this setting one has: $|B| \leq^* |A|$ implies $|B| \leq |A|$, and so $|B| \leq^* |A|$ iff $|B| \leq |A|$ assuming AC. Some authors who doubt the axiom of choice use the term 'onto' for a surjection as defined above and reserve 'surjective' for the stronger notion of a function with a section (a [[split epimorphism]]). 

The axiom [[WISC]] has an equivalent statement (that works in any Boolean [[topos]]) due to Fran&#231;ois Dorais phrased almost entirely in terms of surjections (or epimorphisms): 

>For every set $X$ there is a set $Y$ such that for every surjection $q\colon Z \to X$ there is a function $s\colon Y \to Z$ such that $q\circ s\colon Y\to X$ is a surjection.

One can view this as really a statement about the [[Grothendieck fibration]] over [[Set]] with fibre over $X$ the full subcategory of $Set/X$ on the surjections: every fibre has a [[weakly initial object]].

## In other categories
Since an element $a$ in a set $A$ the [[category of sets]] is just a function from the terminal set to $A$, one could generalise surjections to any category with a [[terminal object]] $1$:

> A morphism $f:A\rightarrow B$ is surjective if, given any [[global element]] $g:1\rightarrow B$, there exists a global element $h:1\rightarrow A$ such that $f \circ h = g$. 

The categorical [[duality|dual]] of a surjective morphism is just a morphism, as in any category with a [[terminal object]], there exists a unique morphism $!:A\rightarrow 1$ for any object $A$ in the category by definition, so follows that:

> For any morphism $f:A\rightarrow B$, there exists morphisms $!_{A}:A\rightarrow 1$ and $!_{B}:B\rightarrow 1$ such that $!_{B} \circ f = !_{A}$. 

## Related concepts

* [[injection]]

* [[epimorphism]]

* [[subquotient]]


[[!redirects surjective function]]
[[!redirects surjective functions]]


[[!redirects surjections]]
[[!redirects surjective]]
[[!redirects surjective map]]
[[!redirects surjective maps]]


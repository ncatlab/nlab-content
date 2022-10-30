
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

If there is a surjection $A \to B$, then one writes[^leqstar] $|B| \leq^* |A|$. The relation $\leq^*$ is a [[preorder]] on the class of all sets, the preorder reflection of the category $Surj$ of sets and surjections. Contrast with the notation $|B| \leq |A|$ if there is an [[injection]] $B\to A$. Assuming the [[axiom of excluded middle]], if there is a injection $B\to A$ and $B$ is [[inhabited]], there is a surjection $A\to B$. Thus $|B| \leq |A|$ implies $|B| \leq^* |A|$. If $B=\empty$ (=not inhabited, since we are assuming excluded middle) then by definition one also has $|B| \leq^* |A|$, so we have the implication in all cases.

[^leqstar]: One also writes $\empty \leq^* |A|$ for all sets $A$, but this is a standalone definition, and doesn't follow from a construction on $Surj$.


The [[axiom of choice]] states precisely that every surjection in the category of sets has a [[section]]. Thus in this setting one has: $|B| \leq^* |A|$ implies $|B| \leq |A|$, and so $|B| \leq^* |A|$ iff $|B| \leq |A|$ assuming AC. Some authors who doubt the axiom of choice use the term 'onto' for a surjection as defined above and reserve 'surjective' for the stronger notion of a function with a section (a [[split epimorphism]]). 


The axiom [[WISC]] has an equivalent statement (that works in any Boolean [[topos]]) due to Fran&#231;ois Dorais phrased almost entirely in terms of surjections (or epimorphisms): 

>For every set $X$ there is a set $Y$ such that for every surjection $q\colon Z \to X$ there is a function $s\colon Y \to Z$ such that $q\circ s\colon Y\to X$ is a surjection.

One can view this as really a statement about the [[Grothendieck fibration]] over [[Set]] with fibre over $X$ the full subcategory of $Set/X$ on the surjections: every fibre has a weakly initial object.

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



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

## In abstract categories
Since an element $a$ in a set $A$ in the [[category of sets]] is just a [[global element]] $a:1\rightarrow A$, one could define surjections in any abstract category $\mathcal{C}$ with a [[terminal object]] $1$:

> A morphism $f:A\rightarrow B$ in $\mathcal{C}$ is a surjection or a surjective morphism if, given any global element $y:1\rightarrow B$, there exists a global element $x:1\rightarrow A$ such that $y = f \circ x$. 

+-- {: .num_prop}
###### Proposition
In a category $\mathcal{C}$ with a [[terminal object]] $1$ such that $1$ is a [[separator]], every surjection is an [[epimorphism]]. 
=--

+-- {: .proof}
###### Proof
For any surjection $f:A\rightarrow B$, suppose there are parallel morphisms $g, h:B\rightarrow C$ such that there $g \circ f = h \circ f$ (a [[fork]]). Then for every global element $y:1\rightarrow B$ there exists a global element $x:1\rightarrow A$ such that $y = f \circ x$, and thus $g \circ y = g \circ f \circ x$ and $h \circ y = h \circ f \circ x$. But since $g \circ f = h \circ f$, $g \circ f \circ x = h \circ f \circ x$, which implies that $g \circ y = h \circ y$. Since $1$ is a [[separator]], then for every global element $y:1\rightarrow B$, if $g \circ y = h \circ y$, then $g = h$, showing that the surjection $f$ is an epimorphism. 
=--

+-- {: .num_prop}
###### Proposition
In a category $\mathcal{C}$ with a [[terminal object]] $1$ and binary [[equalisers]] such that every [[surjection]] has a [[section]] (axiom of choice for surjections), the terminal object $1$ is a [[separator]]. 
=--

+-- {: .proof}
###### Proof
Suppose there are parallel morphisms $g, h:B\rightarrow C$ such that for every global element $y:1\rightarrow B$, $g \circ y = h \circ y$. One could construct an equaliser $f:eq(g,h)\rightarrow B$, which implies that $g \circ f = h \circ f$ and that for any element $x\in eq(g,h)$, $g \circ f \circ x = h \circ f \circ x$. This implies that for every global element $y:1\rightarrow B$, $y = f \circ x$, and the equaliser $f:eq(g,h)\rightarrow B$ is a surjection. Since every surjection has a section $i:B\rightarrow eq(g,h)$ such that $f \circ i = 1_{B}$, the identity morphism on $B$, $g \circ f \circ i = h \circ f \circ i$, $g \circ 1_{B} = h \circ 1_{B}$, and $g = f$. Because for every global element $y:1\rightarrow B$, $g \circ y = h \circ y$ implies $g = h$, the terminal object $1$ is a [[separator]].
=--

### Duals of surjections

The categorical [[duality|dual]] of a surjection, the cosurjection, is a morphism $f:A\rightarrow B$ in an abstract category $\mathcal{C}$ with an [[initial object]] $\emptyset$ such that given a morphism $g:A\rightarrow\emptyset$, there exists a morphism $h:B\rightarrow\emptyset$ such that $h \circ f = g$. 

If the initial object $\emptyset$ is a [[zero object]], then every morphism in $\mathcal{C}$ is a cosurjection. If $\emptyset$ is [[strict initial object|strict]], such as in a [[distributive category]], then the identity morphism on $\emptyset$ is a cosurjection, and every other morphism in $\mathcal{C}$ whose [[source]] isn't $\emptyset$ is vacuously a cosurjection. 

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



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Global elements
* table of contents
{: toc}


## Idea

One striking difference between [[set theory]] and [[category theory]] is that, while [[objects]] of a [[category]] need not have any other structure, a [[set]] comes equipped with the notion of _element_, identifying other sets which belong to it.  Sometimes, a category turns out to possess a similar structure, designating certain [[morphisms]] as __global elements__ (or __global points__ in geometric contexts) of an object.


## Definition

If a category $C$ has a [[terminal object]] $1$, a __global element__ of another object $x$ is a morphism $1 \to x$.

So a global element is a [[generalized element]] at "stage of definition" $1$.

For example:

* In [[Set]], global elements are just elements: a function from a one-element set into $x$ picks out a single element of $x$.

* In [[Cat]], global elements are objects: the terminal category $1$ is the [[discrete category]] with one object, and a [[functor]] from $1$ into a category $C$ singles out an object of $C$.

* In a [[topos]], a global element of the [[subobject classifier]] is called a [[truth value]].

* Working in a [[over category|slice category]] $C/b$, a global element of the object $\pi: e \to b$ is a map into it from the terminal object $1_b: b \to b$; i.e., a [[right inverse]] for $\pi$.  In the context of [[bundles]], a global element of a bundle is called a *[[global section]]*.

If $C$ does not have a terminal object, we can still define a global element of $x\in C$ to be a global element of the [[represented functor|represented]] [[presheaf]] $C(-,x) \in [C^{op},Set]$.  Since the [[Yoneda embedding]] $x \mapsto C(-,x)$ is fully faithful and preserves any [[limits]] that exist in $C$, including terminal objects, if $C$ does have a terminal object then this definition coincides with the more naive one.

If we unravel the general definition more explicitly, it says that a global element of $x$ consists of, for every object $i\in C$, a morphism $e_x : i\to x$ (i.e. a [[generalized element]] of $x$ at stage $i$), such that for any morphism $f:i\to j$ we have $e_j \circ f = e_i$.


## Variations

Many (but not all) of the examples above are [[cartesian closed categories]].  In a more general [[closed category]], a morphism from the unit object to $x$ can be called an _element_ of $x$. For example, an element of an [[abelian group]] $x$ is a morphism from the group $\mathbf{Z}$ of integers to $x$, and of course this is equivalent to the usual notion of element of $x$. Here the adjective 'global' would not conform to the usage above since $\mathbf{Z}$ is not terminal, although we warn that some authors may call a map $\mathbf{Z} \to A$ a "global element" of $A$.

Thus generally, when $C$ is cartesian closed or even [[semicartesian monoidal category|semicartesian monoidal]] closed, the monoidal unit $I$ is terminal and such elements $I \to A$ are global elements in the sense of this article. But again, even in the general monoidal case, some authors call maps of the form $I \to A$ "global elements", even though this conflicts with our usage. 

As an important special case, there is[^1] for [[closed monoidal categories]] a notion of "name of a morphism", as follows. Let $\mathcal{C}$ be closed monoidal, with external ($Set$-valued) homs denoted by $\mathcal{C}(A, B)$, the monoidal product by $\otimes$ and the monoidal unit by $I$, and internal homs by $[A, B]$. Then for each pair $(A, B)$, the evident composite map 

$$\mathcal{C}(A, B) \stackrel{\mathcal{C}(\lambda_A, 1_B)}{\to} \mathcal{C}(I \otimes A, B) \cong \mathcal{C}(I, [A, B])$$ 

($\lambda_A: I \otimes A \to A$ the left unit isomorphism) defines a map which we denote as $name_{A, B}: \mathcal{C}(A,B)\rightarrow\mathcal{C}(I, [A,B])$. Notice this is the component at $(A, B)$ of a natural bijection $name$; it takes a map $f: A \to B$ in $\mathcal{C}$ to its name, typically denoted as $\text{"}f\text{"}: I \to [A, B]$, and which is an element of the internal hom $[A, B]$. 



[^1]: See, e.g., John Baez, Quantum Gravity Seminar, University of California, Riverside, Fall 2006, notes taken by Derek Wise, lecture of 2 November 2006.

Finally, in contrast to a global element, a morphism to $x$ from _any_ object $i$ whatsoever may be seen as a [[generalized element]] of $x$. For example, if $i$ is the [[unit interval]] (in topology, chain complexes, etc), then a map from $i$ to $x$ is a *path* (rather than a point) in $x$. Or in a slice category $C/b$, if $\rho: a \to b$ is an [[embedding]], then a morphism from $\rho$ to $\pi$ is a _local_ section of $\pi$.


[[!redirects global element]]
[[!redirects global elements]]
[[!redirects global point]]
[[!redirects global points]]

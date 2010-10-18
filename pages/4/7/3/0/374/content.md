
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



# Topological spaces
* automatic table of contents goes here
{: toc}


## Definition

A **topological space** is a set $X$ equipped with a set of [[subsets]] of $X$, called **open sets**, which are closed under finite [[intersections]] and arbitrary [[unions]].  Since $X$ itself is the intersection of zero subsets, it is open, and since the empty set $\emptyset$ is the union of zero subsets, it is also open.


The word 'topology' sometimes means the [[topology|study of topological spaces]] but sometimes the collection of open sets in a topological space. In particular, if someone says 'Let $T$ be a topology on $X$', then they mean 'Let $X$ be equipped with the structure of a topological space, and let $T$ be the collection of open sets in this space'.


The morphisms between topological spaces are **[[continuous maps]]**: functions $f:X\to Y$ such that the [[preimage]] of any open set is open.


## Alternate definitions

There are many equivalent ways to define a topological space.  A non-exhaustive list follows:

* A set $X$ with a [[frame]] of open sets (as above).

* A set $X$ with a co-frame of closed sets (the complements of the open sets) satisfying dual axioms.

* A set $X$ with any collection of subsets whatsoever, to be thought of as a [[subbase]] for a topology.

* A pair $(X, int)$, where $int: P(X) \to P(X)$ is a [[lex functor|left exact]] [[comonad]] on the [[power set]] of $X$ (the "interior operator").  The open sets are exactly the fixed points of $int$.

* A pair $(X, cl)$ where $cl$ is a [[rex functor|right exact]] [[Moore closure]] operator satisfying axioms dual to those of $int$.  The closed sets are the fixed points of $cl$.

* A relational $\beta$-module; that is, a [[lax algebra]] of the [[monad]] of [[ultrafilters]] on the [[(1,2)-category]] [[Rel]] of sets and [[binary relations]].  More explicitly, this means a set $X$ together with a relation called "[[convergence space|convergence]]" between ultrafilters and points satisfying certain axioms.

* A set with a convergence relation between [[nets]] or [[filters]] (not just ultrafilters) and points, or even between transfinite [[sequences]] and points, satisfying appropriate axioms.


## Variations

The definition of topological space was a matter of some debate, especially about 100 years ago. Our definition is due to Bourbaki, so may be called **Bourbaki spaces**.  For some purposes, including [[homotopy theory]], it is important to use [[nice topological spaces]] and/or a [[nice category of spaces]], or indeed to directly use a model of $\infty$-[[infinity-groupoid|groupoids]] such as [[simplicial sets]].  On the other hand, when doing [[topos theory]] or working in [[constructive mathematics]], it is often more appropriate to use [[locales]] than topological spaces.  Some applications to [[analysis]] require more general [[convergence spaces]] or other generalisations.

## Examples

### Special cases

* [[finite topological space]]

* [[CW-complex]]

* [[manifold]]

...

### Specific examples

* [[point]]

* [[circle]]

* [[Cantor space]]

* [[long line]]

...

[[!redirects topological space]]
[[!redirects topological spaces]]
[[!redirects topological structure]]
[[!redirects topological structures]]

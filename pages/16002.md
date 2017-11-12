# Contents
* table of contents
{: toc}

## Idea

A _germ of a space_ is an [[equivalence class]] of [[pointed spaces]], where two such spaces regarded as equivalent if they are isomorphic on small [[open neighbourhoods]] of the base points.

## Definition

The category of germs of spaces has as objects pointed spaces $(X,x_0)$, where _space_ may depend on the context ([[topological space]], [[complex manifold]], ...).

Morphisms $(X,x_0) \to (Y,y_0)$ are equivalence classes of basepoint-preserving morphisms $U \to Y$ defined on arbitrary open neighbourhoods $U$ of $x_0$. Two such morphisms are considered equal if they agree on an open neighbourhood of $x_0$ contained in the intersection of their domains.

## Examples

Let $f$ be a [[germ|germ of a holomorphic function]] on a complex manifold $X$, defined on an open neighbourhood $U$ of some point $x_0$. Then the vanishing set of $f$, $V(f) \coloneqq \{ x \in U \,|\, f(x) = 0 \}$, is not well-defined as a space. However, it gives rise to a well-defined germ of a space.

The base space of a [[universal deformation]] of a complex manifold is usually considered as a germ of a space.

## As a localization

The category of germs of space is the [[localization]] of the category of pointed spaces at the class of those morphisms which restrict to isomorphisms on open neighbourhoods of the basepoints.

## Related concepts

 * [[germ]]

 * [[microbundle]]

 * [[synthetic differential topology]]

[[!include infinitesimal and local - table]]

## References

A short exposition is contained in the textbook

* {#Huybrechts04} [[Daniel Huybrechts]] _Complex geometry - an introduction_. Springer (2004). Universitext. 309 pages. ([pdf](http://www.math.uh.edu/~shanyuji/2012/Geometry/Huybrechts.pdf))

For germs in deformation theory, see for instance

* Marco Manetti, _Deformation theory via differential graded Lie algebras_ ([arXiv:0507284](http://arxiv.org/abs/math/0507284)).

[[!redirects germs of a space]]

[[!redirects germs of spaces]]

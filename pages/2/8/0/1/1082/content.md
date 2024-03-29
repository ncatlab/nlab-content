
> maybe you are looking for the (total) _[[derivative]]_ (differential) of a map

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

Abstractly, a __differential__ is the morphism of a [[differential object]] defining a [[chain complex]]: the _boundary operator_.

So in a [[category with translation]] $T : C \to C$ a differential is a morphism $d_V : V \to T(V)$ for some [[object]] $V$ such that

$$
  V \stackrel{d_V}{\to} T V \stackrel{T(d_V)}{\to}
  T T V
$$

is the [[zero morphism]].

Unwrapping this for the case where the [[category with translation]] is a [[category of chain complexes]], it reproduces the ordinary notion of a differential as a degree-$(-1)$ morphism that squares to $0$.

More concretely, the boundary operator on a chain complex is called a _differential_ if this is part of the structure of a [[dg-algebra]] on the complex.

## Examples

The archetypical example that gives the concept its name is the differential in the [[de Rham complex]] $\Omega^\bullet(X)$ of a [[smooth manifold]] $X$, which is given by actual [[differentiation]] of [[smooth function]]s and [[differential form]]s. See also [[differential calculus]].

[[!redirects differentials]]


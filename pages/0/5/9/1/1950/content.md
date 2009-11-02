
This entry describes special methods for the construction of  fibrant replacements in the standard [[model structure on simplicial sets]].


#Contents#
* automatic table of contents
{:toc}

# Idea #

In as far as we may think of [[simplicial set]]s having some suitable properties as a [[simplicial model for weak ∞-categories]] (for instance for [[quasi-category|quasi-categories]]) and of a simplicial set that has the property of being a [[Kan complex]] as an [[∞-groupoid]], _Kan fibrant replacement_ of simplicial sets is the operation of _$\infty$-groupoidification_ in that it sends an $\infty$-category to the $\infty$-groupoid obtained by freely inverting all its non-invertible [[k-morphism]]s.

Technically, the terminology comes from the fact that with respect to the standard [[model structure on simplicial sets]] the [[Kan complex]]es are precisely the fibrant objects.


There are several methods to actually construct the Kan fibrant replacement. One convenient one, called the Ex-functor -- described below -- constructs an $\infty$-groupoid from (the nerve of) an $\infty$-category $C$ by

- taking its 1-morphisms to be ([[cospan|co]])[[span]]s in $C$;

- taking its 2-morphisms to be cospan-of-cospan [[multispan]]s in $C$:

- taking its 3-morphisms to be cospan-of-cospan-of-cospan [[multispan]]s in $C$:

- etc. 

# Ex-functor #


For $\Delta[k]$ the simplicial $k$-[[simplex]] let $sd \Delta[k]$ be its _barycentric subdivision_: this is the simplicial set that is the [[nerve]] of the [[poset]] of non-degenerate sub-simplicies in $\Delta[k]$.

Notice that this simplicial set $sd \Delta^k$ encodes the shape of an $n$-fold [[cospan]] of [[cospan]]s.

For instance

$$
  sd \Delta^1 = \{0 \to (0,1) \leftarrow 1\}
$$

is the ordinary [[cospan]].

These multi-cospan simplicial sets define a functor $Ex : SSet \to SSet$ by setting

$$
  (Ex X)_n = Hom_{SSet}(sd \Delta[k], X)
  \,.
$$

So this functor reads in a simplicial set $X$ and spits out the simplicial set whose 1-cells are [[cospan]]s in $X$.

This comes with a natural map

$$
  X \to Ex X
  \,.
$$

Iterating this construction indefinitely defines a simplicial set $Ex^\infty X$ to be the [[colimit]] over

$$
  X \to Ex X \to Ex Ex X \to \cdots
  \,.
$$

Then

**Proposition**

* $Ex^\infty X$ is a [[Kan complex]];

* $X \to Ex^\infty X$ is a natural weak equivalence.

## References ##

For instance section 3 of 

* Jardine, _Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))
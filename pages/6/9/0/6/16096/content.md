
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[smooth manifold]] $X$, and given $k \in \mathbb{N}\cup \{\infty\}$, there is a [[Lie groupoid]] whose [[objects]] are the points of $X$ and whose [[morphisms]] between two such points $x\to y$ are order-$k$ [[jets]] of local [[diffeomorphisms]] taking $x$ to $y$.

The [[automorphism groups]] of objects in these groupoids are _[[jet groups]]_.

Hence these Lie groupoids are often called _jet groupoids_, e.g. ([Lorenz 09](#Lorenz09)). If one passes from jets to [[germs]] of local diffeomorphisms then one arrives essentially at the [[Haefliger groupoid]] of $X$ (except that this has a more discrete smooth structure on its set of morphisms).

In a context of [[synthetic differential geometry]] or [[differential cohesion]] there is the bundle $T_{inf}^k X\to X$ of order-$k$ [[infinitesimal neighbourhoods]] in $X$. In terms of this the jet groupoid is the [[Atiyah groupoid]] of $T_{inf}^k X$, the groupoid whose morphisms between objects $x$ and $y$ are isomorphism of the [[fibers]] of this bundle over these points.

## Related concepts

* [[jet bundle]]

## References

* {#Lorenz09} Arne Lorenz, _Jet Groupoids, Natural Bundles
and the Vessiot Equivalence Method_, Thesis ([pdf](http://wwwb.math.rwth-aachen.de/~arne/Dissertation_Lorenz_Arne.pdf)) 2009

[[!redirects jet groupoids]]
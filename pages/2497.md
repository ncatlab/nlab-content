
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}



## Idea

The _blob complex_ may be thought of as a generalization of the [[Hochschild complex]] to [[higher category theory|higher categories]] and higher dimensional [[manifold]]s.  

One thinks of the Hochschild complex as associated to a 1-[[category]] and a 1-[[manifold]] (the circle).  It's a fairly small complex, analogous to cellular homology.  The blob complex for the same input data (1-category and circle) yields a [[quasi-isomorphism|quasi-isomorphic]] but much much larger [[chain complex]], analogous to [[singular homology]].  

Its advantage over the Hochschild complex is that it is "local".  In higher dimensions this locality means that it is easy to (well-) define the blob complex of an [[n-category]] + n-manifold without choosing any sort of decomposition of the n-manifold.


## Definition

There are two definitions.  The second is more general, and is homotopy equivalent to the first when both are available.  See references below for more details.


### First definition

* Start with a linear [[n-category]] $C$ with [[strong duality]] -- a [[blob n-category]] -- (e.g. [[pivotal 2-category]]) and an $n$-[[manifold]] $M$.

* Define $B_0(M)$ to be finite linear combinations of 
  "$C$-[[string diagram]]s" drawn on $M$.

* Define $B_1(M)$ to be finite linear combinations of triples $(B, u, r)$, where $B \subset M$ is a ball, $r$ is a [[string diagram]] on $M\setminus B$, and $u$ is a linear combination of  string diagrams on which evaluates to zero.

* Define $B_2(M)$ to be ...


### Second definition

...


## Examples

...


## Related concepts

* [[blob n-category]]

Blob homology has some similarities with 

* [[factorization algebra]]

* [[local net]]s in [[AQFT]].

It should be closely related to

* [[topological chiral homology]]/[[factorization homology]]

## References

A preprint is here:

* [[Scott Morrison]], [[Kevin Walker]], _The blob complex_, ([arxiv/1009.5025](http://arxiv.org/abs/1009.5025)) ([website](http://tqft.net/blobs))  
{#MorrisonWalker}

Notes from talks can be found [here](http://canyon23.net/math/talks) and [here](http://tqft.net/UCR-blobs1).

Some notes appeared in the context of the

* [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]

See the 

* Oberwolfach report No 28, 2009, [pdf](http://www.mfo.de/document/0924/OWR_2009_28.pdf)

[[!redirects blob homology]]
[[!redirects Blob homology]]
[[!redirects blob complex]]
[[!redirects blob complexes]]
[[!redirects blob chain complex]]
[[!redirects blob chain complexes]]

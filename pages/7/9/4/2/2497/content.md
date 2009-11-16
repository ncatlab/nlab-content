#Contents#

* automatic table of contents goes here
{:toc}

#Disclaimer#

In discussion elsewhere it has been asserted that half-baked and incomplete entries are welcome on nLab.  So I'm putting that to the test. -- KW

#Idea#

One way of thinking of the blob complex is as a generalization of the [[Hochschild complex]] to [[higher category theory|higher categories]] and higher dimensional manifolds.  

One thinks of the Hochschild complex as associated to a 1-[[category]] and a 1-[[manifold]] (the circle).  It's a fairly small complex, analogous to cellular homology.  The blob complex for the same input data (1-category and circle) yields a [[quasi-isomorphism|quasi-isomorphic]] but much much larger [[chain complex]], analogous to [[singular homology]].  

Its advantage over the Hochschild complex is that it is "local".  In higher dimensions this locality means that it is easy to (well-) define the blob complex of an [[n-category]] + n-manifold without choosing any sort of decomposition of the n-manifold.


#Definition#

Two definitions.  The second is more general, and is homotopy equivalent to the first when both are available.  See references below for more details.

First:

* Start with a linear n-category C with strong duality (e.g. pivotal 2-category) and an n-manifold M.

* Define B_0(M) to be finite linear combinations of "C string diagrams" drawn on M.

* Define B_1(M) to be finite linear combinations of triples (B, u, r), where B \subset M is is a ball, r is a string diagram on M\setminus B, and u is a linear combination of string diagrams on which evaluates to zero.

* Define B_2(M) to be ...

Second definition:

...

#Examples#

...

#Related entries#

Blob homology has some similarities with 

* [[factorization algebra]]

* [[local net]]s in [[AQFT]].

It should be closely related to

* [[topological chiral homology]].

#References#

A rough pre-preprint can be found [here](http://canyon23.net/math/blob1.pdf) or [here](http://tqft.net/blobs).

Notes from talks can be found [here](http://canyon23.net/math/talks) and [here](http://tqft.net/UCR-blobs1).

Some notes appeared in the context of the

* [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]

See the 

* Oberwolfach report No 28, 2009, [pdf](http://www.mfo.de/programme/schedule/2009/24/OWR_2009_28.pdf)

Currently, most of the above material is taken from the blog discussion [here](http://golem.ph.utexas.edu/category/2009/09/homotopy_theory_and_higher_alg.html#c027052).


[[!redirects blob complex]]
[[!redirects blob chain complex]]

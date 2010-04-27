A [[topological vector space]] is __locally convex__ if it has a base of topology consisting of convex open subsets.  Equivalently, it is a vector space equipped with a [[gauge space|gauge]] consisting of [[seminormed vector space|seminorms]].  As with other topological vector spaces, a locally convex space (LCS) is often assumed to be [[Hausdorff space]].

Locally convex (topological vector) spaces are the standard setup for much of the contemporary [[functional analysis]]. 


## Functionals 

One reason why locally convex TVS are important is that lots of (continuous!) [[functional]]s exist on them, at least if one assumes an appropriate choice principle, e.g., [[axiom of choice]] or [[ultrafilter theorem]] (or just [[dependent choice]] for a [[separable space]]). This fact is encapsulated in the [[Hahn-Banach theorem]]; a nice exposition is given in Terry Tao's [lecture notes](http://terrytao.wordpress.com/2009/01/26/245b-notes-6-duality-and-the-hahn-banach-theorem/). By way of contrast, a TVS which is _not_ locally convex, such as the topological vector space $L^p([0, 1])$ where $0 \lt p \lt 1$, need not have any (nonzero) functionals at all. 

+--{: .query}
[[David Roberts]]: Hurray! I can edit (for now). The following fact is just from memory, but it was the one fact that struck me about LCTVSs and made me realise why we needed local convexity. Please check that it is right.
=--
A simple and concrete example is that for a locally convex TVS $V$ one knows that the coordinate projection functions $V \to k$ are continuous (for $k$ the topological base field). There are examples of non-locally convex TVSs where this is not the case.
+--{: .query}
[[David Roberts]]: I presume that the example $L^p([0,1])$, $p\in (0,1)$, above is one such example. In this instance (for general $p$), the 'coordinate projection' is evaluation at a point in $[0,1]$, and you certainly want this to be continuous.
=--



[[!redirects locally convex spaces]]
[[!redirects locally convex vector space]]
[[!redirects locally convex vector spaces]]
[[!redirects locally convex topological vector space]]
[[!redirects locally convex topological vector spaces]]
[[!redirects locally convex TVS]]
[[!redirects LCS]]
[[!redirects LCTVS]]
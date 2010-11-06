
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Whitehead product** is a bilinear operation on the elements of the [[homotopy groups]] of a [[pointed space|pointed]] [[CW-complex]] $X$.  

More specifically, it takes as input $\alpha\in\pi_r(X)$ and $\beta\in\pi_s(X)$ and produces $[\alpha,\beta]_{Wh}\in\pi_{r+s-1}(X)$.  The operation satisfies a graded Jacobi identity (the conventions on the signs are not uniform in the literature). 

There is also a **generalized Whitehead product** where we can take more general homotopy classes ([[continuous maps]] up to [[homotopy]]) $\alpha\in [S^\cdot Y,X]$ and $\beta\in [S^\cdot Z,X]$ to produce a class $[\alpha,\beta]_{Wh}\in[Y\star Z,X]$. Here $S^\cdot$ denotes the [[reduced suspension]] operation on pointed spaces and $\star$ denotes the [[join of spaces|join]] of CW-complexes. Notice that $pt\star Z = C^\cdot(Z)$ and the [[reduced cone]] of a point is $C^\cdot(pt)=S^1$. Thus for $Y=Z=pt$ the generalized Whitehead product reduced to the usual Whitehead product.

The Whitehead products form one of the [[primary homotopy operation]]s and in fact with [[composition operation]]s and $\pi_1$-actions generate all such operations. This is related to the definition of [[Pi-algebra]].

In the context of [[simplicial group]]s, representing [[connected]] [[homotopy type]]s, there is a formula for the Whitehead product in terms of a [[Samelson product]], which in turn is derived from a [[shuffle]] product which is a sort of non-commutative version of the [[Eilenberg-Zilber map]].  These simplicial formulae come from an analysis of the structure of the [[product of simplices]]. (The formula for the Whitehead product is due to Dan Kan and can be found in the old survey article of Curtis.  The proof that it works has never published.)


## References

See also [wikipedia](http://en.wikipedia.org/wiki/Whitehead_product).
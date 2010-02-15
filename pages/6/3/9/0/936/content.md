<div class="rightHandSide toc">
[[!include homotopy - contents]]
</div>


#Contents#
* automatic table of contents
{:toc}

## Definition 

A **homotopy equivalence** between [[topological space]]s $X$ and $Y$ is a continuous map $f:X\to Y$  such that there exists a continuous map $g:Y\to X$ and [[homotopy|homotopies]] $g \circ f \sim 1_X$ and $f \circ g \sim 1_Y$. (Note the similarity with the strict notion of [[equivalence of categories]].)

More generally, in any [[(∞,1)-category]] $C$ other than [[Top]], a homotopy equivalence in $C$ is just an equivalence in $C$.

If there exists a homotopy equivalence between $X$ and $Y$ we say that $X$ and $Y$ are **homotopy equivalent** or that they have the same **[[homotopy type]]**.  Being homotopy equivalent is evidently an [[equivalence relation]].

For many purposes, one wants instead [[weak homotopy equivalence]]s.  Often when speaking of a homotopy equivalence or a homotopy type, one actually means the weak version.  (This is especially likely on this wiki, due to the relationship to $\infty$-[[infinity-groupoid]]s suggested by the [[homotopy hypothesis]].)

## Properties 

Any homotopy equivalence is also a [[weak homotopy equivalence]].  Conversely, any weak homotopy equivalence between [[m-cofibrant space]]s (spaces that are homotopy equivalent to [[CW complex]]es) is a homotopy equivalence. This is the [[Whitehead theorem]].

The homotopy equivalences are the [[weak equivalence]]s in the Str&oslash;m [[model structure on topological spaces]].  The [[homotopy category]] resulting from inverting all homotopy equivalences in [[Top]] is the same as that resulting from identifying homotopic maps.

##  Strong homotopy equivalences

Sometimes an apparently stronger form of homotopy equivalence is needed.  These seem to have been first noticed by [[Richard Lashof]] in 1970 in work on triangulation and smoothing. The point is one of the interaction between the two homotopies, which are not made explicit in the definition above. Let us set this up slightly differently:

In a homotopy equivalence there are the two maps $f: X\to Y$ and $g: Y\to X$


 
[[!redirects homotopy equivalences]]
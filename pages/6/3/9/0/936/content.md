<div class="rightHandSide toc">
[[!include homotopy - contents]]
</div>


#Contents#
* automatic table of contents
{:toc}

# Definition #

A **homotopy equivalence** is between [[topological space]]s $X$ and $Y$ a continuous map $f:X\to Y$  such that there exists a continuous map $g:Y\to X$ and [[homotopy|homotopies]] $g \circ f \sim 1_X$ and $f \circ g \sim 1_Y$. (Note the similarity with the strict notion of [[equivalence of categories]].)

If there exists a homotopy equivalence between $X$ and $Y$ we say that $X$ and $Y$ are **homotopy equivalent** or that they have the same **[[homotopy type]]**.  Being homotopy equivalent is evidently an [[equivalence relation]].

For many purposes, one wants instead [[weak homotopy equivalence]]s.  Often when speaking of a homotopy equivalence or a homotopy type, one actually means the weak version.  (This is especially likely on this wiki, due to the relationship to $\infty$-[[infinity-groupoid]]s suggested by the [[homotopy hypothesis]].)

# Properties #

Any homotopy equivalence is also a [[weak homotopy equivalence]].  Conversely, any weak homotopy equivalence between [[m-cofibrant space]]s (spaces that are homotopy equivalent to [[CW complex]]es) is a homotopy equivalence. This is the [[Whitehead theorem]].

The homotopy equivalences are the [[weak equivalence]]s in the Str&oslash;m [[model structure on topological spaces]].  The [[homotopy category]] resulting from inverting all homotopy equivalences in [[Top]] is the same as that resulting from identifying homotopic maps.

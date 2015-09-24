## Idea

One fundamental tool in a knot theorist's toolbox is the [[knot diagram]].  In classical [[knot theory]], a knot diagram or link diagram may be considered formally as a 4-valent [[plane graph]] (called the _shadow_ of the knot/link), equipped with annotations on each vertex specifying whether it represents an undercrossing or an overcrossing.  The [[Reidemeister moves]] define an [[equivalence relation]] on knot diagrams, which can be used to determine when two diagrams represent knots (or links) that are [[isotopic]].  It is a theorem that the Reidemeister moves are complete for isotopy, but from a formal perspective, one could also _define_ a classical knot/link as an equivalence class of knot/link diagrams, i.e., of decorated 4-valent plane graphs.

From that perspective, virtual knot theory (introduced by [[Louis Kauffman]]) generalizes classical knot theory by considering knots and links as equivalence classes of decorated 4-valent graphs embedded in [[orientable]] surfaces of arbitrary [[genus of a surface|genus]].  In topological terms, all classical knots can in fact be realized as embeddings of the circle inside a "thickened" sphere $S^2 \times [0,1]$ (rather than in all of $\mathbb{R}^3$), while _virtual knots_ generalize this to embeddings of the circle inside any thickened orientable surface.  If one projects a virtual knot onto the page, the diagram might contain crossings that do _not_ represent places where the knot passes over/under itself, but rather are artifacts of the knot's non-planar shadow.  So, in a virtual knot diagram such crossings are explicitly indicated as "virtual", using a distinct notation from that for under/overcrossings.

## Related concepts

* [[embedded graph]]

## References

* [[Louis Kauffman]], Virtual Knot Theory, _European Journal of Combinatorics_ (1999) 20, 663-691. [pdf](http://homepages.math.uic.edu/~kauffman/VKT.pdf)

* [[Louis Kauffman]], Introduction to Virtual Knot Theory. July 2012. [arXiv](http://arxiv.org/abs/1101.0665)

* [[Greg Kuperberg]], What is a virtual link?, _Algebraic & Geometric Topology_ Volume 3 (2003), 587-591. [pdf](http://arxiv.org/pdf/math/0208039v2.pdf)

* in a brief comment at the n-Caf&#233;, [John Baez writes](https://golem.ph.utexas.edu/category/2008/10/categorification_in_new_scient.html#c019490), "Abstractly, virtual knot theory is the study of the free [[symmetric monoidal category with duals]] on one object $X$ equipped with a morphism $R:X\otimes X\to X\otimes X$ that satisfies the [[Yang-Baxter equation]]".

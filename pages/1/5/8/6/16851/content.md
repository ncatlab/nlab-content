# Contents
* table of contents
{: toc}

## Idea

One fundamental tool in a knot theorist's toolbox is the [[knot diagram]].  In classical [[knot theory]], a knot diagram or link diagram may be considered formally as a 4-valent [[plane graph]] (called the _shadow_ of the knot/link), equipped with annotations on each vertex specifying whether it represents an undercrossing or an overcrossing.  The [[Reidemeister moves]] define an [[equivalence relation]] on knot diagrams, which can be used to determine when two diagrams represent knots (or links) that are [[isotopic]].  It is a theorem that the Reidemeister moves are complete for isotopy, but from a formal perspective, one could also _define_ a classical knot/link as an equivalence class of knot/link diagrams, i.e., of decorated 4-valent plane graphs.

From that perspective, virtual knot theory (introduced by [[Louis Kauffman]]) generalizes classical knot theory by considering knots and links as equivalence classes of decorated 4-valent graphs embedded in [[orientable]] surfaces of arbitrary [[genus of a surface|genus]].  In topological terms, all classical knots can in fact be realized as embeddings of the circle inside a "thickened" sphere $S^2 \times [0,1]$, while _virtual knots_ generalize this to embeddings of the circle inside any thickened orientable surface.  If one projects a virtual knot onto the page, the diagram might contain crossings that do _not_ represent places where the knot passes over/under itself, but rather are artifacts of the knot's non-planar shadow.  So, in a virtual knot diagram such crossings are explicitly indicated as "virtual", using a distinct notation from that for under/overcrossings.

## Motivations

[Kauffman (1999)](#Kauffman1999) describes two sources of motivation for virtual knot theory.  The first is just the extension of classical knot theory to the study of knots in thickened surface of higher genus, and the fact that many classical [[knot invariants]] also yield invariants of such virtual knots.  A separate motivation that Kauffman mentions is of a combinatorial nature, related to the use of so-called [[Gauss codes]] for representing knots, and the fact that it is natural to study non-planar Gauss codes which are realized as virtual knots.

## Categorical formulations

The original work on virtual knot theory is not expressed in categorical language and a categorical foundation of virtual knot theory is not yet firmly established.  However, in a brief comment at the n-Caf&#233;, [John Baez writes](https://golem.ph.utexas.edu/category/2008/10/categorification_in_new_scient.html#c019490) that

> Abstractly, virtual knot theory is the study of the free [[symmetric monoidal category with duals]] on one object $X$ equipped with a morphism $R:X\otimes X\to X\otimes X$ that satisfies the [[Yang-Baxter equation]].

The intuition is that the braiding of the ambient symmetric monoidal category represents the virtual crossings, while the the Yang-Baxter operator $R : X \otimes X \to X \otimes X$ on the object $X$ represents the "real" (i.e., classical) over- and under-crossings of the knot embedded in the thickened surface.

## Terminology

Warning: a virtual knot/link has a genus in the sense of the genus of the underlying thickened surface into which it embeds (or equivalently, the genus of its shadow as a 4-valent [[combinatorial map]]), but this is unrelated to the classical notion of _knot genus_, in the sense of the minimal genus of a [[Seifert surface]] whose [[boundary]] is the knot.

## Related concepts

* [[Gauss diagram]]
* [[embedded graph]]

## References

* {#Kauffman1999} [[Louis Kauffman]], Virtual Knot Theory, _European Journal of Combinatorics_ (1999) 20, 663-691. [pdf](http://homepages.math.uic.edu/~kauffman/VKT.pdf)

* Naoko Kamada and Seiichi Kamada, Abstract Link Diagrams and Virtual Knots, _Journal of Knot Theory and its Ramifications_, Vol. 9, No. 1 (2000), 93-106. [doi](http://dx.doi.org/10.1142/S0218216500000049)

* {#Kauffman2012} [[Louis Kauffman]], Introduction to Virtual Knot Theory. July 2012. [arXiv](http://arxiv.org/abs/1101.0665)

* {#Kuperberg2003} [[Greg Kuperberg]], What is a virtual link?, _Algebraic & Geometric Topology_ Volume 3 (2003), 587-591. [pdf](http://arxiv.org/pdf/math/0208039v2.pdf)

* {#Viro} Oleg Viro, Virtual Links, Orientations of Chord Diagrams and Khovanov Homology, Proceedings of 12th G&#246;kova Geometry-Topology Conference, pp. 184&#8211;209, 2005. [pdf](http://www.pdmi.ras.ru/~olegviro/ggt05-viro.pdf)

* {#ManturovIlyutko} Vassily Olegovich Manturov and Denis Petrovich Ilyutko, _Virtual Knots: The State of the Art_.  Series on Knots and Everything (vol. 51), World Scientific, 2013.

* {#Kauffman2015} [[Louis Kauffman]], Rotational Virtual Knots and Quantum Link Invariants, 14 Oct 2015. [arxiv:1509.00578](http://arxiv.org/abs/1509.00578)
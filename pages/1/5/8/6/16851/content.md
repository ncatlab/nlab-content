+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

One fundamental tool in a knot theorist's toolbox is the [[knot diagram]].
Classically, a [[knot]] is an embedding of the circle $S^1$ into Euclidean space $\mathbb{R}^3$, and knot diagrams arise by projecting back down to the [[plane]] $\mathbb{R}^2$ to obtain a 4-valent [[plane graph]] (referred to as the _shadow_ of the knot), while keeping track of whether each vertex corresponds to an under-crossing or an over-crossing.
Although the knot is traditionally seen as embedded in $\mathbb{R}^3$, it could equally well be realized inside of a "thickened" [[sphere]] $S^2 \times [0,1]$, with its shadow embedded in $S^2$.
From that perspective, _virtual knot theory_ generalizes classical knot theory by considering knots as embeddings of circles into thickened [[orientable]] surfaces $X \times [0,1]$ of arbitrary [[genus of a surface|genus]].
Abstractly, the shadow of such a knot is a 4-valent graph embedded in $X$ (i.e., a [[topological map]]).
However, if one tries to project the knot onto the plane, the corresponding diagram might contain crossings that do _not_ represent places where the knot passes over/under itself inside the thickened surface, but rather are artifacts of the knot's non-planar shadow.
So, in a _virtual knot diagram_ such crossings are explicitly indicated as "virtual", using a distinct notation from that for under/overcrossings.

## Definitions

There are various equivalent definitions of virtual knots/links:

* As equivalence classes of virtual knot/link diagrams, modulo the "virtual" [[Reidemeister moves]] [(Kauffman 1999)](#Kauffman1999).
* As equivalence classes of "abstract" knot/link diagrams embedded in orientable surfaces, modulo the Reidemeister moves [(Kamada and Kamada 2000)](#KamadaKamada).
* As embeddings of circles into thickened orientable surfaces, considered up to [[isotopy]] [(Kuperberg 2003)](#Kuperberg2003).
* As equivalence classes of [[Gauss codes]], modulo relations corresponding to the Reidemeister moves [(Kauffman 1999)](#Kauffman1999).


## Categorical formulations

The original work by [[Louis Kauffman]] is not expressed in categorical language, and to the best knowledge of the present nLab editor, at this time (November 2016) there is still no well-established categorical foundation for virtual knot theory.
However, in late 2008, [[John Baez]] made a brief but interesting [comment at the n-Caf&#233;](https://golem.ph.utexas.edu/category/2008/10/categorification_in_new_scient.html#c019490):

> Abstractly, virtual knot theory is the study of the free [[symmetric monoidal category with duals]] on one object $X$ equipped with a morphism $R:X\otimes X\to X\otimes X$ that satisfies the [[Yang-Baxter equation]].

It seems that the intuition here is that the braiding of the ambient symmetric monoidal category represents the virtual crossings "for free", while the Yang-Baxter operator $R : X \otimes X \to X \otimes X$ on the object $X$ represents the "real" (i.e., classical) over- and under-crossings of the knot embedded in the thickened surface.

## Terminology

Warning: a virtual knot/link has a genus in the sense of the genus of the underlying thickened surface into which it embeds (or equivalently, the genus of its shadow as a topological map), but this is unrelated to the classical notion of _knot genus_, in the sense of the minimal genus of a [[Seifert surface]] whose [[boundary]] is the knot.

## Related concepts

* [[Gauss diagram]]
* [[embedded graph]]

## References

* {#Kauffman1999} [[Louis Kauffman]], Virtual Knot Theory, _European Journal of Combinatorics_ (1999) 20, 663-691. [pdf](http://homepages.math.uic.edu/~kauffman/VKT.pdf)

* {#KamadaKamada} Naoko Kamada and Seiichi Kamada, Abstract Link Diagrams and Virtual Knots, _Journal of Knot Theory and its Ramifications_, Vol. 9, No. 1 (2000), 93-106. [doi](http://dx.doi.org/10.1142/S0218216500000049)

* {#Kauffman2012} [[Louis Kauffman]], Introduction to Virtual Knot Theory. July 2012. [arXiv](http://arxiv.org/abs/1101.0665)

* {#Kuperberg2003} [[Greg Kuperberg]], What is a virtual link?, _Algebraic & Geometric Topology_ Volume 3 (2003), 587-591. [pdf](http://arxiv.org/pdf/math/0208039v2.pdf)

* {#Viro} Oleg Viro, Virtual Links, Orientations of Chord Diagrams and Khovanov Homology, Proceedings of 12th G&#246;kova Geometry-Topology Conference, pp. 184&#8211;209, 2005. [pdf](http://www.pdmi.ras.ru/~olegviro/ggt05-viro.pdf)

* {#ManturovIlyutko} Vassily Olegovich Manturov and Denis Petrovich Ilyutko, _Virtual Knots: The State of the Art_.  Series on Knots and Everything (vol. 51), World Scientific, 2013.

* {#Kauffman2015} [[Louis Kauffman]], Rotational Virtual Knots and Quantum Link Invariants, 14 Oct 2015. [arxiv:1509.00578](http://arxiv.org/abs/1509.00578)
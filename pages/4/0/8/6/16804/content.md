
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
{:toc}

## Idea

A _chord diagram_ is a certain kind of basic combinatorial structure that is considered in various settings such as [[combinatorics]] and [[knot theory]]. Chord diagrams are typically represented graphically as a [[circle]] with some marked [[points]] and [[lines]] connecting those points &#8212; something like so:
<center>
[[!include chord diagram > chord diagram unlabelled]]
</center>
If we label the points of the diagram,
<center>
[[!include chord diagram > chord diagram]]
</center>
then the matching on points induced by the chords corresponds to an [[involution]] on the set of labels ($A \mapsto C$, $B \mapsto D$, $C \mapsto A$, $D \mapsto B$, $E \mapsto F$, $F \mapsto E$).
Considering this situation more abstractly, a chord diagram can be defined formally as a finite [[cyclically ordered set]] equipped with an involution (which may or may not have [[fixed points]], corresponding to unattached points).
The subtle point is that a chord diagram can have non-trivial [[symmetries]] induced by the cyclic structure.
For example, the two labellings
<center>
[[!include chord diagram > chord diagram 2a]]
</center>
and
<center>
[[!include chord diagram > chord diagram 2b]]
</center>
both represent the same underlying chord diagram, corresponding to the involution $(AC)(BE)(DF)$ on the cyclically ordered set $(ABCDEF)$.

In many situations, one also wants to consider a [[rigid]] version of chord diagrams, known as _rooted chord diagrams_ (or _arc diagrams_), where the set of points is instead [[linearly ordered]].
Graphically, one can visualize this as cutting the circle at a particular segment and "opening up" the diagram.
For example, here we cut the first diagram above at the segment AF
<center>
[[!include chord diagram > arc diagram latin]]
</center>
Relabelling the points to follow the linear order,
<center>
[[!include chord diagram > arc diagram]]
</center>
the rooted chord diagram can now be identified with the involution $(02)(13)(45)$ on $\mathbf{6} = \{0 \lt 1 \lt 2 \lt 3 \lt 4 \lt 5\}$.

Every rooted chord diagram uniquely determines a chord diagram (glue the left and right ends back together).
Conversely, a chord diagram with $n$ chords connecting $2n$ distinct points can be rooted in up to $2n$ different ways, but might also have fewer rootings in the case of symmetries.

## Gauss diagrams of ordinary (virtual) knots

Any [[knot diagram]] can be represented faithfully by a certain kind of chord diagram with some extra structure, known as a _Gauss diagram_ [(Polyak and Viro 1994)](#PV94).

Recall that classically, a knot is defined as an embedding of the circle $S^1$ into $\mathbb{R}^3$, which can be represented two-dimensionally by projecting onto the plane $\mathbb{R}^2$ and marking each double point as either an over-crossing or an under-crossing.
One obtains a chord diagram from this knot diagram by considering the original immersing circle and connecting the [[preimages]] of each double point by a chord.
Then, information about crossings can be represented by orienting the chords from over-crossing to under-crossing, while information about the local [[writhe]] of each crossing (in the case of a [[framed knot]]) may be encoded by assigning each chord an additional positive or negative sign.
Finally, fixing a [[base point]] on the original knot gives rise to a Gauss diagram whose underlying chord diagram is naturally rooted.

Once again, this geometric object can be abstracted into a purely combinatorial one, called the _Gauss code_ of the knot (diagram).
To construct the Gauss code, begin by assigning arbitrary labels to the crossings, then run the length of the knot (starting at some arbitrary base point) and output the name of each crossing as you visit it, together with a [[bit]] (or two bits in the case of a framed knot) specifying whether you are at an over-crossing or an under-crossing (of positive or negative writhe).
(In this notation, the involution on the points of the underlying chord diagram is encoded implicitly as a _double-occurrence word_.)

Polyak and Viro called these "Gauss diagrams" after [[Carl Gauss]], who apparently studied the question of which chord diagrams arise from immersions of circles.
This question also played a foundational role in [[virtual knot theory]] &mdash; indeed, according to [Kauffman (1999)](#Kauffman1999), the "fundamental combinatorial motivation" for the definition of virtual knots was the idea that it should be possible to interpret an _arbitrary_ Gauss diagram as encoding a knot (now no longer seen as an embedding of $S^1$ into $\mathbb{R}^3$, but into a thickened surface of arbitrary genus).

## Chord diagrams of singular knots

By an analogous mechanism, any [[singular knot]] $K$ with $n$ simple double points (i.e., points where the knot intersects itself transversally) gives rise to a chord diagram $c(K)$ with $n$ chords, by connecting the preimages of these double points.
This chord diagram $c(K)$ of course does not faithfully represent the original knot $K$ (e.g., it does not include any information about over-crossings and under-crossings).
However, such chord diagrams nonetheless play an important role in the theory of [[Vassiliev invariants]], by the theorem that the value of a Vassiliev invariant $v$ of degree $\le n$ on any singular knot $K$ with $n$ simple double points depends only on the chord diagram $c(K)$.

## Related concepts

* [[involution]]
* [[Vassiliev invariant]]
* [[combinatorial map]]

## References

For chord diagrams and arc diagrams from the perspective of [[combinatorics]], see:

* Jacques Touchard. Sur un probl&#232;me de configurations et sur les fractions continues. Canadian Journal of Mathematics 4 (1952), 2-25. ([doi](http://dx.doi.org/10.4153/CJM-1952-001-8))

* Philippe Flajolet and Marc Noy. Analytic combinatorics of chord diagrams. INRIA technical report 3914, March 2000. ([pdf](http://algo.inria.fr/flajolet/Publications/FlNo00.pdf))

* A. Khruzin. Enumeration of chord diagrams. arXiv:math/0008209, August 2000. ([arxiv](http://arxiv.org/abs/math/0008209))

For the relationship to Gauss diagrams in classical and [[virtual knot theory]], see:

* {#PV94} Michael Polyak and Oleg Viro, Gauss diagram formulas for Vassiliev invariants, _International Mathematics Research Notes_ 1994:11. [pdf](http://www.math.stonybrook.edu/~oleg/math/papers/1994-Polyak-Viro.pdf)

* {#Kauffman1999} [[Louis Kauffman]], Virtual Knot Theory, _European Journal of Combinatorics_ (1999) 20, 663-691. [pdf](http://homepages.math.uic.edu/~kauffman/VKT.pdf)

* {#Viro05} Oleg Viro, Virtual Links, Orientations of Chord Diagrams and Khovanov Homology, Proceedings of 12th G&#246;kova Geometry-Topology Conference, pp. 184&#8211;209, 2005. [pdf](http://www.pdmi.ras.ru/~olegviro/ggt05-viro.pdf)

* [Gauss codes](http://katlas.org/wiki/Gauss_Codes) at the Knot Atlas.

For the connection to [[Vassiliev invariants]] of [[singular knots]], see:

* Chapter 6 of [[Sergei K. Lando]] and [[Alexander K. Zvonkin]], _Graphs on Surfaces and Their Applications_, Springer, 2004.

* [[Dror Bar-Natan]], On the Vassiliev knot invariants, _Topology_ 34 (1995), 423-472. ([html](http://www.math.toronto.edu/~drorbn/papers/OnVassiliev/))

* [[Simon Willerton]], Vassiliev invariants and the [[Hopf algebra]] of chord diagrams, Math. Proc. Camb. Phil. Soc. (1996), 119, 55.

* Greg Muller, ["Chord Diagrams and Lie Algebras"](https://cornellmath.wordpress.com/2007/12/25/chord-diagrams-and-lie-algebras/), blog post at _The Everything Seminar_, 25 December 2007.

[[!redirects chord diagrams]]
[[!redirects rooted chord diagram]]
[[!redirects rooted chord diagrams]]
[[!redirects arc diagram]]
[[!redirects arch diagram]]
[[!redirects arc diagrams]]
[[!redirects arch diagrams]]
[[!redirects Gauss diagram]]
[[!redirects Gauss diagrams]]
[[!redirects Gauss code]]
[[!redirects Gauss codes]]
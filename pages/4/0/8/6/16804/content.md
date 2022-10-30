
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

A _chord diagram_ is a graphical representation of an involution or matching on a (cyclically or linearly) ordered set.
Chord diagrams are a basic object of study in [[combinatorics]], and have found applications in diverse areas, notably in [[knot theory]].
They come in both _rooted_ and _unrooted_ versions.

### Illustration

A typical graphical representation of a chord diagram is as a [[circle]] with some marked [[points]] and [[lines]] connecting those points &#8212; something like so:
<center>
[[!include chord diagram > chord diagram unlabelled]]
</center>
If we label the points of the diagram,
<center>
[[!include chord diagram > chord diagram]]
</center>
then the chords can be seen as describing an involution or matching on the set of marked points (swapping $A$ with $C$, $B$ with $D$, and $E$ with $F$).
The marked points are also equipped with a cyclic order coming from the orientation of the circle, and the subtle point is that a chord diagram can have non-trivial [[symmetries]] when considered up to this action of rotation.
For that reason, in many situations it is useful to equip the circle with a distinguished [[basepoint]] (distinct from the marked points), the result being called a "rooted" diagram.
Rooted chord diagrams may be conveniently visualized by "cutting open" the circle at the basepoint.
For example, here we have rooted the chord diagram above at a basepoint lying on the interval AF, and opened up the circle:
<center>
[[!include chord diagram > arc diagram latin]]
</center>
The marked points of a rooted chord diagram are intrinsically equipped with a [[linear order]] ($A \lt B \lt C \lt D \lt E \lt F$) rather than a cyclic order.

Finally, it is also at times useful to consider chord diagrams with marked points which are not attached to any chord; if we think of the diagram as representing an involution, then this allows for the possibility of representing involutions with [[fixed points]].

## Definitions

### Topological definition

A (unrooted) **chord diagram** of type $(n,k)$ is an [[oriented]] [[circle]] with $n$ distinguished pairs of points joined by chords, and $k$ distinguished unattached points, considered up to orientation-preserving [[diffeomorphism]] of the circle.

A **rooting** of a chord diagram is a choice of basepoint on the circle, distinct from the endpoints of any chord.
A **rooted chord diagram** is a chord diagram equipped with a rooting, considered up to orientation-and-basepoint-preserving diffeomorphism of the circle.

### Combinatorial definitions

## Properties

The special property of rooted chord diagrams is that they are [[rigid]] objects, that is, a rooted chord diagram has no [[automorphism]] other than the [[identity morphism]].
Every rooted chord diagram uniquely determines a chord diagram simply by forgetting the basepoint.
Conversely, an unrooted chord diagram of type $(n,k)$ can be rooted in up to $2n+k$ different ways (corresponding to the $2n+k$ intervals between the marked points), but might also have fewer rootings in the case of symmetries.

## Gauss diagrams of ordinary (virtual) knots

Any [[knot diagram]] can be represented faithfully by a certain kind of chord diagram with some extra structure, known as a _Gauss diagram_ [(Polyak and Viro 1994)](#PV94).

Recall that classically, a knot is defined as an embedding of the circle $S^1$ into $\mathbb{R}^3$, which can be represented two-dimensionally by projecting onto the plane $\mathbb{R}^2$ and marking each double point as either an over-crossing or an under-crossing.
One obtains a chord diagram from this knot diagram by considering the original immersing circle and connecting the [[preimages]] of each double point by a chord.
Then, information about crossings can be represented by orienting the chords from over-crossing to under-crossing, while information about the local [[writhe]] of each crossing (in the case of a [[framed knot]]) may be encoded by assigning each chord an additional positive or negative sign.
Finally, fixing a [[base point]] on the original knot gives rise to a Gauss diagram whose underlying chord diagram is naturally rooted.

Once again, this geometric object can be abstracted into a purely combinatorial one, called the _Gauss code_ of the knot (diagram).
To construct the Gauss code, begin by assigning arbitrary labels to the crossings, then run the length of the knot (starting at some arbitrary base point) and output the name of each crossing as you visit it, together with a [[bit]] (or two bits in the case of a framed knot) specifying whether you are at an over-crossing or an under-crossing (of positive or negative writhe).
(In this notation, the involution on the points of the underlying chord diagram is encoded implicitly as a _double-occurrence word_.)

Polyak and Viro called these "Gauss diagrams" after [[Carl Gauss]], who apparently studied the question of which chord diagrams arise from immersions of circles (see the chapter titled "Gauss is back: curves in the plane" of Ghys's _[A singular mathematical promenade](#Ghys16)_).
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

The following book contains an extensive discussion of chord diagrams associated to singular points of analytic curves:

* {#Ghys16} &#201;tienne Ghys, _A Singular Mathematical Promenade_, preliminary version of December 2016. ([arXiv:1612.06373](https://arxiv.org/abs/1612.06373)) ([author pdf](http://perso.ens-lyon.fr/ghys/articles/Promenade.pdf))

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
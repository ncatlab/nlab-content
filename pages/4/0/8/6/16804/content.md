# Idea

A _chord diagram_ is a certain kind of basic combinatorial structure that is considered in various settings such as [[combinatorics]] and [[knot theory]]. Chord diagrams are typically represented graphically as a [[circle]] with some marked [[points]], and [[lines]] connecting those points &#8212; something like so:
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

In many situations, one also wants to consider a [[rigid]] version of chord diagrams, known as _rooted chord diagrams_ or _arc diagrams_, where the set of points is instead [[linearly ordered]].
Graphically, one can visualize this as cutting the circle at a particular segment and "opening up" the diagram.
For example, here we cut the first diagram above at the segment AF
<center>
[[!include chord diagram > arc diagram latin]]
</center>
Relabelling the points to follow the linear order,
<center>
[[!include chord diagram > arc diagram]]
</center>
the rooted chord diagram can now be identified with the involution $(02)(13)(45)$ in $S_6$.

## Related concepts

* [[Vassiliev invariant]]
* [[combinatorial map]]

## References

For more on chord diagrams emphasizing their connection to [[Vassiliev invariants]] of [[singular knots]], see Chapter 6 of

* [[Sergei K. Lando]] and [[Alexander K. Zvonkin]], _Graphs on Surfaces and Their Applications_, Springer, 2004.

as well as

* [[Dror Bar-Natan]], On the Vassiliev knot invariants, _Topology_ 34 (1995), 423-472. ([html](http://www.math.toronto.edu/~drorbn/papers/OnVassiliev/))

* [[Simon Willerton]], Vassiliev invariants and the [[Hopf algebra]] of chord diagrams, Math. Proc. Camb. Phil. Soc. (1996), 119, 55.

* Greg Muller, ["Chord Diagrams and Lie Algebras"](https://cornellmath.wordpress.com/2007/12/25/chord-diagrams-and-lie-algebras/), blog post at _The Everything Seminar_, 25 December 2007.

For chord diagrams and arc diagrams from the perspective of [[combinatorics]], see

* Jacques Touchard. Sur un probl&#232;me de configurations et sur les fractions continues. Canadian Journal of Mathematics 4 (1952), 2-25. ([doi](http://dx.doi.org/10.4153/CJM-1952-001-8))

* Philippe Flajolet and Marc Noy. Analytic combinatorics of chord diagrams. INRIA technical report 3914, March 2000. ([pdf](http://algo.inria.fr/flajolet/Publications/FlNo00.pdf))

* A. Khruzin. Enumeration of chord diagrams. arXiv:math/0008209, August 2000. ([arxiv](http://arxiv.org/abs/math/0008209))

For the relationship to _Gauss diagrams_ in classical [[knot theory]] as well as [[virtual knot theory]], see:

* Michael Polyak and Oleg Viro, Gauss diagram formulas for Vassiliev invariants, _International Mathematics Research Notes_ 1994:11. [pdf](http://www.math.stonybrook.edu/~oleg/math/papers/1994-Polyak-Viro.pdf)

* {#Viro} Oleg Viro, Virtual Links, Orientations of Chord Diagrams and Khovanov Homology, Proceedings of 12th G&#246;kova Geometry-Topology Conference, pp. 184&#8211;209, 2005. [pdf](http://www.pdmi.ras.ru/~olegviro/ggt05-viro.pdf)


[[!redirects arch diagram]]
[[!redirects arc diagram]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is known as the _Banach-Tarski paradox_ is the [[theorem]] ([Banach-Tarski 24](#BanachTarski24)) that the [[axiom of choice]] implies that any two [[bounded subsets]] in [[Euclidean space]] of [[dimension]] $d \geq 3$ may be partitioned by a [[finite number]] of  pairwise congruent [[subsets]].

This is perceived as a [[paradox]] due to its counter-intuitive interpretation, which becomes particularly vivid if one takes one of the two bounded subsets to be the [[disjoint union]] of two copied of the other: In this case the theorem says, intuitively, that it is possible to break up any shape in 3d [[Euclidean space]] into a [[finite number]] of pieces, such that re-assembling these pieces suitably yields not just the original shape, but that and an entire other copy of it.

It has been pointed out that it is not just the use of the [[axiom of choice]] that is responsible for this perceived [[paradox]], but also the point-based concept of [[topological spaces]] as such, see the discussion _In point-free topology_ [below](#InPointFreeTopology).

## In point-free topology
 {#InPointFreeTopology}

It is argued in ([Simpson 12](#Simpson12)) that the Banach-Tarski paradox disappears if one works in [[point-free topology]], hence with [[locales]] instead of just [[topological spaces]]:

> We view spaces of interest as [[locales]], and the notion of "part" is given by the standard notion of [[sublocale]], $[\cdots]$. Every [[topological space]] determines a [[locale]] $[\cdots]$.  However, when a space is viewed as a locale, the notion of [[sublocale]] gives rise to new "parts" of spaces that are not merely subsets, and need  not  be  determined by their points.

> The usual contradictions are avoided $[$this way$]$. The different pieces in  the partitions defined by Vitali and by Banach and Tarski are deeply intertangled with  each  other.  According  to  our  notion  of "part",  two  such  intertangled pieces are not disjoint from each other, so additivity does not apply. An intuitive explanation for the failure of disjointness is that, although two such pieces share no point in common, they nevertheless overlap on the topological “glue” that bonds neighbouring points together.



## References

The original article:

* {#BanachTarski24} [[Stefan Banach]], [[Alfred Tarski]], _Sur la décomposition des ensembles de points en parties respectivement congruentes_  Fundamenta Mathematicae (in French). 6: 244–277, 1924 ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm6/fm6127.pdf))

Textbook account:

* [[Cornelia Druţu]], [[Michael Kapovich]], Chapter 17 of: *Geometric group theory*, Colloquium Publications **63**, AMS 2018 ([ISBN:978-1-4704-1104-6](https://bookstore.ams.org/coll-63/), [pdf](https://courses.maths.ox.ac.uk/node/view_material/35649))


See also:

* Wikipedia, _[Banach-Tarski paradox](https://en.wikipedia.org/wiki/Banach%E2%80%93Tarski_paradox)_

Discussion in [[point-free topology]]:

* {#Simpson12} [[Alex Simpson]], _Measure, randomness and sublocales_, Annals of Pure and Applied Logic Volume 163, Issue 11, November 2012, Pages 1642-1659 ([pdf](http://homepages.inf.ed.ac.uk/als/Research/Sources/mrs.pdf), [doi:10.1016/j.apal.2011.12.014](https://doi.org/10.1016/j.apal.2011.12.014))

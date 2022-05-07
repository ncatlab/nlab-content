
> This entry is about standard round chord diagrams. For [[linear chord diagrams]] or [[horizontal chord diagrams]] or [[Jacobi diagrams]] or [[Sullivan chord diagrams]] see there.

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--

\tableofcontents

## Idea
 {#Idea}

A _chord diagram_ is a finite trivalent undirected [[graph]] with an embedded [[orientation|oriented]] [[circle]] and all [[vertices]] on that circle, regarded modulo cyclic identifications, if any. 

A typical chord diagram looks like this:

<center>
<img src="https://ncatlab.org/nlab/files/ChordDiagram.jpg" width="300">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

Chord diagrams are a basic object of study in [[combinatorics]] with remarkably many applications in [[mathematics]] and [[physics]], notably in [[knot theory]] and [[Chern-Simons theory]].

If also (trivalent) internal vertices are considered, one speaks of _[[Jacobi diagrams]]_.


## Definitions

Chord diagrams can be defined both in topological terms, which formalize the graphical intuition, as well as in purely combinatorial terms.
We present only the combinatorial definition here, starting from _[[rooted chord diagrams]]_ and using those to define unrooted chord diagrams, rather than the other way around.

(For topological definitions of both unrooted and [[rooted chord diagrams]], see for example Chapter 6 of [Lando and Zvonkin]({#LandoZvonkin}), or Definition 1.5 of [Bar-Natan 1995](#Bar-Natan1995) for the unrooted case.)


### A combinatorial definition

**Rooted chord diagrams**

If we would label the points of a chord diagram,
<center>
[[!include chord diagram > chord diagram]]
</center>
then the chords can be seen as describing a matching (or equivalently, an [[involution]]) on the set of marked points which pairs (or equivalently, _swaps_) $A$ with $C$, $B$ with $D$, and $E$ with $F$.



A subtle point is that a chord diagram can have non-trivial [[symmetries]] when considered up to this action of rotation.
For that reason, in many situations it is useful to equip the circle with a distinguished [[basepoint]] (distinct from the marked points), the result being called a _[[rooted chord diagram]]_.
Rooted chord diagrams may be conveniently visualized by "cutting open" the circle at the basepoint.
For example, here we have rooted the chord diagram above at a basepoint lying on the interval AF, and opened up the circle:
<center>
[[!include chord diagram > arc diagram latin]]
</center>
The marked points of a [[rooted chord diagram]] are intrinsically equipped with a [[linear order]] ($A \lt B \lt C \lt D \lt E \lt F$) rather than a cyclic order.

Finally, it is also at times useful to consider chord diagrams with marked points which are not attached to any chord; if we think of the diagram as representing an involution, then this allows for the possibility of representing involutions with [[fixed points]].


+-- {: .un_defn}
###### Definition

A **[[rooted chord diagram]]** of order $n$ is a [[surjective]] [[monotone function]]
$$
  D : \underset{n\,\text{times}}{\underbrace{[0,1] + \dots + [0,1]}} \twoheadrightarrow [0,2n-1]
$$
from the $n$-fold [[coproduct]] of the [[walking arrow]] (seen as a 2-element [[poset]]) into the [[linear order]] $[0,2n-1] = \{ 0 \lt \dots \lt 2n-1 \}$.
The symmetric group $S_n$ acts freely on the domain $[0,1] + \dots + [0,1]$ of a rooted chord diagram of order $n$, and we consider two rooted chord diagrams to be isomorphic if they only differ by precomposition with such a permutation action.

=--

Equivalently, a rooted chord diagram of order $n$ is a way of arranging the elements of $[0,2n-1]$ into a collection of (necessarily mutually disjoint) ordered pairs $(D_{10}, D_{11}), \dots, (D_{n0},D_{n1})$, where $D_{i0} \lt D_{i1}$ for each $1 \le i \le n$.

Equivalently, a rooted chord diagram of order $n$ is a [[shuffle]] of $n$ distinct 2-letter words $\bar x x$, $\bar y y$, $\bar z z$, etc., considered up to [[alpha-conversion]]. Under this view, rooted chord diagrams are also sometimes referred to as **double-occurrence words**. (For example, the rooted chord diagram in the illustration above can be encoded as the double-occurrence word $\bar x \bar y x y \bar z z$.)

**Unrooted chord diagrams**

Intuitively, the [[cyclic group]] $C_{2n}$ acts on rooted chord diagrams
$$
  D : \underset{n\,\text{times}}{\underbrace{[0,1] + \dots + [0,1]}} \twoheadrightarrow [0,2n-1]
$$
by acting on the codomain $[0,2n-1]$ via the map $\tau_n = x \mapsto x-1\,(\mod{2n})$.
This is not quite well-typed, however, since the composite function $\tau_n \circ D$ is not quite order-preserving.
It is easiest to define the action of $C_{2n}$ in terms of the view of a rooted chord diagram $D$ as a collection of ordered pairs $(D_{10}, D_{11}), \dots, (D_{n0},D_{n1})$.
The action of $\tau_n$ is defined on each pair by
$$
 \tau_n(x,y) = \begin{cases}(x-1,y-1) & x\gt 0 \\ (y-1,2n-1) & x = 0 \end{cases}
$$
and this extends to an action on rooted chord diagrams by acting independently on the pairs.

+-- {: .un_defn}
###### Definition

An **unrooted chord diagram** of order $n$ is a rooted chord diagram of order $n$, considered up to the action of $\tau_n$.

=--

### 4T relation and weight systems
 {#4TRelationAndWeightSystems}

Often one is interested in chord diagrams only modulo the [[4T relation]]:

For $R \in $ [[CRing]] a [[commutative ring]], let $R\langle \mathcal{D}^c \rangle$ denote the $R$-[[linear span]] of the [[set]] $\mathcal{D}^c$ of [[chord diagrams]]. 

Then one traditionally writes

\[
  \label{QuotientSpaceBy4T}
  \mathcal{A}^c 
    \;\coloneqq\;
  R\langle \mathcal{D}^c \rangle/4T 
\]

for the [[quotient spaces]] of the [[linear span]] of [[chord diagrams]] by the [[4T relations]]:

<center>
<img src="https://ncatlab.org/nlab/files/4TRelationsForRoundChordDiagrams.jpg" width="220">
</center>

Hence:

<center>
<img src="https://ncatlab.org/nlab/files/ChordDiagramsModulo4TRelations.jpg" width="800">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

A [[linear function]]

$$
  w \;\colon\; \mathcal{A}^c \longrightarrow R
  \,,
$$

-- hence a plain $R$-valued [[function]] on the [[set]] $\mathcal{D}^c$ of [[chord diagrams]] which is [[invariant]] under the [[4T relation]] --

is called a _[[framed weight system]]_. See there for more.

### Trace from horizontal chord diagrams
 {#TraceFromHorizontalChordDiagrams}

Given a [[horizontal chord diagram]] on $n$ strands and given any choice of [[cyclic permutation]] of $n$ elements, the [[trace of horizontal to round chord diagrams]] is the [[round chord diagram]] obtained by gluing the ends of the strands according to the cyclic permutation, and retaining the chords in the evident way.

The following graphics shows basic examples of the trace operation for [[cyclic permutation]] of strands one step to the right:

<center>
<img src="https://ncatlab.org/nlab/files/TracingHorizontalChordDiagramsExamplesI.jpg" width="700">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

This defines a [[function]]

$$
  tr \;\colon\; \mathcal{C}^{pb} \longrightarrow \mathcal{C}^c
$$

from the [[set]] of [[horizontal chord diagrams]] to the set of [[round chord diagrams]].


## Properties

### Representation as involutions

Every rooted chord diagram 
$$
  D : \underset{n\,\text{times}}{\underbrace{[0,1] + \dots + [0,1]}} \twoheadrightarrow [0,2n-1]
$$
uniquely determines a fixed point free involution
$$
  i_D : \{0,\dots,2n-1\} \to \{0,\dots,2n-1\}
$$
swapping the elements of each chord,
$$
  i_D(x) = \begin{cases}y & (x,y) \in D \\ y & (y,x) \in D\end{cases}
$$
and conversely, any such involution uniquely determines a rooted chord diagram up to isomorphism.
In particular, there are a double-factorial number
$$
 (2n-1)!! = (2n-1)(2n-3)\cdots 1
$$
of distinct isomorphism classes of rooted chord diagrams of order $n$.

### Symmetries

Every rooted chord diagram uniquely determines a chord diagram simply by forgetting the basepoint.
Conversely, an unrooted chord diagram of order $n$ can be rooted in up to $2n$ different ways (corresponding to the $2n$ intervals between the marked points), but might also have fewer rootings in the case of symmetries.

### Relation to Jacobi diagrams
 {#RelationToChernSimonsDiagrams}

[[chord diagrams modulo 4T are Jacobi diagrams modulo STU]]:

<center>
<img src="https://ncatlab.org/nlab/files/ChordDiagModulo4TAreJAcobiDiagModuloSTU.jpg" width="840">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


## Gauss diagrams of ordinary (virtual) knots

Any [[knot diagram]] can be represented faithfully by a certain kind of chord diagram with some extra structure, known as a _Gauss diagram_ [(Polyak and Viro 1994)](#PV94).

Recall that classically, a knot is defined as an embedding of the circle $S^1$ into $\mathbb{R}^3$, which can be represented two-dimensionally by projecting onto the plane $\mathbb{R}^2$ and marking each double point as either an over-crossing or an under-crossing.
One obtains a chord diagram from this knot diagram by considering the original immersing circle and connecting the [[preimages]] of each double point by a chord.
Then, information about crossings can be represented by orienting the chords from over-crossing to under-crossing, while information about the local [[writhe]] of each crossing (in the case of a [[framed knot]]) may be encoded by assigning each chord an additional positive or negative sign.
Finally, fixing a [[base point]] on the original knot gives rise to a Gauss diagram whose underlying chord diagram is naturally rooted.

Once again, this geometric object can be abstracted into a purely combinatorial one, called the _Gauss code_ of the knot (diagram).
To construct the Gauss code, begin by assigning arbitrary labels to the crossings, then run the length of the knot (starting at some arbitrary base point) and output the name of each crossing as you visit it, together with a [[bit]] (or two bits in the case of a framed knot) specifying whether you are at an over-crossing or an under-crossing (of positive or negative writhe).
The underlying (rooted) chord diagram of the knot is thus encoded as a double-occurrence word.

Polyak and Viro called these "Gauss diagrams" after [[Carl Gauss]], who apparently studied the question of which chord diagrams arise from immersions of circles (see the chapter titled "Gauss is back: curves in the plane" of Ghys's _[A singular mathematical promenade](#Ghys16)_).
This question also played a foundational role in [[virtual knot theory]] &mdash; indeed, according to [Kauffman (1999)](#Kauffman1999), the "fundamental combinatorial motivation" for the definition of virtual knots was the idea that it should be possible to interpret an _arbitrary_ Gauss diagram as encoding a knot, now no longer seen as an embedding of $S^1$ into $\mathbb{R}^3$, but into a thickened surface of arbitrary genus.

## Chord diagrams of singular knots

By an analogous mechanism, any [[singular knot]] $K$ with $n$ simple double points (i.e., points where the knot intersects itself transversally) gives rise to a chord diagram $c(K)$ with $n$ chords, by connecting the preimages of these double points.
This chord diagram $c(K)$ of course does not faithfully represent the original knot $K$ (e.g., it does not include any information about over-crossings and under-crossings).
However, such chord diagrams nonetheless play an important role in the theory of [[Vassiliev invariants]], by the theorem that the value of a Vassiliev invariant $v$ of degree $\le n$ on any singular knot $K$ with $n$ simple double points depends only on the chord diagram $c(K)$.

## Related concepts

[[!include chord diagrams and weight systems -- table]]


* [[combinatorial map]]



## References

### General

Early consideration of round chord diagrams (as "linked diagrams"):

* Paul R. Stein, *On a class of linked diagrams, I. Enumeration*, Elsevier Journal of Combinatorial Theory, Series A Volume 24, Issue 3, May 1978, Pages 357-366 (<a href="https://doi.org/10.1016/0097-3165(78)90065-1">doi:10.1016/0097-3165(78)90065-1</a>)

* Paul R. Stein, C. J. Everett, *On a class of linked diagrams II. asymptotics*, Discrete Mathematics Volume 21, Issue 3, 1978, Pages 309-318 (<a href="https://doi.org/10.1016/0012-365X(78)90162-0">doi:10.1016/0012-365X(78)90162-0</a>)

Original discussion of chord diagrams in the context of [[Vassiliev invariants]]:

* {#BarNatan95} [[Dror Bar-Natan]], _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

* {#BarNatan96} [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))

Textbook accounts:

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 4 of:  _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

* [[David Jackson]], [[Iain Moffat]], Section 11 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))

Lecture notes:

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], Alexander Stoimenow, _The Fundamental Theorem of Vassiliev Invariants_ ([arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009))


For chord diagrams and arc diagrams from the perspective of [[combinatorics]], see:

* Jacques Touchard, _Sur un probl&#232;me de configurations et sur les fractions continues_ Canadian Journal of Mathematics 4 (1952), 2-25. ([doi](http://dx.doi.org/10.4153/CJM-1952-001-8))

* Philippe Flajolet and Marc Noy, _Analytic combinatorics of chord diagrams_, INRIA technical report 3914, March 2000. ([pdf](http://algo.inria.fr/flajolet/Publications/FlNo00.pdf))

* A. Khruzin, _Enumeration of chord diagrams_ arXiv:math/0008209, August 2000. ([arxiv](http://arxiv.org/abs/math/0008209))

For the relationship to Gauss diagrams in classical and [[virtual knot theory]], see:

* {#PV94} Michael Polyak and Oleg Viro, Gauss diagram formulas for Vassiliev invariants, _International Mathematics Research Notes_ 1994:11. [pdf](http://www.math.stonybrook.edu/~oleg/math/papers/1994-Polyak-Viro.pdf)

* {#Kauffman1999} [[Louis Kauffman]], Virtual Knot Theory, _European Journal of Combinatorics_ (1999) 20, 663-691. [pdf](http://homepages.math.uic.edu/~kauffman/VKT.pdf)

* {#Viro05} Oleg Viro, Virtual Links, Orientations of Chord Diagrams and Khovanov Homology, Proceedings of 12th G&#246;kova Geometry-Topology Conference, pp. 184&#8211;209, 2005. [pdf](http://www.pdmi.ras.ru/~olegviro/ggt05-viro.pdf)

* [Gauss codes](http://katlas.org/wiki/Gauss_Codes) at the Knot Atlas.

For the connection to [[Vassiliev invariants]] of [[singular knots]], see:

* {#LandoZvonkin} [[Sergei K. Lando]] and [[Alexander K. Zvonkin]], _Graphs on Surfaces and Their Applications_, Springer, 2004. (Chapter 6.)

* {#Bar-Natan1995} [[Dror Bar-Natan]], On the Vassiliev knot invariants, _Topology_ 34 (1995), 423-472. ([html](http://www.math.toronto.edu/~drorbn/papers/OnVassiliev/))

* [[Simon Willerton]], Vassiliev invariants and the [[Hopf algebra]] of chord diagrams, Math. Proc. Camb. Phil. Soc. (1996), 119, 55.

* Greg Muller, ["Chord Diagrams and Lie Algebras"](https://cornellmath.wordpress.com/2007/12/25/chord-diagrams-and-lie-algebras/), blog post at _The Everything Seminar_, 25 December 2007.

The following book contains an extensive discussion of chord diagrams associated to singular points of analytic curves:

* {#Ghys16} &#201;tienne Ghys, _A Singular Mathematical Promenade_, preliminary version of December 2016. ([arXiv:1612.06373](https://arxiv.org/abs/1612.06373)) ([author pdf](http://perso.ens-lyon.fr/ghys/articles/Promenade.pdf))

On [[Vassiliev invariants]] of [[braid group|braids]] via [[chord diagrams]]:

* [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))

Relation to [[spherical curves]]:

* Noboru Ito, _Based chord diagrams of spherical curves_ ([arXiv:2004.12121](https://arxiv.org/abs/2004.12121))

See also:

* Ali Assem Mahmoud, Karen Yeats, _Connected Chord Diagrams and the Combinatorics of Asymptotic Expansions_ ([arXiv:2010.06550](https://arxiv.org/abs/2010.06550))




[[!include weight systems on chord diagrams in physics]]


[[!redirects chord diagrams]]

[[!redirects Gauss diagram]]
[[!redirects Gauss diagrams]]
[[!redirects Gauss code]]
[[!redirects Gauss codes]]
[[!redirects double-occurrence word]]
[[!redirects double-occurrence words]]

[[!redirects round chord diagram]]
[[!redirects round chord diagrams]]

[[!redirects algebra of chord diagrams]]
[[!redirects algebras of chord diagrams]]




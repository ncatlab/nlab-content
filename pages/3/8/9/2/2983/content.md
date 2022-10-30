
#Contents#
* table of contents
{:toc}

## Idea

A **building** (also **Tits building**, **Bruhat--Tits building**) is a combinatorial and geometric structure which simultaneously generalizes certain aspects of [[flag manifold]]s, finite [[projective plane]]s, and [[Riemannian manifold|Riemannian]] [[symmetric space]]s.

Initially introduced by [[Jacques Tits]] as a means to understand the structure of [[exceptional Lie group]]s, the theory has also been used to study the geometry and topology of [[homogeneous space]]s of p-adic Lie groups and their discrete subgroups of symmetries, in the same way that [[tree]]s have been used to study [[free group]]s.


> (for the moment the above text is simply a copy of the intro of the [wikipedia entry](http://en.wikipedia.org/wiki/Building_%28mathematics%29))

See also

* [[toddtrimble:Buildings for category theorists]] 



## Introduction 

This page is intended to be a supplementary exposition of the page [[toddtrimble:Buildings for category theorists]], at least for now. So we will try to explain the aspects of buildings that the kind reader would like to know in order to understand the category theoretic construction over there.
The notion of a building relies heavily on that of a Coxeter group, which we will not explain here, see for example

* [[Wikipedia: [Coxeter groups] (http://en.wikipedia.org/wiki/Coxeter_group) ]]

and especially, for an elementary and readable introduction,

* [[Humphreys, James E.: Reflection groups and Coxeter groups.(Cambridge Studies in Advanced Mathematics 29, 1990, [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0725.20028&format=complete
) )]]

Taking the notion of Coxeter groups for granted, there are currently three different viewpoints of thinking about a building. 
From now on, let W be a Coxeter group and S the set of generators, which may be finite or infinite: In case we need S to be finite we will mention it explicitly. We will call the tuple (W, S) a **Coxeter system** and let $l_S$ be the **length function**
 of W with respect to S.

### Buildings from three Viewpoints

The three viewpoints are distinguished by how one thinks about chambers.

#### Simplicial Complexes

In Tits' original approach, a building is a simplicial complex satisfying additional axioms. Chambers are maximal simplices.

#### Combinatorial Approach

Note that this is not a firmly established term in the literature.
This more modern approach originated with

* [Jaques Tits: A local approach to buildings, The geometric vein (C. Davis, B.Gr&#252;nbaum, and F. A. Sherk, eds.), Springer-Verlag, New York, 1981, pp. 519&#8211;547.]

Buildings are viewed as sets of chambers with a Coxeter-group-valued distance function satisfying certain axioms. Chambers are elements of an abstract set - more is not needed in the definition. As an alternative, chambers can be viewed as vertices of a graph. This is the point of view we will expand in future versions of this page.

#### Buildings as Metric Spaces

The following paper

* [M. W. Davis, Buildings are CAT(0), Geometry and cohomology in group theory
(P. H. Kropholler, G. A. Niblo, and R. St&#246;hr, eds.), London Mathematical
Society Lecture Note Series, vol. 252, Cambridge University Press, Cambridge,
1998, pp. 108&#8211;123.]

explains that every building has a geometric realization that admits a CAT(0) metric, which means that it has metric properties analogous to those of complete simply connected Riemannian manifolds of nonpositive curvature.

* [Wikipedia: [CAT(k) spaces] (http://en.wikipedia.org/wiki/CAT%28k%29_space)]

From this viewpoint chambers are metric spaces.

## Definition

### According to the Combinatorial Approach

This definition is due to

* [Jaques Tits: Twin buildings and groups of Kac-Moody type, Groups, combinatorics
& geometry (M. Liebeck and J. Saxl, eds.), London Mathematical Society
Lecture Note Series, vol. 165, Cambridge University Press, Cambridge, 1992,
pp. 249&#8211;286.]

Let (W, S) be a Coxeter system (see above). 

**Definition:**

A **building of type (W, S)** is a pair (C, $\delta$) of a nonempty set C, whose elements are called **chambers**, and a function 
$\delta$: CxC $\to$ W
subject to the following axioms:

* WD1, "identity of indiscernibles": $\delta$(C, D) = 1 iff C = D

* WD2, "triangle inequality": Let A, B, C be chambers and $\delta$(A, B) = w, $\delta$(C, A) = s, then $\delta$(C, B) = either w or sw. If in addition $l_S$(sw) = $l_S$(w) + 1, then $\delta$(C, B) = sw.

* WD3, "TODO: insert analogy here": Let A, B be chambers and $\delta$(A, B) = w, then for any s $\in$ S there is a chamber C such that $\delta$(C, A) = s and $\delta$(C, B) = sw

This definition is equivalent from the one usually given from the simplicial viewpoint, but we will not prove that here, see e.g. the book by Abramenko and Brown in the introductory references.
In the following paragraphs we will explain a few simple consequences of this definition, and introduce concepts that will allow us to identify the chambers and their "distance" relation with vertices and edges of a graph respectively (TODO: not done yet).

But first let us note that the axioms WD1 and WD2 are somewhat similar to the axioms defining the distance function of a metric space, one notable difference is that the function $\delta$ of a building takes values in the Coxeter group W of the building rather than in the nonnegative real numbers. For this reason, from the combinatorial viewpoint, buildings are sometimes called **W-metric spaces**.

In order to distinguish the two viewpoints, which is, given their equivalence, strictly speaking not necessary, some authors will talk about **W-metric buildings** and **simplicial buildings**.

**Remark:** 
If the Coxeter group W is finite, the building is called **spherical**. The reason for this is, that in this case, for $n := |S|$, the Coxeter group W has a faithful representation in the group of reflections on $\Re^n$. Reflections are in 1:1 correspondence to (linear) hyperplanes, the reflections that are images of the elements of the Coxeter group define a triangulation of the unit sphere of $\Re^n$, such that the resulting simplicial complex provides a geometric realization of the building.

## References

### Introductory

For a short, gentle and geometrical introduction, see:

* [[John Baez]], This Week's Finds in Mathematical Physics, [week 263] (http://math.ucr.edu/home/baez/week263.html) second half.

* Wikipedia on [buildings] (http://en.wikipedia.org/wiki/Bruhat-Tits_building)

An introductory textbook that starts with explaining Coxeter groups is this:

* Abramenko, Peter; Brown, Kenneth S.: Buildings. Theory and applications. (Springer 2008, [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:pre05288866&format=complete) )

A short introduction to spherical buildings (this notion will be explained below):

* Richard M. Weiss: The Structure of Spherical Buildings. (Princeton University Press 2004, [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1061.51011&format=complete) )


[[!redirects buildings]]

[[!redirects Tits building]]
[[!redirects Bruhat-Tits building]]
[[!redirects Bruhat–Tits building]]
[[!redirects Bruhat--Tits building]]

[[!redirects Tits buildings]]
[[!redirects Bruhat-Tits buildings]]
[[!redirects Bruhat–Tits buildings]]
[[!redirects Bruhat--Tits buildings]]

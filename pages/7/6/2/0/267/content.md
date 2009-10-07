<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>


Handling higher structures such as [[higher category theory|higher categories]] usually involves conceiving them as  conglomerates of _cells_ of certain _shape_.

The most familiar of these possible shapes are

* [[globe|globes]];

* [[simplex|simplices]];

* [[cube|cubes]]. 

There are corresponding categories whose 

* objects are the "standard cellular shapes" of the given sort: [[globe|globes]], [[simplex|simplices]], [[cube|cubes]], respectively, one for each natural number $n \in \mathbb{N}$ and usually denoted $[n]$

* morphisms are generated from all possible ways of mapping these standard cellular shapes to each other such that their cellular structure is preserved;

* and composition of such morphisms is subject to the relations which are inherited from the geometric meaning of these maps, which says for instance that the left boundary of the top boundary of a [[cube]] is the same as the top boundary of its left boundary -- these are the  _globular identities_, the _simplicial identities_ and the _cubical identities_, respectively.


The resulting categories of basic cellular shapes are

* the _[[globe category]]_ $\circ$;

* the _[[simplex category]]_ $\triangle$;

* the _[[cube category]]_ $\square$.


A higher structure based on these geometric sheapes is a [[presheaf]] on one of these categories. These are called

* [[globular set]]s;

* [[simplicial set]]s;

* [[cubical set]]s,

respectively. 

Other notions of geometric shape which have been found useful in higher order category theory include [[opetope]]s (based on [[operad]] theory, and invented by Baez-Dolan), [[multitope]]s (due to Hermida-Makkai-Power), and the shapes encapsulated in Joyal's [[disk category]] $\Theta$ (which include globes and simplices as special cases). 

In many definitions of [[higher category theory|higher categories]] an [[infinity-category]] is one of these presheaves

* either equipped with _extra properties_ in the [[geometric definition of higher category|geometric definition of higher categories]];

* or equipped with _extra structure_ in the [[algebraic definition of higher category|algebraic definition of higher categories]]. 

For instance [[omega-category|omega-categories]] are based on [[globular set]]s and [[n-fold category|n-fold categories]] on [[cubical set]]s, while most [[geometric definition of higher category|geometrically defined]] higher categories such as [[quasi-category|quasi-categories]] are based on the [[simplicial set]]s, thought of as a [[nerve]].

However, [[Ronnie Brown]] writes: For the work on higher homotopy groupoids and their applications to higher homotopy van Kampen theorems we found cubical methods essential. In the first of the following papers, we use a higher homotopy cubical $\omega$-groupoid with connections of a filtered space, while the second paper uses a fundamental cat$^n$-group of an $n$-cube of pointed spaces, giving an $n$-fold groupoid in the category of groups. The setting up of these structures is non-trivial,  highly geometric and essential for the homotopical applications. The paper with Loday also uses multisimplicial techniques. 

References: 

* R. Brown and P. J. Higgins, Colimit theorems for relative homotopy groups,  J. Pure Appl. Algebra, 22 (1981) 11-41.

* R. Brown and J.-L. Loday, Van Kampen theorems for diagrams of spaces,  Topology 26 (1987) 311-334.

* [This Week's Finds in Mathematical Physics (Week 242)](http://golem.ph.utexas.edu/category/2006/12/this_weeks_finds_in_mathematic_4.html#c006655) (Discussion at the n-Cafe)
The category [[Top]] of [[topological space|topological spaces]] lacks many good categorical properties.  It is [[complete category|complete]] and [[cocomplete category|cocomplete]], but:

* not [[cartesian closed category|cartesian closed]] or [[locally cartesian closed category|locally cartesian closed]],
* not [[locally presentable category|locally presentable]], and
* not a [[topos]] or even a [[quasitopos]].

The lack of cartesian closure and, to a lesser extent, local presentability, is especially problematic for [[homotopy theory]].  Many different solutions have been proposed, generally involving either restricting to a subcategory of [[Top]] (usually [[reflective subcategory|reflective]] or coreflective, so that it inherits completeness and cocompleteness), enlarging it to a supercategory, or some combination thereof.  Most involve restricting the topologies to those that can be specified on "small" (and in particular, compact) subsets.  Here are some examples.

* The most common approach among algebraic topologists today is to use the subcategory of [[compactly generated space|compactly generated spaces]], which is cartesian closed, but not locally cartesian closed.  It is a coreflective subcategory of a reflective subcategory of $Top$.

* The subcategory of [[Delta-generated spaces]], recently proposed by J. H. Smith, is both cartesian closed and locally presentable.

* An approach of mainly historical interest is to use [[quasitopological space|quasitopological spaces]], an enlargement of $Top$ which is cartesian closed.

* The category $PsTop$ of [[pseudotopological space|pseudotopological spaces]] (also called Choquet spaces) is a quasitopos containing $Top$ as a full reflective subcategory.  In particular, $PsTop$ is [[locally cartesian closed category|locally cartesian closed]] (but not locally presentable).

* In his paper _On a topological topos_, Peter Johnstone described a [[Grothendieck topos]] $E$ which contains the category of [[sequential space|sequential]] topological spaces as a full reflective subcategory which is closed under many colimits (including all those used to define [[CW complex|CW complexes]].  Since $E$ is a Grothendieck topos, it is locally presentable and locally cartesian closed.  Moreover, the [[geometric realization]] and [[singular complex]] functors form a [[geometric morphism]] between $E$ and the category of [[simplicial set|simplicial sets]].

* One can just forget topological spaces and use the category of [[simplicial set]]s as the subject of homotopy theory. That every topological space has a simplicial set as its [[singularization]] now becomes an application of homotopy theory, rather than the starting point. 

#References#

* J. P. May, _A Concise Course in Algebraic Topology_ (Chapter 5, for compactly generated spaces)

* O. Wyler, _Convenient categories for topology_

* L. Fajstrup and J. Rosicky, _A convenient category for directed homotopy_ (for delta-generated spaces)

* E. Spanier, _Quasi-topologies_ (for quasi-topological spaces)

* O. Wyler, _Lecture notes on topoi and quasitopoi_ (for pseudotopological spaces)

* P. Johnstone, _On a topological topos_


> For more see at *[[convenient category of topological spaces]]*.

By a "nice" or "[[convenient category of topological spaces|convenient]]" category of space one means a [[category]] that subsumes at least most of the given kinds of [[spaces]] of interest (typically: [[topological space]]) but possibly also less well-behaved spaces, such that the category itself becomes well behaved.

The point is that the default category [[Top]] of [[topological spaces]] lacks many good category-theoretic properties: It is [[complete category|complete]], [[cocomplete category|cocomplete]] and [[extensive category|extensive]], but:

* not [[cartesian closed category|cartesian closed]] or [[locally cartesian closed category|locally cartesian closed]],

* not [[locally presentable category|locally presentable]], and

* not a [[topos]] or even a [[quasitopos]],

* nor is it even a [[pretopos]] or an [[exact category|exact]] or even a [[regular category]]. 

The lack of cartesian closure and, to a lesser extent, local presentability, is especially problematic for [[homotopy theory]].  Many different solutions for repairing lack of cartesian closure have been proposed, generally involving either restricting to a subcategory of [[Top]] (usually [[reflective subcategory|reflective]] or coreflective, so that it inherits completeness and cocompleteness), enlarging it to a supercategory, or some combination thereof.  Most involve restricting the topologies to those that can be specified on "small" (and in particular, [[compact space|compact]]) subsets.

In particular, a [[convenient category of topological spaces]] is, in the technical sense of the [nLab](http://ncatlab.org/nlab/show/HomePage), a cartesian-closed category of spaces together with some other useful properties (q.v.). 


## Examples

* The frequent choice among algebraic topologists today is to use the subcategory of [[compactly generated space|compactly generated spaces]], which is cartesian closed, but not locally cartesian closed.  It is a coreflective subcategory of a reflective subcategory of $Top$.

* Homotopy theorists often find the category of [[simplicial sets]] to be an especially nice environment. It is for example a [[Grothendieck topos]], thus a [[locally cartesian closed category]] and satisfying all [[exactness properties]] one expects of toposes, and is a [[locally presentable category]]. The fact that every topological space has a simplicial set as its [[singularization]] then becomes an application of the homotopy theory of simplicial sets to the study of topological spaces, rather than a way to use simplicial sets to study the homotopy theory of topological spaces. 

  For more on this see _[[Top]]_, _[[homotopy theory]]_ and [[infinity-groupoid]].

* The subcategory of [[Delta-generated topological spaces]] is also both cartesian closed and locally presentable.

* An approach of mainly historical interest is to use [[quasitopological space|quasitopological spaces]], an enlargement of $Top$ which is cartesian closed.

* The category $PsTop$ of [[pseudotopological space|pseudotopological spaces]] (also called Choquet spaces) is a quasitopos containing $Top$ as a full reflective subcategory.  In particular, $PsTop$ is [[locally cartesian closed category|locally cartesian closed]] (but not locally presentable).

* In his paper _On a topological topos_, Peter Johnstone described a [[Grothendieck topos]] $E$ which contains the category of [[sequential space|sequential]] topological spaces as a full reflective subcategory which is closed under many colimits (including all those used to define [[CW complex|CW complexes]]).  Again, since $E$ is a Grothendieck topos, it is locally presentable and locally cartesian closed.  Moreover, the [[geometric realization]] and [[singular complex]] functors form a [[geometric morphism]] between $E$ and the category of [[simplicial set|simplicial sets]].  The "underlying set" functor $E\to Set$ is not [[faithful functor|faithful]], but it is faithful on the full subcategory of [[subsequential space|subsequential spaces]], which contain the sequential spaces and form a [[quasitopos]].  See [[topological topos]].

* The category of [[compact Hausdorff spaces]] is perfectly nice for some purposes. While neither cartesian closed nor locally presentable, it is however a complete and cocomplete [[pretopos]]. In this way it is both a category of [[nice topological spaces]] and a nice category of topological spaces, thus an exception proving the "rule" described at [[dichotomy between nice objects and nice categories]]. 

* The category of [[locales]] and the full subcategory of [[sober spaces]] can be considered nice for certain purposes. The category of locales is extensive and is opposite to the category of [[frames]] (which is monadic over $Set$ and thus [[exact category|exact]]). The category of locales is however neither cartesian closed nor locally presentable, although there is a nice description of [[exponential object|exponentiable locales]]. Johnstone's Stone Spaces gives an account of topology via locale theory. 

* John Milnor proposed the category of spaces having the homotopy type of a CW complex as a nice category of spaces. If $X$ and $Y$ are objects and $X$ is compact, then there is an exponential object $Y^X$ in this category. This could also be considered a category of [[nice topological spaces]] (which to reiterate, is conceptually distinct from being a nice category of spaces). 

* The category of [[algebraic lattices]], considered as a full subcategory of $T_0$-[[separation axioms|spaces]], is a nice cartesian closed category of spaces in which to do [[domain theory]]. Related to this is the category of [[equilogical spaces]], which is locally cartesian closed (and thus also regular) and arises as the [[exact completion|reg/ex completion]] of the category of $T_0$ spaces. 

* The category of [[condensed sets]] is a nice category of spaces which is a [[well-powered category|well-powered]], [[locally cartesian closed]] [[pretopos|infinitary-pretopos]] in which one can do [[condensed mathematics]]. Related to this is the category of [[pyknotic sets]] and the category of [[light condensed sets]], both of which form [[Grothendieck toposes]]. 

## References

* [[Peter May]], _[[A Concise Course in Algebraic Topology]]_ (Chapter 5, for compactly generated spaces)

* O. Wyler, _Convenient categories for topology_

* L. Fajstrup and J. Rosicky, _A convenient category for directed homotopy_ (for Delta-generated spaces)

* E. Spanier, _Quasi-topologies_ (for quasi-topological spaces)

* O. Wyler, _Lecture notes on topoi and quasitopoi_ (for pseudotopological spaces)

* [[Peter Johnstone]], _On a [[topological topos]]_ 

* [[Peter Johnstone]], [[Stone Spaces]]

* J. Milnor, On spaces having the homotopy type of a CW-complex, Trans. Amer. Math. Soc. 90, no. 2 (1959), 272-280. 


[[!redirects nice categories of spaces]]


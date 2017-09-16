The category [[Top]] of [[topological space|topological spaces]] lacks many good categorical properties.  It is [[complete category|complete]] and [[cocomplete category|cocomplete]], but:

* not [[cartesian closed category|cartesian closed]] or [[locally cartesian closed category|locally cartesian closed]],
* not [[locally presentable category|locally presentable]], and
* not a [[topos]] or even a [[quasitopos]].

The lack of cartesian closure and, to a lesser extent, local presentability, is especially problematic for [[homotopy theory]].  Many different solutions have been proposed, generally involving either restricting to a subcategory of [[Top]] (usually [[reflective subcategory|reflective]] or coreflective, so that it inherits completeness and cocompleteness), enlarging it to a supercategory, or some combination thereof.  Most involve restricting the topologies to those that can be specified on "small" (and in particular, compact) subsets.  Here are some examples.

* The most common approach among algebraic topologists today is to use the subcategory of [[compactly generated space|compactly generated spaces]], which is cartesian closed, but not locally cartesian closed.  It is a coreflective subcategory of a reflective subcategory of $Top$.

* The subcategory of [[Delta-generated space]]s, recently proposed by J. H. Smith, is both cartesian closed and locally presentable.

* An approach of mainly historical interest is to use [[quasitopological space|quasitopological spaces]], an enlargement of $Top$ which is cartesian closed.

* The category $PsTop$ of [[pseudotopological space|pseudotopological spaces]] (also called Choquet spaces) is a quasitopos containing $Top$ as a full reflective subcategory.  In particular, $PsTop$ is [[locally cartesian closed category|locally cartesian closed]] (but not locally presentable).

* In his paper _On a topological topos_, Peter Johnstone described a [[Grothendieck topos]] $E$ which contains the category of [[sequential space|sequential]] topological spaces as a full reflective subcategory which is closed under many colimits (including all those used to define [[CW complex|CW complexes]].  Since $E$ is a Grothendieck topos, it is locally presentable and locally cartesian closed.  Moreover, the [[geometric realization]] and [[singular complex]] functors form a [[geometric morphism]] between $E$ and the category of [[simplicial set|simplicial sets]].

* One can just forget topological spaces and use the category of [[simplicial set]]s as the subject of homotopy theory. That every topological space has a simplicial set as its [[singularization]] now becomes an application of homotopy theory, rather than the starting point. 

#References#

* J. P. May, _A Concise Course in Algebraic Topology_ (Chapter 5, for compactly generated spaces)

* O. Wyler, _Convenient categories for topology_

* L. Fajstrup and J. Rosicky, _A convenient category for directed homotopy_ (for Delta-generated spaces)

* E. Spanier, _Quasi-topologies_ (for quasi-topological spaces)

* O. Wyler, _Lecture notes on topoi and quasitopoi_ (for pseudotopological spaces)

* P. Johnstone, _On a topological topos_

#Discussion#


+-- {: .query}
[[Tim Porter|Tim]]: As I read the entry on nice topological spaces, it really refers to 'nice categories' rather than 'nice spaces'! I have always thought of spaces such as CW-complexes and polyhedra as being 'locally nice', but the corresponding categories are certainly not 'nice' in the sense of  [[nice topological space]]. Perhaps we need to adjust that other entry in some way.

_Toby_:  You\'re right, I think I\'ve been linking that page wrongly.  (I just now did it again on [[homotopy type]]!)  Perhaps we should write [[locally nice space]] or [[locally nice topological space]] (you pick), and I\'ll fix all of the links tomorrow.

[[Tim Porter|Tim]]:I suggest [[locally nice space]].  (For some time I worked in Shape Theory where local singularities were allowed so the spaces were not locally nice!) There would need to be an entry on locally nice. I suggets various meanings are discussed briefly, e.g. locally contractible, locally Euclidean,  ... and so on, but each with a minimum on it as the real stuff is in CW-complex etc and these are the 'ideas'.

[[Mike Shulman|Mike]]: Why not change the page [[nice topological space]] to be about CW-complexes and so on, and move the existing material there to something like [[convenient category of spaces]], which is also a historically valid term?  I am probably to blame for the current misleading content of [[nice topological space]] and I'd be happy to have this changed.

_Toby_:  I thought that [[nice topological space]] was supposed to be about special kinds of spaces, such as locally compact Hausdorff spaces, whose full subcategories of $\Sp$ are also nice.  (Sort of a counterpoint to the [[dichotomy between nice objects and nice categories]], whose theme is better fit by the example of locally Euclidean spaces).  CW-complexes also apply ---if you\'re interested in the homotopy categories.

[[Mike Shulman|Mike]]: Well, that's not what I thought.  (-:  I don't really know any type of space that is nice _and_ whose corresponding subcategory of [[Top]] is also nice.  The category of locally compact Hausdorff spaces, for instance, is not really all that nice.  In fact, I can't think of anything particularly good about it.  I don't even see any reason for it to be complete or cocomplete!

I think it would be better, and less confusing, to have separate pages for "nice spaces" and "nice categories of spaces," or whatever we call them.  And, as I said, I don't see any need to invent a new term like "locally nice."

When algebraic topologists (and, by extension, people talking about $\infty$-groupoids) say "nice space" they usually mean either (1) an object of some convenient category of spaces, or (2) a CW-complex-like space, between which weak homotopy equivalences are homotopy equivalences.  Actually, there is a precise term for the latter sort: an [[m-cofibrant space]], aka a space of the (non-weak) homotopy type of a CW complex.

_Toby_:  I thought the full subcategory of locally compact Hausdorff spaces was cartesian closed?  Maybe not, and it\'s not mentioned above.

But you can see that most of the examples above list nice properties of their full subcategories.  And the page begins by talking about what a lousy category $\Top$ is.  So it seems clearly wrong that you can\'t make $\Top$ a nicer category by taking a full subcategory of nice spaces.  (Not all of the examples are subcategories, of course.)
=--

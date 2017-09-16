# Idea

A **sequential convergence space** is a set equipped with a notion of _sequential convergence_, giving it a "topology" in an informal sense.

Any [[topological space]] (or more generally, any [[convergence space]]) becomes a sequential convergence space with its standard notion of convergence, but only for a [[sequential space]] can the topology be recovered from sequential convergence.  In the other direction, not every sequential convergence space is induced by a topological one.  Despite these apparent drawbacks, sequential convergence spaces have a number of advantages; see below.


# Definition

A **sequential convergence space** is a set $X$ equipped with a relation between sequences and points, called "converges to," with the following properties.

1. For every $x\in X$, the constant sequence $(x)$ converges to $x$.

1. If a sequence $(x_n)$ converges to $x$, then so does any subsequence of $x$.

1. If, for some sequence $(x_n)$ and some point $x$, every subsequence of $(x_n)$ contains a further subsequence converging to $x$, then $(x_n)$ itself converges to $x$.

The final property can be stated less [[constructive mathematics|constructively]] as "if $(x_n)$ does not converge to $x$, then there is a subsequence $(x_{n_k})$ of $(x_n)$ such that no subsequence of $(x_{n_k})$ converges to $x$."

A sequential convergence space is said to be **sequentially Hausdorff** if each sequence converges to at most one limit.


# Properties

The definition of a sequential convergence space is arguably easier and more intuitive than that of a [[topological space]] or [[convergence space]].  Continuity of functions between sequential convergence spaces is likewise easy to define by preservation of convergent sequences.

As mentioned above, the category $STop$ of [[sequential space|sequential (topological) spaces]] is a full reflective subcategory of the category $SConv$ of sequential convergence spaces. Thus, sequential convergence spaces include many spaces of interest to topologists, including all [[metric space|metrizable]] spaces and all [[CW complex|CW complexes]], and so they can be regarded as a sort of [[nice topological space]].

Not every sequential convergence space is a sequential (topological) space, but somewhat surprisingly, every sequentially Hausdorff sequential convergence space _is_ necessarily a sequential space. Note, though, that while any Hausdorff space is sequentially Hausdorff, the converse is not true even for sequential spaces (though it is true for first countable spaces).  Also of note is that $STop$ is coreflective in $Top$.

Furthermore, $SConv$ is _also_ a [[nice category of spaces]]: it is [[locally cartesian closed category|locally cartesian closed]] and in fact a [[quasitopos]].    Since it is a "Grothendieck quasitopos" (the category of presheaves on a category which are sheaves for one [[Grothendieck topology]] and separated for another one), it is also [[locally presentable category|locally presentable]].  In particular, it is [[complete category|complete]] and cocomplete, and has a small [[generator|generating set]].

Of course, the embedding of $STop$ in $SConv$ preserves all [[limit]]s, since it has a left adjoint, but somewhat surprisingly it also preserves many [[colimit]]s.  In particular, it preserves all the colimits used in the construction of a CW complex; thus it makes no difference whether you carry out the construction of a CW complex in $Top$ and then regard the result as a sequential convergence space, or carry out the construction in $SConv$ to begin with.

It follows that the [[geometric realization]] functor from [[simplicial set]]s can equally well be regarded as landing in $Top$, $STop$, or $SConv$.  Of course, it has a singular complex functor as a right adjoint in any of these three cases.  In the cases of $STop$ and $SConv$, geometric realization actually preserves all finite limits; in fact it and the singular complex functor form a [[geometric morphism]] between $sSet$ and a Grothendieck topos that contains $SConv$ as a reflective subcategory (the "topological topos" of Johnstone's paper).  Recall that geometric realization landing in $Top$ doesn't even preserve finite products, unless we replace $Top$ by (for instance) compactly generated spaces.

These properties of sequential convergence spaces should be compared with analogous ones for [[convergence space]]s and their relatives, such as [[pseudotopological space]]s.  The category $Conv$ of convergence spaces is also a complete and cocomplete quasitopos (hence, in particular, locally cartesian closed) and includes *all* of $Top$ as a reflective subcategory.  However, $Conv$ is not locally presentable and has no generator, and while the embedding of $Top$ into $Conv$ also preserves all limits (since it has a left adjoint), it actually preserves _fewer_ colimits than the embedding of $STop$ into $SConv$.  In particular, it does _not_ preserve the colimits used in the construction of CW complexes: if you carry out the construction of a CW complex in $Conv$, in general the result won't even be a topological space.


# Discussion

+--{: .query}
I\'m inclined to call such a thing a 'sequential [[filter|convergence space]]'.  The category of convergence spaces is also quite nice; it\'s cartesian closed, has all limits, and has *all* colimits (and possibly the other properties).  Furthermore, it includes *all* of $Top$ as a reflective subcategory.  (I think that these results are in Lowen-Colebunder\'s book cited at [[filter]].)  ---Toby

[[Mike Shulman|Mike]]: I accept your terminology.  The logic of "subsequential space" is that these are the subobjects of sequential spaces inside the Grothendieck topos of "consequential spaces," but that's not really very persuasive.  "Sequential convergence space" is unfortunately kind of long, but it is logical, and of course once one has established what sort of space one is working with in any particular context one is free to just call them "spaces."

I added some remarks addressing the relationship to convergence spaces.  I also like convergence spaces (and their friends, like pseudotopological spaces) very much, and I'm sure they are important in some contexts, such as analysis or more point-set-y topology.   However, I think that probably sequential convergence spaces are a better choice for homotopy theory, for the reasons I gave above.
=--


# References

* P. T. Johnstone, _On a topological topos_.  Proc. London Math. Soc. (3) 38 (1979) 237--271

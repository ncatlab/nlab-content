# Idea

A **subsequential space** is a set equipped with a notion of _sequential convergence_, giving it a "topology" in an informal sense.

Any [[topological space]] (or more generally, any [[pseudotopological space]]) becomes a subsequential space with its standard notion of convergence, but only for a [[sequential space]] can the topology be recovered from sequential convergence.  In the other direction, not every subsequential space is induced by a topological one.  Despite these apparent drawbacks, subsequential spaces have a number of advantages; see below.


# Definition

A **subsequential space** is a set $X$ equipped with a relation between sequences and points, called "converges to," with the following properties.

1. For every $x\in X$, the constant sequence $(x)$ converges to $x$.

1. If a sequence $(x_n)$ converges to $x$, then so does any subsequence of $x$.

1. If, for some sequence $(x_n)$ and some point $x$, every subsequence of $(x_n)$ contains a further subsequence converging to $x$, then $(x_n)$ itself converges to $x$.

The final property can be stated less [[constructive mathematics|constructively]] as "if $(x_n)$ does not converge to $x$, then there is a subsequence $(x_{n_k})$ of $(x_n)$ such that no subsequence of $(x_{n_k})$ converges to $x$."

Note that this definition matches the definition of [[pseudotopological space]] except for the restriction to sequences instead of general [[net]]s.  Accordingly, one may call a subsequential space a __sequential pseudotopological space__.

A subsequential space is said to be **sequentially [[Hausdorff space|Hausdorff]]** if each sequence converges to at most one limit.


# Properties

The definition of a subsequential space is arguably easier and more intuitive than that of a [[topological space]].  Continuity of functions between subsequential spaces is likewise easy to define by preservation of convergent sequences.

As mentioned above, the category $SeqTop$ of [[sequential space|sequential (topological) spaces]] is a full reflective subcategory of the category $SeqPsTop$ of subsequential spaces. Thus, subsequential spaces include many spaces of interest to topologists, including all [[metric space|metrizable]] spaces and all [[CW complex|CW complexes]], and so they can be regarded as a sort of [[nice topological space]].

Not every subsequential space is a sequential (topological) space, but somewhat surprisingly, every sequentially Hausdorff subsequential space _is_ necessarily a sequential space.  Note, though, that while any Hausdorff space is sequentially Hausdorff, the converse is not true even for sequential spaces (though it is true for first-countable spaces).  Also of note is that $SeqTop$ is coreflective in $Top$.

Furthermore, $SeqPsTop$ is _also_ a [[nice category of spaces]]: it is [[locally cartesian closed category|locally cartesian closed]] and in fact a [[quasitopos]].  Since it is a "Grothendieck quasitopos" (the category of presheaves on a category which are [[sheaf|sheaves]] for one [[Grothendieck topology]] and separated for another one), it is also [[locally presentable category|locally presentable]].  In particular, it is [[complete category|complete]] and cocomplete, and has a small [[generator|generating set]].

Of course, the embedding of $SeqTop$ in $SeqPsTop$ preserves all [[limit]]s, since it has a left adjoint, but somewhat surprisingly it also preserves many [[colimit]]s.  In particular, it preserves all the colimits used in the construction of a CW complex; thus it makes no difference whether you carry out the construction of a CW complex in $Top$ and then regard the result as a subsequential space, or carry out the construction in $SeqPsTop$ to begin with.

It follows that the [[geometric realization]] functor from [[simplicial set]]s can equally well be regarded as landing in $Top$, $SeqTop$, or $SeqPsTop$.  Of course, it has a singular complex functor as a right adjoint in any of these three cases.  In the cases of $SeqTop$ and $SeqPsTop$, geometric realization actually preserves all finite limits; in fact it and the singular complex functor form a [[geometric morphism]] between $SimpSet$ and a Grothendieck topos that contains $SeqPsTop$ as a reflective subcategory (the "topological topos" of Johnstone's paper).  Recall that geometric realization landing in $Top$ doesn't even preserve finite products, unless we replace $Top$ by (for instance) compactly generated spaces.

These properties of subsequential spaces should be compared with analogous ones for [[convergence space]]s and their relatives, such as [[pseudotopological space]]s.  The category $Conv$ of convergence spaces is also a complete and cocomplete quasitopos (hence, in particular, locally cartesian closed) and includes *all* of $Top$ as a reflective subcategory.  However, $Conv$ is not locally presentable and has no generator, and while the embedding of $Top$ into $Conv$ also preserves all limits (since it has a left adjoint), it actually preserves _fewer_ colimits than the embedding of $SeqTop$ into $SeqPsTop$.  In particular, it does _not_ preserve the colimits used in the construction of CW complexes: if you carry out the construction of a CW complex in $Conv$, in general the result won't even be a topological space.


# Discussion

+--{: .query}
I\'m inclined to call such a thing a 'sequential [[convergence space]]'.  The category of convergence spaces is also quite nice; it\'s cartesian closed, has all limits, and has *all* colimits (and possibly the other properties).  Furthermore, it includes *all* of $Top$ as a reflective subcategory.  (I think that these results are in Lowen-Colebunder\'s book cited at [[filter]].)  ---Toby

[[Mike Shulman|Mike]]: I accept your terminology.  The logic of "subsequential space" is that these are the subobjects of sequential spaces inside the Grothendieck topos of "consequential spaces," but that's not really very persuasive.  "Sequential convergence space" is unfortunately kind of long, but it is logical, and of course once one has established what sort of space one is working with in any particular context one is free to just call them "spaces."

I added some remarks addressing the relationship to convergence spaces.  I also like convergence spaces (and their friends, like pseudotopological spaces) very much, and I'm sure they are important in some contexts, such as analysis or more point-set-y topology.   However, I think that probably sequential convergence spaces are a better choice for homotopy theory, for the reasons I gave above.

_Toby_:  Ha, now I\'ve realised that 'sequential convergence space' is really not correct, since the last clause of the definition makes it a pseudotopological space!  So it should be 'sequential pseudotopological space', and now 'subsequential space' is looking nicer than ever.

[[Mike Shulman|Mike]]: Okay.  I didn't realize at first that a "convergence space" is not the same as a pseudotopological space, since pseudotopological spaces seem to me the most natural notion of convergence for filters.  (Are there natural convergence spaces that are not pseudotopological?)  Move it back to [[subsequential space]] if you want.

_Toby_:  First, I really ought to check that I\'ve got the definitions of 'convergence space' and 'Cauchy space' exactly correct.  (In particular, the former varies somewhat in early literature, much as 'topological space' did when it first came out.)  I don\'t *think* that the pseudotopological clause is in there, but ... I need to double-check.  (And if it\'s not, then I\'ll find you your counterexample too.)

_Toby_:  Here\'s your counterexample: convergence almost everywhere.  With this convergence, the space of almost-everywhere defined real-valued Lebesgue-measureable functions on the real line is a sequential convergence space that is not pseudotopological.

[[Mike Shulman|Mike]]: Huh, very interesting!
=--


# References

* P. T. Johnstone, _On a topological topos_.  Proc. London Math. Soc. (3) 38 (1979) 237--271
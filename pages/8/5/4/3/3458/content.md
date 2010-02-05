This entry is on the book __Galois Theories__ by [[Francis Borceux]] and [[George Janelidze]]. 

+-- {: .query}
(Initially it will be in the form of a book review. The initial version is an edited and adapted version of a review of the book by [[Tim Porter]] that appeared in Proceedings of the Edinburgh Mathematical Society (Series 2)  (2002), 45 : 761-762. When the entry has been influenced by other sources, please remove this box) 
=--

The developments  that lead to this book are due to some deeply based analogies
between some initially very different looking mathematical theories, one in algebra, 
another in topology.

Galois originally developed the some of elements of what was to become Galois theory in 
an attempt to understand polynomial equations, continuing work of Abel and others.  In modern language, working
over a base field,  $K$, a field extension $K\subset L$ is a Galois extension
when every element of $L$ is the root of a polynomial in $K[X]$, which factors 
in $L[X]$ into linear factors and all of whose roots are simple.  The group
$Gal[L:K]$ of this extension is the group of field automorphisms of
$L$ which fix all elements of $K$ and the classical Galois theorem asserts
that when $L$, considered as a $K$-vector space, is finite dimensional, the
subgroups $G\subseteq Gal[L:K]$ of the Galois group classify the
intermediate field extensions $K\subseteq M\subseteq L$.  The themes to note
in this classical theory are (i) splitting into simpler structures, (ii)
groups of automorphisms and (iii) intermediate structures classified by
subgroups.


The second theory is that of [[covering space|covering spaces]] in topology.  A covering map
$\alpha : X\to B$ is one that has the property that every point of $B$ has an
open neighbourhood whose inverse image by $\alpha$ is a disjoint union of open 
subsets each of which is mapped homeomorphically onto it by $\alpha$.  Given
any reasonably 'locally nice' space, there is a universal connected covering
space, $p : \widetilde{B}\to B$, such that all connected covering spaces of
$B$ are quotients of $\widetilde{B}$.  Classification of the connected
coverings is by subgroups of the automorphism group of $p$.  Of course, this
automorphism group is isomorphic to the (Poincar&#233;) fundamental group of $B$
(under suitable local conditions).

This topological theory of covering spaces has some similarities to Galois
theory. Again one has automorphism groups and a correspondence between
intermediate structures (this time quotients not subobjects) and perhaps some
notion of splitting - there is an open cover of $B$ over each part of which
the covering splits up as a family of isomorphic pieces.

These two theories, thus, do look vaguely similar, but automorphism groups are 
very common in mathematics and even that sort of 'Galois' correspondence is
not that uncommon, so surely any similarities must not be due to anything
really deep! The story of how the deep connections between them became apparent is
quite long and here is not the place to explore it in any detail.  It involves 
function spaces and Riemann surfaces as well as a lot else that is central to
modern pure maths (if you want a good source for the
theory see the beautiful book \cite{douady^2} by Douady and Douady. The
present book traces a greatly extended mathematical path beyond that
semi-classical link between Galois theory and coverings, but starts at an
elementary beginning. It describes classical Galois theory, then turns to its
extension to infinitary field extensions, to \'etale algebras that became the
foundation for the work of
Grothendieck on the fundamental group of schemes ([[SGA1]]). This was 
at the same time Galois theory and covering space theory although for spaces
for which there was no question of being able to define a fundamental group
using paths.


category: reference
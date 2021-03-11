This entry is about the monograph

\bibitem{BorceuxJanelidze2001} 

+-- {: .query}
(Initially it will be in the form of a book review. The initial version is an edited and adapted version of a review of the book by [[Tim Porter]] that appeared in Proceedings of the Edinburgh Mathematical Society (Series 2)  (2002), 45 : 761-762. When the entry has been influenced by other sources, please remove this box) 
=--

The developments  that lead to this book are due to some deeply based analogies between some initially very different looking mathematical theories, one in algebra, another in topology.

Galois originally developed some of elements of what was to become Galois theory in an attempt to understand polynomial equations, continuing work of Abel and others.  In modern language, working over a base field,  $K$, a field extension $K\subset L$ is a Galois extension when every element of $L$ is the root of a polynomial in $K[X]$, which factors  in $L[X]$ into linear factors and all of whose roots are simple.  The group $Gal[L:K]$ of this extension is the group of field automorphisms of $L$ which fix all elements of $K$ and the classical Galois theorem asserts that when $L$, considered as a $K$-vector space, is finite dimensional, the subgroups $G\subseteq Gal[L:K]$ of the Galois group classify the intermediate field extensions $K\subseteq M\subseteq L$.  The themes to note in this classical theory are (i) splitting into simpler structures, (ii) groups of automorphisms and (iii) intermediate structures classified by subgroups.


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
theory see the beautiful book (see below) by Douady and Douady). 

Borceux and Janelidze's book, _Galois theories_, traces a greatly extended mathematical path beyond that
semi-classical link between Galois theory and coverings, but starts at a fairly
elementary beginning. It describes classical Galois theory, then turns to its
extension to infinitary field extensions, to &#233;tale algebras that became the
foundation for the work of
Grothendieck on the fundamental group of schemes ([[SGA1]]). This was 
at the same time Galois theory and covering space theory, although for spaces
for which there was no question of being able to define a fundamental group
using paths. (This idea was fundamental in Grothendieck's later attempts to develop a higher dimensional version of this Poincar&#233;-Galois theory in his manuscript, [[Pursuing Stacks]].)

This  book explores the connections between these theories, 
searching for further cases of the general 'scenario' and tries to strip back the
superficial structure to reveal aspects of what are the essential features of
all these theories.

The book assumes a certain
knowledge of algebra and general topology, together with some familiarity with 
the __elementary__ language of category theory (categories, functors, natural
transformations, limits and adjoint functors).  Its starts
with a short trip through the theory of field extensions, then goes on to look 
at Grothendieck's extension of this to algebras.  

Chapter 3 handles infinitary Galois theory.  Here [[profinite space|profinite spaces]] and
[[profinite group|profinite groups]] are introduced.  They are also useful in the following chapter
where the extension of Galois theory to commutative rings (due to Magid,
see reference below) is treated.    The [[Pierce
spectrum]] and [[Stone duality]] are handled clearly and simply laying the base for
Magid's profinite Galois groupoid. 


With that first layer of categorical abstraction (Janelidze's abstract
categorical Galois theory) in place, other applications can be explored.
Given the introduction to the area in this review, it may seem strange that
covering maps are only introduced in Chapter 6, but here they can be very neatly
described and handled, beautifully illustrating and enriching the earlier
abstraction.

The final chapter describes one of the most important recent advances in topos 
theory, giving an introduction to the Joyal--Tierney classification of
Grothendieck toposes as sheaves on localic groupoids.  The book ends with a
look at other directions the theory has taken beyond those handled in detail.
This section is particularly valuable as it should set the scene for future
research.

It introduces many deep important 
concepts of algebra and category theory, introduces, motivates and uses in an
interesting way.  As one would expect, this means that the later chapters are sometimes much 
harder going than the earlier ones, but the writing and structure of the book is such that the transition is fairly gradual.  

Some researchers will probably feel that some of the exercises should have been worked out in detail, but given the starting assumptions of the authors, and the reasonably good set of references, there were bound to be such omissions.

##Table of chapter titles.

Introduction; 

1. Classical Galois theory; 

2. Galois theory of Grothendieck; 

3. Infinitary Galois theory; 

4. Categorical Galois theory of commutative rings; 

5. Categorical Galois theorem and factorization systems; 

6. Covering maps; 

7. Non-Galoisian Galois theory; 

Appendix; 

Bibliography; 

Index.

## References ##

* $n$lab entries [[categorical Galois theory]], [[Grothendieck's Galois theory]]

* Grothendieck et al., [[SGA1]]

* R. and A. Douady, _Alg&#232;bre et th&#233;ories galoisiennes_,
  Fernand Nathan, 1977.

* A. R. Magid,  _The separable Galois theory of commutative rings_,
  Marcel Dekker, 1974.


[[!redirects Galois theories]]

category: reference
category: Galois theory
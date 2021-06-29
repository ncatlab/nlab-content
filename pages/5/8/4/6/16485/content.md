# Linearly compact vector spaces, modules, rings, objects#
* table of contents
{:toc}

## Motivation

Linearly compact vector spaces were introduced in the development of the idea of duality. The (algebraic) linear dual of the discrete infinite-dimensional vector space is of larger cardinality so the original space is not isomorphic to the dual of its dual. But if a natural formal topology (which comes say from the filtration of the original space by its finite-dimensional subspaces; the formal topology on the dual is equivalent to consider the dual cofiltration) is given to the algebraic dual, then it makes sense to take the space of _continuous_ linear functional and we recover the original vector space. More precisely this amounts to an embedding of the category of (discrete) vector spaces into the category of linearly compact vector spaces, the latter category has a duality which extends the duality for finite-dimensional vector spaces. 

A standard reference for the basics is the Dieudonn&#233;'s book on formal groups. 

The next definition is copied from Tom Leinster's note that's listed below. 

## Definition

A **linearly compact vector space** over a field $k$ is a topological vector space $V$ over $k$ such that:

* The topology is linear: the open affine subspaces form a basis for the topology.
* Any family of closed affine subspaces with the finite intersection property has nonempty intersection.
* The topology is Hausdorff. 

More generally, a __linearly compact module__ $M$
over a [[topological ring]] $R$
is a Hausdorff linearly topologized
(meaning there is a basis of neighborhoods
of 0 consisting of open submodules)
such that every family of closed cosets
with the finite intersection property
(meaning finite subfamilies have nonempty intersections)
has nonempty intersection.

## Examples

Every [[pseudocompact module]] is linearly compact.

## Related concepts

* [[pseudocompact module]]

## Literature

* [[L. S. Pontrjagin]], _&#220;ber stetige algebraische K&#246;rper_, Ann. of Math. 33 (1932) 163-174
* [[N. Jacobson]], _Totally disconnected locally compact rings_,  Amer. J. Math. 58 (1936) 433-449; _A note on topological fields_, Amer. J. Math. 59 (1937) 889-894
* N. Jacobson , O. Taussky , Locally compact rings, Proc. Nat. Acad. Sci. U.S.A. 21 (1935) 106-108
* Solomon Lefschetz, _Algebraic topology_, Amer. Math. Soc. Colloq. Pub. 27, 1942, reprinted 1963
* I. Kaplansky, _Topological rings_, Amer. J. Math. 69 (1947) 153-183; _Topological methods in valuation theory_, Duke Math. J. 14 (1947) 527-541; _Locally compact rings I_, Amer. J. Math. 10 (1948) 447-459; _II_, Amer. J. Math. 13 (1951) 20-24; _III_, Amer. J. Math. 14 (1952) 929-935; _Topological representations of algebras II_, Trans. Amer. Math. Soc. 68
(1950) 62-75
* Daniel Zelinsky, _Linearly compact modules and rings_, American Journal of Mathematics __75__, No. 1 (Jan., 1953), pp. 79-90 [jstor](http://www.jstor.org/stable/2372616)
* O. Goldman, C. H. Sah, _On a special class of locally compact rings_, J. Algebra 4 (1966) 71-95; _Locally compact rings of special type, J. Algebra 11 (1969) 363-454
* [[Tom Leinster]], [Where Do Linearly Compact Vector Spaces Come From?](https://golem.ph.utexas.edu/category/2012/09/where_do_linearly_compact_vect.html), $n$-Cat Caf&#233; 2012
* Tom Leinster, _Codensity and the ultrafilter monad_, [arxiv/1209.3606](http://arxiv.org/abs/1209.3606)
* [[Jean Dieudonné]], _Introduction to the theory of formal groups_, Dekker, New York 1973. 
* J. Dieudonn&#233;, _Linearly compact spaces and double vector spaces over sfields_, Amer. J. Math. 73, No. 1 (Jan., 1951), pp. 13-19 [jstor](http://www.jstor.org/stable/2372154)

Linearly compact rings and modules are treated in chapter VII, linear compactness and semisimplicity, in

* S. Warner, _Topological rings_, North-Holland Math. Studies 178, 1993

A similar concept: *profinite $k$-modules* - is treated in 

* A. Yekutieli, _On the Structure of Behaviors_, Linear Algebra and its Applications  392 (2004), 159-181.

The definitions of linearly compact subcategories and linearly compact objects in (co)Grothendieck categories can be found in the chapter on duality in 

* N. Popescu, [[Abelian categories with applications to rings and modules]], London Mathematical Society Monographs 3, Academic Press 1973, xii + 470 pp
*  U. Oberst, _Duality theory for Grothendieck categories and linearly compact rings_, J. Algebra __15__ (1970), p. 473 --542, [pdf](http://www.sciencedirect.com/science/article
* Mihail Ursul, _Topological rings satisfying compactness conditions_, Math. and its applications 549, Kluwer 2002, [gBooks](https://books.google.hr/books?id=OGDzOJjcjOQC)

[[!redirects linearly compact ring]]
[[!redirects linearly compact object]]
[[!redirects linearly compact modules]]
[[!redirects linearly compact vector spaces]]
[[!redirects linearly compact vector space]]


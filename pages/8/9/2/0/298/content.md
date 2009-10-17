[[!redirects vertex operator algebras]]

#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The usual definition of _vertex operator algebra_ is long and unenlightning. But due to work by Huang and Kong it is known now that vertex operator algebras are nothing but certain [[FQFT]]s:

There is a [[monoidal category]] or [[operad]] whose [[morphism|morphisms]] are conformal spheres with $n$-punctures marked as incoming and one puncture marked as outgoing (each puncture equipped with a conformally parametrized annular neighborhood). Composition of such spheres is by gluing along puctures. This can be regarded as a category $2Cob_{conf}^0$ of 2-dimensional genus-0 conformal [[cobordism|cobordisms]].

As shown by theorems by Huang and Kong, a vertex operator algebra is precisely a _[[holomorphic representation]]_ of this category, or [[algebra over an operad]] for this [[operad]] i.e. an genus-0 [[conformal field theory|conformal]] [[FQFT]], hence a [[monoidal functor]]

$$
  V : 2Cob_{conf}^0 \to Vect
$$

such that its component $V_1$ is a holomorphic function on the moduli space of conformal punctured spheres.

#References#

The original article with the interpretation of vertex operator algebras as holomorphic algebras over the holomorphic punctured sphere operad is

* Yi-Zhi Huan, _Geometric interpretation of vertex operator algebras_, Proc. Natl. Acad. Sci. USA, Vol 88. (1991) pp. 9964-9968

A standard textbook summarizing these results is

* Huang, _Two-dimensional conformal field theory and vertex operator algebras_

As mentioned in the [acknowledgements](http://books.google.com/books?id=SUUdknTpYjEC&pg=PR11&lpg=PR11&dq=%22vertex+operator+algebras%22+%22trimble%22&source=bl&ots=v3GHx_ra2M&sig=TW5MzAtDi4n_gJjvUHb6eELoAXQ&hl=en&ei=9jdnSoXqKJiCtge6xqDuDw&sa=X&oi=book_result&ct=result&resnum=4) there, [[Todd Trimble]] and [[Jim Stasheff]] had a hand in making the operadic picture manifest itself here.

More recently Huang's student Liang Kong has been developing these results further, generalizing them to open-closed CFTs and to non-chiral, i.e. completely general CFTs. See 

* Liang Kong, _Open-closed field algebras_ Commun. Math. Physics. 280, 207-261 (2008) ([arXiv](http://arxiv.org/abs/math/0610293)).
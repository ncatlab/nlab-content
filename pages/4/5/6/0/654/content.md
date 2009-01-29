#Idea#

The concept of a _2-vector space_ is supposed to be a [[vertical categorification|categorification]] of the concept of a vector space. As usual in the game of `categorification', this requires us to think deeply about what an ordinary vector space really is, and then attempt to categorify that idea. 

## What is a vector space?

There are at least two distinct conceptual roles which vectors and vector spaces play in mathematics:

* A vector is a _column of numbers_. This is the way vector spaces appear in quantum mechanics, elementary linear algebra, etc. 

* A vector is a _direction in space_. Vector spaces of this kind are often the infinitesimal data of some global structure, such as tangent spaces to manifolds, Lie algebras of Lie groups, and so on.

These two different ideas of a `vector space' lead to two diferent ideas of a `2-vector space', broadly speaking those of _Kapranov and Voevodsky_ and those of _Baez and Crans_. 

As usual, there are various different concepts of 2-vector spaces, all of them useful and relevant in different contexts.

Most definitions of 2-vector spaces used in the literature are special cases of the idea that in analogy to how a vector space can be regarded as a [[module]] over the ground field $k$, a 2-vector space $W$ should be a [[category]] which is a [[monoidal category module]] with some nice properties (such as being an abelian category) over a suitable [[monoidal category]] $V$ which plays the role of the categorified ground field. There is then an obvious [[bicategory]] of such module categories.


#Examples



## $C = Disc(k)$

The ground field itself may be regarded as a [[discrete category]] which is then clearly a [[monoidal category]]. A $Disc(k)$-module category is a category whose space of objects and space of morphisms are both $k$-modules -- ordinary vector spaces! -- such that all structure morphisms (source, target, identity, composition) respect the $k$-action -- hence are linear maps. This are categories [[internal category|internal to]] [[Vect]]_k which are equivalent to chain complexes of vector spaces concentrated in degree 0 and 1.

Categories internal to [[Vect]] were explicitly described from the perspective of 2-vector spaces in 

* John C. Baez and Alissa S. Crans, _Higher-Dimensional Algebra VI: Lie 2-Algebras_ ([tac](http://www.tac.mta.ca/tac/volumes/12/15/12-15abs.html)).

in the context of higher [[Lie theory]]. In fact, (following for instance from an extension of the [[Dold-Kan-theorem]] by Brown and Higgins), [[strict omega-category|strict omega-categories]] internal to [[Vect]] are equivalent to chain complexes in non-negative degree and can be regarded as strict $Disc(k)$-$\infty$-modules. This allows to conceive much of [[homological algebra]] and many of the structures appearing in higher [[Lie theory]] -- for instance the definition of [[L-infinity algebra]]s, as being about $\infty$-vector spaces. Regarding a chain complex as an $\infty$-vector space is useful conceptually for understanding the meaning of some constructions on chain complexes, while of course chain complexes themselves are well suited for direct computation with the $\infty$-vector spaces which they are equivalent to. (See also the remark about different notions of 2-vector spaces further below.)

## Module categories of modules

For $V$ a general symmetric [[closed monoidal category]] the full bicatgeory of all [[monoidal category module]]s over $V$ is in general hard to get under control, but what is more tractable is the sub-bicategory which may be addressed as the bicategory of $V$-modules _with basis_ namely the category $V-Mod$ in the sense of [[enriched category theory]] with

* objects are categories $C$ [[enriched category|enriched over]] $V$, to be thought of as placeholders for their categories of [[module]]s, $Mod_C := [C,V]$

* morphisms $C \to D$ are [[bimodule]]s $C^{op}\otimes D \to V$;

* 2-morphisms are natural transformations.

Notice that all $V$-categories $Mod_C$ of modules over a $V$-category $C$ are naturally [[copower|tensored]] over $V$ and hence are [[monoidal category module]]s over $V$. In analogy to how a vector space $W$ (a $k$-module) is equipped with a basis by finding a set $S$ such that $W \simeq [S,k]$, we can think of a general [[monoidal category module]] $W$ over $V$ to be equipped with a basis by providing an [[equivalence]] $W \simeq [C,V]$, for some $V$-category $V$. In this sense $V-Mod$ is the category of $V$ 2-vector spaces with basis.

All of the examples below are special cases of this one.


## $C = Vect_k$

### $Vect$-enriched categories

According to the above a $Vect$-enriched category $C$ can be regarded as a basis for the $Vect$-module $Mod_C = [C,Vect]$. A $Vect$-enriched category is just an  [[algebroid]]. If it has a single object it is an [[algebra]] and $Mod_C$ is the familiar category of modules over an algebra.

Notice that, by the very definition of Morita equivalence, two algebras (algebroids) have equivalent module categories, and hence can be regarded as different bases for the same $Vect$ 2-vector space, iff they are Morita equivalent.

Some blog discussion of this point is at [2-Vectors in Trodheim](http://golem.ph.utexas.edu/category/2007/11/2vectors_in_trondheim.html). $Vect$-enriched categories as models for 2-vector spaces appear in 

* Jacob Lurie, _On the classification of topological field theories_ ([pdf](http://www-math.mit.edu/~lurie/papers/cobordism.pdf)) (see example 1.2.4)

2-vector spaces in the sub-bicategory of algebras ($Vect$-enriched categories with a single object), bimodules and intertwiners are discussed in

* U. Schreiber, _AQFT from $n$-functorial QFT_ ([arXiv](http://arxiv.org/abs/0806.1079)) (appendix A)

and 

* U. Schreiber and K. Waldorf, _Connections on non-abelian gerbes and their holonomy_ ([arXiv](http://arxiv.org/abs/0808.1923))

### Kapranov-Voevodsky 2-vector spaces

Upon further restriction of $Vect-Mod$ to 2-vector spaces whose basis is a _discrete category_, namely a set $S$ (or the $Vect$-enriched category over $S$ which has just the ground field object sitting over each element of $S$) one arrives at $Vect$-modules of the form

$$
  [S, Vect] = Mod_{k^n} \simeq (Vect)^n
$$

(where $k^n$ denotes the algebra of diagonal $n\times n$-matrices). 

The categories $Vect^n$ have been introduced by Kapranov and Voevodsky as 2-vector spaces in

* M. Kapranov and V. Voevodsky, _2-categories and Zamolodchikov tetrahedra equations_ in _Algebraic groups and their generalization: quantum and infinite-dimensional methods, University Park, PA (1991) (eds: W. J. Haboush and B. J. Parshall), Proc. Sympos. Pure Math. 56 (Amer. Math. Soc., Providencem RIm 1994), pp. 177-259

and are one of the oldest and most familiar examples of 2-vector spaces.

### Elgueta 2-vector spaces

A notion of 2-vector spaces in between general module categoies $Mod_C = [C,Vect]$ and Kaparanov-Voevodsky 2-vector spaces is given in

* Josep Elgueta, _Generalized 2-vector spaces and general linear 2-groups_ ([arXiv](http://arxiv.org/abs/math/0606472))


### Infinite-dimensional KV 2-vector spaces

We can regard the objects of the $n$-dimensional  Kapranov-Voevodsky 2-vector space $Vect^n$ -- which are $n$-tuples of vector spaces -- as vector bundles over the finite set of $n$ elements. This has an obvious generalization to vector bundles over any topological space  --in terms of modules these are the finitely generated projective modules of the algebra of continuous functions on this space. So categories of vector bundles can be regarded as infinite-dimensional 2-vector spaces. For the case that the underlying topological space is a _measure space_ such infinite dimensional KV 2-vector spaces have been studied in

* John C. Baez, Aristide Baratin, Laurent Freidel, Derek K. Wise, _Infinite-Dimensional Representations of 2-Groups_ ([arXiv](http://arxiv.org/abs/0812.4969)) 

## $C = $ modular tensor category

The relevance of module categories as models for 2-vector spaces was apparently first realized in the context of [[conformal field theory]], where the monoidal category $V$ in question is a [[modular tensor category]]. A result by Victor Ostrik showed that _all_ $V$-module categories are equivalent to $Mod_A$ for $A$ some one-object $V$-enriched category (i.e. an algebra internal to $V$) in

* V. Ostrik, _Module Categories, weak Hopf Algebras and Modular Invariants_ ([arXiv](http://arxiv.org/abs/math.QA/0111139), [blog](http://golem.ph.utexas.edu/string/archives/000717.html))



#Remark on the different notions of 2-vector spaces#

As the above list shows, there are 2-vector spaces of very different kind. There is not <em>the</em> notion of 2-vector space which is the universal right answer. Different notions of vector spaces are applicable and useful in different situations. 
This can be regarded as nothing but a more pronounced incarnation of the fact that already ordinary vector space appear in different flavors which are useful in different situations (real vector spaces, complex vector spaces, etc.)

For instance $Disc(k)$-module categories are crucial for higher [[Lie theory]] but 2-bundles with fibers $Disc(k)$-module categories are comparatively boring as far as general 2-bundles go, as they are essentially complexes of ordinary vector bundles. See 

* Nils. A. Baas, Marcel B&ouml;kstedt, Tore August Kro, _Two-Categorical Bundles and Their Classifying Spaces_ ([arXiv](http://arxiv.org/abs/math/0612549))

#2-Hilbert spaces#

2-vector spaces have to a large extent been motivated by and applied in (2-dimensional) [[quantum field theory]]. In that context it is usually not the concept of a plain vector space which needs to be categorified, but that of a Hilbert space. 

2-Hilbert spaces as a $V = Hilb$-enriched categories with some extra properties were discribed in

* John Baez, _Higher-Dimensional Algebra II: 2-Hilbert Spaces_ ([arXiv](http://arxiv.org/abs/q-alg/9609018)) .

In applications one often assumes these 2-Hilbert spaces to be [[semisimple]] in which case such a 2-Hilbert space is essentially a Kapranov-Voevodsky-type 2-vector space.

A review of these ideas of 2-Hilbert spaces as well as applications of 2-Hilbert spaces to finite group representation theory are in

* Bruce Bartlett, _On unitary 2-representations of finite groups and topological quantum field theory_ ([arXiv](http://arxiv.org/abs/0901.3975))
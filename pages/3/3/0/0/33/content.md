<div class="rightHandSide toc">
[[!include categorification - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

Roughly speaking, _vertical categorification_ is a procedure in which structures are generalized from the context of [[set theory]] to [[category theory]] or from category theory to [[higher category theory]].

What precisely that means may depend on circumstances and authors, to some extent. What has a more specific definition is the process of [[decategorification]]: this concretely quotients out [[k-morphism]]s in a [[n-category]] to produce a $k$-category for some $k \lt n$, in particular a (possibly large) [[set]] (the set of isomorphism classes or equivalence classes of objects) when $k = 0$.

One may understand _vertical categorification_ as any operation that is a [[section]] of this [[decategorification]] operation, and many examples in the literature are of this kind.

Vertical categorification is closely related to the process of relaxing properties of structures to hold only _up to [[homotopy theory|homotopy]]_.


## Remarks ##

This is in contrast to [[horizontal categorification]].
If you call that 'oidification', then you can call this simply 'categorification'.


## Examples ##

* The maybe archetypical example is the categorification of the [[set]] $\mathbb{N}$ of [[natural numbers]] to the [[category]] [[FinSet]] of [[finite sets]]:

  The set $\mathbb{N}$ is a [[0-category]], while $FinSet$ is a [[1-category]]. The [[decategorification|isomorphism classes]] of $FinSet$ however are in canonical bijection with the elements of $\mathbb{N}$:

  $$ \mathbb{N} \simeq FinSet_\sim .$$

  So $\mathbb{N}$ is the [[decategorification]] of $FinSet$ and accordingly $FinSet$ is a (vertical) categorification of $\mathbb{N}$. 

  From the point of view of [[category theory]], there is some justification to the converse of this statement: the study of the natural numbers is nothing but the study of the isomorphism classes in $FinSet$. In a way, the very notion of **counting** is about this. This point is made nicely in [BaDo98](http://arxiv.org/abs/math.QA/9802029).

  But there are other categorifications of the natural numbers, for instance the category $FinVect$ of finite dimensional [[vector spaces]] (over any given field). This is not equivalent to $FinSet$, but still, its set of isomorphism classes is also canonically in bijection with the natural numbers:

  $$ \mathbb{N} \simeq FinVect_\sim .$$


* One notion of vertical categorification of **[[abelian groups]]** gives _[[chain complexes]] of abelian groups_ which, if in non-negative degree, are equivalent to [[strict ∞-categories]] internal to [[Ab]]. (See the [[Dold-Kan correspondence|Dold?Kan theorem]].)

* Familiar vertical categorifications/homotopifications of algebraic structures include

  * vector spaces &#8594; [[2-vector spaces]]
  * algebras &#8594; $A_\infy$-[[A-∞-algebra|algebras]]
  * Lie algebras &#8594; $L_\infty$-[[L-∞ algebra|algebras]]


## References##

* [[John Baez]] and [[James Dolan|James Dolan]], [Categorification](http://arxiv.org/abs/math.QA/9802029), in _Higher Category
Theory_, eds. Ezra Getzler and Mikhail Kapranov,
Contemp. Math. 230, American Mathematical Society, Providence, Rhode Island, 1998, pp. 1-36.

An early article where the concept of categorification is described is

* Crane and Yetter, 
[Examples of categorification](http://arxiv.org/abs/q-alg/9607028)

A bit of $n$-Caf&eacute; discussion on this subject can be found here: 

* [[John Baez]], [_What is categorification?_](http://golem.ph.utexas.edu/category/2008/10/what_is_categorification.html)


[[!redirects categorification]]
[[!redirects ∞-categorification]]
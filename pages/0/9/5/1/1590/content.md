
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **2-monad** is a [[monad]] on a [[2-category]], or more generally a monad _in_ a [[3-category]].  This concept manifests at varying levels of strictness:

* For a _strict 2-monad_ (which classically is called a simply a "2-monad"), the 2-category $K$ is a [[strict 2-category]], the functor $T:K\to K$ is a [[strict 2-functor]], and the transformations $\mu$ and $\eta$ are [[strict 2-natural transformation]]s and satisfy their laws strictly.  This is the same as a $Cat$-[[enriched category theory|enriched]] monad.  Strict 2-monads live naturally in [[strict 3-category|strict 3-categories]].

* For a fully _weak 2-monad_, $K$ is a weak 2-category (such as a [[bicategory]]), $T$ is a weak (aka pseudo) 2-functor, and $\mu$ and $\eta$ are pseudo natural transformations that satisfy their laws up to specified isomorphisms satisfying coherence conditions.  Weak 2-monads live naturally in fully weak 3-categories (or [[tricategory|tricategories]])

* In between we have various notions that are sometimes called _pseudomonads_.  For instance, we could require $K$ to be a strict 2-category and $T$ a strict 2-functor, but $\mu$ and $\eta$ only pseudo natural.  This sort of pseudomonad lives naturally in a [[Gray-category]].

## Algebras and pseudoalgebras

One can consider various 2-categories of algebras/modules for a 2-monad, depending on whether the algebras satisfy their laws strictly or weakly, and whether the morphisms commute with the algebra structure strictly or weakly.

At the strictest level, for a strict 2-monad $T$ we can consider the $Cat$-enriched [[Eilenberg-Moore category]], which consists of strict algebras (see [[algebra over a monad]]), strict morphisms, and strict transformations between these.  In 2-categorical literature, it is usually denoted $T Alg_s$.  Many common types of structure on categories are specified by strict algebras for a strict 2-monad, but usually the strict morphisms are too strict.

There are three types of weak morphism: _pseudo_ (which preserve the structure up to a specified coherent isomorphism), _lax_ (which preserve it up to a noninvertible transformation) and _colax_ or _oplax_ (for which the transformation goes the other direction).  With strict algebras and these various types of morphism, we obtain 2-categorie $T Alg$ (the pseudo case), $T Alg_l$, and $T Alg_c$ for lax and colax respectively.  One can also define an [[F-category]] of strict and lax morphisms together (or strict and pseudo, or pseudo and lax), and a [[double category]] which includes both lax and colax morphisms.

For example, ordinary (non-strict) [[monoidal category|monoidal categories]] are the _strict_ algebras for a strict 2-monad $T_{MC}$ on $Cat$, but usually we care about pseudo, lax, and oplax [[monoidal functor]]s rather than strict ones.  _Strict_ monoidal categories are the strict algebras for a _different_ strict 2-monad $T_{StrMC}$ on $Cat$.

We can, however, also consider *pseudo* algebras for a 2-monad; see [[pseudoalgebra for a 2-monad]].  If the 2-monad is not strict, then this is usually the only sensible course.  Pseudoalgebras for a strict 2-monad $T$ usually give an "unbiased" weaker notion of the structure specified by $T$.  For example, the pseudoalgebras for $T_{StrMC}$ are, not ordinary monoidal categories, but [[bias|unbiased]] monoidal categories.  (It is true, however, that the 2-category $Ps T_{StrMC} Alg$ of unbiased monoidal categories and strong monoidal functors is strictly 2-equivalent, i.e. Cat-enriched equivalent, to the 2-category of ordinary biased monoidal categories and strong monoidal functors.)

There are also 2-monads that specify [[property-like structure]].  For instance, there is a 2-monad whose algebras are categories with finite products.  Actually, its algebras are categories equipped with _specified_ finite products, the strict morphisms of these algebras preserve these specified finite products on the nose, and the pseudo morphisms preserve them in the usual sense of "preserving finite products."  In this case, _every_ functor between algebras is an oplax morphism, since there is always a canonical comparison map $F(A\times B) \to F(A)\times F(B)$.

## Doctrines

2-monads (particularly on [[Cat]]) are also sometimes called [[doctrine]]s, with the intuition in mind that they are an "algebraic theory" of structure on a category just as a monad (on $Set$) is an [[algebraic theory]] of structure on a set.  However, this use of terminology is arguably at variance with the original intuitive meaning of "doctrine."

## Related concepts

* [[algebraic theory]] / [[Lawvere theory]] /  [[(∞,1)-algebraic theory]]

* [[monad]] / **2-monad**/ [[doctrine]] / [[(∞,1)-monad]]

* [[operad]] / [[(∞,1)-operad]]

## References

* R. Blackwell, G. M. Kelly, and A. J. Power, _Two-dimensional monad theory_, Jour. Pure Appl. Algebra 59 (1989), 1--41
* F. Marmolejo, _Doctrines whose structure forms a fully faithful adjoint string_, Theory and Applications of Categories 3 (1997), 23--44. &lt;http://www.tac.mta.ca/tac/volumes/1997/n2/3-02abs.html>
* [[Steve Lack|S. Lack]], _A coherent approach to pseudomonads_, Adv. Math. 152 (2000), 179--202. &lt;http://www.maths.usyd.edu.au:8000/u/stevel/papers/psm.ps.gz>
* G.M. Kelly and S. Lack, _On property-like structures_, Theory and Applications of Categories 3 (1997) 213--250.  &lt;http://www.tac.mta.ca/tac/volumes/1997/n9/3-09abs.html>
* S. Lack, _Codescent objects and coherence_, JPAA 175 (2002), 223--241.
* I. J. Le Creurer, F. Marmolejo, E. M. Vitale, _Beck's theorem for pseudo-monads_, J. Pure Appl. Algebra 173 (2002), no. 3, 293--313. 

[[!redirects strict 2-monad]]
[[!redirects weak 2-monad]]
[[!redirects pseudo monad]]
[[!redirects pseudo-monad]]
[[!redirects pseudomonad]]
[[!redirects 2-monads]]
[[!redirects pseudomonads]]
[[!redirects pseudo-monads]]
[[!redirects strict 2-monads]]

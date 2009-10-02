A **2-monad** is a [[monad]] on a [[2-category]], or more generally a monad _in_ a [[3-category]].  This concept manifests at varying levels of strictness:

* For a _strict 2-monad_ (which classically is called a simply a "2-monad"), the 2-category $K$ is a [[strict 2-category]], the functor $T:K\to K$ is a [[strict 2-functor]], and the transformations $\mu$ and $\eta$ are [[strict 2-natural transformation]]s and satisfy their laws strictly.  Strict 2-monads live naturally in [[strict 3-category|strict 3-categories]].

* For a fully _weak 2-monad_, $K$ is a weak 2-category (such as a [[bicategory]]), $T$ is a weak (aka pseudo) 2-functor, and $\mu$ and $\eta$ are pseudo natural transformations that satisfy their laws up to specified isomorphisms satisfying coherence conditions.  Weak 2-monads live naturally in fully weak 3-categories (or [[tricategory|tricategories]])

* In between we have various notions that are sometimes called _pseudomonads_.  For instance, we could require $K$ to be a strict 2-category and $T$ a strict 2-functor, but $\mu$ and $\eta$ only pseudo natural.  This sort of pseudomonad lives naturally in a [[Gray-category]].

One can consider various 2-categories of _[[algebra]]s_ (pseudo algebras, $2$-algebras) for a 2-monad, depending on whether the algebras satisfy their laws strictly or weakly, and whether the morphisms commute with the algebra structure strictly or weakly.

Many common types of structure on categories are specified by strict algebras for a strict 2-monad, but usually the strict morphisms are too strict.  There are three types of weak morphism: _pseudo_ (which preserve the structure up to a specified coherent isomorphism), _lax_ (which preserve it up to a noninvertible transformation) and _colax_ or _oplax_ (for which the transformation goes the other direction).

For example, ordinary (non-strict) [[monoidal category|monoidal categories]] are the _strict_ algebras for a strict 2-monad on $Cat$, but usually we care about pseudo, lax, and oplax [[monoidal functor]]s rather than strict ones.  _Strict_ monoidal categories are the strict algebras for a _different_ strict 2-monad on $Cat$, and the _pseudo_ algebras for _this_ 2-monad are, not ordinary monoidal categories, but [[bias|unbiased]] monoidal categories.

There are also 2-monads that specify [[property-like structure]].  For instance, there is a 2-monad whose algebras are categories with finite products.  Actually, its algebras are categories equipped with _specified_ finite products, the strict morphisms of these algebras preserve these specified finite products on the nose, and the pseudo morphisms preserve them in the usual sense of "preserving finite products."  In this case, _every_ functor between algebras is an oplax morphism, since there is always a canonical comparison map $F(A\times B) \to F(A)\times F(B)$.

# Doctrines

2-monads (particularly on [[Cat]]) are also sometimes called [[doctrine]]s, with the intuition in mind that they are an "algebraic theory" of structure on a category just as a monad (on $Set$) is an [[algebraic theory]] of structure on a set.  However, this use of terminology is arguably at variance with the original intuitive meaning of "doctrine."

# References

* R. Blackwell, G. M. Kelly, and A. J. Power, Two-dimensional monad theory, Jour. Pure Appl. Algebra 59 (1989), 1--41
* F. Marmolejo, Doctrines whose structure forms a fully faithful adjoint string, Theory and Applications of Categories 3 (1997), 23--44. &lt;http://www.tac.mta.ca/tac/volumes/1997/n2/3-02abs.html>
* [[Steve Lack|S. Lack]], A coherent approach to pseudomonads, Adv. Math. 152 (2000), 179--202. &lt;http://www.maths.usyd.edu.au:8000/u/stevel/papers/psm.ps.gz>
* G.M. Kelly and S. Lack, On property-like structures, Theory and Applications of Categories 3 (1997) 213--250.  &lt;http://www.tac.mta.ca/tac/volumes/1997/n9/3-09abs.html>
* S. Lack, Codescent objects and coherence.  JPAA 175 (2002), 223--241.


[[!redirects strict 2-monad]]
[[!redirects weak 2-monad]]
[[!redirects pseudo monad]]
[[!redirects pseudo-monad]]
[[!redirects pseudomonad]]
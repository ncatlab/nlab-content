A **lax functor** or **lax $n$-[[n-functor|functor]]** is a morphism of $n$-[[n-category|categories]] that is allowed to have structural cells -- compositors, associators, etc -- that need not be invertible (not even [[weak inverse|weakly]]).

This is to distinguish from [[pseudofunctor]] for which all these cells are required to be [[equivalences]].

This means that the definition of lax functor involves a choice of orientation of these structural cells which is not visible for pseudofunctors. The choice is such that the first example below comes out as stated. With the opposite choice one speaks of an **oplax functor**.

Often the term lax functor is often used for $n$-functors $F : C \to D$ whose domain $C$ is an ordinary [[category]] (regarded as an $n$-category with only trivial higher morphisms), while the codomain $D$ is often taken to be a [[2-category]].

# Examples #

* For $D$ a [[bicategory]], lax functors $F : {*} \to D$ from the [[point]] category to $D$ are equivalent to [[monad]]s in $D$.

  The compositor of the lax functor is the monad product, the unitor is the monad unit.

  * So in particular for $V$ a [[monoidal category]] and $\mathbf{B}V$ its one-object [[delooping]] [[bicategory]], lax functors ${*} \to \mathbf{B}V$ are equivalent to [[monoid]]s in $V$.
 
* Similarly, oplax functors ${*} \to D$ are equivalent to [[comonad]]s in $D$.

* If $C$ is the [[codiscrete category]] on a set $S$, and $D$ is a [[bicategory]], lax functors $F : C \to D$ are the same as categories enriched in $D$ having $S$ as their set of objects.  

   * In particular, if $C = {*}$, then this example reduces to the first one.  

   * Another special case arises when $D = \mathbf{B}V$ for some monoidal category $V$.  Then lax functors $F : C \to D$ are the same as categories enriched in the monoidal category $V$.  

* It makes sense to ask that a functor is lax _and_ oplax in a compatible way such that ${*} \to D$ yields [[Frobenius algebra|Frobenius]] monads.

  This is of relevance in [[conformal field theory]] where Frobenius algebra objects in [[modular tensor category|modular tensor categories]] and bimodules over them play a central role.

  Some old remarks on this case are in [Note on lax functors and bimodules](http://www.math.uni-hamburg.de/home/schreiber/LaxFunc.pdf).

  This relation between lax-oplax functors and [[conformal field theory]] was developed in detail in

  * Liang Kong, Ingo Runkel, _Cardy algebras and sewing constraints, I_ ([arXiv](http://arxiv.org/abs/0807.3356))

  A general discussion of lax-oplax functors is in section 2.1 there.


[[!redirects oplax functor]]
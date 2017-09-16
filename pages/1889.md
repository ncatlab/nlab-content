
A **lax functor** or lax [[n-functor]] is a morphism of [[n-category|n-categories]] that is allowed to have structural cells -- compositors, associators, etc -- that need not be invertible.

This is to distinguish from [[pseudofunctor]] for which all these cells are required to be equivalences.

This means that the definition of lax functor involves a choice of orientation of these structural cells which is not visible for pseudofunctors. The choice is such that the first example below comes out as stated. With the opposite choice one speaks of an **oplax functor**.

Often the term lax functor is often used for $n$-functors $F : C \to D$ whose domain $D$ is an ordinary [[category]] (regarded as an $n$-category with only trivial higher morphisms), while the codomain $D$ is often taken to be a [[2-category]].

# Examples #

* For $D$ a [[bicategory]], lax functors $F : {*} \to D$ from the [[point]] category to $D$ are equivalent to [[monad]]s in $D$.

  The compositor of the lax functor is the monad product, the unitor is the monad unit.

  * So in particular for $V$ a [[monoidal category]] and $\mathbf{B}V$ its one-object [[delooping]] [[bicategory]], lax functors ${*} \to \mathbf{B}V$ are equivalent to [[monoid]]s in $V$.
 
* Similarly, oplax functors ${*} \to D$ are equivalent to [[comonad]]s in $D$.

* If $C$ is the [[codiscrete category]] on a set $S$, and $D$ is a [[bicategory]], lax functors $F : C \to D$ are the same as categories enriched in $D$ having $S$ as their set of objects.  

   * In particular, if $C = {*}$, then this example reduces to the first one.  

   * Another special case arises when $D = \mathbf{B}V$ for some monoidal category $V$.  Then lax functors $F : C \to D$ are the same as categories enriched in the monoidal category $V$.  



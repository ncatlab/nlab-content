An __idempotent monad__  is a [[monad]] $(T,\mu,\eta)$ on a category $C$ such that one (hence all) of the following equivalent statements are true:

1. $\mu: T T \to T$ is a [[natural transformation|natural isomorphism]].

1. For every $T$-algebra ($T$-module)
$(M,u)$, the corresponding $T$-action $u: T M \to M$ is an isomorphism.

1. The forgetful functor $C^T \to C$ (where $C^T$ is the [[Eilenberg-Moore category]] of $T$-algebras) is a [[full and faithful functor]].

The last statement means that in such a case $C^T$ is, up to equivalence a full [[reflective subcategory]] of $C$.  Conversely, the monad induced by any reflective subcategory is idempotent, so giving an idempotent monad on $C$ is equivalent to giving a reflective subcategory of $C$.

In the language of [[stuff, structure, property]], an idempotent monad may be said to equip its algebras with _properties only_ (since $C^T\to C$ is fully faithful), unlike an arbitrary monad, which equips its algebras with _at most structure_ (since $C^T\to C$ is, in general, faithful but not full).

+--{+ .query}
[[Zoran Skoda]]: what do you mean ? The canonical monadic projection functor from EM category by definition forgets the action. 

_Toby_:  This means that it can only forget 'structure', not 'stuff' in the sense of [[stuff, structure, property]].  By definition, that means precisely that it is faithful.

_Zoran_ Aha. I do not use that terminology. Word faithful is standard and 'not forgetting stuff' is confusing and too long in my view. 

_Toby_:  It\'s not supposed to be a technical term but a guide to intuition.  Personally, I wouldn\'t include that sentence about not forgetting stuff, since the previous sentence already states that $C^T \to C$ always forgets at most structure.  But it does help me to get a feel for idempotent monads to see that, in that case, $C^T \to C$ forgets only property.

[[Mike Shulman|Mike]]: Ok, I agree that that sentence is unnecessary and possibly confusing, so I removed it.  I think this query box could now be removed as well.
=--

# References#

* F. Borceux, _Handbook of categorical algebra_, vol.2, p. 196.

* P. Gabriel and M. Zisman, _Calculus of Fractions and Homotopy Theory_
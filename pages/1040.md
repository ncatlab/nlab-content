An __idempotent monad__  is a [[monad]] $(T,\mu,\eta)$ on a category $C$ such that one (hence all) of the following equivalent statements are true:

1. $\mu: T T \to T$ is a [[natural transformation|natural isomorphism]].

1. For every $T$-algebra ($T$-module)
$(M,u)$, the corresponding $T$-action $u: T M \to M$ is an isomorphism.

1. The forgetful functor $C^T \to C$ (where $C^T$ is the [[Eilenberg-Moore category]] of $T$-algebras) is a [[full and faithful functor]].

The last statement means that in such a case $C^T$ is, up to equivalence a full [[reflective subcategory]] of $C$.  Conversely, the monad induced by any reflective subcategory is idempotent, so giving an idempotent monad on $C$ is equivalent to giving a reflective subcategory of $C$.

In the language of [[stuff, structure, property]], an idempotent monad may be said to equip its algebras with _properties only_ (since $C^T\to C$ is fully faithful), unlike an arbitrary monad, which equips its algebras with _at most structure_ (since $C^T\to C$ is, in general, faithful but not full).  Note that no functor which forgets _stuff_ (in the precise sense of [[stuff, structure, property]]) can be monadic.

+--{+ .query}
[[Zoran Skoda]]: what do you mean ? The canonical monadic projection functor from EM category by definition forgets the action. 

_Toby_:  This means that it can only forget 'structure', not 'stuff' in the sense of [[stuff, structure, property]].  By definition, that means precisely that it is faithful.
=--

# References#

* F. Borceux, _Handbook of categorical algebra_, vol.2, p. 196.

* P. Gabriel and M. Zisman, _Calculus of Fractions and Homotopy Theory_
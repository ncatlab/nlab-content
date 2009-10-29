An __idempotent monad__  is a [[monad]] $(T,\mu,\eta)$ on a category $C$ such that one (hence all) of the following equivalent statements are true:

1. $\mu: T T \to T$ is a [[natural transformation|natural isomorphism]].

1. For every $T$-algebra ($T$-module)
$(M,u)$, the corresponding $T$-action $u: T M \to M$ is an isomorphism.

1. The forgetful functor $C^T \to C$ (where $C^T$ is the [[Eilenberg-Moore category]] of $T$-algebras) is a [[full and faithful functor]].

The last statement means that in such a case $C^T$ is, up to equivalence a full [[reflective subcategory]] of $C$.  Conversely, the monad induced by any reflective subcategory is idempotent, so giving an idempotent monad on $C$ is equivalent to giving a reflective subcategory of $C$.

In the language of [[stuff, structure, property]], an idempotent monad may be said to equip its algebras with _properties only_ (since $C^T\to C$ is fully faithful), unlike an arbitrary monad, which equips its algebras with _at most structure_ (since $C^T\to C$ is, in general, faithful but not full).

If $T$ is idempotent, then it follows in particular that an object of $C$ admits at most one structure of $T$-algebra, that this happens precisely when the  unit $\eta_X\colon X\to T X$ is an isomorphism, and in this case the $T$-algebra structure map is $\eta_X^{-1}\colon T X \to X$.  However, it is possible to have a non-idempotent monad for which any object of $C$ admits at most one structure of $T$-algebra, in which case $T$ can be said to equip objects of $C$ with [[property-like structure]]; an easy example is the monad on [[semigroups]] whose algebras are [[monoids]].


# The associated idempotent monad of a monad # 

Let $C$ be a category with [[equalizers]], and let $(T: C \to C, \mu, \eta)$ be a monad on $C$. There is an associated idempotent monad $T'$ which at the functor level is obtained as the equalizer 

$$T' \overset{e}{\to} T \stackrel{\overset{\eta T}{\to}}{\underset{T \eta}{\to}} T T$$ 

The map $\eta: 1_C \to T$ equalizes the pair of maps $\eta T$, $T \eta$, so it factors as $e \circ u$ for some unique map $u: 1_C \to T'$. This defines the unit of the monad $T'$. 

A diagram chase shows that the composite 

$$T' T' \overset{e e}{\to} T T \overset{\mu}{\to} T$$ 

equalizes the pair of maps $\eta T$, $T \eta$; therefore $\mu \circ e e$ factors as $e \circ \mu'$ for some unique map $\mu': T' T' \to T'$. This defines the multiplication of the monad $T'$. By construction, $e: T' \to T$ is a map which preserves the monad structure. 

A result due to Fakir is that the monad $T'$ is idempotent in the sense given above. In fact, if $C$ has equalizers, then the category of idempotent monads on $C$ is a [[coreflective subcategory]] of the category of monads on $C$, meaning that the [[full embedding]] 

$$i: IdemMonad_C \hookrightarrow Monad_C$$ 

has a [[right adjoint]] given by the associated idempotent monad construction. 
 

 

# References#

* F. Borceux, _Handbook of categorical algebra_, vol.2, p. 196.

* P. Gabriel and M. Zisman, _Calculus of Fractions and Homotopy Theory_
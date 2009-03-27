An __idempotent monad__  is a monad $(T,\mu,\eta)$ in a category $C$ such that one of the following equivalent statements are true:

(i) $\mu : TT\to T$ is an isomorphism of the functors;

(ii) for every $T$-algebra ($T$-module)
$(M,u)$, the corresponding $T$-action $u:TM\to M$ is an isomorphism;

(iii) the forgetful functor $C^T\to C$ (where $C^T$ is the Eilenberg-Moore category of $T$-algebras) is a fully faithful functor. 

According to Gabriel-Zisman, there is a correspondence, up to an equivalence of categories, between the [[reflective subcategory|reflective subcategories]] in $C$, and Eilenberg-Moore categories for idempotent monads in $C$.

Literature: F. Borceux, Handbook of categorical algebra, vol.2, p. 196.
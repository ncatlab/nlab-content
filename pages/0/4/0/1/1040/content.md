An __idempotent monad__  is a [[monad]] $(T,\mu,\eta)$ on a category $C$ such that one (hence all) of the following equivalent statements are true:

1. $\mu: T T \to T$ is a [[natural transformation|natural isomorphism]]. 

1. All components of $\mu: T T \to T$ are monic.

1. The maps $T\eta, \eta T: T \to T T$ are equal. 

1. For every $T$-algebra ($T$-module)
$(M,u)$, the corresponding $T$-action $u: T M \to M$ is an isomorphism.

1. The forgetful functor $C^T \to C$ (where $C^T$ is the [[Eilenberg-Moore category]] of $T$-algebras) is a [[full and faithful functor]].

1. There exists an adjunction $F\dashv U$ such that the induced monad $(FU, F\epsilon U)$ is isomorphic to $(T,\mu)$ and $U$ is fully faithful. 

_Proof of equivalence (in more than one way)._  $1\Rightarrow 2$ is trivial.

$2\Rightarrow 3$ Compositions $\mu\circ T\eta$ and $\mu\circ\eta T$ are always the identity (unit axioms for the monad), and in particular agree; if $\mu$ has all components monic, this implies $T\eta = \eta T$. 

$3\Rightarrow 4$ Compatibility of action and unit is $u \circ \eta_M = id_M$, hence also $T(u)\circ T(\eta_M) = id_{T M}$. If $T\eta = \eta T$ then this 
implies $id_M = T(u)\circ \eta_{T M} = \eta_M\circ U$, where the naturality of $\eta$ is used in the second equality. Therefore we exhibited $\eta_M$ both as a left and a right inverse of $u$. 

$4\Rightarrow 1$ If every action is iso, then the components of multiplication $\mu_M : TTM\to TM$ are isos as a special case, namely of the free action on $TM$. 

$4\Rightarrow 5$ For any monad $T$, the forgetful functor from Eilenberg-Moore category $C^T$ to $C$ is faithful: a morphism of $T$-algebras is always a morphism of underlying objects in $C$. To show that it is also full, we consider any pair $(M,u)$, $(M',u')$ in $C^T$ 
and must show that any $f: M\to M'$ is actually 
a map $f : (M,u)\to (M',u')$; i.e. $u'\circ Tf = f\circ u$. But we know that $\eta_M, \eta_{M'}$ are inverses of $u,u'$ respectively and 
the naturality for $\eta$ says $\eta_{M'}\circ f = Tf \circ \eta_M$. Compose that equation with $u$ on the right and $u'$ on the left with the result (notice that we used just the invertibility of $u$).  

$5\Rightarrow 6$ Trivial, because the Eilenberg-Moore construction induces the original monad by the standard recipe. 

$6\Rightarrow 3$ By $6$ the counit $\epsilon$ is iso, hence $U\epsilon F$ has a unique 2-sided inverse; by triangle identities, $T\eta$ and $\eta T$ are both right inverses of $U\epsilon F$, hence 2-sided inverses, hence they are equal.

$6\Rightarrow 1$ If $F\dashv U$ is an adjunction with $U$ fully faithful, 
then the counit $\epsilon$ is iso. The induced monad has multiplication 
$\mu = U\epsilon F$ hence iso; every isomorphic monad is also iso. Q. E. D. 

Part 5 means that in such a case $C^T$ is, up to equivalence a full [[reflective subcategory]] of $C$.  Conversely, the monad induced by any reflective subcategory is idempotent, so giving an idempotent monad on $C$ is equivalent to giving a reflective subcategory of $C$.

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
 
+--{: .query}
[[Mike Shulman]]: How about some examples of monads and their associated idempotent monads?

Do 2-monads have associated lax-, colax-, or pseudo-idempotent 2-monads?
=--
 

# References#

* F. Borceux, _Handbook of categorical algebra_, vol.2, p. 196.

* P. Gabriel and M. Zisman, _Calculus of Fractions and Homotopy Theory_
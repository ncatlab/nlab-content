A geometric morphism $f: E \to F$ between Grothendieck toposes is defined to be a pair of functors $f^* : F \to E$, $f_* : E \to F$ for which $f^*$ is left adjoint to $f_*$ and preserves finite limits. This terminology was inspired by the observation that if $E$ and $F$ are the toposes of sheaves on sober topological spaces $X$ and $Y$ respectively, then continuous maps $X \to Y$ correspond precisely to geometric morphisms $E \to F$. The question then arises as to what sort of structures are preserved by the _inverse image_ functors (i.e. the $f^*$) of geometric morphisms. Clearly, those definable using finite limits and small colimits. In syntactic terms these are the models of **geometric theories**. A geometric theory is a first order theory (because in general inverse images do not preserve power-set formation) definable by an axiom scheme consisting of universally quantified implications between **positive** predicates. A predicate is positive if it contains no universal quantifiers, no implications and no negations.

By framing this notion in the internal language of a topos $S$ we can talk of geometric theories over $S$, with models in $S$-toposes. As a simple example, if we have a sheaf $A$ of rings on a topological space $X$ we can describe left $A$-modules as models of a geometric theory over $Sh(X)$, the topos of sheaves on X, and this notion is definable in $Sh(X)$-toposes.

Given a geometric theory $T$ over a topos $S$ we can form the $S$-topos $S[T] \to S$ that _classifies_ $T$. That is to say that the category of $T$-models in an $S$-topos $E$ is naturally equivalent to the category of morphisms of $S$-toposes $E \to S[T]$. In other words

$$T-mod(E) \simeq Top_S(E,S[T])$$

If $T'$ is another geometric theory over $S$, then we may say that a map of theories $T \to T'$ is a morphism of $S$-toposes $h: S[T'] \to S[T]$; equivalently it is a $T$-model in $S[T']$. Composition with $h$ induces a functor, _forget along_ $h$, from $T'$-models to $T$-models in any $S$-topos. If we pass to the _gros categories of models_ then these forgetful functors have left adjoints.
For if $a: E \to S[T]$ is a $T$-model in $E$, pulling $a$ back along $h$ yields a $T'$-model, not in $E$ but in the pullback.

Define the gros category $T-mod$ of $T$-models to have as objects pairs $(E,A)$ where $E$ is an $S$-topos and $A$ is
a $T$-model in $E$. A map $(f,g): (E,A) \to (F,B)$ is given
by a morphism $f: F \to E$ of $S$-toposes and a homomorphism $g: f^*(A) \to B$ of $T$-models in $F$. The
composition of maps should be evident. A map $h: T \to T'$
of geometric theories over $S$ induces a forgetful functor
$T'-Mod \to T-Mod$ which leaves unchanged the $S$-topos of residence, which has a left adjoint $T-Mod \to T'-Mod$ which may change the topos. This is a consequence of general facts about finite 2-limits of the 2-category of 
bounded $S$-toposes.


# Definition #

Recall that an [[orthogonal factorization system|(orthogonal) factorization system]] in a [[category]] $C$ consists of two classes of maps $(E,M)$ such that every morphism in $C$ factors as an $E$-morphism followed by an $M$-morphism, and we have $e\perp m$ for any $e\in E$ and $m\in M$ (see [[orthogonality]]).

To [[enriched category|enrich]] this, we should first consider enriched orthogonality.  The statement $e\perp m$ for maps $e:A\to B$ and $m:X\to Y$ can be rephrased by saying that the square
$$
\array{C(B,X) & \to & C(A,X)\\
  \downarrow && \downarrow \\
  C(B,Y) & \to & C(A,Y)}
$$
is a [[pullback]] in [[Set]].  It is then clear that if $C$ is enriched over some [[monoidal category]] $V$, to say that $e\perp m$ in an enriched sense, we should instead require this square to be a pullback of enriched hom-objects in $V$.  Note, though, that $e$ and $m$ are still maps in the underlying ordinary category $C_0$ of $C$.  Likewise, the factorization property still only makes sense for maps in $C_0$.

Therefore, we define an **enriched (orthogonal) factorization system** on an enriched category $C$ to consist of two classes of maps $(E,M)$ in $C_0$ such that

1. $e\perp m$ in the above enriched sense for every $e\in E$ and $m\in M$, and
1. Every map in $C_0$ factors as an $E$-map followed by an $M$-map.

By the definition of $C_0$, enriched orthogonality implies ordinary orthogonality.  Therefore, an enriched factorization system on $C$ induces an ordinary factorization system on $C_0$.  Conversely, if $C$ has [[power]]s that preserve the maps in $M$, or [[copower]]s that preserve the maps in $E$, then unenriched orthogonality in $C_0$ implies enriched orthogonality by a Yoneda lemma argument.


# Functoriality #

Moreover, the factorization functor can be made into an enriched functor in the following way.  There is a $V$-category $C^{\mathbf{2}}$ whose objects are morphisms in $C_0$ and whose hom-objects are defined by, for $f_1:X_1\to Y_1$ and $f_2:X_2\to Y_2$, a pullback
$$
\array{C^{\mathbf{2}}(f_1,f_2) & \to & C(X_1,X_2)\\
  \downarrow && \downarrow \\
  C(Y_1,Y_2) & \to & C(X_1,Y_2).}
$$
(This is the [[power]] of $C$ by ${\mathbf{2}}$ in the 2-category $V-Cat$, and also the $V$-functor category $[{\mathbf{2}}_V,C]$, where ${\mathbf{2}}_V$ denotes the free $V$-category on ${\mathbf{2}}$.)

Likewise, we have $C^{\mathbf{3}}$ whose objects are composable pairs $X\overset{f}{\to} Y \overset{g}{\to} Z$ of morphisms in $C_0$, and whose hom-objects are defined by pullbacks
$$
\array{C^{\mathbf{3}}((f_1,g_1),(f_2,g_2)) & \to & C^{\mathbf{2}}(f_1,f_2)\\
  \downarrow && \downarrow \\
  C^{\mathbf{2}}(g_1,g_2) & \to & C(Y_1,Y_2).}
$$
By functoriality we then mean that the factorization is given by a functor $C^{\mathbf{2}} \to C^{\mathbf{3}}$ which, when composed with the "composition" functor $C^{\mathbf{3}} \to C^{\mathbf{2}}$, gives the identity of $C^{\mathbf{2}}$.

The interesting part of the enrichment of this functor is the following: given $f_1:X_1\to Z_1$ and $f_2:X_2\to Z_2$ in $C^{\mathbf{2}}$, with factorizations $X_1 \overset{m_1}{\to} Y_1 \overset{e_1}{\to} Z_1$ and $X_2 \overset{m_2}{\to} Y_2 \overset{e_2}{\to} Z_2$, by enriched orthogonality we have a pullback
$$
\array{C(Y_1,Y_2) & \to & C(X_1,Y_2)\\
  \downarrow & & \downarrow\\
  C(Y_1,Z_2) & \to & C(X_1,Z_2)}
$$
and we also have a commutative square
$$
\array{C^{\mathbf{2}}(f_1,f_2) & \to & C(X_1,X_2) & \to & C(X_1,Y_2)\\
  \downarrow &&&& \\
  C(Z_1,Z_2) &&&& \downarrow\\
  \downarrow &&&& \\
  C(Y_1,Z_2) & & \longrightarrow & & C(X_1,Z_2)
}
$$
inducing a map $C^{\mathbf{2}}(f_1,f_2) \to C(Y_1,Y_2)$.  It is then straightforward to construct the rest of the functor.

This argument, as it depends crucially on the universality of the pullback and hence the uniqueness part of orthogonality, fails for [[weak factorization system]]s.  Although they can be made functorial in many cases, rarely can their functoriality be made enriched (as far as is known).

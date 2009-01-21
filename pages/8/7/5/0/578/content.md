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

By definition of $C_0$, enriched orthogonality implies ordinary orthogonality.  Therefore, an enriched factorization system on $C$ induces an ordinary factorization system on $C_0$.

# Functoriality #

Moreover, the factorization functor can be made into an enriched functor in the following way.  There is a $V$-category $C^{\mathbf{2}}$ whose objects are morphisms in $C_0$ and whose hom-objects are defined by, for $f:X\to Y$ and $g:Z\to W$, a pullback
$$
\array{C^{\mathbf{2}}(f,g) & \to & C(X,Z)\\
  \downarrow && \downarrow \\
  C(Y,W) & \to & C(X,W)}.
$$
(This is the [[power]] of $C$ by ${\mathbf{2}}$ in the 2-category $V-Cat$, and also the $V$-functor category $[{\mathbf{2}}_V,C]$, where ${\mathbf{2}}_V$ denotes the free $V$-category on ${\mathbf{2}}$.)  Likewise, we have $C^{\mathbf{3}}$ whose objects are composable pairs of morphisms in $C_0$.  By functoriality we then mean that it is given by a functor $C^{\mathbf{2}} \to C^{\mathbf{3}}$ which gives the identity when composed with the "composition" functor $C^{\mathbf{3}} \to C^{\mathbf{2}}$.

(to be continued...)

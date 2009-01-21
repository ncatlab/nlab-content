# Definition #

Two [[morphism]]s $e:A\to B$ and $m:C\to D$ in a [[category]] are said to be **orthogonal**, written $e\perp m$, if in any commutative square
$$
\array{ A & \overset{e}{\to} & B\\
  \downarrow && \downarrow \\
  C & \underset{m}{\to} & D}
$$
there exists a unique diagonal filler making both triangles commute:
$$
\array{ A & \overset{e}{\to} & B\\
  \downarrow & \swarrow & \downarrow \\
  C & \underset{m}{\to} & D}
$$

Given a class of maps $E$, the class $\{m | e\perp m \;\forall e\in E\}$ is denoted $E^{\downarrow}$ or $E^\perp$.  Likewise, given $M$, the class $\{e | e\perp m \;\forall m\in M\}$ is denoted $M^{\uparrow}$ or ${}^\perp M$.  These operations form a [[Galois connection]] on the poset of classes of morphisms in the ambient category.  In particular, we have $({}^\perp(E^\perp))^\perp = E^\perp$ and ${}^\perp(({}^\perp M)^\perp) = {}^\perp M$.

A pair $(E,M)$ such that $E^\perp = M$ and $E = {}^\perp M$ is sometimes called a **prefactorization system**.  If in addition every morphism factors as an $E$-morphism followed by an $M$-morphism, it is an (orthogonal) [[orthogonal factorization system|factorization system]].

# Examples #

* Of course, any [[orthogonal factorization system]] gives plenty of examples.  The ur-example is that $e\perp m$ in [[Set]] (or actually, any [[pretopos]]) for any surjection $e$ and injection $m$.

* A [[strong epimorphism]] in any category is, by definition, an epmiorphism in ${}^\perp(Mono)$ where $Mono$ is the class of monomorphisms.  (If the category has equalizers, then every map in ${}^\perp(Mono)$ is epic.)  Dually, a [[strong monomorphism]] is a monomorphism in $(Epi)^\perp$.

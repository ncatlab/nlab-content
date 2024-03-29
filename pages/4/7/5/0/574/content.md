
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

(This entry describes two distinct notions, one in the theory of [[inner product spaces]], and the second in a more purely [[category theory|category theoretic]] context.)

## In inner product spaces

Two elements $x,y$ in an [[inner product space]], $(V, \langle -,-\rangle)$, are **orthogonal** or [[normal vectors]], denoted $x \perp y,$ if $\langle x,y\rangle = 0$.

## In category theory

### Definition 

Two [[morphism]]s $e:A\to B$ and $m:C\to D$ in a [[category]] are said to be **orthogonal**, written $e\perp m$, if $e$ has the [[left lifting property]] with respect to $m$, i.e. if in any [[commutative diagram|commutative square]]

$$
\array{ A & \overset{e}{\to} & B\\
  \downarrow && \downarrow \\
  C & \underset{m}{\to} & D}
$$

there exists a unique diagonal [[filler]] making both triangles commute:

$$
\array{ A & \overset{e}{\to} & B\\
  \downarrow & \swarrow & \downarrow \\
  C & \underset{m}{\to} & D}
$$

Given a [[class]] of maps $E$, the class $\{m | e\perp m \;\forall e\in E\}$ is denoted $E^{\downarrow}$ or $E^\perp$.  Likewise, given $M$, the class $\{e | e\perp m \;\forall m\in M\}$ is denoted $M^{\uparrow}$ or ${}^\perp M$.  These operations form a [[Galois connection]] on the poset of classes of morphisms in the ambient category.  In particular, we have $({}^\perp(E^\perp))^\perp = E^\perp$ and ${}^\perp(({}^\perp M)^\perp) = {}^\perp M$.

A pair $(E,M)$ such that $E^\perp = M$ and $E = {}^\perp M$ is sometimes called a **prefactorization system**.  If in addition every morphism factors as an $E$-morphism followed by an $M$-morphism, it is an (orthogonal) [[orthogonal factorization system|factorization system]].

### Examples 

* Of course, any [[orthogonal factorization system]] gives plenty of examples.  The ur-example is that $e\perp m$ in [[Set]] (or actually, any [[pretopos]]) for any surjection $e$ and injection $m$.

* A [[strong epimorphism]] in any category is, by definition, an epimorphism in ${}^\perp(Mono)$, where $Mono$ is the class of monomorphisms.  (If the category has equalizers, then every map in ${}^\perp(Mono)$ is epic.)  Dually, a [[strong monomorphism]] is a monomorphism in $(Epi)^\perp$.

* The [[orthogonal subcategory problem]] for a [[class]] of [[morphism]]s $\Sigma$ in a [[category]] $C$ asks whether the [[full subcategory]] $\Sigma^\perp$ of [[object]]s $X$ [[orthogonal]] to $\Sigma$ is a [[reflective subcategory]]. Here we define $f \perp X$ to mean $f \perp !: X \to 1$. 

  The orthogonal subcategory problem is related to [[localization]]. Suppose $\Sigma^\perp$ is indeed a [[reflective subcategory]]; let $r: C \to \Sigma^\perp$ be the reflector (the [[left adjoint]] to the inclusion $i: \Sigma^\perp \to C$). Certainly $r$ sends arrows in $\Sigma$ to isomorphisms in $\Sigma^\perp$. Indeed, if $f: A \to B$ belongs to $\Sigma$, then the inverse to $r(f): r(A) \to r(B)$ is the unique arrow extending $1_{r(A)}$ along $r(f): r(A) \to r(B)$ to an arrow $g: r(B) \to r(A)$, using the fact that $r(A)$ belongs to $\Sigma^\perp$. 

## Related concepts

* [[injective object]]

[[!include (co)isotropic subspaces - table]]

* [[orthogonal structure]], [[orthogonal basis]]

* [[Grassmannian]], [[Stiefel manifold]]

* [[orthogonal spectrum]], [[coordinate-free spectrum]], [[equivariant spectrum]]

[[!redirects orthogonal]]

[[!redirects orthogonal complement]]
[[!redirects orthogonal complements]]

[[!redirects perpendicular]]

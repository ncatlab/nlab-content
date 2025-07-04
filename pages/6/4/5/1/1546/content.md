
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The **Atiyah Lie groupoid** $At(P)$ of a smooth $G$-[[principal bundle]] $P \to X$ is the [[Lie groupoid]] whose [[objects]] are the [[fibers]] of the bundle, and whose [[morphisms]] are the $G$-[[equivariant maps]] between the fibers. 

Schematically:

$$
  At(P)
  \,=\, 
  \left\{
     P_x \stackrel{\alpha}{\to} P_y
     | x,y \in X
  \right\}
  \,.
$$

Its [[Lie algebroid]] is the [[Atiyah Lie algebroid]] $at(P)$ of $P$.

Both the Atiyah Lie groupoid and its Lie algebroid are used to characterize and are characterized by [[connection on a bundle|connections]] on $P$.



## Definition

As generally for every [[Lie algebroid]], there are different [[Lie groupoids]] [[Lie integration|integrating]] the [[Atiyah Lie algebroid]]. We describe two of them.

The Atiyah Lie algebroid $at(P)$ of the [[principal bundle]] $P \to X$ comes canonically with a morphism $at(X) \to T X$ to the [[tangent Lie algebroid]].

The simplest [[Lie integration]] of the tangent Lie algebroid is the [[pair groupoid]] $X \times X$ of $X$. On the other hand, the universal integration is the [[fundamental groupoid]] $\Pi(X)$ (both coincide precisey if $X$ is a [[simply connected space]]). 

Accordingly, there is a version of the Atiyah Lie groupoid over $X \times X$, and a richer version over $\Pi(X)$. 

### Over the pair groupoid

For $G$ a Lie group and $p \colon P \to X$ a $G$-principal bundle, the **Atiyah groupoid** $At(P)$ -- also called the **gauge groupoid** or **transport groupoid** -- of $P$ is the [[Lie groupoid]] with

* the [[smooth manifold]] of [[objects]] is $Obj(At(P)) \coloneqq X$;
* the [[smooth manifold]] of [[morphisms]] $Mor(At(P)) = (P \times P)/G$, where the [[quotient object|quotient]] is taken with respect to the [[diagonal action]] of $G$ on $P \times P$;

* the [[source]]/[[target]] maps are those induced by the bundle projection $p$;

  notice that a point $f \colon * \to (P \times P)/G$ over $(x_1 = s(f), x_2 = t(f))$, being an [[equivalence class]] of a pair $(s_1, s_2) \in P \times P$ is canonically identified with the unique $G$-equivariant [[function]] $f \colon P_{x_1} \to P_{x_2}$ which sends $s_1$ to $s_2$;

* [[composition]] is the given by ordinary composition of these functions.


### The integrated Atiyah sequence

The Atiyah groupoid sits in a sequence of groupoids

$$
  Ad(P) \to At(P) \to Pair(X)
$$

where

* $Ad(P) = P \times_G G$ is the **adjoint bundle** of groups associated via the adjoint action of $G$ on itself; regarded as a smooth union $\coprod_{x \in X} \mathbf{B} P_x \times_G G$ of one-object groupoids coming from [[group]]s;

* $Pair(X) = (X \times X \rightrightarrows X)$ is the [[pair groupoid]] of $X$

* the [[functor]] $Ad(P) \to At(P)$ is the identity on objects and on morphisms given by the canonical identification $P_x \times_G G \stackrel{\simeq}{\to} (P_x \times P_x)/G$, where again we use the diagonal action of $G$ on $P_x \times P_x$.

* the functor $At(P) \to Pair(X)$ is the unique one that is the identity on objects.



Notice that a splitting (a [[section]])

$$
  Pair(X) \to At(P)
$$

of the Atiyah groupoid is a trivialization of $P$. On the other hand, locally on [[contractible space|contractible]] $U \subset X$ we have $Pair(U) \simeq \Pi_1(U)$ with $U$ the [[fundamental groupoid]] of $U$, and a splitting $Pair(U) \simeq \Pi_1(U) \to At(P)|_U$ is still a trivialization over $U$ but indicates now that one may want to interpret it as giving rise to a flat [[connection]].

### Over a path groupoid

We have the sequence of  surjective and [[full functor]]s of
[[path category|path categories]]  

$$
  P_1(X) \to \Pi_1(X) \to Pair(X)
$$

with $\Pi_1(X)$ the [[fundamental groupoid]] and $P_1(X)$ the smooth [[path groupoid]] and may refine the Atiyah groupoid by pulling back along these.

Write therefore $At'(P) := At(P) \times_{Pair(X)} \Pi_1(X)$ for the [[pullback]]

$$
  \array{
     At'(P) &\to& \Pi_1(X)
     \\
     \downarrow && \downarrow
     \\
     At(P) &\to& Pair(X)
  }
  \,.
$$ 

A splitting $\Pi_1(X) \to At'(P)$ of the top row is now precisely a flat [[connection]] on $P$.

If we pull back further to $A''$ 

$$
  \array{
     At''(P) &\to& P_1(X)
     \\
     \downarrow && \downarrow
     \\
     At'(P) &\to& \Pi_1(X)
     \\
     \downarrow && \downarrow
     \\
     At(P) &\to& Pair(X)
  }
  \,.
$$ 

then splittings of $P_1(X) \to At''(X)$ are precisely (not necessarily flat) connections on $P$.

All this is more well known in terms of the [[Lie algebroid]] underlying the Atiyah Lie groupoid, i.e. the **Atiyah Lie algebroid** sequence

$$
  ad(P) \to at(P) \to T X
  \,,
$$

where 

* $ad(P) = P \times_g Lie(G)$ is the adjoint bundle of Lie algebras, associated via the adjoint action of $G$ on its Lie algebra;

* $at(P) = (T P)/G$ is the **Atiyah Lie algebroid**

* $T X$ is the [[tangent Lie algebroid]].

Indeed, a splitting $\nabla_{flat} : T X \to at(P)$ of this sequence in the category of [[Lie algebroid]]s is precisely again a flat connection on $P$ and integrates under [[Lie integration]] to the splitting of $At'(P)$ discussed above.

To get non-flat connections in the literature one often sees discussed splittings of the Atiyah Lie algebroid sequence in the category just of vector bundles. In that case one finds the curvature of the connection precisely as the obstruction to having a splitting even in Lie algebroids.

One can describe non-flat connections without leaving the context of Lie algebroids by passing to higher Lie algebroids, namely $L_\infty$-[[L-infinity-algebroid|algebroids]].


## Related concepts

* [[higher Atiyah groupoid]]

  * [[Atiyah Lie groupoid]], [[Atiyah Lie algebroid]]

  * [[Courant Lie 2-groupoid]], [[Courant Lie 2-algebroid]]

  * [[quantomorphism group]], [[quantomorphism n-group]]

* [[Schauenburg bialgebroid]] (analogue for affine noncommutative principal bundles)

[[!include higher Atiyah groupoid - table]]



[[!redirects Atiyah Lie groupoids]]

[[!redirects Atiyah Lie-groupoid]]

[[!redirects Atiyah groupoid]]
[[!redirects Atiyah groupoids]]


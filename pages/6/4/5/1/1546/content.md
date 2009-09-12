#Idea#

The Atiyah Lie groupoid of a $G$-[[principal bundle]] is the [[Lie groupoid]] whose objects are the fibers of the bundle, and whose morphisms are the $G$-equivariant morphisms between the fibers.

#Definition#

For $G$ a Lie group and $P \to X$ a $G$-principal bundle, the **Atiyah groupoid** $At(P)$ -- also called the **gauge groupoid** or **transport groupoid** -- of $P$ is the [[Lie groupoid]] with

* $Obj(At(P)) = X$;
* $Mor(At(P)) = (P \times P)/G$, where the [[quotient object|quotient]] is taken with respect to the [[diagonal action]] of $G$ on $P \times P$.

The Atiyah groupoid sits in an sequence of groupoids

$$
  Ad(P) \to At(P) \to Codisc(X)
$$

where

* $Ad(P) = P \times_G G$ is the **adjoint bundle** of groups associated via the adjoint action of $G$ on itself; regarded as a smooth union $\coprod_{x \in X} \mathbf{B} P_x \times_G G$ of one-object groupoids coming from [[group]]s;

* $Codisc(X) = (X \times X \rightrightarrows X)$ is the [[codiscrete groupoid]] of $X$

* the [[functor]] $Ad(P) \to At(P)$ is the identity on objects and on morphisms given by the canonical identification $P_x \times_G G \stackrel{\simeq}{\to} (P_x \times P_x) G$, where again we use the diagonal action of $G$ on $P_x \times P_x$.

* the functor $At(P) \to Codisc(X)$ is the unique one that is the identity on objects.

+-- {: .query}
What is all of this $diag$ stuff?  I don\'t understand either $(P \times P)/_{diag} G$ or $(P_x \times P_x)_{diag} G$.  ---Toby

[[David Roberts]]: It's to do with the diagonal action of $G$ on $P\times P$ as opposed to the antidiagonal (if $G$ is abelian) or the action on only one factor. I agree that it's a bad notation.

_Toby_:  How well do you think it works now, with the notation suppressed and a note added in words?  (For what it\'s worth, the diagonal action seems to me the only obvious thing to do here, although admittedly the others that you mention do exist.)

_Todd_: I personally believe it works well. A small note is that this construction can also be regarded as a tensor product, regarding the first factor $P$ as a right $G$-module and the second a left module, where the actions are related by $g p = p g^{-1}$. 

_Toby_:  H\'m, maybe we should write [[diagonal action]] if there\'s something interesting to say about it.
=--

Notice that a splitting (a [[section]])

$$
  Codisc(X) \to At(P)
$$

of the Atiyah groupoid is a trivialization of $P$. On the other hand, locally on [[contractible space|contractible]] $U \subset X$ we have $Codisc(U) \simeq \Pi_1(U)$ with $U$ the [[fundamental groupoid]] of $U$, and a splitting $Codisc(U) \simeq \Pi_1(U) \to At(P)|_U$ is still a trivialization over $U$ but indicates now that one may want to interpret it as giving rise to a flat [[connection]].

Indeed, we have the sequence of 
of surjective and [[full functor]]s of
[[path category|path categories]]  

$$
  P_1(X) \to \Pi_1(X) \to Codisc(X)
$$

with $\Pi_1(X)$ the [[fundamental groupoid]] and $P_1(X)$ the smooth [[path groupoid]] and may refine the Atiyah groupoid by pulling back along these.

Write therefore $At'(P) := At(P) \times_{Codisc(X)} \Pi_1(X)$ for the [[pullback]]

$$
  \array{
     At'(P) &\to& \Pi_1(X)
     \\
     \downarrow && \downarrow
     \\
     At(P) &\to& Codisc(X)
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
     At(P) &\to& Codisc(X)
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

* $T X$ is the [[Lie algebroid|tangent Lie algebroid]].

Indeed, a splitting $\nabla_{flat} : T X \to at(P)$ of this sequence in the category of [[Lie algebroid]]s is precisely again a flat connection on $P$ and integrates under [[Lie integration]] to the splitting of $At'(P)$ discussed above.

To get non-flat connections in the literature one often sees discussed splittings of the Atiyah Lie algebroid sequence in the category just of vector bundles. In that case one finds the curvature of the connection precisely as the obstruction to having a splitting even in Lie algebroids.

One can describe non-flat connections without leaving the context of Lie algebroids by passing to higher Lie algebroids, namely $L_\infty$-[[L-infinity-algebroid|algebroids]].

#References#

...

some related blog discussion is at

* [n-Transport and Higher Schreier Theory](http://golem.ph.utexas.edu/category/2006/09/nconnections_and_higher_schrei.html)


[[!redirects Atiyah Lie-groupoid]]
[[!redirects Atiyah Lie-algebroid]]
[[!redirects Atiyah Lie algebroid]]

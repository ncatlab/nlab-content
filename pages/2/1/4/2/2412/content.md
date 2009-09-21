

> this is a sub-entry of [[geometric models for elliptic cohomology]] and [[A Survey of Elliptic Cohomology]] 

>see there for background and context.

> **raw material**: this are notes taken more or less verbatim in a seminar -- needs polishing




next:

* [[(1,1)-dimensional Euclidean field theories and K-theory]]

* [[(2,1)-dimensional Euclidean field theories and tmf]]


***

In the following $RB$ or $RBord$ and the like denotes a category of [[cobordism]]s that are equipped with _Riemannian structure_, i.e. with [[Riemannian metric]].
Similarly $EB$ or $EBord$ or the like denotes a category of cobordisms with _Eudlidean structure_, by which is meant a _flat_ Riemannian metric.



**definition**

$d$-dimensional Riemanninan field theories are symmetric monoidal functors $d-RB \to TV$ from $d$-dimensional Riemannian bordisms to [[topological vector space]]s.

A field theory is very similar to a [[representation]] of a group. Only where a representation of a [[group]] $G$ is a functor from the [[delooping]] $\mathbf{B}G = {*}//G$ of $G$ to [[Vect]], an [[FQFT]] is a representation of a more complicated domain category.

**how does [[topology]] enter?**

for $X$ some [[topological space]] there is also a [[symmetric monoidal category]] 

$$
  d-RB(X)
$$

of Riemannian bordisms equipped with a continuous map to $X$.

Notice that $d RB(X)$ does depend covariantly on $X$. This means that Fun^\otimes(d RB(X), TV)$ is contravariant in $X$.

When special structure is around, however, we also have a push-forward of such functors along morphisms.

**Example: push-forward to the point**: for $X$ as above and $X \to {*}$ the unique map to the [[point]] heuristically we want a map

$$
  d RFT(X) \stackrel{p_*}{\to} d RFT(pt)
$$

notice that this push-forward is not an [[adjoint functor]]. Instead, it is a maap that comes from integration over fibers. In particular it will change the degree of [[cohomology theory|cohomology theories]].

heuristically the pushforward

$$
    d RFT(X) \stackrel{p_*}{\to} d RFT(pt)
$$

acts on field theories $E_X$ over $X$ 

$$
  $E_X \mapsto E$
$$

by the assignment

$$
  E(Y^{d-1}) \mapsto 
  \Gamma\left(
  \array{
     E_X(Y)
     \\
     \downarrow
     \\
     Maps(Y,X)
  }
  regarded as a vector bundle
  \right)
$$

for instance when $E_X(Y) = \mathbb{C}$ then $E(Y) = \Gamma(Maps(Y,X))$.

For instance take $\Sigma$ to be the pair of panty with input $Y_0$ and output $Y_1$ and let $F : \Sigma \to X$ be a map.


Then $E(\Sigma)$ willy take some section $\Psi \in E(Y_0)$ to 

$$
  E(\Sigma)(\Psi) : (f_1 : Y_1 \to X)
  \mapsto
  \int_{\{F : \Sigma \to X\} | F/Y_1 = f_1} E_X(F)(\Psi(f_0))
  \frac{1}{Z}\exp(-S(F) dvol)
  \,.
$$

Here the expression $\frac{1}{Z}\exp(-S(F) dvol)$ denotes a would-be measure which is still to be defined. 

Here $f_0 = F/Y_0$ is the restriction of $F$ to $Y_0$.

Contravariant functors with push-forward also arise as part of a [[cohomology theory]] 

$$
  h^n : Diff^{op} \to Ab
$$

from the category [[Diff]] of smooth [[manifold]]s to the category [[Ab]] of abelian groups that satisfies the axioms of [[generalized (Eilenberg-Steenrod) cohomology]] theory.

These Eilenberg-Steenrod axcioms are

1. **homtopy axiom** for $h^n$

1. **Mayer-Vietoris axiom** for $h^n$

1. **suspension isomorphism** $h^n(X) \simeq h^{n+1}_{cvs}(X \times \mathbb{R})$

here in the last axiom for [[topological space]]s we'd simply have the [[suspension]] $h^{n+1}(\Sigma X)$. Here in order to stay within [[manifold]]s we instead do as indicated, where ${}_{cvs}$ means "compact vertical support".

Concerning the **homotopy axiom**: given any [[functor]] that sends manifolds to a category of [[FQFT]]s over $X$
  
  $$
    d-FTs := h : Diff^{op} \to C
  $$

  in $dRFT$s we can make it a homotopy functor by defining

  $\omega_0, \omega_1 \in h(X)$ to be [[concordance|concordant]] if $\exists \omega \in h(X \times \mathbb{R})$ such that $\omega/(X\times \{i\}) \simeq \omega_i$ in $h(X)$, $i = 0,1$

then under this relation

$$
  X \mapsto  d-RFT(X)/\simeq
$$

is a homotopy invariant functor

**Homework**: for $h(X) = \Omega^n_{closed}(X)$

we have that $\omega_0$ concordant to $\omega_1$ exactly when $\omega_0 = \omega_1 + d \alpha$ for some $\alpha \in \Omega^{n-1}(X)$

Concerning the **Mayer-Vietoris axiom**: if $X = U \cup V$ then the functor should respect this gluing.

suppose $E \in 2-RFT(X)$ is a 2d Riemmanian field theory. let $\gamma : S^1 \to X$ be a loop in $X$. then $E(\gamma)$ is a [[vector space]].

If $\gamma$ sits neither entirely in $U$ or in $V$, then there is no way that the vector space $E(\gamma)$ can be reconstructed by knowing just the restriction of $R$ to $U$ and $V$. 

So this is a **problem** for the definition of field theories so far.

The **proposed solution** (from [[What is an elliptic object?]]) is to use _extended_ [[FQFT]]s instead. This introduces **locality** into [[FQFT]]s, at the expense of working with [[n-category|n-categories]].

This will however not be studied here for the moment.

Concerning the **suspension isomorphism**: for that first we need for $n \in \mathbb{Z}$ the notion of a field theory over $X$ of **degree $n$**, ie.e

$$
  X \mapsto d-RFTs^n(X)
$$

such that for $n=0$ this is an ordiary Riemannian field theory, in $d-RFT(X)$.

This requires to replace [[manifold]]s by [[supermanifold]]s.

**Example** let $d = 0$ and consider 0-dimensional TFTs over $X$.

so consider

$$
  Fun^\otimes(0 Bord(X), TV)
$$


in $0 Bord(X)$ there is only a single [[object]]: the [[empty set]] $\emptyset$ which has a unique map $\emptyset \to X$

the collecton of morphisms is $\{finite set \to X\}$ in there is $Hom_{Diff}(pt,X)$.

here composition of morphisms is the same as tensor product of objects: both comes from the disjoint union of these finite set domains.

$$
  E : 0 Bord(X) \to TV_{\mathbb{R}}
$$

$$
  \emptyset \mapsto \mathbb{R}
$$

$$
  x \in X \mapsto E(X) \in \mathb{R}
$$

so a priori we have

$$
  Fun^\otimes(0 Bord(X), TV) \simeq Maps(X, \mathbb{R})
  \,,
$$

where on the right we have _all_ maps.

This is not quite what is intended. We want to see _smooth_ maps on the right. To get that, we need to talk about _smooth functors_ on the left. This is the topic of later discussion, which will yield 

$$
  SmoothFun^\otimes(0 Bord(X), TV) \simeq C^\infty(X, \mathbb{R})
  \,.
$$

But one other ting goes wrong the: the corresponding homotopy functor is $C^\infty(X)/\simeq = \{0\}$. So turning this into an Eilenberg-Steenrod theory yields the trivial theory.

The way out to that will be to go to [[supermanifold]]s.

**Punchline** of this session here:

$$
  (0|1)-TFTs(X)
  \simeq
  SmoothFun^\otimes((0|1)Bord(X), TV)
$$ 

and then it is a $lemma^G$ that

$$
  C^\infty(SuperDiff(\mathbb{R}^{0|1}, X))^G
  \simeq 
  \Omega^\bullet(X)^G
  = (\oplus_{n = 0}^{\infty} \Omega^n(X))^G
$$

where $G$ is the [[supergroup]] $G = Diff(\mathbb{R}^{0|1}) \wim42 \mathbb{R}^{0|1} \rtimes \mathbb{R}^\times$.

The degree decomposition on forms then turns out to be the eigenvalue decompositon of the $\mathbb{R}^\times$-part, while the deRham differential is the $\mathbb{R}^{0|1}$-action (cite Kontsevich, Severa here ...)

so then from that one finds that the $G$-invariant bit is the _closed_ 0-forms

$$
  \Omega^\bullet(X)^G
  \simeq
  \Omega^0_{closed}(X)
$$

So we get $n$-**Lemma** :

$$
  (0|1)-TFT^n(X) \simeq \Omega^n_{cl}(X)
$$

and

$$
  (0|1)-TFT^n(X)_{concord} \simeq H^n_{dR}(X)
$$

**push-forward**

Now with the super-directions included, there is a notion of push-forward of the TFTs that does shift the degree, and we get the following

**Theorem (Stolz-Teichner-Kreck-Hehnhold)**

when $X$ is oriented

$$
  (0|1)TFT^n(X) \stackrel{push}{\to} (0|1)TFT^0
  \simeq \mathbb{R}
$$

$$
  \Omega^n_{cl}(X) \stackrel{\int_{X_n}}{\to}
  \Omega^0_{cl}(pt)
  \simeq
  \mathbb{R}
$$

and similarly after dividing out concordance, the push-forward becomes the push-forward in [[deRham cohomology]].




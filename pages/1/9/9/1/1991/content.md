
+-- {: .standout}

Research material. 

=--


# Idea #

We introduce a notion [[nLab:duality|dual]] to that of [[nLab:infinity-stack|∞-stack]] -- a generalized space -- which in the sense of [[nLab:space and quantity|space and quantity]] gives the corresponding notion of generalized quantity.

This is such that if we have a [[nLab:smooth infinity-stack|smooth ∞-stack]] -- i.e. a [[nLab:Lie infinity-groupoid|Lie ∞-groupoid]] -- its $(\infty,1)$-quantity is the dual to the corresponding [[nLab:Lie infinity-algebroid|Lie ∞-algebroid]]: its [[nLab:Chevalley-Eilenberg algebra|Chevalley-Eilenberg algebra]].

For instance 

* the $(\infty,1)$-quantity of functions on the  [[path ∞-groupoid]] $\Pi(X)$ is the deRham complex of [[differential form]]s on $X$;

* the $(\infty,1)$-quantity of functions on the [[nLab:delooping|delooping]] $\mathbf{B}G$ of a [[nLab:Lie group|Lie group]] $G$ is the [[nLab:Chevalley-Eilenberg algebra|Chevalley-Eilenberg algebra]] of its [[nLab:Lie algebra|Lie algebra]].



Recall from the discussion at [[nLab:models for infinity-stack (infinity,1)-toposes|models for ∞-stack (∞,1)-toposes]] that [[simplicial presheaf|simplicial presheaves]] model generalized spaces, in the form of [[∞-groupoid]]s with extra structure (smooth structure, for instance, in the case of [[smooth ∞-stack]]s).

In the sense of [[nLab:space and quantity|space and quantity]] the [[duality|concrete dual]] notion obtained by homming into objects of the underlying [[nLab:site|site]] should be tought of as $(\infty,1)$-quantities.
This way we obtain _model for $(\infty,1)$-quantities_ in terms of a category of cosimplicial copresheaves $[C,[\Delta, Set]]\,.$

For $C =$ [[CartSp]] those copresehaves that respect [[nLab:product|product]]s in $C$ are [[nLab:generalized smooth algebra|generalized smooth algebra]]s. By the  dual [[nLab:Dold-Kan correspondence|Dold-Kan correspondence]] cosimplicial smooth algebras are equivalent to **differential graded smooth algebras** (in non-negative degree), namely [[nLab:differential graded algebra|differential graded algebra]]s in the context of [[nLab:generalized smooth algebra|generalized smooth algebra]]s. Therefore our $(\infty,1)$-quantities are also modeled by cochain complexes of copresheaves and in this incarnation they reproduce various entities familiar in [[nLab:homological algebra|homological algebra]] and [[nLab:Lie theory|Lie theory]]. 


# Definition #


+-- {: .un_defn}
###### Definition (homotopical category of $(\infty,1)$-quantities)

Let $C = $ [[CartSp]]. Write 

$$
  CoSCoSh(C) \subset [C,[\Delta,Set]]
$$

for the full [[nLab:subcategory|subcategory]] of [[nLab:simplicial object|cosimplicial]] [[presheaf|copresheaves]] on $C$ that respect [[nLab:product|product]]s. This are the [[simplicial object|cosimplicial objects]] in the category of [[generalized smooth algebra]]s.

We regard $CoSCoSh(C)$ as a [[nLab:category with weak equivalences|category with weak equivalences]] by declaring a morphism to be a weak equivalence if objectwise under the dual [[nLab:Dold-Kan correspondence|Dold-Kan correspondence]] it induces a [[nLab:quasi-isomorphism|quasi-isomorphism]] of [[nLab:cochain complex|cochain complex]]es.

=--

In more detail this means that a morphism $f : A \to B$ is a weak equivalence if for all $\mathbb{R}^n \in C$ the morphism $f(U) : A(U) \to B(U)$ of cosimplicial abelian groups (using the additive structure of [[generalized smooth algebra]]s) induces under the dual normalized [[nLab:Moore complex|Moore complex]] a morphism $N^\bullet f(U) : N^\bullet A(U) \to N^\bullet(B(U))$ that induces an isomorphism on [[nLab:chain homology and cohomology|cochain complex cohomology]].



+-- {: .un_defn}
###### Definition (quantities on an $\infty$-stack)

Recall that for $X$ a [[presheaf]] on $C$ its [[generalized smooth algebra]] is its [[dualizing object|Isbell dual]] copresheaf

$$
  C^\infty(X) : U \mapsto PSh_C(X, Y(U))
  \,,
$$ 

where $Y$ is the [[Yoneda embedding]].

This extends to a functor

$$
  C^\infty(-) : SPSh(C)  \to CoSSh(C)
$$

from simplicial presheaves to cosimplicial smooth algebras by degreewise application: for $X_\bullet \in SPSh(X)$ we have 

$$
  C^\infty(X_\bullet)^k = C^\infty(X_k)
  \,.
$$

For $X_\bullet \in SConSh(C)$ a simplicial [[concrete sheaf]] (a simplcial [[diffeological space]]) there is an obvious notion of open simplicial neighbourhood $V_\bullet \subset X_\bullet$ of the entirely degenerate simplices (those in the image of $X([k]\to [0])$). Let

$$
  C^\infty_{loc}(X_\bullet) := colim_V C^\infty(V_\bullet)
$$

be the $(\infty,1)$-quantity of _local_ functions on $X$.

=--


# Examples #

## Singular cohomology and differential forms ##

Given [[smooth space]] $X$ let $C^\infty(X^{\Delta_{inf}^k})$ be the [[generalized smooth algebra]] of functions on the space of infinitesimal $k$-[[simplex|simplices]] in $X$. This naturally forms a cosimplicial smooth algebra $C^\infty(X^{\Delta_{inf}^\bullet})$. The corresponding dual normalized [[Moore complex]] is the [[cochain complex]] of [[differential forms in synthetic differential geometry]].

Now let $\Pi(X)$ be the [[path infinity-groupoid]] of $X$. Then the Moore complex associated with the cosimplicial smooth algebra $C^\infty(\Pi(X)) := C^\infty(X^{\Delta^\bullet_C})$ is the one that computes **singular cohomology**.

By the deRham theorem (see section 4.3 of [[Models for Smooth Infinitesimal Analysis|SmoothMod]] for the synthetic version) the functor 

$$
  \int : C^\infty(X^{\Delta^\bullet_{inf}}) 
  \stackrel{\simeq}{\to}
  C^\infty(\Pi(X))
$$

that integrates differential forms over simplices is an isomorphism on the cohomologies of the corresponding [[Moore complex]]es, hence by the [[Dold-Kan correspondence]] is a weak equivalence of cosimplicial smooth algebras.


## Group cohomology and Chevalley-Eilenberg algebra of a Lie algebra ##

Let $G$ be a [[Lie group]] and let $\mathbf{B}G$ be its [[delooping]] regarded as a [[Kan complex]] valued [[simplicial presheaf]] (on [[Diff]] or [[CartSp]] or the like). The cosimplicial smooth algebra $C^\infty(\mathbf{B}G)$ has in degree $k$ the smooth algebra of $\mathbb{R}$-valued functions on $G^{\times_k}$. The differential of the corresponding dual [[Moore complex]] $N^\bullet(C^\infty(\mathbf{B}G))$ is the one that computes smooth [[group cohomology]] on $G$ with coefficients in $\mathbb{R}$ with the trivial module structure.

Let $g$ be the [[Lie algebra]] of $G$ and let $CE(g)$ denote the [[Chevalley-Eilenberg cochain complex]] that computes [[Lie algebra cohomology]] with coefficients in the corresponding trivial Lie algebra module.

There is a canonical cochain map

$$
  diff : N^\bullet(C^\infty(\mathbf{B}G)) 
  \stackrel{\simeq}{\to} CE^\bullet(g)
  \,,
$$

the vanEst morphism, that sends a function on $G^{\times k}$ to its differential at the identity. If $G$ is $k$-connected, this morphism is an isomorphism on degree $(n \leq k+1)$-cohomology. Hence the cosimplicial algebra $C^\infty(\mathbf{B}G)$ is weakly equivalent to that truncation to the (cosimplicial version of) the Chevalley-Eilenberg algebra.

Let now $C^\infty_{loc}(\mathbf{B}G) \subset C^\infty(\mathbf{B}G)$ be the cosimplicial algebra of function [[germ]]s at the totally degenerate simplices (the identity $n$-cells on the identity $(n-1)$-cells on the...).

The cohomology of the corresponding cochain complex is the _local Lie group cohomology_. It coincides with the Lie algebra cohomology. Therefore it should be true that under the cosimplicial [[Dold-Kan correspondence]] we have a weak equivalence

$$
  C^\infty_{loc}(\mathbf{B}G) \simeq CE(g)
  \,.
$$


## Lie algebra valued differential forms ##

Let $X$ be a manifold and $G$ a [[Lie group]] with [[Lie algebra]] $g$. A _flat $g$-valued differential 1-form_ $A \in \Omega^1(X,g)$ with $d A + [A \wedge A ] = 0$ is the same as

* a smooth functor 

  $$
    \Pi(X) \to \mathbf{B}G
  $$ 

  from the [[path infinity-groupoid]] to $\mathbf{B}G$ (as described at [[connection on a bundle]])

* a morphism of [[differential graded algebra]]s 

  $$
    \Omega^\bullet(X) \leftarrow CE(g)
    \,.
  $$

(The emphasis of this simple but far-reaching observation goes back to Cartan. For a detailed account of this in its wider context see for instance [LInfCon](http://arxiv.org/abs/0801.3480))

Using the above we find that the systematic relation between these two points of view is that the latter is the image under $C^\infty(-) [C^{op},[\Delta^{op}, Set]] \to [C,[\Delta, Set]]$ in that

$$
  \array{
     \Pi(X) &\stackrel{P exp(\int_{-} A)}{\to}& 
      \mathbf{B}G
     \\
     \\
     C^\infty_{loc}(\Pi(X)) &\leftarrow& 
     C^\infty_{loc}(\mathbf{B}G)
     \\
     {}^\simeq\uparrow^\int && {}^{diff}\downarrow^\simeq
     \\
     \Omega^\bullet(X)
     &\stackrel{A}{\leftarrow}&
     CE(g)
  }
$$



#Details#

##Cosimplicial objects##

For $K$ a cosimplicial object 
we shall write 

* the degree increasing maps as $d_i^* : K^n \to K^{n+1}$

* the degree lowering maps as $s_i^* : K^{n+1} \to K^n$.

The reason is that in the present context all our cosimplicial 
objects are to be thought of as some [[nLab:duality|concrete dual]]s
of simplicial objects. 

The archetypical example is the following.


##The $(\infty,1)$-quantity of functions on infinitesimal simplices ##

Let $X$ be a [[nLab:smooth space|smooth space]]. Write $C^\infty([\Delta_{inf}^k,X])$
for the [[nLab:generalized smooth algebra|generalized smooth algebra]] (a certain copresheaf on
[[nLab:CartSp|CartSp]]) that plays the role of 
the algebra of functions on the space of $k$-dimensional infinitesimal
simplices in $X$. As $k$ varies this naturally arranges itself into
a cosimplicial copresheaf 
$C^\infty([\Delta_{inf}^\bullet,X]) := C^\infty(X^{\Delta_{inf}^k})$
which we call the **$(\infty,1)$-quantity of functions on infinitesimal
simplices** in $X$.

For later reference we list in detail the interpretation of the face and degenercy maps in this cosimplicial object.

* First think of $X^{\Delta^k_{inf}} := [\Delta^k_{inf}, X]$ as the 
space of infinitesimal $k$-simplices in $X$ (formalized as such in some
context that need not concern us here).


  * The maps $\delta_i : [k] \to [k+1]$ induce the face maps

    $$
    d_i := [\delta_i, X] : X^{\Delta^{k+1}_{inf}} 
     \to X^{\Delta^{k}_{inf}}
    $$

   that send a $(k+1)$-simplex to its $i$th $k$-face.

  * The maps $\sigma_i : [k+1] \to [k]$ induce the degeneracy maps

    $$
     s_i := [\sigma_i, X] : X^{\Delta^{+1}_{inf}} 
     \to X^{\Delta^{k+1}_{inf}}
    $$

    that regard a $k$-simplex as a $(k+1)$-simplex with degenerate $i$th face.

* Accordingly, in the cosimplicial smooth algebra $C^\infty([\Delta^\bullet_{inf},X])$ of smooth algebras of functions on infinitesimal simplices 

  * we have maps

    $$
      d_i^* := C^\infty([\delta_i, X]) : C^\infty(X^{\Delta^{k}_{inf}}) \to 
     C^\infty(X^{\Delta^{k+1}_{inf}})
    $$

    that build a function on $(k+1)$-simplices from one on $k$-simplices by evaluating the latter on the $i$th faces 

  * and maps

    $$
      s_i^* := C^\infty([\sigma_i, X]) : C^\infty(X^{\Delta^{k+1}_{inf}}) \to 
     C^\infty(X^{\Delta^{k}_{inf}})
    $$

    that restrict functions on all $(k+1)$-simplices to those simplices whose $i$th face is degenerate and regard the result as a function on $k$-simplices.

## The Moore complex of an $(\infty,1)$-quantity ##

Let $K = K^\bullet$ be a cosimplicial [[nLab:generalized smooth algebra|generalized smooth algebra]]. 
Its **Moore complex** is the connective (meaning: $\mathbb{N}$-graded) 
[[nLab:cochain complex|cochain complex]] (degree of coboundary maps is $+1$) $C^\bullet(K)$ which is degreewise equal to $K$ in that $C^n(K) := K^n$ and whose coboundary map is the alternating sum
of face maps

$$
  d : \sum_{i=0}^n (-1)^i d_i^* : C^{n-1}(K) \to C^n(K)
  \,. 
$$

Its **normalized Moore complex** $N^\bullet(K)$ is the subcomplex on the joint [[nLab:kernel|kernel]] of all but the last degeneracy maps

$$
  N^n(K) = \cap_{i=0}^{n-1} ker(s_i^*)
  \,.
$$




## The Moore DGA of an $(\infty,1)$-quantity ##


Write $CoSh(CartSp)$ -- or just $CoSh$ in the present context -- for the category of product-preserving
copresheaves on [[nLab:CartSp|CartSp]] and $CoSCoSh(CartSp)$ -- or just 
$CoSCoSh$ in the present context --  for the category
of cosimplicial objects of that.

Regard $CoSh$ as a [[nLab:monoidal category|monoidal category]] using its [[nLab:coproduct|coproduct]],
which plays the role of the completed [[nLab:tensor product|tensor product]]
of [[nLab:generalized smooth algebra|generalized smooth algebra]]s. By degreewise application
this induces a monoidal structure on $CoSCoSh$

$$
  \otimes : CoSCoSh \times CoSCoSh \to CoSCoSh
$$

$$
  (K_1 \otimes K_2)^n := K_1^n \otimes K_2^n
  \,.
$$

Let also the category $Ch^\bullet_*$ of connective cochain complexes
be a [[monoidal category]] in the standard way

$$
  \otimes : Ch^\bullet_+ \times Ch^\bullet_+ \to Ch^\bullet_+
  \,.
$$


+-- {: .un_prop }
###### Proposition

There is a [[nLab:natural transformation|natural transformation]]

$$
  \mu_K : C^\infty(K) \otimes C^\infty(K) \to C^\infty(K \otimes K)
$$

natural in $K \in CoSCoSh$ with the tensor products as above
and with $C^\bullet : CoSCoSh \to Ch^\bullet_+$ the Moore complex
functor which satisfies uniticity and associativity in the obvious way
that makes it the component of a lax monoidal functor (or something close).

=--


+-- {: .proof}
###### Proof

On homogeneous elements $a \otimes b \in C^p(K) \otimes C^q(K)
 \subset 
 (C(K) \otimes C(K))
 = \oplus_{p+q = n} C^p(K) \otimes C^q(K)$ with $a \in C^p(K) = K^p$ and
$b \in C^q(K) = K^q$ define the cochain map $\mu_K$ by 

$$
  \mu_K(a \otimes b) :=
  \sum_{(\mu,\nu)} sign(\mu,\nu) (d_\mu^* a) \otimes (d_\nu^* b) \in
  C^{p+q}(K \otimes K) = K^{p+q} \otimes K^{p+q}
$$ 

where

* the sum is over all pairs of morphisms $\delta_\mu : [p] \to [p+q]$
and $\delta_\nu : [q] \to [p+q]$ of ordered sets such that their [[fiber product]] is
a singleton

* the map $d_\mu^* := K(\delta_\mu) : K^p \to K^{p+q}$ is the induced one,
similarly for $d_\nu^*$;

* the expression $sign(\mu,\nu)$ is the signature of the obvious permutation.

Then check... (haven't yet in full detail, maybe this needs a bit of tweaking, but should be right essentially).

=--



This induces on the Moore cochain complex $C^\bullet(K)$ 
of a cosimplicial smooth algebra $K \in CoSCoSh$ the structure of a
[[nLab:monoid|monoid]] in $Ch^\bullet_+$, hence of a connective [[nLab:differential graded algebra|differential graded algebra]]
with product given by

$$
  C^\bullet(K) \otimes C^\bullet(K)
  \stackrel{\mu_K}{\to}
  C^\bullet(K \otimes K)
  \stackrel{C^\bullet(\cdot)}{\to}
  C^\bullet(K)
$$

with $\cdot : K \otimes K \to K$ degreewise the product 
$\cdot : K^n \times K^n \to K^n$ in the [[nLab:generalized smooth algebra|generalized smooth algebra]]
$K^n$.

The (normalized) [[nLab:Moore complex|Moore complex]] $C^\bullet(K)$ (or $N^\bullet(K)$) 
of an $(\infty,1)$-quantity $K \in CoSCoSh$
equipped with this monoidal structure
we call the (normalized) **Moore [[nLab:differential graded algebra|differential graded algebra]]**
-- or **Moore DGA** for short -- of $K$.


+-- {: .un_prop }
###### Proposition

Let $X$ be a smooth manifold.

The normalized Moore DGA  of the $(\infty,1)$-quantity $C^\infty([\Delta_{inf}^\bullet,X])$ 
of functions on infinitesimal simplices in $X$ is isomorphic, as 
a [[nLab:differential graded algebra|differential graded algebra]] to the deRham DGA
of [[nLab:differential form|differential forms]] on $X$.

$$
  \Omega^\bullet(X) \simeq N^\bullet(C^\infty([\Delta_{inf}^\bullet,X]))
$$

=--


+-- {: .proof}
###### Proof

Unwrapping what this means it reduces item per item to
the characterization of differential forms as functions on
infinitesimal simplices as given by [[Anders Kock]]. See [[nLab:differential forms in synthetic differential geometry|differential forms in synthetic differential geometry]].

=--



[[!redirects (infinity,1) quantity]]
[[!redirects (∞,1)-quantity]]
[[!redirects (∞,1) quantity]]
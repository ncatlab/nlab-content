+-- {: .standout}

Research material. 

=--


# Idea #

We introduce a notion [[duality|dual]] to that of [[infinity-stack|∞-stack]] -- a generalized space -- which in the sense of [[space and quantity|space and quantity]] gives the corresponding notion of generalized quantity.

This is such that if we have a [[smooth infinity-stack|smooth ∞-stack]] -- i.e. a [[Lie infinity-groupoid|Lie ∞-groupoid]] -- its $(\infty,1)$-quantity is the dual to the corresponding [[Lie infinity-algebroid|Lie ∞-algebroid]]: its [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg algebra]].

For instance 

* the $(\infty,1)$-quantity of functions on the  [[path ∞-groupoid]] $\Pi(X)$ is the deRham complex of [[differential form]]s on $X$;

* the $(\infty,1)$-quantity of functions on the [[delooping|delooping]] $\mathbf{B}G$ of a [[Lie group|Lie group]] $G$ is the [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg algebra]] of its [[Lie algebra|Lie algebra]].



Recall from the discussion at [[models for infinity-stack (infinity,1)-toposes|models for ∞-stack (∞,1)-toposes]] that [[simplicial presheaf|simplicial presheaves]] model generalized spaces, in the form of [[∞-groupoid]]s with extra structure (smooth structure, for instance, in the case of [[smooth ∞-stack]]s).

In the sense of [[space and quantity|space and quantity]] the [[duality|concrete dual]] notion obtained by homming into objects of the underlying [[site|site]] should be tought of as $(\infty,1)$-quantities.
This way we obtain _model for $(\infty,1)$-quantities_ in terms of a category of cosimplicial copresheaves $[C,[\Delta, Set]]\,.$

For $C =$ [[CartSp]] those copresehaves that respect [[product|product]]s in $C$ are [[generalized smooth algebra|generalized smooth algebra]]s. By the  dual [[Dold-Kan correspondence|Dold-Kan correspondence]] cosimplicial smooth algebras are equivalent to **differential graded smooth algebras** (in non-negative degree), namely [[differential graded algebra|differential graded algebra]]s in the context of [[generalized smooth algebra|generalized smooth algebra]]s. Therefore our $(\infty,1)$-quantities are also modeled by cochain complexes of copresheaves and in this incarnation they reproduce various entities familiar in [[homological algebra|homological algebra]] and [[Lie theory|Lie theory]]. 


# Definition #


+-- {: .un_defn}
###### Definition (homotopical category of $(\infty,1)$-quantities)

Let $C = $ [[CartSp]]. Write 

$$
  CoSCoSh(C) \subset [C,[\Delta,Set]]
$$

for the full [[subcategory|subcategory]] of [[simplicial object|cosimplicial]] [[presheaf|copresheaves]] on $C$ that respect [[product|product]]s. This are the [[simplicial object|cosimplicial objects]] in the category of [[generalized smooth algebra]]s.

We regard $CoSCoSh(C)$ as a [[category with weak equivalences|category with weak equivalences]] by declaring a morphism to be a weak equivalence if objectwise under the dual [[Dold-Kan correspondence|Dold-Kan correspondence]] it induces a [[quasi-isomorphism|quasi-isomorphism]] of [[cochain complex|cochain complex]]es.

=--

In more detail this means that a morphism $f : A \to B$ is a weak equivalence if for all $\mathbb{R}^n \in C$ the morphism $f(U) : A(U) \to B(U)$ of cosimplicial abelian groups (using the additive structure of [[generalized smooth algebra]]s) induces under the dual normalized [[Moore complex|Moore complex]] a morphism $N^\bullet f(U) : N^\bullet A(U) \to N^\bullet(B(U))$ that induces an isomorphism on [[chain homology and cohomology|cochain complex cohomology]].



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
     {}^\simeq\downarrow^{diff} 
     && {}^{diff}\downarrow^\simeq
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
objects are to be thought of as some [[duality|concrete dual]]s
of simplicial objects. 

The archetypical example is the following.


##The $(\infty,1)$-quantity of functions on infinitesimal simplices ##

Let $X$ be a [[smooth space|smooth space]]. Write $C^\infty([\Delta_{inf}^k,X])$
for the [[generalized smooth algebra|generalized smooth algebra]] (a certain copresheaf on
[[CartSp|CartSp]]) that plays the role of 
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

Let $K = K^\bullet$ be a cosimplicial [[generalized smooth algebra|generalized smooth algebra]]. 
Its **Moore complex** is the connective (meaning: $\mathbb{N}$-graded) 
[[cochain complex|cochain complex]] (degree of coboundary maps is $+1$) $C^\bullet(K)$ which is degreewise equal to $K$ in that $C^n(K) := K^n$ and whose coboundary map is the alternating sum
of face maps

$$
  d : \sum_{i=0}^n (-1)^i d_i^* : C^{n-1}(K) \to C^n(K)
  \,. 
$$

Its **normalized Moore complex** $N^\bullet(K)$ is the subcomplex on the joint [[kernel|kernel]] of all but the last degeneracy maps

$$
  N^n(K) = \cap_{i=0}^{n-1} ker(s_i^*)
  \,.
$$




## The differential graded algebra of an $(\infty,1)$-quantity ##


Write $CoSh(CartSp)$ -- or just $CoSh$ in the present context -- for the category of product-preserving
copresheaves on [[CartSp|CartSp]] and $CoSCoSh(CartSp)$ -- or just 
$CoSCoSh$ in the present context --  for the category
of cosimplicial objects of that.

Regard $CoSh$ as a [[monoidal category|monoidal category]] using its [[coproduct|coproduct]],
which plays the role of the completed [[tensor product|tensor product]]
of [[generalized smooth algebra|generalized smooth algebra]]s. By degreewise application
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

For $K \in CoSCoSh$ a cosimplicial algebra, there is on its [[Moore complex|Moore cochain complex]] $C^\bullet(K)$ the structure of a [[monoid]] (hence of a [[differential graded algebra]])

$$
  \mu_K : C^\bullet(K) \otimes C^\bullet(K) \to C^\bullet(K)
$$

such that for $K = A$ a cosimplicial object constant on an algebra $A$ this product on $C^\bullet(A) = A$ reproduces that on $A$.

=--


+-- {: .proof}
###### Proof

We define the map $\mu_K$ and check that it has all the right properties.

First introduce some notation to handle this combinatorial problem.

For $p \in \mathbb{N}$ we write, as usual $[p] = \{0 \lt 1 \lt \cdots \lt p\}$ for the totally ordered set with $p+1$-elements.

When the codomain is understood, we denote an order-preserving injective map $\delta_\mu : [p] \to [p+q]$ by the string $\mu = (\mu_0, \mu_1, \cdots, \mu_p)$ of its values, so that $\delta_\mu : i \mapsto \mu_i$.

We write $(\mu_0, \cdots,\hat \mu_i, \cdots, \mu_p)$ for the string obtained from $(\mu_0, \mu_1, \cdots, \mu_p)$ by _omitting_ the $i$th entry.

At the same time, with domain and codomain understood, we still write $\delta_i : [p] \to [p+1]$ for the standard (dual) face map that leaves out the $i$th value. 

Observe that with this notation we have 

$$
  \delta_{\mu} \circ \delta_i
  =
  \delta_{(\mu_0, \cdots, \hat \mu_i, \cdots, \mu_p)}
$$

and

$$
  \delta_i \circ \delta_\mu
  =
  \delta_{\mu_0, \cdots, \mu_{k-1}, (\mu_k)+1, \cdots (\mu_p) + 1}
  \,,
$$

where $\mu_k$ is the lowest of the $\mu_\cdot$ greater or equal to $i$.

For $K$ any cosimplicial object we write

$$
  d_\mu^* : K^p \to K^{p+q}
$$ 

for the image of $\delta_\mu$ under $K$.

A pair two order preserving injective maps $\delta_\mu : [p] \to [p+q]$ and $\delta_\nu : [q] \to [p+q]$ that have precisely one point in their images in common, i.e. such that their [[pullback]] is

$$
  \array{
    [0] &\to& [p]
    \\
    \downarrow && \downarrow^{\delta_\mu}
    \\
    [q] &\stackrel{\delta_\nu}{\to}& [p+q]
  }
$$

we call in the following an **overlapping partition** of $[p+q]$. We also write $(\mu,\nu)_{[p+q]}$ or $(\mu_0,\cdots,\mu_p,\nu_0, \cdots, \nu_q)_{[p+q]}$ for this overlapping partition.

To each overlapping partition of $[p+q]$ we assign a sign $sgn(\mu,\nu) \in \{-1,+1\}$ given by

$$
  sgn(\mu,\nu)_{[p+q]}
  =
  \prod_{i=0}^p (-1)^{\mu_i -i}
  \,.
$$

This is the same as 

$$
  \cdots =
  \prod_{i=0}^q (-1)^{\nu_i - (p+i)}
  \,.
$$


With that notation understood, now define the cochain map

$$
  \mu_K
  : 
  C^\bullet(K) \otimes C^\bullet(L)
  \to 
  C^\bullet(K \otimes L)
  \,.
$$ 

by defining it on homogeneous elements 

$$
 a \otimes b \in C^p(K) \otimes C^q(L)
  \subset 
 (C(K) \otimes C(K))
 = \oplus_{p+q = n} C^p(K) \otimes C^q(K)
$$ 

with $a \in C^p(K) = K^p$ and
$b \in C^q(K) = K^q$  by the formula

+-- {: .standout}



$$
  \mu_{K}
   : a \otimes b
   \;\;\mapsto\;\;
  \sum_{(\mu,\nu)_{[p+q]}} 
   sgn(\mu,\nu)_{[p+q]} \;\;(d_\mu^* a) \;\cdot\; (d_\nu^* b) 
  \;\;\;\;\;\;\in
  C^{p+q}(K) 
  \,.
$$ 

=--


To amplify again: here on the left we see a homogenoeus element in a tensor product $\otimes$, whereas on the right we see the product $-\cdot- : K^{p+q} \otimes K^{p+q} \to K^{p+q}$ in the algebra $K^{p+q}$.

Now we check that this definition has all the right properties.

* **it is indeed a cochain map**

  We need to check that $\mu_K$ respects the differential

  $$
    d = \sum_i (-1)^i d_i^*
  $$

  that is given by the alternating sum over dual face maps.

  This means that for all $a,b$ as above the two maps

  $$
    \array{
      d(a \otimes b)
      =
      (d a)_{p+1}\otimes b_q +(-1)^p a_{p} \otimes (d b)_{q+1}
      &\stackrel{\mu_K}{\mapsto}&
       \sum_{i=0}^{p+1}
       \sum_{(\mu,\nu)_{[(p+1)+q]}}
        sgn(\mu,\nu)_{[(p+1)+q]}
        (-1)^i
        (d_\mu^* d_i^* a) \cdot (d_\nu^* b)
        +
        \sum_{i=0}^{q+1}
        \sum_{(\mu,\nu)_{[p+(q+1)]}}
        sgn(\mu,\nu)_{[p+(q+1)]}
        (-1)^p 
        (-1)^i
        (d_\mu^* a) \cdot (d_\nu^* d_i^* b)
      \\
      \uparrow^{d}
      \\
      a_p \otimes b_q
    }
  $$

  and
  
  $$
    \array{
      &&
      \sum_{i=0}^{p+q+1}
      \sum_{(\mu,\nu)_{[p+q]}} 
      sgn(\mu\nu)_{[p+q]}
      (-1)^i
       (d_i^* d_\mu^* a) \cdot (d_i^* d_\nu^* b)
      \\
      && \uparrow^{d}
      \\
      a_p \otimes b_q
      &\stackrel{\mu_K}{\mapsto}&
      \sum_{(\mu,\nu)_{[p+q]}} 
      sgn(\mu\nu)_{[p+q]}
       (d_\mu^* a) \cdot (d_\nu^* b)
    }
  $$

  have to coincide. 

  By the above observation on face map yoga the first result equals

  $$
    \mu_K(d (a\otimes b)) =
        \sum_{i=0}^{p+1}      
       \sum_{(\mu_0,\cdots,\hat\mu_i, \cdots,\mu_{p+1},\nu_0,\cdots,\nu_{q})}
        sgn(\mu,\nu)_{[(p+1)+q]}
        (-1)^i
        \;\;
        (d_\mu^* a) \cdot (d_\nu^* b)
        +
        \sum_{j=0}^{q+1}
       \sum_{(\mu_0,\cdots,\mu_{p},\nu_0,\cdots,\hat \nu_j, \cdots,\nu_{q+1})}
        sgn(\mu,\nu)_{[p+(q+1)]}
        (-1)^{p+j}
        \;\;
        (d_\mu^* a) \cdot (d_\nu^* b)
  $$

  whereas the second is

  $$
    d(\mu_K(a\otimes b))
    =
      \sum_{i=0}^{p+q+1} \sum_{(\mu_0,\cdots,\mu_{(k(i)-1)},(\mu_{k(i)})+1,\cdots,(\mu_p)+1,\nu_0,\cdots,\nu_{(l(i)-1)},(\nu_{l(i)})+1,\cdots, (\nu_q)+1)} 
      (-1)^i
      sgn(\mu,\nu)_{[p+q]}
      \;\;
       (d_\mu^* a) \cdot (d_\nu^* b)
  $$

  Here in the last sum $\mu_{k(i)}$ and $\nu_{l(i)}$ are defined to be those elements in $\mu$ and $\nu$ that are the smallest ones greater or equal to $i$

  Observe that the sums in the two expressions are _almost_ over the same configurations: 

  * in the second expression the sum is over all overlapping partitions of the ordered sets obtained from $[p+q+1]$ by removing the $i$th element. 

  * in the first expression the nature of the sum depends on which elements get removed, indicated by $\hat \mu_i$ and $\hat \nu_i$:

    * if the element $\mu_i$ or $\nu_i$ that is removed is _not_ the unique one that coincides with one of the $\nu_\cdot$s or $\mu_\cdot$, respectively, then the remaining sum is also a sum over overlapping partitions of sets obtained from $[p+q+1]$ by removing one element, namely the element $\mu_i$ or the element $\nu_i$, respectively. So this piece of the sum is as the one in the secodn expression.

    * if the element $\mu_i$ or $\nu_i$ that is removed however happens to be the one that is part of the overlap of the overlapping partition, then the remaining sum is over all _ordinary shuffles_. This holds both for the first as well as for the second big sum in the first expression. 

  So this means that for the equality to hold, the two pieces of the sums of the first expression where one of the overlapping indices is removed have to cancel each other. 

  To see this, notice that for $\mu_i$ in the overlap, the ordinary shuffle $(\mu_0, \cdots, \hat \mu_i, \cdots, \mu_{p+1}, \nu_0,\cdots, \nu_q)$ has signature that differs from $sgn(\mu,\nu)_{[p+q+1]}$ by the factor $(-1)^{(\mu_i-i)+(p+1-i)}$.

  Similarly, the ordinary shuffle $(\mu_0,\cdots, \mu_p,\nu_0, \cdots, \hat \nu_j, \cdots, \nu_{q+1})$ has signature that differs from $sgn(\mu,\nu)_{[p+q+1]}$ by the factor $(-1)^{\nu_j - (j+p) + j}$.


=--

+-- {: .standout}

...Not done yet...

=--



The (normalized) [[Moore complex|Moore complex]] $C^\bullet(K)$ (or $N^\bullet(K)$) 
of an $(\infty,1)$-quantity $K \in CoSCoSh$
equipped with this monoidal structure
we call the (normalized) **Moore [[differential graded algebra|differential graded algebra]]**
-- or **Moore DGA** for short -- of $K$.


+-- {: .un_prop }
###### Proposition

Let $X$ be a smooth manifold.

The normalized Moore DGA  of the $(\infty,1)$-quantity $C^\infty([\Delta_{inf}^\bullet,X])$ 
of functions on infinitesimal simplices in $X$ is isomorphic, as 
a [[differential graded algebra|differential graded algebra]] to the deRham DGA
of [[differential form|differential forms]] on $X$.

$$
  \Omega^\bullet(X) \simeq N^\bullet(C^\infty([\Delta_{inf}^\bullet,X]))
$$

=--


+-- {: .proof}
###### Proof

Unwrapping what this means it reduces item per item to
the characterization of differential forms as functions on
infinitesimal simplices as given by [[Anders Kock]]. See [[differential forms in synthetic differential geometry|differential forms in synthetic differential geometry]].

=--



[[!redirects (infinity,1) quantity]]
[[!redirects (∞,1)-quantity]]
[[!redirects (∞,1) quantity]]
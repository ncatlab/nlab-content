[[!redirects (infinity,1)-quantity]]
+-- {: .standout}

Research material. 

=--


# Idea #

+-- {: .standout}

In the sense of [[space and quantity]] a quantity is a [[presheaf|co-presheaf]].

The notion of $\infty$-quantity is the [[vertical categorification|∞-categorification]] of this.

So $\infty$-quantities are [[duality|dual]] to [[∞-space]]s.

=--

# Contents #

1. [Background and motivation](#background)

1. [Definition](#definition)

1. [The differential graded algebra of an $\infty$-quantity](#DGA)


1. [Examples](#examples)

   1. [singular cohomology](#singluarcohomology)

   1. [Lie group cohomology](#Liegroupcohomology)

   1. [differential forms](#differentialforms)

   1. [Chevalley-Eilenberg algebra of Lie ∞-algebroids](#CEalgebra)

   1. [Lie ∞-algebroid valued differential forms ](#Lievaluedddifferentialforms)

1. [References](#references)

#Background and motivation {#background}

The [[vertical categorification|categorification]] of the notion of _space_ is that o _[[∞-space]]_ -- a [[higher category theory|higher categorical]] presheaf usually called an [[infinity-stack|∞-stack]]. These may be [[model structure on simplicial presheaves|modeled]] by [[simplicial presheaf|simplicial presheaves]].

Here we discuss the notion [[duality|dual]] to the notion $\infty$-space/$\infty$-stack/simplicial presheaf in the sense of [[space and quantity]]: that of _$\infty$-quantity_ .

This is such that for instance in the smooth context of [[smooth infinity-stack|smooth ∞-stack]] -- i.e. a [[Lie infinity-groupoid|Lie ∞-groupoid]] -- the $\infty$-quantity $C^\infty(A)$ dual to a [[Lie infinity-groupoid|Lie ∞-groupoid]] $A$ is the cosimplicial algebra of smooth functions on neighbourhoods of identities in $A$ which turns out to be the [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg algebra]] of the corresponding  [[Lie infinity-algebroid|Lie ∞-algebroid]]. 

For instance 

* the $\infty$-quantity of functions on the  [[path ∞-groupoid]] $\Pi(X)$ is the [[deRham complex]] of [[differential form]]s on $X$;

* the $\infty$-quantity of functions on the [[delooping|delooping]] $\mathbf{B}G$ of a [[Lie group|Lie group]] $G$ is the [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg algebra]] of its [[Lie algebra|Lie algebra]].



Recall from the discussion at [[models for infinity-stack (infinity,1)-toposes|models for ∞-stack (∞,1)-toposes]] that [[simplicial presheaf|simplicial presheaves]] model generalized spaces, in the form of [[∞-groupoid]]s with extra structure (smooth structure, for instance, in the case of [[smooth ∞-stack]]s).

In the sense of [[space and quantity|space and quantity]] the [[duality|concrete dual]] notion obtained by homming into objects of the underlying [[site|site]] should be tought of as $(\infty,1)$-quantities.
This way we obtain _model for $(\infty,1)$-quantities_ in terms of a category of cosimplicial copresheaves $[C,[\Delta, Set]]\,.$

For $C =$ [[CartSp]] those copresehaves that respect [[product|product]]s in $C$ are [[generalized smooth algebra|generalized smooth algebra]]s. By the  dual [[Dold-Kan correspondence|Dold-Kan correspondence]] cosimplicial smooth algebras are equivalent to **differential graded smooth algebras** (in non-negative degree), namely [[differential graded algebra|differential graded algebra]]s in the context of [[generalized smooth algebra|generalized smooth algebra]]s. Therefore our $(\infty,1)$-quantities are also modeled by cochain complexes of copresheaves and in this incarnation they reproduce various entities familiar in [[homological algebra|homological algebra]] and [[Lie theory|Lie theory]]. 


# Definition {#definition}

Let $C$ be a [[site]] with [[product]]s. 

We model $\infty$-quantities on $C$ the way [[simplicial presheaf|simplicial presheaves]] on $C$ are [[models for ∞-stack (∞,1)-toposes|models for ∞-space (∞,1)-toposes]]. 

A special case of particular interest to keep in mind is the choice $C = $ [[CartSp]].  For that choice of test spaces we have that

* [[∞-space]]s modeled on $C$ are [[Lie ∞-groupoid]]s

* quantities (1-quantities) modeled on $C$ are [[generalized smooth algebra]]s;

* $\infty$-quantities modeled on $C$ include examples such as smooth [[singular cohomology]] and [[Lie ∞-algebroid]]s.

+-- {: .un_defn}
###### Definition (1-quantitiies and cosheaves)

We shall write $CoSh(C) \subset CoPSh(C) := [C,Set]$ for the full [[subcategory]] of that on those [[presheaf|co-presheaves]] $A$ on $C$ that satisfy the "co-sheaf" condition that for all there is an [[isomorphism]]

$$
  A(U \times V) \stackrel{\simeq}{\to} A(U) \times A(V)
$$ 

[[natural transformation|natural]] in $U,V$.

=--

+-- {: .un_remark}
###### Remark (smooth $\infty$-algebras)

For $C = $ [[CartSp]] the cosheaves on $C$ are the [[generalized smooth algebra]]s

$$
  CoSh(CartSp) \simeq C^\infty Alg
  \,.
$$

=--

+-- {: .un_remark}
###### Remark (cosimplicial notation)


For $K$ a cosimplicial object  we shall write 

* the degree increasing maps as $d_i : K^n \to K^{n+1}$

* the degree lowering maps as $s_i : K^{n+1} \to K^n$.

=--


+-- {: .un_defn}
###### Definition (homotopical category of $\infty$-quantities)


$$
  CoSCoSh(C) = [\Delta,CoSh(C)] \subset [C,[\Delta,Set]]
$$

for the category of **cosimplicial cosheaves** on $C$, the [[simplicial object|cosimplicial objects]] in the category of cosheaves.

We regard $CoSCoSh(C)$ as a [[category with weak equivalences|category with weak equivalences]] by declaring a morphism to be a weak equivalence if it induces an [[isomorphism]] on [[cohomotopy]] groups. (...explain...)

=--

+-- {: .un_remark}
###### Remark (model structure on cosimplicial algebras)

For $C = $ [[CartSp]] the condition on weak equivalences above becomes under the [[Dold-Kan correspondence]] the condition that a morphism is a weak equivalence precisely if under the [[Moore complex|Moore cochain complex]] functor it induces an isomorphism on [[chain homology and cohomology|cochain cohomology]].

Moreover, in this case the forgetful functor from [[generalized smooth algebra]]s to ordinary algebras sends $CoSCoSh(C)$ to the category $[\Delta,Algebras]$ of cosimplicial algebras. There is a standard [[model category]] structure on these, with the weak equivalences as above, and the fibrations the objectwise surjections. See definition 9.1 of

* Castiglioni, Corti&#241;as, _Cosimplicial versus DG-rings_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0306/0306289v3.pdf))

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



# The differential graded algebra of an $\infty$-quantity {#DGA}

Let $C = $ [[CartSp]], so that an $\infty$-quantity modeled on $C$ is a [[generalized smooth algebra]]. 

As described at [[monoidal Dold-Kan correspondence]], the [[Moore complex|Moore cochain complex]] $C(K)$ of a cosimplicial algebra $K$ is a [[differential graded algebra]], whose product is the [[cup product]]

$$
  \cup
  :
  C^\bullet(K)\otimes C^\bullet(K)
  \to 
  C^\bullet(K)
  \,.
$$

We call $C(K)$ the [[differential graded algebra]] given by the $\infty$-quantity $K$.




# Examples {#examples}


## Singular cohomology {#singluarcohomology}


Let $C = $ [[CartSp]].

Let $\Pi(X)$ be the [[Lie ∞-groupoid]] that is the [[path ∞-groupoid]] of $X$. The [[Moore complex|Moore cochain complex]] assoctated with the $\infty$-quantity $C^\infty(\Pi(X)) := C^\infty(X^{\Delta^\bullet_C})$ of functions on $\Pi(X)$ is manifestly the one that computes [[singular cohomology]] (with values in $\mathbb{R}$).

The monoidal structure induced in $C^\infty(\Pi(X))$ under the [[monoidal Dold-Kan correspondence]] is manifestly the ordinary [[cup product]] on [[singular cohomology]].




## Lie group cohomology {#Liegroupcohomology}

Let $G$ be a [[Lie group]] and let $\mathbf{B}G$ be its [[delooping]] regarded as a [[Kan complex]] valued [[simplicial presheaf]] (on [[Diff]] or [[CartSp]] or the like). The cosimplicial smooth algebra $C^\infty(\mathbf{B}G)$ has in degree $k$ the smooth algebra of $\mathbb{R}$-valued functions on $G^{\times_k}$. The differential of the corresponding dual [[Moore complex]] $N^\bullet(C^\infty(\mathbf{B}G))$ is the one that computes smooth [[group cohomology]] on $G$ with coefficients in $\mathbb{R}$ with the trivial module structure.


## Differential forms {#differentialforms}


Consider again the example of [[singular cohomology]] of a [[smooth space]] $X$ above. In the sense of [[synthetic differential geometry]] we have a natural restriction map

$$
  C^\infty(X^{\Delta^k}) \to C^\infty(X^{\Delta^k_{inf}})
$$

from functions on simplices in $X$ to functions on infinitesimal simplices. (This is an operation on [[generalized smooth algebra]]s alone, really, which _defines_ in turn what one means by infinitesimal simplices. ), i.e. from functions on the full [[path infinity-groupoid]] to functions on just the [[infinitesimal singular simplicial complex]] of $X$.

The cosimplicial copresheaf $C^\infty(X^{\Delta^\bullet_{inf}})$ we call the **$\infty$-quantity of functions on infinitesimal simplices** in $X$.

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


+-- {: .un_prop }
###### Proposition

Let $X$ be a smooth manifold.

The normalized Moore DGA  of the $\infty$-quantity $C^\infty([\Delta_{inf}^\bullet,X])$ 
of functions on infinitesimal simplices in $X$ is isomorphic, as 
a [[differential graded algebra]] to the differential algebra
of [[differential form|differential forms]] on $X$.

$$
  \Omega^\bullet(X) \simeq N^\bullet(C^\infty([\Delta_{inf}^\bullet,X]))
$$

=--


+-- {: .proof}
###### Proof

Unwrapping what this means in detail, it turns out that this is item-per-item the characterization of differential forms as functions on infinitesimal simplices as given by [[Anders Kock]] in his work on [[synthetic differential geometry]]. See [[differential forms in synthetic differential geometry|differential forms in synthetic differential geometry]].

Anders Kock's crucial insight in this context has been that the description of differential forms simplifies notably when considering them in terms of functions on infinitesimal simplices. He noticed that

* plain functions on infinitesimal simplices are _automatically_ alternating if they have the property that they vanish on degenaret simplices and hence are isomorphic to differential forms;

* the coboundary operator on differential forms is given by the expression that defines the diferential of the Moore cochain complex on functions on simplices;

* the ordinary [[cup product]] on such functions on infinitesimal simplicies is already the [[wedge product]] on the [[differential form]]s represented by them.

But notice that

* those functions on infinitesimal simplices that vanish on degenerate simplices are precisely those that are in the joint kernel of the degeneracy maps of the cosimplicial ring $C^\infty(X^{\Delta^\bullet_{inf}})$. Therefore these are precisely the elements of the _normalized_ Moore complex $N^\bullet(C^\infty(X^{\Delta^\bullet_{inf}}))$ of $C^\infty(X^{\Delta^\bullet_{inf}})$;

* the induced monoidal structure on the Moore complex is, by the above, precisely the cup product.

The relevant theorems by Anders Kock are found here:

the identification of the deRham complex as functions on infinitesimal simplices that vanish on degenerate simplices is theorem 18.3 in

* Anders Kock, _Synthetic differential geometry_ ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

That the coboundary operator on such simplicial differential forms is precisely the differential in the Moore cochain complex is around equation (3.2.1) in 

* Anders Kock, _Synthetic Geometry of Manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf)) 

That the wedge product on differential forms is then just the [[cup product]] of these functions on infinitesimal simplices is in section 3.5 of that book.

=--




## Chevalley-Eilenberg algebra {#CEalgebra}

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


## Lie algebra valued differential forms {#Lievaluedddifferentialforms}

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


# References {#references}

At least for algebraic groups the statement that the [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg complex]] of a [[Lie algebra]] is the [[Moore complex|normalized Moore cochain complex]] of the cosimplicial algebra of functions on neighbourhoods of the identity in $\mathbf{B}G$ is well known. One reference where this is recalled is 

* Anette Huber, Guido Kings, _A $p$-adic analogue of the Borel regulator and the Block-Kato exponential map_ ([pdf](http://www.math.uni-leipzig.de/~huber/preprints/lazard.pdf))

The analog of the map of cosimplicial rings that above is called $C^\infty(\mathbf{B}G) \to C^\infty_{loc}(\mathbf{B}G)$ is in Lemma 3.4.2 there. The normalized Moore cochain complex $N^\bullet(C^\infty(\mathbf{B}G)_{loc})$ of a cosimplicial ring is in definition 3.4.3 and then the isomorphism with the [[Chevalley-Eilenberg algebra]] $N^\bullet(C^\infty(\mathbf{B}G)) \simew CE(Lie(G))$ is prop. 3.4.4.


[[!redirects (infinity,1)-quantity]]
[[!redirects (∞,1)-quantity]]

[[!redirects ∞-quantity]]
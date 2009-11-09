

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

In ordinary [[category theory]] the [[Yoneda extension]] of a [[functor]] $F : C \to D$ is its left [[Kan extension]] through the [[Yoneda embedding]] of its domain to a functor $\hat F : PSh(C) \to D$.

In [[higher category theory]] there should be a corresponding version of this construction.

In particular with categories replaced by [[(∞,1)-category|(∞,1)-catgeories]] there should be a version with the category of [[presheaf|presheaves]] replaced by a [[(∞,1)-category of (∞,1)-presheaves]], corresponding to the [[Yoneda lemma for (∞,1)-categories]].

This in turn should have a [[presentable (infinity,1)-category|presentation]] in terms of the global [[model structure on simplicial presheaves]].


## Statement ##

+-- {: .standout}

  [[Urs Schreiber]]: this here is something I thought about. Check. Even to the extent that this is right, it is clearly not yet a full answer, but at best a step in the right direction.

=--


Let $C$ be a [[category]] and write $[C^{op}, SSet]_{proj} = SPSh(C)_{proj}$ for the projective [[nLab:model structure on simplicial presheaves|model structure on simplicial presheaves]] on $C$. Let $\mathbf{D}$ be  any [[combinatorial simplicial model category]].


+-- {: .un_proposition }
###### Proposition

If $F$ takes values in cofibrant objects of $\mathbf{D}$ then the [[SSet]]-[[enriched category theory|enriched]] [[Yoneda extension]] $\hat F$ of $F$ is the [[nLab:left adjoint|left adjoint]] part of an [[SSet]]-[[Quillen adjunction]] 

$$
   \hat F : SPSh(C)_{proj}
   \stackrel{\leftarrow}{\to}
   \mathbf{D}
   :
   R
   \,.
$$


=--

Accordingly, if $F$ does not take values in cofibrant objects but where a cofibrant replacement functor $Q : \mathbf{D} \to \mathbf{D}$ is given, the [[Yoneda extension]] $\widehat{Q F}$ of $Q F$ is an $(\infty,1)$-extension up to weak equivalence of $F$.


### Proof ###


We prove this in two steps.


+-- {: .num_lemma}
###### Lemma

The [[Yoneda extension]] $F : SPSh(C)_{proj} \to \mathbf{D}$ preserves cofibrations and acyclic cofibrations.

=--

+-- {: .proof}
###### Proof 

Recall that the [[Yoneda extension]] of $F : SPSh(C)_{proj} \to \mathbf{D}$ is given by the [[nLab:coend|coend]] formula

$$
  \hat F : X \mapsto \int^{U \in C} F(U) \cdot X(U)
  \,,
$$

where in the integrand we have the [[copower|tensoring]] of the object $F(U) \in \mathbf{D}$ by the [[simplicial set]] $X(U)$.

The lemma now rests on the fact that this [[coend]] over the [[copower|tensor]]

$$
  \int (-)\cdot (-) 
   : 
     [C,\mathbf{D}]_{inj}
     \cdot
     [C^{op}, SSet]_{proj}
   \to
   \mathbf{D}
$$

is a [[Quillen bifunctor]] using the injective and projective [[global model structure on functors]] as indicated. This is [[Higher Topos Theory|HTT prop. A.2.9.26 & rmk. A.2.9.27]] and recalled at [[Quillen bifunctor]].

Since by assumption $F(U)$ is cofibrant for all $U$ we have that $\hat F$ itself is cofibrant regarded as an object of $[C,\mathbf{D}]_{inj}$. From the definition of [[Quillen bifunctor]]s it follows that

$$
  \hat F = \int^U F(U) \cdot (-)(U) : SPSh(C)_{proj} \to \mathbf{D}
$$

preserves cofibrations and acyclic cofibrations. 

=--


+-- {: .un_lemma }
###### Lemma 

The functor $\hat F$ has an [[enriched functor|enriched]]  [[right adjoint]]

$$
  R : \mathbf{D} \to \mathrm{SPSh}(C)
$$

given by
  
$$
  R(A)
  =
  \mathbf{D}(F(-), A)
  \,.
$$


=--


+-- {: .proof}
###### Proof

This is a standard argument. 

We demonstrate the Hom-isomorphism that characterizes the [[adjunction]]:

Start with the above [[coend]] description of $\hat F$ 

$$
  \mathbf{D}({\hat F}(X), A)
  \simeq
  \mathbf{D}(
    \int^{U \in S}
     F(U) \cdot X(U) 
     ,
     A
  )
  \,.
$$

Then use the continuity of the enriched Hom-functor to pass it through the coend and obtain the following [[end]]:

$$
  \cdots \simeq
  \int_{U \in S}
    \mathbf{D}({\hat F}(U) \cdot X(U), A)
  \,.
$$

The defining property of the tensoring operation 
implies that this is equivalent to

$$
  \simeq
  \int_{U \in S}
  SSet( X(U), \mathbf{D}(F(U),A)) 
  \,.
$$

But this is the [[enriched functor category|end-formula]] for the $SSet$-object of 
[[natural transformation]]s between [[simplicial presheaf|simplicial presheaves]]:

$$
  \cdots
  \simeq
  [C^{op},SSet](X, \mathbf{D}(\Pi(-), A))
  \,.
$$

By definition this is the desired right hand of the hom isomorphism

$$
  \cdots
  =  [C^{op}, SSet](X, R(A))
  \,.
$$

=--

These two lemmas together constitute the proof of the proposition.

[[!redirects (∞,1)-Yoneda extension]]
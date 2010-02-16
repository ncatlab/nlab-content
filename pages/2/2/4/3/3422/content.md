<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>

> under construction

#Contents#
* automatic table of contents
{:toc}

## Idea

The **$(\infty,1)$-Grothendieck construction** is the analog of the [[Grothendieck construction]] which establishes an equivalence

$$
  Fib(C) \simeq 2Func(C^{op}, Cat)
$$

between [[fibered category|fibered categories]] and [[pseudofunctor]]s from [[category theory]] to [[(∞,1)-category]]-[[higher category theory|theory]].

The Grothendieck construction for [[∞-groupoid]]s constitutes an equivalence of [[(∞,1)-categories]]

$$
  RFib(C) \simeq \infty Func(C^{op}, \infty Grpd)
$$

of [[right fibration]]s and [[(∞,1)-functor]]s to [[? Grpd]], while the full Grothendieck construction for [[(∞,1)-categories]] constitutes an equivalence 

$$
  CartFib(C) \simeq \infty Func(C^{op}, (\infty,1)Cat)
$$

between [[Cartesian fibration]]s and [[(∞,1)-functor]]s to [[(∞,1)Cat]].


The correspondence between $(\infty,1)$-categorical [[cartesian fibrations]] $E \to C$ and [[(infinity,1)-presheaf|(∞,1)-presheaves]] $C \to (\infty,1)Cat^{op}$ may be [[model category|modeled]] by the [[Quillen equivalence]] between the [[model structure on marked simplicial over-sets]] and the projective [[global model structure on simplicial presheaves]].


## For $\infty$-groupoids


+-- {: .un_theorem}
###### Theorem 
**($(\infty,0)$-Grothendieck construction)**

Let $C$ be an [[(∞,1)-category]]. There is an equivalence 

$$
  RFib(C) \simeq Func(C^{op}, \infty Grpd)
$$

where in the left we have the $(\infty,1)$-category of [[right fibration]]s over $C$ and on the right the [[(∞,1)-category of (∞,1)-functors]] from the [[opposite category]] $C^{op}$ to [[∞Grpd]], i.e. the [[(∞,1)-category of (∞,1)-presheaves]] on $C$.

=--


In the next section we discuss how this statement is presented in terms of [[model categories]].

> (For the moment that also serves to define what the left hand side of the equivalence in the above theorem is).



### Model category presentation

Regard the [[(∞,1)-category]] $C$ in its incarnation as a [[simplicially enriched category]].

Let $S$ be a [[simplicial set]], $\mathcal{C}(S)$ the corresponding [[simplicially enriched category]] (where $\mathcal{C}$ is the adjoint of the [[homotopy coherent nerve]]) and let $\phi : \mathcal{C}(S) \to C$ be an [[SSet]]-[[enriched functor]].

+-- {: .un_theorem}
###### Theorem 
**(presentation of $(\infty,0)$-Grothendieck construction)**


This induces a [[Quillen adjunction]]

$$
  (St_\phi \dashv Un_\phi) : SSet/S
  \stackrel{\overset{Un_{\phi}}{\leftarrow}}{\overset{St_\phi}{\to}}
  [C^{op}, SSet]
$$

between the [[model structure for right fibrations]] and the global projective [[model structure on simplicial presheaves]] on $S$.

If $\phi$ is an equivalence in the [[model structure on simplicial categories]] then this Quillen adjunction is a [[Quillen equivalence]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, theorem 2.2.1.2]].

=--


## For $(\infty,1)$-categories

+-- {: .un_theorem}
###### Theorem 
**($(\infty,1)$-Grothendieck construction)**

Let $C$ be an [[(∞,1)-category]]. There is an equivalence 

$$
  Cart(C) \simeq Func(C^{op}, (\infty,1) Cat)
$$

where in the left we have the $(\infty,1)$-category of [[Cartesian fibration]]s over $C$ and on the right the [[(∞,1)-category of (∞,1)-functors]] from $C^{op}$ to the [[(∞,1)-category of (∞,1)-categories]].

=--


In the next section we discuss how this statement is presented in terms of [[model categories]].

> (For the moment that also serves to define what the left hand side of the equivalence in the above theorem is).

See also

* [[universal fibration of (∞,1)-categories]]. 


### Model category presentation



Regard the [[(∞,1)-category]] $C$ in its incarnation as a [[simplicially enriched category]].

Let $S$ be a [[simplicial set]], $\mathcal{C}(S)$ the corresponding [[simplicially enriched category]] (where $\mathcal{C}$ is the adjoint of the [[homotopy coherent nerve]]) and let $\phi : \mathcal{C}(S) \to C$ be an [[SSet]]-[[enriched functor]].

+-- {: .un_theorem}
###### Theorem 
**(presentation of $(\infty,1)$-Grothendieck construction)**


This induces a [[Quillen adjunction]]

$$
  (St_\phi \dashv Un_\phi) : SSet^+/S
  \stackrel{\overset{Un_{\phi}}{\leftarrow}}{\overset{St_\phi}{\to}}
  [C^{op}, SSet^+]
$$

between the [[model structure for Cartesian fibrations]] and the projective [[global model structure on functors]] with values in the [[model structure on marked simplicial over-sets|model structure on marked simplicial sets]].


If $\phi$ is an equivalence in the [[model structure on simplicial categories]] then this Quillen adjunction is a [[Quillen equivalence]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, theorem 3.2.0.1]].

=--




## Relation beween the model structures

+-- {: .un_theorem}
###### Theorem (HTT, section 3.1.5)

Let $S$ be a [[simplicial set]].

There is a sequence of [[Quillen adjunction]]s

$$
  (sSet/S)_{Joyal}
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  sSet^+/S
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  (sSet^+/S)^{loc}
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  (sSet/S)_{rfib}
  \stackrel{\overset{}{\to}}{\overset{}{\leftarrow}}
  (sSet/S)_{Quillen}
  \,.
$$

Where from left to right we have

1. the [[model structure on an overcategory]] for the Joyal [[model structure for quasi-categories]];

1. the [[model structure for Cartesian fibrations]];

1. some localizaton of the model structure for Cartesian fibrations;

1. the [[model structure for right fibrations]] 

1. the [[model structure on an overcategory]] for the Quillen [[model structure on simplicial sets]];

The first and third Quillen adjunction here is a [[Quillen equivalence]] if $S$ is a [[Kan complex]].

=--


[[!redirects (∞,1)-Grothendieck construction]]
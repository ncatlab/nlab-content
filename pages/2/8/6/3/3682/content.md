
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Homotopy Kan extensions are models/presentations for [[Kan extension]]s in [[(∞,1)-category]] theory in terms of [[homotopical category]] theory and [[enriched category theory]].

As a special case they reduce to [[homotopy limit]]s and [[homotopy colimit]]s, which in turn are models for [[limit in a quasi-category|(∞,1)-categorical limits and colimits]].

## In combinatorial simplicial model categories

The following describes homotopy Kan extensions in the context of [[combinatorial simplicial model categories]], i.e. $sSet_{Quillen}$-[[enriched model categories]] whose underlying ordinary model category is [[combinatorial model category|combinatorial]]. The discussion goes through verbatim also with $sSet_{Quillen}$ replaced by any [[excellent model category]].

### Recollection of ordinary global Kan extensions

Recall the global definition of ordinary [[Kan extension]]s: for $A$ a [[category]] and $p : C \to C'$ a [[functor]] between  [[small categories]], we have the [[functor categories]] $[C,A]$ and $[C',A]$ and precomposition with $p$ induces a functor

$$
  p^* : [C',A] \to [C,A]
  \,.
$$

If $A$ has all limits and colimits, then this functor has a [[left adjoint]] $Lan_p$ and a [[right adjoint]] $Ran_p$

$$
  (Lan_p \dashv p^* \dashv Ran_p)
  :=
  (p_! \dashv p^* \dashv p_*)
  :
  [C,A]
  \stackrel{\overset{Lan_p}{\to}}{\stackrel{\overset{p^*}{\leftarrow}}{\underset{Ran_p}{\to}}}
  [C',A]
  \,.
$$

These are the left and right [[Kan extension]] functors.

The following definition is the straightforward evident generalization of this from plain categories to [[simplicial model categories]].


### Definition

Let $A$ be a [[combinatorial simplicial model category]]. 
Let $C, C'$ be [[small category|small]] [[sSet]]-[[enriched model categories]]. Write $[C,A]$ and $[C',A]$ for the corresponding [[enriched functor categories]]. Notice that these carry the injective and the projective [[global model structure on functors]] $[C,A]_{inj}$ and $[C,A]_{proj}$, which themselves are combinatorial simplicial model categories.

Let 

$$
  f : C \to C'
$$ 

be an [[sSet]]-[[enriched functor]]. Let

$$
  f^* : [C'.A] \to [C,A]
$$

be the [[sSet]]-[[enriched functor]] induced by precomposition with $f$.



+-- {: .un_prop}
###### Definition/Proposition


The functor $f^*$ has both an [[sSet]]-[[left adjoint]] $f_!$ as well as a [[right adjoint]] $f_*$

$$
  (f_! \dashv f^* \dashv f_*) \; : \;
  [C,A]
  \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
  [C',A]
$$

and 

* $(f_! \dashv f^*)$ is a [[Quillen adjunction]] for 
  the projective [[global model structure on functors]]

  $$
    (f_! \dashv f^*) : [C,A]_{proj} \stackre{\to}{\leftarrow} [C',A]_{proj}
    \,,
  $$

* $(f^* \dashv f_)$ is a [[Quillen adjunction]] 
  for the injective [[global model structure on functors]]

  $$
    (f^*\dashv f_*) : [C,A]_{inj} \stackre{\to}{\leftarrow} [C',A]_{inj}
    \,,
  $$

If $f : C \to C'$ is a weak equivalence in the [[model structure on sSet-categories]] then these are [[Quillen equivalence]]s.

Now

* the right [[derived functor]]

  $$
    R f_* : ([C,A]_{proj})^\circ \to ([C',A]_{proj})^\circ
  $$

  is the **homotopy right Kan extension** functor;

* the left [[derived functor]]

  $$
    L f_{!} : ([C,A]_{inj})^\circ \to ([C',A]_{inj})^\circ
  $$

  is the **homotopy left Kan extension** functor.

Given $F \in [C,A]$ and $G \in [C',A]$ and a morphism $\eta : G \to f_* F$, we say that $\eta$ **exhibits $G$ as a homotopy right Kan extension** of $F$ if for some injectively fibrant replacement $F \to \hat F$ the composite morphism $G \to f_* F \to f_* \hat F$ is a weak equivalence.

For the special case that $C' = *$ we have

* the right [[derived functor]]

  $$
    R f_* : ([C,A]_{proj})^\circ \to ([*,A]_{proj})^\circ =\simeq A^\circ
  $$

  is the **[[homotopy limit]]** functor;

* the left [[derived functor]]

  $$
    L f_{!} : ([C,A]_{inj})^\circ \to ([*,A]_{inj})^\circ = A^\circ
  $$

  is the **[[homotopy colimit]]** functor.


=--


+-- {: .proof}
###### Proof

The statement of the Quillen adjunctions appears as [[Higher Topos Theory|HTT, prop A.3.3.7]]. The statement about the Quillen equivalences as [[Higher Topos Theory|HTT, prop A.3.3.8]].

=--

### Properties

Recall that for $F : C \to A$ an ordinary [[functor]] between ordinary [[categories]], its ordinary [[limit]] $\lim_\leftarrow F$ is characterized by the fact that for every object $a \in A$ the set $Hom(a, \lim_\leftarrow F)$ is the limit in [[Set]] of the functor $C \to A \stackrel{Hom_A(a,-)}{\to} Set$. So all ordinary limits are determined by limits in [[Set]].

The analogous statement here is that all homotopy limits are determined by homotopy limits in $sSet_{Quillen}$.

+-- {: .un_prop}
###### Proposition

Let $F \in [C,A]$ and $G \in [C',A]$ be fibrant in the projective [[global model structure on functors]]. Then a morphism $\eta : G \to f_* A$ exhibts $G$ as a homotopy right Kan extension of $F$ precisely if for each cofibrant $a \in A$ -- equivalently for each fibrant-cofibrant $a \in A$ -- the morphism

$$  
  \eta_a : A(a,G(-)) \to f_* A(a,F(-))
$$

exhibits $A(a,G(-)) : C' \to sSet_{Quillen}$ as a homotopy right Kan extension of $A(a,G(-)) : C \to sSet_{Quillen}$;

=--


+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, prop. A.3.3.12]].

=--

## In Kan-complex enriched categories

### Definition

The above characterization of homotopy Kan extensions in simplicial combinatorial model categories $A$ in terms of homotopy Kan extensions in $sSet$ only involves [[hom-object]]s of the form $A(a,c)$, where $a$ is cofibrant and $c$ is fibrant. So it involves only the [[derived hom-space]]s of $A$, which are [[Kan complex]]es.

Accordingly, this characterization makes sense for $A$ any locally fibrant $sSet_{Quillen}$-enriched category, i.e. for every Kan-complex-enriched category:


+-- {: .un_definition}
###### Definition

For $A$ a [[Kan complex]]-[[enriched category]] and $f : C \to C'$ an [[enriched functor]] of small [[sSet]]-[[enriched categories]], 
given $F \in [C,A]$ and $G \in [C',A]$ we say a morphism $\eta : G \to f_* F$, **exhibits $G$ as a homotopy right Kan extension** if for all $a \in A$ the morphis,

$$  
  \eta_a : A(a,G(-)) \to f_* A(a,F(-))
$$

exhibits $A(a,G(-)) : C' \to sSet_{Quillen}$ as a homotopy right Kan extension of $A(a,G(-)) : C \to sSet_{Quillen}$.

=--

### Properties

Under the [[homotopy coherent nerve]], homotopy colimits in a Kan-complex enriched categories as defined above are [[limit in a quasi-category|quasi-categorical colimits]]:

+-- {: .un_prop}
###### Proposition

For $C$ and $A$ Kan-complex-enriched categories and $F \in [C,A]$, a morphism $\eta : F \to const_q$ exhibits $q \in A$ as a homotopy colimit in $A$ in the above sense precisely  if for $N(f) : N(C) \to N(A)$ the corresponding morphism of [[quasi-categories]] under the [[homotopy coherent nerve]] and $N(f)^\triangleright : N(C)^\triangleright \to N(A)$ the extension to cones given by $\eta$, $N(f)^{\triangleright}$ is a [[limit in a quasi-category|quasi-categorical colimit diagram]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, theorem 4.2.4.1]].

=--

## References

For instance section A.3.3 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
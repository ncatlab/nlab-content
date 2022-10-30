

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Homotopy Kan extensions are models/presentations for [[(∞,1)-Kan extension]]s -- i.e. [[Kan extension]]s in an [[(∞,1)-category]] theory -- in terms of [[homotopical category]] theory and [[enriched category theory]].

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
Let $C, C'$ be [[small category|small]] [[sSet]]-[[enriched model categories]]. Write $[C,A]$ and $[C',A]$ for the corresponding [[enriched functor categories]]. Notice that these carry the injective and the projective [[model structure on functors]] $[C,A]_{inj}$ and $[C,A]_{proj}$, which themselves are combinatorial simplicial model categories.

Let 

$$
  f : C \to C'
$$ 

be an [[sSet]]-[[enriched functor]]. Let

$$
  f^* : [C'.A] \to [C,A]
$$

be the [[sSet]]-[[enriched functor]] induced by precomposition with $f$.



+-- {: .num_prop}
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
  the projective [[model structure on functors]]

  $$
    (f_! \dashv f^*) : [C,A]_{proj} \stackrel{\to}{\leftarrow} [C',A]_{proj}
    \,,
  $$

* $(f^* \dashv f_*)$ is a [[Quillen adjunction]] 
  for the injective [[model structure on functors]]

  $$
    (f^*\dashv f_*) : [C,A]_{inj} \stackrel{\to}{\leftarrow} [C',A]_{inj}
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


+-- {: .num_defn}
###### Definition

Since intrinsically Kan extensions, as every universal construciton, are supposed to be only defined up to weak equivalence, it is sometimes useful to make the extra freedom of choosing any weakly equivalent object explicit by the following definition.

Given $F \in [C,A]$ and $G \in [C',A]$ and a morphism $\eta : G \to f_* F$, we say that $\eta$ **exhibits $G$ as a homotopy right Kan extension** of $F$ if for some injectively fibrant replacement $F \to \hat F$ the composite morphism $G \to f_* F \to f_* \hat F$ is a weak equivalence.

So $f_* \hat F$ here is a homotopy Kan extension as produced by the derived functor, while $G$ may be a more general object, weakly equivalent to it.

=--


### Properties

#### Derived-hom into a ho-Kan extension is a ho-Kan extention {#HomIntoKanExt}

Recall that for $F : C \to A$ an ordinary [[functor]] between ordinary [[categories]], its ordinary [[limit]] $\lim_\leftarrow F$ is characterized by the fact that for every object $a \in A$ the set $Hom(a, \lim_\leftarrow F)$ is the limit in [[Set]] of the functor $C \to A \stackrel{Hom_A(a,-)}{\to} Set$. So all ordinary limits are determined by limits in [[Set]].

The analogous statement here is that all homotopy limits are determined by homotopy limits in $sSet_{Quillen}$.

+-- {: .num_prop}
###### Proposition

Let $F \in [C,A]$ and $G \in [C',A]$ be fibrant in the projective [[model structure on functors]]. Then a morphism $\eta : G \to f_* F$ exhibits $G$ as a homotopy right Kan extension of $F$ precisely if for each cofibrant $a \in A$ -- equivalently for each fibrant-cofibrant $a \in A$ -- the morphism

$$  
  \eta_a : A(a,G(-)) \to  A(a, f_* F(-))
$$

exhibits $A(a,G(-))  \in [C',sSet]$ as a homotopy right Kan extension of $A(a,F(-)) \in [C,sSet]$.

=--


+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, prop. A.3.3.12]].

First notice that a  replacement $F \stackrel{\simeq}{\to} \hat F$ in [C,A]_{inj} by a fibrant $\hat F$ induces a weak equivalence $A(a,F(-)) \to A(a,\hat F(-))$ for all cofibrant $a \in A$, since $F$ is assumed projectively fibrant and using the properties of [[derived hom-space]]s in an [[enriched model category]].

Therefore we may assume without loss of generality that $F$ is already injectively fibrant. Then it also follows that for all cofibrant $a \in A $ we have that $A(a,F(-)) \in [C,sSet]_{inj}$ is fibrant: because $A(a,(-))$ having [[right lifting property]] against all acyclic cofibrations $H \to H'$ in $[C,sSet]_{inj}$ 

$$
  \array{
    H &\to & A(a,F(-))
    \\
    \downarrow & \nearrow
    \\
    H'
  }
$$

is equivalent, by the [[sSet]]-[[copower|tensor]]-adjunction in $A$, to $F$ itself having the right lifting property against the map from $A \cdot H : c \mapsto H(c)\cdot A$ to $H' \cdot A$

$$
  \array{
    H\cdot a &\to & F
    \\
    \downarrow & \nearrow
    \\
    H'\cdot a
  }
  \,.
$$

But since tensoring in $A$ with [[sSet]] is a left [[Quillen bifunctor]] by definition of [[enriched model category]], we have that tensoring the cofibrant $a$ with an acyclic cofibration of simplicial sets produces an acaclic cofibration in $A$, so that $H \cdot a \to H'\cdot a$ is an acyclic cofibration in $[C,sSet]_{inj}$. But by the previous remark $F$ is (can assumed to be) injectively fibrant, hence the lift exists. Hence $A(a,F(-))$ is indeed injectively fibrant.

With this in hand, we have now the following equivalent restatement of the claim:

$\eta$ is a weak equivalence precisely if $\eta_a$ is for all cofibrant (or cofibrant and fibrant) $a$.

The implication $(\eta we) \Rightarrow (\eta_a we)$ follows because in the [[enriched model category]] $A$, the functor $A(a,F(-))$ out of the cofibrant objectwise $a$ into the fibrant $F(-)$  preserves weak equivalences.

Conversely, if $\eta_a: A(a,G(-)) \to A(a,f_* F(-))$ is a weak equivalence for all fibrant and cofibrant $a$, then for all $c \in C$ $\eta(c) : G(c) \to f_* F(c)$ is a weak equivalence for all $c \in C$ by the [[Yoneda lemma]], for instance in the $Ho(sSet)$-enriched [[homotopy category]] $Ho(A)$ of $A$: a morphism in $Ho(A)$ is an iso if homming all other objects into it produces an isomorphism.


=--


+-- {: .num_remark}
###### Remark

Notice that the statement makes sense in the full $sSet$-subcategory $A^\circ$ on fibrant-cofibrant objects of $A$, without needing any further mentioning on the model category structure on $A$, only that on $sSet_{Quillen}$ is involved. This allows to define homotopy Kan extensions in arbitrary Kan-complex enriched categories, which may or may not arise as $A^\circ$ for A a simplicial model category. This is discussed below.


=--


## In Kan-complex enriched categories {#InKanCplCat}

We obtain a notion of homotopy Kan extension that does not depend on any model category structure or even on weak equivalences anymore, but takes place entirely just in Kan-complex enriched categories.

### Definition

The above characterization of homotopy Kan extensions in simplicial combinatorial model categories $A$ in terms of homotopy Kan extensions in $sSet$ only involves [[hom-object]]s of the form $A(a,c)$, where $a$ is cofibrant and $c$ is fibrant. So it involves only the [[derived hom-space]]s of $A$, which are [[Kan complex]]es.

Accordingly, this characterization makes sense for $A$ any locally fibrant $sSet_{Quillen}$-enriched category, i.e. for every Kan-complex-enriched category:


+-- {: .num_defn}
###### Definition

For $A$ a [[Kan complex]]-[[enriched category]] and $f : C \to C'$ an [[enriched functor]] of small [[sSet]]-[[enriched categories]], 
given $F \in [C,A]$ and $G \in [C',A]$ we say a morphism $\eta : G \to f_* F$, **exhibits $G$ as a homotopy right Kan extension** if for all $a \in A$ the morphism

$$  
  \eta_a : A(a,G(-)) \to  A(a,f_* F(-))
$$

exhibits $A(a,G(-)) : C' \to sSet_{Quillen}$ as a homotopy right Kan extension of $A(a,F(-)) : C \to sSet_{Quillen}$.

=--

### Homotopy limits and colimits {#Holims}

If the diagram category $C'$ is the terminal $sSet$-category, the left and right homotopy Kan extension along $f : C \to {*}$ is the [[homotopy limit]] and [[homotopy colimit]], respectively.

#### Characterization in terms of hom-adjuncts

In thae case that we are homotopy Kan extending to the point, if $\eta : G \to f_* F$ exhibits a right homotopy Kan extension, $G \in A$ is  a single object of $A$ and by adjunction this corresponds to a [[natural transformation]] $f^* G = const G \to F$, whose components are a collection of morphisms

$$
  \{ \eta_c : G \to F(c) \}_{c \in C}
$$

in $A$. Then 

+-- {: .num_cor}
###### Corollary

The fact that $\eta$ exhibits a right homotopy Kan extension is equivalent to the statement that for all $a \in A$ the morphism

$$
  A(a, G) \to \lim_{\leftarrow} A(a,F(-))
$$

induced by composing with the $\{\eta_c\}$ _exhibits $A(a,G)$ as a homotopy limit_  of $A(a,F(-))$ in $sSet_{Quillen}$, in the above sense.

Since $\lim_{\leftarrow} A(a,F(-)) = [C,sSet](const a,F)$ is an isomorphissm, this in turn is equivalent to the statemeent that

$$
  A(a, G) \to [C,sSet](const a, F)
$$

exhibits that homotopy Kan extension.

=--

Analogously for homotopy colimits.

#### Relation to quasi-categorical limits and colimits

The above considerations can be used to show that under the [[homotopy coherent nerve]], homotopy colimits in a Kan-complex enriched categories as defined above are [[limit in a quasi-category|quasi-categorical colimits]]:

+-- {: .num_prop}
###### Proposition

For $C$ and $A$ Kan-complex-enriched categories and $F \in [C,A]$, a morphism $\eta : F \to const_q$ exhibits $q \in A$ as a homotopy colimit in $A$ in the above sense precisely  if for $N(f) : N(C) \to N(A)$ the corresponding morphism of [[quasi-categories]] under the [[homotopy coherent nerve]] and $N(f)^\triangleright : N(C)^\triangleright \to N(A)$ the extension to cones given by $\eta$, $N(f)^{\triangleright}$ is a [[limit in a quasi-category|quasi-categorical colimit diagram]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, theorem 4.2.4.1]]. Some details on the proof are discussed at [[limit in a quasi-category]].

=--

## In terms of derivators

The notion of [[derivator]] is largely a tool for handling homotopy Kan extensions. See there for details.






































## Properties

### Pointwise homotopy Kan extensions
 {#Pointwise}

Under suitable conditions (but typically) homotopy Kan extensions may be computed [pointwise](Kan+extension#Pointwise) by [[homotopy colimits]].

Discussion of pointwise homotopy Kan extensions in [[cofibration categories]] is in ([Radulescu-Banu 06, theorem 9.6.5](#Radulescu-Banu06)). This is reviewed in the context of [[model categories]] in ([Cisinski 09, prop. 1.14](#Cisinski09)). In the more general context of [[relative categories]] discussion is in ([Gonzales 11, section 4](#Gonzales11)).

See also at [(∞,1)-Kan extension -- Properties -- Pointwise](/%28infinity%2C1%29-Kan+extension#Pointwise).




## References

General theory of homotopy Kan extensions is discussed in  

* [[Jacob Lurie]], section A.3.3 of _[[Higher Topos Theory]]_

* [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]], 
  [[Jeff Smith]], _[[Homotopy Limit Functors on Model Categories
and Homotopical Categories]]_ , volume 113 of Mathematical Surveys and Monographs

* [[Bruno Kahn]], [[Georges Maltsiniotis]], _[[Structures de Dérivabilité]]_

* [[Jean-Marc Cordier]] and [[Tim Porter]], _Homotopy Coherent Category Theory_, Trans. Amer. Math. Soc. 349 (1997) 1-54.

A list of basic properties is in 

* [[Samuel Isaacson]], section 4 of _Exercises on homotopy colimits_ ([pdf](http://math.mit.edu/~mbehrens/TAGS/Isaacson_exer.pdf))

Pointwise [[homotopy Kan extensions]] are discussed in 

* {#Radulescu-Banu06} Andrei Radulescu-Banu, _Cofibrations in Homotopy Theory_ ([arXiv:0610009](http://arxiv.org/abs/math/0610009))

* {#Cisinski09} [[Denis-Charles Cisinski]], 

  _Images directes cohomologiques dans les cat&#233;gories de mod&#232;les, Ann. Math.Blaise Pascal 10 (2003), 195&#8211;244.

  _Locally constant functors_, Math. Proc. Camb. Phil. Soc. (2009), 147, 593 ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/lcmodcat3.pdf))


* {#Gonzales11} Beatriz Rodriguez Gonzalez, section 4 of _Realizable homotopy colimits_ ([arXiv:1104.0646](http://arxiv.org/abs/1104.0646))



[[!redirects homotopy Kan extensions]]
[[!redirects left homotopy Kan extension]]
[[!redirects left homotopy Kan extensions]]
[[!redirects homotopy left Kan extension]]
[[!redirects homotopy left Kan extensions]]
[[!redirects right homotopy Kan extension]]
[[!redirects right homotopy Kan extensions]]
[[!redirects homotopy right Kan extension]]
[[!redirects homotopy right Kan extensions]]
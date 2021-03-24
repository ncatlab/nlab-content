
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##  Idea 
 
The _universal fibration of [[(infinity,1)-category|(∞,1)-categories]] is the [[generalized universal bundle]] of $(\infty,1)$-categories in that it is [[Cartesian fibration]]

$$
  p : Z \to (\infty,1)Cat^{op}
$$

over the [[opposite category]] of the [[(∞,1)-category of (∞,1)-categories]] such that

* its fiber  $p^{-1}(C)$ over $C \in (\infty,1)Cat$ is just the $(\infty,1)$-category $C$ itself;

* every [[Cartesian fibration]] $p : C \to D$ arises as the [[pullback]] of the universal fibration along an [[(∞,1)-functor]] $S_p : D \to (\infty,1)Cat^{op}$.


Recall from the discussion at [[generalized universal bundle]] and at [[stuff, structure, property]] that for [[n-category|n-categories]] at least for low $n$ the corresponding universal object was the $n$-category $n Cat_*$ of [[pointed object|pointed]] $n$-categories. $Z$ should at least morally be $(\infty,1)Cat_*$.


## Definition 

### For $(\infty,1)$-categories

One description of the universal cartesian fibration is given in section 3.3.2 of [[Higher Topos Theory|HTT]] as the contravariant [[(∞,1)-Grothendieck construction]] applied to the identity functor $((\infty,1)Cat^{op})^{op} \to (\infty,1)Cat$. 

We can also give a more direct description:

+-- {: .num_prop }
###### Proposition

$Z^{op}$ is equivalent to the full subcategory of $(\infty,1)Cat^{[1]}$ spanned by the morphisms of the form $[C_{x/} \to C]$ for small (∞,1)-categories $C$ and objects $x \in C$.

The universal fibration $Z \to (\infty,1)Cat^{op}$ is opposite to the target evaluation.

Dually, the universal cocartesian fibration is $Z' \to (\infty,1)Cat$ where $Z'$ is the (∞,1)-category of arrows of the form $[C_{/x} \to C]$.

=--
+-- {: .proof }
###### Proof

This is the proof idea of [this mathoverflow post](#direct).

By proposition 5.5.3.3 of Higher Topos Theory, there are presentable fibrations $RFib \to (\infty,1)Cat$ and $(\infty,1)Cat^{[1]} \xrightarrow{tgt} (\infty,1)Cat$ classifying functors $C \mapsto \mathcal{P}(C)$ and $C \mapsto (\infty,1)Cat_{/C}$.

By proposition 5.3.6.2 of Higher Topos Theory, the yoneda embedding $j : C \to \mathcal{P}(C)$ is a natural transformation, and the covariant Grothendieck construction provides a cocartesian functor $Z' \to RFib$. Since it is fiberwise fully faithful and $(-)_!$ preserves representable presheaves, we can identify $Z'$ with the full subcategory of $RFib$ consisting of the representable presheaves.

The Grothendieck construction provides a fully faithful $\mathcal{P}(C) \to 
(\infty,1)Cat_{/C}$ whose essential image is the right fibrations. The contravariant Grothendieck construction a cartesian functor $RFib \to (\infty,1)Cat^{[1]}$. Since it is fiberwise fully faithful and pullbacks preserve right fibrations, we can identify $RFib$ with the full subcategory of $( \infty,1)Cat^{[1]}$ spanned by right fibrations.

By the relationship between the covariant and contravariant Grothendieck constructions, the universal cartesian fibration is classified by $op : ((\infty,1)Cat^{op})^{op} \to (\infty,1)Cat$.

=--

+-- {: .num_remark }
###### Remark

A key point of this description is that for any small (∞,1)-category $C$, the functor $x \mapsto C_{/x}$ (where $x \to y$ acts by composition) is a fully faithful functor $C \to (\infty,1)Cat_{/C}$. Dually, $x \mapsto C_{x/}$ is a fully faithful functor $C^{op} \to (\infty,1)Cat_{/C}$

=--

The hom-spaces of the universal cocartesian fibration can be described as
$$
  Z'([C_{/x} \to C], [D_{/y} \to D]) \simeq Core(eval_x \downarrow y)
$$
where $eval_x : D^C \to D$. This should be compared with the lax [[slice 2-category]] construction. In fact, $Z'$ can be constructed by taking the underlying (∞,1) category of the lax coslice (or colax, depending on convention) over the point of the (∞,2)-category of (∞,1)-categories.


### For $\infty$-Groupoids 
  {#RestInfGrpd}

+-- {: .num_defn }
###### Definition

The universal fibration of $(\infty,1)$-categories restricts to a [[Cartesian fibration]] $Z|_{\infty Grpd} \to \infty Grpd^{op}$ over [[∞Grpd]] by [[pullback]] along the inclusion morphism $\infty Grpd \hookrightarrow (\infty,1)Cat$

$$
  \array{
    Z|_{\infty Grpd} &\to& Z
    \\
    \downarrow && \downarrow
    \\
    \infty Grpd^{op} &\hookrightarrow& (\infty,1)Cat^{op}
  }
  \,.
$$

=--

This is the _[[universal Kan fibration]]_.

+-- {: .num_remark }
###### Remark

The [[∞-functor]] $Z|_{\infty Grpd} \to \infty Grpd^{op}$ is even a [[right fibration]] and it is the _universal right fibration_. In fact it is (when restricted to small objects) the [[object classifier]] in the [[(∞,1)-topos]] [[∞Grpd]], see at [object classifier -- In ∞Grpd](%28sub%29object+classifier+in+an+%28infinity%2C1%29-topos#ObjectClassifierInInfinityGroupoid). 

=--

+-- {: .num_prop }
###### Proposition

The universal left fibration is the forgetful functor
$\infty Grpd_* \to \infty Grpd$. Its opposite is the universal right fibration.

=--
+-- {: .proof}
###### Proof
This is proposition 3.3.2.7 of [[Higher Topos Theory|HTT]].
=--

+-- {: .num_prop }
###### Proposition

The following are equivalent:

* An [[∞-functor]] $p : C \to D$ is a [[right Kan fibration]].

* Every functor $S_p : D \to (\infty,1)Cat$ that classifies $p$ as a [[Cartesian fibration]] factors through [[∞-Grpd]].

* There is a functor $G_p : D \to \infty Grpd$ that classifies $p$ as a [[right Kan fibration]].

=--

+-- {: .proof}
###### Proof

This is proposition 3.3.2.5 in [[Higher Topos Theory|HTT]].

=--






## Models

For concretely constructing the relation between [[Cartesian fibration]]s $p : E \to C$ of [[(infinity,1)-categories|(∞,1)-categories]] and [[(∞,1)-functor]]s $F_p : C \to (\infty,1)Cat$ one may use a [[Quillen equivalence]] between suitable [[model category|model categories]] of [[marked simplicial set]]s.

For $C$ an [[(∞,1)-category]] regarded as a [[quasi-category]] (i.e. as a [[simplicial set]] with certain properties), the two model categories in question are

* the projective [[global model structure on simplicial presheaves]] on $[C,SSet]$ -- this models the [[(∞,1)-category of (∞,1)-functors]] $(\infty,1)Func(C,(\infty,1)Cat)$.

* the _covariant model structure_ on the [[over category]] $SSet/C$ -- this models the $(\infty,1)$-category of [[Cartesian fibration]]s over $C$.


The [[Quillen equivalence]] between these is established by the [[relative nerve]] construction

$$
  N_{-}(C) : [C,SSet] \to SSet/C
  \,.
$$

By the [[adjoint functor theorem]] this functor has a [[left adjoint]]

$$
  F_{-}(C) : SSet/C \to [C,SSet]
  \,.
$$

For $p : E \to C$ a [[left Kan fibration]] the functor $F_p(C) : C \to SSet$ sends $c \in Obj(C)$ to the [[fiber]] $p^{-1}(c) := E \times_C \{c\}$

$$
  F_p(C) : c \mapsto p^{-1}(c)
  \,.
$$

(See remark 3.2.5.5 of [[Higher Topos Theory|HTT]]).


## References

The universal fibration as such is discussed in section 3.3.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The concrete description in terms of model theory on marked simplicial sets is in section 3.2. A simpler version of this is in section 2.2.1

The direct description of the universal fibration is discussed at

* {#direct} MathOverflow: _[A construction of the universal cocartesian fibration](https://mathoverflow.net/questions/383275/)_

Discussion of fibrations via [[(∞,2)-category]] theory 

* [[Jacob Lurie]], chapter 5 _[Fibrations of ∞-Categories](https://kerodon.net/tag/01J2)_ (2021) in: _[[Kerodon]]_

[[!redirects universal fibration of (∞,1)-categories]]

[[!redirects universal right fibration]]

[[!redirects universal Cartesian fibration]]

[[!redirects universal fibration of ∞-groupoids]]



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
* automatic table of contents goes here
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

...see section 3.3.2 of [[Higher Topos Theory|HTT]]...



### Restriction to $\infty$-Groupoids {#RestInfGrpd}

The universal fibration of $(\infty,1)$-categories restricts to a [[Cartesian fibration]] $Z|_{\infty Grpd} \to \infty Grpd^{op}$ over [[∞-Grpd]] by [[pullback]] along the inclusion morphism $\infty Grpd \hookrightarrow (\infty,1)Cat$

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

The [[∞-functor]] $Z|_{\infty Grpd} \to \infty Grpd^{op}$ is even a [[right fibration]] and it is the universal right fibration. 

+-- {: .un_prop }
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

[[!redirects universal fibration of (∞,1)-categories]]
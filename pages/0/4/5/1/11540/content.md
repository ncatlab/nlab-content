
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### Functoriality w.r.t. functors

Given a [[small category]] $C$, one can consider the [[category of presheaves]] $PSh(C, D)$ valued in some [[category]] $D$.  Given some assumptions on $D$, any [[functor]] of small categories $F \colon C \to C'$ induces two [[adjoint functors|adjoint pairs]]

  $$ F_! \,\colon\, PSh(C, D) \rightleftarrows PSh(C', D) \,\colon\, F^\ast $$

  $$ F^* \,\colon\, PSh(C', D) \rightleftarrows PSh(C, D) \,\colon\, F_\ast $$

Here, $F^\ast$ is given by precomposition with $F$, whereas $F_!$ and $F_\ast$ are the left and right (global) [[Kan extensions]] along $F$.


### Functoriality w.r.t. profunctors

In fact, more generally, any [[profunctor]] $\mathcal{P} : C \nrightarrow C'$ (i.e. $\mathcal{P} : C \times {C'}^{op} \to D$ or, after [[currying]], $P : C \to PSh(C', D)$) gives rise to a single [[adjunction|adjoint pair]]

  $$ P_\odot \,\colon\, PSh(C, D) \rightleftarrows PSh(C', D) \,\colon\, P^\odot $$

($P_\odot$ and $P^\odot$ are not standard notations) where $P_\odot$ is the [[Yoneda extension]] of $P$.

A functor $F \,\colon\, C \to C'$ gives rise to two profunctors:

* a [[companion]] profunctor $\hat F : C \nrightarrow C'$, given by

  $$ \hat F \,\colon\, C \times {C'}^{op} \to D : (c, c') \mapsto Hom_{C'}(c', Fc). $$

  After currying, this amounts to the functor $y \circ F : C \to PSh(C')$.

* a [[conjoint]] profunctor $\check F : C' \nrightarrow C$, given by

  $$ \check F \,\colon\, C' \times {C}^{op} \to D \,\colon\, (c', c) \mapsto Hom_{C'}(Fc, c'). $$

  After currying, this amounts to the functor $F^* \circ y : C' \to PSh(C)$.

The former profunctor produces the adjoint pair $F_! \dashv F^*$, i.e. $F_! = (y \circ F)_\odot$ and $F^* \cong (y \circ F)^\odot$.
The latter profunctor produces the adjoint pair $F^* \dashv F_*$, i.e. $F^* \cong (F^* \circ y)_\odot$ and $F_* = (F^* \circ y)^\odot$.

## Definitions

+-- {: .num_defn}
###### Definition

Let $F : C \to C'$ be a functor of small categories and $D$ some category.  The **[[restriction of scalars]]** functor $F^* \,\colon\, PSh(C', D) \to PSh(C, D)$ is given by the formula $H \mapsto H \circ f$, i.e. mapping a [[presheaf]] $H \,\colon\, C'^{op} \to D$ to the composite
  $$C^{op} \stackrel{F}{\to} C'^{op} \stackrel{H}{\to} D.$$
=--

+-- {: .num_prop}
###### Proposition

Suppose $D$ admits small [[colimits]] (resp. small [[limits]]).  Then the functor $F^\ast$ admits a [[left adjoint]] $F_!$ (resp. [[right adjoint]] $F_\ast$).
=--


## Properties

+-- {: .num_lemma}
###### Lemma

Let $F \,\colon\, C \rightleftarrows C' \,\colon\, G$ be an [[adjoint pair]] and consider the induced functors $(F_!, F^\ast, F_\ast)$ and $(G_!, G^*, G_*)$.  One has

* $F_!$ is left adjoint to $G_!$,
* $F^*$ is left adjoint to $G^*$,
* $F_*$ is left adjoint to $G_*$,
* $F_* \cong G^*$,
* $F^* \cong G_!$.
=--

Note that all these claims are in fact equivalent.

+-- {: .num_lemma}
###### Lemma
If $F$ is fully faithful, then so are $F_!$ and $F_*$.
=--

+-- {: .proof}
###### Proof
A left adjoint functor $L \dashv R$ is fully faithful precisely if $R L$ is naturally isomorphic to the identity functor (by the unit). Dually, $R$ is fully faithful precisely if $L R$ is naturally isomorphic to the identity (by the co-unit). Hence, it suffices to prove $F^* F_! \cong Id$, which by uniqueness of the right adjoint immediately implies that $F^* F_* \cong Id$ and thus proves both claims.

Being a left adjoint, $F^* F_!$ preserves colimits. Because every presheaf is a colimit of representable objects, it is sufficient to show that $F^* F_! y \cong y$ where $y$ is the Yoneda-embedding. We have
\[
(F^* F_! y I) J \cong (F^* y F I) J = (y F I) (F J) = Hom(F J, F I) \cong Hom(J, I) = (y I) J.
\]
=--

## See also

For functoriality of [[sheaves]], see

* [[restriction and extension of sheaves]]
* [[direct image]]
* [[inverse image]]

The pseudofunctor $PSh$ (with $-_!$ as its action on morphisms) takes a category to its [[free cocompletion]]. As such, it has the structure of a weak [[2-monad]], and more specifically it is a prototypical example of a [[lax-idempotent 2-monad]]. It factors over its Eilenberg-Moore 2-category, the 2-category of ([[total category|total]]? [[cocomplete]]?) categories, as a [[lax-idempotent 2-adjunction]].
The bind operation for $PSh$ is given by [[Yoneda extension]] and the [[Kleisli 2-category]] of $PSh$ is [[Prof]].

## References

* [[SGA 4]], Exp. I, no. 5.
* [[Stacks Project]], tags [00VC](http://stacks.math.columbia.edu/tag/00VC) and [00XF](http://stacks.math.columbia.edu/tag/00XF).
 * {#Nuyts24} [[Andreas Nuyts]], _Lifting Profunctors to Presheaf Categories_, [note](https://anuyts.github.io/files/lifting-profunctors.pdf)
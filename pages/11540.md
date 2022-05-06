
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

Given a [[small category]] $C$, one can consider the [[category of presheaves]] $PSh(C, D)$ valued in some [[category]] $D$.  Given some assumptions on $D$, any [[functor]] of small categories $F : C \to C'$ induces two [[adjunction|adjoint pairs]]

  $$ F_! : PSh(C, D) \rightleftarrows PSh(C', D) : F^* $$

  $$ F^* : PSh(C', D) \rightleftarrows PSh(C, D) : F_* $$

## Definitions

+-- {: .num_defn}
###### Definition

Let $F : C \to C'$ be a functor of small categories and $D$ some category.  The **[[restriction of scalars]]** functor $F^* : PSh(C', D) \to PSh(C, D)$ is given by the formula $H \mapsto H \circ f$, i.e. mapping a [[presheaf]] $H : C'^{op} \to D$ to the composite
  $$C^{op} \stackrel{F}{\to} C'^{op} \stackrel{H}{\to} D.$$
=--

+-- {: .num_prop}
###### Proposition

Suppose $D$ admits small [[colimits]] (resp. small [[limits]]).  Then the functor $F^*$ admits a [[left adjoint]] $F_!$ (resp. [[right adjoint]] $F_*$).
=--


## Properties

+-- {: .num_lemma}
###### Lemma

Let $F : C \rightleftarrows C' : G$ be an [[adjoint pair]] and consider the induced functors $(F_!, F^*, F_*)$ and $(G_!, G^*, G_*)$.  One has

* $F_!$ is left adjoint to $G_!$,
* $F^*$ is left adjoint to $G^*$,
* $F_*$ is left adjoint to $G_*$,
* $F_* = G^*$,
* $F^* = G_!$.
=--

Note that all these claims are in fact equivalent.

+-- {: .num_lemma}
###### Lemma
If $F$ is fully faithful, then so are $F_!$ and $F_*$.
=--

+-- {: .proof}
###### Proof
A left adjoint functor $L \dashv R$ is fully faithful precisely if $RL$ is naturally isomorphic to the identity functor (by the unit). Dually, $R$ is fully faithful precisely if $LR$ is naturally isomorphic to the identity (by the co-unit). Hence, it suffices to prove $F^* F_! \cong Id$, which by uniqueness of the right adjoint immediately implies that $F^* F_* \cong Id$ and thus proves both claims.

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

## References

* [[SGA 4]], Exp. I, no. 5.
* [[Stacks Project]], tags [00VC](http://stacks.math.columbia.edu/tag/00VC) and [00XF](http://stacks.math.columbia.edu/tag/00XF).
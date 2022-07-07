
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

The _pushout-product axiom_ is a compatibility condition between 

1. a [[closed monoidal category|closed]]$\,$[[monoidal category|symmetric monoidal]] structure 

2. a [[model category]] structure

on a category.

[[closed monoidal category|Closed]]$\;$[[monoidal category|symmetric monoidal categories]] and having a model category structure, that satisfies the pushout-product axiom, together with a unit condition, are called [[monoidal model category|monoidal model categories]] and hence are in particular [[closed monoidal homotopical category|closed monoidal homotopical categories]].

This is relevant in [[enriched homotopy theory]], which pairs [[enriched category theory]] with [[homotopy theory]].

## Definition

Let $C$ be a [[closed monoidal category|closed]] [[monoidal category|symmetric monoidal category]] equipped with a [[model category]] structure. 

Then $C$ satisfies the _pushout-product axiom_ if for any pair of [[cofibrations]] $f : X \to Y$ and $f' \colon X' \to Y'$ their [[pushout-product]], hence the induced morphism out of the [[coproduct]]

$$
  (X \otimes Y') \coprod_{X \otimes X'} (Y \otimes X')
  \to
  Y \otimes Y'
  \,,
$$

is itself a cofibration, which, furthermore, is [[acyclic cofibration|acyclic]] if $f$ or $f'$ is.

This means that the [[tensor product]]

$$
  \otimes \colon C \times C \to C
$$ 

is a left [[Quillen bifunctor]].

If the monoidal category underlying $C$ is a [[closed monoidal category]], one can [[formal duality|dually]] define the _pullback-power axiom_ to mean that if $f \colon A \to B$ is a [[cofibration]] and $g \colon X \to Y$ is a [[fibration]], their [[pullback power]] 

$$
  [B, X]
  \to
  [A, X] \times_{[A,Y]} [B, Y]
  \,,
$$

is a fibration, which, furthermore, is [[acyclic fibration|acyclic]] if $f$ or $g$ is.

However, by [[Joyal-Tierney calculus#IteratedLifting|Joyal-Tierney calculus]], the pullback-power axiom holds if and only if the pushout-power axiom holds.

## Remarks

* This implies in particular that tensoring with [[cofibrant objects]] preserves cofibrations and acyclic cofibrations.

* However the tensor product of two (acyclic) cofibrations is in general not an (acyclic) cofibration.

* The pushout-product axiom makes sense more generally in the context of a [[two-variable adjunction]] between model categories.  This is important in [[enriched homotopy theory]].

## Related concepts


* [[monoidal model category]]


* dually: [pullback-power axiom](enriched+model+category#PullbackPowerAxiom) in [[enriched model categories]]

* [[Joyal-Tierney calculus]]

## References

Discussion for [[model (infinity,1)-categories|model $\infty$-categories]] (such as with [[homotopy Kan fibrations]]):

* {#MazelGee15} [[Aaron Mazel-Gee]], around Def. 4.3 in: *Model ∞-categories II: Quillen adjunctions*, New York Journal of Mathematics **27** (2021) 508-550.  &lbrack;[arXiv:1510.04392](https://arxiv.org/abs/1510.04392), [nyjm:27-21](http://nyjm.albany.edu/j/2021/27-21.html)&rbrack;



[[!redirects pushout product axiom]]


[[!redirects pullback-power axiom]]
[[!redirects pullback power axiom]]



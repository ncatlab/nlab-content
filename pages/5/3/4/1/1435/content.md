
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#The category $CRing$#
* table of contents
{:toc}

## Definition ##

$CRing$ is the category of commutative [[ring]]s and ring homomorphisms.

A commutative ring is a commutative [[monoid object]] in [[Ab]], so $CRing = CMon(Ab)$ is the [[category of commutative monoids]] in [[abelian groups]]. 




The [[opposite category]] $CRing^{op}$ is the category of [[affine schemes]].

## Properties

### Cocartesian co-monoidal structure
 {#CocartesianComnonoidalStructure}

+-- {: .num_prop #CoproductIsTensorProduct}
###### Proposition

The [[coproduct]] in $CRing$ is given by the underlying [[tensor product of abelian groups]], equipped with its canonically induced commutative ring structure.

=--

By [this general proposition](category+of+monoids#PushoutsInCMonGivenByTensorProduct) discussed at _[[category of commutative monoids]]_.

+-- {: .num_remark }
###### Remark

Prop. \ref{CoproductIsTensorProduct} means that tensor product of commutative rings exhibits [[cartesian monoidal category]] structure on the [[opposite category]] $CRing^{op}$. 

=--

## Generalizations ##

* The [[slice category]] of $CRing$ under a ring $R$ is the category $R$[[CAlg]] of commutative [[associative algebra]]s over $R$.

* There is a "smooth" version of $CRing^{op}$: the category of [[smooth locus|smooth loci]].

* There is a [[higher category theory]] version of $CRing$: the $(\infty,1)$-[[(∞,1)-category|category]] of $E_\infty$-[[E-∞ ring|rings]].


category: category
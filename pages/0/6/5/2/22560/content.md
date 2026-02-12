[[!redirects magma category]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Just as a [[monoidal category]] is the [[categorification]] of a [[monoid]] and a [[rig category]] is the categorification of a [[rig]], a *magmoidal category* should be the categorification of a [[magma]]. 

## Definition

A __magmoidal category__ or __magmal category__ is a [[category]] $C$ with a [[functor]] 

$$\otimes: C \times C \to C$$ 

from the [[product category]] of $C$ with itself. 

If there is a specified object $I$, and natural isomorphisms $\lambda_A:\colon A\otimes I\stackrel{\simeq}{\to} A$ and $\rho_A:\colon I\otimes A\stackrel{\simeq}{\to} A$ satisfying $\rho_I = \lambda_I\colon I\otimes I\stackrel{\simeq}{\to} I$, then it is a **magmoidal category with unit**.

Note that this coherence condition appeared in [[Mac Lane]]'s original definition of a [[monoidal category]], but was proven to follow from the other coherence conditions for a monoidal category by [[Max Kelly]]. (The coherence condition usually placed on unitors in [[monoidal categories]] cannot even be stated in the context of a magmoidal category, since there is no associator to relate $A\otimes (I\otimes B)$ and $(A\otimes I)\otimes B$.)


## Examples

For example, [[monoidal categories]] such as [[braided monoidal categories]], [[symmetric monoidal categories]], [[cartesian monoidal categories]], [[cocartesian monoidal categories]], and [[rig categories]] are all magmoidal categories. 

Every [[magma]] is a [[discrete category|discrete]] magmoidal category. 

An [[Ackermann groupoid]] is a particular sort of [[poset]] that is magmoidal (where 'groupoid' is here a synonym for '[[magma]]').

## Related concepts

* [[magma]]

* [[magmoidal groupoid]]

* [[categorification]]

* [[magmoid]]

* [[residual]]

## References

* [[David Michael Roberts]], *Substructural fixed-point theorems and the diagonal argument: theme and variations*, Compositionality **5** issue 8 (2023) doi:[10.32408/compositionality-5-8](https://doi.org/10.32408/compositionality-5-8),
([arXiv:2110.00239](https://arxiv.org/abs/2110.00239)).

The concept seems to first be named in:

* [[Alexei Davydov]], _Nuclei of categories with tensor products_, Theory and Applications of Categories, Vol. 18, 2007, No. 16, pp 440-472. [tac:18-16](http://www.tac.mta.ca/tac/volumes/18/16/18-16abs.html)

The terminology __magmal category__ first appears in:

* [[Ross Street]], _Wood fusion for magmal comonads_, [arXiv:2311.07088](https://arxiv.org/abs/2311.07088) (2023).

[[!redirects magmoidal categories]]
[[!redirects magmal category]]
[[!redirects magmal categories]]




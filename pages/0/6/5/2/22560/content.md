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

A __magmoidal category__ is a [[category]] $C$ with a [[functor]] 

$$\otimes: C \times C \to C$$ 

from the [[product category]] of $C$ with itself. 

If there is a specified object $I$, and natural isomorphisms $\lambda_A:\colon A\otimes I\stackrel{\simeq}{\to} A$ and $\rho_A:\colon I\otimes A\stackrel{\simeq}{\to} A$, then it is a **magmoidal category with unit**.


## Examples

For example, [[monoidal categories]] such as [[braided monoidal categories]], [[symmetric monoidal categories]], [[cartesian monoidal categories]], [[cocartesian monoidal categories]], and [[rig categories]] are all magma categories. 

An [[Ackermann groupoid]] is a particular sort of [[poset]] that is magmoidal (where 'groupoid' is here a synonym for '[[magma]]').

## Related concepts

* [[magma]]

* [[categorification]]

* [[magmoid]]

## Reference

The concept seems to first be named in

* [[Alexei Davydov]], _Nuclei of categories with tensor products_, Theory and Applications of Categories, Vol. 18, 2007, No. 16, pp 440-472. [journal page](http://www.tac.mta.ca/tac/volumes/18/16/18-16abs.html)

[[!redirects magmoids]]
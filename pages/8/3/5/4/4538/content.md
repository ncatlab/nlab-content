
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $C_\bullet$ a [[chain complex]] (of [[abelian group]]s) and $F$ a [[field]] the [[homology group]] $H_p(C,F)$ and the [[cohomomology group]] $H^p(C,F)$ are related simply by dualization

$$
  H^p(C,F) \simeq Hom_F(H_p(C,F), F)
  \,.
$$

If the coefficients is not a [[field]] but an arbitrary [[abelian group]], then this relationship is more complicated and is expressed by the _universal coefficient theorem_ . 

## Statement

Let $C_\bullet$ be a [[chain complex]] of [[free construction|free]] [[abelian group]]s. Let $A$ be an arbitrary [[abelian group]]. Then we have an [[exact sequence]]

$$
  0 \to 
   Ext^1(H_{n-1}(C, \mathbb{Z}), B)
   \to 
   H^n(C, B) 
   \to 
   Hom(H_n(C,\mathbb{Z}), B)
   \to 
   0
  \,,
$$

where on the left we have the first [[Ext group]].

## References

The note

* Adam Clay, _The universal coefficient theorems and K&#252;nneth formulas_ ([pdf](http://www.math.ubc.ca/~aclay/Algtopology.pdf))

surveys and spells out statement and proof of the theorem.

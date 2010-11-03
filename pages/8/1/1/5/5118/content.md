
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


## Definition

For $C$ and $D$ [[monoidal model categories]], a **lax monoidal Quillen adjunction**

$$
  (L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
  D
$$

is

* a [[Quillen adjunction]] $(L \dashv R)$ between the underlying [[model categories]];

* equipped with the structure of a [[lax monoidal functor]] on $R$ with respect to the underlying [[monoidal categories]]

* such that the induced structure of an [[oplax monoidal functor]] on $L$ satisfies:

  1. for all cofibrant objects $x,y \in D$ the oplax monoidal transformation

     $$
       L(x \otimes y) \to L(x) \otimes L(y)
     $$

     is a weak equivalence in $C$    

  1. for some (hence any) cofibrant [[resolution]] $q : \hat I_D \stackrel{\simeq}{\to} I_D$ of the monoidal unit object in $D$, the composite

     $$
       L(\hat I_D) \stackrel{L(q)}{\to} L(I_D) \to I_C
     $$

     is a weak equivalence in $C$.

This is called a **strong monoidal Quillen adjunction** if $L$ is a [[strong monoidal functor]]. 

## Related concepts

* [[Quillen adjunction]]

* [[Quillen equivalence]]

* **monoidal Quillen adjunction**

## References

The notion of strong monoidal Quillen adjunction is def. 4.2.16 in 

* Hovey, _Model categories_

The lax monoidal version is considered as definition 3.6 of 

* [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342))
{#SchwedeShipley}


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
* table of contents
{:toc}

## Definition

Let $C : sAb \to Ch_\bullet^+$ be the chains/[[Moore complex]] functor of the [[Dold-Kan correspondence]].

Let $(sAb, \otmes)$ be the standard [[monoidal category]] structure given degreewise by the [[tensor product]] on [[Ab]] and let $(Ch_\bullet^+, \otimes)$ be the standard monoidal structure on the [[category of chain complexes]].

For $A,B \in sAb$ two abelian [[simplicial group]]s, the **Alexander-Whitney map** is the [[natural transformation]] on [[chain complex]]es

$$
  \Delta_{A,B} :  C(A \otimes B) \to C(A) \otimes C(B)
$$

defined on two $n$-simplices $a \in A_n$ and $b \in $b \in B_n$ by

$$
  \Delta_{A,B} : a \otimes b \mapsto \oplus_{p + q = n} \tilde (d^p a) \otimes (d^q_0 b)
  \,,
$$

where (...)

This restricts to the normalized chains complex

$$
  \Delta_{A,B} :  N(A \otimes B) \to N(A) \otimes N(B)
  \,.
$$


## Properties

The Alexander-Whitney map is an [[oplax monoidal transformation]] that makes $C$ and $N$ into [[oplax monoidal functor]]s. For details see [[monoidal Dold-Kan correspondence]].

On normalized chain complexes the AW map has a [[right inverse]], given by the [[Eilenberg-Zilber map]] $\nabla_{A,B}$:

$$
  Id 
  :
  N A \otimes N B \stackrel{\nabla_{A,B}}{\to} N(A \otimes B)
  \stackrel{\Delta_{A,B}}{\to}
  N A \otimes N B
  \,.
$$

The AW map is _not_ [[symmetric monoidal category|symmetric]].

## Related concepts

* **Alexander-Whitney map**

* [[Eilenberg-Zilber map]]


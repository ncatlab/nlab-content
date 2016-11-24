+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Given a [[field]] $k$, $SVect_k$ is the [[symmetric monoidal category]] of [[super vector space]]s over $k$. This is the [[category]] of $\mathbb{Z}_2$-[[graded vector space]]s equipped with the unique non-trivial symmetric [[braided monoidal category|braided monoidal structure]]. If the field $k$ is understood, one often just writes $SVect$.

Objects in $SVect$ are vector spaces with a [[direct sum]] decomposition

$$
  V = V_{even} \oplus V_{odd}
$$

and the [[tensor product]] is given in terms of that on vector spaces by

$$
  V \otimes W = 
  (V_{even} \otimes W_{even} \oplus V_{odd}\otimes W_{odd})
  \oplus
  (V_{even} \otimes W_{odd} \oplus V_{odd} \otimes W_{even})
$$

but equipped with the non-trivial braiding morphism

$$
  b_{V, W} : V \otimes W \to W \otimes V
$$

that is the usual braiding isomorphism of [[Vect]] on $V_{even} \otimes W_{even}$ and on $V_{even} \otimes W_{odd} \oplus V_{odd} \otimes W_{even}$ but is $(-1)$ times this on $V_{odd}\otimes W_{odd}$.

##Related entries

* [[Vect]]
* [[super algebra]]

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

For $V$ an [[inner product space]], the **symbol map** constitutes an [[isomorphism]] of [[super vector spaces]] between the [[Clifford algebra]] of $V$ and the [[exterior algebra]] on $V$.

## Definition

Let $V$ be an [[inner product space]]. Write $Cl(V)$ for its [[Clifford algebra]] and $\wedge^\bullet V$ for its [[Grassmann algebra]]. 

For $v \in V$ any vector, write

$$
  v\wedge : \wedge^\bullet V \to \wedge^\bullet V
$$

for the [[linear map]] given by exterior product with $v$.

Let 

$$
  \langle -,-\rangle : \wedge^\bullet V \otimes \wedge^\bullet V \to \mathbb{R}
$$

be the [[Hodge inner product]] on the [[exterior algebra]] induced from the inner product. With respect to this inner product the above multiplication operator has an [[adjoint operator]]

$$
  \iota_v : \wedge^\bullet V \to \wedge^\bullet V
$$

called _contraction_ with $V$. These operators satisfy the [[canonical anticommutation relations]]

$$
  [v\wedge, w\wedge ] = 0
$$

$$
 [\iota_v, \iota_w] = 0
$$

$$
  [\iota_v, w\wedge] = \langle v,w\rangle
$$

(where all these are [[supercommutators]], hence in fact [[anticommutators]] in the present case).

There is a canonical [[representation]] of the [[Clifford algebra]] on the exterior algebra induced by this construction

$$
  \rho : Cl(V)\otimes \wedge^\bullet V \to \wedge^\bullet V
$$

given by

$$
  (\gamma_v, \phi) \mapsto (v \wedge + \iota_v) \phi
  \,.
$$

The **symbol map** is the restriction of this action to the identity element $1 \in \wedge^\bullet V$:

$$
  \sigma := \rho(-,1) : Cl(V) \to \wedge^\bullet V
  \,.
$$

This is an [[isomorphism]] of $\mathbb{Z}_2$-[[graded vector space]]. 

The [[inverse]] maps is on even-graded elements given by sending [[bivector]]s to their Clifford incarnation

$$
  \sigma^{-1} : v \wedge w \mapsto \frac{1}{2}\left(\gamma_v \cdot \gamma_w - \gamma_w \cdot \gamma_v\right)
  \,.
$$

## Related concepts

* The symbol map may be thought of as a special case of a _[[symbol of a differential operator]]_. See there for more.

## References

For instance section 2.5 of 

* [[Eckhard Meinrenken]], _Clifford algebras and Lie groups_ ([pdf](https://sites.icmc.usp.br/grossi/other/meinrenken.pdf))
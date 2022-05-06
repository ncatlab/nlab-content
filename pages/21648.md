
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

By $SL(2,\mathbb{H})$ one denotes the [[special linear group]] of $2 \times 2$ [[matrices]] with [[coefficients]] in the [[quaternions]], where "special" refers to their [[Dieudonné determinant]] being unity:

$$
  SL(2,\mathbb{H})
  \;:=\;
  \left\{
     \left.
     \left[
       \array{
         a & b 
         \\
         c & d 
       }
     \right]
     \;\right\vert\;
     \left\Vert
       a d - a c a^{-1} b
     \right\Vert
     \;=\;
     1
  \right\}
$$

(here $\left\Vert q\right\Vert^2 \;:=\; q \bar q \in \mathbb{R}$ is the [[norm]](-square) on [[quaternions]]).

## Properties

### Relation to $Sp(2)$
 {#RelationToSp2}

Every quaternionic [[unitary matrix]] (hence in [[Sp(2)]]) happens to have unit [[Dieudonné determinant]] ([Cohen-De Leo 99, Cor. 6.4](Dieudonne+determinant#CohenDeLeo99)). Therefore we have a [[subgroup]] inclusion

$$
  Sp(2)
  \;=\;
  U(2,\mathbb{H})
  \;\subset\;
  SL(2,\mathbb{H})
  \,.
$$

### Relation to $Spin(5,1)$
 {#RelationToSpin51}

Under [[conjugation action]] on $2 \times 2$ [[Hermitian matrices]] with [[coefficients]] in the [[quaternions]], $SL(2,\mathbb{H})$ is identified with [[Spin(5,1)]] and its canonical [[action]] on [[Minkowski spacetime]] $\mathbb{R}^{5,1}$.

For more on this see at _[[spin representation]]_, _[[supersymmetry and division algebras]]_ and _[[geometry of physics -- supersymmetry]]_.



## Related concepts

[[!include exceptional spinors and division algebras -- table]]

## References

* [[Joás Venâncio]], [[Carlos Batista]], Sections 2,3 of: _Two-Component Spinorial Formalism using Quaternions for Six-dimensional Spacetimes_ ([arXiv:2007.04296](https://arxiv.org/abs/2007.04296))


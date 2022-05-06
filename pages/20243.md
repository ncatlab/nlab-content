
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[Lie group]] denoted $Sp(n).Sp(1)$ or just $Sp(n)Sp(1)$ is the [[quotient group]] of the given [[quaternion unitary groups]] by their [[diagonal]] [[center]] [[cyclic group of order 2]].

A [[smooth manifold]] of [[dimension]] $4n$ with [[G-structure]] for this group $G = Sp(n).Sp(1)$ is a [[quaternion-Kähler manifold]].

## Definition

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$ with $n \geq 2$, the [[Lie group]] denoted $Sp(n).Sp(1)$ or just $Sp(n)Sp(1)$ is the [[quotient group]] of the [[direct product group]] $Sp(n) \times Sp(1)$ of [[quaternion unitary groups]] $Sp(n)$ (in particular $Sp(1) \simeq$ [[Spin(3)]]) by the [[diagonal]] [[center]] [[cyclic group of order 2]] $\mathbb{Z}_2$:

$$
  Sp(n).Sp(1)
  \;\coloneqq\;
  \big(
    Sp(n)
     \times
    Sp(1)
  \big)/_{diag}\mathbb{Z}_2
$$

hence the [[quotient group]] by the [[subgroup]]

\[
  \label{DiagonalCenter}
  \mathbb{Z}_2
  \;\simeq\;
  \big\{ 
    (1,1), (-1,-1)
  \big\}
  \hookrightarrow
  Sp(n) \times Sp(1)
  \,.
\]

=--

## Properties

### As the effective quotient of $Sp(n)\times Sp(1)$ acting on $\mathbb{H}^n$ 

The [[direct product group]] $Sp(n) \times Sp(1)$ has a canonical [[action]] on the [[quaternion]] [[vector space]] $\mathbb{H}^n$, where the factor [[Sp(n)]] acts as $2 \times 2$ [[quaternion unitary group|quaternion unitary]] [[matrix multiplication]] from the left, and $Sp(1)$ acts by [[diagonal]] $1 \times 1$ matrix action on each $\mathbb{H}$-summand from the right.

For instance for $n = 2$ this action controls the [[quaternionic Hopf fibration]] and its $Sp(2)$ [[equivariant function|equivariance]] (see [there](quaternionic+Hopf+fibration#EquivariantStructure)).

But this action is not an [[effective group action]]: Precisely the diagonal center (eq:DiagonalCenter) acts trivially.

## References

See the references at _[[quaternion-Kähler manifold]]_.

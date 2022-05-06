
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

(e.g. [Čadek-Vanžura 97, Sec. 2](#CadekVanzura97))

## Properties

### As the effective quotient of $Sp(n)\times Sp(1)$ acting on $\mathbb{H}^n$ 

The [[direct product group]] $Sp(n) \times Sp(1)$ has a canonical [[action]] on the [[quaternion]] [[vector space]] $\mathbb{H}^n$, where the factor [[Sp(n)]] acts as $2 \times 2$ [[quaternion unitary group|quaternion unitary]] [[matrix multiplication]] from the left, and $Sp(1)$ acts by [[diagonal]] $1 \times 1$ matrix action on each $\mathbb{H}$-summand from the right.

For instance for $n = 2$ this action controls the [[quaternionic Hopf fibration]] and its $Sp(2)$ [[equivariant function|equivariance]] (see [there](quaternionic+Hopf+fibration#EquivariantStructure)).

But this action is not an [[effective group action]]: Precisely the diagonal center (eq:DiagonalCenter) acts trivially.

There is then a [[commuting diagram]] of [[Lie groups]]

$$
  \array{
    Sp(2) \times Sp(1)
    &\longrightarrow&
    Spin(8)
    \\
    \big\downarrow && \big\downarrow
    \\
    Sp(2) \cdot Sp(1)    
    &\longrightarrow&
    SO(8)
  }
$$
with the horizontal maps being [[group homomorphisms]] to [[Spin(8)]] and [[SO(8)]], respectively, the left morphism being the defining [[quotient]] projection and the right morphism the [[double cover]] morphism that defines the [[spin group]].

(e.g. [Čadek-Vanžura 97, p. 4](#CadekVanzura97))

 
## References

* {#CadekVanzura97} [[Martin Čadek]], Jiří Vanžura, Section 2 of _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))



See also the references at _[[quaternion-Kähler manifold]]_.

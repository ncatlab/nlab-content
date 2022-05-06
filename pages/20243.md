
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

The [[Lie group]] denoted $Sp(n).Sp(1)$ or just $Sp(n)Sp(1)$ is the [[quotient group]] of the [[direct product group]] of the given [[quaternion unitary groups]] by their [[diagonal]] [[center]] [[cyclic group of order 2]].

A [[smooth manifold]] of [[dimension]] $4n$ with [[G-structure]] for this group $G = Sp(n).Sp(1)$ is a [[quaternion-Kähler manifold]].

Similarly, for $Spin(n_1)$, $Spin(n_2)$ [[spin groups]] in some dimension, the group denoted $Spin(n_1) \cdot Spin(n_2)$ or just $Spin(n_1)Spin(n_2)$ is the [[quotient group]] of the [[direct product group]] $Spin(n_1) \times Spin(n_2)$ by the [[diagonal]] [[center]] [[cyclic group of order 2]].

\linebreak

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

\[
  \label{CompatibilityDiagram}
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
\]
with the horizontal maps being [[group homomorphisms]] to [[Spin(8)]] and [[SO(8)]], respectively, the left morphism being the defining [[quotient]] projection and the right morphism the [[double cover]] morphism that defines the [[spin group]].

(e.g. [Čadek-Vanžura 97, p. 4](#CadekVanzura97))

## Examples

### $n = 1$, the group $SO(4)$

The case of $Sp(n)\cdot Sp(1)$ for $n = 1$ is special, as in this case the canonical inclusion $Sp(n)\cdot Sp(1) \hookrightarrow SO(4n)$ becomes an [[isomorphism]]

$$
  Sp(1)\cdot Sp(1)
  \;\simeq\;
  SO(4)
$$

with the [[special orthogonal group]] [[SO(4)]],
and hence the compatibility diagram (eq:CompatibilityDiagram) now exhibits at the top the exceptional isomorphism $Sp(1) \times Sp(1) \simeq $ [[Spin(4)]] (see [there](Spin4#ExceptionalIsomorphisms))

In summary:


+-- {: .num_prop }
###### Proposition

There is a [[commuting diagram]] of [[Lie groups]] of the form

$$
  \array{
    ( q_1, q_2 )
    &\mapsto&
    (x \mapsto q_1 \cdot x \cdot \overline{q}_2) 
    \\
    Sp(1) \times Sp(1) 
    &\overset{\simeq}{\longrightarrow}&
    Spin(4)
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    Sp(1)\cdot Sp(1)
    &\overset{\simeq}{\longrightarrow}&
    SO(4)
  }
$$

where

1. in the top left we have [[Sp(1)]] = [[Spin(3)]],

1. in the top right we have [[Spin(4)]],

1. in the bottom left we have [[Sp(n).Sp(1)|Sp(1).Sp(1)]]

1. in the bottom right we have [[SO(4)]]

1. the horizontal morphism assigns the [[conjugation action]] of unit [[quaternions]], as indicated,

1. the right vertical morphism is the defining [[double cover]],

1. the left vertical morphism is the defining [[quotient group]]-projection.

=--


\linebreak


## Related concepts

[[!include low dimensional rotation groups -- table]]

 
## References

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], Section 2 of _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))

* {#CadekVanzura98b} [[Martin Čadek]], [[Jiří Vanžura]], _Almost quaternionic structures on eight-manifolds_, Osaka J. Math. Volume 35, Number 1 (1998), 165-190 ([euclid:1200787905](https://projecteuclid.org/euclid.ojm/1200787905))

See also the references at _[[quaternion-Kähler manifold]]_.

The group $Spin(4)\cdot Spin(3)$ appears in 

* {#Kerr96} Megan M. Kerr, Lemma 6.2 of _Some New Homogeneous Einstein Metrics on Symmetric Spaces_, Transactions of the American Mathematical Society, Vol. 348, No. 1 (1996), pp. 153-171 ([jstor:2155169](https://www.jstor.org/stable/2155169))

* {#KacSmilga00} [[Victor Kac]], A.V. Smilga, around (1.10) in _Vacuum structure in supersymmetric Yang-Mills theories with any gauge group_, in _The Many Faces of the Superworld, pp. 185-234 (2000)_ ([arXiv:hep-th/9902029](https://arxiv.org/abs/hep-th/9902029), [doi:10.1142/9789812793850_0014](https://doi.org/10.1142/9789812793850_0014))

* {#GroveWilkingZiller} Karsten Grove, Burkhard Wilking, Wolfgang Ziller, p. 30 of _Positively Curved Cohomogeneity One Manifolds and 3-Sasakian Geometry_ ([arXiv:math/0511464](https://arxiv.org/abs/math/0511464))

[[!redirects Sp(2).Sp(1)]]

[[!redirects Spn.Sp1]]

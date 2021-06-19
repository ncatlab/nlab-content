
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

The [[special orthogonal group]] in [[dimension]] 4.

## Properties

### Exceptional isomorphisms

+-- {: .num_prop #TheExceptionalIso}
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


### Cohomology

+-- {: .num_prop}
###### Proposition

The [[integral cohomology]] [[cohomology ring|ring]] of the [[classifying space]] $B SO(4)$ is

$$
  H^\bullet
  \big(
    p_1, \chi, W_3
  \big)
  /
  \big( 
    2 W_3
  \big)
$$

where 

* $p_1$ is the [[first Pontryagin class]]

* $\chi$ is the [[Euler class]],

* $W_3$ is the [[integral Stiefel-Whitney class]].

Notice that the [[cup product]] of the [[Euler class]] with itself is the [[second Pontryagin class]]

$$
  \chi \smile \chi \;=\; p_2
  \,,
$$

which therefore, while present, does not appear as a separate generator.

=--

This is a special case of [Brown 82, Theorem 1.5](#Brown82), reviewed for instance as [Rudolph-Schmidt 17, Thm. 4.2.23 with Rmk. 4.2.25](#RudolphSchmidt17).

\linebreak

### Homotopy groups

The [[homotopy groups]] of $SO(4)$ in [[low-dimensional topology|low degrees]] are


| $G$ | $\pi_1$ | $\pi_2$ | $\pi_3$ | $\pi_4$ | $\pi_5$ | $\pi_6$ | $\pi_7$ | $\pi_8$ | $\pi_9$ | $\pi_10$ | $\pi_11$ | $\pi_12$ | $\pi_13$ | $\pi_14$ | $\pi_15$ |
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $SO(4)$ | $\mathbb{Z}_2$ | 0 | $\mathbb{Z}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{12}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{2}^{\oplus 2}$ | $\mathbb{Z}_{3}^{\oplus 2}$ | $\mathbb{Z}_{15}^{\oplus 2}$|$\mathbb{Z}_{2}^{\oplus 2}$ |$\mathbb{Z}_{2}^{\oplus 4}$  | $\mathbb{Z}_2^{\oplus 2}\oplus\mathbb{Z}_{12}^{\oplus 2}$ | $\mathbb{Z}_2^{\oplus 4}\oplus\mathbb{Z}_{84}^{\oplus 2}$ | $\mathbb{Z}_2^{\oplus 4}$ | 

\linebreak

## Related concepts

[[!include low dimensional rotation groups -- table]]


## References

* {#Berger87} [[Marcel Berger]], Section 8.9.8 of: *Geometry I*, Springer 1987 ([doi:10.1007/978-3-540-93815-6](https://doi.org/10.1007/978-3-540-93815-6))


* Jason Hanson, _Rotations in three, four, and five dimensions_ ([arXiv:1103.5263](https://arxiv.org/abs/1103.5263))


See also

* Wikipedia, _[Rotations in 4-dimensional Euclidean space](https://en.wikipedia.org/wiki/Rotations_in_4-dimensional_Euclidean_space)_

On the [[integral cohomology]] of the [[classifying space]]:

* {#Brown82} [[Edgar H. Brown]], _The Cohomology of $B SO_n$ and $BO_n$ with Integer Coefficients_, Proceedings of the American Mathematical Society, Vol. 85, No. 2 (Jun., 1982), pp. 283-288 ([jstor:2044298](https://www.jstor.org/stable/2044298))

reviewed in 

* {#RudolphSchmidt17} Gerd Rudolph, Matthias Schmidt, around Theorem 4.2.23 of _Differential Geometry and Mathematical Physics: Part II. Fibre Bundles, Topology and Gauge Fields_, Theoretical and Mathematical Physics series, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))


[[!redirects SO4]]

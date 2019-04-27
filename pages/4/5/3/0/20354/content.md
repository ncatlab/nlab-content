
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[group theory]], but particularly in [[Lie group]]-[[Lie theory|theory]], the term "biquotient" tends to mean the [[quotient space]] of a [[topological group]] or [[Lie group]] $G$ by the [[action]] of _two_ [[subgroups]] $H_1, H_2 \subset G$, hence by the action of their [[direct product group]] $H_1 \times H_2$, one factor regarded as [[action|acting]] by group multiplication from the left, the other (more precisely: its [opposite](opposite+category#OppositeGroup)) acting by multiplication from the right. 

This is typically and suggestively denoted as

$$
  H_1 \backslash G / H_2
  \;\coloneqq\;
  G/( H_1 \times H_2^{op} )
  \;\coloneqq\;
  G/( g \sim h_1 \cdot g \cdot h_2 \vert h_i \in H_i )
  \,.
$$

Another way to think of a biquotient is as a [[double coset space]], see there for more.

Typically extra conditions are imposed on $H_1, H_2 \subset G$, such as that $H_i \subset G$ are [[closed subspaces|closed]] [[subgroups]] and notably that the induced action of $H_1$ on the single [[quotient space]]/[[coset space]] $G/H_2$ of the other, is still [[free action|free]]. 

More generally, one can consider biquotients of $G$ by [[subgroups]] of the [[direct product group]] (e.g. [Kapovitch](#Kapovitch)).

## Examples

### Gromoll-Meyer sphere

The [[Gromoll-Meyer sphere]] -- an [[exotic 7-sphere]] -- arises as the [[biquotient]] of [[Sp(2)]] by two copies of [[Sp(1)]].


## References

For instance: 

* Burt Totaro, _Cheeger manifolds and the classification of biquotients_ ([arXiv:math/0210247](https://arxiv.org/abs/math/0210247))

In [[rational homotopy theory]]:

* {#Kapovitch} Vitali Kapovitch, _A note on rational homotopy of biquotients_ ([pdf](http://www.math.utoronto.ca/vtk/biquotient.pdf))


[[!redirects biquotients]]

[[!redirects biquotient space]]
[[!redirects biquotient spaces]]

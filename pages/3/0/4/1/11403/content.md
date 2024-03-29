
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Eisenstein series_ $G_{2k}$ for $k \geq 2$ are [[series]]  expressions for certain [[modular forms]].

They appear as the coefficients of the [[exponential series]]-expression of the [[Weierstrass sigma-function]], and hence of the [[Hirzebruch series]] of the [[Witten genus]].

Moreover, a combination of $G_2$ and $G_4$ expresses the [[j-invariant]] which characterizes [[elliptic curves]].

## Definition

$$
  G_{2k}(\tau)
   \coloneqq
  \underset{(m,n) \in \mathbb{Z}^2\backslash (0,0)}{\sum}
  \frac{1}{(m+n \tau)^{2k}}
  \,.
$$

## Properties

### Relation to the $j$-invariant
 {#RelationToJInvariant}

With

$$
  g_2 \coloneqq 60 G_4
$$

$$
  g_3 \coloneqq 140 G_6
$$

$$
  \Delta \coloneqq g_2^3 - 27 g_3^2
$$

the [[j-invariant]] is

$$
  j = 1728 \frac{g_2^3}{\Delta}
  \,.
$$

### Relation to Weierstrass $\sigma$-function and Witten genus
 {#RelationToWeierstrassFunctionAndWittenGenus}

$$
  \frac{x}{e^{x/2} - e^{-x/2}}
  \prod_{n\geq 1}
  \frac{(1-q^n)^2}{(1-q^n e^x)(1-q^n e^{-x})}
  =
  \exp\left(
    \sum_{k \geq 2} 2 G_k \frac{x^k}{k!}
  \right)
$$

([Ando-Hopkins-Rezk 10, prop. 10.9](#AndoHopkinsRezk10))


### Relation to Bernoulli numbers

The $q$-independent term in $G_{k}$ is proportional to the $k$th [[Bernoulli number]] $B_k$

$$
  G_k = - \frac{B_k}{2k} + \sum_{n= 1}^\infty \sigma_{k-1}(n)q^n
  \,,
$$

where

$$
  \sigma_{k-1}(n) =  \sum_{d|n} d^{k-1}
  \,.
$$

Reducing to this constant term reduces the [above](#RelationToWeierstrassFunctionAndWittenGenus) exponential characteristic series for the [[Witten genus]] to that of the [[A-hat genus]].

## References

* Wikipedia, _[Eisenstein series](https://en.wikipedia.org/wiki/Eisenstein_series)_

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))
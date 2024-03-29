
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

A [[modular form]].

## Properties

### Relation to Eisenstein series

Let $G_{2k}$ be the [[Eisenstein series]], then

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


## Related concepts

* The Weierstrass $\sigma$-function is proportional to the (inverse of the) characteristic series of the [[Witten genus]] ([Ando-Basterra 00, section 5.1](#AndoBasterra00))


## References

Named after [[Karl Weierstrass]].

An introductory review is in 

* {#Hain08} Richard Hain, section 5.1 of _Lectures on Moduli Spaces of Elliptic Curves_ ([arXiv:0812.1803](http://arxiv.org/abs/0812.1803))


A textbook account includes for instance

* Joseph Silverman, _The arithmetic of elliptic curves_, volume 106 of Graduate Texts in Mathematics. Springer, 1986

Relation to the [[Witten genus]] is discussed for instance in 

* {#AndoBasterra00} [[Matthew Ando]], Maria Basterra, _The Witten genus and equivariant elliptic cohomology_ ([arXiv:0008192](http://arxiv.org/abs/math/0008192))

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

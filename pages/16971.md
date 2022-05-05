
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a $G$-[[equivariant spectrum]], its _fixed point spectrum_ $F^G X$ is the plain [[spectrum]] which is value of the [[derived functor]] of the naive $G$-[[fixed point]] functor on $X$. This constitutes a suitably derived functor

$$
  F^G \;\colon\; G Spectra \longrightarrow Spectra
$$

(e.g. [Schwede 15, def. 7.1](#Schwede15), [Mandell-May 02, arojnd thm. 3.3](#MandellMay02))

More generally, for $N \subset G$ a [[normal subgroup]], there is the $N$-fixed point spectrum regarded as $G/N$-spectrum, equivariant under the  remaining [[quotient group]] $G/N$:

$$
  F^N \;\colon\; G Spectra \longrightarrow G/N Spectra
$$

([Mandell-May 02, def. 3.8](#MandellMay02), [Greenlees-Shipley 11, Prop. 3.3](#GreenleesShipley11))

These are [[right derived functor|derived]] [[right adjoint]] to the operation of regarding a $G/N$-spectrum as a $G$-spectrum, via the projection $G \to G/N$

([Mandell-May 02, theorem 3.12](#MandellMay02), [Greenlees-Shipley 11, Prop. 3.3](#GreenleesShipley11))


## Properties

### Relation to equivariant homotopy groups

The plain [[homotopy groups]] of the $G$-fixed point spectrum of $X$ are the [[equivariant homotopy groups]] of the $G$-spectrum $X$:

$$
  \pi_k(F^G X) \simeq \pi_k^G(X)
$$

(e.g. [Schwede 15, prop. 7.2](#Schwede15))

## Examples

### For equivariant suspension spectra

For $\Sigma^\infty_G X$ an [[equivariant suspension spectrum]] the fixed point spectrum is given by the _[[tom Dieck splitting]]_ formula

$$
  F^G(\Sigma^\infty_G X)
  \simeq
  \underset{[H\subset G]}{\oplus}
  \Sigma^\infty( E W(X)_+ \wedge_{W H} X^H )
  \,.
$$

(e.g. [Schwede 15, example 7.7](#Schwede15))



## Related concepts

* [[fixed point space]]

* [[homotopy fixed points]]

* [[geometric fixed point spectrum]]

* [[categorical fixed point spectrum]]


* [[tom Dieck splitting]]

## References


* {#Lewis00} [[L. Gaunce Lewis, Jr.]], _Splitting theorems for certain equivariant spectra_, Memoirs of the AMS, number 686, March 2000, Volume 144 ([pdf](http://hopf.math.purdue.edu/LewisG/spltspec.pdf))

* {#MandellMay02} [[Michael  Mandell]], [[Peter May]], _Equivariant orthogonal spectra and S-modules_, Mem. Amer. Math. Soc. 159 (2002), no. 755, x+108. MR 2003i:55012 ([pdf](http://www.math.uiuc.edu/K-theory/0408/MMM.pdf), [K-theory archive](http://www.math.uiuc.edu/K-theory/0408/))

* {#GreenleesShipley11} [[John Greenlees]], [[Brooke Shipley]], p. 18 of _An algebraic model for rational torus-equivariant spectra_ ([arXiv:1101.2511](https://arxiv.org/abs/1101.2511))

* {#GreenleesShipley13} [[John Greenlees]], [[Brooke Shipley]], _Fixed point adjunctions for equivariant module spectra_, Algebr. Geom. Topol. 14 (2014) 1779-1799 ([arXiv:1301.5869](https://arxiv.org/abs/1301.5869))

* {#Schwede15} [[Stefan Schwede]], _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))


[[!redirects fixed point spectra]]
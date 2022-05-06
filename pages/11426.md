
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The universal [[Thom spectrum]] (see there for more) of the [[orthogonal group]]. (...) Abstractly, this is the [[homotopy colimit]] of the [[J-homomorphism]] in [[Spectra]]:

$$
  MO = \underset{\rightarrow}{\lim}(B O \stackrel{J}{\to} B GL_1(\mathbb{S}) \to Spectra)
$$

## Properties

### Thom's theorem on $M O$
 {#ThomTheoremOnMO}

By [[Thom's theorem]] the [[stable homotopy groups]] of $M O$ form the [[bordism ring]] of unoriented manifolds

$$
  \pi_\bullet(M O) \simeq \Omega^O_\bullet
  \,.
$$

Moreover, this is the [[polynomial algebra]]

$$
  \pi_\bullet(M O)
  \simeq
  (\mathbb{Z}/2\mathbb{Z})[ x_n \;|\; n \in \mathbb{N}, \,n \geq 2, \, n \neq 2^t-1]
  \,.
$$

Due to ([Thom 54](#Thom54)). See for instance ([Kochmann 96, theorem 3.7.6](#Kochmann96))

The corresponding statement for [[MU]] is considerably more subtle, see _[[Milnor-Quillen theorem on MU]]_.



## Related concepts

* [[homology of MO]]

* [[orientation in generalized cohomology]]


\linebreak

[[!include flavours of cobordism cohomology theories -- table]]


## References

* {#Thom54} [[René Thom]], _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_ Comment. Math. Helv. 28, (1954). 17-86

Review includes

* {#Kochmann96} [[Stanley Kochmann]], section 1.5 and section 3.7 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


* {#Malkiewich11} [[Cary Malkiewich]], section 2 of _Unoriented cobordism and $M O$_, 2011 ([pdf](http://math.uiuc.edu/~cmalkiew/cobordism.pdf))

In the incarnation of $MO$ as a [[symmetric spectrum]] is discussed in

* {#Schwede12} [[Stefan Schwede]], Example I.2.8 in _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf))

In the incarnation as an [[orthogonal spectrum]] (in fact as an [[equivariant spectrum]] in [[global equivariant stable homotopy theory]]):

* [[Stefan Schwede]], chapter V.4 of _[[Global homotopy theory]]_, 2015



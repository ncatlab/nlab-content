
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

Due to ([Thom 54](#Thom54)). See for instance ([Kochman 96, theorem 3.7.6](#Kochman96))

The corresponding statement for [[MU]] is considerably more subtle, see _[[Milnor-Quillen theorem on MU]]_.



## Related concepts

* [[homology of MO]]

* [[orientation in generalized cohomology]]


\linebreak

[[!include flavours of cobordism cohomology theories -- table]]


## References

* {#Thom54} [[René Thom]], _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_ Comment. Math. Helv. 28, (1954). 17-86

* {#Novikov62} [[Sergei Novikov]], _Homotopy properties of Thom complexes_, Mat. Sbornik 57 (1962), no. 4, 407–442, 407&#8211;442 ([pdf](http://www.mi-ras.ru/~snovikov/6.pdf), [[NovikovThomComplexes.pdf:file]])


Textbook accounts:

* {#Stong68} [[Robert Stong]], Chapter VI of: _Notes on Cobordism theory_, Princeton University Press, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [ISBN:9780691649016](http://press.princeton.edu/titles/6465.html), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/stongcob.pdf))


* {#Kochman96} [[Stanley Kochman]], section 1.5 and section 3.7 of: _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

Review:

* {#Malkiewich11} [[Cary Malkiewich]], section 2 of: _Unoriented cobordism and $M O$_, 2011 ([pdf](http://math.uiuc.edu/~cmalkiew/cobordism.pdf))

* [[Branko Juran]], _Thom spaces and the Oriented Cobordism Ring_, 2020 ([pdf](http://www.math.uni-bonn.de/people/daniel/2020/CharClasses/Vortrag4.pdf), [[JuranMO.pdf:file]])

Discussion of [[MO]]-bordism with [[MSO]]-[[manifold with boundary|boundaries]]:

* G. E. Mitchell, _Bordism of Manifolds with Oriented Boundaries_, Proceedings of the American Mathematical Society Vol. 47, No. 1 (Jan., 1975), pp. 208-214 ([doi:10.2307/2040234](https://doi.org/10.2307/2040234))



In the incarnation of $MO$ as a [[symmetric spectrum]]:

* {#Schwede12} [[Stefan Schwede]], Example I.2.8 in _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf))

In the incarnation as an [[orthogonal spectrum]] (in fact as an [[equivariant spectrum]] in [[global equivariant stable homotopy theory]]):

* [[Stefan Schwede]], chapter V.4 of _[[Global homotopy theory]]_, 2015



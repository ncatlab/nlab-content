
#Contents#
* table of contents
{:toc}

## Idea

The _basic line bundle on the 2-sphere_ is the [[complex line bundle]] on the [[2-sphere]] whose [[first Chern class]] is a generator of $H^2(S^2, \mathbb{Z})$.

This is the [[pullback bundle]] of the map $S^2 \to B U(1) \simeq B^2 \mathbb{Z}$ to the [[classifying space]]/[[Eilenberg-MacLane space]] which itself represents a generator of the [[homotopy group]] $\pi_2(S^2) \simeq \mathbb{Z}$.

Beware that this basic line bundle is sometimes called the "canonical line bundle on the 2-sphere", but it is  _not_ [[isomorphism|isomorphuic]] to what in complex geometry is called the [[canonical bundle]] of the 2-sphere regarded as a [[Riemann surface]]. Instead it is "one half" of the latter, its [[theta characteristic]]. See also at _[[geometric quantization of the 2-sphere]]_.

## Properties

Write $h$ for the basic line bundle on the 2-sphere

$h \otimes h \oplus 1 \simeq h \oplus h$

([Hatcher, Example 1.13](#Hatcher))

[[fundamental product theorem in K-theory]]

$$
  K(X)[h]/(h-1)^2 \overset{\simeq}{\longrightarrow} K(X \times S^2)
$$

([Hatcher, theorem 2.2](#Hatcher))

more generally:

$$
  K(X)[h]/((h-1)(l h -1))
   \simeq
  K(P(1 \oplus L))
$$

([Wirthmuller 12, p. 17](#Wirthmuller12))

## References

* {#Hatcher} [[Allen Hatcher]], _Vector bundles and K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* {#Wirthmuller12} [[Klaus Wirthmüller]], _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))


[[!redirects basic line bundles on the 2-sphere]]
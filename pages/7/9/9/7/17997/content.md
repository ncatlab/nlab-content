
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _fundamental product theorem in K-theory_ is a statement relating the [[topological K-theory]]-ring of a [[product topological space]] with the [[2-sphere]] to the K-theory ring of the original space with a generator for the [[basic line bundle on the 2-sphere]] adjoined.

This theorem in particular serves as a substantial step in a [[proof]] of [[Bott periodicity]] for [[topological K-theory]].


## Statement

Write $h$ for the [[basic line bundle on the 2-sphere]]

$h \otimes h \oplus 1 \simeq h \oplus h$

([Hatcher, Example 1.13](#Hatcher))

_fundamental product theorem in K-theory_

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

* {#Hatcher} [[Allen Hatcher]], section 2.1 (from p. 45 on) in _Vector bundles and K-theory_ ([web](https://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 6, from p. 19 on _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))



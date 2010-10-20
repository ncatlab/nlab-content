
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

By **$Toposes$** is denoted the [[category]] of [[topos]]es. Usually this means:

* [[object]]s are [[topos]]es;

* [[morphism]]s are [[geometric morphism]]s of toposes.

This naturally a [[2-category]] with [[2-morphism]]s being [[natural transformation]]s: as such it is the (non-full) [[sub-2-category]] of [[Cat]] on categories that are toposes and morphisms that are geometric morphisms.

There is also the sub-2-category $ShToposes$ of [[sheaf topos]]es. 

## Properties

The operation of forming [[categories of sheaves]]

$$
  Sh(-) : Top \to ShToposes
$$

embeds [[topological space]]s into toposes. For $f : X \to Y$ a [[continuous map]] we have that $Sh(f)$ is the [[geometric morphism]]

$$
  Sh(f) : Sh(X) \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  Sh(Y)
$$

with 

* $f_$ the [[direct image]]

* and $f^*$ the [[inverse image]].

The [[terminal object]] in $ShToposes$ is the topos set [[Set]] $\simeq Sh(*)$.



category: category
---
Some standard references are in folder AG/Topos theory

[What is a topos, by Illusie](http://www.ams.org/notices/200409/what-is-illusie.pdf)

Many more references on [Wikipedia](http://en.wikipedia.org/wiki/Topos_theory)

Caramello: [The unification of Mathematics via Topos Theory](http://front.math.ucdavis.edu/1006.3930) (see also other things by Caramello on her webpage)


[Joyal and Moerdijk](http://www.jstor.org/pss/2374854): Toposes are Cohomologically Equivalent to Spaces (1990)

[nLab](http://ncatlab.org/nlab/show/topos)

[nLab](http://www.ncatlab.org/nlab/show/quasitopos) quasi-topos

&lt;http://www.ncatlab.org/nlab/show/cosmos>

[nLab list of entries related to topos theory](http://ncatlab.org/nlab/show/sheaf+and+topos+theory)

&lt;http://www.ncatlab.org/nlab/show/classifying+topos>

&lt;http://ncatlab.org/nlab/show/natural+numbers+object>

&lt;http://ncatlab.org/nlab/show/Sheaves+in+Geometry+and+Logic>

&lt;http://www.ncatlab.org/nlab/show/geometric+morphism>

Toposes Triples Theories, by Barr and Wells, in Homol alg folder

Borceux vol 3 maybe.

nLab page on [[nlab:Topos]]

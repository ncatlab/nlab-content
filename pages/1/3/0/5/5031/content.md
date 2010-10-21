
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

By __$Topos$__ (or __$Toposes$__) is denoted the [[category]] of [[topos]]es. Usually this means:

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

* $f_*$ the [[direct image]]

* and $f^*$ the [[inverse image]].

The [[terminal object]] in $ShToposes$ is the topos set [[Set]] $\simeq Sh(*)$.


category: category

[[!redirects Topos]]
[[!redirects Topoi]]
[[!redirects Toposes]]

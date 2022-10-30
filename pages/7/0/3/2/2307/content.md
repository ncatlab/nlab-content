

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[cobordism theory]], the [[cohomology theory]] [[Brown representability theorem|represented]] by a [[Thom spectrum]] is called a _cobordism cohomology theory_.


## Definition

### As represented by a spectrum

_Cobordism cohomology theory_, denoted [[MO]] for _oriented cobordism cohomology_ , [[MU]] for _complex cobordism cohomology_  etc, is the [[generalized (Eilenberg-Steenrod) cohomology]] theory represented by the universal [[Thom spectrum]].

This spectrum, also denoted $M U$
is the [[spectrum]] is in degree $2 n$ given by the [[Thom space]] of the [[vector bundle]] that is  [[associated bundle|associated]] by the defining [[representation]] of the [[unitary group]] $U(n)$ on $\mathbb{C}^n$ to the [[generalized universal bundle|universtal]] $U(n)$-[[principal bundle]]:

$$
  M U(2n) = Thom
  \left(
    standard\;associated\;bundle\;to\;universal\;bundle
    \array{
      E U(n) \\ \downarrow \\ B U(n)
    }
  \right)
$$


The _periodic_ complex cobordism theory is given by adding up all the even degree powers of this theory:

$$
  M P = \vee_{n \in \mathbb{Z}} \Sigma^{2 n} M U
$$

There is a canonical [[oriented cohomology theory|orientation]] on this obtained from the map

$$
  \omega : \mathbb{C}P^\infty \stackrel{\simeq}{\to}
  M U(1)
  \;\;\;\;
  M U(\mathbb{C}P^\infty)
$$

(???)

this is the universal even periodic cohomology theory with orientation

The [[cohomology ring]] $M P({*})$ is the [[Lazard ring]] which is the universal coefficient ring for [[formal group law]]s.

The [[periodic cohomology theory|periodic]] version is sometimes written $PMU$.

### Homology groups

For $X$ a [[manifold]], the [[group]] $MU_\ast(X)$ is the group of equivalence classes of maps $\Sigma \to X$ from manifolds $\Sigma$ with [[complex structure]] on the stable [[normal bundle]], modulo suitable complex [[cobordisms]].

e.g ([Ravenel chapter 1, section 2](#Ravenel))

(...)


### Differential cohomology refinement

The refinement of cobordism cohomology theory to [[differential cohomology]] is [[differential cobordism cohomology]].

## Properties

### On the point: Cobordism and Lazard ring

The [[graded ring]] given by evaluating complex cobordism theory on the point is both the complex [[cobordism ring]] as well as the [[Lazard ring]] classifying [[formal group laws]].

+-- {: .num_theorem #RelationToCobordismRing}
###### Theorem

Evaluation of $MU$ on the point yields the complex [[cobordism ring]], whose underlying group is

$$
  \pi_\ast MU \simeq MU_\ast(pt) \simeq \mathbb{Z}[x_1, x_2, \cdots]
  \,,
$$

where the generator $x_i$ is in degree $2 i$.

=--

This is due to ([Milnor 60](#Milnor60), [Novikov 60](#Novikov60), [Novikov 62](#Novikov62)). A review is in ([Ravenel theorem 1.2.18](#Ravenel), [Ravenel, ch. 3, theorem 3.1.5](#Ravenel)).


The [[formal group law]] associated with $MU$ as with any [[complex oriented cohomology theory]] is classified by a [[ring]] [[homomorphism]] $L \longrightarrow \pi_\bullet(MU)$ out of the [[Lazard ring]].

+-- {: .num_theorem}
###### Theorem

This canonical [[homomorphism]] is an [[isomorphism]]

$$
  L \stackrel{\simeq}{\longrightarrow} \pi_\bullet(MU)
$$

between the [[Lazard ring]] and the $MU$-[[cohomology ring]], hence by theorem \ref{RelationToCobordismRing} with the complex [[cobordism ring]].

=--

This is [[Quillen's theorem on MU]].
(e.g [Lurie 10, lect. 7, theorem 1](#LurieLect7))


### On itself: Hopf algebroid structure on dual Steenrod algebra

Moreover, the dual $MU$-[[Steenrod algebra]] $MU_\bullet(MU)$
forms a [[commutative Hopf algebroid]] over the [[Lazard ring]]. 
This is the content of the _[[Landweber-Novikov theorem]]_.

### Universal complex orientation
 {#UniversalComplexOrientation}


For $E$ an [[E-infinity ring]] there is a [[bijection]] between [[complex oriented cohomology theory|complex orientation]] of $E$ and [[E-infinity ring]] maps of the form

$$
  MU \longrightarrow E
  \,.
$$

(e.g [Lurie 10, lect. 6, theorem 8](#LurieLect6), [Ravenel, chapter 4, lemma 4.1.13](#Ravenel))

See also at _[[complex orientation and MU]]_.

### Nilpotence theorem

* [[nilpotence theorem]]

### Snaith's theorem

[[Snaith's theorem]] asserts that the [[periodic complex cobordism spectrum]] is the [[∞-group ∞-ring]] of the [[classifying space]] for stable [[complex vector bundles]] (the classifying space for [[topological K-theory]]) localized at the [[Bott element]] $\beta$:

$$
  PMU \simeq \mathbb{S}[B U][\beta^{-1}]
  \,.
$$

### $p$-Localization and Brown-Peterson spectrum

The [[p-localization]] of $MU$ decomoses into the 
[[Brown-Peterson spectra]].

## Related concepts

* [[Thom spectrum]]

* [[equivariant complex cobordism cohomology theory]]

* [[cobordism theory determining homology theory]]

* [[MR-theory]]

* [[algebraic cobordism]], [[algebraic cobordism spectrum]]

* [[Adams-Novikov spectral sequence]]

[[!include chromatic tower examples - table]]

## References

### General

Original articles include

* {#Milnor60} [[John Milnor]], _On the cobordism ring &#173;$\Omega^\bullet$ and a complex analogue_, Amer. J. Math. 82 (1960), 505&#8211;521.
 
* {#Novikov60} [[Sergei Novikov]], _Some problems in the topology of manifolds connected with the theory of Thom spaces_, Dokl. Akad. Nauk. SSSR. 132 (1960), 1031&#8211;1034 (Russian). 

* {#Novikov62} [[Sergei Novikov]], _Homotopy properties of Thom complexes_, Mat. Sb. (N.S.) 57 (99) (1962), 407&#8211;442.
 
Textbook accounts include

* {#Stong68} [[Robert Stong]], _Notes on Cobordism theory_, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [publisher page](http://press.princeton.edu/titles/6465.html))


* {#Adams74} [[Frank Adams]], _Stable homotopy theory and generalized homology_, Chicago lectures in mathematics, 1974

* {#Ravenel} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_
 
with an emphasis on the use of $MU$ in the [[Adams-Novikov spectral sequence]], and

* {#Rudyak98} [[Yuli Rudyak]], _On Thom spectra, orientability and cobordism_, Springer Monographs in Mathematics, 1998 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rudyakthom.pdf))
 


Lecture notes include 

* {#Hopkins99} [[Mike Hopkins]], section 4 of _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

* {#Ebert12} [[Johannes Ebert]], _A lecture course on Cobordism Theory_, 2012 ([pdf](http://wwwmath.uni-muenster.de/u/jeber_02/skripten/bordism-skript.pdf))

* {#Schwede12} [[Stefan Schwede]], Example I.2.8 in _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf))


* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html)), Lecture 5 _Complex bordism_ 
([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture5.pdf))

* {#LurieLect6} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html)) Lecture 6 _MU and complex orientations_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture6.pdf)) 
 
 

* {#LurieLect7} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html)),  Lecture 7 _The homology of MU_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture7.pdf))
 

For further context see also the discussion at

* _[[A Survey of Elliptic Cohomology - cohomology theories]]_

See also

* [[Haynes Miller]], _"Chromatic" homotopy theory_ May 2011 ([pdf](http://www-math.mit.edu/~hrm/papers/chromatic.pdf))

### Higher algebra over $MU$

* [[Neil Strickland]], _Products on $MU$-modules_ ([pdf](http://hopf.math.purdue.edu/Strickland/mult.pdf))

### Equivariant theory


For general discussion of equivariant complex oriented cohomology see at _[equivariant cohomology -- References -- Complex oriented cohomology](equivariant+cohomology#InComplexOrientedGeneralizedCohomologyTheory)_

### Relation to CFT

A relation to [[2d CFT]] over [[Spec(Z)]] was suggested in

* Toshiyuki Katsura, Yuji Shimizu, [[Kenji Ueno]], _Complex cobordism ring and conformal field theory over $\mathbb{Z}$_, Mathematische Annalen
March 1991, Volume 291, Issue 1, pp 551-571 ([journal](http://link.springer.com/article/10.1007%2FBF01445226))


[[!redirects complex cobordism spectrum]]
[[!redirects periodic complex cobordism spectrum]]


[[!redirects complex cobordism cohomology theory]]
[[!redirects complex cobordism]]

[[!redirects complex bordism]]

[[!redirects cobordism homology theory]]

[[!redirects complex cobordism cohomology]]
[[!redirects complex cobordism cohomology theory]]

[[!redirects MU]]

[[!redirects complex cobordism theory]]
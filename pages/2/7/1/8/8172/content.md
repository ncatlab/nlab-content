
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Adams spectral sequence_ ([Adams 58](#Adams58)) is a type of [[spectral sequences]] used for computations  in [[stable homotopy theory]]. It computes the [[homotopy groups]] of a [[spectrum]] from its [[homology]]/[[cohomology]], as [[modules]]/[[comodules]] over its [[cohomology operations]]. The Adams spectral sequence can be seen as a variant of the [[Serre spectral sequence]] obtained by replacing a single fibration by an "[[Adams resolution]]".

The original Adams spectral sequence for [[ordinary cohomology]] is further refined by the _[[Adams-Novikov spectral sequence]]_ ([Novikov 67](#Novikov67)) by replacing [[ordinary cohomology]] modulo $p$ by [[complex cobordism cohomology theory]] or [[Brown-Peterson theory]] or the like. Generally, for $E$ a suitable [[E-infinity ring]] there is a corresponding $E$-Adams(-Novikov) spectral sequence whose second page is given by $E$-[[generalized cohomology]].

Working with the Adams spectral sequence tends to be fairly involved, as is clear from the subtlety of the results it computes (notably [[stable homotopy groups of spheres]]) and as witnessed by the fact that one uses further [[spectral sequences]] just to compute the low pages of the Adams spectral sequence, e.g. the [[May spectral sequence]] and the  [[chromatic spectral sequence]]. 

A neat conceptual picture of what happens in the Adams spectral sequence has emerged long after its conception with the arrival of [[higher algebra]] in [[stable (infinity,1)-category|stable infinity-category theory]]. A nice, brief, illuminating modern (and funny) account of this is in ([Wilson 13](#Wilson13)), further details are in ([Lurie 10](#Lurie10)).

## Definition

### Traditional

Given a [[connective spectrum]] $X$ such that $H^\bullet(X)$
has finite type, then for each [[prime number]] $p$ there exists a [[spectral sequence]] which converges to the [[homotopy groups]] of $X$ modulo $p$ $\pi_ast(X) \otimes \mathbb{Z}_p$ and whose $E^2$-page is

$$
  E_2^{s,t} \simeq  Ext_A^{s,t}(H^\bullet(X), \mathbb{Z}/(p) )
$$

where $A$ is the [[Steenrod algebra]]. 

This is built via an [[Adams resolution]]

$$
  \array{
    X = X_0 &\stackrel{g_0}{\leftarrow}&  X_1 &\stackrel{g_1}{\leftarrow}& X_2 &\stackrel{g_2}{\leftarrow}& X_3 &\stackrel{}{\leftarrow}& \cdots
    \\
    \downarrow^{\mathrlap{f_0}} && \downarrow^{\mathrlap{f_1}} && \downarrow^{\mathrlap{f_2}} && \downarrow^{\mathrlap{f_3}} &&
    \\
    K_0 && K_1 && K_2 && K_2
  }
$$

The [[long exact sequence]] induced by this give an [[exact couple]] and the Adams spectral sequence is the corresponding [[spectral sequence]].

This is due to ([Adams 58](#Adams58)). A review is around ([Ravenel, theorem, 2.1.1, def. 2.1.8](#Ravenel)).

### Via cosimplicial spectra 

Let $p$ be a [[prime number]]. Write

$$
  R \coloneqq H \mathbb{F}_p
$$

for the [[Eilenberg-MacLane spectrum]] of the [[field]] $\mathbb{F}_p$. The [[A-∞ algebra]] structure on this induces an [[augmentation|augmented]] [[cosimplicial object|cosimplicial]] [[spectrum]]

$$
  \overline{R}^\bullet \;\colon\; k \mapsto R^{\otimes k}
  \,.
$$

Write $R^\bullet$ for the underlying [[cosimplicial object]] (here and in the following the overline indicates [[augmentation]]).

For $X$ any other [[spectrum]], [[tensor product|tensoring]] induces the (augmented) cosimplicial spectrum

$$
  \overline{X}^\bullet \coloneqq X \otimes \overline{R}^\bullet
  \,.
$$

Now the [[augmentation]] morphism induces a canonical map from $\overline{X}^{-1}$ into the [[totalization]] of $X^\bullet$

$$
  \overline{X}^{-1} \longrightarrow Tot X^\bullet
  \,.
$$

The Adams spectral sequence computes the [[kernels]] of the morphisms on [[homotopy groups]] of this map. 

In this form this appears as ([Lurie 10, theorem 2](#Lurie10)). For the traditional formulation see ([Ravenel, ch. 3, prop. 3.1.2](#Ravenel)).

## Properties

### Relation to Steenrod algebra

The $E_2$-page of the Adams spectral sequence for the $p$-component of 
$\pi_{n+k}(S^n)$  is the ordinary [[Steenrod algebra]] (for given prime $p$).

More generally, For $R$ an [[E-infinity ring]] such that its dual $R$-[[Steenrod algebra]] in the form of the self-[[homology]] $R_\bullet(R)$ is a [[Hopf algebroid]] over $R_\bullet = \pi_\bullet(R)$ (see at [Steenrod algebra -- Hopf algebroid structure](Steenrod+algebra#HopfAlgebraStructure)), then the $E^2$-term of the $E$-Adams spectral sequence is an [[Ext]] of $E_\bullet(E)$-[[comodules]]

$$
  E^2 \simeq Ext_{R_\bullet(R)}(R_\bullet, R_\bullet(X))
  \,.
$$

See the [references below](#ReferencesHopfAlgebroidStructure).

## Related concepts

* [[Adams-Novikov spectral sequence]]

* [[May spectral sequence]]

* [[Steenrod algebra]]

## References

### General

The original articles are

* [[John Adams]], _On the structure and applications of the Steenrod algebra_, Comm. Math. Helv. 32 (1958),
180&#8211;214.
 {#Adams58}

* [[Sergei Novikov]], _The methods of algebraic topology from the viewpoint of cobordism theories_, Izv. Akad. Nauk. SSSR. Ser. Mat. 31 (1967), 855&#8211;951 (Russian).
 {#Novikov67}

Convergence is nicely treated at the end of

* A. K. Bousfield, _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. 

A unique homological perspective is provided in

* [[Haynes Miller]], _On relations between Adams spectral sequences, with an application to the stable homotopy of a Moore space_, J. Pure Appl. Algebra 20 (1981)

Trasditional reviews include

* [[John Adams]], part III of _Stable homotopy and generalised homology, University of Chicago Press, Chicago, Ill., 1974, Chicago Lectures in Mathematics.

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, page 8 of chapter I _An introduction to the homotopy groups of spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenel1.pdf)) and section 1 of chapter 2
 {#Ravenel}

  also Section A.6 of Ravenel's orange book 1992

* [[Paul Goerss]], _The Adams-Novikov spectral sequence and the Homotopy Groups of Spheres_, lecture notes 2007 ([pdf](http://www.math.northwestern.edu/~pgoerss/papers/stras1.pdf))
 {#Goerss2007}

* [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_ ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

See also

* Nerses Aramian, _The Adams spectral sequence_ ([pdf](http://www.math.uiuc.edu/~bertg/Aramian_ASS.pdf))

* [[Alexander Kupers]], _An introduction to the Adams spectral sequence_ ([pdf](http://math.stanford.edu/~kupers/adamsss.pdf))

* R. Bruner, _An Adams spectral sequence primer_ ([pdf](http://www.math.wayne.edu/~rrb/papers/adams.pdf))

* Michael Adamaszek, _An elementary guide to the Adams-Novikov $Ext$_ ([pdf](http://www.math.uni-bremen.de/~aszek/bp.pdf))

* [pdf](http://www.math.harvard.edu/~sia/notes/classical_topology_adams.pdf)


A nice review from the modern point of view of [[higher algebra]] is in 

* [[Dylan Wilson]] _Spectral Sequences from Sequences of Spectra: Towards the
Spectrum of the Category of Spectra_ lecture at [2013 Pre-Talbot Seminar](http://math.northwestern.edu/~htanaka/pretalbot2013/index.php) ([pdf](http://math.northwestern.edu/~htanaka/pretalbot2013/notes/2013-03-21-Dylan-Wilson-ANSS.pdf))
 {#Wilson13}

More along these lines is in

* [[Jacob Lurie]], _[Chromatic homotopy theory lecture](http://www.math.harvard.edu/~lurie/252x.html)_, lecture 8, _The Adams Spectral Sequence_, 2010 ([pdf] (http://www.math.harvard.edu/~lurie/252xnotes/Lecture8.pdf))
  {#Lurie10}

* [[Jacob Lurie]], _[Chromatic homotopy theory lecture](http://www.math.harvard.edu/~lurie/252x.html)_, lecture 9, _The Adams Spectral Sequence for $MU$_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture9.pdf))








### Hopf algebroid $Ext$-structure on $E^2$
 {#ReferencesHopfAlgebroidStructure}


* [[Andrew Baker]], _Brave new Hopf algebroids_ ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/brave-ha.pdf))
 {#Baker}

* [[Andrew Baker]], [[Andrey Lazarev]], _On the Adams Spectral Sequence for R-modules_, Algebr. Geom. Topol. 1 (2001) 173-199 ([arXiv:http://arxiv.org/abs/math/0105079](http://arxiv.org/abs/math/0105079))
 {#BakerLazarev01}

* [[Andrew Baker]] and Alain Jeanneret, _Brave new Hopf algebroids and extensions of $MU$-algebras_, Homology Homotopy Appl. Volume 4, Number 1 (2002), 163-173. ([Euclid](http://projecteuclid.org/euclid.hha/1139840059))
 {#BakerJeanneret02}

* [[Mark Hovey]], _Homotopy theory of comodules over a Hopf algebroid_ ([arXiv:math/0301229](http://arxiv.org/abs/math/0301229)) 
 {#Hovey03}
 


[[!redirects Adams spectral sequences]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The _stable homotopy category_ $Ho(Spectra)$ is the [[category]] of [[spectra]] and [[homotopy classes]] of morphisms between them, the object of study in classical [[stable homotopy theory]]. Equivalently this is the [[homotopy category of an (∞,1)-category]] of the [[stable (∞,1)-category of spectra]] and the latter is the proper context for [[stable homotopy theory]]. But with due care exercised, the stable homotopy category itself is useful.

The stable homotopy category may be thought of as the [[stabilization]] of the classical [[homotopy category]] $Ho(Top)$ under the operation of forming [[loop space objects]] $\Omega$ and [[reduced suspensions]] $\Sigma$: via forming [[suspension spectra]] $\Sigma^\infty$ every [[pointed object]] in the classical [[homotopy category]] maps to the stable homotopy category, and under this map the [[loop space]]- and [[reduced suspension]]-[[functors]] become inverse [[equivalence of categories|equivalences]] on the stable homotopy category.

$$
  \array{
     Ho(Top)^{\ast/} 
      &
      \underoverset{\underset{\Omega}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{} 
      &
     Ho(Top)^{\ast/}
     \\
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     &&
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     \\
     Ho(Spectra) 
     &
     \underoverset{\underset{\Omega}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{\simeq}
     &
     Ho(Spectra)
  }
  \,.
$$


In contrast to the classical [[homotopy category]], the stable homotopy category is a [[triangulated category]] (a shadow of the fact that the [[(∞,1)-category of spectra]] is a [[stable (∞,1)-category]]). As such it may be thought of as a refinement of the [[derived category]] [[category of chain complexes|of chain complexes]] (of [[abelian groups]]): every [[chain complex]] gives rise to a [[spectrum]] and every [[chain map]] to a map between these spectra (the [[stable Dold-Kan correspondence]]), but there are many more spectra and maps between them than arise from chain complexes and chain maps.

Equipped with the [[smash product of spectra]] "$\wedge$" and with [[function spectra]] $[-,-]$, the stable homotopy category becomes a [[symmetric monoidal category|symmetric]] [[closed monoidal category]]. 

A ([[commutative monoid|commutative]]) [[monoid object]] with respect to $\wedge$ is ([[commutative ring spectrum|commutative]]) [[ring spectrum]].

For $E \in Ho(Spectra)$ any spectrum, then the [[functor]]

$$
  E_\bullet \coloneqq \pi_0((\Sigma^\bullet E) \wedge(-)) \;\colon\; Ho(Spectra) \longrightarrow Ab
$$ 

is a [[generalized homology theory]], while the functor

$$
  E^\bullet \coloneqq \pi_0[-,\Sigma^\bullet E] \;\colon\; Ho(Spectra)^\op \longrightarrow Ab
$$

is a [[generalized cohomology theory]].


## Definition

There are various different-looking ways to define the stable homotopy category.

### Via eventually defined maps

One of the first constructions of the stable homotopy category is due to ([Adams 74, part III, sections 2 and 3](#Adams74)), following ([Boardman 65](#Boardman65)). This _[[Adams category]]_ is defined to be the category of [[CW-spectra]] with [[homotopy classes]] of "eventually defined" functions between them.

Hostorically this was advertized as being a construction free of tools of [[category theory]]. See ([Lewis-May-Steinberger 86, pages 1-3](#LewismaySteinberger86)) for review and critical assessment

### Via left homotopy
 {#ViaSpectrificationofSequentialPreSpectra}

([Lewis-May-Steinberger 86, "preamble" pages 1-7](#LewisMaySteinberger86), [Elmendorf-Kriz-May 95, p. 8](#ElmendorfKrizMay95), [Malkiewich 14](#Malkiewich14))

For $E$ a [[sequential spectrum|sequential]] [[pre-spectrum]] and $X$ a [[pointed topological space]], write

$$
  (E \wedge X)_n \coloneqq E_n \wedge X
$$

for the degreewise [[smash product]] of [[pointed topological spaces]]. Write $I_+$ for the unit [[interval]] with a base point adjoined, such that for any spectrum $E$, the [[smash product]] $E \wedge I_+$ is its _[[cylinder spectrum]]_.

A _[[left homotopy]]_ between morphism of pre-spectra $f,g \colon E_1 \longrightarrow E_2$ is a morphism of spectra

$$
  \phi \;\colon\; E_1\wedge I_+ \longrightarrow E_2
$$

such that $\phi|_0 = f$ and $\phi|_1 = g$.

In order for this to be the homotopy-correct notion, we need to apply it with [[domain]] a [[CW-spectrum]] and [[codomain]] an [[Omega-spectrum]].

Let $PreSpectra \stackrel{\overset{L}{\longrightarrow}}{\underset{\ell}{\longleftarrow}} Spectra$ be the 1-categorical [[adjunction]] between [[Omega-spectra]] and [[prespectra]], in the sense defined at [[coordinate-free spectrum]], where $\ell$ is the [[forgetful functor]] and $L$ is [[spectrification]]. 

There is also a [[CW-spectrum]]-replacement functor $\Gamma$.

Write then 

$$
  [E_1,E_2]
  \coloneqq
  Hom(\Gamma E_1, L E_2)_{\sim_{left\;homotopy}}
$$ 

for the corresponding [[homotopy classes]] of maps. 


### Via model structures

There are several [[model categories]] which exhibit [[model structures for spectra]], hence whose [[homotopy category]] is equivalent to the stable homotopy category.

For instance the [[Bousfield-Friedlander model structure]] of [[sequential spectrum|sequential]] [[pre-spectra]] in [[simplicial sets]] ([Bousfield-Friedlander  78](#BousfieldFriedlander78)).

(...)


## Properties

### Symmetric monoidal structure

The [[smash product of spectra]] makes the stable homotopy category into a [[symmetric monoidal category]].

An ([[commutative monoid|commutative]]) [[monoid object]] with respect to this is a ([[commutative ring spectrum|commutative]]) [[ring spectrum]]. A [[module object]] over such is a [[module spectrum]].

### Triangulated structure

The [[homotopy fiber sequences]] of spectra gives the stable homotopy category the structure of a [[triangulated category]].

## Related concepts

* [[Ho(Top)]]

* [[Whitehead theorem]]

## References

The original direct definitions of the stable homotopy category (for precursors see at _[[Spanier-Whitehead category]]_) is due to

* {#Boardman65} [[Michael Boardman]], _Stable homotopy theory_, mimeographed notes, University of Warwick, 1965 onward

Early accounts include

* {#Vogt69} [[Rainer Vogt]], _Boardman's stable homotopy category_, lectures, spring 1969

* {#Cohen70} J. M. Cohen, _Stable Homotopy_, Springer Lecture Notes in Math., No. 165,  Springer-Verlag, Berlin, 1970. 

* [[Dieter Puppe]], _On the stable homotopy category_, Topology and its application (1973)  ([[PuppeStableHomotopyCategory.pdf:file]])

* {#Adams74} [[Frank Adams]], Part III, section 2 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

A fun scan of the (pre-)history of the stable homotopy category is in 

* [[Peter May]], _The hare and the hedgehog_, speech at [[Michael Boardman]]'s birthday meeting ([txt](http://hopf.math.purdue.edu/May/boardman.txt))

See also the references at _[[stable homotopy theory]]_.

Origin articles realizing the stabel homotopy category as the [[homotopy category]] of a [[model category]] include

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], _Homotopy theory of $\Gamma$-spaces, spectra, and bisimplicial sets_, Springer Lecture Notes in Math., Vol. 658, Springer, Berlin, 1978, pp. 80-130. ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/bousfield-friedlander.pdf))


Original articles in the context of [[highly structured spectra]] include

* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], M. Steinberger, _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics, 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf))

* {#ElmendorfKrizMay95} [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], _[[Modern foundations for stable homotopy theory]]_, in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_, Amsterdam: North-Holland, 1995 pp. 213&#8211;253,  ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_, in I.M. James (ed.), _[[Handbook of Algebraic Topology]]_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

and lecture notes such as

* {#Malkiewich14} [[Cary Malkiewich]], _The stable homotopy category_, 2014 ([pdf](http://math.stanford.edu/~carym/stable.pdf))


[[!redirects HoSpectra]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
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

For $E$ a [[cohomology theory]], and $f \colon X \to Y$ a map of suitable [[spaces]], an ordinary [[Umkehr map]] for the induced map $E^\bullet(f) \colon E^\bullet(Y) \to E^{\bullet}(X)$ is a [[dual morphism]] together with self-[[dual objects|duality]] [[equivalences]] for $E^\bullet(X)$ and $E^\bullet(Y)$ ([[orientation in generalized cohomology|orientation]]/[[Atiyah duality]]+[[Thom isomorphism]]). 

More generally, $E^\bullet(X)$ may not be self-dual, but its [[dual object]] may be [[twisted cohomology]] $E^{\bullet+ \chi}(X)$ for some twist $\chi$. In this case the [[Umkehr map]] goes not between the original spaces and their cohomology, but between [[twisted cohomology]] variants of these.

## Definition

### Abstract duality and Atiyah-Milnor-Spanier duality + Pontryagin-Thom collapse

+-- {: .num_defn #SpanierDualityOperation}
###### Definition

Write

$$
  D \coloneqq (-)^\vee\circ \Sigma^\infty_+ \coloneqq L_{whe} Top \to \mathbb{S}Mod
$$

for the [[Spanier-Whitehead duality]] map which sends a [[topological space]] first to its [[suspension spectrum]] and then that to its [[dual object]] in the [[(∞,1)-category of spectra]].

=--

([ABG 11, def 10.3](#ABG11)).

+-- {: .num_prop}
###### Proposition

For $X$ a [[compact manifold]], let $X \to \mathbb{R}^n$ be an [[embedding]] and write $S^n \to X^{\nu_n}$ for the classical [[Pontryagin-Thom collapse map]] for this situation, and write

$$
  \mathbb{S} \to X^{-T X}
$$

for the corresponding [[looping]] map from the [[sphere spectrum]] to the [[Thom spectrum]] of the negative [[tangent bundle]] of $X$. Then [[Atiyah duality]] produces an [[equivalence]]

$$
  X^{- T X} \simeq D X
$$

which identifies the [[Thom spectrum]] with the [[dual object]] of $\Sigma^\infty_+ X$ in $\mathbb{S} Mod$ and this constitutes a [[commuting diagram]]

$$
  \array{
    && X^{- T X}
    \\
    & \nearrow & \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbb{S}
    &\underset{D(X \to \ast)}{\to}&
    D X
  }
$$

identifying the classical [[Pontryagin-Thom collapse map]] with the abstract [[dual morphism]] construction of prop. \ref{SpanierDualityOperation}.

More generally, for $W \hookrightarrow X$ an [[embedding]] of [[manifolds]], then [[Atiyah duality]] identifies the [[Pontryagin-Thom collapse maps]] 

$$
  \mathbb{S} \to X^{-T X} \to W^{- T W}
$$

with the abstract [[dual morphisms]]

$$
  \mathbb{S} \to D X \to D W
  \,.
$$


=--

([ABG 11, prop. 10.5](#ABG11)).

### Umkehr map

+-- {: .num_remark}
###### Remark

Given now $E \in CRing_\infty$ an [[E-∞ ring]], then the [[dual morphism]] $\mathbb{S} \to D X$ induces under [[smash product]] a similar Pontryagin-Thom collapse map, but now not in [[sphere spectrum]]-[[(∞,1)-modules]] but in $E$-[[(∞,1)-modules]].

$$
  E \to D X \otimes_{\mathbb{S}} E
  \,.
$$

The image of this under the $E$-[[generalized cohomology theory|cohomology]] functor produces 

$$
  [D X \otimes_{\mathbb{S}} E, E] \to E
  \,.
$$

If now one has a [[Thom isomorphism]] ($E$-[[orientation in generalized cohomology|orientation]]) $ [D X \otimes_{\mathbb{S}} E, E] \simeq [X,E]$ that identifies the cohomology of the dual object with the original cohomology, then together with the above this produces the [[Umkehr map]]

$$
  [X,E] \simeq [D X \otimes_{\mathbb{S}} E, E] \to E
$$

that pushes the $E$-cohomology of $X$ to the $E$-cohomology of the point. Analogously if instead of the terminal map $X \to \ast$ we start with a more general map $X \to Y$.

More generally a [[Thom isomorphism]] may not exists, but $[D X \otimes_{\mathbb{S}} E, E]$ may still be equivalent to a [[twisted cohomology]]-variant $[X,E]_{\chi}$ of $[X,E]$, namely to $[\Gamma_X(\chi),E]$, where $\chi \colon \Pi(X) \to E Line \hookrightarrow E Mod$ is an ([[flat (∞,1)-bundle|flat]]) $E$-[[(∞,1)-module bundle]] on $X$ and and $\Gamma \simeq \underset{\to}{\lim}$ is the [[(∞,1)-colimit]] (the [[generalized Thom spectrum]] construction). In this case the above yields a **twisted Umkehr map**.


=--

([ABG 10, 9.1](#ABG10))

## Examples

* [[fiber integration in ordinary cohomology]]

* [[fiber integration in ordinary differential cohomology]]

* [[fiber integration in K-theory]]

  For a detailed discussion of an example in [[K-theory]] see also at _[[Poincaré duality algebra]]_ and at _[[Freed-Witten-Kapustin anomaly]]_.

* [[fiber integration in differential K-theory]]

## Related concepts

[[!include generalized fiber integration synonyms - table]]

## References

Twisted Umkehr maps in [[topological K-theory]] are discussed (somewhat implicitly sometimes) in the literature on [[KK-theory]]. See the references at _[[Poincaré duality algebra]]_.

The general abstract formulation in [[stable homotopy theory]] is sketched in section 9 of

* {#ABG10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 {#ABG10}

and in section 10 of

* {#ABG11} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Parametrized spectra, multiplicative Thom spectra, and the twisted Umkehr map_, Geom. Topol. 22(7): 3761-3825 (2018).  ([arXiv:1112.2203](http://arxiv.org/abs/1112.2203), [doi:10.2140/gt.2018.22.3761](https://doi.org/10.2140/gt.2018.22.3761))
 

A review and applications to [[quantization]] of [[local prequantum field theory]] is in 

* {#Nuiten13} [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, master thesis, August 2013

Formalization in [[dependent linear type theory]] is discussed 

* [[Urs Schreiber]], _[[schreiber:Quantization via Linear homotopy types]]_
 

[[!redirects twisted Umkehr maps]]
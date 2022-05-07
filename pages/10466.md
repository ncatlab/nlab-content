
> under construction (some more harmonization needed)

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
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

What is called _global equivariant homotopy theory_ is a variant of [[equivariant cohomology]] in [[homotopy theory]] where [[pointed object|pointed]] [[topological spaces]]/[[homotopy types]] are equipped with $G$-[[infinity-actions]] "for all [[compact Lie groups]] $G$ at once", or more generally for a [[global family]].

Sometimes this is referred to just as "global homotopy theory", leaving the equivariance implicit. There is also a [[stabilization|stable]] version involving [[spectra]] equipped with [[infinity-actions]], see at _[[global equivariant stable homotopy theory]]_.

More precisely, the _global equivariant homotopy category_ is the [[(∞,1)-category]] (or else its [[homotopy category of an (∞,1)-category|homotopy category]]) of [[(∞,1)-presheaves]] $PSh_\infty(Orb)$ on the  [[global orbit category]] $Orb$ ([Henriques-Gepner 07, section 1.3](#HenriquesGepner07)), regarded as an [[(∞,1)-category]].

Here $Orb$ has as [[objects]] [[compact Lie groups]] and the [[(∞,1)-categorical hom-spaces]] $Orb(G,H) \coloneqq \Pi [\mathbf{B}G, \mathbf{B}H] $, where on the right we have the [[geometric realization of cohesive infinity-groupoids|fundamental (∞,1)-groupoid]] of the [[topological groupoid]] of [[group homomorphisms]] and [[conjugation|conjugations]].





## Definition
 {#Definition}


We follow ([Rezk 14](#Rezk14)). Beware that the terminology there differs slightly but crucially in some places from ([Henriques-Gepner 07](#HenriquesGepner07)). Whatever terminology one uses, the following are the key definitions.

The following is the _[[global equivariant indexing category]]_.

+-- {: .num_defn #GlobalIndexingCategory}
###### Definition

Write $Glo$  for the [[(∞,1)-category]] whose

* [[objects]] are [[compact Lie groups]]; 

* [[(∞,1)-categorical hom-spaces]] $Glo(G,H)$ are the [[geometric realizations]] of the [[Lie groupoid]] of smooth functors and smooth [[natural transformations]] $Top\infty Grpd(\mathbf{B}G, \mathbf{B}H)$.

=--

([Rezk 14, 2.1](#Rezk14))

+-- {: .num_defn}
###### Remark

Equivalent models for the global indexing category, def. \ref{GlobalIndexingCategory} include the category "$O_{gl}$" of ([May 90](#May90)).
Another variant is $\mathbf{O}_{gl}$ of ([Schwede 13](#Schwede13)).

=--

([Rezk 14, 2.4, 2.5](#Rezk14))

The following is the _[[global orbit category]]_.

+-- {: .num_defn #GlobalOrbitCategory}
###### Definition

Write 

$$
  Orb \longrightarrow Glo
$$

for the non-[[full sub-(∞,1)-category|full]] [[sub-(∞,1)-category]] of the global indexing category, def. \ref{GlobalIndexingCategory}, on the [[injection|injective]] group homomorphisms.

=--

([Rezk14, 4.5](#Rezk14))

The following defines the _global equivariant homotopy theory_ $PSh_\infty(Glo)$.

+-- {: .num_defn #GlobalEquivariantHomotopyTopos}
###### Definition

Write

$$
  Top_{Glo} \coloneqq PSh_\infty(Glo)
$$

for the [[(∞,1)-category of (∞,1)-presheaves]] (an [[(∞,1)-topos]]) on the global indexing category $Glo$ of def. \ref{GlobalIndexingCategory}, and write
$$
  \mathbb{B} \;\colon\; Glo \longrightarrow PSh_\infty(Glo)
$$

for the [[(∞,1)-Yoneda embedding]].

Similarly write 

$$
  Top_{Orb} \coloneqq PSh_\infty(Orb)
$$

for the [[(∞,1)-category of (∞,1)-presheaves]] on the  [[global orbit category]] $Orb$ of def. \ref{GlobalOrbitCategory}, and write again

$$
  \mathbb{B} \;\colon\; Orb \longrightarrow PSh_\infty(Orb)
$$

for its [[(∞,1)-Yoneda embedding]].

=--

([Rezk 14, 3.1 and 4.5](#Rezk14))

The following recovers the ordinary ("local") [[equivariant homotopy theory]] of a given [[topological group]] $G$ ("of $G$-spaces").

+-- {: .num_defn #LocalEquivariantHomotopyTheory}
###### Definition

For $G$ a [[topological group]], write 

$$
  G Top \coloneqq PSh_\infty(Orb)/\mathbb{B}G
$$

for the [[slice (∞,1)-topos]] of $PSh_\infty(Orb)$ over the image of $G$ under the [[(∞,1)-Yoneda embedding]], as in def. \ref{GlobalEquivariantHomotopyTopos}.

=--

This is ([Rezk 14, 1.5](#Rezk14)). Depending on axiomatization this is either a definition or [[Elmendorf's theorem]], see at _[[equivariant homotopy theory]]_ for more on this.


## Properties

### Cohesion

+-- {: .num_prop #CohesionOfGlobalEquivariantHomotopyTheory}
###### Proposition

The global equivariant homotopy theory $PSh_\infty(Glo)$ of def. \ref{GlobalEquivariantHomotopyTopos} is a [[cohesive (∞,1)-topos]] over the canonical [[base (∞,1)-topos]] [[∞Grpd]]:

the [[global section geometric morphism]]

$$
  (\Delta \dashv \Gamma)
  \;\colon\;
  PSh_\infty(Glo)
  \longrightarrow
  \infty Grpd
$$

is given (as for all (∞,1)-presheaf (∞,1)-toposes) by the [[direct image]]/[[global section]] functor being the [[homotopy limit]] over the opposite [[(∞,1)-site]]

$$
  \Gamma X \simeq \underset{\leftarrow}{\lim}(Glo^{op}\stackrel{X}{\to} \infty Grpd)
$$

and the [[inverse image]]/[[constant ∞-stack]] functor literally assigning constant presheaves:

$$
  \Delta S \colon G \mapsto S
 \,.
$$

This is a [[full and faithful (∞,1)-functor]].



Moreover,  $\Delta$ has a further [[left adjoint]] $\Pi$ which preserves [[finite products]], and $\Gamma$ has a further [[right adjoint]] $\nabla$.

=--

([Rezk 14, 5.1](#Rezk14))

More in detail, the [[shape modality]], [[flat modality]] and [[sharp modality]] of this [[cohesion]] of the global equivariant homotopy theory has the following description.


### Relation between global and local equivariant homotopy theory



+-- {: .num_defn #InclusionOfGSpacesInTheGlobalTheory}
###### Definition

For $G$ a [[compact Lie group]] define an [[(∞,1)-functor]]

$$
  \delta_G \;\colon\; G Top \longrightarrow PSh_\infty(Glo)
$$

sending a [[topological G-space]] to the  he presheaf which sends a group $H$ to the [[geometric realization]] of the [[topological groupoid]] of maps from $\mathbf{B}H$ to the [[action groupoid]] $X//G$:

$$
  \delta_G(X)\;\colon\; H \mapsto \Pi( [\mathbf{B}H, X//G] )  
  \,.
$$

Observe that by def. \ref{GlobalEquivariantHomotopyTopos} this gives $\delta_G(\ast) \simeq \mathbb{B}G$ and so $\delta_G$ induces a functor

$$
  \Delta_G \;\colon\; G Top \simeq G Top/\ast \simeq PSh_\infty(Orb)/\mathbb{B}G \stackrel{\delta_G}{\longrightarrow} PSh_\infty(Glo)/\mathbb{B}G
 \,.
$$

=--

([Rezk 14, 3.2](#Rezk14))

+-- {: .num_prop #OrdinaryQuotientAndHomotopyQuotientViaCohesion}
###### Proposition
**(ordinary [[quotient]] and [[homotopy quotient]] via equivariant cohesion)**

On a $G$-space $X \in G Top$ included via def. \ref{InclusionOfGSpacesInTheGlobalTheory} into the global equivariant homotopy theory, 

* the [[shape modality]] of def. \ref{CohesionOfGlobalEquivariantHomotopyTheory} produces the [[homotopy type]] of the ordinary [[quotient]] of the $G$-[[action]]

  $$
    \Pi(\delta_G(X)) \simeq \vert X/G \vert
    \,,
  $$

* the [[flat modality]] of def. \ref{CohesionOfGlobalEquivariantHomotopyTheory} produces the [[homotopy type]] of the [[homotopy quotient]]/[[homotopy coinvariants]] of the $G$-[[action]] ([[∞-action]])

  $$
    \Gamma(\delta_G(X)) \simeq \vert X//G \vert
    \,,
  $$

In particular then the [[points-to-pieces transform]] of general [[cohesion]] yields the comparison map

$$
  \vert X//G \vert
  \longrightarrow
  \vert X/G \vert
   \,.
$$

=--

([Rezk 14, 5.1](#Rezk14))

+-- {: .num_prop #CohesionOnLocalSlice}
###### Proposition

For $G$ any [[compact Lie group]], the [[cohesion]] of the global equivariant homotopy theory, prop. \ref{CohesionOfGlobalEquivariantHomotopyTheory}, descends to the [[slice (∞,1)-toposes]]

$$
  PSh_\infty(Glo)/\mathbb{B}G
  \longrightarrow
  PSh_\infty(Orb)/\mathbb{B}G \simeq G Top
  \,,
$$

hence to cohesion over the "local" $G$-[[equivariant homotopy theory]].

The inclusion $\Delta_G$ is that of def. \ref{InclusionOfGSpacesInTheGlobalTheory}.

=--

([Rezk 14, 5.3](#Rezk14))

### Relation to topological stacks and orbispaces

> under construction

By the main theorem of ([Henriques-Gepner 07](#HenriquesGepner07)) the [[(∞,1)-presheaves]] on the  [[global orbit category]] are equivalently "cellular" [[topological stacks]]/[[topological groupoids]] ("[[orbispaces]]"), we might write this as

$$
  ETopGrpd^{cell} = PSh_\infty(Orb)
  \,.
$$

(As such the global equivariant homotopy theory should be similar to [[ETop∞Grpd]]. Observe that this is a [[cohesive (∞,1)-topos]] with $\Pi$ such that it sends a topological [[action groupoid]] of a [[topological group]] $G$ acting on a [[topological space]] $X$ to the [[homotopy quotient]] $\Pi(X)//\Pi(G)$.)

The central theorem of ([Rezk 14](#Rezk14)) (using a slightly different definition than [Henriques-Gepner 07](#HenriquesGepner07)) is that $PSh_\infty(Orb)$ is a [[cohesive (∞,1)-topos]] with $\Gamma$ producing homotopy quotients.



## Related concepts

* [[orbifold cohomology]]

* [[global equivariant stable homotopy theory]]

* [[proper equivariant homotopy theory]]

[[!include equivariant homotopy theory -- table]]

[[!include homotopy type representation theory -- table]]

## References

The [[global orbit category]] $Orb$ is considered in 

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))

* {#Lurie} [[Jacob Lurie]], Section 3 of _Elliptic cohomology III: Tempered Cohomology_ ([pdf](http://www.math.harvard.edu/~lurie/papers/Elliptic-III-Tempered.pdf))

  
Global unstable equivariant homotopy theory is discussed as a [[localization]] of the category of "orthogonal spaces" (the unstable version of [[orthogonal spectra]]) in

* {#Schwede17} [[Stefan Schwede]], _Orbispaces, orthogonal spaces, and the universal compact Lie group_ ([arXiv:1711.06019](https://arxiv.org/abs/1711.06019))

* {#Schwede18} [[Stefan Schwede]], _[[Global homotopy theory]]_ ([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

see also 

* {#May90} [[Peter May]], _Some remarks on equivariant bundles and classifying spaces_, Asterisque 191 (1990), 7, 239-253. International Conference on Homotopy Theory (Marseille-Luminy, 1988).

Discussion of the global equivariant homotopy theory as a [[cohesive (∞,1)-topos]] is in 

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)

Discussion of a model structure for global equivariance with respect to [[geometrically discrete ∞-groupoid|geometrically discrete]] [[simplicial groups]]/[[∞-group]] (globalizing the [[Borel model structure]] for [[∞-actions]]) is in 

* [[Yonatan Harpaz]], [[Matan Prasma]], _The Grothendieck construction for model categories_ ([arXiv:1404.1852](http://arxiv.org/abs/1404.1852))

Discussion from a perspective of [[homotopy type theory]] is in 

* {#Shulman15} [[Mike Shulman]], _Univalence for inverse EI diagrams_ ([arXiv:1508.02410](http://arxiv.org/abs/1508.02410))

The example of global equivariant [[algebraic K-theory]]:

* [[Stefan Schwede]], _Global algebraic K-theory_ ([arXiv:1912.08872](https://arxiv.org/abs/1912.08872))

On [[orbifold cohomology]] seen in [[global equivariant homotopy theory]]:

* {#Juran20} [[Branko Juran]], _Orbifolds, Orbispaces and Global Homotopy Theory_ ([arXiv:2006.12374](https://arxiv.org/abs/2006.12374))

following the suggestion in [Schwede 17, Intro](#Schwede17), [Schwede 18, p. ix-x](#Schwede18).


[[!redirects global homotopy theory]]

[[!redirects global equivariant homotopy category]]

[[!redirects globally equivariant homotopy theory]]

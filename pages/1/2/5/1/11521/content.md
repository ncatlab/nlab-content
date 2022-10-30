
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

The _global equivariant indexing category_ is the full subcategory of [[topological ∞-groupoids]] on those which are [[deloopings]] of [[compact Lie groups]], with hom-spaces being the [[geometric realization]] of the [[internal homs]] there.

The [[(∞,1)-presheaves]] over the global equivariant indexing category is the [[global equivariant homotopy theory]]. This is a [[cohesive (∞,1)-topos]] over [[∞Grpd]] ([Rezk 14](#Rezk14)).

## Definition

The following defines the _global equivariant indexing category_ $Glo$.

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

for the non-full [[sub-(∞,1)-category]] of the global indexing category, def. \ref{GlobalIndexingCategory}, on the [[injection|injective]] group homomorphisms.

=--

([Rezk 14, 4.5](#Rezk14))

## Properties

### Relation to the local orbit category

The [[slice (∞,1)-category]] of the global orbit category over $\mathbf{B}G$ is the local [[orbit category]] of $G$

$$
  Glo_{/\mathbf{B}G}  \simeq Orb_G
 \,.
$$

### Relation to orbispaces and $G$-spaces

The [[(∞,1)-category of (∞,1)-presheaves]] over the global orbit category is that of [[orbispaces]].

Accordingly, by the discussion [here](over-%28infinity%2C1%29-topos#SheavesOnBigSite), the [[slice (∞,1)-topos]] of orbispaces over $\mathbf{B}G$ is that of [[G-spaces]]

$$
  PSh_\infty(Orb)_{/\mathbf{B}G}
  \simeq
  PSh_\infty(Orb_{/\mathbf{B}G})
  \simeq
  PSh_\infty(Orb_G)
  \simeq
  G Space
$$

(where the last step is [[Elmendorf's theorem]]).


### Relation to equivariant homotopy theory


The [[(∞,1)-category of (∞,1)-presheaves]] on the [[global equivariant indexing category]] is the [[global equivariant homotopy theory]] and under the canonical projection is a [[cohesive (∞,1)-topos]] over [[∞Grpd]]. Its [[slice (∞,1)-topos]] over the terminal oribispace is cohesive over [[orbispaces]]

$$
  PSh_\infty(Glo)_{/\mathcal{N}} \to Psh_\infty(Orb)
 \,.
$$

## References

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))
  
* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)

See also 

* {#Schwede13} [[Stefan Schwede]], _Global homotopy theory_, 2013 ([pdf](http://www.math.uni-bonn.de/~schwede/global.pdf))


* {#May90} [[Peter May]], _Some remarks on equivariant bundles and classifying spaces_, Asterisque 191 (1990), 7, 239-253. International Conference on Homotopy Theory (Marseille-Luminy, 1988).

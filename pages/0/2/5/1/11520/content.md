
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

The _global orbit category_ is the unification of all $G$-[[orbit categories]] as the [[groups]] $G$ are allowed to vary. 

The [[(∞,1)-presheaves]] over the global orbit category provide the [[base (∞,1)-topos]] over which the [[global equivariant homotopy theory]] (see there) is a [[cohesive (∞,1)-topos]] ([Rezk 14](#Rezk14)).

## Definition

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

The following is the _ [[global orbit category]]_.

+-- {: .num_defn #GlobalOrbitCategory}
###### Definition

Write 

$$
  Orb \longrightarrow Glo
$$

for the non-full [[sub-(∞,1)-category]] of the global indexing category, def. \ref{GlobalIndexingCategory}, on the [[injection|injective]] group homomorphisms.

=--

([Rezk 14, 4.5](#Rezk14))

## References

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))
  
* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)

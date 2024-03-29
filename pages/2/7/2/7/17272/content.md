
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The analog in [[stable homotopy theory]]  of [[weak homotopy equivalences]] in classical [[homotopy theory]].

The stable weak equivalences of [[sequential spectra]] in [[simplicial sets]] form the weak equivalences in the [[Bousfield-Friedlander model structure]] for [[stable homotopy theory]].

Beware that for other types of spectra there may be subtle corrections to this statement. For instance for [[symmetric spectra]] the maps that are stable weak equivalences on the underlying sequential spectra are guaranteed to be weak equivalences in the [[model structure on symmetric spectra]] only on [[semistable symmetric spectra]].


## Definition

### For sequential spectra

+-- {: .num_defn #StableHomotopyGroups}
###### Definition

The [[stable homotopy groups]] of a [[sequential spectrum]] $X$, is the $\mathbb{Z}$-[[graded abelian groups]] given by the [[colimit]] of [[homotopy groups]] of the component spaces (or of their [[geometric realization]] if they are given as [[simplicial sets]])

$$
  \pi_\bullet(X)
  \coloneqq
  \underset{\longrightarrow}{\lim}_k
  \pi_{\bullet+k}({ X_n })
  \,.
$$

This constitutes a [[functor]]

$$
  \pi_\bullet \;\colon\; SeqSpec(sSet) \longrightarrow Ab^{\mathbb{Z}}
  \,.
$$

=--

+-- {: .num_defn #StableWeakEquivalenceOfSequentialsSetSpectra}
###### Definition

A morphism $f \colon X \longrightarrow Y$ of [[sequential spectra]], is called a [[stable weak homotopy equivalence]], if its image under the [[stable homotopy group]]-functor of def. \ref{StableHomotopyGroups} is an [[isomorphism]]

$$
  \pi_\bullet(f) \;\colon\; \pi_\bullet(X) \longrightarrow \pi_\bullet(Y)
  \,.
$$

=--

## Properties

### Closure properties


(e.g. [MMSS 00, theorem 7.4 ](#MMSS00))


## References

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings of the London Mathematical Society, 82 (2001), 441-512 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf))


[[!redirects stable weak homotopy equivalences]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

For suitable setups, there is a canonical [[homomorphism]] from [[algebraic K-theory]] to [[topological K-theory]] with given [[coefficients]].

This usually goes just by "the comparison map". (e.g. [Rosenberg, theorem 2.1](#Rosenberg))

## Statement

### For complex K-theory

There is a canonical [[homomorphism]] of [[spectra]]

$$
  K \mathbb{C} \longrightarrow KU
$$

from the [[algebraic K-theory]] spectrum of the [[complex numbers]] to [[KU]] (e.g. [Paluch 01, lemma 2.6](#Paluch01)). 

In fact in terms of [[cohesion]] of [[smooth spectra]], this is a component of a [[natural transformation]], this we discuss [below](#FormulationInCohesion).

### Formulation in cohesive homotopy-type theory
 {#FormulationInCohesion}

Given a [[cohesive (infinity,1)-topos]] and a [[symmetric monoidal (∞,1)-category]] $V\in CMon_\infty(Cat_\infty(\mathbf{H}))$, [[internal (∞,1)-category|internal]] to $\mathbf{H}$ write

$$
  \mathcal{K}(V)\in Stab(\mathbf{H})\hookrightarrow T \mathbf{H}
$$

for its [[K-theory of a symmetric monoidal (∞,1)-category]] (formed locally and then [[∞-stackification|∞-stackified]]). This is a [[stable homotopy type]] in the [[tangent cohesive (∞,1)-topos]].

The [[flat modality]] part $\flat \mathcal{K}(V)$ is the [[algebraic K-theory]] of $\flat V \in CMon_\infty(Cat_\infty)$. The [[shape modality]] part on the other hand is a "topological" version of this

The [[points-to-pieces transform]] $\flat \to \Pi$ provides a [[natural transformation|natural]] comparison map

$$
  \flat (\mathcal{K}(V)) \longrightarrow \Pi (\mathcal{K}(V))
  \,.
$$

For instance for $\mathbf{H}= $ [[Smooth∞Grpd]] and $V = \mathbf{Vect}^{\oplus}$ the [[stack]] of smooth [[vector bundles]] with [[direct sum]] monoidal structure, then $\flat \mathcal{K}(V)\simeq K \mathbb{C}$ is the [[algebraic K-theory]] of the [[complex numbers]] and $\Pi \mathcal{K}(V)\simeq $ [[KU]] is complex [[topological K-theory]].

See at _[[differential cohomology diagram]]_ for more on this.

## References

* [[Henri Gillet]], _Comparing algebraic and topological K-theory_, in _Higher Algebraic K-Theory: an overview_ Lecture Notes in Mathematics Volume 1491, 1992, pp 55-99


Discussion relating [[algebraic K-theory]] of [[varieties]] to complex topological K-theory is in 

* {#Paluch01} Michael Paluch, _Algebraic $K$-theory and topological spaces_, K-theory 471 (2001) ([web](http://www.math.uiuc.edu/K-theory/0471/))

and for [[sheaves of spectra]] of [[twisted K-theory]] in 

* {#AntieuWilliams11} [[Benjamin Antieau]], [[Ben Williams]], section 2.3 of _The period-index problem for twisted topological K-theory_, Geometry & Topology ([arXiv:1104.4654](http://arxiv.org/abs/1104.4654))

Discussion in terms of [[Banach algebras]] is in 

* {#Rosenberg} [[Jonathan Rosenberg]], _Comparison between algebraic and topological K-theory for Banach algebras and $C^\ast$-algebras_   ([pdf](http://www2.math.umd.edu/~jmr/algtopK.pdf))


[[!redirects comparison between algebraic and topological K-theory]]
[[!redirects comparison mapso between algebraic and topological K-theory]]

[[!redirects comparison map between algebraic K-theory and topological K-theory]]
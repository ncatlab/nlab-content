
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

An _algebra spectrum_ or _[[A-∞ algebra]]-spectrum_ over a [[ring spectrum]] is the analog in the [[higher algebra]] of [[stable homotopy theory]] of an [[associative algebra]] over a [[ring]] on ordinary [[algebra]].

## Definition

Abstractly, an _$A_\infty$-algebra spectrum_ over an [[E-∞ ring spectrum]] $R$ is [[algebra in an (∞,1)-category]] in the [[stable (∞,1)-category]] of $R$-[[module spectra]].

Concretely this [[(∞,1)-category]] is [[presentable (∞,1)-category|presented]] by the [[model structure on monoids]] in the [[monoidal model category|monoidal]] $R$-modules in the [[model structure on symmetric spectra]].

(...)


## Properties

### Stable monoidal Dold-Kan correspondence

Let $R := H \mathbb{Z}$ be the [[Eilenberg-MacLane spectrum]] for the [[integer]]s. 

+-- {: .num_prop}
###### Proposition

There is a zig-zag of [[monoidal Quillen adjunction|lax monoidal]] [[Quillen equivalences]]

$$
  H \mathbb{Z} Mod
    \stackrel{\overset{Z}{\longrightarrow}}{\underset{U}{\leftarrow}}
  Sp^\Sigma(sAb)
    \stackrel{\overset{L}{\leftarrow}}{\underset{\phi^* N}{\longrightarrow}}
  Sp^\Sigma(Ch_+)
   \stackrel{\overset{D}{\longrightarrow}}{\underset{R}{\leftarrow}}
  Ch_\bullet
  \,,
$$

between [[monoidal model categories]] satisfying the [[monoid axiom in a monoidal model category]]:

* the model structure for $H \mathbb{Z}$-[[module spectra]];

* the [[model structure on symmetric spectrum objects]] in [[simplicial abelian group]]s and in [[chain complex]]es;

* and the [[model structure on chain complexes]] (unbounded).

This induces a [[Quillen equivalence]] between the corresponding [[model structures on monoids]] in these [[monoidal category|monoidal categories]], which on the left is the model structure on $H \mathbb{Z}$-algebra spectra and on the right the [[model structure on dg-algebras]]:

$$
  H \mathbb{Z} Alg \simeq dgAlg_\mathbb{Z}
  \,.
$$

=--

This is due to ([Shipley](#Shipley)). The corresponding [[equivalence of (∞,1)-categories]] for $R$ a commutative rings with the intrinsically defined [[(∞,1)-category]] of [[En-algebra|E1-algebra]] objects on the left appears as ([Lurie, prop. 7.1.4.6](#Lurie)).

+-- {: .num_remark}
###### Remark

This is a stable version of the [[monoidal Dold-Kan correspondence]]. See there for more details.

=--

## Related concepts

* [[ring spectrum]], [[module spectrum]]

* [[symmetric algebra spectrum]]

* [[A-∞ algebra]], [[algebra in an (∞,1)-category]]

## References

An account in terms of [[(∞,1)-category theory]] is in section 7.1.4 of

* [[Jacob Lurie]], _[[Higher Algebra]]_

The equivalence of $H \mathbb{Z}$-algebra spectra with [[dg-algebra]]s is due to

* [[Brooke Shipley]], _$H \mathbb{Z}$-algebra spectra are differential graded algebras_ , Amer. Jour. of Math. 129 (2007) 351-379. ([arXiv:math/0209215](http://arxiv.org/abs/math/0209215))
 {#Shipley}

Eilenberg-MacLane spectra $H R$ for $R$ itself a [[dg-algebra]] are discussed in

* [[Daniel Dugger]], [[Brooke Shipley]], _Topological equivalences for differential graded algebras_ ([arXiv:math/0604259](http://arxiv.org/abs/math/0604259))

See also the references at [[stable homotopy theory]].

[[!redirects algebra spectra]]


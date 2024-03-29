
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[pointed object|pointed]] [[homotopy type]] $X_\ast$ could be called _linear_ (following the terminology of _[[linear model category]]_) if the canonical [[morphism]]

$$
  \Sigma \Omega X \longrightarrow X
$$

from the [[suspension object]] of its [[loop space object]] is an [[equivalence in an (infinity,1)-category|equivalence]].

By [[Goodwillie calculus]] the [[tangent (∞,1)-topos]] $T\mathbf{H}$ of some [[(∞,1)-topos]] $\mathbf{H}$ is the [[localization of an (∞,1)-category|localization]] of the [[classifying (∞,1)-topos]] $\mathbf{H}[X_\ast]$ (of pointed objects), that regard each pointed finite [[powering]] $X_\ast^\bullet$ of the generic pointed object $X_\ast$ as a linear homotopy type.

See at [excisive functor -- Characterization via the generic pointed object](https://ncatlab.org/nlab/show/excisive+infinity-functor#CharacterizationViaAGenericStableObject).

Therefore a pointed homotopy type $X_\ast$ such that all its finite pointed powers are linear could be called a _stable homotopy type_.

For $\mathbf{H}$ an [[(∞,1)-topos]] and $T \mathbf{H}$ its [[tangent (∞,1)-topos]], then all homotopy types in $T_\ast \mathbf{H} \hookrightarrow T \mathbf{H}$ are stable in this sense, these are equivalently the [[spectrum objects]] in $\mathbf{H}$.


## Related concepts

* [[sequential spectrum type]]

* [[dependent linear type theory]]

* [[equivariant homotopy type]]

* [[modal homotopy type]]

* [[geometric homotopy type]], [[cohesive homotopy type]]

## References

An account using [[modal homotopy type theory]] is in

* [[Mitchell Riley]], [[Eric Finster]], [[Daniel Licata]], _Synthetic Spectra via a Monadic and Comonadic Modality_, ([arXiv:2102.04099](https://arxiv.org/abs/2102.04099))

[[!redirects stable homotopy types]]
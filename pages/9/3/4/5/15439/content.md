
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In a context of [[synthetic differential geometry]] or [[differential cohesion]], then given any [[space]] $X$ and a [[point]] $x \colon \ast \to X$, then the _formal disk_ in $X$ at $x$ is just the [[infinitesimally thickened point]] which is the [[formal neighbourhood]] of that point. If there is a concept of [[dimension]] for $X$, then the dimension of that formal disk is the dimension of $X$ at that point.

[[Isbell duality|Dually]] in terms of [[function algebras]], in the typical models formal disks are the [[formal spectra]] of [[formal power series]] algebras. The formal spectra of the [[Laurent series]] algebras are instead the "punctured formal disks", hence formal disks with their unique global point removed.

More concretely, if $S$ is any [[infinity-cohesive site]] of "differentiable spaces" (such as for instance [[complex analytic manifolds]]) and $S_{synthdiff}$ is the corresponding site of infinitesimal thickenings (for instance complex analytic [[smooth loci]] of the form the product of a complex manifold with an [[infinitesimally thickened point]]), then we have relative [[cohesion]] of $Sh_\infty(S_{synthdiff})$ over $Sh_\infty(InfPoints)$ (see at _[[synthetic differential ∞-groupoid]]_) and for any space $X$ then the [[flat modality]] takes it to its union $\flat X$ of all formal disks around all [[global points]] of $X$.

## Properties

### Function field analogy

## Related concepts

* [[affine line]]

* [[infinitesimally thickened point]]

* [[infinitesimal disk bundle]]

[[!include function field analogy -- table]]

## References

Discussion in [[differential cohesion]] is in

* [[Igor Khavkine]], [[Urs Schreiber]], _[[schreiber:Synthetic variational calculus|Synthetic geometry of differential equations: I. Jets and comonad structure]]_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))

and formalization in [[homotopy type theory]] is in 

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_, PhD Thesis, 2017

* {#Wellen18} [[Felix Wellen]], _[[schreiber:Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966))




[[!redirects formal disks]]

[[!redirects formal disc]]
[[!redirects formal discs]]
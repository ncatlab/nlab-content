
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
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _$J$-homomorphism_ is traditionally a family of [[group]] homomorphisms

$$
  J_i \;\colon\; \pi_i(O(n)) \longrightarrow \pi_{n+i}(S^n)
$$

from the [[homotopy groups]] of (the [[topological space]] underlying) the [[orthogonal group]] to the [[homotopy groups of spheres]].

This refines to a morphism of [[∞-groups]]

$$
  J \;\colon\; O \longrightarrow GL_1(\mathbb{S})
$$

from the [[stable orthogonal group]] (regarded as a [[group object in an (∞,1)-category|group object]] in $L_{whe} Top \simeq$ [[∞Grpd]])
to the [[∞-group of units]] of the [[sphere spectrum]], regarded as an [[E-∞ ring spectrum]].

By postcomposition with the [[delooping]] of the J-homomorphism  $B J \;\colon\; B O \to B GL_1(\mathbb{S}) $, the $J$-homomorphism sends real [[vector bundles]] to [[sphere spectrum]]-bundles, namely [[(∞,1)-line bundles]] with typical [[fiber]] $\mathbb{S}$. See at _[[Thom space]]_ for more on this.

## Details
 {#Details}

For $n \in \mathbb{N}$ regard the $n$-[[sphere]] (as a [[topological space]]) as the [[one-point compactification]] of the [[Cartesian space]] $\mathbb{R}^n$

$$
  S^n \simeq (\mathbb{R}^n)^\ast
  \,.
$$

+-- {: .num_remark #ActionOfOrthogonalOnSphere}
###### Remark

Via this presentation the $n$-sphere inherits from the canonical [[action]] of the [[orthogonal group]] $O(n)$ on $\mathbb{R}^n$ an [[action]] of $O(n)$ on $S^n$ (by [[continuous maps]]) which preserves the base point (the "point at infinity").

=--

+-- {: .num_defn #AutoequivalencesOfnSphere}
###### Definition

For $n \in \mathbb{N}$ write $H(n)$ for the [[automorphism ∞-group]] of homotopy self-equivalences $S^n \longrightarrow S^n$, hence

$$
  H(n) \coloneqq Aut_{\infty Grpd^{\ast/}}(S^n)
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

The [[∞-group]] $H(n)$, def. \ref{AutoequivalencesOfnSphere}, constitutes the two [[connected components]] of the $n$-fold based [[loop space]] $\Omega^n S^n$ corresponding to  the [[homotopy groups]] $\pm 1 \in \pi_n(S^n)$.

=--

+-- {: .num_defn #OrthogonalActionOnSphereOnHomotopyGroups}
###### Definition

For $n \in \mathbb{N}$ the action of $O(n)$ on $S^n$
of remark \ref{ActionOfOrthogonalOnSphere} induces a canonical
homomorphism

$$
  O(n) \longrightarrow Aut_{\infty Grpd^{\ast/}}(S^n)
  \,.
$$

This in turn induces for each $i \in \mathbb{N}$ homomorphisms of [[homotopy groups]] of the form

$$
  \pi_i(O(n)) \longrightarrow \pi_i(\Omega^n S^n) \simeq \pi_{n+i}(S^n)
  \,.
$$


=--

+-- {: .num_prop #OrthogonalActionOnSphereOnHomotopyGroups}
###### Proposition

The homomorphism of remark \ref{OrthogonalActionOnSphereOnHomotopyGroups} are compatible with  [[suspension]] and therefore induce homomorphisms

$$
  \pi_i(O) \longrightarrow \pi_i(\mathbb{S})
$$

from the [[homotopy groups]] of the [[stable orthogonal group]]
to the [[stable homotopy groups of spheres]].

=--

This is the J-homomorphisms on [[homotopy groups]].

## Related concepts

* [[orientation in generalized cohomology]]

## References

The J-homomorphism was introduced in 

* [[George Whitehead]], _On the homotopy groups of spheres and rotation groups_, Annals of Mathematics. Second Series 43 (4): 634&#8211;640 (1942), ([JSTOR](http://www.jstor.org/stable/1968956)).

Lecture notes include

* [[Akhil Mathew]], _Notes on the J-homomorphism_ ([pdf](http://people.fas.harvard.edu/~amathew/j.pdf))

Discussion in the modern perspective of [[higher algebra]] is for instance in 

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_ ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))

[[!redirects J-homomorphisms]]
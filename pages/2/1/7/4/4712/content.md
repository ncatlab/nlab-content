
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

A _nonabelian bundle gerbe_ is a model for the [[Lie groupoid]] which is the total space of a smooth $AUT(H)$-[[principal 2-bundle]] for $AUT(H)$ the [[Lie 2-group]] that is the [[automorphism 2-group]] of a [[Lie group]] $H$.

Specifically, a nonabelian bundle gerbe on a [[smooth manifold]] $X$ is given by a [[surjective submersion]] $Y \to X$ and an $H$-[[bibundle]] $P \to Y\times_X Y$ together with a morphism of $H$-bibundles

$$
  \mu : \pi_0^* P \otimes \pi_2^* P \to \pi_1^* P
$$

that is associative in the evident sense. This construction serves to model [[pullback]]s of [[Lie 2-groupoid]]s of the form

$$
  \array{
    \tilde P &\to& \mathbf{E}AUT(H)
    \\
    \downarrow && \downarrow
    \\
    C(Y) &\stackrel{g}{\to}& \mathbf{B}AUT(H)
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    X
  }
  \,,
$$

where on the rght we have the [[universal principal infinity-bundle|universal principal 2-bundle]].

The resulting [[Lie groupoid]] $\tilde P$ is an extension of the [[Cech groupoid]] $C(Y)$ by $AUT(H)$.
This generalizes the case of ordinary [[bundle gerbe]]s, which are models for $\mathbf{B}U(1)$-principal 2-bundles, for $\mathbf{B}U(1)$ the <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#BnU1">circle 2-group</a>.

## References

* Paolo Aschieri, Luigi Cantini, [[Branislav Jurco]], _Nonabelian Bundle Gerbes, their Differential Geometry and Gauge Theory_ ([arXiv:hep-th/0312154](http://arxiv.org/abs/hep-th/0312154))



[[!redirects nonabelian bundle gerbes]]
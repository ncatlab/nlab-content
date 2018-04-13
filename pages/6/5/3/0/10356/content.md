
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[string theory]], [[D-branes]] appear in a "[[prequantum field theory|prequantum]]" version and in a more refined quantum version. A [[D-brane charge]] is an element in the [[twisted K-theory|twisted]] [[equivariant K-theory]] of [[spacetime]], and the [[quantization]] of a prequantum D-brane given by a [[submanifold]] [[worldvolume]] carrying a [[Chan-Paton bundle]] is the [[push-forward in generalized cohomology|push-forward]] of this [[equivariant vector bundle]] along the embedding. If the embedding is not into a [[fixed point]] of the [[orbifold]] [[action]], then under this push-forward the [[D-brane charge]] is a sum of generating classes in twisted equivariant K-theory. Therefore the "quantum" D-branes corresponding to these generating classes of [[equivariant K-theory]] are called the _fractional D-branes_ (as the others are "composed" of these). They can usually be obtained by [[motivic quantization|quantization]]/push-forward of [[Chan-Paton gauge fields]] placed at orientifold fixed-points


More in detail, for $X$ a [[spacetime]], possibly an [[orbifold]], carrying a [[B-field]] which is modulated (as discussed there) by a map $\chi \;\colon\; X \longrightarrow \mathbf{B}^2 U(1)$, then a [[prequantum field theory|prequantum]] [[boundary field theory|boundary condition]] for the [[open string]] [[sigma-model]] charged under this [[B-field]] is a [[diagram]] of the form

$$
  \array{
    && Q
    \\
    & \swarrow && \searrow^{\mathrlap{i}}
    \\
     \ast && \swArrow_\xi && X
     \\
     & \searrow && \swarrow_{\chi}
     \\
     && \mathbf{B}^2 U(1)
     \\
     && \downarrow^{\mathrlap{\rho}}
    \\
     && KU Mod
  }
  \,.
$$

Typically here $i \colon Q \hookrightarrow X$ is assumed to be a [[submanifold]], or in the $G$-[[orbifold]] case a $G$-equivariant embedding of a $G$-principal bundle on $Q$ (a map of the corresponding [[smooth stacks]]).

Here $Q$ is then the [[worldvolume]] of the [[prequantum field theory|prequantum]] [[D-brane]], $\xi$ is the (underlying [[instanton sector]] of the) [[Chan-Paton gauge field]] that it carries. 

If the [[Freed-Witten anomaly cancellation]] condition holds, which says that $i$ has [[K-orientation]] in $\chi$-[[twisted K-theory|twisted]] (and [[equivariant K-theory|equivariant]]) [[complex K-theory]], then this diagram has a [[motivic quantization]] to a map of [[KU]]-[[infinity-modules|modules]]

$$
  KU^\bullet(\ast) \stackrel{i_! \xi}{\longrightarrow}
  KU^{\bullet + \chi}(X)
$$

given by the [[push-forward in generalized cohomology|push-forward]]/relative [[index]] of the [[Chan-Paton gauge field]] in [[topological K-theory]] from the [[worldvolume]] $Q$ to [[spacetime]] $X$.

This is equivalent an element

$$
  ind_i(\xi) \in KU^{\bullet + \chi}(X)
$$

in the $\chi$-[[twisted K-theory]] of $X$, and as such it is called the [[D-brane charge]].

Not every element of the twisted K-theory may arise this way. We may think of a general morphism

$$
  q
  \;\colon\;
  KU^\bullet(\ast) \stackrel{}{\longrightarrow}
  KU^{\bullet + \chi}(X)
$$

as a quantum [[boundary field theory|boundary condition]], hence as a "quantum" [[D-brane]] for the [[open string]] [[sigma-model]]. These include all elements of the twisted K-theory, in particular the generators. These generators are called the _fractional D-branes_.

In particular, in the simple case that $X = \mathbb{C}^n/\Gamma$ is the global [[orbifold]] of a [[finite group]] acting on a [[Cartesian space]], the [[complex K-theory]] corresponds to the [[representation ring]] of $\Gamma$. In this case the fractional branes correspond simply to the [[irreducible representations]] of $\Gamma$.


## Related concepts

* [NS5 half-brane](NS5-brane#NSHalfBranes)


## References

Early discussion in physics language include

* Diaconescu, [[Michael Douglas]], [[Jaume Gomis]], _Fractional Branes and Wrapped Branes_, JHEP 9802:013,1998 ([arXiv:hep-th/9712230](http://arxiv.org/abs/hep-th/9712230))

The mathematical meaning is stated relatively clearly for instance on the bottom of p. 3 of 

* [[Emil Martinec]], [[Gregory Moore]], _On Decay of K-theory_ ([arXiv:hep-th/0212059](http://arxiv.org/abs/hep-th/0212059))


[[!redirects fractional D-branes]]

[[!redirects fractional brane]]
[[!redirects fractional branes]]

[[!redirects half-brane]]
[[!redirects half-branes]]

[[!redirects half brane]]
[[!redirects half branes]]


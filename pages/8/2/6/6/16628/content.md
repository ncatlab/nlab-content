
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Bloch group_ $\mathcal{B}(\mathbb{C})$ is the [[quotient]] of the degree-3 [[group homology]] $H_3^{grp}(\flat PSL(2,\mathbb{C}), \mathbb{Z})$ of the [[complex numbers|complex]] [[projective linear group]] $PSL(2,\mathbb{C})$ (with [[discrete topological space|discrete topology]]) by its [[torsion subgroup]], which is $\mathbb{Q}/\mathbb{Z}$.

Accordingly $H_3^{grp}(\flat PSL(2,\mathbb{C}), \mathbb{Z})$ itself is also called the _extended Bloch group_ ([Neumann 04](#Neumann04)).

## Properties


### Relation to hyperbolic 3-manifolds
 {#RelationToHyperbolic3Manifolds}

The [[fundamental class]] of a [[hyperbolic 3-manifold]] $X$ canonically gives an element in the Bloch group: let $X = \mathbb{H}^3/\Gamma$ for $\Gamma\hookrightarrow PSL(2,\mathbb{C})$, then the [[homotopy type]] of $X$ is that of $B\Gamma$ and hence the fundamental class maps forward under

$$ 
  H_3(X,\mathbb{Z})
  \simeq
  H_3(B \Gamma, \mathbb{Z})
  \simeq
  H_3^{grp}(\Gamma, \mathbb{Z})
  \longrightarrow
  H_3^{grp}(\flat PSL(2,\mathbb{C}), \mathbb{Z})
  \longrightarrow
  H_3^{grp}(\flat PSL(2,\mathbb{C}), \mathbb{Z})/(\mathbb{Q}/\mathbb{Z})
  \,.
$$

(e.g. [Neumann 11, section 2.2](#Neumann11))

### Cheeger-Simons class and complex volume
 {#RelationToCheegerSimonsClass}

There is a group [[homomorphism]]

$$
  \hat c
  \colon
  H_3(\flat PSL(2,\mathbb{C}), \mathbb{Z})
  \longrightarrow
  \mathbb{C}/\pi^2 \mathbb{Z}
$$

such that when applied to a [[fundamental class]] $[X]$ of a
[[hyperbolic 3-manifold]] according to the [above](#RelationToHyperbolic3Manifolds), then it yields its [[complex volume]]

$$
  \hat c([X]) = cs(X) + i vol(X)
  \,.
$$

This is called the _[[Cheeger-Simons class]]_.

(e.g. [Neumann 11, section 2.3](#Neumann11))

### Relation to algebraic K-theory

Up to [[torsion subgroups]], the extended Bloch group of a is isomorphic to the third [[algebraic K-theory]] group $K_3^{ind}(\mathbb{C})$ ([Suslin90](#Suslin90), [Zickert 09](#Zickert09)).

### Relation to the Borel regulator

For $k$ an [[algebraic number field]] and $\{\sigma_i \colon k \hookrightarrow \mathbb{C}\}$ its complex embeddings, write

$$
  vol_i \coloneqq vol \circ (\sigma_i)_\ast \colon 
  H_3(PSL(2,k),\mathbb{Z})
  \to 
  \mathbb{R}
$$

for the induced volume measures, using the [[Cheeger-Simons class]] from [above](#RelationToCheegerSimonsClass). The [[direct product]] of these volumes is called the _[[Borel regulator]]_

$$
  Borel \coloneqq (vol_1, \cdots, vol_{r_2})
  \colon
  H_3(PSL(2,\mathbb{C}), \mathbb{Z})
  \longrightarrow
  \mathbb{R}^{r_2}
  \,.
$$

(e.g. [Zickert 09, (1.2)](#Zickert09))

Now the point is that restricted to the Bloch group proper the Borel regulator is [[injective]].

(e.g. [Neumann 11, theorem 2.4](#Neumann11))

## Related concepts

* [[hyperbolic manifold]]

* [[Cheeger-Simons class]], [[complex volume]]

* [[Borel regulator]]

## References

* {#Neumann04} [[Walter Neumann]], _Extended Bloch group and the Cheeger-Chern-Simons class_, Geom. Topol. 8 (2004) 413-474 ([arXiv:math/0307092](http://arxiv.org/abs/math/0307092))

The relation to [[algebraic K-theory]] and the [[Borel regulator]] is due to

* Chih-Han Sah, _Homology of classical Lie groups made discrete. III._, J. Pure Appl. Algebra, 56(3):269&#8211;312, 1989.

* {#Suslin90} [[Andrei Suslin]]. _$K_3$ of a field, and the Bloch group_. Trudy Mat. Inst. Steklov., 183:180&#8211;199, 229, 1990. Translated in Proc. Steklov Inst. Math. 1991, no. 4, 217&#8211;239, Galois theory, rings, algebraic groups and their applications (Russian).

* {#Zickert09} [[Christian Zickert]], _The extended Bloch group and algebraic K-theory_ ([arXiv:0910.4005](http://arxiv.org/abs/0910.4005))

Review is in

* {#Neumann11} [[Walter Neumann]], section 2.4 _Realizing arithmetic invariants of hyperbolic 3-manifolds_, Contemporary Math 541 (Amer. Math. Soc. 2011), 233--246 ([arXiv:1108.0062](http://arxiv.org/abs/1108.0062))

[[!redirects Bloch groups]]
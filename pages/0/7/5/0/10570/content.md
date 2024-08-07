
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given a sequence of inclusions

$$
  T \subset B \subset G
$$

where

* $G$ is a [[connected topological space|connected]] [[complex geometry|complex]] [[reductive group|reductive]] [[algebraic group]]

* $B$ is a [[Borel subgroup]]

* $T$ is a [[maximal torus]];

this induces

* the [[Weyl group]] $W_0 = N(T)/T$;

* the [[character lattice]] $\mathfrak{h}_{\mathbb{Z}}^\ast = Hom(T, \mathbb{C}^\times)$;

* the [[cocharacter lattice]] $\mathfrak{h}_{\mathbb{C}} = Hom(\mathbb{C}^\times, T)$.

* a _[[standard parabolic subgroup]]_ of $G$ is a subgroup $P_J$ including $B$ such that $G/P$ is a [[projective variety]];

   [[parabolic subgroup]] is one [[conjugation|conjugate]] to the standard parabolic subgroup.

* the [[flag variety]] $G/B$;

* the _[[partial flag varieties]]_ $G/P_J$


A **Bruhat decomposition** is, if it exists, a [[coproduct]] decomposition into a disjoint union of [[double cosets]]

$$
  G = \underset{w \in W_0}{\coprod} B w B
$$

$$
  G =  \underset{u \in W^J}{\coprod} B u P_j
$$

with 

* $W_J \coloneqq \{v \in W_0 | v T  \subset P_J\}$

* $W^J \coloneqq \{coset\; representatives\; u \; of \; cosets \; in W_0/W_J\}$

into [[Schubert varieties]] 

$$
  X_w = \overline{B w B} \subset G/B
$$

$$
  X_u^J = \overline{B u P_J} \subset G/P_J
  \,.
$$


## Related concepts

* [[Schubert calculus]]

## References

Named after [[François Bruhat]].

See also:

* [[Daniel Bump]], *The Bruhat decomposition*, chapter 27 in: *Lie groups*, Graduate Texts in Mathematics **225**, Springer (2013) &lbrack;[doi:10.1007/978-1-4614-8024-2](https://doi.org/10.1007/978-1-4614-8024-2), [pdf](https://www-fourier.ujf-grenoble.fr/~panchish/ETE%20LAMA%202018-AP/lecturesZETAS2018/BumpD-Lie%20groups.pdf)&rbrack;



* Wikipedia, _[Bruhat decomposition](http://en.wikipedia.org/wiki/Bruhat_decomposition)_


[[!redirects Bruhat decompositions]]


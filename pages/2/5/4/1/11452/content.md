
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
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

## Idea

In the context of [[real-oriented cohomology theory]], notably in _[[KR-theory]]_, by "real space" (real manifold) one means a [[space]] ([[manifold]]) equipped with an [[action]] of the [[group of order 2]] $\mathbb{Z}/2\mathbb{Z}$ (a "non-linear [[real structure]]").

In the context of [[string theory]] real spaces appear as [[orientifold]] [[target space|target]] [[spacetimes]]. The involution [[fixed points]] here are known as _[[O-planes]]_.

## Examples

### Real circles

There are three non-equivalent real structures on the [[circle]] $S^1$, usually denoted

* $S^{2,0}$ for the trivial involution;

* $S^{1,1}$ for the reflection involution (identifying the two semi-circles);

* $S^{0,2}$ for the antipodal involution (rotation by $\pi$).

Accordingly [[real-oriented cohomology theory]] is bigraded in a way modeled on this bigrading.

(This is standard notation, but maybe $S^{1,0}$, $S^{\tfrac{1}{2}, \tfrac{1}{2}}, S^{0,1}$ would be more suggestive. Indeed the quotients in the first and the last case are actually circles, while in the second case it is the semi-circle.)

### Complexified cartesian spaces

The complex $n$-dimensional complexified cartesian space ${\mathbb{C}}^n$ equipped with its conjugative involution is a real space. Explicitly, this involution sends $(z^1,\ldots, z^n)$ to $(\bar{z^1},\ldots, \bar{z^n})$.

### Complex projective spaces.

The complex $n$-dimensional complex projective space ${\mathbb{P}}^n_{\mathbb{C}}$ equipped with a conjugation involution is a real space. For each choice of affine chart, the conjugation involution of this chart (which is biholomorphic to ${\mathbb{C}}^n$) extends to a conjugation involution on ${\mathbb{P}}^n_{\mathbb{C}}$. Any two conjugation involutions are ${\mathbb{Z}}/2$-equivariantly diffeomorphic.

For example, the Riemann surface ${\mathbb{P}}^1_{\mathbb{C}}$ is diffeomorphic to the 2-sphere $S^2$ and its conjugation involution is the antipodal action.

### Complex general and special linear groups.

For $A$ a square matrix, the determinant of its conjugation transpose equals the conjugate of its determinant. In symbols, ${\mathrm{det}} A^* = \overline{{\mathrm{det}} A}$. Hence sending a square matrix to its conjugate transpose is an involution on the complex general $GL(n,{\mathbb{C}})$ and special $SL(n,{\mathbb{C}})$.

In particular, the real space $SL(1,{\mathbb{C}})$ equipped with this conjugate transpose involution is equivariantly diffeomorphic to $S^{0,2}$, the circle equipped with its antipodal action (dicussed above).

## Properties

### Relation to real cobordism

There is a "real" analog of [[complex cobordism cohomology theory]] $MU$, the [[MR cohomology theory]] $M \mathbb{R}$.

While $\pi_\bullet(M \mathbb{R})$ is _not_ the [[cobordism ring]] of [[real manifolds]], still every [[real manifold]] does give a class in $M \mathbb{R}$ ([Kriz 01, p. 13](#Kriz01)). For details see here: [pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm161/fm16115.pdf).


## Related concepts

* [[equivariant cohomology]]

## References

* {#Atiyah66} [[Michael Atiyah]], _K-theory and reality_, The Quarterly Journal of Mathematics. Oxford. Second Series 17 (1) (1966),: 367&#8211;386, doi:10.1093/qmath/17.1.367, ISSN 0033-5606, MR 0206940

* {#Kriz01} [[Igor Kriz]], _Real-oriented homotopy theory and an analogue of the
Adams}Novikov spectral sequence_, Topology 40 (2001) 317-399 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/hukriz.pdf))


[[!redirects real spaces]]

[[!redirects real manifold]]
[[!redirects real manifolds]]


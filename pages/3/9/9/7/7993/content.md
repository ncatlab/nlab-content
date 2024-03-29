
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In the context of _[[geometric quantization]]_ a _metaplectic correction_ is a choice of [[metaplectic structure]] on the given [[symplectic manifold]]. It allows to make the [[space of states (in geometric quantization)|space of states]] into a [[Hilbert space]].

It is called a _correction_ mostly for historical reasons, since it was not included in all constructions from the beginning. 

## Properties

### Induced inner product / Hilbert space structure
 {#InducedInnerProduct}

A [[metaplectic structure]] on a [[symplectic manifold]] $(X, \omega)$ induces a [[metalinear structure]] on each [[Lagrangian submanifold]] $Q \hookrightarrow X$ of a given [[foliation]] by Lagrangian submanifolds ([[polarization]]). This allows to form a [[square root]] line bundle $\sqrt{\Lambda^n T^* Q}$ of the [[canonical bundle]] of $Q$ (a "[[Theta characteristic]]", see [below](#RelationToSpinCStructure)) and hence induces an [[inner product]] on [[sections]] of the [[tensor product]] $E|_Q \otimes \sqrt{\Lambda^n T^* Q}$ with the restriction of any [[line bundle]] $E$ on $X$ (a prequantum line bundle, notably).

### Relation to $Spin$-structure and $Spin^c$-structure
 {#RelationToSpinCStructure}

Let $(X,\omega)$ be a [[compact topological space|compact]] [[symplectic manifold]] equipped with a [[Kähler polarization]] $\mathcal{P}$ hence a [[Kähler manifold]] structure $J$. A metaplectic structure is now a choice of [[square root]] $\sqrt{\Omega^{n,0}}$ of the [[canonical line bundle]] $\Omega^{n,0}$ (a [[Theta characteristic]] for the [[complex analytic space]] $X$). This is equivalently a [[spin structure]] on $X$ (see the discussion at _[spin structure -- over K&#228;hler manifolds](spin%20structure#OverAKahlerManifold)_).

Now given a [[prequantum line bundle]] $L_\omega$, in this case the [Dolbault quantization](geometric+quantization#IndexOfDolbeaultDiracOperator) of $L_\omega$ coincides with the [[spin^c quantization]] of the [[spin^c structure]] induced by $J$ and $L_\omega \otimes \sqrt{\Omega^{n,0}}$.

This appears as ([Paradan 09, prop. 2.2](#Paradan09)).





### Relation to geometric quantization

See at 

* _[geometric quantization -- Quantum space of states](#geometric+quantization#GeometricQuantizationProper)_.

## Related concepts

* [[metaplectic group]]

[[!include square roots of line bundles - table]]

## References

For general discussion see the references listed at _[[geometric quantization]]_, for instance the introduction in section 7.2 of

* Sean Bates, [[Alan Weinstein]], _Lectures on geometric quantization_ ([pdf](http://math.berkeley.edu/~alanw/GofQ.pdf))

or

* [[Martin Schottenloher]], _Metaplectic reduction_ ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/GQ/12%20Metaplectic%20Correction.1.1.pdf))

* Alexander Cardona, _Geometric and metaplectic quantization_ ([pdf](http://pentagono.uniandes.edu.co/~acardona/GMQ.pdf))

Relation to [[spin^c quantization]] is discussed in 

* [[Paul-Emile Paradan]], _Spin-quantization commutes with reduction_, J. Symplectic Geom. Volume 10, Number 3 (2012), 389-422. ([arXiv:0911.1067](http://arxiv.org/abs/0911.1067), [Euclid](http://projecteuclid.org/euclid.jsg/1350392491))
 {#Paradan09}

Discussion with an eye towards [[Theta characteristics]] is in 

* [[Andrei Tyurin]], _Quantization, classical and quantum field theory and Theta-functions_ ([arXiv:math/0210466v1](http://arxiv.org/abs/math/0210466v1))


Further references include

* L. Charles, _Semi-classical properties of geometric quantization with metaplectic correction_ ([arXiv:math.SG/0602168](http://arxiv.org/abs/math.SG/0602168))

[[!redirects metaplectic correction]]
[[!redirects metaplectic corrections]]

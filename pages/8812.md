
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $X$ a [[smooth manifold]], $E \to X$ a [[vector bundle]] and $D : \Gamma(E) \to \Gamma(E)$ a [[linear differential operator]] on [[sections]] of $E$, its **symbol** is the bundle morphism

$$
   \sigma(D) \;:\; T^* X \otimes_X E \to E
$$

from the [[tensor product of vector bundles]] with the [[cotangent bundle]] which is given at any point $x \in X$ on a [[cotangent vector]] of the form $(\mathbf{d}f)_x \in \Gamma(T^* X)_x$ by

$$
  \sigma(D)_x \;\colon\; \mathbf{d}f_x \mapsto [D,f]_x
  \,,
$$

where in the [[commutator]] on the right we regard multiplication by $f$ as an [[endomorphism]] of $\Gamma(E)$.

The symbol may naturally be thought of as an element in the [[K-theory]] of $X$ ([Freed](#Freed)).

Generally, the symbol of a possibly non-linear [[differential operator]] is similarly the map on the [[cotangent bundle]] given by "replacing [[partial derivatives]] by [[covectors]]" in the definition of the differential operator. In this case the _principal symbol_ is the highest degree [[homogeneous function|homogeneous]] component of the symbol.

## Examples

+-- {: .num_defn #SymbolMap}
###### Definition
**([[symbol map]])**

For $X = \mathbb{R}^n$ a [[Cartesian space]] and $D$ the [[Dirac operator]] of the [[flat connection]], the symbol of $D$ reproduces the [[symbol map]] between [[differential forms]] and [[Clifford algebra]] elements.

=--

+-- {: .num_example #BicharacteristicFlow}
###### Example
**([[bicharacteristic flow]])**

For $E$ a [[real vector bundle|real]] [[trivial line bundle]] then the principal symbol is equivalently just a real-valued [[smooth function]] on the [[cotangent bundle]]. Since any cotangent bundle is canonically a [[symplectic manifold]], in this case the symbol may be regarded as a [[Hamiltonian]] funtion. The corresponding [[Hamiltonian flow]] is called the _[[bicharacteristic flow]]_ of the given differential operator.

=--

## Related concepts

* [[symbol order]]

* [[elliptic differential operator]], [[elliptic chain complex]]

* [[hyperbolic differential operator]]

* [[propagation of singularities theorem]]

## References


* [[Nigel Higson]], [[John Roe]], chapter 2.5 of  _Lectures on operator K-theory and the Atiyah-Singer Index Theorem_ ([pdf](http://folk.uio.no/rognes/higson/Book.pdf))

* {#Freed} [[Dan Freed]], _Geometry of Dirac operators_ ([pdf](http://www.ma.utexas.edu/users/dafr/DiracNotes.pdf))
 
See also

* Wikipedia, _[Symbol of a differential operator](http://en.wikipedia.org/wiki/Symbol_of_a_differential_operator)_

[[!redirects principal symbol]]
[[!redirects principal symbols]]


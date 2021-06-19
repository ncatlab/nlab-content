+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A __dyadic rational algebra__ or __dy-algebra__ is an [[associative unital algebra]] over the [[dyadic rational numbers]]

## Examples

The [[decimal rational numbers]] $\mathbb{Z}[1/10]$, the [[rational numbers]] $\mathbb{Q}$, and the [[real numbers]] $\mathbb{R}$ are dyadic rational algebras. 

Any $\mathbb{R}$-algebra, such as the [[complex numbers]], [[quaternions]], and finite dimensional [[Clifford algebras]] over the real numbers, is also a dyadic rational algebra. 

## Properties

Every dyadic rational algebra is a [[symmetric midpoint algebra]] with the midpoint operation given by 

$$
  a \vert b \coloneqq \frac{1}{2} (a + b)
$$

### Symmetric and commutator products

In any dyadic rational algebra, one can define the __symmetric product__ to be

$$
  a \cdot b \coloneqq \frac{1}{2} (a b + b a)
$$

and the __commutator product__ to be 

$$
  a \times b \coloneqq \frac{1}{2} (a b - b a)
$$

The symmetric product in a dyadic rational algebra is [[commutative]]:

$$
  a \cdot b = b \cdot a
$$

while the commutator product is anticommutative

$$ 
  a \times b = -(b \times a)
$$

and satisfiea the [[Jacobi identity]]

$$
  a \times (b \times c) + b \times (c \times a) + c \times (a \times b) = 0
$$

The bivector subalgebra of a [[Clifford algebra]] over the real numbers with the commutator product provides a model for [[spin geometry]] and [[Lie groups]], and the vector submodule of a Clifford algebra over the real numbers with the symmetric product is an [[inner product space]]. 

## Related concepts

* [[dyadic rational number]]

* [[dyadic rational module]]

* [[symmetric midpoint algebra]]

* [[Clifford algebra]]

* [[geometric algebra]]

* [[spin geometry]]

## References

The relation to symmetric midpoint algebras could be found in 

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

The symmetric and commutator product is defined in this reference for Clifford algebras over the real numbers, but the definition is valid in any dyadic rational algebra: 

* [[Chris Doran]], Anthony Lasenby, _Geometric algebra for physicists_, Cambridge University Press (2003) ([pdf](http://catdir.loc.gov/catdir/samples/cam033/2002035182.pdf))
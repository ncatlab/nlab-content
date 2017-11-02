
#Contents#
* table of contents
{:toc}

## Definition

A **unitary operator** is a [[unitary morphism]] in the [[†-category]] [[Hilb]].

Explicitly, this means the following.

### Unitary operators

A **unitary operator** $U$ on a [[Hilbert space]] $\mathcal{H}$ is a bounded linear operator $U: \mathcal{H} \to \mathcal{H}$  that satisfies

$U^{*}U=U U^{*}=I$

where $U^{*}$ is the [[Hilbert space adjoint]] of $U$ and $I$ is the [[identity]] operator.  This property is equivalent to saying that the range of $U$ is dense and that $U$ preserves the inner product $\langle \cdot,\cdot\rangle$ on the Hilbert space.  An operator is unitary if and only if $U^{-1}=U^{*}$.

Unitary operators are the [[isomorphism]]s of Hilbert spaces since they preserve the basic structure of the space, e.g. the topology.  The group of all unitary operators from a given Hilbert space to itself is sometimes called the [[unitary group]] $U(\mathcal{H})$ or  _Hilbert group_ of $H$ and is denoted Hilb($H$).

Sometimes operators may only obey the _[[isometry]]_ $U^{*}U=I$ or the _[[coisometry]]_ $U U^{*}=I$.

The generalization of a unitary operator is called a _unitary element_ of a [[unital algebra|unital]] [[star-algebra|*-algebra]].

### Unitary matrices

If a basis for a finite dimensional Hilbert space is chosen, the defnition of unitary operator reduces to that of unitary matrix.

A unitary matrix is an $n \times n$ matrix with complex entries that satisfies the condition

$U^{*}U=U U^{*}=I_{n}$.

This is equivalent to saying that both the rows and the columns of $U$ form an orthonormal basis in $\mathbb{C}^{n}$ with respect to the respective inner product.  $U$ is also a [[normal matrix]] whose [[eigenvalue]]s lie on the unit circle.

## Notation

The notation used here for the adjoint, $U^{*}$, is commonly used in linear algebraic circles (as is $U^{H}$).  In [[quantum mechanics]], $U^{\dagger}$ is exclusively used for the adjoint while $U^{*}$ is interpreted as the same thing as $\bar{U}$, i.e. the complex conjugate.

## Examples

* In [[harmonic analysis]], [[Parseval's theorem]] says that the [[Fourier transform]] is a unitary operator.

## Related concepts

* [[unitary group]]

* [[special unitary group]]

* [[Hermitian operator]]

[[!redirects unitary operators]]
[[!redirects unitary]]

[[!redirects unitary linear operator]]
[[!redirects unitary linear operators]]

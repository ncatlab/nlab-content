


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn #HermiteNormalForm}
###### Definition
**(Hermite normal form)**

A [[matrix]] 

$$
  H \in Mat_{n \times m}(\mathbb{Z})
$$ 

with [[integer]] entries ($n$ rows, $m$ columns) is said to be in _Hermite normal form_ if the following conditions hold:

1. All entries are [[non-negative numbers]] $\in \mathbb{N} \subset \mathbb{Z}$:

   $$
     H_{i j} \geq 0
     \,.
   $$

1. The first non-vanishing entry $p_{i} \coloneqq H_{i,j_{i}}$ in each row is strictly to the right of the first non-vanishing entry $p_{i-1} = H_{i,j_{i-1}}$ of the previous row (if any):

   $$
     j_{ i} \gt j_{i - 1}
   $$

   These entries are called the _pivots_ of $H$.

1. Each pivot $p_i$ is strictly larger than all entries above it in the same row:

   For $1 \leq i' \lt i$ we have $H_{i', j_i} \lt p_i = H_{i, j_i}$.

=--

(e.g. [Mader 00, theorem 1.5.1](#Mader00))

+-- {: .num_remark}
###### Remark

There are slightly different conventions in use for Def. \ref{HermiteNormalForm}, e.g. some authors require the non-vanishing non-pivotal entries to be negative instead of positive. These conventions are equivalent, in that the uniqueness of Hermite normal form, Theorem \ref{UniquenessOfHermiteNormalForm} below applies with respect to each of them.

=--

## Properties

### Uniqueness

+-- {: .num_theorem #UniquenessOfHermiteNormalForm}
###### Theorem
**(uniqueness of Hermite normal form)**

For 

$$
  M \in Mat_{n \times m}(\mathbb{Z})
$$ 

a [[matrix]] with [[integer]] entries, there exists a _unique_ [[invertible matrix]] with [[integer]] coefficients

$$
  U \;\in\; GL(n, \mathbb{Z}) \subset Mat_{n \times n}(\mathbb{Z})
$$

such that the [[matrix product]]

$$
  H \;\coloneqq\; U \cdot M
$$

has Hermite normal form (Def. \ref{HermiteNormalForm}).

=--

Existence follows by integer row reduction of integer matrices, see e.g. [Gilbert-Pathria 90, p. 3/4](#GilbertPathria90). Uniqueness requires more work (see e.g. [Mader 00, theorem 1.5.2](#Mader00)).

## Related concepts

* [[Smith normal form]]

* [[Gram-Schmidt process]]

## References

Integer row reduction for integer matrices via [[greatest common divisors]] is explained for instance in 

* {#GilbertPathria90} William Gilbert, Anu Pathria, _Linear Diophantine Equations_, 1990 ([pdf](https://www.math.uwaterloo.ca/~wgilbert/Research/GilbertPathria.pdf), [[GilbertPathria90.pdf:file]])

Discussion of the general theory of integer matrices includes

* {#Mader00} A. Mader, section 1.5 of _Almost completely decomposable groups_, CRC Press 2000

Computational implementation is discussed in

* George Labahn, Vincent Neiger, Wei Zhou, _Fast, deterministic computation of the Hermite normal form and determinant of a polynomial matrix_ ([arXiv:1607.04176](https://arxiv.org/abs/1607.04176))

See also 

* Wikipedia, _[Hermite normal form](https://en.wikipedia.org/wiki/Hermite_normal_form)_

[[!redirects Hermite normal forms]]
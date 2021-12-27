

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Exceptional structures
+-- {: .hide}
[[!include exceptional structures -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

24 is the [[natural number]] that follows 23 and precedes 25. It occurs in modern systems of measurement for historical reasons, thanks ultimately to its having many [[prime factors]]

$$
  24
  \,=\,
  2 \cdot 2 \cdot 2 \cdot 3 
$$

and it arises in many circumstances in [[mathematics]] and [[physics]], the relations between which are not always immediately apparent.

## Examples

### Modular arithmetic

Fix a [[natural number]] $n$, and consider those numbers $x$ whose squares are congruent to 1 [[modulo]] $n$:

\[ x^2 \equiv 1 (\mod n) \, . \]

A necessary condition for satisfying this is for $x$ and $n$ to be [[coprime integer|coprime]]. For some choices of $n$, this condition is sufficient, i.e., every $x$ coprime to $n$ satisfies this congruence. In fact, this congruence is equivalent to $gcd(x,n) = 1$ if and only if $n$ divides 24.

### Cannonball problem

The cannonball problem asks what size square pyramids can be made by stacking spheres such that the total number of spheres is a square number. Apart from the trivial solutions involving 0 spheres or 1 sphere, the only solution is a pyramid 24 layers tall:

\[ 0^2 + 1^2 + 2^2 + \cdots + 24^2 = 70^2 \, . \]

### Leech lattice

The [[Leech lattice]] is a "universally optimal" packing of hyperspheres in $\mathbb{R}^{24}$ originally discovered in [[coding theory]]. Surprisingly, it is closely related to the cannonball problem, since it can be constructed from a Lorentzian lattice in two higher dimensions by a method that uses the fact that

\[ v = (0, 1, 2, \ldots, 24, 70) \]

has zero norm under that metric.

### Mathieu groups

The largest [[Mathieu group]], $M_{24}$, is the [[automorphism group]] of a [[Steiner system]] containing 24 blocks. $M_{24}$ is also the automorphism group of the [[binary Golay code]], an [[abelian group]] which is a 12-dimensional subspace of the [[vector space]] $\mathbb{F}_2^{24}$.

The binary Golay code can be used to construct the Leech lattice. Essentially, each codeword defines a point in 24-dimensional space, and we can fill in and build out this set. In more detail: Let $c$ be a Golay codeword, scale it by a factor 2, and add either $4x$, where $x$ is a vector in $\mathbb{Z}^{24}$ whose components sum to an even number, or $1 + 4y$ where $y \in \mathbb{Z}^{24}$ and its components sum to an odd number.

### 24-cell and the binary tetrahedral group

The [[24-cell]] is a four-dimensional [[regular polytope]] with 24 vertices. Interpreting these vertices as [[quaternion]]s, they form a [[group]] under quaternion multiplication, and this group is [[isomorphism|isomorphic]] to the [[binary tetrahedral group]].

### Third stable homotopy group of spheres

The [[third stable homotopy group of spheres]] is the [[cyclic group]] of order 24.

### String theory

Critical [[bosonic string theory|Bosonic string theory]] requires 26 [[spacetime]] [[dimension of a manifold|dimensions]] of [[target spacetime]] (for vanishing [[dilaton]], at least), which can be broken down into 2 dimensions for the string [[worldsheet]] itself and 24 transversal directions for its oscillations. 

This is also related to the conventional choice of normalization for the [[central charge]] of the [[Virasoro algebra]]:

\[ [L_m, L_n] = (m - n) L_{m+n} + \frac{c}{12}(m^3 - m) \delta_{m+n,0} \, . \]

Several classes of [[string theory vacua]] require the presence of exactly [[24 branes transverse to K3|24 branes of codimension 4]] transverse to a [[K3-surface]]-[[fiber]].


## Related concepts

Appearances of 24 and its factors, particularly 8 and 12, are a meta-pattern in mathematics; another such meta-pattern is [[ADE classification]]. Sometimes these meta-patterns overlap. 

For example, [[tesselation|tessellating]] $\mathbb{R}^4$ with regular 24-cells creates the 24-cell honeycomb, in which the centers of the 24-cells are the points of the $D_4$ lattice. Meanwhile, the [[binary tetrahedral group]] corresponds to the $E_6$ [[Dynkin diagram]] (see *[[McKay correspondence]]*). 

Families of two-dimensional [[conformal field theory|conformal field theories]], in which the [[Virasoro algebra]] plays a key role, are among the examples falling into an ADE classification.

* [[Bernoulli number]]

* [[moduli space of curves]]

* [[Dwyer-Wilkerson H-space]], which would be the automorphism group of a [[normed division algebra]] if one could exist in 24 dimensions

* [[Dedekind eta function]]

## References

* [More Mysteries of the Number 24](https://golem.ph.utexas.edu/category/2007/06/more_mysteries_of_the_number_2.html) at the $n$-Category Café

* [The Binary Octahedral Group](https://golem.ph.utexas.edu/category/2021/12/the_binary_octahedral_group.html) at the $n$-Category Café

* [John Baez on the Number 24](https://math.ucr.edu/home/baez/numbers/#24)

* H. Cohn, A. Kumar, S. D. Miller, D. Radchenko and M. Viazovska, *Universal optimality of the $E_8$ and Leech lattices and interpolation formulas*, 
([arXiv:1902.05438](https://arxiv.org/abs/1902.05438)).

* [[Terry Gannon]], section 2.5.1 of: *Moonshine Beyond the Monster* Cambridge University Press, 2006  ([doi:10.1017/CBO9780511535116](https://doi.org/10.1017/CBO9780511535116))

* [Bernoulli Numbers and the J-homomorphism](https://golem.ph.utexas.edu/category/2020/12/bernoulli_numbers_and_the_jhom.html) at the $n$-Category Café

* Sloane, N. J. (1980). A note on the Leech lattice as a code for the Gaussian channel. Information and Control, 46(3), 270--272.
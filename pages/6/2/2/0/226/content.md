

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Definition

For $k$ a [[field]] or a [[division ring]], a __vector space__ over $k$ 
(or a $k$-vector space) is a [[module]] over the [[ring]] $k$.  When the vector space is fixed, its elements are called _vectors_, the field $k$ is referred to as the base field of the ground field of the vector space, and the elements of $k$ are called _scalars_. 

Sometimes a vector space over $k$ is called a __$k$-linear space__.  (Compare '$k$-[[linear map]]'.) If $k$ is only a division ring then we
carefully distinguish the left $k$-vector spaces and right $k$-vector spaces.

The [[category]] of vector spaces is typically denoted [[Vect]], or 
$Vect_k$ if we wish to make the field $k$ (the *ground field*) explicit. So

$$
  Vect_k \coloneqq k Mod
  \,.
$$

This category has vector spaces over $k$ as objects, and $k$-linear maps between these as morphisms.

### Multisorted notion 

Alternatively, one sometimes defines "vector space" as a two-sorted notion; taking the field $k$ as one of the sorts and a module over $k$ as the other. More generally, the notion of "module" can also be considered as two-sorted, involving a ring and a module over that ring. 

This is occasionally convenient; for example, one may define the notion of [[topological vector space]] or topological module as an [[internalization]] in $Top$ of the multisorted notion. This procedure is entirely straightforward for topological modules, as the notion of module can be given by a two-sorted Lawvere theory $T$, whence a topological module (for instance) is just a product-preserving functor $T \to Top$. One may then define a topological vector space as a topological module whose underlying (discretized) ring sort is a field. 


## Properties

Every [[free object|free]] vector space admits a [[basis of a vector space|basis]]. 

The _[[basis theorem]]_, which is equivalent to the [[axiom of choice]], states that every vector space is a free vector space.

## Related concepts

* **vector space**, [[dual vector space]], 

  * [[finite-dimensional vector space]]

  * [[real vector space]], [[complex vector space]]

  * [[topological vector space]], [[convenient vector space]]

  * [[virtual vector space]]

* [[tensor product of vector spaces]]

* [[real structure]], [[complex structure]], [[quaternionic structure]]

* [[vector bundle]], 

* [[lattice in a vector space]]

* [[vector G-space]]

* [[2-vector space]], [[n-vector space]]

* [[inner product space]]

* [[linear operator]], [[matrix]], [[determinant]], [[eigenvalue]],  [[eigenvector]]

## References

The vector spaces seem to have been first introduced in

* Giuseppe Peano, _Calcolo Geometrico secondo l'Ausdehnungslehre di H. Grassmann preceduto dalle Operazioni della Logica Deduttiva_, Torino 1888

The literature on vector spaces is now extremely large, including lots of elementary linear algebra textbooks. Classics include

* [[Michael Artin]], Algebra
* Israel M. Gelfand, Lectures on linear algebra
* P. R. Halmos, Finite dimensional vector spaces
* [[M M Postnikov]], Lectures on geometry, semester 2: Linear algebra

Affine spaces are sets which are torsors over the abelian group of vectors of a vector space. Thus vector spaces may serve as a basis for the affine and for the Euclidean geometry. This approach has been invented by [[Hermann Weyl]] in 1918. Dieudonné wrote an influential book on such an approach to 2d and 3d Euclidian geometry, in which the basics of vector spaces in low dimension is introduced along the way (the book is intended for high school teachers):

* Jean Alexandre Dieudonn&#233;, Linear algebra and geometry

[[!redirects vector space]]
[[!redirects vector spaces]]
[[!redirects linear space]]
[[!redirects linear spaces]]

[[!redirects Grassmannian]]


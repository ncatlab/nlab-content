#Contents#
* automatic table of contents 
{:toc}


## Idea

Intuitively speaking, a braided monoidal category is a category with a tensor product and an isomorphism called the 'braiding' which lets us 'switch' two objects in a tensor product like $x \otimes y$.

## Definition

A **braided monoidal category** is a [[monoidal category]] $V$ equipped with a natural isomorphism
$$ B_{x,y} : x \otimes y \to y \otimes x $$
called the _braiding_, which must satisfy two axioms encoding the compatibility of the braiding with the associtive and unital structure of the tensor product.

write $a_{x,y,z} : (x \otimes y) \otimes z \to x \otimes (y \otimes z)$ for the components of the associator in $V$ and $l_x : I \otimes x \to x$ and $r_x : x \otimes I \to x$ for the left and right unitors. 

Then compatibility of the braiding with associativity is the condition that for all $x,y,z \in Obj(V)$ the diagram

$$
  \array{
   (x \otimes y) \otimes z 
   &\stackrel{a_{x,y,z}}{\to}&
   x \otimes (y \otimes z)
   &\stackrel{B_{x,y \otimes z}}{\to}&
   (y \otimes z) \otimes x
   \\
   \downarrow^{B_{x,y}\otimes Id}
   &&&&
   \downarrow^{a_{y,z,x}}
   \\
   (y \otimes x) \otimes z
   &\stackrel{a_{y,x,z}}{\to}&
   y \otimes (x \otimes z)
   &\stackrel{Id \otimes B_{x,z}}{\to}&
   y \otimes (z \otimes x)
  }
$$

commutes. Since it has six edges, this is often called a "hexagon identity", even though this says very little about the nature of this identity.

The compatibility with the left and right unitors is that for all objects $x$ the diagram

$$
  \array{
    I \otimes X &&\stackrel{B_{I,x}}{\to}&& x \otimes I
    \\
    & {}_{l_x}\searrow && \swarrow_{r_x}  
    \\
    && X
  }
$$

commutes.

More tersely, we could define a braided monoidal category to be a [[tricategory]] with one object and one 1-cell.  However, unlike the definition of a monoidal category as a [[bicategory]] with one object, this identification is not trivial; a doubly-degenerate tricategory is literally a category with two monoidal structures that interchange up to isomorphism.  It requires the [[Eckmann-Hilton argument]] to deduce an equivalence with braided monoidal categories.

If the braiding squares to the identity, then the braided monoidal category is a [[symmetric monoidal category]].

## Basic Facts

There is a [[strict 2-category]] BrMonCat with:

* braided monoidal categories as objects,
* [[braided monoidal functor|braided monoidal functors]] as morphisms, 
* [[braided monoidal natural transformation|braided monoidal natural transformations]] as 2-morphisms.

For definitions of all these concepts, see:

* [[John Baez]], [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

For an elementary introduction to braided monoidal categories using string diagrams, see:

* John Baez and [[Mike Stay]], [Physics, topology, logic and computation: a Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf).

+--{.query}
Eventually we should include all these diagrams here!  Can anyone help out?
=--

## Alternative characterizations

A braided monoidal category is equivalently a category that is equipped with the structure of an [[algebra over an operad|algebra over]] the [[little cubes operad|little 2-cubes operad]].

Details are in example 1.2.4 of

* [[Jacob Lurie]], [[E-k-Algebras]]


[[!redirects braided monoidal categories]]
[[!redirects braided category]]
[[!redirects braided categories]]
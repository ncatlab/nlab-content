
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* automatic table of contents 
{:toc}


## Idea

Intuitively speaking, a braided monoidal category is a category with a tensor product and an isomorphism called the 'braiding' which lets us 'switch' two objects in a tensor product like $x \otimes y$.

## Definition

A **braided monoidal category**, or __braided tensor category__, is a [[monoidal category]] $V$ equipped with a [[natural isomorphism]]

$$ B_{x,y} : x \otimes y \to y \otimes x $$

called the **braiding**, which must satisfy two axioms called **hexagon identities** encoding the compatibility of the braiding with the [[associator]] for the tensor product.  

If the braiding squares to the identity, then the braided monoidal category is a [[symmetric monoidal category]].


### The coherence laws

To see the haxagon identities, let us write $a_{x,y,z} : (x \otimes y) \otimes z \to x \otimes (y \otimes z)$ for the components of the associator in $V$.   Then the first hexagon identity says that for all $x,y,z \in Obj(V)$ the following diagram commutes:

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

The second hexagon identity says that for all $x,y,z \in Obj(V)$ the following diagram commutes:

$$
  \array{
   x \otimes (y \otimes z) 
   &\stackrel{a^{-1}_{x,y,z}}{\to}&
   (x \otimes y) \otimes z
   &\stackrel{B_{x \otimes y, z}}{\to}&
   z \otimes (x \otimes y)
   \\
   \downarrow^{Id \otimes B_{y,z}}
   &&&&
   \downarrow^{a^{-1}_{z,x,y}}
   \\
   x \otimes (z \otimes y)
   &\stackrel{a^{-1}_{x,z,y}}{\to}&
   (x \otimes z) \otimes y
   &\stackrel{B_{x,z} \otimes Id}{\to}&
   (z \otimes x) \otimes y
  }
$$

Intuitively speaking, the first hexagon identity says we can braid $x \otimes y$ past $z$ all at once or in two steps.  The second hexagon identity says we can braid $x$ past $y \otimes z$ 'all at once' or in two steps.

From these axioms, it follows that the braiding is compatible with the left and right unitors $l_x : I \otimes x \to x$ and $r_x : x \otimes I \to x$.   That is to say, for all objects $x$ the diagram

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

### In terms of higher monoidal structure

In terms of the language of [[k-tuply monoidal n-categories]] a braided monoidal category is a _doubly monoidal 1-category_ .

Accordingly, by [[delooping]] twice, it may be identified with a [[tricategory]] with a single [[object]] and a single 1-[[morphism]]. 

However, unlike the definition of a monoidal category as a [[bicategory]] with one object, this identification is not trivial; a doubly-degenerate tricategory is literally a category with two monoidal structures that [[interchange law|interchange]] up to isomorphism.  It requires the [[Eckmann-Hilton argument]] to deduce an equivalence with braided monoidal categories.


A commutative [[monoid]] is the same as a monoid [[internalization|in the category of]] monoids.
Similarly, a braided monoidal category is equivalent to a monoidal-category object (that is, a [[pseudomonoid]]) in the monoidal 2-category of monoidal categories.  This result probably goes back to Joyal and Street.

+--{.query}
Reference, anyone?
=--

A braided monoidal category is equivalently a category that is equipped with the structure of an [[algebra over an operad|algebra over]] the [[little cubes operad|little 2-cubes operad]].

Details are in example 1.2.4 of

* [[Jacob Lurie]], $\mathbb{E}[k]$-[[Ek-Algebras|Algebras]]




### The 2-category of braided monoidal categories

There is a [[strict 2-category]] BrMonCat with:

* braided monoidal categories as objects,
* [[braided monoidal functor|braided monoidal functors]] as morphisms, 
* [[braided monoidal natural transformation|braided monoidal natural transformations]] as 2-morphisms.

## References

The original papers on braided monoidal categories are by [[Andre Joyal|Joyal]] and [[Ross Street|Street]].  The published version does not completely supersede the _Macquarie Math Reports_ version, which has some nice extra results:

* [[André Joyal]] and [[Ross Street]], [Braided monoidal categories](http://rutherglen.ics.mq.edu.au/~street/JS86.pdf), _Macquarie Math Reports_ **860081** (1986). 

* [[André Joyal]] and [[Ross Street]], _Braided tensor categories_ , Adv. Math. **102** (1993), 20--78.

For definitions of braided monoidal categories, braided monoidal functors and braided monoidal natural transformations, see:

* [[John Baez]], [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

For an elementary introduction to braided monoidal categories using [[string diagram]]s, see:

* [[John Baez]] and [[Mike Stay]], [Physics, topology, logic and computation: a Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf), to appear in _New Structures in Physics_, ed. Bob Coecke. 

+--{.query}
Eventually we should include all these diagrams here, along with the definition of braided monoidal functor and braided monoidal natural transformation!  Can anyone help out?
=--


[[!redirects braided monoidal category]]
[[!redirects braided monoidal categories]]
[[!redirects braided category]]
[[!redirects braided categories]]
[[!redirects braided tensor category]]
[[!redirects braided tensor categories]]


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
* automatic table of contents goes here
{:toc}


## Idea 

A _symmetric monoidal category_ is a category with a product operation -- a [[monoidal category]] -- for which the product is _as commutative as possible_.

The point is that there are different degrees to which higher categorical products may be commutative. While a bare [[monoid]] is either commutative or not, a [[monoidal category]] may be a [[braided monoidal category]] -- which already means that the order of products may be reversed up to some [[isomorphism]] -- without being _symmetric_ monoidal -- which means that changing the order of a product twice, from $a \otimes b$ to $b \otimes a$ back to $a \otimes b$, indeed does yield a result [[equality|equal]] to the original.

For higher monoidal categories there are accordingly ever more shades of the notion of "commutativity" of the monoidal product. This is described in detail at [[k-tuply monoidal n-category]]. 

In general, the term _symmetric monoidal_ is used for the maximally commutative case. See for instance [[symmetric monoidal (∞,1)-category]]. Notably, a symmetric monoidal [[∞-groupoid]] is, under the [[homotopy hypothesis]], the same as a [[spectrum|connective spectrum]].


## Definition

A **symmetric monoidal category** is a [[braided monoidal category]] for which the braiding 
$$ B_{x,y} : x \otimes y \to y \otimes x $$
satisfies an additional axiom:
$$ B_{y,x} B_{x,y} = 1_{x \otimes y}  $$
for all objects $x, y$.  Intuitively this says that switching things twice has no effect.

Expanding this out a bit: a  **symmetric monoidal category** is, to begin with a [[category]] $M$ equipped with a [[functor]]
$$ \otimes : M \times M \to M $$
called the **tensor product**, an object
$$ 1 \in M $$
called the **unit object**, a natural isomorphism
$$ a_{x,y,z} : (x \otimes y) \otimes z \to x \otimes (y \otimes z) $$
called the **associator**, a natural isomorphism
$$ \lambda_x : 1 \otimes x \to x $$
called the **left unitor**, a natural isomorphism 
$$  \rho_x : x \otimes 1 \to x $$
called the **right unitor**, and a natural isomorphism
$$ B_{x,y} : x \otimes y \to y \otimes x $$
called the **braiding**.  We then demand that the associator obey the **pentagon identity**, which says this diagram commutes:

+--{: style="text-align:center"}
[[!include monoidal category > pentagon]]
=--

We demand that the associator and unitors  obey the **triangle identity**, which says this diagram commutes:

$$
  \array{
     & (x \otimes 1) \otimes y &\stackrel{a_{x,1,y}}{\longrightarrow} & x \otimes (1 \otimes y)
      \\
      
      & {}_{\rho_x \otimes 1_y}\searrow
       
       && \swarrow_{1_x \otimes \lambda_y}
      & 
     \\
     &&
     x \otimes y
     &&
     
  }
$$

We demand that the braiding and associator obey the first **hexagon identity**:

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

And lastly, we demand that
$$ B_{y,x} B_{x,y} = 1_{x \otimes y} . $$
(The definition of [[braided monoidal category]] has _two_ hexagon identities, but either one implies the other given this equation.)


## Basic facts

There is a [[strict 2-category]] SymmMonCat with:

* symmetric monoidal categories as objects,
* [[symmetric monoidal functor]]s as morphisms, 
* [[symmetric monoidal natural transformation]]s as 2-morphisms.

A symmetric monoidal category is equivalently a category that is equipped with the structure of an [[algebra over an operad|algebra over]] the [[little cubes operad|little k-cubes operad]] for $k \geq 3$

Details are in examples 1.2.3 and 1.2.4 of

* [[Jacob Lurie]], $\mathbb{E}[k]$-[[Ek-Algebras|Algebras]]


## Examples 

* Every [[cartesian monoidal category]] is necessarily symmetric monoidal, due to the essential uniqueness of the categorical [[product]]. This includes cases such as [[Set]], [[Cat]].

* For $k$ some [[field]], the category [[Vect]] of $k$-vector spaces carries the standard structure of a [[monoidal category]] coming from the [[tensor product]], over $k$, of vector spaces. The standard braiding that identifies $V \otimes W$ with $W \otimes V$ by mapping homogeneous elements $v \otimes w$ to $w \otimes v$ obviously makes [[Vect]] into a symmetric monoidal category.

* The category of $\mathbb{Z}_2$-[[graded vector space]]s, on the other hand, has two different symmetric monoidal extensions of the standard [[tensor product]] monoidal structure. One is the trivial one from above, the other is the one that induces a a sign when two odd-graded vectors $v$ and $w$ are passed past each other : $v \otimes w \mapsto - w \otimes v$. This non-trivial symmetric monoidal structure on $Vect[\mathbb[Z}_2]$ defines the symmetric monoidal category of [[super vector space]]s.


## References

For definitions of symmetric monoidal categories, [[symmetric monoidal functor]]s and [[symmetric monoidal natural transformation]]s, see:

* [[John Baez]], [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

For an elementary introduction to symmetric monoidal categories using string diagrams, see:

* John Baez and [[Mike Stay]], [Physics, topology, logic and computation: a Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf).

Eventually we should include all these definitions and diagrams here!  I don't know a good way to do this yet.

[[!redirects symmetric monoidal categories]]
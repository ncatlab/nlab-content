
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
* table of contents 
{:toc}


## Idea

Intuitively speaking, a braided monoidal category is a category with a tensor product and an isomorphism called the 'braiding' which lets us 'switch' two objects in a tensor product like $x \otimes y$.  Thus the tensor product is "commutative" in a sense, but not as coherently commutative as in a [[symmetric monoidal category]].

A braided monoidal category is a special case of the notion of [[braided pseudomonoid]] in a [[braided monoidal 2-category]].

## Definition
 {#Definition}

+-- {: .num_defn #BraidedMonoidalCategory} 
###### Definition

A **braided monoidal category**, or ("braided [[tensor category]]", but see there), is a [[monoidal category]] $\mathcal{C}$ equipped with a [[natural isomorphism]]

$$ 
  B_{x,y} : x \otimes y \to y \otimes x 
$$

called the **[[braiding]]**, such that the following two kinds of [[commuting diagram|diagrams commute]] for all [[objects]] involved (called the **hexagon identities** encoding the compatibility of the braiding with the [[associator]] for the tensor product):

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

and

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
  \,,
$$

where $a_{x,y,z} \colon (x \otimes y) \otimes z \to x \otimes (y \otimes z)$ denotes the components of the [[associator]] of $\mathcal{C}^\otimes$. 


=--

+-- {: .num_defn} 
###### Definition


If the braiding in def. \ref{BraidedMonoidalCategory} "squares" to the identity in that $B_{y,x} \circ B_{x,y} = id_{x \otimes y}$, then the braided monoidal category is called a _[[symmetric monoidal category]]_.

=--

+-- {: .num_remark} 
###### Remark

Intuitively speaking, the first hexagon identity in def. \ref{BraidedMonoidalCategory} says we may braid $x$ past $y \otimes z$ 'all at once' or in two steps. The second hexagon identity says that we may braid $x \otimes y$ past $z$ all at once or in two steps. 

=--

+-- {: .num_remark} 
###### Remark

From these axioms in def. \ref{BraidedMonoidalCategory}, it follows that the braiding is compatible with the left and right [[unitors]] $l_x : I \otimes x \to x$ and $r_x : x \otimes I \to x$.   That is to say, for all objects $x$ the diagram

$$
  \array{
    I \otimes x &&\stackrel{B_{I,x}}{\to}&& x \otimes I
    \\
    & {}_{l_x}\searrow && \swarrow_{r_x}  
    \\
    && x
  }
$$

commutes.  

=--

### In terms of higher monoidal structure

In terms of the language of [[k-tuply monoidal n-categories]] a braided monoidal category is a _doubly monoidal 1-category_ .

Accordingly, by [[delooping]] twice, it may be identified with a [[tricategory]] with a single [[object]] and a single 1-[[morphism]]. 

However, unlike the definition of a monoidal category as a [[bicategory]] with one object, this identification is not trivial; a doubly-degenerate tricategory is literally a category with two monoidal structures that [[interchange law|interchange]] up to isomorphism.  It requires the [[Eckmann-Hilton argument]] to deduce an equivalence with braided monoidal categories.


A commutative [[monoid]] is the same as a monoid [[internalization|in the category of]] monoids.
Similarly, a braided monoidal category is equivalent to a monoidal-category object (that is, a [[pseudomonoid]]) in the monoidal 2-category of monoidal categories.  This result goes back to the [1986 paper by Joyal and Street](http://maths.mq.edu.au/~street/JS1.pdf).  (There is also a notion of [[braided pseudomonoid]] that specializes directly in [[Cat]] to braided monoidal categories.)

A braided monoidal category is equivalently a category that is equipped with the structure of an [[algebra over an operad|algebra over]] the [[little cubes operad|little 2-cubes operad]].

Details are in example 1.2.4 of

* [[Jacob Lurie]], $\mathbb{E}[k]$-[[Ek-Algebras|Algebras]]


### The 2-category of braided monoidal categories

There is a [[strict 2-category]] BrMonCat with:

* braided monoidal categories as objects,
* [[braided monoidal functor|braided monoidal functors]] as morphisms, 
* [[braided monoidal natural transformation|braided monoidal natural transformations]] as 2-morphisms.

## Examples

* Any [[symmetric monoidal category]] is a braided monoidal category.

* The monoidal category $R$-$\mathcal{GMod}$ of [[graded modules]] over a [[commutative ring]] $R$ (with the usual [[tensor product of modules|tensor product of graded modules]]) can be made into a braided monoidal category in multiple ways, each one given by an invertible element $u$ of the base ring. Infact, all braidings on $R$-$\mathcal{GMod}$ arise in this way (as in [Joyal, Street](JoyalStreet86)). The braiding $B^u_{V,W} : V \otimes W \to W \otimes V$, is defined as
$$
  x \otimes y \mapsto u^{|x||y|} y \otimes x,
$$
where $|x|$ and $|y|$ denote the degrees. It's evident that the resulting braided monoidal category is symmetric if and only if $u^2 = 1$.

* The category of [[crossed G-set|crossed G-sets]].

## Properties

### Tannaka duality

[[!include structure on algebras and their module categories - table]]

## Related concepts

* [[k-tuply monoidal (n,r)-category]]

* [[monoidal category]], [[monoidal (∞,1)-category]]

* **braided monoidal category**, [[braided monoidal (∞,1)-category]]

  * [[braided 2-group]], [[braided ∞-group]]
 
  * [[braided monoidal 2-category]]

* [[symmetric monoidal category]], [[symmetric monoidal (∞,1)-category]]

* [[closed monoidal category]] ,  [[closed monoidal (∞,1)-category]]

* [[2-fold monoidal category]], [[duoidal category]]

## References

Exposition of basics of [[monoidal categories]] and [[categorical algebra]]:

* _[[geometry of physics -- categories and toposes]]_, Section 2: _[Basic notions of categorical algebra](geometry+of+physics+--+categories+and+toposes#BasicNotionsOfCategoricalAlgebra)_


The original papers on braided monoidal categories are by [[Andre Joyal|Joyal]] and [[Ross Street|Street]]. The published version does not completely supersede the _Macquarie Math Reports_ version, which has some nice extra results:

* {#JoyalStreet86} [[André Joyal]] and [[Ross Street]], *Braided monoidal categories*, _Macquarie Math Reports_ **860081** (1986) ([pdf](http://maths.mq.edu.au/~street/JS1.pdf))

* [[André Joyal]], [[Ross Street]], _Braided tensor categories_, Adv. Math. **102** (1993), 20--78 ([doi:10.1006/aima.1993.1055](https://doi.org/10.1006/aima.1993.1055))

Around the same time the same definition was also proposed independently by [[Lawrence Breen]] in a letter to [[Pierre Deligne]]:

* {#Breen88} [[Lawrence Breen]], _Une lettre &#224; P. Deligne au sujet des $2$-cat&#233;gories tress&#233;es_ (1988) ([pdf](http://www.math.univ-paris13.fr/~breen/deligne.pdf))

Textbook accounts include

* {#EGNO15} [[nLab:Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[nLab:Victor Ostrik]], chapter 2 of _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf))


For a review of definitions of braided monoidal categories, braided monoidal functors and braided monoidal natural transformations, see:

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

[[!redirects hexagon identity]]
[[!redirects hexagon identities]]


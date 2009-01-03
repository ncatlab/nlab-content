#Idea#

A category $C$ is _closed_ if for any pair $a, b$ of object the collection of morphisms from $a$ to $b$ can be regarded as forming itself an object of $C$.

## Examples ##

 * The tautological example is the category [[Set]] of sets: the collection of maps between any two sets is itself a set. 

 * The category of abelian groups is closed: for any two abelian groups $A, B$ the set of homomorphisms $A \to B$ carries (pointwise defined) abelian group structure. 

 * Certain categories [[Top]] of [[nice topological spaces]] are closed: for any two nice topological spaces $X$, $Y$ the set of continuous maps $X \to Y$ can be equipped with a topology to become a nice topological space itself.

## Formalization ##

The strategy for formalizing this idea that "the collection of morphisms from $a$ to $b$ can be regarded as an object of $C$ itself" is to mimic the situation in [[Set]] where for any three objects (sets) $a$, $b$, $c$ we have an isomorphism
$$
  Hom(a \otimes b, c) \simeq Hom(a, Hom(b,c))
  \,,
$$
naturally in all three arguments,
where $\otimes = \times$ is the standard [[cartesian monoidal category|cartesian]] [[product]] of sets.

This can be read as a characterization of the Hom-object $Hom(b,c)$ and is the basis for the following definition.

# Defintition #

A [[monoidal category]] $C$ is _closed_ if for all objects $b \in C_0$ the functor $ - \otimes b : C \to C$ has a [[adjunction|right adjoint]] functor $[b,-] : C \to C$.

This means that for all $a,b,c \in C_0$ we have a bijection

$$
  Hom_C(a \otimes b, c) \simeq Hom_C(a, [b,c])
$$

natural in all arguments.

The object $[b,c]$ is called the **internal hom** of $b$ and $c$. This is commonly also denoted by lower case $hom(b,c)$ (and then often underlined).

#References#

For instance section 1.5 _Closed and biclosed monoidal categories_ of

* Max Kelly, _Basic concepts of enriched category theory_ ([tac](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html))
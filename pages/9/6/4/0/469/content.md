A closed monoidal category is a [[monoidal category]] that is also a [[closed category]], in a compatible way.

## Formalization ##

The strategy for formalizing the idea of a closed category, that "the collection of morphisms from $a$ to $b$ can be regarded as an object of $C$ itself", is to mimic the situation in [[Set]] where for any three objects (sets) $a$, $b$, $c$ we have an isomorphism
$$
  Hom(a \otimes b, c) \simeq Hom(a, Hom(b,c))
  \,,
$$
naturally in all three arguments,
where $\otimes = \times$ is the standard [[cartesian monoidal category|cartesian]] [[product]] of sets.

This can be read as a characterization of the Hom-object $Hom(b,c)$ and is the basis for the following definition.

# Definition #

A symmetric [[monoidal category]] $C$ is **closed** if for all objects $b \in C_0$ the functor $ - \otimes b : C \to C$ has a [[adjunction|right adjoint]] functor $[b,-] : C \to C$.

This means that for all $a,b,c \in C_0$ we have a bijection

$$
  Hom_C(a \otimes b, c) \simeq Hom_C(a, [b,c])
$$

natural in all arguments.

The object $[b,c]$ is called the **internal hom** of $b$ and $c$. This is commonly also denoted by lower case $hom(b,c)$ (and then often underlined).

If the monoidal structure of $C$ is [[cartesian monoidal category|cartesian]], then $C$ is called **cartesian closed**.  In this case the internal hom is often called an **exponential** and written $c^b$.

If $C$ is not symmetric, then $-\otimes b$ and $b\otimes -$ are different functors, and either one or both may have an adjoint.  The terminology here is less standard, but many people use **left closed**, **right closed**, and **biclosed**.

## Examples ##

 * The tautological example is the category [[Set]] of sets: the collection of maps between any two sets is itself a set.  More generally, any [[topos]] is cartesian closed.

 * The category of abelian groups is closed: for any two abelian groups $A, B$ the set of homomorphisms $A \to B$ carries (pointwise defined) abelian group structure. 

 * Certain categories [[Top]] of [[nice topological space|nice topological spaces]] are cartesian closed: for any two nice topological spaces $X$, $Y$ the set of continuous maps $X \to Y$ can be equipped with a topology to become a nice topological space itself.

 * Certain categories of nice _based_  topological spaces are closed symmetric monoidal.  The monoidal structure is the [[smash product]] and the internal-hom is the set of basepoint-preserving maps with topology induced from the space of unbased ones.

 * The category [[Cat]] is cartesian closed: the internal-hom is the [[functor category]] of functors and natural transformations.

 * The category $2-Cat$ of [[strict 2-category|strict 2-categories]] and strict 2-functors is closed symmetric monoidal under the [[Gray tensor product]].  The internal-hom is the 2-category of strict 2-functors, _pseudo_ natural transformations, and modifications.

 * The category of strict $\omega$-[[strict omega-category|categories]] is also biclosed monoidal, under the [[Crans-Gray tensor product]].

 * If $M$ is a monoidal category and $Set^{M^{op}}$ is endowed with the tensor product given by the induced [[Day convolution]] product, then $Set^{M^{op}}$ is biclosed monoidal. 

 * The category of [[species]], with the monoidal structure given by substitution product of species, is closed monoidal (each functor $- \circ G$ admits a right adjoint) but not biclosed monoidal. 

#References#

* Max Kelly, _Basic concepts of enriched category theory_, section 1.5, ([tac](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html)) 

* Samuel Eilenberg and Max Kelly, _Closed categories_.  Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965).
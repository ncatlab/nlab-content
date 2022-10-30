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

A closed monoidal category $C$ is a [[monoidal category]] that is also a [[closed category]], in a compatible way:

it has for each [[object]] $X$ a [[functor]] $(-) \otimes X : C \to C$ of forming the [[tensor product]] with $X$, as well as a functor $[X,-] : C \to C$ of forming the [[internal-hom]] with $X$, and these form a pair of [[adjoint functor]]s.


The strategy for formalizing the idea of a closed category, that "the collection of morphisms from $a$ to $b$ can be regarded as an object of $C$ itself", is to mimic the situation in [[Set]] where for any three objects (sets) $a$, $b$, $c$ we have an isomorphism
$$
  Hom(a \otimes b, c) \simeq Hom(a, Hom(b,c))
  \,,
$$
naturally in all three arguments,
where $\otimes = \times$ is the standard [[cartesian product]] of sets.  This [[natural isomorphism]] is called [[currying]].

Currying can be read as a characterization of the [[internal hom]] $Hom(b,c)$ and is the basis for the following definition.


## Definition #

A [[symmetric monoidal category|symmetric]] [[monoidal category]] $C$ is **closed** if for all objects $b \in C_0$ the functor $ - \otimes b : C \to C$ has a [[adjoint functor|right adjoint]] functor $[b,-] : C \to C$.

This means that for all $a,b,c \in C_0$ we have a bijection

$$
  Hom_C(a \otimes b, c) \simeq Hom_C(a, [b,c])
$$

natural in all arguments.

The object $[b,c]$ is called the **[[internal hom]]** of $b$ and $c$. This is commonly also denoted by lower case $hom(b,c)$ (and then often underlined).

If the monoidal structure of $C$ is [[cartesian monoidal category|cartesian]], then $C$ is called **cartesian closed**.  In this case the internal hom is often called an **exponential** and written $c^b$.

If $C$ is not symmetric, then $-\otimes b$ and $b\otimes -$ are different functors, and either one or both may have an adjoint.  The terminology here is less standard, but many people use **left closed**, **right closed**, and **biclosed**.


## Examples ##

 * The tautological example is the category [[Set]] of sets: the collection of maps between any two sets is itself a set.  More generally, any [[topos]] is cartesian closed.

 * The category of abelian groups is closed: for any two abelian groups $A, B$ the set of homomorphisms $A \to B$ carries (pointwise defined) abelian group structure. 

* A [[discrete category|discrete]] monoidal category (i.e., a [[monoid]]) is left closed iff it is right closed iff every object has an inverse (i.e., it is a [[group]]).

 * Certain [[nice category of spaces|nice categories]] of topological spaces are cartesian closed: for any two nice enough topological spaces $X$, $Y$ the set of continuous maps $X \to Y$ can be equipped with a topology to become a nice topological space itself.

 * Certain nice categories of _based_  topological spaces are closed symmetric monoidal.  The monoidal structure is the [[smash product]] and the internal-hom is the set of basepoint-preserving maps with topology induced from the space of unbased ones.

 * The category [[Cat]] is cartesian closed: the internal-hom is the [[functor category]] of functors and natural transformations.

 * The category $2 Cat$ of [[strict 2-category|strict 2-categories]] and strict 2-functors is closed symmetric monoidal under the [[Gray tensor product]].  The internal-hom is the 2-category of strict 2-functors, _pseudo_ natural transformations, and modifications.

 * The category of strict $\omega$-[[strict omega-category|categories]] is also biclosed monoidal, under the [[Crans-Gray tensor product]].

 * If $M$ is a monoidal category and $Set^{M^{op}}$ is endowed with the tensor product given by the induced [[Day convolution]] product, then $Set^{M^{op}}$ is biclosed monoidal. 

 * The category of [[species]], with the monoidal structure given by substitution product of species, is closed monoidal (each functor $- \circ G$ admits a right adjoint) but not biclosed monoidal. 

 * The category of [[modules]] over any [[Hopf monoid]] in a closed monoidal category, or more generally algebras for any [[Hopf monad]], is again a closed monoidal category.  In particular, the category of modules over any [[group object]] in a [[cartesian closed category]] is (cartesian) closed monoidal.


### Functor categories

+-- {: .num_theorem}
###### Theorem
Let $C$ be a [[complete category|complete]] closed monoidal category and $I$ any [[small category]].  Then the [[functor category]] $[I,C]$ is closed monoidal with the pointwise tensor product, $(F\otimes G)(x) = F(x) \otimes G(x)$.
=--
+-- {: .proof}
###### Proof
Since $C$ is complete, the category $[I,C]$ is [[comonadic functor|comonadic]] over $C^{ob I}$; the comonad is defined by right [[Kan extension]] along the inclusion $ob I \hookrightarrow I$.  Now for any $F\in [I,C]$, consider the following square:
$$\array{[I,C] & \overset{F\otimes - }{\to} & [I,C] \\
  \downarrow && \downarrow\\
  C^{ob I}& \underset{F_0 \otimes -}{\to} & C^{ob I}}
$$
This commutes because the tensor product in $[I,C]$ is pointwise (here $F_0$ means the family of objects $F(x)$ in $C^{ob I}$).
Since $C$ is closed, $F_0 \otimes -$ has a right adjoint.
Since the vertical functors are comonadic, the (dual of the) [[adjoint lifting theorem]] implies that $F\otimes -$ has a right adjoint as well.
=--

## Related concepts

* [[monoidal category]], [[monoidal (∞,1)-category]]

* [[symmetric monoidal category]], [[symmetric monoidal (∞,1)-category]]

* **closed monoidal category** ,  [[closed monoidal (∞,1)-category]]

  * [[closed monoidal functor]]

  * [[indexed closed monoidal category]]

* [[string diagram]], [[Kelly-Mac Lane diagram]]

##References#

In [[enriched category theory]] the enriching category is taken to be closed monoidal. Accordingly the standard textbook on enriched category theory

* [[Max Kelly]], _Basic concepts of enriched category theory_, section 1.5, ([tac](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html)) 

has a chapter on just closed monoidal categories.

See also the article

* [[Samuel Eilenberg]] and [[Max Kelly]], _Closed categories_.  Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965).

on the concept of closed categories.

[[!redirects closed symmetric monoidal category]]
[[!redirects closed symmetric monoidal categories]]
[[!redirects monoidal closed category]]
[[!redirects closed monoidal categories]]
[[!redirects monoidal closed categories]]
[[!redirects biclosed monoidal category]]
[[!redirects left closed monoidal category]]
[[!redirects right closed monoidal category]]
[[!redirects biclosed monoidal categories]]
[[!redirects left closed monoidal categories]]
[[!redirects right closed monoidal categories]]
[[!redirects closed symmetric monoidal structure]]
[[!redirects closed monoidal structure]]
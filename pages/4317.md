
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

# Rig categories
* table of contents
{: toc}

## Idea

Recall that a [[rig]] is a '[[ring]] without negatives': a [[monoid object]] in the [[monoidal category]] of [[commutative monoids]] with the usual [[tensor product]].  [[categorification|Categorifying]] this notion, we obtain various notions of _[[2-rig]]_.  One of these, in which both "addition" and "multiplication" are represented by abstract [[monoidal category|monoidal structures]], is the notion of *rig category*, also known as a *bimonoidal category*.

A typical example would be the [[groupoid]] of [[finite set|finite sets]] and [[bijection|bijections]], with [[disjoint union]] playing the role of addition and [[cartesian product]] playing the role of multiplication.  This rig category can be thought of as a categorification of the set of [[natural numbers]].  Note that in this example, disjoint union is _not_ the categorical [[coproduct]], and product of sets is _not_ the categorical [[product]] (because we are working in the *groupoid* of finite sets).

## Definition

A **rig category**, or **bimonoidal category**, $C$ is a category with a [[symmetric monoidal category|symmetric monoidal]] structure $(C,\oplus,0)$ for addition and a [[monoidal category|monoidal]] structure $(C, \otimes, I)$ for multiplication, together with left and right [[distributivity law|distributivity]] [[natural isomorphisms]]

$$ 
  d_\ell   
  \;\colon\; 
  x \otimes (y \oplus z) 
  \longrightarrow 
  (x \otimes y) \oplus (x \otimes z) 
$$

$$ 
  d_r 
  \;\colon\; 
  (x \oplus y) \otimes z 
  \longrightarrow 
  (x \otimes z) \oplus (y \otimes z) 
$$

and absorption/annihilation [[natural isomorphisms]]

$$ a_\ell \;\colon\; x \otimes 0 \longrightarrow 0 $$

$$ a_r \;\colon\; 0 \otimes x \longrightarrow 0 $$

satisfying a set of [[coherence laws]] worked out in ([Laplaza 72](#Laplaza72)) and ([Kelly74](#Kelly74)).

Note that these authors used the term "ring category".  We take the liberty of switching to "rig category" because it is typical for these to lack additive inverses.

While a rig can have the [[extra property]] of being [[commutative ring|commutative]] (i.e. of its multiplication being commutative), a rig category can have the [[extra structure]] of (its monoidal structure $\otimes$) being [[braided monoidal category|braided]] (compatibly with the distributive laws) and may then have the further property of being [[symmetric monoidal category|symmetric]].

## Examples

Rig categories are part of the hierarchy of [[distributivity for monoidal structures]].  

### Distributive categories

A rig category where $\oplus$ is the [[category theory|category-theoretic]] [[coproduct]] and $\otimes$ is the category-theoretic [[product]] ([[Cartesian product]]) is called a _[[distributive category]]_.

For example, 

* the category [[Set]] of [[sets]], 

* any [[topos]], 

* the category [[Top]] of [[topological spaces]] with respect to forming [[product topological spaces]] and [[disjoint union topological spaces]];

are distributive categories, hence rig categories with $\times$ and $+$.

### Distributive monoidal categories
 {#DistributiveMonoidalCategories}

In between, we have the notion of [[distributive monoidal category]], where $\oplus$ is the coproduct but $\otimes$ is a possibly non-cartesian [[monoidal category|monoidal structure]].  

Examples of this sort include [[Ab]], $R$[[Mod]], [[Vect]] and [[Vect(X)]]:

* [[Ab]], the category of [[abelian groups]] equipped with the [[tensor product of abelian groups]]

* $R$[[Mod]], the category of [[modules]] over a [[commutative ring]] $R$, equipped  with the [[tensor product of modules]]

* $k$[[Vect]] = $k$[[Mod]], the category of [[vector space]] over some [[field]] $k$, equipped with the [[tensor product of vector spaces]],

* $k$[[Vect(X)]], the category of ([[topological vector bundles|topological]]) [[vector bundles]] for $X$ some ([[topological space|topological]]) [[space]], equipped with the [[tensor product of vector bundles]].

In all these cases the coproduct is the respective [[direct sum]] (e.g. [[direct sum of vector bundles]] in the last case).

Also:

* the category of [[pointed topological spaces]] with respect to forming [[smash product]] and [[wedge sum]] (e.g. [Hatcher, Section 4.F](algebraic+topology#Hatcher)).




## Baez's conjecture

+-- {: .un_theorem}
###### Conjecture (John Baez)

Using the correct definition of the 2-category of symmetric rig categories, the groupoid $FinSet^{\times}$ of finite sets and bijections is the [[initial object|initial]] symmetric rig category, just as $\N$ is the initial commutative rig.   Note that a suitably weakened concept of 'initial' is needed here; see [[2-limit]].  In other words, given any symmetric rig category $R$, there is a unique symmetric rig morphism $FinSet^{\times} \to R$, up to an [[equivalence]] which is itself unique up to an [[isomorphism]] which is actually unique (up to [[equality]]).
=--

This conjecture has been established in ([Elgueta 2021](#Elg21)). See also ([Comfort-Delpeuch-Hedges, Sec. 8](#CDH)).

## Related concepts

* [[distributivity for monoidal structures]]

  * [[distributive category]], [[distributive monoidal category]]

  * If the distributivity morphisms are not invertible, then we have the notion of [[colax-distributive rig category]].

  * [[duoidal category]]

  * [[2-rig]]

* The notion of a [[bipermutative category]] is a strictification of the notion of [[symmetric monoidal category|symmetric]] rig category.  Every symmetric rig category is equivalent to a bipermutative category ([May, prop. VI 3.5]).  Similarly, every rig category is equivalent to a strict rig category ([Guillou, theorem 1.2](#Guillou)).

* [[K-theory of a bipermutative category]]

* [[BDR 2-vector bundle]].

## References

The [[coherence law|coherence]] for the [[distributivity law]] in bimonoidal categories has been given in

* M. Laplaza, _Coherence for distributivity_, Lecture Notes in Mathematics 281, Springer Verlag, Berlin, 1972, pp. 29-72.
 {#Laplaza72}

* G. Kelly, _Coherence theorems for lax algebras and distributive laws_, Lecture Notes in Mathematics 420, Springer Verlag, Berlin, 1974, pp. 281-375.
 {#Kelly74}

where these categories are called _ring categories_. Discussion with an eye towards the [[K-theory of a bipermutative category]] is in

* [[Peter May]], _$E_\infty$ Ring Spaces and $E_\infty$ Ring spectra_, Springer lectures notes in mathematics, Vol. 533, (1977) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/e_infty.pdf)) chaper VI
 {#May}

* Bertrand Guillou, _Strictification of categories weakly enriched in symmetric monoidal categories, [arXiv:0909.5270](http://arxiv.org/abs/0909.5270)
 {#Guillou}


* Ang&#233;lica Osorno, _Spectra associated to symmetric monoidal bicategories_ ([arXiv:1005.2227](http://arxiv.org/abs/1005.2227))

A [[string diagram]] treatment of rig categories via _sheet diagrams_ is in

* {#CDH} Cole Comfort, Antonin Delpeuch, [[Jules Hedges]], _Sheet diagrams for bimonoidal categories_, ([arXiv:2010.13361](https://arxiv.org/abs/2010.13361))

Biinitiality of the groupoid of finite sets is shown in 

* {#Elg21} Josep Elgueta, _The groupoid of finite sets is biinitial in the 2-category of rig categories_, Journal of Pure and Applied Algebra
**225** Issue 11 (2021) 106738, doi:[10.1016/j.jpaa.2021.106738](https://doi.org/10.1016/j.jpaa.2021.106738), [arXiv:2004.08684](https://arxiv.org/abs/2004.08684).

[[!redirects rig category]]
[[!redirects rig categories]]

[[!redirects rig-category]]
[[!redirects rig-categories]]


[[!redirects ring category]]
[[!redirects ring categories]]
[[!redirects bimonoidal category]]
[[!redirects bimonoidal categories]]
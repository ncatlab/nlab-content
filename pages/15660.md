

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The notion of _dg-module_ over a [[dg-algebra]] is the specialization of [[module over a monoid]] to the category of [[chain complexes]]. More generally one can consider dg-modules over [[dg-algebras]] with many objects, i.e. [[dg-categories]].

## Definition

### Over dg-algebras

Let $A$ be a [[dg-algebra]] in an [[abelian category]], hence a [[monoid]] in the [[symmetric monoidal category|symmetric monoidal]] [[category of chain complexes]] with respect to the [[tensor product of chain complexes]]. 

+-- {: .num_defn}
###### Definition

A left (resp. right) **dg-module** over $A$ is a left (resp. right) [[module over a monoid|module]] over the [[monoid]] $A$.

Spelling this out in components, it means the following:

A _[[dg-module]]_ over $A$ is a [[chain complex]] $V$ equipped with a [[chain map]]

$$
  \rho \;\colon\; A \otimes V \longrightarrow V
$$

out of the [[tensor product of chain complexes]], which satisfies the [[action]] property. Explicitly this means that

1. $\rho$ preserves degrees: for all $a \in A$ and $v \in V$ of homogeneous degrees ${\vert a \vert}$ and ${\vert v \vert}$, respectively, then $\vert \rho(a,v)\vert = {\vert a \vert} + {\vert v \vert}$;

1. for all $a \in A$, $v \in V$ with $a$ in degree $\vert a \vert$, then 

   $$
     d_V (\rho(a,v)) = \rho(d_A a, v) + (-1)^{\vert a\vert} \rho(a,d_V v)
   $$

1. for all $a,b \in A$, $v \in V$ then

   $$
     \rho(a,\rho(b,v)) = \rho(a \cdot b,v)
     \,.
   $$


For $(V_i, \rho_i)$ two [[dg-modules]] over $A$, then a [[homomorphism]] between them is a [[chain map]]

$$
  \phi \;\colon\; V_1 \longrightarrow V_2
$$

such that for all $a \in A$ and $v \in V$ then 

$$
  \rho_2(a, \phi(v)) = \phi(\rho_1(a,v))
  \,.
$$

This defines a [[category]] $A Mod$ of [[dg-modules]] over $A$. 

We say that a morphism of dg-modules is a _[[quasi-isomorphism]]_ if its underlying [[chain map]] is, hence if it induces an isomorphism on [[chain homology]]. This makes $A Mod$ a [[category with weak equivalences]].

=--



### Over dg-categories

More generally let $T$ be a [[dg-category]].

+-- {: .num_defn}
###### Definition

A left (resp. right) **dg-module** over $T$ is a [[module over an enriched category|module]] over $T$ in the sense of [[enriched category theory]]. That is, it is a functor of [[dg-categories]]
  $$ M : T^{op} \longrightarrow dg-mod_k $$
(resp. $M : T \longrightarrow dg-mod_k$) where $k$ is the base [[commutative ring]].
=--

Note that when $T$ is a [[dg-category]] with a single object, a dg-module over $T$ is the same thing as a dg-module over the [[dg-algebra]] of [[endomorphisms]] of the unique object.

+-- {: .num_defn}
###### Definition
The **shift** of a dg-module $M$ over $T$ by an [[integer]] $n$ is the dg-module $M[n]$ defined by composing $M$ with the shift [[endofunctor]] $-[n]$ on $dg-mod_k$.
=--


## Properties

By general [[enriched category theory]], dg-modules themselves form a [[dg-category]] which we denote $dg-mod_T$.

+-- {: .num_defn}
###### Definition
A dg-module $M \in dg-mod_T$ is called **representable** if it is in the [[essential image]] of the [[dg-Yoneda embedding]].

$M$ is called **free** if it is equivalent to a [[direct sum]] of shifts of representable dg-modules.

$M$ is called **semi-free** if it admits a [[filtration]] whose [[associated graded objects]] are free dg-modules.
=--


## Related concepts

* [[minimal dg-module]]

* [[dg-comodule]]

## References


* [[Bertrand Toen]], section 3 in _The homotopy theory of dg-categories and derived Morita theory_, [arXiv:math/0408337](http://arxiv.org/abs/math/0408337).

Paragraph 2.2 of

* [[Dmitri Orlov]], _Smooth and proper noncommutative schemes and gluing of DG categories_, [arXiv:1402.7364](http://arxiv.org/abs/1402.7364).

[[!redirects dg-modules]]

[[!redirects dg-presheaf]]
[[!redirects dg-presheaves]]
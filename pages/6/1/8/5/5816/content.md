
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

One notion often called an __enriched bicategory__ is the same as that of an [[enriched category]], but where the enriching context $\mathcal{V}$ is allowed to be generalized from a [[monoidal category]] to a [[monoidal bicategory]], while suitably weakening the [[associativity]] and [[unitality]] conditions on the enrichment.  Thus, it has a collection of objects with [[hom-objects]] $C(x,y)\in\mathcal{V}$.  It may also naturally be called a **pseudo enriched category**.

A different notion that is also sometimes called an **enriched bicategory** is that of a [[bicategory]] enriched over a [[monoidal category|monoidal 1-category]] $V$ (which must be at least [[braided monoidal category|braided]]) at the level of 2-cells only.  Thus it has a collection of objects, with 1-morphisms between the objects, and for any parallel 1-morphisms $f,g\colon x\to y$, a hom-object $C(x,y)(f,g) \in V$.  This can be identified with a $(V Cat)$-enriched bicategory in the previous sense, so on this page we focus on the former, more general, definition.


## Definition

For $\mathcal{V}$ a [[monoidal bicategory]], a  $\mathcal{V}$-enriched (bi)category $C$ consists of

* a collection of [[object]]s;

* for every ordered pair $(x,y)$ of objects a [[hom-object]] $C(x,y) \in \mathcal{V}$

* for every ordered triple $(x,y,z)$ a [[composition]] morphism of the form

  $$
    comp_{x,y,z} : C(x,y)\otimes C(y,z) \to C(x,z)
  $$ 

  in $\mathcal{V}$

* for every object $x$ an [[identity]] morphism

  $$
    i_x : I \to C(x,x) 
  $$

  from the tensor unit of $\mathcal{V}$;

* a [[natural isomorphism|natural 2-ismorphism]]

  $$
    \alpha : comp(Id \otimes comp) \Rightarrow comp(comp \otimes Id)
  $$
 
  called the [[associator]]

* similarly left and right [[unitor]]s

* such that some more or less evident [[coherence]] conditions hold (see the references).


## Examples

* When $\mathcal{V} = Cat$, a $\mathcal{V}$-enriched bicategory is just a plain [[bicategory]].

* When $\mathcal{V}$ is an ordinary [[monoidal category]], a $\mathcal{V}$-enriched bicategory is just an ordinary [[enriched category]].

* When $\mathcal{V}$ is the cartesian monoidal 2-category of bicategories, pseudo [[2-functors]], and [[icons]], then a $\mathcal{V}$-enriched bicategory is an [[iconic tricategory]].

* When $\mathcal{V}$ is the cartesian monoidal 2-category of [[fully faithful functors]], then a $\mathcal{V}$-enriched bicategory is a weak [[F-category]].

## References

Bicategories enriched in monoidal 2-categories first appeared in:

* Syméon Bozapalides, _Théorie formelle des bicatégories_, PhD thesis, 1976.

* Syméon Bozapalides, _Bicatégories relatives à une 2-catégorie multiplicative_, [[CRAS]], 1976.

The definition appeared independently in:

* S. M. Carmody, _Cobordism Categories_, PhD thesis, University of Cambridge, 1995.

A definition also appeared in 

* [[Steve Lack]], _The algebra of distributive and extensive categories_ , PhD thesis, University of Cambridge, 1995.

Forcey has studied the combinatorics of [[polytope]]s associated to enrichment and [[higher category theory|higher categories]] in detail. See for example

* S. Forcey, _Quotients of the Multiplihedron as Categoried Associahedra_ ,  ([arXiv:0803.2694](http://arxiv.org/abs/0803.2694)).

The definition is reviewed in 

* [[Alex Hoffnung]], _Notes on enrichment_, ([[Hoffnung_enrichment.pdf:file]]),

and in Chapter 7 of

* [[Alex Hoffnung]], _Foundations of Categorified Representation Theory_ ([pdf](https://math.ucr.edu/home/baez/thesis_hoffnung.pdf))

and studied further in

* [[Richard Garner]] and [[Mike Shulman]], *Enriched categories as a free cocompletion*, [arXiv](http://arxiv.org/abs/1301.3191)

A theorem about representing lax enriched functors as lax algebras:

* [[Cristina Pedicchio]], _Relazioni tra K-morfismi e lax-algebre_ (1979), [pdf](https://www.openstarts.units.it/server/api/core/bitstreams/504222d5-c20e-4243-b8c3-cb0e94dafdae/content)

[[!redirects enriched bicategories]]
[[!redirects enriched 2-category]]
[[!redirects pseudo enriched category]]
[[!redirects enriched 2-categories]]
[[!redirects pseudo enriched categories]]
[[!redirects category enriched over a monoidal bicategory]]
[[!redirects category enriched over a monoidal 2-category]]
[[!redirects category enriched in a monoidal bicategory]]
[[!redirects category enriched in a monoidal 2-category]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _semi-simplicial object_ is like a [[simplicial object]], but without degeneracy maps. In [[Set]] it is a [[semi-simplicial set]].

## Definition

### In terms of functors

For $\mathcal{C}$ a [[category]] or [[(∞,1)-category]], a semi-simplicial object $X$ in $\mathcal{C}$ is a [[functor]] or [[(∞,1)-functor]]
$$
  X \colon \Delta_+^{op}  \to \mathcal{C}
$$
from $\Delta_+$, the [[wide subcategory]] of the [[simplex category]] on the injective functions (the co-face maps).

### In homotopy type theory

One may try to formulate semi-simplicial [[types]] in [[homotopy type theory]]. See the discussion at ([IAS](#IAS)).

## Properties

### Directedness

As opposed to the [[simplex category]] $\Delta$, the subcategory $\Delta_+$ is a [[direct category]].

## Examples
 {#Examples}

* in [[Sets]]: [[semisimplicial set]]:

* in [[TopologicalSpaces]]: [[semi-simplicial topological space]]

* in [[SimplicialSets]]: [[semi-Segal space]] (if extra conditions are met)

* in [[type theory]]: [[homotopytypetheory:semi-simplicial types]]

## Related concepts

* [[simplicial object]]

  * [[simplicial set]]

  * [[simplicial object in an (∞,1)-category]]

* **semi-simplicial object**

  * [[semisimplicial set]]

* [[semi-category]]

  * [[semi-Segal space]]

* [[Homotopy Type System]] ("HTS")

## References
 {#References}

> For more references see also at _[[semi-simplicial set]]_ and _[[semi-Segal space]]_.

### Semi-simplicial bundles

Discussion of semi-simplicial [[fiber bundles]] is in 

* M. Barratt, V. Gugenheim and J. C. Moore, _On semisimplicial fibre bundles_, Amer. J. Math. 81 (1959), 639-657.

* S. Weingram, _The realization of a semisimplicial bundle map is a $k$-bundle map_ ([pdf](http://www.ams.org/journals/tran/1967-127-03/S0002-9947-1967-0231382-7/S0002-9947-1967-0231382-7.pdf))

### In homotopy type theory
 {#ReferencesInHomotopyTypeTheory}

Discussion of formulation of semsiplicial [[types]] in the context of [[homotopy type theory]] (for use as discussed at _[[category object in an (infinity,1)-category]]_) is in

* [[UF-IAS-2012]], _[Semi-simplicial types](http://uf-ias-2012.wikispaces.com/Semi-simplicial+types)_
 {#IAS}

[[Coq]]-code for semi-simplicial types in [[homotopy type theory]] had been proposed in

* [[Vladimir Voevodsky]], _[semisimplicial.v](http://uf-ias-2012.wikispaces.com/file/detail/semisimplicial.v)_

but its execution requires augmenting [[homotopy type theory]] with an auxilirary [[extensional type theory|extensional]] [[identity type]], discussed in 

* [[Vladimir Voevodsky]], _A type system with two kinds of identity types_ (Feb. 2013) ([pdf](http://uf-ias-2012.wikispaces.com/file/view/HTS_slides.pdf/410105196/HTS_slides.pdf))

See at _[[Homotopy Type System]]_ ("HTS") for more on this.

More along these lines is in 

* [[Hugo Herbelin]], _A dependently-typed construction of semi-simplicial types_ (March 2013) ([pdf](http://uf-ias-2012.wikispaces.com/file/view/semi-simplicial.pdf/416038766/semi-simplicial.pdf))


* [[Bruno Barras]], [[Thierry Coquand]], Simon Huber, _A generalization of Takeuti-Gandy Interpretation_  ([pdf](https://uf-ias-2012.wikispaces.com/file/view/semi.pdf))

[[!redirects semi-simplicial object]]
[[!redirects semisimplicial object]]
[[!redirects semi-simplicial objects]]
[[!redirects semisimplicial objects]]

[[!redirects semi-simplicial type]]
[[!redirects semisimplicial type]]
[[!redirects semi-simplicial types]]
[[!redirects semisimplicial types]]
[[!redirects category of semisimplices]]
[[!redirects categories of semisimplices]]

[[!redirects semisimplicial]]
[[!redirects semi-simplicial]]

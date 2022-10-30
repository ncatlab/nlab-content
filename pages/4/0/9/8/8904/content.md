
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
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

## Related concepts

* [[simplicial object]]

  * [[simplicial set]]

  * [[simplicial object in an (∞,1)-category]]

* **semi-simplicial object**

  * [[semisimplicial set]]

* [[semi-category]]

  * [[semi-Segal space]]

## References

Discussion of semi-simplicial [[fiber bundles]] is in 

* M. Barratt, V. Gugenheim and J. C. Moore, _On semisimplicial fibre bundles_, Amer. J. Math. 81 (1959), 639-657.

* S. Weingram, _The realization of a semisimplicial bundle map is a $k$-bundle map_ ([pdf](http://www.ams.org/journals/tran/1967-127-03/S0002-9947-1967-0231382-7/S0002-9947-1967-0231382-7.pdf))

Discussion of formulation of semsiplicial [[types]] in the context of [[homotopy type theory]] is in

* [[UF-IAS-2012]], _[Semi-simplicial types](http://uf-ias-2012.wikispaces.com/Semi-simplicial+types)_
 {#IAS}

[[Coq]]-code for semi-simplicial types in [[homotopy type theory]] is at 

* [[Vladimir Voevodsky]], _[semisimplicial.v](http://uf-ias-2012.wikispaces.com/file/detail/semisimplicial.v)_

For more references see those at _[[semi-simplicial set]]_ and _[[semi-Segal space]]_.

[[!redirects semi-simplicial object]]
[[!redirects semisimplicial object]]
[[!redirects semi-simplicial objects]]
[[!redirects semisimplicial objects]]

[[!redirects semi-simplicial type]]
[[!redirects semisimplicial type]]
[[!redirects semi-simplicial types]]
[[!redirects semisimplicial types]]

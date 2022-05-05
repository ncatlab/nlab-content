
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[morphism]] $f\colon A\to B$ in a [[2-category]] $K$ is said to be **(representably) faithful** if for all objects $X$, the induced [[functor]]
$$K(X,A) \to K(X,B)$$
is [[faithful functor|faithful]].  In [[Cat]], this is equivalent to $f$ being faithful in the usual sense.

## Remarks

* Faithful morphisms may also be called **2-monic** and said to make their [[source]] into a **2-subobject** of their [[target]].  See [[subcategory]] for discussion.

* Faithful morphisms often form the right class of a [[factorization system in a 2-category|factorization system]].  In [[Cat]], the left class consists of [[essentially surjective functor|essentially surjective]] and [[full functor|full]] functors.

* Of course, any [[fully faithful morphism]] is also faithful, and in particular any [[inverter]] or [[equifier]] is faithful.  Moreover, any [[inserter]] is also faithful, though not generally fully-faithful.

## Related pages

* the analogous concept in [[(∞,1)-categories]] is that of _[[0-truncated morphism of an (∞,1)-category|0-truncated morphisms]]_ (see <a href="n-truncated+object+of+an+(infinity,1)-category#TruncatedMorphismsBetweenGroupoids">there</a>).


* [[subcategory]]
* [[fully faithful morphism]]
* [[conservative morphism]]
* [[pseudomonic morphism]]
* [[discrete morphism]]

[[!redirects faithful morphisms]]
[[!redirects 2-monic morphism]]
[[!redirects 2-monic morphisms]]
[[!redirects 2-subobject]]
[[!redirects 2-subobjects]]

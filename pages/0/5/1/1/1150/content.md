
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

In the most general sense, a **bundle** over an [[object]] $B$ in a [[category]] $\mathcal{C}$ is simply an object $E$ of $\mathcal{C}$ equipped with a [[morphism]] in $\mathcal{C}$ from $E$ to $B$:
$$ \array { E \\ \downarrow^{\mathrlap{p}} \\ B } $$

One often refers to such a bundle simply as $E$, even though $B$ is really part of the data.

For $x \in B$ a [[generalized element]] of $B$, the [[fiber]] $E_x$ of the bundle over $x$ is the [[pullback]] $x^* E$.

Given two bundles $E_1$ and $E_2$ over $B$, then a _morphism of bundles over $B$_ is a [[morphism]] $E_1 \to E_2$ which makes this [[commuting diagram|diagram commute]]:

$$
  \array{
    E_1 && \longrightarrow && E_2
    \\
    & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && B 
  }
  \,.
$$

This way bundles over $B$ form a [[category]], also called the _[[slice category]]_ $\mathcal{C}_{/B}$ of $\mathcal{C}$ over $B$.


## Bundles with extra structure and properties

One generally considers bundles with extra properties or structure:


* [[fiber bundle]],

* [[microbundle]]

* [[principal bundle]]

* [[vector bundle]],

* [[connection on a bundle|bundle with connection]]

  * [[Simons-Sullivan structured bundle]]

* etc.

## The collection of all bundles

The category of bundles over a given object $B$ is the [[over category]] $\mathcal{C}/B$. The collection of all bundles in a given [[category]] $\mathcal{C}$ therefore arranges itself into the [[codomain fibration]] $cod : [I,\mathcal{C}] \to \mathcal{C}$. As such, the [[descent]] for bundles may be expressed as [[monadic descent]] with respect to the codomain [[bifibration]]. This does in general not work inside one of the more restrictive subcategories of bundles with extra structure and property, as the push-forward operation typically does not respect these extra conditions. For more on this see [monadic descent of bundles](http://ncatlab.org/nlab/show/monadic+descent#ForCodomainFibs).

## Related concepts

* Bundles tend to have [[sheaf|sheaves]] of local [[section]]s.

* In [[physics]], [[gauge field]]s may be described in terms of [[connection on a bundle|bundles with connection]].

## Related concepts

* **bundle**, [[display map]]

* [[sub-bundle]]

* [[retractive space]]

* **[[fiber bundle]]** / [[fiber ∞-bundle]]

  * [[associated bundle]]

  * [[vector bundle]]

    * [[line bundle]]

    * [[stable vector bundle]]

  * [[sphere bundle]]

  * [[natural bundle]]

  * [[equivariant bundle]]

  * [[bundle of spectra]]

  * [[fiber bundles in physics]]

* [[principal bundle]] / [[torsor]] / [[associated bundle]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]]

* [[(∞,1)-vector bundle]] / [[(∞,n)-vector bundle]]

  * [[spherical fibration]]

## References

Introductory notes on [[fiber bundles]], [[vector bundles]] and [[connections on bundles]]:

* Steven Bradlow, [Vector bundles and introduction to gauge theory](http://cwillett.imathas.com/bundles/)

See also many references at *[[fiber bundles in physics]]*.


[[!redirects bundles]]

[[!redirects bundle morphism]]
[[!redirects bundle morphisms]]

[[!redirects bundle homomorphism]]
[[!redirects bundle homomorphisms]]

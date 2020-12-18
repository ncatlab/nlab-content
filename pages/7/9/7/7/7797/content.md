
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $X$ a [[space]] with a notion of _[[dimension]]_ $n = dim(X) \in \mathbb{N}$ and a notion of ([[Kähler differential form|Kähler]]) [[differential forms]] on it, the _canonical bundle_ or [[canonical sheaf]] over $X$ is the [[line bundle]] (or its  [[sheaf]] of [[sections]]) of $n$-forms on $X$, the $dim(X)$-fold [[exterior product]] 

$$
  L_{can} \coloneqq \Omega^n_X 
$$

of the bundle $\Omega^1_X$ of 1-forms.




The [[first Chern class]] of this bundle is also called the **canonical [[characteristic class]]** or just the **canonical class** of $X$.

The inverse of the canonical line bundle (i.e. that with minus its [[first Chern class]]) is called the _anticanonical line bundle_.

Over an [[algebraic variety]], the [[divisor (algebraic geometry)|divisor]] corresponding to the canonical line bundle is called the _[[canonical divisor]]_.

A [[square root]] of the canonical class, hence another characteristic class $\Theta$ such that the [[cup product]] $2 \Theta = \Theta \cup \Theta$ equals the canonical class is called a _[[Theta characteristic]]_ (see also _[[metalinear structure]]_).

## Examples

### In complex analytic geometry
 {#InComplexAnalysis}

For $X$ [[complex manifold]] regarded over the complex numbers, then [[Kähler differential forms]] are _holomorphic_ forms. Hence the canonical bundle for $dim_{\mathbb{C}}(X) = n$ is $\Omega^{n,0}$ (see also at _[[Dolbeault complex]]_), a [[complex line bundle]].

For $X$ a [[Riemann surface]] of [[genus of a surface|genus]] $g$, the [[degree of a coherent sheaf|degree]] of the canonical bundle is $2 g - 2$. This means it is divisible by 2 and hence there are "[[Theta characteristic]]" square roots.

In particular the [[first Chern class]] of the canonical bundle on the [[2-sphere]] is _twice_ that of the [[basic line bundle on the 2-sphere]], the generator in $H^2(S^2, \mathbb{Z}) \simeq \mathbb{Z}$. See also at _[[geometric quantization of the 2-sphere]]_.


## Related concepts

* [[density bundle]]

* [[volume form]]

* [[Kodaira vanishing theorem]]

[[!include square roots of line bundles - table]]



## References

In the context of [[algebraic geometry]]:

* Vladimir Lazi&#263; _Lecture 7. Canonical bundle, I and II_ (2011) ([pdf I](http://www.staff.uni-bayreuth.de/~btm113/AGlect7.pdf), [pdf II](http://www.staff.uni-bayreuth.de/~btm113/AGlect8.pdf))

See also

* Wikipedia, _[Canonical bundle](http://en.wikipedia.org/wiki/Canonical_bundle)_

[[!redirects canonical bundles]]

[[!redirects canonical class]]
[[!redirects canonical characteristic class]]
[[!redirects canonical classes]]
[[!redirects canonical characteristic classes]]

[[!redirects canonical line bundle]]
[[!redirects canonical line bundles]]

[[!redirects anticanonical line bundle]]
[[!anticanonical line bundles]]

[[!redirects anti-canonical line bundle]]
[[!anti-canonical line bundles]]




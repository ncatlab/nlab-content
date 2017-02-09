
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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


## Definition

A _line bundle_ is a [[vector bundle]] of rank (or [[dimension]]) $1$, i.e. a vector bundle whose typical fiber is a $1$-dimensional [[vector space]] (a [[line]]).

For complex vector bundles, [[complex line]] bundles are canonically [[associated bundles]] of [[circle group]]-[[principal bundles]].

## Properties

The class of line bundles has a nicer behaviour (in some ways) than the class of vector bundles in general.  In particular, the [[dual vector bundle]] of a line bundle $L$ is a [[weak inverse]] of $L$ under the tensor product of line bundles.  Thus the isomorphism classes of line bundles form a [[group]].

## Examples

+-- {: .num_example}
###### Example

The [[Möbius strip]] is the unique, up to [[isomorphism]], non-trivial [[real vector bundle|real]] line bundle over the [[circle]].

=--

+-- {: .num_example}
###### Example

Over any [[manifold]] there is canonically the _[[density line bundle]]_ which is the [[associated bundle]] to the [[principal bundle]] underlying the [[tangent bundle]] by the [[determinant]] homomorphism.

=--

Similarly:

+-- {: .num_example #CanonicalLineBundle}
###### Example

Every [[orientable]] [[complex manifold]] carries a [[complex vector bundle|comple]] line bundle of top-degree [[holomorphic differential forms]]. This is called its _[[canonical line bundle]]_. 

=--

+-- {: .num_example}
###### Example

The line bundle on the [[2-sphere]] whose [[first Chern class]] is a generator of $H^2(S^2, \mathbb{Z}) \simeq \mathbb{Z}$ is the [[pullback bundle]] of the [[universal complex line bundle]] (example \ref{UniversalComplexLineBundle}) along the map

$$
  S^2 \longrightarrow B U(1) \simeq B^2 \mathbb{Z}
$$

which itself represents the generator in the second [[homotopy group]] $\pi_2(S^2) \simeq \mathbb{Z}$.

Beware that this is _not_ the "[[canonical line bundle]]" from example \ref{CanonicalLineBundle}, but "half" of it, its [[theta characteristic]]. See at _[[geometric quantization of the 2-sphere]]_ for more on this.

=--

+-- {: .num_example #UniversalComplexLineBundle}
###### Example

The [[classifying space]]/[[Eilenberg-MacLane space]] $B U(1) \simeq B^2 \mathbb{Z}$ carries the [[circle group]]-[[universal principal bundle]]. The corresponding [[associated bundle]] via the canonical [[action]] of $U(1)$ on $\mathbb{C}$ is the [[universal complex line bundle]].

=--

+-- {: .num_example}
###### Example

The [[product]] of any [[space]] $X$ with the [[moduli stack]] $Pic_X$ of line bundles over it (its [[Picard stack]]) carries a tautological line bundle. This is called the _[[Poincaré line bundle]]_ of $X$.

=--

## Related concepts

* [[complex vector space]]

  * [[complex line]]

* [[complex vector bundle]]

  * [[complex line bundle]]

* [[holomorphic line bundle]], [[algebraic line bundle]]

* [[theta characteristic]]

* [[cubical structure on a line bundle]]

* [[bundle gerbe]]

* [[circle n-bundle with connection]]

* [[line 2-bundle]]

* [[line n-bundle]]

[[!include moduli of higher lines -- table]]


[[!redirects line bundles]]

[[!redirects complex line bundle]]
[[!redirects complex line bundles]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[connection on a bundle]] may be understood as a construction that serves to interpolate between a [[principal bundle]] and its [[characteristic class]] in real cohomology, represented by [[curvature characteristic form]]s of the connection.

If one allows (and it makes good sense to allow this) curvature characteristic forms to be represented not necessarily by globally defined forms, but by [[cocycle]]s in the [[abelian sheaf cohomology]] of the truncated [[de Rham complex]] $\Omega^1(-) \stackrel{d_{dR}}{\to} \Omega^2(-) \to \cdots \to \Omega^n_{cl}(X)$ then a weaker notion than that of a connection serves the same purpose: that of a _pseudo-connection_ .

Effectively a pseudo-connection on a principal bundle is locally a collection of [[Lie-algebra valued 1-form]]s, that do _not_ have to satisfy the cocycle condition familiar from connections.

That makes pseudo-connections rather empty structures. And in a precise sense this is actually the point of them: there is a (non-concrete) [[Lie groupoid]] $\mathbf{B}G_{diff}$ such that [[Cech cohomology|Cech cocycles]] with values in it are those for $G$-principal bundles with pseudo-connections. This groupoid is in fact weakly equivalent to the [[delooping]] groupoid $\mathbf{B}G$ that serves to classify just bare smooth $G$-principal bundles

$$
  \mathbf{B}G_{diff} \stackrel{\simeq}{\to} \mathbf{B}G
  \,.
$$

The purpose of pseudo-connections is precisely to form this [[resolution]] of $\mathbf{B}G$, which allows to represent an intrinsic curvature characteristic class to be modeled by an [[anafunctor]] with tip $\mathbf{B}G_{diff}$.

While for ordinary $G$-principal bundles the notion of pseudo-connection can be (and traditionally is) circumvented, it does become crucial for [[gerbe]]s and [[principal 2-bundle]]s and more generally in [[infinity-Chern-Weil theory]]. For instance an [[equivariant cohomology|equivariant]] [[gerbe]] _with_ connection is _not_ an equivariant object in the 2-category of gerbes with ordinary connections, but a certain constrained equivariant gerbe with pseudo-connection.

## Details

For the moment see [[infinity-Chern-Weil theory]]. 



(...)

## References

The term _pseudo-connection_ for generalized connections on [[bundle gerbe]]s apparently first appeared in 

(...)

Not under this name, but being the same concept, they are considered on bundle gerbes in some detail in 

* [[Konrad Waldorf]], ...



[[!redirects pseudo-connections]]
[[!redirects pseudo connection]]
[[!redirects pseudo connections]]
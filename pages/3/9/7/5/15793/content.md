
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A type of [[fiber bundle]] (usually: [[vector bundle]]) over ([[smooth manifold|smooth]]) [[manifolds]] is called _natural_ if suitable homomorphisms of manifolds naturally lift to morphisms of the corresponding bundles covering them.

The archetypical example is the [[tangent bundle]] $T X$ of a manifold $X$. For $f \colon X \to Y$ any [[smooth function]] then push-forward of vector fields yields a fiberwise linear morphism $d f \colon T X \to T Y$ of tangent bundles which covers $f$, in that the [[diagram]]

$$
  \array{
    T X &\stackrel{d f}{\longrightarrow}& T Y
    \\
    \downarrow && \downarrow 
    \\
    X &\stackrel{f}{\longrightarrow}& Y
  }
$$

[[commuting diagram|commutes]]. (This functoriality of the tangent bundle construction is incidentally also the incarnation of the [[chain rule]] (see there) of [[differentiation]]).

Formally, there is a [[category]] of fiber bundles over manifolds with [[morphisms]] the morphisms of bundles covering morphisms of the base spaces, and there is a projection functor from fiber bundles to their base manifolds. A natural bundle is a [[section]] of this projection functor.

Also "contravariantly natural" bundles such as bundle of [[covectors]] are sometimes referred to as natural bundles (e.g. [Kolar-Michor-Slovak](#KolarMichorSlovak)). But these are covariantly natural not with respect to all smooth functions between manifolds, but only for [[local diffeomorphisms]].

## Examples

* [[tractor bundle]]

## References

Originally introduced in

* [[Albert Nijenhuis]], _Geometric aspects of formal differential operations on tensor fields_, Proceedings of the International Congress of Mathematicians 1958, 463–469.

* [[Albert Nijenhuis]], _Natural bundles and their general properties_, in: _Differential Geometry (in honor of Kentaro Yano)_, Kinokuniya, Tokyo, 1972, pp. 317–334.

A comprehensive reference is available in

* {#KolarMichorSlovak} [[Ivan Kolář]], [[Peter Michor]], [[Jan Slovák]], section 14 of _[[Natural operations in differential geometry]]_ ([pdf](http://www.emis.de/monographs/KSM/kmsbookh.pdf))


[[!redirects natural bundles]]

[[!redirects natural vector bundle]]
[[!redirects natural vector bundles]]

[[!redirects natural operation]]
[[!redirects natural operations]]

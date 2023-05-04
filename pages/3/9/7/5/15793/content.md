
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

Also "contravariantly natural" bundles such as bundle of [[covectors]] are sometimes referred to as natural bundles (e.g. [Kolář-Michor-Slovak](#KolarMichorSlovak)). But these are covariantly natural not with respect to all smooth functions between manifolds, but only for [[local diffeomorphisms]].

## Examples

* [[tractor bundle]]

* [[Schouten-Nijenhuis bracket]]

## References

Originally introduced in

* [[Albert Nijenhuis]], _Geometric aspects of formal differential operations on tensor fields_, Proceedings of the International Congress of Mathematicians 1958, 463–469.  [PDF](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1958/ICM1958.ocr.pdf).

* [[Albert Nijenhuis]], _Natural bundles and their general properties_, in: _Differential Geometry (in honor of Kentaro Yano)_, Kinokuniya, Tokyo, 1972, pp. 317–334.  [PDF](https://dmitripavlov.org/scans/nijenhuis-natural-bundles-and-their-general-properties.pdf).

A comprehensive reference is available in

* {#KolarMichorSlovak} [[Ivan Kolář]], [[Peter Michor]], [[Jan Slovák]], section 14 of: _[[Natural operations in differential geometry]]_, Springer (1993) &lbrack;[webpage](https://www.emis.de/monographs/KSM/), [doi:10.1007/978-3-662-02950-3](https://link.springer.com/book/10.1007/978-3-662-02950-3), [pdf](http://www.emis.de/monographs/KSM/kmsbookh.pdf)&rbrack;

The example of the [[Schouten-Nijenhuis bracket]]:

* {#Michor87} [[Peter W. Michor]], *Remarks on the Schouten-Nijenhuis bracket*,  In: Bureš, J. and Souček, V. (eds.): *Proceedings of the Winter School "Geometry and Physics"* Circolo Matematico di Palermo, Palermo (1987) 207-215 &lbrack;[dml:701423](https://dml.cz/handle/10338.dmlcz/701423), [pdf](https://dml.cz/bitstream/handle/10338.dmlcz/701423/WSGP_07-1987-1_21.pdf), [[Michor-SchoutenNijenhuisBracket.pdf:file]]&rbrack;


[[!redirects natural bundles]]

[[!redirects natural vector bundle]]
[[!redirects natural vector bundles]]

[[!redirects natural operation]]
[[!redirects natural operations]]

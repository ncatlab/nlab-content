
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--


# Functors of descent type

* table of contents
{: toc}

## Idea

A functor is of *descent type* if it satisfies "half" of the condition to be [[monadic]].

## Definition

A functor $U:B\to A$ is of **descent type** (or is **premonadic**) if 

1. it has a [[left adjoint]] $F:A\to B$, and
2. for all $b\in B$ the canonical [[fork]] $F U F U b \underoverset{F U \epsilon}{\epsilon F U}{\rightrightarrows} F U b \xrightarrow{\epsilon} b$ is a [[coequalizer]].

The second condition is equivalent to asking that the comparison functor $B \to A^{U F}$ from $B$ to the [[Eilenberg-Moore category]] of the [[monad]] $U F$ is [[fully faithful]]. When the comparison functor is [[essentially surjective]] (hence an [[equivalence of categories]]), $U$ is of [[effective descent type]] or [[monadic]].

## Examples

By [[monadic descent]], a morphism $f$ in the base of a [[fibration]] is a [[descent morphism]] if and only if $f^*$ is of descent type.  This is presumably the origin of the terminology; $f$ is an [[effective descent morphism]] when $f^*$ is monadic.

## Related pages

* [[monadic functor]], [[monadicity theorem]]
* [[descent]], [[monadic descent]]

[[!redirects descent type]]
[[!redirects functors of descent type]]
[[!redirects premonadic functor]]
[[!redirects premonadic functors]]

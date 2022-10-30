
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Extensional type theory is_ the flavor of [[type theory]] in which [[function extensionality]] holds by identities: two [[terms]] $f, g$ of [[function types]] are identified if all their values agree, if $\forall x, f(x) = g(x)$.

If this distinction is not made, one speaks of [[intensional type theory]]. If, however, the [[univalence axiom]] is added to intensional type theory -- to obtain [[homotopy type theory]] -- then function extensionality holds again, but only by [[equivalence]].

## Properties

### Decidibility

Only the intensional but not the [[extensional type theory|extensional]] [[Martin-Löf type theory]] is [[decidable]]. See _[[intensional type theory]]_ for more on this.

## References

Among the most thorough recent treatments of extensional type theory are

* [[Ieke Moerdijk]], E. Palmgren, _Wellfounded trees in categories_. Ann. Pure Appl. Logic, 104:189-218 (2000)

* [[Ieke Moerdijk]], E. Palmgren, _Type theories, toposes and constructive set theory: predicative aspects of AST_,  Ann. Pure Appl. Logic, 114:155-201, (2002)


[[!redirects intensional type theories]]

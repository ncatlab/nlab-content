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

## Idea ##

The type-theoretic version of the fact that in [[set theory]] [[functions]] preserve [[equality]] between [[elements]] in [[sets]]. 

## Definition ##

In [[Martin-Löf type theory]], given [[types]] $A$ and $B$, a [[function]] $f:A \to B$, and [[terms]] $a:A$ and $b:A$, there is a function $\mathrm{ap}_f:(a =_A b) \to (f(a) =_B f(b))$ called the **action on [[identifications]] of $f$** or the **application of $f$ to identifications**. 

## See also ##

* [[identification]]
* [[identity type]]

## References ##

* [[Univalent Foundations Project]], [[Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects application of a function to identifications]]
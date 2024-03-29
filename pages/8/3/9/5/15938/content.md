
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[formal logic]] one speaks of a "fragment" of a [[theory]] when referring to just part of it. Specifically, when rules of [[type formation]] or some of the [[natural deduction|inference rules]] are omitted, one says that one retains a "fragment" of the original theory.

This terminology is jargon and has not been formalized. What exactly counts as a fragment of a theory and what not differs a bit from author to author.

## Examples

### First-order logic in type theory
 {#FirstOrderFragment}

In [[type theory]] [[first order logic]] of [[propositions]] is contained via "[[propositions as types]]" essentially as the sub-theory dealing with types of type [[Prop]], hence with [[bracket types]] or what in [[homotopy type theory]] are called [[(-1)-types]].

Some authors speak of the "first-order fragment" of type theory when referring to this restriction (e.g. [Bezem-Hendriks-Nivelle 02](#BezemHendriksNivelle2002), [Hendriks 13](#Hendriks13)).

### Multiplicative conjunction in linear logic

By default [[linear logic]] has a wealth of [[conjunctions]]. Discarding or ignoring all of them except the [[multiplicative conjunction]] yield the fragment of _[[multiplicative linear logic]]_.

## References

* {#BezemHendriksNivelle2002} Marc Bezem, Dimitri Hendriks, Hans de Nivelle, _Automated Proof Construction in Type Theory using Resolution_, 2002 ([pdf](http://www.phil.uu.nl/ozsl/articles/Hendriks01.pdf))

* {#Hendriks13} Dimitri Hendriks, _Metamathematics in Coq_, 2013 ([pdf](http://www.phil.uu.nl/ozsl/articles/Hendriks03.pdf))



[[!redirects fragments]]
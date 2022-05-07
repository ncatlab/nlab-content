
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Introduced by [Hovey 1998](#Hovey98), the notion of *semimodel categories* s a relaxation of that of [[model categories]] which allows for a largely similar theory.

The notion of a [[weak model category]] and [[premodel category]]
relaxes the definition even further.

## Definition

(See [Hovey 98](#Hovey98), Theorem 3.3.)

A __left semimodel category__ is a [[relative category]]
equipped with a class of [[cofibrations]] and [[fibrations]]
such that [[weak equivalences]] are closed under [[retracts]]
and the [[2-out-of-3 property]],
[[cofibrations]] have a [[left lifting property]] with respect
to [[trivial fibrations]],
[[trivial cofibrations]] with [[cofibrant]] source
have a [[left lifting property]] with respect to [[fibrations]],
and morphisms with [[cofibrant]] source
can be factored as a [[cofibration]] followed by a [[fibration]],
either one of which can be further made trivial.

A __right semimodel category__ is defined by passing to the [[opposite category]].

## Examples

\begin{example}
**([[semimodel structure on semisimplicial sets]])**
There exists a right semi-model structure on the category of [[semi-simplicial sets]] ([Rooduijn 2018](#Rooduijn2018)).
\end{example}

## References

The definition is due to:

* {#Hovey98} [[Mark Hovey]], _Monoidal model categories_ ([arXiv:math/9803002](https://arxiv.org/abs/math/9803002))

The example of the [[semimodel structure on semisimplicial sets]]:

* {#Rooduijn2018} Jan Rooduijn, *A right semimodel structure on semisimplicial sets*, Amsterdam 2018 ([pdf](https://eprints.illc.uva.nl/id/eprint/1663/1/MoL-2018-34.text.pdf), [mol:4787](https://msclogic.illc.uva.nl/theses/archive/publication/4787/A-right-semimodel-structure-on-semisimplicial-sets))

[[!redirects semimodel categories]]

[[!redirects semi-model category]]
[[!redirects semi-model categories]]

[[!redirects semimodel structure]]
[[!redirects semimodel structures]]
[[!redirects semi-model structure]]
[[!redirects semi-model structures]]



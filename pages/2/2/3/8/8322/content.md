
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



# The exchange rule
* table of contents
{: toc}

## Idea

In [[logic]], the _exchange rule_ or _permutation rule_ states that the order of the [[premise]]s is irrelevant to the validity of a [[deduction]].  Along with the [[weakening rule]] and the [[contraction rule]], it is one of the most commonly adopted [[structural rules]].

This rule is commonly discarded in [[linguistics|natural language parsers]], such as those built on [[categorial grammar]]s or similar, such as link-grammar. This is because in most natural languages, word-order matters; the proper "deduction" or parse of a sentence depends on the order of of "premises"/words.

## Statements

Exactly how this looks depends on the [[logic]] used.

One possible formulation allows us to derive $\Gamma, B, A, \Gamma' \vdash C$ from $\Gamma, A, B, \Gamma' \vdash C$.

## Related entries

* [[inference rule]]

* [[structural rule]]

* [[contraction rule]]

* [[weakening rule]]

## References

The notion of exchange as a [[structural inference rule]] originates (under the German name *Vertauschung*) with: 

* {#Gentzen35} [[Gerhard Gentzen]], §1.2.1 in: _Untersuchungen &#252;ber das logische Schlie&#223;en I_ _Mathematische Zeitschrift_ **39** 1 (1935) &lbrack;[doi:10.1007/BF01201353](http://dx.doi.org/10.1007/BF01201353)&rbrack;

* {#Gentzen69} [[Gerhard Gentzen]], §1.21 in: *Investigations into Logical Deduction*, in M. E. Szabo (ed.), *The Collected Papers of Gerhard Gentzen*, Studies in Logic and the Foundations of Mathematics **55**, Springer (1969) 68-131 &lbrack;[ISBN:978-0-444-53419-4](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/55), [pdf](https://logic-teaching.github.io/prop/texts/Gentzen%201969%20-%20Investigations%20into%20Logical%20Deduction.pdf)&rbrack;

On the [[categorical semantics]]:

* {#Jacobs98} [[Bart Jacobs]], p. 122 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;



[[!redirects exchange rule]]
[[!redirects exchange rules]]
[[!redirects permutation rule]]
[[!redirects permutation rules]]

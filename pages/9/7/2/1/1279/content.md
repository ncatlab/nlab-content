# Sequent calculus
* table of contents
{: toc}

## Introduction

Sequent calculus was introduced by Gerhard Gentzen in his 1933 thesis as a formal system for studying the properties of proof systems presented in the style of [[natural deduction]] (also introduced by Gentzen).  It has since been widely adopted over natural deduction in proof theory and automated theorem proving.

The sequent calculus incorporates the _cut rule_, which allows for the composition of proofs.  Gentzen's main result (the _Hauptsatz_) was that any sequent proof that uses the cut rule can be transformed into one that doesn't.  This yields a normalization algorithm for proofs, which provided much of the inspiration behind Lambek's approach to categorical logic.

The most important property of cut-free proofs is that every formula occuring anywhere in a proof is a subformula of a formula contained in the conclusion of the proof (the _subformula property_).  This makes induction over proof-trees much more straightforward than with natural deduction or other systems.


## References

* Gentzen, Gerhard.  'Untersuchungen &#252;ber das logische Schlie&#223;en I', _Mathematische Zeitschrift_ 39(1), Springer-Verlag 1935. &lt;http://dx.doi.org/10.1007/BF01201353>.

* The [Wikipedia article](http://en.wikipedia.org/wiki/Sequent_calculus) provides a good summary.


[[!redirects sequent calculus]]
[[!redirects sequent]]

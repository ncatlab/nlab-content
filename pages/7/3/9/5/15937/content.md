# Reverse mathematics
* table of contents
{: toc}

## Idea

_Reverse mathematics_ refers mainly to a program introduced by Harvey Friedman and Stephen Simpson, which aims to establish for many theorems of classical analysis exactly which set existence principles they rely on. They consider the formalization of analysis based on Polish spaces in the language of second order arithmetic (hence the need to focus on separable spaces). One then tries to show that various theorems are equivalent to a set existence axiom relative to a weak base theory, usually $\mathrm{RCA}_0$ (a finitistically reducible system axiomatizing recursive set comprehension only). The implication from a set existence axiom to a theorem is the usual (forward) direction of mathematics, while the implication from a theorem back to the axiom is _reverse_ direction of reverse mathematics.

There are other uses of the term reverse mathematics, notably _constructive reverse mathematics_ (see below).

## The "Big Five" subsystems

Work on reverses mathematics has isolated five subsystems of second order arithmetic that correspond to many classical theorems. For more information see [[ordinal analysis]].

These are in increasing order: $\mathrm{RCA}_0$, $\mathrm{WKL}_0$, $\mathrm{ACA}_0$, $\mathrm{ATR}_0$ and $\Pi^1_1{-}\mathrm{CA}_0$. The first two are finitistically reducible, but $\mathrm{WKL}_0$ introduces non-recursive sets. The system $\mathrm{ACA}_0$ has the same strength as first-order Peano arithmetic, $\mathrm{PA}$. The system $\mathrm{ATR}_0$ is predicatively reducible, while the system $\Pi^1_1{-}\mathrm{CA}_0$ corresponds to the first-order system $\mathrm{ID}_{\lt\omega}$ of finitely many generalized inductive definitions.

## Constructive reverse mathematics

_Constructive reverse mathematics_ refers to a similar program initiated by Ishihara which aims to calibrate non-constructive theorems with respect to non-constructive axioms over a constructive base theory. The non-constructive axioms he considers are

* Omniscience principles, in decreasing strength: LPO (limited principle of omniscience), WLPO (weak LPO), LLPO (lesser LPO).

* Variations of Markov's Principles (MP): WMP (Weak MP), MP$^{\vee}$ (disjunctive MP).

* Principles from Brouwer's intuitionism: FAN$_\Delta$ (detachable fan principle), BD-N (boundedness principle).

## References

* Stephen G. Simpson, _Subsystems of Second Order Arithmetic_, 2nd edition, Cambridge University Press, 2010.


* Wikipedia, _[Reverse mathematics](http://en.wikipedia.org/wiki/Reverse_mathematics)_

* _Natural examples of Reverse Mathematics outside classical analysis?_, [MO:q/185941](http://mathoverflow.net/q/185941/381)

In the context of [[constructive mathematics]]:

* [[Hajime Ishihara]], _Reverse Mathematics in Bishop's Constructive Mathematics_, Philosophia Scienti&#230;, CS 6 (2006) ([doi:10.4000/philosophiascientiae.406](https://doi.org/10.4000/philosophiascientiae.406),  [pdf](https://philosophiascientiae.revues.org/pdf/406))

* [[Hannes Diener]], *Constructive Reverse Mathematics*, 2018 ([arXiv:1804.05495](https://arxiv.org/abs/1804.05495), [dspace:ubsi/1306](https://dspace.ub.uni-siegen.de/handle/ubsi/1306))


[[!redirects constructive reverse mathematics]]

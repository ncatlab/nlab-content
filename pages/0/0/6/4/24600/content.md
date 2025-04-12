

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
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

Cubical path types are a form of [[path types]] in [[dependent type theory]] used in [[cubical type theories]]. 

A major difference between cubical path types and Martin-Löf identity types is the behaviour of the J rule. In Martin-Löf identity types the J rule holds up to definitional equality, but for cubical path types, the J rule only holds up to a path. 

Another difference is that [[transport]] generally behaves better with cubical path types.  Certain rules for the computation of transports in concrete type families hold up to definitional equality for cubical path types, but only up to an identification for Martin-Löf identity types. 

## Rules

The rules for (dependent) cubical path types are as follows

* Formation

$$\frac{\Gamma, i:I \vdash A \; \mathrm{type} \quad \Gamma \vdash a:[0/i]A \quad \Gamma \vdash b:[1/i]A}{\Gamma \vdash \mathrm{path}_{i.A}(a,b) \; \mathrm{type}}$$

* Introduction

$$\frac{\Gamma, i:I \vdash a:A}{\Gamma \vdash \lambda i.a:\mathrm{path}_{i.A}([0/i]a,[1/i]a)}$$

* Elimination

$$\frac{\Gamma \vdash p:\mathrm{path}_{i.A}(a,b) \quad \Gamma \vdash r:I}{\Gamma \vdash p(r):[r/i]A [\partial(r) \to [r \equiv 0 \to a \vert r \equiv 1 \to b]]}$$

* Computation

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash (\lambda i.a)(r) \equiv [r/i]a:[r/i]A}$$

* Uniqueness (optional)

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash p \equiv \lambda i.p(i) : \mathrm{path}_{i.A}(a,b)}$$

In addition, there are coercion and composition operations which make the path type behave like an identity type:

* Coercion:

$$\frac{\Gamma, i:I \vdash A \; \mathrm{type} \quad \Gamma \vdash a:[r/i]A}{\Gamma \vdash \mathrm{coe}^{r \rightsquigarrow r'}_{i.A} a:[r'/i]A \; [r' \equiv r \to a]}$$

* Composition:

...

## Regularity

In general, cubical path types in cubical type theory do not satisfy the J rule definitionally. However one could force the J rule to hold definitionally by appending a coercion [[regularity]] rule:

$$\frac{\Gamma, i:I, j:I \vdash A \equiv [j/i]A \; \mathrm{type}}{\Gamma \vdash \mathrm{coe}^{r \rightsquigarrow r'}_{i.A} a \equiv a:[r'/i]A}$$

to the type theory. 

## See also

* [[cubical type theory]]

* [[identity type]]

* [[indexed heterogeneous identity type]]

## References

On why cubical path types and Martin-Löf identity types are different:

* [[Andrew Swan]], *Separating Path and Identity Types in Presheaf Models of Univalent Type Theory*, ([arXiv:1808.00920](https://arxiv.org/abs/1808.00920))

On cubical path types in [[XTT]]:

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _Cubical syntax for reflection-free extensional equality_. In Herman Geuvers, editor, _4th International Conference on Formal Structures for Computation and Deduction (FSCD 2019)_, volume 131 of _Leibniz International Proceedings in Informatics (LIPIcs)_, pages 31:1-31:25. ([arXiv:1904.08562](https://arxiv.org/abs/1904.08562), [doi:10.4230/LIPIcs.FCSD.2019.31](https://doi.org/10.4230/LIPIcs.FCSD.2019.31))

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _A Cubical Language for Bishop Sets_, Logical Methods in Computer Science, 18 (1), 2022. ([arXiv:2003.01491](https://arxiv.org/abs/2003.01491)). 

[[!redirects cubical path]]
[[!redirects cubical paths]]

[[!redirects cubical path type]]
[[!redirects cubical path types]]

[[!redirects cubical identity type]]
[[!redirects cubical identity types]]


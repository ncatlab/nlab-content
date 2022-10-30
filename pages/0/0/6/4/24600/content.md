
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

Path types are an alternative to [[identity types]] in [[dependent type theory]]. They are primarily used in [[cubical type theories]]. 

A major difference between path types and identity types is the behaviour of the J rule. In [[identity types]] the J rule holds up to definitional equality, but for path types, the J rule only holds up to a path. 

Another difference is that [[transport]] behaves better with path types, holding up to definitional equality for path types but only up to an identification for [[identity types]]. 

## Regularity

In general, path types in cubical type theory do not satisfy the J rule definitionally. However one could force the J rule to hold definitionally by appending coercion operations: 

$$\frac{\Gamma, i:I \vdash A \; \mathrm{type} \quad \Gamma \vdash a:[r/i]A}{\Gamma \vdash \mathrm{coe}^{r \rightsquigarrow r'}_{i.A} a:[r'/i]A \; [r' \equiv r \to a]}$$

and a coercion [[regularity]] rule:

$$\frac{\Gamma, i:I, j:I \vdash A \equiv [j/i]A \; \mathrm{type}}{\Gamma \vdash \mathrm{coe}^{r \rightsquigarrow r'}_{i.A} a \equiv a:[r'/i]A}$$

to the type theory. 

## See also

* [[cubical type theory]]

* [[identity type]]

## References

On why path types and identity types are different:

* [[Andrew Swan]], *Separating Path and Identity Types in Presheaf Models of Univalent Type Theory*, ([arXiv:1808.00920](https://arxiv.org/abs/1808.00920))

On path types in [[XTT]]:

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _Cubical syntax for reflection-free extensional equality_. In Herman Geuvers, editor, _4th International Conference on Formal Structures for Computation and Deduction (FSCD 2019)_, volume 131 of _Leibniz International Proceedings in Informatics (LIPIcs)_, pages 31:1-31:25. ([arXiv:1904.08562](https://arxiv.org/abs/1904.08562), [doi:10.4230/LIPIcs.FCSD.2019.31](https://doi.org/10.4230/LIPIcs.FCSD.2019.31))

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _A Cubical Language for Bishop Sets_, Logical Methods in Computer Science, 18 (1), 2022. ([arXiv:2003.01491](https://arxiv.org/abs/2003.01491)). 

[[!redirects path type]]
[[!redirects path types]]
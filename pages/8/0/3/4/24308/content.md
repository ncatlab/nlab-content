+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

The counterpart of [[finite sets]] in [[type theory]]

## Definition ##

In [[type theory]], given [[natural numbers]] $n:\mathbb{N}$, the __family of finite types__ $\mathrm{Fin}_\mathcal{U}(n)$ of a universe $\mathcal{U}$ with empty type $\emptyset_\mathcal{U}:\mathcal{U}$, unit type $\mathbb{1}_\mathcal{U}:\mathcal{U}$, and binary coproducts $(-)+_\mathcal{U}(-):\mathcal{U} \times \mathcal{U} \to \mathcal{U}$ is an [[inductive family]] inductively defined by

$$\mathrm{Fin}_\mathcal{U}(0) \coloneqq \sum_{A:\mathcal{U}} A \cong_\mathcal{U} \emptyset_\mathcal{U}$$

$$\mathrm{Fin}_\mathcal{U}(s(n)) \coloneqq \sum_{A:\mathcal{U}} \left[\sum_{B:\mathrm{Fin}_\mathcal{U}(n)} A \cong_\mathcal{U} B +_\mathcal{U} \mathbb{1}_\mathcal{U}\right]$$

## See also ##

* [[natural numbers]]
* [[inductive family]]

## References ##

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* Marc Bezem, Ulrik Buchholtz, Pierre Cagne, Bjørn Ian Dundas, and Daniel R. Grayson, [Symmetry book](https://unimath.github.io/SymmetryBook/book.pdf) (2021) 

* Egbert Rijke, [[Introduction to Homotopy Type Theory]]
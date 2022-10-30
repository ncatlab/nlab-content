+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $C$ be a [[stable (∞,1)-category]] (or [[(∞,1)-topos]]) and $A \in C$ a stable coefficient object. For $X \in C$ and $n \in \mathbb{Z}$ or ($n \in \mathbb{N}$) write

$$
  H^n(X,A) := \pi_0 C(X, \mathbf{B}^n A)
$$

for the [[cohomology]] of $X$ with coefficients in $A$ in degree $n$.

Say a [[morphism]] in $C$ is _$A$-local_ if it induces [[isomorphism]]s on all these [[cohomology group]]s. Let $W$ be the [[class]] of all such morphisms. 

Then the $A$-**cohomology localization** of $C$ is -- if it exists -- the [[localization of an (∞,1)-category]] of $C$ at $W$.

## Examples

* At [[function algebras on ∞-stacks]] is discussed a class  of examples of cohomology localizations of [[(∞,1)-sheaf (∞,1)-toposes]] over [[site]]s of [[algebra over a Lawvere theory|algebras over]] an abelian [[Lawvere theory]] at cohomology with coefficients in the canonical [[line object]] $\mathbb{A}^1$.

## Related concepts

* [[homology localization]]

## References

[[set theory|Set theoretic]] issues in cohomology localization -- and their solution using [[large cardinal]] axioms such as [[Vopenka's principle]], is discussed in

* [[Carles Casacuberta]], Dirk Scevenels, [[Jeff Smith]], _Implications of large-cardinal principles in homotopical localization_  Advances in Mathematics Volume 197, Issue 1, 20 October 2005, Pages 120-139 

* Joan Bagaria, [[Carles Casacuberta]], A. R. D. Mathias, [[Jiri Rosicky]], _Definable orthogonality classes in accessible categories are small_ ([arXiv:1101.2792](http://arxiv.org/abs/1101.2792))

[[!redirects homotopy localizations]]
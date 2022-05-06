
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a _[[number field]]_ $K$, with [[ring of integers]] $\mathcal{O}_K$, then the _regulator_ $Reg_K$ is a number which measure the size of the [[group of units]] $GL_1(\mathcal{O}_K)$.

Since the [[determinant]] constitutes a group [[homomorphism]] $K_1 \to GL_1$ from first [[algebraic K-theory]] to the [[group of units]], the regulator may also be thought of as extracting information on the first [[algebraic K-theory]] group. This is the perspective taken in the generalization to _[[higher regulators]]_ (Beilinson regulators) which are effectivlely [[Chern characters]] for algebraic K-theory.

## Properties

### Relation to zeta function and class number formula

The [[Dedekind zeta function]] $\zeta_K$ of $K$ has a [[simple pole]] at $s = 1$. The _[[class number formula]]_ says that its [[residue]] there is proportional the the product of the regulator with the [[class number]] of $K$

$$
  \underset{s\to 1}{\lim} (s-1) \zeta_K(s)
  \propto
  ClassNumber_K \cdot Regulator_K
  \,.
$$

## Related concepts

* [[Dirichlet's unit theorem]]

* [[higher regulator]]

## References

* Wikipedia, _[Dirichlet's unit theorem](http://en.wikipedia.org/wiki/Regulator_of_a_number_field)_ -- _[The regulator](http://en.wikipedia.org/wiki/Regulator_of_a_number_field#The_regulator)_

[[!redirects regulators of a number field]]
[[!redirects regulators of number fields]]
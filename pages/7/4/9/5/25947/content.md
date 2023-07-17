+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[dependent type theory]] with [[judgmental equality]], a **congruence rule** is an [[inference rule]] which states that [[judgmental equality]] is respected. 

For example, there is a congruence rule for element conversion, which states that given judgmentally equal types $A$ and $B$ and judgmentally equal elements $a$ and $b$ of $A$, $a$ and $b$ are judgmentally equal elements of $B$:

$$\frac{\Gamma \vdash A \equiv B \; \mathrm{type} \quad \Gamma \vdash a \equiv b:A}{\Gamma \vdash a \equiv b:B}$$

## See also

* [[inference rule]]

* [[structural rule]]

## References

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))
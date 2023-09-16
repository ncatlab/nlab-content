
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

\tableofcontents

## Definition

Given a type $A$ and a type family $x:A \vdash B(x)$, **John Major equality** or **heterogeneous equality** is a type family indexed by $a:A$, $b:A$, $y:B(a)$, and $z:B(b)$, defined as the [[dependent sum type]] of the [[heterogeneous identity type]] $\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$ over all [[identifications]] $p:\mathrm{Id}_A(a, b)$. 

$$\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z) \coloneqq \sum_{p:\mathrm{Id}_A(a, b)} \mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$$

Suppressing the annotations in the equivalence above, the equivalence becomes

$$\mathrm{JMEq}(a, b, y, z) \coloneqq \sum_{p:\mathrm{Id}_A(a, b)} \mathrm{hId}(a, b, p, y, z)$$

Usually, these are defined for a [[Tarski universe]] $(U, \mathrm{El})$ or a [[Russell universe]] $(U, )$ (a zero-width whitespace character instead of $\mathrm{El}$), for which the type becomes

$$\mathrm{JMEq}(A, B, x, y) \coloneqq \sum_{p:\mathrm{Id}_U(A, B)} \mathrm{hId}(A, B, p, y, z)$$

## Related concepts

* [[heterogeneous identity type]]

## References

* [[Conor McBride]], *Dependently Typed Functional Programs and their Proofs*, (1999) $[$[pdf](https://www.lfcs.inf.ed.ac.uk/reports/00/ECS-LFCS-00-419/ECS-LFCS-00-419.pdf)$]$

* [[Théo Winterhalter]], *A conservative and constructive translation from extensional type theory to weak type theory*, Strength of Weak Type Theory, [[DutchCATS]], 11 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_winterhalter.pdf))

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

Given a type $A$ and a type family $x:A \vdash B(x)$, **John Major equality** or **heterogeneous equality** is a type family indexed by $a:A$, $b:A$, $y:B(a)$, and $z:B(b)$ representing the notion of equality between elements $y$ and $z$ over the type family $x:A \vdash B(x)$. There are a few different ways to define John Major equality: 

* as the [[dependent sum type]] of the [[heterogeneous identity type]] 
$$\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \equiv \mathrm{Id}_{B(b)}(\mathrm{transport}_{x:A.B(x)}(a, b, p)(y), z)$$ 
over all [[identifications]] $p:\mathrm{Id}_A(a, b)$. 

$$\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z) \coloneqq \sum_{p:\mathrm{Id}_A(a, b)} \mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$$

* as the [[identity type]] of [[dependent pairs]] in the [[dependent sum type]] $\sum_{x:A} B(x)$

$$\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z) \coloneqq \mathrm{Id}_{\sum_{x:A} B(x)}\left(\mathrm{pair}(a, y), \mathrm{pair}(b, z)\right)$$

By the extensionality property of [[dependent sum types]], these two definitions are equivalent. 

Usually, these are defined for a [[Tarski universe]] $(U, \mathrm{El})$ or a [[Russell universe]] $(U)$. Suppressing the annotations in John Major equality above, the type becomes $\mathrm{JMEq}(a, b, y, z)$, defined as one of 

$$\mathrm{JMEq}(A, B, x, y) \coloneqq \sum_{p:\mathrm{Id}_U(A, B)} \mathrm{hId}(A, B, p, y, z)$$

$$\mathrm{JMEq}(A, B, x, y) \coloneqq \mathrm{Id}_{\sum_{X:U} X}\left(\mathrm{pair}(x, A), \mathrm{pair}(y, B)\right)$$

for [[Russell universes]]

## Related concepts

* [[heterogeneous identity type]]

## References

For better or worse, the terminology "John Major equality" was coinded in [McBride 1999 §5.1.3](#McBride99) with reference to British political discussion of that times:

* {#McBride99} [[Conor McBride]], *Dependently Typed Functional Programs and their Proofs*, (1999) &lbrack;[pdf](https://www.lfcs.inf.ed.ac.uk/reports/00/ECS-LFCS-00-419/ECS-LFCS-00-419.pdf)&rbrack;

* [[Théo Winterhalter]], *A conservative and constructive translation from extensional type theory to weak type theory*, Strength of Weak Type Theory, [[DutchCATS]], 11 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_winterhalter.pdf))


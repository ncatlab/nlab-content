
> This article is about locally finite types in [[dependent type theory]]. For the notion of  [[homomorphisms]] between [[schemes]] which are locally of finite type, see [[morphism of finite type]]. 

---

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[dependent type theory]], a **locally finite type** or a **locally $Fin$-small type** is a type $A$ such that for all elements $x:A$ and $y:A$, there is a natural number $n:\mathbb{N}$ and an [[equivalence of types]] between the [[identity type]] $x =_A y$ and the standard [[finite type]] $\mathrm{Fin}(n)$. 

## Properties

Since finite types are [[h-sets]], every locally finite type is an [[h-groupoid]], because its identity types are all h-sets. 

## See also

* [[finite set]], [[finite type]]

* [[FinSet]]

* [[locally finite category]]

* [[locally small type]]
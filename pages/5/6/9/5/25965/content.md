
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

In [[dependent type theory]], a **locally finite type** is a type $A$ such that for all elements $x:A$ and $y:A$, there is a natural number $n:\mathbb{N}$ and an [[equivalence of types]] between the [[identity type]] $x =_A y$ and the standard [[finite type]] $\mathrm{Fin}(n)$. 

The type of all finite types is a [[univalent universe]] $Fin$; thus one could also refer to a locally finite type as a **locally $Fin$-small type**, since locally finite types are precisely the types that are [[locally small type|locally small]] relative to the univalent universe $Fin$ of finite types. 

## Examples

\begin{example}
Every [[locally finite category|locally finite]] [[univalent category]] is a locally finite type. 
\end{example}

\begin{example}
The locally finite [[h-sets]] are precisely the [[h-sets]] with [[decidable equality]]
\end{example}

## Properties

Since finite types are [[h-sets]], every locally finite type is an [[h-groupoid]], because its identity types are all h-sets. In particular, locally finite types are precisely the [[locally finite category|locally finite]] [[univalent categories]] which are [[groupoids]]. 

## See also

* [[finite set]], [[finite type]]

* [[FinSet]]

* [[locally finite category]]

* [[locally small type]]

* [[pi-finite type]]
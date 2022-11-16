
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Definition

A **De Morgan Heyting category** is a [[Heyting category]] $C$ (such as a [[topos]] or [[pretopos]]) in which for every object $X \in \mathrm{Ob}(C)$ the pseudocomplement of the intersection of two subobjects $A \in \mathrm{Sub}(X)$ and $B \in \mathrm{Sub}(X)$ is the union of the pseudocomplements of $A$ and $B$, $((A \cap B) \implies \emptyset) = (A \implies \emptyset) \cup (B \implies \emptyset)$. Equivalently, it is a Heyting category $C$ in which for every object $X \in \mathrm{Ob}(C)$ the union of the pseudocomplement of every [[subobject]] $A \in \mathrm{Sub}(X)$ and the double pseudocomplement of $A$ is an [[improper subobject]], $A \in \mathrm{Sub}(X)$, $(A \implies \emptyset) \cup ((A \implies \emptyset) \implies \emptyset) = \Im(X)$. 

Therefore, the [[subobject poset]] $Sub(X)$ of any [[object]] $X \in \mathrm{Ob}(C)$ is a [[De Morgan Heyting algebra]]. [[De Morgan's law]] and [[weak excluded middle]] hold in the [[internal logic]] of $C$. 

In addition, every De Morgan Heyting category $C$ is a [[first-order hyperdoctrine|first order]] [[De Morgan Heyting hyperdoctrine]] given by the [[subobject poset]] [[functor]] $\mathrm{sub}:\mathcal{C}^{op} \to DeMorgHeytAlg$. 

## See also

* [[De Morgan Heyting algebra]]

* [[Heyting category]]

* [[Boolean category]]

[[!redirects De Morgan Heyting category]]
[[!redirects De Morgan Heyting categories]]
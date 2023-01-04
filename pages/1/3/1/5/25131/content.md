
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[dependent type theory]], given a [[type]] $A$, the **automorphism type** on $A$ is the [[equivalence type]] between $A$ and $A$ itself, $\mathrm{Aut}(A) \coloneqq (A \simeq A)$. 

## Properties

$\mathrm{Aut}(A)$ forms an [[automorphism group]] in [[dependent type theories]] with [[UIP]] or [[axiom K]] and an [[automorphism infinity-group]] in type theories without [[UIP]] or [[axiom K]]. 

The automorphism type on an [[n-truncation modality|$n$-truncated type]] $A$ is an [[n-group|$(n + 1)$-group]]. 

Given a [[natural number]] $n:\mathbb{N}$, the automorphism type on a [[finite set]] with $n$ elements $\mathrm{Aut}(\mathrm{Fin}(n))$ has $n!$ elements, where $n!$ is the [[factorial]] of $n$. The automorphism type on the natural numbers $\mathrm{Aut}(\mathbb{N})$ is an [[uncountable set]], and in general, given an [[infinite set]] $A$, there is an equivalence $\mathrm{Aut}(A) \simeq (A \to \mathbb{2})$ between the automorphism type of $A$ and the function type from $A$ to the [[two-valued type]]. 

## See also

* [[equivalence type]]

* [[automorphism group]], [[automorphism infinity-group]]

* [[loop space type]] (for the equivalent for [[identity types]])

[[!redirects automorphism type]]
[[!redirects automorphism types]]

[[!redirects type of automorphisms]]
[[!redirects types of automorphisms]]
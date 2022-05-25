+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

## Definition ##

In a [[dependent type theory]] with [[identity types]], a subtype of a [[type]] $A$ is a type $B$ with a term 
$$i: \left[\sum_{f:B \to A} is1Monic(f)\right]$$ 
indicating the mere existence of a [[n-monomorphism|1-monic function]], where $[T]$ is the [[propositional truncation]] of $T$. This is different from a subtype with a chosen 1-monic function, a type $B$ with a term 
$$i: \sum_{f:B \to A} is1Monic(f)$$ 
in the same way that [[inhabited sets]] and [[pointed sets]] are different. 

In a [[dependent type theory]] with [[identity types]] and a hierarchy of [[type universes]] a la Tarski, given a universe $(\mathcal{U},\mathcal{T}_{\mathcal{U}})$ a subtype of a type $A:\mathcal{U}$ is a function $B:\mathcal{T}_{\mathcal{U}}(A) \to \mathrm{Prop}_\mathcal{U}$. 

## See also ##

* [[dependent type theory]]

* [[n-monomorphism]]

* [[coercion]]

[[!redirects subtypes]]
[[!redirects subtyping]]
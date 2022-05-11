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

In a [[dependent type theory]] with [[identity types]], a subtype of a [[type]] $A$ is a type $B$ with a [[n-monomorphism|1-monic function]] $f:B \to A$. 

In a [[dependent type theory]] with [[identity types]] and a hierarchy of [[type universes]] a la Tarski, given a universe $(\mathcal{U},\mathcal{T}_{\mathcal{U}})$ a subtype of a type $A:\mathcal{U}$ is a function $B:\mathcal{T}_{\mathcal{U}}(A) \to \mathrm{Prop}_\mathcal{U}$. 

## See also ##

* [[dependent type theory]]

* [[n-monomorphism]]

* [[coercion]]

[[!redirects subtypes]]
[[!redirects subtyping]]
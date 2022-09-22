+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]

=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

There are two ways to show that two objects of a [[presetoid]] are identified with each other: by way of the [[identity type]], and by way of the type of [[isomorphisms]] in the [[core]] [[pregroupoid]] of a presetoid. Univalent setoids are precisely the presetoids which the two notions of identifying objects with each other coincide. 

## Definition

For each object $a:Ob(A)$ and $b:Ob(A)$ of a presetoid $A$, there is a function 
$$\mathrm{idtoiso}(a, b):(a =_A b) \to (a \cong_A b)$$
from the [[identity type]] to the type of isomorphisms in the [[core]] [[pregroupoid]] $\mathrm{Core}(A)$ of $A$. A presetoid is a **univalent setoid** or a **saturated setoid** if for each object $a:Ob(A)$ and $b:Ob(A)$ the function 
$$\mathrm{idtoiso}(a, b):(a =_A b) \simeq (a \cong_A b)$$
is an equivalence of types. 

Since every type of morphisms in the core of the presetoid is a [[h-set]], this means that every univalent setoid is a [[h-groupoid]]. 

## Examples 

* Every thin univalent setoid is a [[set]] (i.e. an [[h-set]]). 
* [[univalent dagger categories]]
* [[h-groupoids]] (i.e. univalent groupoids)

## See also 

* [[setoid]]
* [[presetoid]]
* [[quotient set]]
* [[structure identity principle]]

[[!redirects univalent setoids]]
[[!redirects saturated setoid]]
[[!redirects saturated setoids]]

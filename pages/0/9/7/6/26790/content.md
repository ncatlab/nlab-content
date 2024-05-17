
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

In [[dependent type theory]], a **record type** is a type which consists of variadic [[tuples]] called *records*, whose individual elements in the tuples are called *fields*. 

Finitary record types can be defined in terms of the [[unit type]] and iterated [[dependent sum types]]. Examples of finitary record types include [[unit types]], [[negative copies]], [[product types]], [[dependent sum types]], etc...

Infinitary record types have an infinite number of fields and require something like [[two-level type theory]] to be implemented. An example of an infinitary record type is any [[semi-simplicial types in homotopy type theory|semi-simplicial type]]. 

## Related concepts

* [[dependent sum type]]

## Implementations

Most type-theory based proof assistants include primitive record types, with [[dependent sum types]] defined as a particular case of these, rather than requiring general record types to be defined using dependent sum types.  This includes:

* [[Coq]]
* [[Agda]]
* [[Lean]]
* [[Narya]]

[[!redirects record type]]
[[!redirects record types]]

[[!redirects record]]
[[!redirects records]]

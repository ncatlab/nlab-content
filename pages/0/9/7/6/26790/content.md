
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

## References

A proof assistant which makes use of record types:

* [Narya](https://github.com/mikeshulman/narya)

[[!redirects record type]]
[[!redirects record types]]

[[!redirects record]]
[[!redirects records]]

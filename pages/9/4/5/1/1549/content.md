
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

A class $I$ of [[object]]s in a [[cartesian closed category]] $C$ is called an **exponential ideal** if whenever $Y\in I$ and $X\in C$, the [[exponential object]] $Y^X$ is in $I$.  

## Properties

+-- {: .num_theorem}
###### Theorem

If $I \hookrightarrow C$ is a [[reflective subcategory]], then it is an exponential ideal if and only if its [[reflector]] $C\to I$ preserves [[finite products]].

=--

This appears for instance as ([Johnstone, A4.3.1](#Johnstone)). See also at _[[reflective subuniverse]]_.  Note that in this case $I$ is itself a [[cartesian closed category]], since being a reflective subcategory it is also closed under finite products.


## References

The relation of exponential ideals to [[reflective subcategories]] is discussed in section A4.3.1 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
  {#Johnstone}

[[!redirects exponential ideals]]
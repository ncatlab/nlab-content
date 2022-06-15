
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The term **homotopy level** (or **h-level**), originating in [[homotopy type theory]], is another name for the notion of [[truncated object|truncation]] (particularly in [[(∞,1)-categories]] and their 
[[internal logic|internal language]] of [[homotopy type theory]]) in which the numbering is offset by 2:

a [[homotopy n-type]] is a [[type]] of homotopy level $n+2$.  

This offset in counting enables it to "start" at 0 rather than (-2), which is convenient when defining it by induction over the natural numbers in type theory.  Thus, the correspondence between the various terminologies is indicated in the following table:

[[!include homotopy n-types - table]]

## Definition ##

A [[type]] $A$ has a __homotopy level__ or __h-level__ of $n$ if the type $hasHLevel(n, A)$ is inhabited, for [[natural numbers|natural number]] $n:\mathbb{N}$.  $hasHLevel(n, A)$ is inductively defined as

$$hasHLevel(0, A) \coloneqq isContr(A)$$
$$hasHLevel(s(n), A) \coloneqq \prod_{a:A} \prod_{b:A} hasHLevel(n, a =_A b)$$

## Examples ##

* Every [[proposition]] has a homotopy level of $1$. 

* Every [[set]] has a homotopy level of $2$. 

## Referencees ##

* Ayberk Tosun, Formal Topology in Univalent Foundations, ([pdf](https://odr.chalmers.se/handle/20.500.12380/301098))

[[!redirects homotopy level]]
[[!redirects homotopy levels]]
[[!redirects h-level]]
[[!redirects h-levels]]

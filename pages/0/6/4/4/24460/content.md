+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[rewriting system]] is terminating if we cannot perform a never-ending computation.

## Definition

Let $(X,\rightarrow)$ be an [[abstract rewriting system]]. Then $\rightarrow$ is terminating, strongly normalizing or noetherian iff there doesn't exist any infinite reduction $x_{1} \rightarrow x_{2} \rightarrow ... \rightarrow x_{n} \rightarrow ... $

## Example 

The cut elimination of [[second order linear logic]] is strongly normalizable, see [Pagani & Tortora de Falco (2009)](#PaganiTortora09) where they prove it using notably Girard's [[reducibility candidates]].

## Related entries

* It is possible that only one term is strongly normalizable but not the entire rewriting system: see [[normal form]].

* [[abstract rewriting system]]

* [[rewriting system]]



## References

On [[strong normalization]] of second order linear logic:

* {#PaganiTortora09} [[Michele Pagani]], [[Lorenzo Tortora de Falco]], *Strong Normalization Property for Second Order Linear Logic* (2009) &lbrack;[pdf](https://www.irif.fr/~michele/snllTCS-1.pdf)&rbrack;


[[!redirects strongly normalizing]]
[[!redirects strong normalization]]
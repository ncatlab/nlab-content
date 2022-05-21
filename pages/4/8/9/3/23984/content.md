
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

In [[Martin-Löf type theory]], given a type $A$, a judgment $z:A \vdash B(z)\ \mathrm{type}$, terms $x:A$ and $y:A$, and an identity $p:(x =_A y)$, there are **transport functions** $\overrightarrow{\mathrm{tr}}_{B}^{p}:B(x) \to B(y)$ and $\overleftarrow{\mathrm{tr}}_{B}^{p}:B(y) \to B(x)$, such that for all $v:B(y)$, the [[fiber]] of $\overrightarrow{\mathrm{tr}}_{B}^{p}$ at $v$ is [[contractible]], and for all $u:B(x)$, the [[fiber]] of $\overleftarrow{\mathrm{tr}}_{B}^{p}$ at $u$ is [[contractible]]. 

## See also ##

* [[identity type]]
* [[dependent identity type]]

## References ##

* [[Univalent Foundations Project]], [[Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects transports]]
[[!redirects transporting]]
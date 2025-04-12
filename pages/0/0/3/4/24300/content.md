+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
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

In [[homotopy type theory]], given a [[type universe]] $\mathcal{U}$, a [[type]] $A$ is **locally $\mathcal{U}$-small** if for all terms $a:A$ and $b:A$, the identity type $a =_A b$ is [[essentially small type|essentially $\mathcal{U}$-small]]. 

More generally, given a type $A$ and a type family $x:A \vdash B(x)$, a type $C$ is **locally $(A, B)$-small** if for all terms $a:C$ and $b:C$ the identity type $a =_C b$ is [[essentially small type|essentially $(A, B)$-small]]. 

## See also ##

* [[type universe]]
* [[essentially small type]]
* [[type theoretic axiom of replacement]]
* [[locally finite type]]

## References ##


* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]]: Section 2.19 of: *[[Symmetry]]* (2021) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$

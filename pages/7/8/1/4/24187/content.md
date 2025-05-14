+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
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

_Sphere types_ are the [[axiom|axiomatization]] of the [[homotopy type]] of the ([[shape modality|shape]] of) the [[spheres]] in the context of [[homotopy type theory]].

## Definition
 {#Definition}

For $n = 0$, the *[[0-sphere]]*-type is defined to the [[type of booleans]] $\mathbf{2}$:

\[
  \label{ZeroSphereType}
  S^0 
   \,\coloneqq\, 
  \mathbf{2}
  \,.
\]

By [[induction]] on the [[natural number]] $n$: For $n \geq 1$, the *$n$-sphere type* is be defined as 

* the (un-reduced) [[suspension type]] $\mathrm{S}(-)$ of the $(n-1)$-sphere type $S^{n-1}$;

or equivalently

* the $n$-fold iterated [[suspension type]] $\mathrm{S}^n(-)$ of $S^0$ (eq:ZeroSphereType):

$$
  S^n 
   \;\coloneqq\; 
  \mathrm{S} S^{n-1}
    \;=\;
  \mathrm{S}^n S^0
  \,.
$$

## See also

* [[circle type]]

* [[synthetic homotopy theory]]

* [[homotopy groups of spheres]]

## References

* [[Univalent Foundations Project]], §6.4 & §6.5 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;




[[!redirects sphere types]]

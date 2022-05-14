
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

The notion of a *partially ordered object* is the generalization of that of *[[partially ordered sets]]* as one passes from the ambient [[category of sets]] [[internalization|into]] more general ambient  [[categories]] with suitable properties.

## Definitions

In a [[finitely complete category]] $C$, a **partially ordered object** is a [[preordered object]] $(X, R, s, t, \rho, \tau_p)$ with a [[monomorphism]] $\alpha:R \times_X R^\op \hookrightarrow X \times X$ which [[factors]] through the [[diagonal]] $\alpha = \Delta_X \circ \alpha^{'}$, where $\alpha^{'}:R \times_X R^\op \hookrightarrow X$. 

## See also

* [[preordered object]]

* [[partially ordered set]]

* [[opposite internal relation]]

* [[meet-semilattice object]]

* [[join-semilattice object]]

[[!redirects partially ordered objects]]
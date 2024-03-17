
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[Riemannian geometry|Riemann]]-[[Cartan geometry|Cartan]] [[differential geometry]], what are called Cartan's *structural equations* (*équations de structure* [Cartan 1923, p. 368](#Cartan1923), see [Scholz 2019, p. 53](#Scholz19)) are expressions for the [[torsion]] $T$ and the [[curvature]] $R$ of a [[Cartan moving frame]] $e$ with ([[Cartan connection|Cartan]]-)[[connection on a vector bundle|connection]] $\omega$ via the [[exterior derivative]] and [[wedge product]] of their [[differential form]]-representatives (shown as usual in components on any local [[chart]] with respect to a [[trivial fiber bundle|trivialized]] [[fiber bundles]]  and using [[Einstein summation convention]]):

\[
  \label{TheStructuralEquations}
  \begin{array}{ccccc}
    T^a 
    &=& \mathrm{d}e^a &+& \omega^a{}_b \wedge e^b
    \,,
    \\
    R^{ab} &=& \mathrm{d} \omega^{a b} &+& \omega^{a}{}_c \wedge \omega^{c b}
    \,.
  \end{array}
\]

In the historically motivating case relating to the description of the [[field (physics)|field]] of [[gravity]] in what is now called [[first-order formulation of gravity|first-order formulation]], the representatives of the [[frame field]] and [[connection on a bundle|connection]]

$$
  \begin{array}{rcl}
    \big(e^a\big)_{a = 0}^{d}
    &\in&
    \Omega^1_{dR}\big(-; \mathbb{R}^{1+d}\big)
    \,,
    \\
    \big(
      \omega^{a b} \,=\, -\omega^{b a}
    \big)_{a,b \in 0}^d
    &\in& 
   \Omega^1_{dR}\big(-; \mathfrak{so}(1,d)\big)
  \end{array}
$$

are [[differential 1-forms]] which may jointly be understood as taking [[Lie algebra valued differential form|values]] in the [[Poincaré Lie algebra]] of a given dimension, and the two structural equations (eq:TheStructuralEquations) jointly express the total [[curvature 2-form]] of this connection, broken up into its components.

## Related concepts

* [[Bianchi identities]]


## References

[[!include Cartan structural equations and Bianchi identities -- references]]





[[!redirects Cartan's structural equations]]

[[!redirects Cartan structural relations]]
[[!redirects Cartan structural relation]]



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

## Idea

In [[type theory]], **term elimination** are the [[natural deduction]] rules for how to use [[terms]] of a given [[type]]. 

For example, the term elimination rules for the [[sum type]] are as follows:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B}{\Gamma \vdash \mathrm{ind}_{A + B}(z.C, x.c, y.d, e):C[e/z]}$$

## Contextual term elimination

Similar to the [[conversion rules]] for types, there are also **contextual term elimination** rules for types. These differ from the usual term elimination rules in that in that there is an additional context member $\Delta$ attached to the end of the context $\Gamma, x:A$ so that the full context becomes $\Gamma, x:A, \Delta$. By definition, $\Delta$ is dependent upon $x:A$, and the conclusion usually involves substituting $x:A$ by some given term $a:A$ in the context, becoming $\Gamma, \Delta[a/x]$. For example, the contextual term elimination rules for the [[sum type]] are given by:

$$\frac{\Gamma, z:A + B, \Delta \vdash C \; \mathrm{type} \quad \Gamma, x:A, \Delta[\mathrm{inl}(x)/z] \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B, \Delta[\mathrm{inr}(y)/z] \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B}{\Gamma, \Delta[e/z] \vdash \mathrm{ind}_{A + B}(z.C, x.c, y.d, e):C[e/z]}$$

And in [[first order logic]] over [[type theory]], the contextual term elimination rules for the sum types are given by:

$$\frac{\Gamma, z:A + B, \Delta \vert \Phi \vdash C \; \mathrm{type} \quad \Gamma, x:A, \Delta[\mathrm{inl}(x)/z] \vert \Phi[\mathrm{inl}(x)/z] \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B, \Delta[\mathrm{inr}(y)/z] \vert \Phi[\mathrm{inr}(y)/z] \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B}{\Gamma, \Delta[e/z] \vert \Phi[e/z] \vdash \mathrm{ind}_{A + B}(z.C, x.c, y.d, e):C[e/z]}$$

## See also

* [[formation rule]], [[introduction rule]], [[conversion rule]]
* [[beta-conversion]], [[eta-conversion]]
* [[definition rule]]
* [[equality]]

## References

Contextual [[dependent product types]] and contextual [[identity types]] are defined in the appendix of:

* [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

where the term elimination rules are contextual term elimination rules. 

[[!redirects term elimination]]
[[!redirects term elimination rule]]
[[!redirects term elimination rules]]
[[!redirects elimination rule]]
[[!redirects elimination rules]]

[[!redirects contextual term elimination]]
[[!redirects contextual term elimination rule]]
[[!redirects contextual term elimination rules]]
[[!redirects contextual elimination rule]]
[[!redirects contextual elimination rules]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Subformula property
* table of contents
{: toc}

## Idea

The **subformula property** is a property of [[cut elimination|cut-free]] presentations of the [[sequent calculus]]. It says that in any derivation

$$\frac{\vdots}{\Gamma\vdash \Delta}$$

any type appearing above the line is a *subformula* of one of the types appearing in $\Gamma,\Delta$. This makes it easy to make arguments about provability: while it is not obvious that a cut-full system that the contradiction/empty sequent $\cdot\vdash\cdot$ is derivable, it is a corollary of the subformula property that the $\cdot \vdash \cdot$ is *not* derivable because all of the rules of the cut-free calculus involve a type above the line.

This property is a formal expression of the *modularity* of type theoretic connectives: each connective is given by rules which involve only its arguments.
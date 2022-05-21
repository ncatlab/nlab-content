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

## Definition 

### In Martin-Löf type theory

In [[Martin-Löf type theory]], given a [[type]] $A$, a [[type family]] $x:A \vdash B(x)$, [[terms]] $a:A$, $b:A$, and [[identity]] $p:a =_A b$, a **dependent identity type** or a **heterogeneous identity type** is the [[transport]] of the [[identity type]] along the identity $p$:

$$a =_B^p b \coloneqq \mathrm{tr}_B^p(a =_{B(b)} b)$$ 

### In higher observational type theory 

In [[higher observational type theory]], the [[type formation|formation rule]] for the dependent identity types is given by

$$\frac{\varsigma:\delta =_\Delta \delta^{'} \quad \delta \vdash A\ \mathrm{type} \quad a:A[\delta] \quad a^{'}:A[\delta^{'}]}{a =_{\Delta.A}^\varsigma a^{'}\ \mathrm{type}}$$

where $\Delta$ is a [[type telescope]].

... needs to be finished

## Categorical semantics

needs to be written

## See also

[[!include notions of type]]

## References

* [[Mike Shulman]], Towards a Third-Generation HOTT Part 2 ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-05.pdf), [video](https://www.youtube.com/watch?v=5ciDNfmvMdU))

[[!redirects dependent identity types]]
[[!redirects heterogeneous identity type]]
[[!redirects heterogeneous identity types]]
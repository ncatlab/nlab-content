
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **Horn theory** is a [[theory]] in which every [[axiom]] has a certain special form.

## Definition

Let $\Sigma$ be a [[signature (in logic)|signature]]. A **[[term]]** of $\Sigma$ is an expression built out of [[variables]] and [[function symbols]]. (For example, $x y^{-1} z$ is a term in the language of [[groups]].) An **atomic formula** relative to $\Sigma$ is a formula that consists of a [[relation symbol]] of $\Sigma$ (including [[equality]]) applied to terms. 

A **Horn clause** is a logical expression of the form 

$$\phi_1 \wedge \ldots \wedge \phi_n \vdash \phi$$ 

where each $\phi_i$ and $\phi$ is atomic. A (universal) **Horn theory** is a [[theory]] in which every [[axiom]] is a Horn clause. 

## Related concepts

* [[modular lattice]]

* [[lattice-ordered ring]]

## References


* [[Michael Barr]], *Models of Horn theories*, in: *Categories in Computer Science and Logic*, Contemporary Math. **92**, Amer. Math. Soc. (1989) 1–7 &lbrack;[pdf](https://www.math.mcgill.ca/barr/papers/horn.pdf), [[Barr-ModelsOfHornTheories.pdf:file]]&rbrack;

[[!redirects Horn theories]] 

[[!redirects Horn clause]]
[[!redirects Horn clauses]]

[[!redirects Horn logic]]

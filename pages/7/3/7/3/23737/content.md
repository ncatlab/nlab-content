

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

### General

By a *smooth functor* one may generally understand an [[internal functor]] [[internalization|in]] the [[category]] of [[SmoothManifolds]], hence a [[homomorphism]] between [[internal categories]] or [[internal groupoids]] ([[Lie groupoids]]) in [[SmoothManifolds]].

Slightly alternatively, a smooth functor may be understood as an [[enriched functor]] between [[enriched categories]] over [[SmoothManifolds]].

### In global analysis

Much more specifically, "smooth functor" is used by [Kriegl & Michor 97, Sec 29.5](KrieglandMichor1997) to refer to an [[endofunctor]] of [[FinDimVect]], when $FinDimVect$ is viewed as a [[enriched category|category enriched]] in the category of [[smooth manifolds]].

That is, a smooth functor is a functor $F \colon FinDimVect \to FinDimVect$ such that the map $FinDimVect(X,Y) \to FinDimVect(F(X),F(Y))$ is smooth for every $X$, $Y$.

Currently, the remainder of this entry focuses on this specific notion.

## Examples

The iterated tensor product $X \mapsto X^{\otimes n}$ is a smooth functor.

The iterated wedge product $X \mapsto \bigwedge_{i=1}^n X$ is a smooth functor

## Extensions

The concept of smooth functor can be extended to multivariate functors $FinDimVect^n \to FinDimVect$, and also to [[contravariant functors]] $FinDimVect^{op} \to FinDimVect$, such as the dual $V \mapsto V^*$.

## Related concepts

* [[linear functor]]

## References

* {#KrieglandMichor1997} [[Andreas Kriegl]], [[Peter Michor]], *[[The Convenient Setting of Global Analysis]]*, Mathematical Surveys and Monographs **53**, American Mathematical Society (1997) &lbrack;ISBN: 978-0-8218-0780-4, [ams:surv-53](https://bookstore.ams.org/surv-53), [pdf](https://www.mat.univie.ac.at/~michor/apbookh-ams.pdf)&rbrack;



[[!redirects smooth functors]]



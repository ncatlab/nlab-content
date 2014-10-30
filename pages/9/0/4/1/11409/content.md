


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **compactness theorem** is a fundamental result of _[[model theory]]_ on the existence of [[models]] of [[first-order theories]].

Historically it goes back to work of [[Gödel]] and Mal'cev in the 1930s.

[[Lindström's theorem]] uses the compactness and the [[Löwenheim-Skolem theorem]] to characterize classical first-order logic. The validity or non-validity of the compactness theorem in logical systems other than first-order logic plays under the name of _compactness property_ an important role in [[abstract model theory]].

## Theorem

A set of first-order formulas $\Phi$ has a model precisely iff every finite subset of $\Phi$ has a model.

## Remark

There are different proofs for the compactness theorem e.g. an entirely 'semantic' one using [[ultraproduct|ultraproducts]]. A particularly transparent one relies on the completeness theorem for first-order logic and the essential finitude of the notion of formal proof[^end]: Suppose $\Phi$ has no model, due to completeness this implies that there is a contradiction $\varphi$ with $\Phi\vdash\varphi$ but such a deduction of $\varphi$ can involve only a finite subset $\Phi_0\subset \Phi$ hence $\Phi_0\vdash\varphi$ and $\Phi_0$ would have no model as well.

[^end]: In the German literature the compactness theorem is therefore also called 'Endlichkeitssatz'.

The motivation for the terminology stems from the observation that the compactness theorem literally expresses the compactness of a suitable topology on first-order structures.

## Related concepts

* [[Löwenheim-Skolem theorem]]

* [[Skolem's paradox]]

* [[Lindström's theorem]]

* [[Deligne completeness theorem]]

* [[Stone duality]]

## References

* Wikipedia, _[compactness theorem](https://en.wikipedia.org/wiki/Compactness_theorem)_



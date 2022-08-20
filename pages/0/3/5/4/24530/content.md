#Contents#
* table of contents
{:toc}

## Idea 

A [[monoidal monad]] on a [[cartesian monoidal category]] is _affine_ or _semicartesian_ when its [[Eilenberg-Moore category|category of algebras]] is a [[semicartesian monoidal category]], that is, a model of [[affine logic]].

## Definition

Let $T$ be a monoidal monad on a cartesian monoidal category. Then $T$ is affine if any of the following hold

1. The unit of the monad $\eta_1 : 1 \to T1$ is an [[isomorphism]].
2. The morphism $(T\pi, T\pi) \circ \alpha : T X \times T Y \to T X \times T Y$ is the identity, where $\alpha : T X \times T Y \to T (X \times Y)$ is the natural transformation from the [[monoidal monad]] structure.

This should be generalizable to monads on [[cartesian multicategories]].

## References

* [[Anders Kock]], _Bilinearity and Cartesian Closed Monads_, Mathematica Scandinavia, 29 (1971): 161-174. <http://eudml.org/doc/166201>.

* {#Jacobs94} B. Jacobs, _Semantics of Weakening and Contraction_, Annals of Pure and Applied Logic, volume 69, Issue 1, (1994) pp.73-106, doi:[10.1016/0168-0072(94)90020-5](https://doi.org/10.1016/0168-0072%2894%2990020-5)

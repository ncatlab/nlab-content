
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[functor]] is an **amnestic isofibration** if it is an [[amnestic functor]] and an [[isofibration]]. The combination of these properties admits a particularly simply description in terms of a [[lifting property]].

\begin{proposition}
  A functor $U : \mathcal{D} \to \mathcal{C}$ is an amnestic isofibration if and only if, for any object $D$ in $\mathcal{D}$ and any isomorphism $f : C \to U D$ in $\mathcal{C}$, there is a _unique_ isomorphism $\tilde{f} : \tilde{C} \to D$ such that $U \tilde{f} = f$.
\end{proposition}
\begin{proof}
 Indeed, if $\tilde{f}' : \tilde{C}' \to D$ were any other isomorphism such that $U \tilde{f}' = f$, then $U (\tilde{f}^{-1} \circ \tilde{f}') = id_C$, so we must have $\tilde{f} = \tilde{f}'$.
\end{proof}

Amnestic isofibrations are occasionally called **discrete isofibrations**, but this term may be misleading, because they are not [[isofibrations]] with discrete fibres.

## Properties

\begin{proposition}
A [[monadic functor]] is *strictly monadic* if and only if it is also an [[amnestic  isofibration]].
\end{proposition}
\begin{proof}
Clearly, a strictly monadic functor is an amnestic isofibration; and if a monadic functor $U$ is amnestic, then the [[comparison functor]] $K$ is also [[amnestic functor|amnestic]], and if $U$ is a monadic isofibration, so is $K$; therefore in this case $K$ must be an isomorphism of categories. 
\end{proof}

## Examples

* If $F : A \to B$ is a [[bijective on objects functor]], then $[F, C] : [B, C] \to [A, C]$ is an amnestic isofibration (Lemma 2.4.8 of [Avery 2017](#Avery17)).

## Related concepts

* [[amnestic functor]]
* [[isofibration]]
* [[conservative functor]]
* [[monadic functor]]

## References

A reference using the term *amnestic isofibrations*:

* {#Avery17} [[Tom Avery]]: _Structure and Semantics_ &lbrack;[arXiv:1708.01050](https://arxiv.org/abs/1708.01050)&rbrack;

A reference using the term *discrete isofibrations*:

* {#Lack09} [[Steve Lack]]: _A 2-categories companion_, in [[John Baez]], [[Peter May]]: _[[Towards Higher Categories]]_, Springer, (2009) &lbrack;[arXiv:math/0702535](http://arxiv.org/abs/math/0702535)&rbrack;

[[!redirects amnestic isofibrations]]
[[!redirects discrete isofibration]]
[[!redirects discrete isofibrations]]

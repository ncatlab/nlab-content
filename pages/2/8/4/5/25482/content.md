
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $L \dashv R$ be a pair of [[adjoint functors]] (an [[adjunction]] in [[Cat]]).
\begin{tikzcd}
	C & D
	\arrow[""{name=0, anchor=center, inner sep=0}, "L", bend left, from=1-1, to=1-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "R", bend left, from=1-2, to=1-1]
	\arrow["\dashv"{anchor=center, rotate=-90}, draw=none, from=0, to=1]
\end{tikzcd}

The **envelope** of the adjunction, denoted $Env(L \dashv R)$, is the [[category]] whose [[objects]] are [[quadruples]]

$$
(c \in C, d \in D, f : L c \to d, g \colon c \to R d)
$$

such that $f$ and $g$ are each other's [[mate]], and whose [[morphisms]] are [[pairs]]

$$
(p \colon c \to c', q \colon d \to d')
$$

such that $(R q) \circ g = g' \circ p$ or equivalently $q \circ f = f' \circ (L p)$.

## Properties

* {#EnvelopeOfAdjunctionCOmmaCategory} A [[functor]] $L \colon C \to D$ is [[left adjoint]] to a functor $R \colon D \to C$ if and only if there is an isomorphism of [[comma categories]] $L \downarrow D \cong C \downarrow R$ and this isomorphism commutes with the [[forgetful functors]] to the [[product category]] $C \times D$ (see [there](adjoint+functor#InTermsOfCommaCategories)). In this case, the envelope $Env(L \dashv R)$ is also isomorphic to these comma categories over the evident [[forgetful functor]] to $C \times D$.

* Every adjunction factors through its envelope via a [[reflection|reflective subcategory]] and a [[coreflection|coreflective subcategory]].
\begin{tikzcd}
	C & {\mathrm{Env}(L \dashv R)} & D
	\arrow[""{name=0, anchor=center, inner sep=0}, "{\mathrm{cod}}", shift left=3, from=1-2, to=1-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, shift left=3, hook, from=1-3, to=1-2]
	\arrow[""{name=2, anchor=center, inner sep=0}, shift left=3, hook, from=1-1, to=1-2]
	\arrow[""{name=3, anchor=center, inner sep=0}, "{\mathrm{dom}}", shift left=2, from=1-2, to=1-1]
	\arrow["\dashv"{anchor=center, rotate=-90}, draw=none, from=0, to=1]
	\arrow["\dashv"{anchor=center, rotate=-90}, draw=none, from=2, to=3]
\end{tikzcd}
See Lemma 4.1 of [Pavlovic and Hughes](#PavlovicHughes).

* Denoting by $Inv(F \dashv G)$ the [[fixed point of an adjunction|fixed point]] of $F \dashv G$, the following square of [[fully faithful]] functors forms a [[2-pullback]] in [[Cat]].
\begin{tikzcd}
	{Inv(F \dashv G)} & C \\
	D & {Env(F \dashv G)}
	\arrow[hook, from=1-1, to=1-2]
	\arrow[hook, from=1-1, to=2-1]
	\arrow[hook, from=1-2, to=2-2]
	\arrow[hook, from=2-1, to=2-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=1-1, to=2-2]
\end{tikzcd}
In particular, $Inv(F \dashv G)$ is the full subcategory of $Env(F \dashv G)$ whose objects $(c, d, f, g)$ have $f$ and $g$ isomorphisms.
(See Lemma 12.1 of [Avery and Leinster](#AveryLeinster).)

* The envelope construction (respectively the [[fixed point of an adjunction|fixed point]] construction) can be seen as [[2-adjunctions]] between [[Cat]], and the 2-category of adjunctions (respectively the [[wide subcategory|wide]] sub-2-category of adjunctions whose morphisms $(P, Q, \alpha, \beta)$ have $\alpha$ and $\beta$ invertible)).
\begin{tikzcd}
	& {\mathrm{ADJ}} \\
	{\mathrm{CAT}} \\
	& {\mathrm{ADJ}_{\cong}}
	\arrow[""{name=0, anchor=center, inner sep=0}, shift left=3, hook, from=2-1, to=3-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, shift left=3, hook, from=2-1, to=1-2]
	\arrow[hook, from=3-2, to=1-2]
	\arrow[""{name=2, anchor=center, inner sep=0}, "{\mathrm{Env}}", shift left=3, from=1-2, to=2-1]
	\arrow[""{name=3, anchor=center, inner sep=0}, "{\mathrm{Inv}}", shift left=3, from=3-2, to=2-1]
	\arrow["\dashv"{anchor=center, rotate=-48}, draw=none, from=1, to=2]
	\arrow["\dashv"{anchor=center, rotate=-132}, draw=none, from=0, to=3]
\end{tikzcd}
(See Remark 12.2 of [Avery and Leinster](#AveryLeinster).)

## Examples

* The envelope of the [[Isbell duality]] adjunction associated to a category $A$ is the [[Isbell envelope]] of $A$ (called the _category of gaps_ in $A$ by [Pavlovic and Hughes](#PavlovicHughes)).

* The envelope of the [[nuclear adjunction]] associated to the [[Isbell duality]] adjunction for a small category $A$ is what [Pavlovic and Hughes](#PavlovicHughes) call the _category of intervals_ in $A$.

## Related concepts

* [[fixed point of an adjunction]]

## References

* {#AveryLeinster} [[Tom Avery]], [[Tom Leinster]]. _Isbell conjugacy and the reflexive completion_. Theory and Applications of Categories, **36** 12 (2021) 306-347 &lbrack;[tac:36-12](http://www.tac.mta.ca/tac/volumes/36/12/36-12abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/36/12/36-12.pdf)&rbrack;

* {#PavlovicHughes} [[Dusko Pavlovic]], and Dominic JD Hughes. _Tight limits and completions from Dedekind-MacNeille to Lambek-Isbell_. ([arXiv](https://arxiv.org/abs/2204.09285))

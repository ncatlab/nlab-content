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

The **Ehrenfeucht-Fra&#239;ss&#233; comonad** is a [[comonad]] introduced by [[Samson Abramsky]] and [[Nihil Shah]] in [Abramsky-Shah 2018](#AbramskyShah), to study [[Ehrenfeucht-Fraïssé games]].

If $\mathcal{R}(\sigma)$ denotes the set of $\sigma$-structures, for $\sigma$ a relational signature, there is a comonad $\mathbb{E}_k$ on $\mathcal{R}(\sigma)$, where

- The elements of $\mathbb{E}_k\mathcal{A}$ are finite nonempty sequences in $\mathcal{A}$
- CoKleisli morphisms $\mathbb{E}_k \mathcal{A} \to \mathcal{B}$ correspond to winning strateges for duplicator in the **existential** Ehrenfeucht-Fraïssé game of length $k$, played from $\mathcal{A}$ to $\mathcal{B}$, i.e the one where spoiler only plays in $\mathcal{A}$, duplicator only plays in $\mathcal{B}$, and the two substructures are only required to satisfy the same formulas from the positive existential fragment. The correspondence between strategies and coKleisli morphisms is that, given a sequence of choices by Spoiler $a_1, \dots a_n \in \mathcal{A}$, $f(a_1, \dots a_n) \in \mathcal{B}$ is the choice by Duplicator (supposed to correspond to $a_n$.

There are also a description of the "proper" Ehrenfeucht-Fraïssé game in terms of this comonad, see [Abramsky-Shah 2018](#AbramskyShah) for more details.

## Definition

Let $\mathcal{R}(\sigma)$ be as above.

- The underlying set of $\mathbb{E}_k(\mathcal{A})$, given a $\sigma$-structure $\mathcal{A}$, is, as noted above, the set of nonempty sequences $a_1, \dots a_n$ with $n \leq k$.
- The action on functions is defined in the obvious way, $\mathbb{E}_k(f)(a_1, \dots a_n) = (f(a_1), \dots f(a_n))$.
- The counit is defined by $\epsilon(a_1, \dots a_n) = a_n$
- Given a relation symbol $R \in \sigma$, $R(s_1, \dots s_m)$ if and only if
  - For each $i,j$, either $s_i$ is a prefix of $s_j$ and vice versa
  - And $R(\epsilon(s_1), \dots, \epsilon(s_m))$.
- The comultiplication $\delta: \mathbb{E}_k(\mathcal{A}) \to \mathbb{E}_k\mathbb{E}_k\mathcal{A}$ is given by $\delta(a_1, \dots a_n) = ((a_1), (a_1,a_2), \dots (a_1, \dots a_n))$, i.e by taking the sequence of prefixes of the sequence.

## References

* {#AbramskyShah} [[Samson Abramsky]] and [[Nihil Shah]],
_Relating Structure and Power: Comonadic Semantics for Computational Resources_ ([arXiv:1806.09031](https://arxiv.org/abs/1806.09031))


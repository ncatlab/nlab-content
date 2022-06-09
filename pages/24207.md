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

## Idea

The _smash product type_ is an [[axiom|axiomatization]] of the [[smash product]] in the context of [[homotopy type theory]].

## Definition

The smash product type of two [[pointed type|pointed types]] $A,B$ can be defined as the [[pushout type]] of the span

$$\mathbf 1 \leftarrow A \wedge B \rightarrow A \times B$$

where $A \wedge B \rightarrow A \times B$ is the inclusion of the [[wedge sum type]] in the [[product type]] both of which are pointed. The resulting pushout is denoted the smash product $A \wedge B$ and is pointed by $\star_{A \wedge B}\equiv\mathrm{inl}(\star_{\mathbf 1})$

It can also be defined as the pushout type of the span

$$\mathbf{2} \leftarrow A + B \rightarrow A \times B$$

## See also

* [[higher inductive type]]

* [[smash product]]

## References ##

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Floris van Doorn]] (2018), _On the Formalization of Higher Inductive Types and Synthetic Homotopy Theory_, ([arXiv:1808.10690](https://arxiv.org/abs/1808.10690), [web](http://florisvandoorn.com/papers/dissertation.pdf))

* [[Kuen-Bang Hou]], *Higher-Dimensional Types in the Mechanization of Homotopy Theory*, Ph. D. Thesis 2017 ([web](https://favonia.org/files/thesis.pdf))
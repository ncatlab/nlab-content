[[!redirects select monad]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
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

In a [[cartesian closed category]], given an [[object]] $S$, the _selection monad_, also known as the _select monad_, is the [[endofunctor]] $J_S(X) \mapsto [[X, S], X]$. It is a [[strong monad]].

There is a monad [[homomorphism]] from the selection monad to the [[continuation monad]] for $S$, $K_S(X) = (X \to S) \to S$, which sends $\epsilon \in J_S(X)$ to $\bar{\epsilon} \in K_S(X)$, where $\bar{\epsilon}(p) = p(\epsilon(p))$.

If we understand the continuation monad as mapping an object to the generalized [[quantifiers]] over it, with $S$ a generalized [[truth value]], a selection function for a generalized quantifier is an element of its [[preimage]] under the monad morphism. 

For instance, a selection functional for the [[supremum]] functional $sup: (X \to S) \to X$, when it exists, gives a point at which a function attains its maximum value.

Due to the resemblance of an [[algebra over a monad|algebra]], $J_S(A) \to A$, to [[Peirce's law]] in logic, $((p \Rightarrow q) \Rightarrow p) \Rightarrow p $, $J_S$ is also called the _Peirce monad_ in ([Escardó-Oliva 2012](#Escardó-Oliva2012)).

## Properties

There is a [[distributive law]] $T J_S \Rightarrow J_S T$ for every strong monad $T$ ([Fiore 2019](#Fiore2019)).

## References

* [[Martín Escardó]] and Paulo Oliva, _Selection Functions, Bar Recursion, and Backward Induction_, Mathematical Structures in Computer Science, 20(2):127–168, 2010, ([pdf](https://www.cs.bham.ac.uk/~mhe/papers/selection-escardo-oliva.pdf))

* [[Martín Escardó]] and Paulo Oliva, _What Sequential Games, the Tychonoff Theorem and the Double-Negation Shift have in Common_, ([pdf](https://www.cs.bham.ac.uk/~mhe/papers/msfp2010/Escardo-Oliva-MSFP2010.pdf))

*  {#Escardó-Oliva2012} [[Martín Escardó]] and Paulo Oliva, _The Peirce translation_, Annals of Pure and Applied Logic, 163(6):681–692, 2012, ([pdf](https://www.cs.bham.ac.uk/~mhe/papers/peirce.pdf)).

* [[Jules Hedges]], _The selection monad as a CPS transformation_, ([arXiv:1503.06061](https://arxiv.org/abs/1503.06061))

* Martin Abadi, [[Gordon Plotkin]], _Smart Choices and the Selection Monad_, ([arXiv:2007.08926](https://arxiv.org/abs/2007.08926))

* Marcelo Fiore, _Fast-growing clones_, ([Talk at CT 2019](http://conferences.inf.ed.ac.uk/ct2019/slides/fiore.pdf))
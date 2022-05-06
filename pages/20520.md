#Contents#
* table of contents
{:toc}

## Idea

By analogy with [[graded algebra]], a **$\mathcal{M}$-graded monad** in a category $\mathbb{C}$ for a [[monoidal category]], $(\mathcal{M}, \otimes, I)$, is a [[lax monoidal functor]], $(\mathcal{M}, \otimes, I) \to ([\mathbb{C}, \mathbb{C}], \circ, id_{\mathbb{C}})$. This generalizes the concept of [[monad]] which may be consider as graded by $\mathbf{1}$, the [[terminal category]].

Equivalently, a $\mathcal{M}$-graded monad is a lax [[2-functor]] from the [delooping](https://ncatlab.org/nlab/show/delooping#deloopings_of_higher_categorical_structures) (or "suspension") of $\mathcal{M}$, $\mathbf{B} \mathcal{M} \to Cat$. Just as [[monads]] may be defined in any 2-category, $K$, so we may generalize graded monads to lax 2-functors $\mathbf{B} \mathcal{M} \to K$.

Graded monads are also known as **parametric** monads.
 

## Related concepts

* [[graded modality]]
* [[monad]]

## References 

* Soichiro Fujii, Shin-ya Katsumata, and [[Paul-André Melliès]], _Towards a Formal Theory of Graded Monads_, ([pdf](https://www.irif.fr/~mellies/papers/fossacs2016-final-paper.pdf))

* Soichiro Fujii, _A 2-Categorical Study of Graded and Indexed Monads_, ([arXiv:1904.08083](https://arxiv.org/abs/1904.08083))

* Ulrich Dorsch, Stefan Milius and Lutz Schröder, _Graded Monads and Graded Logics for the Linear Time – Branching Time Spectrum_, ([arXiv:1812.01317](https://arxiv.org/abs/1812.01317))
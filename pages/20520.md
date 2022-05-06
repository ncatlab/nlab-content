#Contents#
* table of contents
{:toc}

## Idea

By analogy with [[graded algebra]], a **$\mathcal{M}$-graded monad** in a category $\mathcal{C}$ for a [[monoidal category]], $(\mathcal{M}, \otimes, I)$, is a [[lax monoidal functor]], $(\mathcal{M}, \otimes, I) \to ([\mathcal{C}, \mathcal{C}], \circ, id_{\mathcal{C}})$. This generalizes the concept of [[monad]] which may be consider as graded by $\mathbf{1}$, the [[terminal category]]. This definition may be rephrased in terms of a lax action of $\mathcal{M}$ on $\mathcal{C}$.

Equivalently, a $\mathcal{M}$-graded monad is a lax [[2-functor]] from the [delooping](https://ncatlab.org/nlab/show/delooping#deloopings_of_higher_categorical_structures) (or "suspension") of $\mathcal{M}$, $\mathbf{B} \mathcal{M} \to Cat$. Just as [[monads]] may be defined in any 2-category, $K$, this suggests that we may generalize graded monads to lax 2-functors $\mathbf{B} \mathcal{M} \to K$.

Graded monads are also known as **parametric** monads. The grading idea may also be applied to [[comonads]].

## Examples

1. The grading may arise from a monoid $(M, \otimes, e)$. Then for some given category, $C$, we have a family of endofunctors, $T_m$, indexed by elements of $M$, with maps $\mu_{m, n, X}: T_m(T_n X) \to T_{m \otimes n} X$ and $\eta_{X}: X \to T_{e} X$, for $m, n$ in $M$ and $X$ in $C$. For instance, there is a $(\mathbb{N}_{\gt 0}, \times, 1)$-graded monad on sets where $T_n$ returns lists of length $n$ of elements of a set. 

1. Any [[graded modality]], such as found in [[bounded linear logic]].

1. For graded monads relevant for probability theory see ([Perrone](#Perrone)).

1. Given the strict action of a monoidal category, $\mathcal{M}$ on a category $\mathcal{B}$, and an adjunction

\begin{center}
  \begin{tikzcd}
    \mathcal{A}
     \arrow[r, shift right=6pt, "R"', "\bot"]
    & 
    \mathcal{B},
     \arrow[l, shift right=6pt, "L"']
  \end{tikzcd}
\end{center}
then $\mathcal{A}$ inherits a lax action of $\mathcal{M}$ and is hence a graded monad. Every lax action can be generated from a strict action in this way. Initial and terminal such resolutions of a lax action then generalize the $\mathcal{M} \cong 1$ situation in which is a monad is resolved into adjunctions with the [[Kleisli category|Kleisli]] and [[Eilenberg-Moore category|Eilenberg-Moore]] categories ([FKM 16](#FKM)).

## Related concepts

* [[graded modality]]
* [[monad]]
* [[actegory]]

## References 

* {#FKM} Soichiro Fujii, Shin-ya Katsumata, and [[Paul-André Melliès]], _Towards a Formal Theory of Graded Monads_, ([pdf](https://www.irif.fr/~mellies/papers/fossacs2016-final-paper.pdf))

* Soichiro Fujii, _A 2-Categorical Study of Graded and Indexed Monads_, ([arXiv:1904.08083](https://arxiv.org/abs/1904.08083))

* Ulrich Dorsch, Stefan Milius and Lutz Schröder, _Graded Monads and Graded Logics for the Linear Time – Branching Time Spectrum_, ([arXiv:1812.01317](https://arxiv.org/abs/1812.01317))

* {#Perrone} Paolo Perrone, _Categorical Probability and Stochastic Dominance in Metric Spaces_, ([thesis](https://personal-homepages.mis.mpg.de/perrone/phdthesis.pdf))
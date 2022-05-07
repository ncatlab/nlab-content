#Contents#
* table of contents
{:toc}

## Idea

By analogy with [[graded algebra]], an **$\mathcal{M}$-graded monad** in a category $\mathcal{C}$ for a [[monoidal category]], $(\mathcal{M}, \otimes, I)$, is a [[lax monoidal functor]], $(\mathcal{M}, \otimes, I) \to ([\mathcal{C}, \mathcal{C}], \circ, id_{\mathcal{C}})$. This generalizes the concept of [[monad]], which may be considered as graded by $\mathbf{1}$, the [[terminal category]]. This definition may be rephrased in terms of a lax action of $\mathcal{M}$ on $\mathcal{C}$.

Equivalently, an $\mathcal{M}$-graded monad is a lax [[2-functor]] from the [[delooping#deloopings_of_higher_categorical_structures|delooping]] (or "suspension") of $\mathcal{M}$, $\mathbf{B} \mathcal{M} \to Cat$. Just as [[monads]] may be defined in any 2-category, $K$, this suggests that we may generalize graded monads to lax 2-functors $\mathbf{B} \mathcal{M} \to K$.

A further generalization is to category-valued monads, lax functors from any category to $Cat$ ([OrchWadEad](#OrchWadEad)), and then to 2-category-valued monads from any 2-category.

Graded monads are also known as **parametric** monads. The grading idea may also be applied to [[comonads]].

## Examples

1. The grading may arise from a monoid $(M, \otimes, e)$. Then for some given category, $C$, we have a family of endofunctors, $T_m$, indexed by elements of $M$, with maps $\mu_{m, n, X}: T_m(T_n X) \to T_{m \otimes n} X$ and $\eta_{X}: X \to T_{e} X$, for $m, n$ in $M$ and $X$ in $C$. For instance, there is a $(\mathbb{N}, \times, 1)$-graded monad on sets where $T_n$ returns lists of length $n$ of elements of a set. 

1. In computer science, monads model [[side effects|effects]] and comonads coeffects. Grading can therefore allow further annotation of these. For instance, there are graded versions of the [[reader monad]], [[state monad]] and [[writer comonad]] ([OrchPet](#OrchPet)).

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

## Uses

Graded monads can be used to construct ordinary monads by left Kan extension in the 2-category of [[monoidal category|monoidal categories]], [[lax monoidal functor|lax monoidal functors]], and [[monoidal natural transformation|monoidal transformations]]. There are known criteria for when this Kan extension exists; see ([Fritz & Perrone 18, Theorem 2.1](#FPKan)), as well as the references in there on algebraic Kan extensions.

For example, taking the left Kan extension of the graded list monad $\mathbf{B} \mathbb{N} \to [Set,Set]$ described above results in the usual list monad on $Set$, given by a lax monoidal functor $1 \to [Set,Set]$. Based on a similar construction on the category of complete metric spaces, ([Fritz & Perrone 17](#FPKant)) have contructed a monad of Radon probability measures without any appeal to measure theory; the intuitive idea being that a probability measure can be thought of as an idealized version of a finite sample, and spaces of finite samples make up a graded monad. Forgetting the grading by taking the above Kan extension then produces the _Kantorovich monad_, containing all Radon probability measures of finite first moment. This construction reduces certain problems in measure-theoretic probability to purely combinatorial problems.

A *useful feature* of such constructions is that the multiplication of the graded monad is often a _strong_ monoidal functor in practice. For the graded list monad, this is because a list of length $m n$ can be decomposed uniquely into a list of length $m$ of lists of length $n$, so that the multiplication $T_m T_n X \longrightarrow T_{m n} X$ is an isomorphism. For the probability monad mentioned in the previous paragraph, the analogous phenomenon occurs as well, and this can be exploited e.g. in order to prove a disintegration theorem for finite first moment Radon probability measures on complete metric spaces ([Perrone, Theorem 2.6.9](#Perrone)).

## Related concepts

* [[graded modality]]
* [[monad]]
* [[actegory]]

## References 

* {#FKM} Soichiro Fujii, Shin-ya Katsumata, and [[Paul-André Melliès]], _Towards a Formal Theory of Graded Monads_, ([pdf](https://www.irif.fr/~mellies/papers/fossacs2016-final-paper.pdf))

* Soichiro Fujii, _A 2-Categorical Study of Graded and Indexed Monads_, ([arXiv:1904.08083](https://arxiv.org/abs/1904.08083))

* Ulrich Dorsch, Stefan Milius and Lutz Schröder, _Graded Monads and Graded Logics for the Linear Time – Branching Time Spectrum_, ([arXiv:1812.01317](https://arxiv.org/abs/1812.01317))

* {#Perrone} [[Paolo Perrone]], _Categorical Probability and Stochastic Dominance in Metric Spaces_, ([thesis](http://www.paoloperrone.org/phdthesis.pdf))

* {#FPKan} [[Tobias Fritz]] and Paolo Perrone, _A Criterion for Kan Extensions of Lax Monoidal Functors_, ([arXiv:1809.10481](https://arxiv.org/abs/1809.10481)).

* {#FPKant} [[Tobias Fritz]] and Paolo Perrone, _A Probability Monad as the Colimit of Spaces of Finite Samples_, ([arXiv:1712.05363](https://arxiv.org/abs/1712.05363)).

* {#OrchPet} [[Dominic Orchard]], Tomas Petricek, _Embedding effect systems in Haskell_, ([pdf](https://www.doc.ic.ac.uk/~dorchard/publ/haskell14-effects.pdf))

* {#OrchWadEad} Dominic Orchard, Philip Wadler, Harley Eades, _Unifying graded and parameterised monads_, ([arXiv:2001.10274](https://arxiv.org/abs/2001.10274))
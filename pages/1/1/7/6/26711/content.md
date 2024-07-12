

#Content#
* table of contents
{:toc}

## Idea

$G$-$\infty$-operads are to [[(∞,1)-operads]] as [[equivariant symmetric monoidal category|equivariant symmetric monoidal categories]] are to [[symmetric monoidal categories]]

## Definition

G-$\infty$-operads may be defined as [[algebraic pattern|fibrous patterns]] over the [[Burnside category]] $\mathrm{Span}(\mathbb{F}_G)$.
Explicitly:
\begin{definition}
  A **$G$-$\infty$-operad** is a functor $\pi_{\mathcal{O}}:\mathcal{O}^{\otimes} \rightarrow \mathrm{Span}(\mathbb{F}_G)$ such that

1. $\mathcal{O}^{\otimes}$ has $\pi_{\mathcal{O}}$-cocartesian lifts for backwards maps

2. For every $S \in \mathbb{F}_{\mathcal{T}}$, cocartesian transport along $\pi$-cocartesian lifts lying over the inclusions $(S \leftarrow U = U \mid U \in \mathrm{Orb}(S))$ implement an equivalence
$$
  \mathcal{O}_S \simeq \prod_{U \in \mathrm{Orb}(S)} \mathcal{O}_U,
$$
where $\mathcal{O}_S = \pi^{-1}_{\mathcal{O}}(S)$.

3. For every map of orbits $T \rightarrow S$ and pair of objects $(\mathbf{C},\mathbf{D}) \in \mathcal{O}_T \times \mathcal{O}_S$, writing $\mathbf{D} = (D_U \mid U \in \mathrm{Orb}(S))$, postcomposition with the $\pi$-cartesian lifts yields an equivalence
$$
  \mathrm{Map}_{\mathcal{O}^{\otimes}}^{T \rightarrow S}(\mathbf{C}, \mathbf{D}) \simeq \prod_{U \in \mathrm{Orb}(S)} \mathrm{Map}_{\mathcal{O}^{\otimes}}^{T \leftarrow T_U \rightarrow U}(\mathbf{C}, D_U),
$$
where $T_U \coloneqq T \times_S U$.

A morphism of $G$-$\infty$-operads is a functor over $\mathrm{Span}(\mathbb{F}_G)$ preserving cocartesian lifts for backwards maps.
\end{definition}

\begin{proposition}
  A functor $\mathcal{C}^{\otimes} \rightarrow \mathrm{Span}(\mathbb{F}_G)$ is simultaneously a $G$-$\infty$-operad and a [[cocartesian fibration]] if and only if it is the [[straightening functor|unstraightening]] of a [[equivariant symmetric monoidal category|G-symmetric monoidal $\infty$-category]]
\end{proposition}

\begin{definition}
  If $\mathcal{O}^{\otimes},\mathcal{P}^{\otimes}$ are $G$-$\infty$-operads, an **$\mathcal{O}$-algebra in $\mathcal{P}^{\otimes}$** is a morphism of $G$-$\infty$-operads $\mathcal{O}^{\otimes} \rightarrow \mathcal{P}^{\otimes}$;
we denote by 
$$
\mathrm{Alg}_{\mathcal{O}}(\mathcal{P}) \subset \mathrm{Fun}_{/\mathrm{Span}(\mathbb{F}_G)}(\mathcal{O}^{\otimes}, \mathcal{P}^{\otimes})
$$ 
the full subcategory spanned by $\mathcal{O}$-algebras in $\mathcal{P}$.

In particular, if $\mathcal{C}^{\otimes}$ is a $G$-symmetric monoidal $\infty$-category, then $\mathcal{O}$-algebras in $\mathcal{C}^{\otimes}$ are defined to be $\mathcal{O}$-algebras in the underlying $G$-$\infty$-operad of $\mathcal{C}^{\otimes}$.

\end{definition}

## Examples

* [[N-∞ operads]]

* [[EV operads]]

* [[equivariant linear isometries operad]]

## Related concepts

* [[Parametrized Higher Category Theory and Higher Algebra]]

* [[equivariant symmetric monoidal category]]

* [[algebraic pattern]]

## References


Originally, 

* [[Denis Nardin]], [[Jay Shah]], _Parametrized and equivariant higher algebra_, (2022) ([arxiv:2203.00072](https://arxiv.org/abs/2203.00072))

In terms of the [[Burnside category]],

* {#Barkan22} [[Shaul Barkan]], [[Rune Haugseng]], [[Jan Steinebrunner]], _Envelopes for Algebraic Patterns_, (2022) ([arXiv:2208.07183](https://arxiv.org/abs/2208.07183))

* [[Natalie Stewart]]: _On tensor products of equivariant commutative operads_ (draft)  &lbrack;[pdf](https://nataliesstewart.github.io/files/Ninfty_draft.pdf)&rbrack;


[[!redirects G-∞-operad]]
[[!redirects G-∞ operad]]
[[!redirects G-∞ operads]]
[[!redirects G-operad]]
[[!redirects N-∞ operads]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Equivariant higher algebra
+--{: .hide}
[[!include equivariant higher algebra - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Content#
* table of contents
{:toc}

## Idea

A [[G-∞-operad|$G$-$\infty$-operad]] is an _$\mathcal{N}_\infty$-operad_ if it is infinitely [[ connected space|connected]] (or equivalently, [[homotopy n-type|$0$-truncated]]), unital, and prescribes binary multiplications on fixed points for all subgroups.

These are meant to model the _equivariant commutative operads_ which contain a non-genuine version of $\mathbb{E}_\infty$.

## Definition

Let $\underline{\mathbb{F}}_G^\infty \subset \underline{\mathbb{F}}_G$ be the $G$-[[indexing system]] whose $H$-sets are those finite $H$-sets with [[trivial]] action, and let $I^\infty \subset \mathbb{F}_G$ be the corresponding indexing category. Let $\mathbb{E}_\infty^{\otimes} = \left( \mathrm{Span}_{I^\infty}(\mathbb{F}_G) \rightarrow \mathrm{Span}(\mathbb{F}_G) \right)$ be the corresponding fibration.
This turns out to be a [[G-∞-operad]].
 
\begin{definition}
  A **weak $\mathcal{N}_\infty$-operad for $G$** is a $G$-0-operad.
  An **$\mathcal{N}_\infty$-operad for $G$** is a weak $\mathcal{N}_\infty$-operad for $G$ $\mathcal{O}^{\otimes}$ admitting a map $\mathbb{E}_\infty^{\otimes} \rightarrow \mathcal{O}^{\otimes}$.
\end{definition}

## Properties
### Relationship to indexing systems/arity support

Fix $S = \coprod_{i \leq n} [G/H_i] \in \mathbb{F}_G$ a $G$-set.
Recall that $\mathrm{Ind}_{H_i}^{G}:\mathbb{F}_{H_i} \rightarrow \mathbb{F}_{G, /[G/H_i]}$ is an equivalence;
given $\varphi:T \rightarrow S$ an equivariant function of $G$-sets, write $T_i$ for the $H_i$-set corresponding with $\varphi^{-1}([G/H_i])$.

\begin{definition}
Given $\mathcal{O}^{\otimes}$ a $G$-operad, the **arity support of $\mathcal{O}^{\otimes}$ is the subcategory
$$
  A \mathcal{O} \coloneqq \left\{T \rightarrow S \;\;\; \mid \;\;\; \forall [G/H_i], \in \mathrm{Orbit}(S), \;\; \mathcal{O}(T_i) \neq \emptyset \right\} \subset \mathbb{F}_{G}.
$$

\end{definition}

Let $\mathrm{Op}_G^{\Gamma}$ be the [[(∞,1)-category]] presented by the graph model structure on $G$-operads, and let $\mathcal{N}_\infty-\mathrm{Op}_G^{\Gamma} \subset \mathrm{Op}_G^{\Gamma}$ be the full subcategory spanned by $\mathcal{N}_\infty$-operads.

\begin{theorem}
  The functor $A$ restricts to an equivalence
  $$
    A:\mathcal{N}_\infty-\mathrm{Op}_G^{\Gamma} \xrightarrow\sim \mathrm{Index}_G,
  $$
  the latter denoting the poset of [[indexing systems]].
\end{theorem}

Fully-faithfullness in the [graph model category of $G$-operads](#Bonventre17), was proved in [Blumberg-Hill 13](#Blumberg13), followed by independent proofs in 2017 by [Rubin](#Rubin17), [Gutiérrez-White](#Gutierrez17), and [Bonventre-Pereira](#Bonventre17).

Subsequently, this was generalized to the orbital setting in [Nardin-Shah 22](#Nardin22), and to weak indexing systems in [Stewart 24](#Stewart24):

\begin{theorem}
  For all [[G-∞-operads]] $\mathcal{O}^{\otimes}$, $A \mathcal{O}$ is a [[indexing system|weak indexing category]], and the associated functor
$$
  A:\mathrm{Op}_G \rightarrow \mathrm{wIndex}_G
$$
  attains a fully faithful faithful right adjoint whose image is the weak $\mathcal{N}_\infty$-operads for $G$;
  the image of the subposet $\mathrm{Index}_G \subset \mathrm{wIndex}_G$ is the $\mathcal{N}_\infty$-operads for $G$.
\end{theorem}

### As sub-terminal $G$-$\infty$-operads

Let $\mathcal{N}_{(-)\infty}^{\otimes}:\mathrm{wIndex}_G \rightarrow \mathrm{Op}_G$ be the right adjoint to $A$.
The adjoint relationship implies that, for all $G$-$\infty$-operads $\mathcal{P}^{\otimes}$, we have 
$$
  \Map(\mathcal{P}^{\otimes}, \mathcal{N}_{I\infty}^{\otimes}) = \begin{cases}
  * & A\mathcal{P} \subset I,\\
  \emptyset & \mathrm{otherwise}.
\end{cases}
$$
In other words, $\mathcal{N}_{I \infty}^{\otimes} \in \mathrm{Op}_G$ is a [[subterminal object]] classifying the arity support condition $A(-) \leq I$. 
We refer to the resulting full subcategory $\mathrm{Op}_I \coloneqq \mathrm{Op}_{G, \mathcal{N}_{I \infty}^{\otimes}} \subset \mathrm{Op}_G$ as the *$I$-operads*. 

On the other hand, it is shown in [Stewart 24](#Stewart24) that the functor $\mathcal{O}^{\otimes} \mapsto \mathcal{O}(S)$ is [[corepresentable]], so if $\mathcal{O}^{\otimes}$ is a [[subterminal]] $G$-$\infty$-operad, its $S$-ary operation space $\mathcal{O}(S)$ is either empty or contractible for all $S$;
unwinding definitions, this shows that a $G$-$\infty$-operad is [[subterminal]] if and only if it's a weak $\mathcal{N}_\infty$-operad for $G$.

### As $\otimes$-idempotent $G$-$\infty$-operads.
(...)

## Algebras over $\mathcal{N}_\infty$-operads
(...)

## Related concepts

* [[Parametrized Higher Category Theory and Higher Algebra]]

* [[equivariant symmetric monoidal category]], [[G-∞-operad]]

* [[indexing system]]

* [[algebraic pattern]]

## References

Originally,

* {#Blumberg13} [[Andrew Blumberg]], [[Michael Hill]], _Operadic multiplications in equivariant spectra, norms, and transfers_, ([arXiv:1309.1750](https://arxiv.org/abs/1309.1750))

Classification via indexing systems (each independently proves this):

* {#Rubin17} [[Jonathan Rubin]], _Combinatorial $N_\infty$ operads_ (2017), ([arXiv:1705.03585](https://arxiv.org/abs/1705.03585))

* {#Gutierrez17} [[Javier Gutiérrez]], [[David White]], _Encoding Equivariant Commutativity via Operads_ (2017), ([arXiv:1707.02130](https://arxiv.org/abs/1707.02130))

* {#Bonventre17} Peter Bonventre, Luis Pereira, _Genuine equivariant operads_, (2017) ([1707.02226](https://arxiv.org/abs/1707.02226))

* {#Nardin22} [[Denis Nardin]], [[Jay Shah]], _Parametrized and equivariant higher algebra_, (2022) ([arxiv:2203.00072](https://arxiv.org/abs/2203.00072))

* {#Stewart24} [[Natalie Stewart]]: _On tensor products of equivariant commutative operads_ (draft)  &lbrack;[pdf](https://nataliesstewart.github.io/files/Ninfty_draft.pdf)&rbrack;

Presentation of algebras in the $C_p$-equivariant case:

* [[Lucy Yang]], _On normed $\mathbb{E}_\infty$-rings in genuine equivariant $C_p$-spectra_, (2023) ([arXiv:2308.16107](https://arxiv.org/abs/2308.16107))

[[!redirects N-∞ operads]]
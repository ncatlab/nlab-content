[[!redirects N-∞ operads]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

A [[G-∞-operad|$G$-$\infty$-operad]] is an _$\mathcal{N}_\infty$-operad_ if it is infinitely [[ connected space|connected]], unital, and prescribes binary multiplications on fixed points for all subgroups.

These are meant to model the _equivariant commutative operads_ which contain a non-genuine version of $\mathbb{E}_\infty$.



## Properties

Fix $S = \coprod_{i \leq n} [G/H_i] \in \mathbb{F}_G$ a $G$-set.
Recall that $\mathrm{Ind}_{H_i}^{G}:\mathbb{F}_{H_i} \rightarrow \mathbb{F}_{G, /[G/H_i]}$ is an equivalence;
given $\varphi:T \rightarrow S$ an equivariant function of $G$-sets, write $T_i$ for the $H_i$-set corresponding with $\varphi^{-1}([G/H_i])$.


Given $\mathcal{O}^{\otimes}$ a $G$-operad, we define the subcategory
$$
  A \mathcal{O} \coloneqq \left\{T \rightarrow S \;\;\; \mid \;\;\; \forall [G/H_i], \in \mathrm{Orbit}(S), \;\; \mathcal{O}(T_i) \neq \emptyset \right\} \subset \mathbb{F}_{G}.
$$

Let $\mathrm{Op}_G^{\Gamma}$ be the [[(∞,1)-category]] presented by the graph model structure on $G$-operads, and let $\mathcal{N}_\infty-\mathrm{Op}_G^{\Gamma} \subset \mathrm{Op}_G^{\Gamma}$ be the full subcategory spanned by $\mathcal{N}_\infty$-operads.

\begin{theorem}
  The functor $A$ restricts to an equivalence
  $$
    A:\mathcal{N}_\infty-\mathrm{Op}_G^{\Gamma} \xrightarrow\sim \mathrm{Index}_G,
  $$
  the latter denoting the poset of [[indexing systems]].
\end{theorem}

Fully-faithfullness in the [graph model category of $G$-operads](#Bonventre17), was proved in [Blumberg-Hill 13](#Blumberg13), followed by independent proofs in 2017 by [Rubin](#Rubin17), [Gutiérrez-White](#Gutierrez17), and [Bonventre-Pereira](#Bonventre17).

Subsequently, this was generalized to the orbital setting in [Nardin-Shah 22](#Nardin22).

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

Presentation of algebras in the $C_p$-equivariant case:

* [[Lucy Yang]], _On normed $\mathbb{E}_\infty$-rings in genuine equivariant $C_p$-spectra_, (2023) ([arXiv:2308.16107](https://arxiv.org/abs/2308.16107))

[[!redirects N-∞ operads]]
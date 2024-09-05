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

On the other hand, it is shown in [Stewart 24](#Stewart24) that the functor $\mathcal{O}^{\otimes} \mapsto \mathcal{O}(S)$ is [[corepresentable functor|corepresentable]], so if $\mathcal{O}^{\otimes}$ is a [[subterminal]] $G$-$\infty$-operad, its $S$-ary operation space $\mathcal{O}(S)$ is either empty or contractible for all $S$;
unwinding definitions, this shows that a $G$-$\infty$-operad is [[subterminal]] if and only if it's a weak $\mathcal{N}_\infty$-operad for $G$.

### As $\otimes$-idempotent $G$-$\infty$-operads.

The [[Boardman-Vogt tensor product]] naturally extends to a tensor product on $G$-operads via the formula 
$$\mathcal{O}^{\otimes} \otimes^{BV} \mathcal{P}^{\otimes} \coloneqq L_{\mathrm{Op}_G} \left(
\mathcal{O}^{\otimes} \times \mathcal{P}^{\otimes} 
\rightarrow 
\mathrm{Span}(\mathbb{F}_G) \times \mathrm{Span}(\mathbb{F}_G)
\xrightarrow{\wedge}
 \mathrm{Span}(\mathbb{F}_G))
\right),$$    

where $\wedge:\mathrm{Span}(\mathbb{F}_G) \times \mathrm{Span}(\mathbb{F}_G) \rightarrow \mathrm{Span}(\mathbb{F}_G)$ is induced by the [[cartesian product]] of finite $G$-sets.
The following is shown in [Stewart 24](#Stewart24).

\begin{theorem}
  There exists an equivalence $\mathcal{N}_{I\infty}^{\otimes} \otimes^{BV} \mathcal{N}_{I \infty}^{\otimes} \simeq \mathcal{N}_{I \infty}^{\otimes}$ if and only if $I$ is an [[indexing system|aE-unital weak indexing system]], in which case a reduced $G$-$\infty$-operad $\mathcal{O}^{\otimes}$ satisfies
$$
  \mathcal{O}^{\otimes} \otimes^{BV} \mathcal{N}_{I \infty}^{\otimes} \simeq \mathcal{O}^{\otimes}
$$
if and only if  the [[G-∞-category]] $\underline{\mathrm{Alg}}_{\mathcal{O}}(\underline{\mathcal{S}}_G)$ of $\mathcal{O}$-algebras in [[G-spaces]] is [[G-semiadditivity|I-semiadditive]].

\end{theorem}

As a corollary, [Stewart 24](#Stewart24) concludes the following.

\begin{corollary}
  If $I$ and $J$ are [[indexing system|unital weak indexing systems]], then there is a (unique) equivalence
  $$
    \mathcal{N}_{I\infty}^{\otimes} \otimes^{BV} \mathcal{N}_{J \infty}^{\otimes} \simeq \mathcal{N}_{I \vee J \infty}^{\otimes},
  $$
  where $I \vee J$ denotes the join of $I$ and $J$ in the poset of [[indexing systems|weak indexing systems]].

\end{corollary}

The same theorem extends to [[indexing system|aE-unital weak indexing systems]], but the statement is somewhat more complicated;
since indexing systems are a join-closed full sub-poset of weak indexing systems, this specializes to a theorem on the level of indexing systems, by omitting the words "unital weak."

In the language of §6.3 of [Blumberg-Hill 13](#Blumberg13), 
this confirms that in the homotopy-coherent setting every action of an $\mathcal{N}_\infty$-operad interchanges with itself, and every pair of interchanging $I$- and $J$-commutative algebra structures agrees on $I \cap J$ and is restricted from an $I \vee J$-commutative algebra structure.

## Algebras over $\mathcal{N}_\infty$-operads

### As incomplete Mackey functors in the cartesian setting

The following theorem was proved in the setting of *graph $G$-operads* and for $\mathcal{C} = \underline{\mathcal{S}}_G$ in [Marc 24](#Marc24), and in the setting of [[G-∞-operads]] in [Stewart 24](#Stewart24).
\begin{theorem}
  If $\mathcal{C}^{\otimes}$ is a [[equivariant symmetric monoidal category|I-symmetric monoidal ∞-category]] whose indexed tensor products are [[indexed products]], then there is a canonical equivalence 
$$
\mathrm{Alg}_{\mathcal{N}_{I \infty}}(\mathcal{C}) \simeq \mathrm{CMon}_I(\mathcal{C})
$$
over $\mathcal{C}$.
In particular, if $\mathcal{C}$ is the $G$-$\infty$-category of coefficient systems in an [[∞-category]] $\mathcal{V}$ with its [[Cartesian G-symmetric monoidal ∞-category|Cartesian structure]], then there is an equivalence
$$
  \mathrm{Alg}_{\mathcal{N}_{I \infty}}(\mathcal{C}) \simeq \mathrm{Fun}^{\times}(\mathrm{Span}(\mathbb{F}_G, \mathcal{V}).
$$

\end{theorem} 

### As incomplete Tambara functors

In [CHLL 24](#Tambara), it is shown that the equivariant Day convolution [[equivariant symmetric monoidal category|G-symmetric monoidal structure]] structure on the equivariant functor category $\mathrm{Fun}(\mathrm{Span}(\underline{\mathbb{F}_G}), \mathcal{C})$ restricts to a $G$-symmetric monoidal structure on the [[G-∞-category]] $\underline{\mathrm{CMon}}_G(\mathcal{C})$ of [[G-commutative monoids]] in $\mathcal{C}$.
Then, [CHLL 24 Theorem B](#Tambara) shows the following.

\begin{theorem}
  There is a fully faithful functor
$$
  \mathrm{CAlg}_I(\underline{\mathrm{Sp}}_G^{\otimes}) \hookrightarrow \mathrm{Fun}^{\times}(\mathrm{BiSpan}(\mathbb{F}_G), \mathcal{S})
$$
  whose image consists of the functors whose $H$-value "additive" commutative monoid is grouplike for all $H \subset G$.
\end{theorem} 

### As normed algebras

(under construction...)

Let $p$ be a [[prime number]] and $C_p$ the [[cyclic group]] of order $p$.
Let $(-)^e\colon \mathrm{Sp}_G \rightarrow \mathrm{Sp}^{BG}$ be the *underlying spectrum with $G$-action, and let $N_e^G$ be the Hill-Hopkins-Ravanel norm $G$-spectrum on a spectrum. 

Given $A \in \mathrm{CAlg}(\mathrm{Sp}^{BC_p})$ a (highly structured) [[E-infinity-ring
|commutative ring spectrum]] with $C_p$-action, we let $A^{\otimes^{\Delta} p}  \in \mathrm{CAlg}(\mathrm{Sp}^{BC_p})$ be the [[E-infinity-ring
|commutative ring spectrum]] with diagonal $C_p$-action 

$$
  \sigma(a_1 \otimes \cdots \otimes a_p) = \sigma(a_p) \otimes \sigma(a_1) \otimes \cdots \otimes \sigma(a_{p-1}).
$$

Furthermore, we let $A^{\otimes^{\tau} p}  \in \mathrm{CAlg}(\mathrm{Sp}^{BC_p})$ be the [[E-infinity-ring
|commutative ring spectrum]] with transpotiion $C_p$-action 

$$
  \sigma(a_1 \otimes \cdots \otimes a_p) = a_p \otimes a_1 \otimes \cdots \otimes a_{p-1}.
$$

\begin{definition}
  A **normed $\mathbb{E}_\infty$-algebra in $C_p$-spectra** is the data of

* an $\mathbb{E}_\infty$-algebra in $C_p$, 

* a morphism of $\mathbb{E}_\infty$-rings $n_A\colon N^{C_p}_e A^e_{h_{C_p}} \rightarrow A$, and
 
* a homotopy making the following diagram $\mathcal{O}_{C_p} \rightarrow \mathbb{E}_\infty \mathrm{Alg}(\mathrm{Sp})^{B C_p}$ commute:

\begin{tikzcd}
	{\left( A^e \right)^{\otimes^{\tau}p} } & {A^e} \\
	{\left( A^e \right)^{\otimes^{\Delta}p} }
	\arrow["{n_A}", from=1-1, to=1-2]
	\arrow["{\mathrm{id} \otimes \sigma \otimes \cdots \otimes \sigma^{p-1}}"', "\sim", from=1-1, to=2-1]
	\arrow["\mu"', from=2-1, to=1-2]
\end{tikzcd}
  
  We denote the category of normed $\mathbb{E}_\infty$-algebras in $C_p$-spectra by $\mathrm{NAlg}_{C_p}(\mathrm{Sp}_{C_p})$.
\end{definition}

[Yang 23](#Yang23) constructs a forgetful functor $U\colon \mathrm{CAlg}_{C_p}(\mathrm{Sp}_{C_p}) \rightarrow \mathrm{NAlg}_{C_p}(\mathrm{Sp}_{C_p})$.
The main result of [Yang 23](#Yang23) is that this is an equivalence:

\begin{theorem}
  The forgetful functor
$$
  U\colon \mathrm{CAlg}_{C_p}(\mathrm{Sp}_{C_p}) \rightarrow \mathrm{NAlg}_{C_p}(\mathrm{Sp}_{C_p})
$$
  is an equivalence.
\end{theorem}

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

Presentation of algebras in various cases:

* {#Yang23}[[Lucy Yang]], _On normed $\mathbb{E}_\infty$-rings in genuine equivariant $C_p$-spectra_, (2023) ([arXiv:2308.16107](https://arxiv.org/abs/2308.16107))

* {#Marc24} Gregoire Marc, _A higher Mackey functor description of algebras over an $\mathcal{N}_\infty$-operad_, (2024) ([arXiv:2402.12447](https://arxiv.org/abs/2402.12447))

* {#Tambara} [[Bastiaan Cnossen]], [[Rune Haugseng]], [[Tobias Lenz]], [[Sil Linskens]]: _Normed equivariant ring spectra and higher Tambara functors_ ([arXiv:2407.08399](https://arxiv.org/abs/2407.08399))

[[!redirects N-∞ operads]]
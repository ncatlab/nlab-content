

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

Bishop introduced the [[principles of omniscience]] for the [[natural numbers]] to show that certain results in pointwise [[analysis]] could not be constructive, by showing that these results implied a principle of omniscience. There are similar axioms in analysis which imply the principles of omniscience for natural numbers, called the **analytic principles of omniscience**. 

The analytic principles of omniscience are as follows:

*  The __analytic LPO__ states that the usual [[apartness relation]] on the set $\mathbb{R}$ of [[real numbers]] is [[decidable relation|decidable]] ($x \neq y$ or $x = y$), or equivalently __[[trichotomy]]__ for the real numbers ($x \lt y$ or $x = y$ or $x \gt y$), or equivalently, that the real numbers form a [[discrete field]].

* The __analytic WLPO__ states that $\mathbb{R}$ has [[decidable equality]], or that the partial order on the real numbers is [[decidable]] ($x \leq y$ or $\neg (x \leq y)$). 

*  The __analytic LLPO__ states that the usual order on $\mathbb{R}$ is a [[total order]] ($x \leq y$ or $x \geq y$), which (by analogy with trichotomy) may be called __dichotomy__ for the real numbers.

The analytic principles of omniscience imply the corresponding ones for natural numbers; the converses hold if we assume [[weak countable choice]] (as Bishop did). (Note that we need not accept $WCC$ to see that an analytic result implies a principle of omniscience and so cannot be constructively valid.)

However, there are many different notions of real numbers in [[constructive mathematics]], so there are many different notions of the analytic principles of omniscience. So let us define a real number field $R$ to be an [[lattice-ordered ring|lattice-ordered]] [[Archimedean ordered field|Archimedean ordered]] [[field extension]] of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$. Thus, given a real number field $R$ one has unique [[ring homomorphisms]] of real number fields
$$\mathbb{R}_C \hookrightarrow R \hookrightarrow \mathbb{R}_D$$
where $\mathbb{R}_D$ is the field of [[Dedekind real numbers]]. In general the ring homomorphisms are not provably [[isomorphisms]] unless the [[Dedekind real numbers]] and [[Cauchy real numbers]] coincide. 

For each real number field $R$, one has similar statements of the analytic principles of omniscience: 

*  The __$R$-analytic LPO__ states that the usual [[apartness relation]] on the real number field $R$ [[decidable relation|decidable]] ($x \neq y$ or $x = y$), or equivalently __[[trichotomy]]__ for the real number field $R$ ($x \lt y$ or $x = y$ or $x \gt y$), or equivalently, that the real number field $R$ is a [[discrete field]].

* The __$R$-analytic WLPO__ states that the real number field $R$ has [[decidable equality]], or that the partial order on $R$ is [[decidable]] ($x \leq y$ or $\neg (x \leq y)$). 

*  The __$R$-analytic LLPO__ states that the lattice order on $R$ is a [[total order]] ($x \leq y$ or $x \geq y$), which (by analogy with trichotomy) may be called __dichotomy__ for the real number field $R$.

One has a hierarchy of analytic principles of omniscience, where

* The (sequential-, modulated-, Cantor-, Cauchy-, $\mathbb{R}_C$-) analytic principles of omniscience is the weakest and equivalent to the corresponding principles of omniscience for the natural numbers;

* The (Dedekind-, $\mathbb{R}_D$-)analytic principle of omniscience is the strongest. 

* For any other real number field $R$ which is neither equivalent to the Cauchy real numbers or the Dedekind real numbers, the corresponding $R$-analytic principles of omniscience are intermediate in strength between the Cauchy-analytic principles of omniscence and the Dedekind-analytic principles of omniscience. 

* Suppose that there are two real number fields $R$ and $R'$ such that $R'$ is a [[field extension]] of $R$. Then each $R'$-analytic principle of omniscience implies the respective $R$-analytic principle of omniscience. 

Finally, one has the following: Let $\Sigma$ be the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]]. It is a sub-$\sigma$-frame of the [[frame of truth values]], which implies that one can construct a set of Dedekind real numbers $\mathrm{R}_\Sigma$ out of Dedekind cuts in $\Sigma^\mathbb{Q} \times \Sigma^\mathbb{Q}$. Also, let $\mathbb{R}_H$ be the [[HoTT book real numbers]], which are the initial [[sequentially Cauchy complete space|sequentially Cauchy complete]] [[Archimedean ordered field]]. One has ring homomorphisms
$$\mathrm{R}_C \hookrightarrow \mathrm{R}_H \hookrightarrow \mathrm{R}_\Sigma \hookrightarrow \mathrm{R}_D$$
Then, 

\begin{theorem}
The LPO for natural numbers, the $\mathbb{R}_C$-analytic LPO, the $\mathbb{R}_H$-analytic LPO, and the $\mathbb{R}_\Sigma$-analytic LPO are equivalent to each other. 
\end{theorem}

\begin{proof}
The LPO for natural numbers is equivalent to the [[boolean domain]] $\mathbb{2}$ being the initial $\sigma$-frame $\Sigma \coloneqq \mathbb{2}$. This implies that one can use the booleans to construct $\mathbb{R}_\Sigma$. The LPO also implies the $\mathbb{R}_\Sigma$-analytic LPO, since the [[pseudo-order]] relation $\lt$ on $\mathbb{R}_\Sigma$ is defined as an [[existential quantification]] over the rational numbers, which is [[decidable]] because of LPO and the fact that the rational numbers are in bijection with the natural numbers. The $\mathbb{R}_\Sigma$-analytic LPO implies that every real number in $\mathbb{R}_\Sigma$ comes with the structure of a [[locator]], which implies that $\mathbb{R}_C$, $\mathbb{R}_H$, and $\mathbb{R}_\Sigma$ are isomorphic as real number fields. Thus, the $\mathbb{R}_\Sigma$-analytic LPO, $\mathbb{R}_H$-analytic LPO, and $\mathbb{R}_C$-analytic LPO are equivalent to each other. Finally, the $\mathbb{R}_C$-analytic LPO is equivalent to the LPO for natural numbers, which is sufficient to establish that the converses of the above implications hold. 
\end{proof}

The analytic $\mathrm{LPO}$ for any field of real numbers $\mathbb{R}$ implies the [[fundamental theorem of algebra]] for $\mathbb{R}$. 

## Related concepts

* [[principle of omniscience]]

* [[axiom of real cohesion]]

* [[intermediate value theorem]]

* [[analytic Markov's principle]]

## References

The analytic WLPO and LLPO are mentioned in the following paper, although unfortunately it uses the phrase "analytic LPO" for what should really be the analytic *WLPO* (the reals have decidable equality):

* {#Shulman18} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

[[!redirects analytic principle of omniscience]]
[[!redirects analytic principles of omniscience]]

[[!redirects analytic LPO]]
[[!redirects analytic limited principle of omniscience]]
[[!redirects analytic limited principles of omniscience]]

[[!redirects analytic LLPO]]
[[!redirects analytic lesser limited principle of omniscience]]
[[!redirects analytic lesser limited principles of omniscience]]

[[!redirects analytic WLPO]]
[[!redirects analytic weak limited principle of omniscience]]
[[!redirects analytic weak limited principles of omniscience]]
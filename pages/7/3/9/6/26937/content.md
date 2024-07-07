

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

Bishop introduced the [[principles of omniscience]] for the [[natural numbers]] to show that certain results in pointwise [[analysis]] could not be constructive, by showing that these results implied a principle of omniscience. There are similar axioms in analysis which imply the principles of omniscience for natural numbers, called the **analytic principles of omniscience**. These include

* The [[analytic limited principle of omniscience]]

* The [[analytic weak limited principle of omniscience]]

* The [[analytic lesser limited principle of omniscience]]

* (sometimes) The [[analytic Markov's principle]]

## Definition

There are many different notions of real numbers in [[constructive mathematics]]. What all these real numbers have in common are that they are an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$; i.e. there are unique [[ring homomorphisms]] of real number fields
$$\mathbb{R}_C \hookrightarrow R \hookrightarrow \mathbb{R}_D$$
where $\mathbb{R}_D$ is the field of [[Dedekind real numbers]] - the latter always exists since $\mathbb{R}_D$ is the [[terminal object|terminal]] Archimedean ordered field. In general the ring homomorphisms are not provably [[isomorphisms]] unless the [[Dedekind real numbers]] and [[Cauchy real numbers]] coincide. Thus, there are many different notions of the analytic principles of omniscience; the analytic principles of omniscience are defined for each Archimedean ordered field extension of the Cauchy real numbers. 

### Analytic limited principle of omniscience

\begin{definition}
Let $R$ be an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$. The __analytic LPO__ for $R$ states that the usual [[apartness relation]] on $R$ [[decidable relation|decidable]] ($x \neq y$ or $x = y$), or equivalently __[[trichotomy]]__ for $R$ ($x \lt y$ or $x = y$ or $x \gt y$), or equivalently, that $R$ is a [[discrete field]].
\end{definition}

\begin{theorem}
The analytic LPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$ implies the LPO for [[natural numbers]]. 
\end{theorem}

\begin{proof}
...
\end{proof}

\begin{theorem}
The LPO for [[natural numbers]] implies the analytic LPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{theorem}

\begin{proof}
...
\end{proof}

\begin{lemma}
The LPO for [[natural numbers]] is equivalent to the analytic LPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{lemma}

\begin{theorem}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then the analytic LPO for $R$ implies that $R$ is isomorphic to $\mathbb{R}_C$
\end{theorem}

\begin{proof}
... use theorems 11.4.1 and 11.4.3 of [UFP 2013](#UFP13). 
\end{proof}

\begin{theorem}
Suppose that there are two Archimedean ordered fields $R$ and $R'$ such that both are [[field extensions]] of the [[Cauchy real numbers]] $\mathbb{R}_C$ and $R'$ is a [[field extension]] of $R$. Then, the analytic LPO for $R'$ implies the analytic LPO for $R$. 
\end{theorem}

\begin{proof}
Analytic LPO for $R'$ implies that $R'$ is [[isomorphic]] to the [[Cauchy real numbers]], which implies that any subfield of $R'$ which is a field extension of the Cauchy real numbers is isomorphic to $R'$. Since this is true of $R$, this implies that the analytic LPO for $R$ also holds, since $R'$ and $R$ are isomorphic fields. 
\end{proof}

\begin{lemma}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then, the analytic LPO for $R$ implies the LPO for [[natural numbers]]. 
\end{lemma}

\begin{proof}
Since the field of Cauchy real numbers is a (trivial) field extension of itself, the analytic LPO for $R$ implies the analytic LPO for the Cauchy real numbers, which implies the LPO for the natural numbers. 
\end{proof}

Thus, one has a hierarchy of analytic limited principles of omniscience, where

* The (sequential-, modulated-, Cantor-, Cauchy-, $\mathbb{R}_C$-) analytic LPO is the weakest and equivalent to the LPO for the [[natural numbers]];

* The (Dedekind-, $\mathbb{R}_D$-)analytic LPO is the strongest. 

* For any other Archimedean ordered field extension of the Cauchy real numbers $R$ which is neither equivalent to the Cauchy real numbers or the Dedekind real numbers, the $R$-analytic LPO are intermediate in strength between the Cauchy-analytic LPO and the Dedekind-analytic LPO. 

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

### Analytic weak limited principle of omniscience

\begin{definition}
Let $R$ be an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$. The __analytic WLPO__ for $R$ states that $R$ has [[decidable equality]], or that the partial order on $R$ is [[decidable]] ($x \leq y$ or $\neg (x \leq y)$). 
\end{definition}

\begin{theorem}
The analytic WLPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$ implies the WLPO for [[natural numbers]]. 
\end{theorem}

\begin{proof}
...
\end{proof}

\begin{theorem}
The WLPO for [[natural numbers]] implies the analytic WLPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{theorem}

\begin{proof}
...
\end{proof}

\begin{lemma}
The WLPO for [[natural numbers]] is equivalent to the analytic WLPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{lemma}

\begin{theorem}
Suppose that there are two Archimedean ordered fields $R$ and $R'$ such that both are [[field extensions]] of the [[Cauchy real numbers]] $\mathbb{R}_C$ and $R'$ is a [[field extension]] of $R$. Then, the analytic WLPO for $R'$ implies the analytic WLPO for $R$. 
\end{theorem}

\begin{proof}
Analytic WLPO for $R'$ implies that $R'$ has [[decidable equality]]. Any subset of a set with decidable equality also has decidable equality. Since $R$ is a subfield of $R'$, $R$ also has decidable equality, which is the analytic WLPO for $R$. 
\end{proof}

\begin{lemma}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then, the analytic WLPO for $R$ implies the WLPO for [[natural numbers]]. 
\end{lemma}

\begin{proof}
Since the field of Cauchy real numbers is a (trivial) field extension of itself, the analytic WLPO for $R$ implies the analytic WLPO for the Cauchy real numbers, which implies the WLPO for the natural numbers. 
\end{proof}

Thus, one has a hierarchy of analytic weak limited principles of omniscience, where

* The (sequential-, modulated-, Cantor-, Cauchy-, $\mathbb{R}_C$-) analytic WLPO is the weakest and equivalent to the WLPO for the [[natural numbers]];

* The (Dedekind-, $\mathbb{R}_D$-)analytic WLPO is the strongest. 

* For any other Archimedean ordered field extension of the Cauchy real numbers $R$ which is neither equivalent to the Cauchy real numbers or the Dedekind real numbers, the $R$-analytic WLPO are intermediate in strength between the Cauchy-analytic WLPO and the Dedekind-analytic WLPO. 

## Related concepts

* [[principle of omniscience]]

* [[axiom of real cohesion]]

* [[intermediate value theorem]]

* [[analytic Markov's principle]]

## References

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

The analytic WLPO and LLPO are mentioned in the following paper, although unfortunately it uses the phrase "analytic LPO" for what should really be the analytic *WLPO* (the reals have decidable equality):

* {#Shulman18} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

[[!redirects analytic principle of omniscience]]
[[!redirects analytic principles of omniscience]]

[[!redirects analytic LPO]]
[[!redirects analytic limited principle of omniscience]]
[[!redirects analytic limited principles of omniscience]]

[[!redirects analytic WLPO]]
[[!redirects analytic weak limited principle of omniscience]]
[[!redirects analytic weak limited principles of omniscience]]
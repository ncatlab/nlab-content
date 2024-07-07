
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[real analysis]], there is a principle on the [[Cauchy real numbers]] which is equivalent in strength to the [[lesser limited principle of omniscience]] for [[natural numbers]], and states that the [[partial order]] on the [[Cauchy real numbers]] is a [[total order]]. This principle can be generalised from the Cauchy real numbers to all notions of [[real numbers]], such as the [[Dedekind real numbers]], and is hence called the *analytic lesser limited principle of omniscience*, or the *analytic LLPO*. In [[classical mathematics]], all of these are implied by [[excluded middle]]; however, in [[neutral constructive mathematics]], the different analytic LLPO are different principles of different strength, because the Cauchy and Dedekind real numbers and any other notion of real numbers between the Cauchy and Dedekind real numbers cannot be proven to coincide. 

## Definition

There are many different notions of real numbers in [[constructive mathematics]]. What all these real numbers have in common are that they are an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$; i.e. there are unique [[ring homomorphisms]] of ordered fields
$$\mathbb{R}_C \hookrightarrow R \hookrightarrow \mathbb{R}_D$$
where $\mathbb{R}_D$ is the ordered field of [[Dedekind real numbers]] - the homomorphism into $\mathbb{R}_D$ always exists since $\mathbb{R}_D$ is the [[terminal object|terminal]] Archimedean ordered field. In general the ring homomorphisms are not provably [[isomorphisms]] unless the [[Dedekind real numbers]] and [[Cauchy real numbers]] coincide. Thus, there are many different notions of the analytic lesser limited principle of omniscience; the analytic lesser limited principles of omniscience are defined for each Archimedean ordered field extension of the Cauchy real numbers. 

\begin{definition}
Let $R$ be an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$. The __analytic lesser limited principle of omniscience__ or __analytic LLPO__ for $R$ states that the [[partial order]] on $R$ is a [[total order]] ($x \leq y$ or $x \geq y$), which (by analogy with trichotomy) may be called __dichotomy__ for $R$.
\end{definition}

**Warning**. Given an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]], the *analytic lesser limited principle of omniscience for $R$* is not to be confused with the *[[lesser limited principle of omniscience]] for $R$* - the latter is the statement that for every [[function]] $f$ and $g$ from $R$ to the [[boolean domain]], if it isn't true that at the same time, there exist an element $x$ in $R$ such that $f(x) = \mathrm{true}$ and there exist an element $y$ in $R$ such that $g(y) = \mathrm{true}$, then either $f(x) = \mathrm{false}$ for all elements $x$ in $R$ or $g(y) = \mathrm{false}$ for all elements $y$ in $R$. For $R$ the Cauchy real numbers, the analytic LLPO for the Cauchy real numbers is equivalent to the LLPO for the [[natural numbers]], while the LLPO for the [[Cauchy real numbers]] is much stronger than the LLPO for the [[natural numbers]]. 

\begin{theorem}
The analytic LLPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$ implies the LLPO for [[natural numbers]]. 
\end{theorem}

\begin{proof}
TBD...
\end{proof}

\begin{theorem}
The LLPO for [[natural numbers]] implies the analytic LLPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{theorem}

\begin{proof}
TBD...
\end{proof}

\begin{lemma}
The LLPO for [[natural numbers]] is equivalent to the analytic LLPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{lemma}

\begin{theorem}
Suppose that there are two Archimedean ordered fields $R$ and $R'$ such that both are [[field extensions]] of the [[Cauchy real numbers]] $\mathbb{R}_C$ and $R'$ is a [[field extension]] of $R$. Then, the analytic LLPO for $R'$ implies the analytic LLPO for $R$. 
\end{theorem}

\begin{proof}
TBD...
\end{proof}

\begin{lemma}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then, the analytic LLPO for $R$ implies the LLPO for [[natural numbers]]. 
\end{lemma}

\begin{proof}
Since the field of Cauchy real numbers is a (trivial) field extension of itself, the analytic LLPO for $R$ implies the analytic LLPO for the Cauchy real numbers, which implies the LLPO for the natural numbers. 
\end{proof}

Thus, one has a hierarchy of analytic lesser limited principles of omniscience, where

* The (sequential-, modulated-, Cantor-, Cauchy-, $\mathbb{R}_C$-) analytic LLPO is the weakest and equivalent to the LLPO for the [[natural numbers]];

* The (Dedekind-, $\mathbb{R}_D$-)analytic LLPO is the strongest. 

* For any other Archimedean ordered field extension of the Cauchy real numbers $R$ which is neither equivalent to the Cauchy real numbers or the Dedekind real numbers, the $R$-analytic LLPO are intermediate in strength between the Cauchy-analytic LLPO and the Dedekind-analytic LLPO. 

Let $R$ be any Archimedean ordered field extension of the Cauchy real numbers. The analytic LLPO makes sense for any  [[Archimedean ordered local ring|Archimedean ordered]] [[local Artinian algebra|local Artinian $R$-algebra]] $A$ as well, where the relation $\lt$ is in general only a [[strict weak order]] instead of a [[pseudo-order]], the [[preorder]] $\geq$ is not a [[partial order]], and the equivalence relation $a \approx b$ derived from the preorder holds if and only if $a - b$ is [[nilpotent]]. In this case, the analytic LLPO for the Weil $R$-algebra $A$ says that the [[preorder]] on $A$ is a [[total preorder]], and the quotient of $A$ by its [[nilradical]] is the field of real numbers $R$ satisfying the analytic LLPO. 

## Models

* The analytic LLPO for [[Dedekind real numbers]] holds in Johnstone's [[topological topos]], as a consequence of the preservation of finite closed unions by the inclusion of sequential spaces.

* The analytic LLPO for [[Dedekind real numbers]] fails in the cohesive types of [[Mike Shulman]]'s [[real-cohesive homotopy type theory]], which model [[Euclidean-topological infinity-groupoids]]. However, the analytic LLPO for [[Cauchy real numbers]] holds in the cohesive types, since the analytic LPO for Cauchy real numbers hold and imply the analytic LLPO for Cauchy real numbers. 

## Related concepts

* [[lesser limited principle of omniscience]]

* [[analytic LPO]]

* [[analytic WLPO]]

* [[analytic Markov's principle]]

## References

* [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

[[!redirects analytic LLPO]]
[[!redirects analytic lesser limited principle of omniscience]]
[[!redirects analytic lesser limited principles of omniscience]]

[[!redirects analytic LLPO for Cauchy real numbers]]
[[!redirects analytic lesser limited principle of omniscience for Cauchy real numbers]]
[[!redirects analytic lesser limited principles of omniscience for Cauchy real numbers]]

[[!redirects Cauchy-analytic LLPO]]
[[!redirects Cauchy-analytic lesser limited principle of omniscience]]
[[!redirects Cauchy-analytic lesser limited principles of omniscience]]

[[!redirects Cauchy analytic LLPO]]
[[!redirects Cauchy analytic lesser limited principle of omniscience]]
[[!redirects Cauchy analytic lesser limited principles of omniscience]]

[[!redirects analytic LLPO for Dedekind real numbers]]
[[!redirects analytic lesser limited principle of omniscience for Dedekind real numbers]]
[[!redirects analytic lesser limited principles of omniscience for Dedekind real numbers]]

[[!redirects Dedekind-analytic LLPO]]
[[!redirects Dedekind-analytic lesser limited principle of omniscience]]
[[!redirects Dedekind-analytic lesser limited principles of omniscience]]

[[!redirects Dedekind analytic LLPO]]
[[!redirects Dedekind analytic lesser limited principle of omniscience]]
[[!redirects Dedekind analytic lesser limited principles of omniscience]]
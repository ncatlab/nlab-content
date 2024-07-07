
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

In [[real analysis]], there is a principle on the [[Cauchy real numbers]] which is equivalent in strength to the [[weak limited principle of omniscience]] for [[natural numbers]], and states that the [[partial order]] on the [[Cauchy real numbers]] is a [[decidable relation]], or that the [[Cauchy real numbers]] have [[decidable equality]]. This principle can be generalised from the Cauchy real numbers to all notions of [[real numbers]], such as the [[Dedekind real numbers]], and is hence called the *analytic weak limited principle of omniscience*, or the *analytic WLPO*. In [[classical mathematics]], all of these are implied by [[excluded middle]]; however, in [[neutral constructive mathematics]], the different analytic WLPO are different principles of different strength, because the Cauchy and Dedekind real numbers and any other notion of real numbers between the Cauchy and Dedekind real numbers cannot be proven to coincide. 

## Definition

There are many different notions of real numbers in [[constructive mathematics]]. What all these real numbers have in common are that they are an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$; i.e. there are unique [[ring homomorphisms]] of ordered fields
$$\mathbb{R}_C \hookrightarrow R \hookrightarrow \mathbb{R}_D$$
where $\mathbb{R}_D$ is the ordered field of [[Dedekind real numbers]] - the homomorphism into $\mathbb{R}_D$ always exists since $\mathbb{R}_D$ is the [[terminal object|terminal]] Archimedean ordered field. In general the ring homomorphisms are not provably [[isomorphisms]] unless the [[Dedekind real numbers]] and [[Cauchy real numbers]] coincide. Thus, there are many different notions of the analytic weak limited principle of omniscience; the analytic weak limited principles of omniscience are defined for each Archimedean ordered field extension of the Cauchy real numbers. 

\begin{definition}
Let $R$ be an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$. The **analytic weak limited principle of omniscience** or **analytic WLPO** for $R$ states that $R$ has [[decidable equality]], or that the partial order on $R$ is [[decidable]] ($x \leq y$ or $\neg (x \leq y)$). 
\end{definition}

**Warning**. Given an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]], the *analytic weak limited principle of omniscience for $R$* is not to be confused with the *[[weak limited principle of omniscience]] for $R$* - the latter is the statement that for every [[function]] $f$ from $R$ to the [[boolean domain]], the [[universal quantifier]] "for all elements $x$ in $R$, $f(x) = 0$" is [[decidable proposition|decidable]]. For $R$ the Cauchy real numbers, the analytic WLPO for the Cauchy real numbers is equivalent to the WLPO for the [[natural numbers]], while the WLPO for the [[Cauchy real numbers]] is much stronger than the WLPO for the [[natural numbers]]. 

Let $R$ be any Archimedean ordered field extension of the Cauchy real numbers. The analytic WLPO makes sense for any  [[Archimedean ordered local ring|Archimedean ordered]] [[local Artinian algebra|local Artinian $R$-algebra]] $A$ as well, where the relation $\lt$ is in general only a [[strict weak order]] instead of a [[pseudo-order]], the [[preorder]] $\geq$ is not a [[partial order]], and the equivalence relation $a \approx b$ derived from the preorder holds if and only if $a - b$ is [[nilpotent]]. In this case, the analytic WLPO for the Weil $R$-algebra $A$ says that the [[preorder]] on $A$ is a [[decidable relation]], or that the [[equivalence relation]] $a \approx b$ is a [[decidable relation]], or nilpotency is decidable, and the quotient of $A$ by its [[nilradical]] is the field of real numbers $R$ satisfying the analytic WLPO. 

## Properties

\begin{theorem}
The analytic WLPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$ implies the WLPO for [[natural numbers]]. 
\end{theorem}

\begin{proof}
Let $f$ be a function from the [[natural numbers]] to the [[boolean domain]]. Define the [[sequence]] $u$ on the rationals as 
$$u(n) = \sum_{x = 0}^k \frac{f(n)}{2^x}$$ 
This sequence is a [[Cauchy sequence]] with a modulus of continuity, so taking the limit of this Cauchy sequence yields a Cauchy real number $[u]$. The analytic WLPO on the Cauchy reals implies that $[u] = 0$ is decidable. Since $[u] = 0$ if and only if $f(n) = 0$ for all $n$, $[u] = 0$ is decidable if and only if "$f(n) = 0$ for all $n$" is decidable, the latter of which is the WLPO for natural numbers. Thus, analytic WLPO implies the WLPO for natural numbers.
\end{proof}

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

\begin{theorem}
The WLPO for [[natural numbers]] implies the analytic WLPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{theorem}

\begin{proof}
...
\end{proof}

\begin{lemma}
The WLPO for [[natural numbers]] is equivalent to the analytic WLPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{lemma}

Thus, one has a hierarchy of analytic weak limited principles of omniscience, where

* The (sequential-, modulated-, Cantor-, Cauchy-, $\mathbb{R}_C$-) analytic WLPO is the weakest and equivalent to the WLPO for the [[natural numbers]];

* The (Dedekind-, $\mathbb{R}_D$-)analytic WLPO is the strongest. 

* For any other Archimedean ordered field extension of the Cauchy real numbers $R$ which is neither equivalent to the Cauchy real numbers or the Dedekind real numbers, the $R$-analytic WLPO are intermediate in strength between the Cauchy-analytic WLPO and the Dedekind-analytic WLPO. 

Given an Archimedean ordered field extension $R$ of the [[Cauchy real numbers]], there are other statements related to the analytic WLPO:

* That every element of $R$ has a choice of [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) implies that the analytic $\mathrm{WPO}$ for $R$ holds. 

* [[countable set|Subcountability]] of $R$ implies the analytic $\mathrm{WLPO}$ because [[natural numbers]] have [[decidable equality]] and injections preserve and reflect decidable equality. 

## Models

* The analytic WLPO for both [[Cauchy real numbers]] and [[Dedekind real numbers]] fails in Johnstone's [[topological topos]].

* The analytic WLPO for [[Dedekind real numbers]] fails in the cohesive types of [[Mike Shulman]]'s [[real-cohesive homotopy type theory]], which model [[Euclidean-topological infinity-groupoids]]. However, the analytic WLPO for [[Cauchy real numbers]] holds in the cohesive types, since the analytic LPO for Cauchy real numbers hold and imply the analytic WLPO for Cauchy real numbers. 

## Related concepts

* [[weak limited principle of omniscience]]

* [[analytic LPO]]

* [[analytic LLPO]]

* [[analytic Markov's principle]]

## References

The analytic WLPO is mentioned in the following paper, although unfortunately it uses the phrase "analytic LPO" for what should really be the analytic *WLPO* (the reals have decidable equality). In addition, it makes the wrong statement that LPO is equivalent to Cauchy reals having decidable equality; it is WLPO which is equivalent to Cauchy reals having decidable equality (i.e. analytic WLPO for Cauchy reals), while LPO is equivalent to Cauchy reals having *[[decidable relation|decidable]] [[tight apartness relation|tight apartness]]*. 

* [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

[[!redirects analytic WLPO]]
[[!redirects analytic weak limited principle of omniscience]]
[[!redirects analytic weak limited principles of omniscience]]

[[!redirects analytic WLPO for Cauchy real numbers]]
[[!redirects analytic weak limited principle of omniscience for Cauchy real numbers]]
[[!redirects analytic weak limited principles of omniscience for Cauchy real numbers]]

[[!redirects Cauchy-analytic WLPO]]
[[!redirects Cauchy-analytic weak limited principle of omniscience]]
[[!redirects Cauchy-analytic weak limited principles of omniscience]]

[[!redirects Cauchy analytic WLPO]]
[[!redirects Cauchy analytic weak limited principle of omniscience]]
[[!redirects Cauchy analytic weak limited principles of omniscience]]

[[!redirects analytic WLPO for Dedekind real numbers]]
[[!redirects analytic weak limited principle of omniscience for Dedekind real numbers]]
[[!redirects analytic weak limited principles of omniscience for Dedekind real numbers]]

[[!redirects Dedekind-analytic WLPO]]
[[!redirects Dedekind-analytic weak limited principle of omniscience]]
[[!redirects Dedekind-analytic weak limited principles of omniscience]]

[[!redirects Dedekind analytic WLPO]]
[[!redirects Dedekind analytic weak limited principle of omniscience]]
[[!redirects Dedekind analytic weak limited principles of omniscience]]
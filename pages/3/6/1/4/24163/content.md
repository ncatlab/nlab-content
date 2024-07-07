
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

In [[real analysis]], there is a principle on the [[Cauchy real numbers]] which is equivalent in strength to [[Markov's principle]] for [[natural numbers]], and states that the [[tight apartness relation]] on the [[Cauchy real numbers]] is a [[stable relation]]. This principle can be generalised from the Cauchy real numbers to all notions of [[real numbers]], such as the [[Dedekind real numbers]], and is hence called the *analytic Markov's principle*. In [[classical mathematics]], all of these are implied by [[excluded middle]]; however, in [[neutral constructive mathematics]], the different analytic Markov's principles are different principles of different strength, because the Cauchy and Dedekind real numbers and any other notion of real numbers between the Cauchy and Dedekind real numbers cannot be proven to coincide. 

## Definition

There are many different notions of real numbers in [[constructive mathematics]]. What all these real numbers have in common are that they are an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$; i.e. there are unique [[ring homomorphisms]] of ordered fields
$$\mathbb{R}_C \hookrightarrow R \hookrightarrow \mathbb{R}_D$$
where $\mathbb{R}_D$ is the ordered field of [[Dedekind real numbers]] - the homomorphism into $\mathbb{R}_D$ always exists since $\mathbb{R}_D$ is the [[terminal object|terminal]] Archimedean ordered field. In general the ring homomorphisms are not provably [[isomorphisms]] unless the [[Dedekind real numbers]] and [[Cauchy real numbers]] coincide. Thus, there are many different notions of the analytic Markov's principle; the analytic Markov's principles are defined for each Archimedean ordered field extension of the Cauchy real numbers. 

\begin{definition}
Let $R$ be an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$. The __analytic Markov's principle__ for $R$ states that the [[pseudo-order]] on $R$ is a [[stable relation]], or equivalently, the [[tight apartness relation]] is a [[stable relation]], or equivalently. 
\end{definition}

**Warning**. Given an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]], the *analytic Markov's principle for $R$* is not to be confused with the *[[Markov's principle]] for $R$* - the latter is the statement that for every [[function]] $f$ from $R$ to the [[boolean domain]], the [[existential quantifier]] "for all elements $x$ in $R$, $f(x) = \mathrm{true}$" is [[stable proposition|stable]]. For $R$ the Cauchy real numbers, the analytic Markov's principle for the Cauchy real numbers is equivalent to the arkov's principle for the [[natural numbers]], while the arkov's principle for the [[Cauchy real numbers]] is much stronger than the arkov's principle for the [[natural numbers]]. 

\begin{theorem}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then the analytic Markov's principle for $R$ is equivalent to the statement which says that for all elements $x \in R$, $\neg (x \leq 0)$ implies $0 \lt x$, the definition of analytic Markov's principle in [Shulman 2018](#Shulman18). 
\end{theorem}

\begin{proof}
If we take $x = s - r$, this becomes $\neg (s - r \leq 0)$ implies $0 \lt s - r$, and by the order and arithmetic properties of the real numbers, this is equivalent to $\neg (s \leq r)$ implies $r \lt s$, which is the same as $\neg \neg (r \lt s)$ implies $r \lt s$, the analytic Markov's principle. 
\end{proof}

\begin{theorem}
The analytic Markov's principle for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$ implies Markov's principle for [[natural numbers]]. 
\end{theorem}

\begin{proof}
TBD...
\end{proof}

\begin{theorem}
Markov's principle for [[natural numbers]] implies the analytic Markov's principle for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{theorem}

\begin{proof}
TBD...
\end{proof}

\begin{lemma}
Markov's principle for [[natural numbers]] is equivalent to the analytic Markov's principle for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$. 
\end{lemma}

\begin{theorem}
Suppose that there are two Archimedean ordered fields $R$ and $R'$ such that both are [[field extensions]] of the [[Cauchy real numbers]] $\mathbb{R}_C$ and $R'$ is a [[field extension]] of $R$. Then, the analytic Markov's principle for $R'$ implies the analytic Markov's principle for $R$. 
\end{theorem}

\begin{proof}
TBD...
\end{proof}

\begin{lemma}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then, the analytic Markov's principle for $R$ implies Markov's principle for [[natural numbers]]. 
\end{lemma}

\begin{proof}
Since the field of Cauchy real numbers is a (trivial) field extension of itself, the analytic Markov's principle for $R$ implies the analytic Markov's principle for the Cauchy real numbers, which implies Markov's principle for the natural numbers. 
\end{proof}

Thus, one has a hierarchy of analytic Markov's principles of omniscience, where

* The (sequential-, modulated-, Cantor-, Cauchy-, $\mathbb{R}_C$-) analytic Markov's principle is the weakest and equivalent to Markov's principle for the [[natural numbers]];

* The (Dedekind-, $\mathbb{R}_D$-)analytic Markov's principle is the strongest. 

* For any other Archimedean ordered field extension of the Cauchy real numbers $R$ which is neither equivalent to the Cauchy real numbers or the Dedekind real numbers, the $R$-analytic Markov's principle are intermediate in strength between the Cauchy-analytic Markov's principle and the Dedekind-analytic Markov's principle. 

Let $R$ be any Archimedean ordered field extension of the Cauchy real numbers. The analytic Markov's principle makes sense for any  [[Archimedean ordered local ring|Archimedean ordered]] [[local Artinian algebra|local Artinian $R$-algebra]] $A$ as well, where the relation $\lt$ is in general only a [[strict weak order]] instead of a [[pseudo-order]], the [[preorder]] $\geq$ is not a [[partial order]], and the equivalence relation $a \approx b$ derived from the preorder holds if and only if $a - b$ is [[nilpotent]]. In this case, the analytic Markov's principle for the Weil $R$-algebra $A$ says that the [[apartness relation]] or [[strict weak order]] on $A$ is a [[stable relation]], and the quotient of $A$ by its [[nilradical]] is the field of real numbers $R$ satisfying the analytic Markov's principle. 

## Models

* The analytic Markov's principle for [[Dedekind real numbers]] holds in Johnstone's [[topological topos]].

* The analytic Markov's principle for [[Dedekind real numbers]] holds in the cohesive types of [[Mike Shulman]]'s [[real-cohesive homotopy type theory]], which model [[Euclidean-topological infinity-groupoids]]. 

## See also ##

* [[Markov's principle]]

* [[axiom of real cohesion]]

* [[intermediate value theorem]]

* [[analytic LPO]]

* [[analytic WLPO]]

* [[analytic LLPO]]

## References ##

* {#Shulman18} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

[[!redirects analytic MP]]
[[!redirects analytic Markov's principle]]
[[!redirects analytic Markov's principles]]

[[!redirects analytic MP for Cauchy real numbers]]
[[!redirects analytic Markov's principle for Cauchy real numbers]]
[[!redirects analytic Markov's principles for Cauchy real numbers]]

[[!redirects Cauchy-analytic MP]]
[[!redirects Cauchy-analytic Markov's principle]]
[[!redirects Cauchy-analytic Markov's principles]]

[[!redirects Cauchy analytic MP]]
[[!redirects Cauchy analytic Markov's principle]]
[[!redirects Cauchy analytic Markov's principles]]

[[!redirects analytic MP for Dedekind real numbers]]
[[!redirects analytic Markov's principle for Dedekind real numbers]]
[[!redirects analytic Markov's principles for Dedekind real numbers]]

[[!redirects Dedekind-analytic MP]]
[[!redirects Dedekind-analytic Markov's principle]]
[[!redirects Dedekind-analytic Markov's principles]]

[[!redirects Dedekind analytic MP]]
[[!redirects Dedekind analytic Markov's principle]]
[[!redirects Dedekind analytic Markov's principles]]
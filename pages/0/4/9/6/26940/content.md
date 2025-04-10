
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

In [[real analysis]], there is a principle on the [[Cauchy real numbers]] which is equivalent in strength to the [[limited principle of omniscience]] for [[natural numbers]], and states that the [[pseudo-order]] on the [[Cauchy real numbers]] is a [[decidable relation]], or that the [[Cauchy real numbers]] have [[decidable relation|decidable]] [[tight apartness relation|tight apartness]]. This principle can be generalised from the Cauchy real numbers to all notions of [[real numbers]], such as the [[Dedekind real numbers]], and is hence called the *analytic limited principle of omniscience*, or the *analytic LPO*. In [[classical mathematics]], all of these are implied by [[excluded middle]]; however, in [[neutral constructive mathematics]], the different analytic LPO are different principles of different strength, because the Cauchy and Dedekind real numbers and any other notion of real numbers between the Cauchy and Dedekind real numbers cannot be proven to coincide. 

## Definition

There are many different notions of real numbers in [[constructive mathematics]]. What all these real numbers have in common are that they are an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$; i.e. there are unique [[ring homomorphisms]] of ordered fields
$$\mathbb{R}_C \hookrightarrow R \hookrightarrow \mathbb{R}_D$$
where $\mathbb{R}_D$ is the ordered field of [[Dedekind real numbers]] - the homomorphism into $\mathbb{R}_D$ always exists since $\mathbb{R}_D$ is the [[terminal object|terminal]] Archimedean ordered field. In general the ring homomorphisms are not provably [[isomorphisms]] unless the [[Dedekind real numbers]] and [[Cauchy real numbers]] coincide. Thus, there are many different notions of the analytic limited principle of omniscience; the analytic limited principles of omniscience are defined for each Archimedean ordered field extension of the Cauchy real numbers. 

\begin{definition}
Let $R$ be an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] of the field of (sequential, modulated) [[Cauchy real numbers]] $\mathrm{R}_C$. The __analytic LPO__ for $R$ states that the usual [[apartness relation]] on $R$ [[decidable relation|decidable]] ($x \neq y$ or $x = y$), or equivalently __[[trichotomy]]__ for $R$ ($x \lt y$ or $x = y$ or $x \gt y$), or equivalently, that $R$ is a [[discrete field]].
\end{definition}

**Warning**. Given an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]], the *analytic limited principle of omniscience for $R$* is not to be confused with the *[[limited principle of omniscience]] for $R$* - the latter is the statement that for every [[function]] $f$ from $R$ to the [[boolean domain]], either there exists an element $x$ in $R$ such that $f(x) = 1$, or for all elements $x$ in $R$, $f(x) = 0$. For $R$ the Cauchy real numbers, the analytic LPO for the Cauchy real numbers is equivalent to the LPO for the [[natural numbers]], while the LPO for the [[Cauchy real numbers]] is much stronger than the LPO for the [[natural numbers]]. 

Let $R$ be any Archimedean ordered field extension of the Cauchy real numbers. The analytic LPO also makes sense for any [[Archimedean ordered local ring|Archimedean ordered]] [[local Artinian algebra|local Artinian $R$-algebra]] $A$ as well, where the relation $\lt$ is in general only a [[strict weak order]] instead of a [[pseudo-order]], the [[preorder]] $\geq$ is not a [[partial order]], and the equivalence relation $a \approx b$ derived from the preorder holds if and only if $a - b$ is [[nilpotent]]. In this case, the analytic LPO for the Weil $R$-algebra $A$ says that the [[strict weak order]] on $A$ is a [[decidable relation]], or that the [[apartness relation]] $a \# b$ is a [[decidable relation]], or invertibility is decidable, and the quotient of $A$ by its [[nilradical]] is the field of real numbers $R$ satisfying the analytic LPO. 

## Properties

\begin{theorem}
The analytic LPO for the (sequential, modulated) [[Cauchy real numbers]] $\mathbb{R}_C$ implies the LPO for [[natural numbers]]. 
\end{theorem}

\begin{proof}
Let $f$ be a function from the [[natural numbers]] to the [[boolean domain]]. Define the [[sequence]] $u$ on the rationals as 
$$u(n) = \sum_{x = 0}^k \frac{f(n)}{2^x}$$ 
This sequence is a [[Cauchy sequence]] with a modulus of continuity, so taking the limit of this Cauchy sequence yields a Cauchy real number $[u]$. The analytic LPO on the Cauchy reals states that either $[u] \# 0$ or $[u] = 0$. In the former case, $[u] \gt \frac{1}{2^k}$ for some natural number $k$ so there exists an $n$ such that $f(n) = 1$, and in the latter case, $f(n) = 0$ for all $n$. Thus, the LPO for natural numbers hold. 
\end{proof}

\begin{theorem}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then the analytic LPO for $R$ implies that $R$ is isomorphic to $\mathbb{R}_C$
\end{theorem}

\begin{proof}
Every [[Archimedean ordered field]] is a subfield of the [[Dedekind real numbers]], which means that by [[coercion]] one can consider the elements of any Archimedean ordered field to be Dedekind real numbers, which are Dedekind cuts. Theorem 10.6.3 of [Booij 2020](#Booij20) says that any Dedekind real number (i.e. Dedekind cut) for which there exists a [[locator]] is a [[Cauchy real number]]. This implies that given an Archimedean ordered field $R$, if for every element in $R$ there exists a [[locator]], then every element in $R$ is a Cauchy real number, and $R$ is a [[subfield]] of the Cauchy real numbers. If $R$ is also a field extension of the [[Cauchy real numbers]], then $R$ is [[isomorphic]] to the Cauchy real numbers, since the [[Cantor-Schroeder-Bernstein theorem]] holds for [[Archimedean ordered fields]] and [[ring homomorphisms]] in the category of Archimedean ordered fields. 

The analytic LPO implies that corollary 11.4.3 of [UFP 2013](#UFP13) can be proven: If analytic LPO holds then "$(x \lt y) \to (x \lt z) + (z \lt y)$ can be proved: either $x \lt z$ or $\neg(x \lt z)$. In the former case we are done, while in the latter we get $z \lt y$ because $z \leq x \lt y$." Therefore, we get a [[locator]] for every element of $R$, which then implies that $R$ is isomorphic to the Cauchy real numbers. 
\end{proof}

\begin{theorem}
Suppose that there are two Archimedean ordered fields $R$ and $R'$ such that both are [[field extensions]] of the [[Cauchy real numbers]] $\mathbb{R}_C$ and $R'$ is a [[field extension]] of $R$. Then, the analytic LPO for $R'$ implies the analytic LPO for $R$. 
\end{theorem}

\begin{proof}
Analytic LPO for $R'$ implies that $R'$ is [[isomorphic]] to the [[Cauchy real numbers]], which implies that any subfield of $R'$ which is a field extension of the Cauchy real numbers is isomorphic to $R'$, since the [[Cantor-Schroeder-Bernstein theorem]] holds for [[Archimedean ordered fields]] and [[ring homomorphisms]] in the category of Archimedean ordered fields. Since this is true of $R$, this implies that the analytic LPO for $R$ also holds, since $R'$ and $R$ are isomorphic fields. 
\end{proof}

\begin{lemma}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then, the analytic LPO for $R$ implies the LPO for [[natural numbers]]. 
\end{lemma}

\begin{proof}
Since the field of Cauchy real numbers is a (trivial) field extension of itself, the analytic LPO for $R$ implies the analytic LPO for the Cauchy real numbers, which implies the LPO for the natural numbers. 
\end{proof}

Let $\Sigma$ be the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]]. It is a sub-$\sigma$-frame of the [[frame of truth values]]. One can construct a set of Dedekind real numbers $\mathrm{R}_\Sigma$ out of Dedekind cuts valued in the initial $\sigma$-frame $\Sigma \subseteq \Omega$ (see section 11.2 of [UFP 2013](#UFP13)), where then one has ring homomorphisms
$$\mathrm{R}_C \hookrightarrow \mathrm{R}_\Sigma \hookrightarrow \mathrm{R}_D$$

\begin{theorem}
The LPO for natural numbers is equivalent to the [[boolean domain]] $\mathbb{2}$ being the initial $\sigma$-frame $\Sigma \coloneqq \mathbb{2}$. 
\end{theorem}

\begin{proof}
By definition of initial $\sigma$-frame, there is at most one $\sigma$-frame homomorphism from the [[boolean domain]] $\mathbb{2}$ to the initial $\sigma$-frame $\Sigma$, which is given by the unique [[lattice]] homomorphism from $\mathbb{2}$ to $\Sigma$ since $\mathbb{2}$ is the initial [[distributive lattice]]. 

The LPO for natural numbers is equivalent to the condition that $\mathbb{2}$ has $\mathbb{N}$-indexed joins such that for all sequences $s:\mathbb{N} \to \mathbb{2}$, $\bigvee_{n \in \mathbb{N}} s(n) = 1$ implies that there exists an $n \in \mathbb{N}$ such that $s(n) = 1$. This is only the case if the lattice homomorphism from $\mathbb{2}$ to $\Sigma$ is a $\sigma$-frame homomorphism. 
\end{proof}

Thus, one can use the decidable Dedekind cuts $\mathbb{2}^\mathbb{Q} \times \mathbb{2}^\mathbb{Q}$ to construct the Dedekind real numbers, since $\Sigma \cong \mathbb{2}$ is the initial $\sigma$-frame. 

\begin{theorem}
The LPO for natural numbers implies the analytic LPO for subset of Dedekind real numbers $\mathrm{R}_\Sigma \subseteq \mathbb{R}_D$ constructed out of Dedekind cuts in valued in the initial $\sigma$-frame $\Sigma \subseteq \Omega$.
\end{theorem}

\begin{proof}
LPO for the natural numbers implies that for each rational number $q$, the left and right Dedekind cuts for an element $x$ of $\mathrm{R}_\Sigma$, evaluated at $q$, $L_x(q)$ and $R_x(q)$, are both decidable propositions. In addition, LPO for the natural numbers implies that any [[existential quantification]] of a decidable predicate  over the rational numbers is itself a decidable proposition. The [[pseudo-order]] relation $\lt$ on $\mathbb{R}_\Sigma$ is defined as 
$$x \lt y \coloneqq \exists q \in \mathbb{Q}.L_x(q) \wedge R_y(q)$$
Since $L_x(q)$ and $R_y(q)$ are both decidable, the conjunction is also decidable, and so is the existential quantifier by LPO for the natural numbers, and by definition the strict order on $\mathrm{R}_\Sigma$, which is the analytic LPO for $\mathrm{R}_\Sigma$. 
\end{proof}

\begin{theorem}
The LPO for natural numbers, the $\mathbb{R}_C$-analytic LPO, and the $\mathbb{R}_\Sigma$-analytic LPO are equivalent to each other. 
\end{theorem}

\begin{proof}
We showed that the the $\mathbb{R}_C$-analytic LPO implies the LPO for natural numbers, that the $\mathbb{R}_\Sigma$-analytic LPO implies the $\mathbb{R}_C$-analytic LPO, and the LPO for natural numbers implies the $\mathbb{R}_\Sigma$-analytic LPO. By transitivity of implication, the converses also hold, so all three statements are equivalent to each other. 
\end{proof}

\begin{theorem}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then the analytic LPO for $R$ implies that $R$ is equivalent to $\mathbb{R}_C$ and $\mathbb{R}_\Sigma$.
\end{theorem}

\begin{proof}
Analytic LPO for $R$ implies the LPO for natural numbers, which implies that $\mathbb{R}_C$ is equivalent to $\mathbb{R}_\Sigma$. Theorem 11.2.14 in [UFP 2013](#UFP13) states that given the initial $\sigma$-frame $\Sigma$, every Archimedean ordered field which is admissible for $\Sigma$ is a subfield of $\mathbb{R}_\Sigma$. The LPO for natural numbers implies the initial $\sigma$-frame is the boolean domain, which means that analytic LPO for $R$ implies that $R$ is admissible for the boolean domain, and hence a subfield of $\mathbb{R}_\Sigma$. This means that $R$ coincides with both $\mathbb{R}_C$ and $\mathbb{R}_\Sigma$, since the [[Cantor-Schroeder-Bernstein theorem]] holds for [[Archimedean ordered fields]] and [[ring homomorphisms]]. 
\end{proof}

\begin{lemma}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then the analytic LPO for $R$ implies that $R$ is [[sequentially Cauchy complete]]. 
\end{lemma}

\begin{proof}
Analytic LPO for $R$ implies that $R$ is equivalent to $\mathbb{R}_\Sigma$. Since $\mathbb{R}_\Sigma$ is constructed out of Dedekind cuts (valued in the initial $\sigma$-frame $\Sigma$), theorem 11.2.12 and corollary 11.2.13 of [UFP 2013](#UFP13) states that $\mathbb{R}_\Sigma$ is sequentially Cauchy complete, which then implies that $R$ is sequentially Cauchy complete. 
\end{proof}

Finally, let $\mathbb{R}_H$ be the [[HoTT book real numbers]], which are the initial [[sequentially Cauchy complete space|sequentially Cauchy complete]] [[Archimedean ordered field]]. Then, 

\begin{theorem}
The LPO for natural numbers and the analytic LPO for $\mathbb{R}_H$ are equivalent to each other. 
\end{theorem}

\begin{proof}
There is a ring homomorphism $\mathbb{R}_H \hookrightarrow \mathbb{R}_\Sigma$ because $\mathbb{R}_\Sigma$ is Cauchy complete and $\mathbb{R}_H$ is initial in the category of Cauchy complete Archimedean ordered fields, and there is a ring homomorphism $\mathbb{R}_C \hookrightarrow \mathbb{R}_H$ because the rational numbers are a subset of $\mathbb{R}_H$, and $\mathbb{R}_C$ is the limit of Cauchy sequences of rational numbers (with modulus), while $\mathbb{R}_H$ is the limit of Cauchy sequences of elements of $\mathbb{R}_H$, implying that $\mathbb{R}_C$ embeds in $\mathbb{R}_H$. 

Since the LPO for natural numbers is equivalent to the analytic LPO for $\mathrm{R}_\Sigma$, this in turn implies that $\mathrm{R}_C$ and $\mathrm{R}_\Sigma$ are isomorphic fields, which implies that $\mathbb{R}_H$ is isomorphic to $\mathrm{R}_\Sigma$, since the [[Cantor-Schroeder-Bernstein theorem]] holds for [[Archimedean ordered fields]] and [[ring homomorphisms]] in the category of Archimedean ordered fields. Thus, the analytic LPO for $\mathrm{R}_\Sigma$ is equivalent to the analytic LPO for $\mathrm{R}_H$ and equivalent to the LPO for natural numbers. 
\end{proof}

Thus, one has a hierarchy of analytic limited principles of omniscience, where

* The analytic LPO for the (sequential, modulated) [[Cauchy real numbers]], for the [[Escardo-Simpson real numbers]]/[[HoTT book real numbers]], and for the subset of the Dedekind real numbers whose Dedekind cuts are valued in the initial $\sigma$-frame, are all the weakest and equivalent to the LPO for the [[natural numbers]];

* The analytic LPO for the Dedekind real numbers is the strongest. 

* For any other Archimedean ordered field extension of the Cauchy real numbers $R$ which is neither equivalent to the Cauchy real numbers or the Dedekind real numbers, the analytic LPO for $R$ are intermediate in strength between the Cauchy-analytic LPO and the Dedekind-analytic LPO. 

\begin{theorem}
Given a [[sigma-frame|$\sigma$-subframe]] $\Sigma$ of the $\sigma$-frame of [[truth values]], that the $\Sigma$-[[Dedekind completion]] of every [[Archimedean ordered integral domain]] using of Dedekind cuts valued in $\Sigma$ is [[isomorphic]] to either the [[integers]] $\mathbb{Z}$ or the $\Sigma$-[[Dedekind real numbers]] $\mathbb{R}_\Sigma$ is equivalent to the analytic $\mathrm{LPO}$ for $\mathbb{R}_\Sigma$. 
\end{theorem}

\begin{proof}
Consider the Archimedean ordered integral domain $R$ with an arbitrary element $x \in R$. The $\Sigma$-Dedekind completion of $R$ is the integers if and only if $x$ is equal to an integer, and the $\Sigma$-Dedekind completion of $R$ is the $\Sigma$-Dedekind real numbers if and only if $x$ is [[tight apartness|apart from]] an integer. However, $x$ is equal to an integer or apart from an integer for all $x \in R$ if and only if $R$ is a [[discrete integral domain]], and the claim that every Archimedean ordered integral domain is discrete is equivalent to the analytic $\mathrm{LPO}$ for the $\Sigma$-Dedekind real numbers. 
\end{proof}

## Related statements

Given an Archimedean ordered field extension $R$ of the [[Cauchy real numbers]], there are other statements related to the analytic LPO for $R$:

* That the [[floor]] and [[ceiling]] [[partial functions]] are [[total functions]] on $R$ is equivalent to the analytic LPO for $R$. 

* That $R$ coincides with the [[prealgebra real numbers]] is equivalent to the analytic LPO for $R$. 

* The analytic $\mathrm{LPO}$ for $R$ implies the [[fundamental theorem of algebra]] for $R$. 

* That every [[apartness relation]] on a [[set]] is [[decidable relation|decidable]] implies that analytic LPO for $R$:

$$((\forall x.\neg (x \# x)) \wedge (\forall x, y.(x \# y) \Rightarrow (y \# x)) \wedge (\forall x, y, z.(x \# y) \wedge (y \# z) \Rightarrow (x \# z))) \Rightarrow 
(\forall x, y.(x \# y) \vee \neg (x \# y))$$

## Models

* The analytic LPO for both [[Cauchy real numbers]] and [[Dedekind real numbers]] fails in Johnstone's [[topological topos]], since it contradicts [[Brouwer's continuity principle]] which holds for both the [[Cauchy real numbers]] and the [[Dedekind real numbers]].

* The analytic LPO for [[Dedekind real numbers]] fails in the cohesive types of [[Mike Shulman]]'s [[real-cohesive homotopy type theory]], which model [[Euclidean-topological infinity-groupoids]], since it contradicts [[Brouwer's continuity principle]] which holds for the [[Dedekind real numbers]]. However, the analytic LPO for [[Cauchy real numbers]] holds in the cohesive types, since the LPO for natural numbers hold and is equivalent to the analytic LPO for Cauchy real numbers. 

## Related concepts

* [[limited principle of omniscience]]

* [[axiom of real cohesion]]

* [[Brouwer's continuity principle]]

* [[intermediate value theorem]]

* [[analytic WLPO]]

* [[analytic LLPO]]

* [[analytic Markov's principle]]

## References

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* {#Booij20} [[Auke Booij]], *Analysis in Univalent Type Theory* (2020) &lbrack;[etheses:10411](http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf), [[Booij-AnalysisInUF.pdf:file]]&rbrack;

* {#BirchfieldSwan24} [[Madeleine Birchfield]], [[Andrew Swan]] (2024) on Category Theory Zulip, [LPO and sigma-frame structure on booleans](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/LPO.20and.20sigma-frame.20structure.20on.20booleans)

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

The phrase "analytic LPO" is mentioned in the following paper, although in that paper it actually refer to the [[analytic WLPO]] (the reals have decidable equality) instead of the actual analytic LPO (the reals have decidable tight apartness). In addition, it makes the wrong statement that LPO is equivalent to Cauchy reals having decidable equality; it is WLPO which is equivalent to Cauchy reals having decidable equality (i.e. analytic WLPO for Cauchy reals), while LPO is equivalent to Cauchy reals having *[[decidable relation|decidable]] [[tight apartness relation|tight apartness]]*. 

* [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

[[!redirects analytic LPO]]
[[!redirects analytic limited principle of omniscience]]
[[!redirects analytic limited principles of omniscience]]

[[!redirects analytic LPO for Cauchy real numbers]]
[[!redirects analytic limited principle of omniscience for Cauchy real numbers]]
[[!redirects analytic limited principles of omniscience for Cauchy real numbers]]

[[!redirects Cauchy-analytic LPO]]
[[!redirects Cauchy-analytic limited principle of omniscience]]
[[!redirects Cauchy-analytic limited principles of omniscience]]

[[!redirects Cauchy analytic LPO]]
[[!redirects Cauchy analytic limited principle of omniscience]]
[[!redirects Cauchy analytic limited principles of omniscience]]

[[!redirects analytic LPO for Dedekind real numbers]]
[[!redirects analytic limited principle of omniscience for Dedekind real numbers]]
[[!redirects analytic limited principles of omniscience for Dedekind real numbers]]

[[!redirects Dedekind-analytic LPO]]
[[!redirects Dedekind-analytic limited principle of omniscience]]
[[!redirects Dedekind-analytic limited principles of omniscience]]

[[!redirects Dedekind analytic LPO]]
[[!redirects Dedekind analytic limited principle of omniscience]]
[[!redirects Dedekind analytic limited principles of omniscience]]
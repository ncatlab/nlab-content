
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

**Warning**. Given an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] $R$ of the field of (sequential, modulated) [[Cauchy real numbers]], the *analytic limited principle of omniscience for $R$* is not to be confused with the *[[limited principle of omniscience]] for $R$* - the latter is the statement that $R$ is an [[exhaustible set]]: for every [[function]] $f$ from $R$ to the [[boolean domain]], either there exists an element $x$ in $R$ such that $f(x) = 1$, or for all elements $x$ in $R$, $f(x) = 0$. For $R$ the Cauchy real numbers, the analytic LPO for the Cauchy real numbers is equivalent to the LPO for the [[natural numbers]], while the LPO for the [[Cauchy real numbers]] is much stronger than the LPO for the [[natural numbers]]. 

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
The analytic LPO implies that the [[Archimedean ordered field]] $R$ is [[admissible Archimedean ordered field|admissible]] for the [[booleans]], and thus admissible for the set of [[semi-decidable propositions]]. Since the [[Cauchy real numbers]] $\mathbb{R}_C$ are the [[terminal object|terminal]] [[Archimedean ordered field]] that is admissible for the set of [[semi-decidable propositions]], $R$ is isomorphic with the [[Cauchy real numbers]] $\mathbb{R}_C$. 
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

Let $\Sigma \subseteq \Omega$ be the set of [[Sierpinski semi-decidable truth values]]. One can construct a set of Dedekind real numbers $\mathrm{R}_\Sigma$ out of Dedekind cuts valued in Sierpinski semi-decidable truth values (see [Univalent Foundations Project 2013](#UFP13), [Gilbert 2017](#Gilbert17), [Bidlingmaier, Faissole & Spitters 2019](#BFS19)), where then one has subset inclusions
$$\mathrm{R}_C \subseteq \mathrm{R}_\Sigma \subseteq \mathrm{R}_D$$

\begin{theorem}
The LPO for natural numbers is equivalent to the [[boolean domain]] $\mathbb{2}$ being the set of [[Sierpinski semi-decidable truth values]] $\Sigma$. 
\end{theorem}

\begin{proof}
[[Sierpinski semi-decidable truth values]] are closed under [[existential quantification]] over the [[natural numbers]]. If the set $\Sigma$ of Sierpinski semi-decidable truth values is equivalent to the [[boolean domain]] $\mathbb{2}$, then the booleans are closed under existential quantification over the natural numbers, which is precisely the LPO for natural numbers. 
\end{proof}

Thus, one can use the decidable Dedekind cuts $\mathbb{2}^\mathbb{Q} \times \mathbb{2}^\mathbb{Q}$ to construct the Dedekind real numbers, since $\Sigma \cong \mathbb{2}$ is a sub-$\sigma$-frame of the $\sigma$-frame of truth values $\Omega$. 

\begin{theorem}
The LPO for natural numbers implies the analytic LPO for subset of Dedekind real numbers $\mathrm{R}_\Sigma \subseteq \mathbb{R}_D$ constructed out of Dedekind cuts in valued Sierpinski semi-decidable truth values $\Sigma \subseteq \Omega$.
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
Analytic LPO for $R$ implies the LPO for natural numbers, which implies that $\mathbb{R}_C$ is equivalent to $\mathbb{R}_\Sigma$. The set of Sierpinski semi-decidable truth values is a $\sigma$-subframe of the [[frame of truth values]]. Theorem 11.2.14 in [UFP 2013](#UFP13) states that given the set of Sierpinski semi-decidable truth values $\Sigma$, every Archimedean ordered field which is admissible for $\Sigma$ is a subfield of $\mathbb{R}_\Sigma$. The LPO for natural numbers implies the set of Sierpinski semi-decidable truth values is the boolean domain, which means that analytic LPO for $R$ implies that $R$ is admissible for the boolean domain, and hence a subfield of $\mathbb{R}_\Sigma$. This means that $R$ coincides with both $\mathbb{R}_C$ and $\mathbb{R}_\Sigma$, since the [[Cantor-Schroeder-Bernstein theorem]] holds for [[Archimedean ordered fields]] and [[ring homomorphisms]]. 
\end{proof}

\begin{lemma}
Suppose that there is an Archimedean ordered field $R$ which is a [[field extension]] of the [[Cauchy real numbers]] $\mathbb{R}_C$. Then the analytic LPO for $R$ implies that $R$ is [[sequentially Cauchy complete]]. 
\end{lemma}

\begin{proof}
Analytic LPO for $R$ implies that $R$ is equivalent to $\mathbb{R}_\Sigma$. Since $\mathbb{R}_\Sigma$ is constructed out of Dedekind cuts (valued in the set of Sierpinski semi-decidable truth values $\Sigma$), theorem 11.2.12 and corollary 11.2.13 of [UFP 2013](#UFP13) states that $\mathbb{R}_\Sigma$ is sequentially Cauchy complete, which then implies that $R$ is sequentially Cauchy complete. 
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

* The analytic LPO for the (sequential, modulated) [[Cauchy real numbers]], for the [[Escardo-Simpson real numbers]]/[[HoTT book real numbers]], and for the subset of the Dedekind real numbers whose Dedekind cuts are valued in the set of Sierpinski semi-decidable truth values $\Sigma$, are all the weakest and equivalent to the LPO for the [[natural numbers]];

* The analytic LPO for the Dedekind real numbers is the strongest. 

* For any other Archimedean ordered field extension of the Cauchy real numbers $R$ which is neither equivalent to the Cauchy real numbers or the Dedekind real numbers, the analytic LPO for $R$ are intermediate in strength between the Cauchy-analytic LPO and the Dedekind-analytic LPO. 

\begin{theorem}
Given a [[sigma-frame|$\sigma$-subframe]] $\Sigma$ of the $\sigma$-frame of [[truth values]], that the $\Sigma$-[[Dedekind completion]] of every [[Archimedean ordered integral domain]] using of Dedekind cuts valued in $\Sigma$ is [[isomorphic]] to either the [[integers]] $\mathbb{Z}$ or the $\Sigma$-[[Dedekind real numbers]] $\mathbb{R}_\Sigma$ is equivalent to the analytic $\mathrm{LPO}$ for $\mathbb{R}_\Sigma$. 
\end{theorem}

\begin{proof}
Consider the Archimedean ordered integral domain $R$ with an arbitrary element $x \in R$. The $\Sigma$-Dedekind completion of $R$ is the integers if and only if $x$ is equal to an integer, and the $\Sigma$-Dedekind completion of $R$ is the $\Sigma$-Dedekind real numbers if and only if $x$ is [[tight apartness|apart from]] an integer. However, $x$ is equal to an integer or apart from an integer for all $x \in R$ if and only if $R$ is a [[discrete integral domain]], and the claim that every Archimedean ordered integral domain is discrete is equivalent to the analytic $\mathrm{LPO}$ for the $\Sigma$-Dedekind real numbers. 
\end{proof}

\begin{theorem}
The [[choiceless LPO]] as defined in [King 2024](#King24) implies the analytic LPO for any field of real numbers $R$. 
\end{theorem}

\begin{proof}
For all real numbers $r \in R$ and natural numbers $n \in \mathbb{N}$, let the predicate $P(r, n)$ be defined as the predicate $P(r, n) \coloneqq r \gt 0 \vee r \lt 0$, which is constant on the natural numbers, and let the predicate $Q(r, n)$ be defined as the predicate $Q(r, n) \coloneqq r \gt -\frac{1}{2^n} \wedge r \lt \frac{1}{2^n}$. One can show that for all real numbers $r \in R$ and natural numbers $n \in \mathbb{N}$, we have $P(r, n) \vee Q(r, n)$. Then the [[choiceless LPO]] implies that for all real numbers $r \in R$, we have 
$$(\exists n \in \mathbb{N}.r \gt 0 \vee r \lt 0) \vee (\forall n \in \mathbb{N}.r \gt -\frac{1}{2^n} \wedge r \lt \frac{1}{2^n})$$
Since $\forall n \in \mathbb{N}.r \gt -\frac{1}{2^n} \wedge r \lt \frac{1}{2^n}$ is equivalent to $r = 0$ and $\exists n \in \mathbb{N}.r \gt 0 \vee r \lt 0$ is equivalent to $r \gt 0 \vee r \lt 0$ for all real numbers $r \in R$, we have 
$$(r \gt 0 \vee r \lt 0) \vee (r = 0)$$ 
which is precisely analytic Markov's principle for the field of real numbers $R$. 
\end{proof}

\begin{lemma}
The [[choiceless LPO]] as defined in [King 2024](#King24) implies that the [[Dedekind real numbers]] and [[Cauchy real numbers]] coincide. 
\end{lemma}

\begin{proof}
The choiceless LPO implies the analytic LPO for both Dedekind real numbers and Cauchy real numbers, which implies that they coincide with each other. 
\end{proof}

## Related statements

Given an Archimedean ordered field extension $R$ of the [[Cauchy real numbers]], there are other statements related to the analytic LPO for $R$:

* That the [[floor]] and [[ceiling]] [[partial functions]] are [[total functions]] on $R$ is equivalent to the analytic LPO for $R$. 

* That $R$ coincides with the union of [[rational numbers]] and strictly [[irrational numbers]] (defined as non-repeating infinite [[radix notation|sequence of digits]]) is equivalent to the analytic LPO for $R$. 

* The analytic $\mathrm{LPO}$ for $R$ implies the [[fundamental theorem of algebra]] for $R$. 

* That every [[apartness relation]] on a [[set]] is [[decidable relation|decidable]] implies that analytic LPO for $R$:

$$((\forall x.\neg (x \# x)) \wedge (\forall x, y.(x \# y) \Rightarrow (y \# x)) \wedge (\forall x, y, z.(x \# y) \wedge (y \# z) \Rightarrow (x \# z))) \Rightarrow 
(\forall x, y.(x \# y) \vee \neg (x \# y))$$

## Models

* The analytic LPO for both [[Cauchy real numbers]] and [[Dedekind real numbers]] fails in Johnstone's [[topological topos]], since it contradicts [[Brouwer's continuity principle]] which holds for both the [[Cauchy real numbers]] and the [[Dedekind real numbers]].

* The analytic LPO for [[Dedekind real numbers]] fails in the cohesive types of [[Mike Shulman]]'s [[real-cohesive homotopy type theory]], which model [[Euclidean-topological infinity-groupoids]], since it contradicts [[Brouwer's continuity principle]] which holds for the [[Dedekind real numbers]]. However, the analytic LPO for [[Cauchy real numbers]] holds in the cohesive types, since the LPO for natural numbers hold and is equivalent to the analytic LPO for Cauchy real numbers. 

## Related concepts

* [[resizing axiom]]

* [[limited principle of omniscience]]

* [[axiom of real cohesion]]

* [[Brouwer's continuity principle]]

* [[intermediate value theorem]]

* [[analytic WLPO]]

* [[analytic LLPO]]

* [[analytic Markov's principle]]

## References

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* {#Gilbert17} Gaëtan Gilbert. *Formalising real numbers in homotopy type theory.* In CPP’17, Proceedings of the 6th ACM SIGPLAN Conference on Certified Programs and Proofs, pages 112–124, 2017. &lbrack;[doi:10.1145/3018610.3018614](https://doi.org/10.1145/3018610.3018614)&rbrack;.

* {#BFS19} Martin E. Bidlingmaier, Florian Faissole, [[Bas Spitters]], *Synthetic topology in Homotopy Type Theory for probabilistic programming*. Mathematical Structures in Computer Science, 2021;31(10):1301-1329. &lbrack;[doi:10.1017/S0960129521000165](https://doi.org/10.1017/S0960129521000165), [arXiv:1912.07339](https://arxiv.org/abs/1912.07339)&rbrack;

* {#Booij20} [[Auke Booij]], *Analysis in Univalent Type Theory* (2020) &lbrack;[etheses:10411](http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf), [[Booij-AnalysisInUF.pdf:file]]&rbrack;

* {#BirchfieldSwan24} [[Madeleine Birchfield]], [[Andrew Swan]] (2024) on Category Theory Zulip, [LPO and sigma-frame structure on booleans](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/LPO.20and.20sigma-frame.20structure.20on.20booleans)

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

* {#King24} Christopher King, *What are these generalizations of the principles of omniscience called?*, MathOverflow, 15 February 2024. ([web](https://mathoverflow.net/questions/464247/what-are-these-generalizations-of-the-principles-of-omniscience-called))

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
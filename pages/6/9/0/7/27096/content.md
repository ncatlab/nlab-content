
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Definition

### In cohesive homotopy type theory

The **axiom of punctual cohesion** or **axiom C1** states that there is a [[pointed type]] $I$ with designated point $p:I$ such that every crisp type $T$ is discrete if and only if every function from $I$ into $\mathrm{Disc}(T)$ is a [[constant function]]. $\mathrm{Disc}$ is a [[modality]] which takes types in the crisp mode to its corresponding discrete type in the cohesive mode, and a discrete type $A$ in the cohesive mode is one for which the canonical function $\flat(-):A \to \flat A$ is an [[equivalence of types]]. 

[Shulman 2018](#Shulman18) showed that axiom C1 implies [[axiom C0]], which implies that every function from $I$ into a discrete type $A$ is a constant function; conversely, if every function from $I$ to a discrete type $A$ is constant, then it holds for the discrete types which are in the image of the $\mathrm{Disc}$ modality. 

## Properties

\begin{theorem}
The [[type of booleans]] $\mathbb{2}$ is discrete.
\end{theorem}

\begin{proof}
Theorem 6.19 of [Shulman 18](#Shulman18) says that the [[unit type]] is crisply discrete, and theorem 6.21 of [Shulman 18](#Shulman18) says that the [[sum type]] of two crisply discrete types is itself crisply discrete. Since the type of booleans is the [[sum type]] of two copies of the unit type, the type of booleans is crisply discrete, thus discrete.  
\end{proof}

\begin{theorem}
The natural numbers $\mathbb{N}$ are discrete.
\end{theorem}

\begin{proof}
Theorem 6.21 of [Shulman 18](#Shulman18) says that the [[natural numbers]] is crisply discrete, thus discrete.  
\end{proof}

\begin{theorem}
Assuming crisp [[excluded middle]] and punctual cohesion, the [[limited principle of omniscience]] holds. 
\end{theorem}

\begin{proof}
Since the [[natural numbers]] $\mathbb{N}$ and the [[type of booleans]] $\mathbb{2}$ are discrete, the function type $\mathbb{N} \to \mathbb{2}$ is also discrete by [[axiom C0]], so we may assume that any function $f:\mathbb{N} \to \mathbb{2}$ is crisp. Then the [[existential quantifier]] on $\exists x:A.f(x) = 1$
is crisp, so by crisp excluded middle, we have $\exists x:A.f(x) = 1$ or $\neg \exists x:A.f(x) = 1$. But $\neg \exists x:A.f(x) = 1$ is just $\forall x:A.f(x) = 0$, so we are done. 
\end{proof}

\begin{theorem}
Assuming crisp [[excluded middle]] and punctual cohesion, the [[Cauchy real numbers]] $\mathbb{R}_C$, [[HoTT book real numbers]] $\mathbb{R}_H$, the $\Sigma$-[[Dedekind real numbers]] $\mathbb{R}_\Sigma$ constructed using Dedekind cuts valued in the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]] $\Sigma$, and the [[flat modality]] of the [[terminal object|terminal]] [[Archimedean ordered field]] $\flat \mathbb{R}$ are all isomorphic [[Archimedean ordered fields]] in the cohesive mode. 
\end{theorem}

\begin{proof}
The [[limited principle of omniscience]] implies that for each rational number $q$, the left and right Dedekind cuts for an element $x$ of $\mathrm{R}_\Sigma$, evaluated at $q$, $L_x(q)$ and $R_x(q)$, are both decidable propositions. In addition, limited principle of omniscience implies that any [[existential quantification]] of a decidable predicate  over the rational numbers is itself a decidable proposition. The [[pseudo-order]] relation $\lt$ on $\mathbb{R}_\Sigma$ is defined as 
$$x \lt y \coloneqq \exists q \in \mathbb{Q}.L_x(q) \wedge R_y(q)$$
Since $L_x(q)$ and $R_y(q)$ are both decidable, the conjunction is also decidable, and so is the existential quantifier by LPO for the natural numbers, and by definition the strict order on $\mathrm{R}_\Sigma$, which is the [[analytic LPO]] for $\mathrm{R}_\Sigma$. 

The analytic LPO for $\mathrm{R}_\Sigma$ implies that every element $x$ in $\mathrm{R}_\Sigma$ has a [[locator]] by corollary 11.4.3 of the [[HoTT book]]. This then implies that $\mathrm{R}_\Sigma$ is isomorphic to $\mathbb{R}_C$ by corollary 11.4.1 of the [[HoTT book]], and since the [[Cantor-Schroeder-Bernstein theorem]] holds for [[Archimedean ordered fields]] and [[ring homomorphisms]] in the category of Archimedean ordered fields, $\mathrm{R}_H$ is also isomorphic to both $\mathrm{R}_\Sigma$ and $\mathbb{R}_C$. 

Finally, every element of $\flat \mathbb{R}$ can be assumed to be a crisp element, and crisp excluded middle implies that every element of $\flat \mathbb{R}$ has a locator, and is thus a crisp [[Cauchy real number]]. Thus, we have $\flat \mathbb{R} \simeq \flat \mathbb{R}_C$ since $\flat \mathbb{R}_C$ already embeds into $\flat \mathbb{R}$, and since $\mathbb{R}_C$ has [[decidable tight apartness]], it is discrete and we have $\mathbb{R}_C \simeq \flat \mathbb{R}_C$. Thus, we have in the cohesive mode
$$\mathbb{R}_C \simeq \mathbb{R}_H \simeq \mathbb{R}_\Sigma \simeq \flat \mathbb{R}$$
\end{proof}

## Related concepts

* [[axiom of cohesion]]

* [[axiom of sufficient cohesion]]

* [[axiom of real cohesion]]

## References

* {#Shulman18} [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Shulman17} [[Mike Shulman]], *Homotopy type theory: the logic of space*, New Spaces in Mathematics: Formal and Conceptual Reflections, ed. Gabriel Catren and Mathieu Anel, Cambridge University Press, 2021 ([arXiv:1703.03007](https://arxiv.org/abs/1703.03007), [doi:10.1017/9781108854429](https://doi.org/10.1017/9781108854429))

* {#Aberle24} [[C.B. Aberlé]], *Parametricity via Cohesion* &lbrack;[arXiv:2404.03825](https://arxiv.org/abs/2404.03825)&rbrack; 

[[!redirects punctual cohesion]]
[[!redirects axiom of punctual cohesion]]
[[!redirects axioms of punctual cohesion]]

[[!redirects axiom C1]]

[[!redirects axiom of punctual local connectedness]]
[[!redirects axioms of punctual local connectedness]]
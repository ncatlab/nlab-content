
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

## Definition

### In cohesive type theory

In [[cohesive type theory]], the axiom of **sufficient cohesion** states that there is a [[type]] $I$ with elements $0:I$ and $1:I$ such that $\neg (0 =_I 1)$ and the [[shape]] of $I$ is a [[contractible type]]. 

This is equivalent in strength to **axiom C2**, which says that there is a [[type]] $I$ with elements $0:I$ and $1:I$ such that $\neg (0 =_I 1)$ and every crisp type $T$ is discrete if and only if every function from $I$ into $\mathrm{Disc}(T)$ is a [[constant function]]. $\mathrm{Disc}$ is a [[modality]] which takes types in the crisp mode to its corresponding discrete type in the cohesive mode, and a discrete type $A$ in the cohesive mode is one for which the canonical function $\flat(-):A \to \flat A$ is an [[equivalence of types]]. 

[Shulman 2018](#Shulman18) showed that Axiom C2 implies that every function from $I$ into a discrete type $A$ is a constant function; conversely, if every function from $I$ to a discrete type $A$ is constant, then it holds for the discrete types which are in the image of the $\mathrm{Disc}$ modality. Finally, [Aberlé 2024](#Aberle24) proved that the axiom of sufficient cohesion holds if and only if every function from $I$ into a discrete type $A$ is a constant function. 

## Properties

\begin{theorem}
Assuming the axiom of sufficient cohesion, the [[boolean domain]] $\mathbb{2}$ is a discrete type.
\end{theorem}

\begin{proof}
TBD, see [Aberlé 2024](#Aberle24) for the time being. 
\end{proof}

Since the [[boolean domain]] is discrete, the type $I$ is [[compact connected]]:

\begin{theorem}
Assuming the axiom of sufficient cohesion, if the function $\mathrm{const}_{\mathbb{2}, I}$ is an equivalence of types, then for all $I$-indexed families of [[mere propositions]] $x:I \vdash P(x)$, if for all $x:I$, $P(x) \vee \neg P(x)$ is contractible, then either for all $x:I$, $P(x)$ is contractible, or for all $x:I$, $\neg P(x)$ is contractible. 
\end{theorem}

\begin{proof}
If the family of mere propositions $x:I \vdash P(x)$ is such that for all $x:I$, $P(x) \vee \neg P(x)$ is contractible, then there is a function $P':R \to \mathbb{2}$ into the [[boolean domain]] $\mathbb{2}$ with $\delta_{P'}^{1_2}(x):(P'(x) = 1_2)) \simeq P(x)$ and $\delta_{P'}^{0_2}(x):(P'(x) = 0_2)) \simeq \neg P(x)$. But since $\mathbb{2}$ is discrete, then by sufficient cohesion $P'$ is constant, which implies that either for all $x:I$, $P'(x) = 1_2$ and thus $P(x)$ is contractible, or for all $x:I$, $P'(x) = 0_2$ and thus $\neg P(x)$ is contractible. Thus, $I$ is compact connected. 
\end{proof}

\begin{definition}
The [[shape modality]] of a type $A$ is defined to be the [[localization of a type|localization]] of $A$ at the type $I$

$$\esh A \coloneqq L_I(A)$$
\end{definition}

\begin{theorem}
Assuming the axiom of sufficient cohesion, there exists a pullback which is not preserved by the [[shape modality]]. 
\end{theorem}

\begin{proof}
By the recursion principle of the [[positive type|positive]] [[unit type]], there are functions $\mathrm{rec}_\mathbb{1}^I(0):\mathbb{1} \to I$ and $\mathrm{rec}_\mathbb{1}^I(1):\mathbb{1} \to I$. By the fact that $\neg (0 =_I 1)$, the pullback of these two functions is the [[empty type]] $\emptyset$. However, while the shape of $\mathbb{1}$ is always contractible and the shape of $I$ is contractible by the axiom of sufficient cohesion, the shape of $\emptyset$ is still $\emptyset$, which is not contractible. 
\end{proof}

## Related concepts

* [[axiom of cohesion]]

* [[axiom of real cohesion]]

## References

* {#Lawvere07} [[William Lawvere]]. Axiomatic cohesion. Theory and Applications of Categories, 19(3):41–49, 2007.

* {#Shulman18} [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Aberle24} [[C.B. Aberlé]], *Parametricity via Cohesion* &lbrack;[arXiv:2404.03825](https://arxiv.org/abs/2404.03825)&rbrack; 

[[!redirects sufficient cohesion]]
[[!redirects axiom of sufficient cohesion]]
[[!redirects axioms of sufficient cohesion]]

[[!redirects sufficient-cohesion]]
[[!redirects axiom of sufficient-cohesion]]
[[!redirects axioms of sufficient-cohesion]]

[[!redirects axiom C2]]

[[!redirects axiom of contractible codiscreteness]]
[[!redirects axioms of contractible codiscreteness]]
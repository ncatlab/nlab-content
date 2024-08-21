
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
Assuming punctual cohesion, all [[mere propositions]] are discrete.
\end{theorem}

\begin{proof}
Since $I$ is a [[pointed type]], if $A$ is a proposition and there is a function $I \to A$, then $A$ is a [[contractible type]], which means that every function into $A$ is a [[constant function]], and thus that $A$ is a discrete type. 
\end{proof}

\begin{lemma}
Let $A$ be a cohesive type with a [[tight apartness relation]]. Assuming punctual cohesion, for each $x:A$ and $y:A$ the type $x \# y$ is discrete. 
\end{lemma}

\begin{proof}
The type $x \# y$ is a mere proposition and is thus discrete. 
\end{proof}

\begin{theorem}
Assuming punctual cohesion, the [[boolean domain]] is discrete.
\end{theorem}

\begin{proof}
There might be a proof somewhere in [Shulman 18](#Shulman18) since the author asserts it as fact later in the paper assuming punctual cohesion. 
\end{proof}

Since the [[boolean domain]] is discrete, the type $I$ is [[compact connected]]:

\begin{theorem}
Assuming the axiom of punctual cohesion, if the function $\mathrm{const}_{\mathbb{2}, I}$ is an equivalence of types, then for all $I$-indexed families of [[mere propositions]] $x:I \vdash P(x)$, if for all $x:I$, $P(x) \vee \neg P(x)$ is contractible, then either for all $x:I$, $P(x)$ is contractible, or for all $x:I$, $\neg P(x)$ is contractible. 
\end{theorem}

\begin{proof}
If the family of mere propositions $x:I \vdash P(x)$ is such that for all $x:I$, $P(x) \vee \neg P(x)$ is contractible, then there is a function $P':I \to \mathbb{2}$ into the [[boolean domain]] $\mathbb{2}$ with $\delta_{P'}^{1_2}(x):(P'(x) = 1_2)) \simeq P(x)$ and $\delta_{P'}^{0_2}(x):(P'(x) = 0_2)) \simeq \neg P(x)$. But since $\mathbb{2}$ is discrete, then by punctual cohesion $P'$ is constant, which implies that either for all $x:I$, $P'(x) = 1_2$ and thus $P(x)$ is contractible, or for all $x:I$, $P'(x) = 0_2$ and thus $\neg P(x)$ is contractible. Thus, $I$ is compact connected. 
\end{proof}

\begin{theorem}
Let $A$ be a cohesive type with a [[tight apartness relation]]. Assuming punctual cohesion and crisp [[excluded middle]], if the [[tight apartness relation]] on $A$ is [[decidable tight apartness relation|decidable]], then $A$ is discrete. 
\end{theorem}

\begin{proof}
Since the [[tight apartness relation]] and [[equality]] are incompatible propositions, we have for all $x:A$ and $y:A$ that 
$$(x \# y) \vee (x = y) \simeq (x \# y) + (x = y)$$
so we can define functions by induction on the [[boolean domain]]. Given a function $f:I \to A$ there is a function $g:I \to \mathbb{2}$ defined as 
$$
g(r) \coloneqq 
\begin{cases}
1 & f(r) = f(p) \\
0 & f(r) \# f(p)
\end{cases}
$$
Since the boolean domain is discrete, $g$ is constant, but $g(p) = 1$, so $g(r) = 1$ and $f(r) = f(p)$ for all $r:I$, meaning that $f$ is also a constant function. Thus $A$ is discrete. 
\end{proof}

To do: show if possible that any tight apartness relation on a discrete type $A$ is crisp. 

## Related concepts

* [[axiom of cohesion]]

* [[axiom of sufficient cohesion]]

* [[axiom of real cohesion]]

## References

* {#Shulman18} [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Shulman17} [[Mike Shulman]], *Homotopy type theory: the logic of space*, New Spaces in Mathematics: Formal and Conceptual Reflections, ed. Gabriel Catren and Mathieu Anel, Cambridge University Press, 2021 ([arXiv:1703.03007](https://arxiv.org/abs/1703.03007), [doi:10.1017/9781108854429](https://doi.org/10.1017/9781108854429))

[[!redirects punctual cohesion]]
[[!redirects axiom of punctual cohesion]]
[[!redirects axioms of punctual cohesion]]

[[!redirects axiom C1]]

[[!redirects axiom of punctual local connectedness]]
[[!redirects axioms of punctual local connectedness]]
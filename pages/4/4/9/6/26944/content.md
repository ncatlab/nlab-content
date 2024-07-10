
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
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

\tableofcontents

## Idea

The [[Cauchy real numbers]] or [[regular real numbers]] are defined as the [[quotient set]] of [[Cauchy sequences]] of [[rational numbers]] by a suitable equivalence relation, and is provably an [[Archimedean ordered field|Archimedean ordered]] [[field extension]] of the rational numbers.  

The same construction could be perform by taking any Archimedean ordered field $F$ and quotienting the set of Cauchy sequences of elements in $F$ by a similar suitable equivalence relation, and the resulting quotient set $\mathcal{C}(F)$ is likewise an Archimedean ordered field extension of $F$. 

This construction is important since it yields an [[endofunctor]] $F \mapsto \mathcal{C}(F)$ in the [[category]] of [[Archimedean ordered fields]] and [[ring homomorphisms]], whose [[algebra for an endofunctor|algebras]] are the [[sequentially Cauchy complete]] [[Archimedean ordered fields]]. In particular, one can define the [[Escardo-Simpson real numbers]] as the [[initial algebra of the endofunctor]] $F \mapsto \mathcal{C}(F)$ and prove that the [[terminal]] object ([[Dedekind real numbers]]) is an [[algebra of the endofunctor]] $F \mapsto \mathcal{C}(F)$, thus yielding [[predicative mathematics|predicative]] and [[constructive mathematics|constructive]] definitions of both notions of real numbers (i.e. without [[power sets]], or even general [[function sets]], since only sequence sets - function sets from the natural numbers - are needed). In addition, [[excluded middle]] or [[countable choice]] is sufficient to show that this endofunctor is [[idempotent]] up to [[isomorphism]]. 

The author of this article does not know if this general construction is known in the [[real analysis]] literature by some already existing name. However, the author feels that "Cauchy quotient" is a suitable placeholder name, since it is the *quotient* set of *Cauchy sequences* in an [[Archimedean ordered field]]. 

## Definition

Let $F$ be an [[Archimedean ordered field]]. Then a sequence in $F$ is an element of the [[function set]] $F^\mathbb{N}$. A sequence $x \in F^\mathbb{N}$ is a [[Cauchy sequence]] if for all natural numbers $m$ and $n$, 
$$-\left(\frac{1}{m} + \frac{1}{n}\right) \lt x(m) - x(n) \lt \frac{1}{m} + \frac{1}{n}$$

In the case of the [[rational numbers]], this is usually expressed as one [[inequality]] using the [[absolute value]] function, but here we do not assume that the Archimedean ordered field has an absolute value function or equivalently a [[lattice]] order. 

We denote the set of [[Cauchy sequences]] in $F$ as the set 

$$\mathrm{Cauchy}(F) \coloneqq \left\{x \in F^\mathbb{N} \vert -\left(\frac{1}{m} + \frac{1}{n}\right) \lt x(m) - x(n) \lt \frac{1}{m} + \frac{1}{n}\right\}$$

Given two Cauchy sequences $x$ and $y$, there is an relation $x \approx y$ defined by

$$x \approx y \coloneqq \forall n \in \mathbb{N}.-\frac{2}{n} \lt x(n) - y(n) \lt \frac{2}{n}$$

\begin{theorem}
This relation is an [[equivalence relation]]. 
\end{theorem}

\begin{proof}
TODO: Adapt the proof found in Proposition 3.3.2 and Lemma 3.3.3 [Murray 2022](#Murray22) to the case where $F$ is any Archimedean ordered field. 
\end{proof}

Since the above relation is an equivalence relation on the set $\mathrm{Cauchy}(F)$ of Cauchy sequences in $F$, we can take the [[quotient set]] 
$$\mathcal{C}(F) \coloneqq \mathrm{Cauchy}(F) / \approx$$ 
resulting in a set $\mathcal{C}(F)$ called the **Cauchy quotient**. 

\begin{theorem}
$\mathrm{Cauchy}(F)$ is an [[Archimedean ordered field setoid]]. 
\end{theorem}

\begin{proof}
TODO: Adapt the proofs found in section 3.3 of [Murray 2022](#Murray22), as well as in other sources (to be found) for multiplication and division. 
\end{proof}

\begin{theorem}
$\mathcal{C}(F)$ is an [[Archimedean ordered field]]. 
\end{theorem}

\begin{proof}
The quotient of any [[ordered field setoid]] by its equivalence relation is an [[ordered field]], and quotienting preserves the [[Archimedean property]]. Since $\mathrm{Cauchy}(F)$ is an Archimedean ordered field setoid, this implies that $\mathcal{C}(F)$ is an Archimedean ordered field. 
\end{proof}

\begin{theorem}
$\mathcal{C}(F)$ is a field extension of $F$. 
\end{theorem}

\begin{proof}
Since every constant sequence in $F$ is a Cauchy sequence, the composite of the function $\lambda x:F.\lambda n:\mathbb{N}.x$ from $F$ to $\mathrm{Cauchy}(F)$ with the quotient set [[effective epimorphism|effective]] [[surjection]] from $\mathrm{Cauchy}(F)$ to $\mathcal{C}(F)$ yields a [[ring homomorphism]] from $F$ to $\mathcal{C}(F)$. Thus, $\mathcal{C}(F)$ is a field extension of $F$. 
\end{proof}

## As an endofunctor

\begin{theorem}
Given [[setoids]] $(A, \sim_A)$ and $(B, \sim_B)$ with a [[function]] $f:A \to B$ which preserves and reflects the [[equivalence relations]]. Then there is an injection $[f]:(A / \sim_A) \to (B / \sim_B)$. 
\end{theorem}

\begin{proof}
...
\end{proof}

\begin{theorem}
Given Archimedean ordered fields $F$ and $K$ with [[ring homomorphism]] $h:F \to K$, there is an injection from $\mathrm{Cauchy}(F)$ to $\mathrm{Cauchy}(K)$ which preserves and reflects the equivalence relations on Cauchy sequences. 
\end{theorem}

\begin{proof}
...
\end{proof}

\begin{theorem}
Given Archimedean ordered fields $F$ and $K$ with [[ring homomorphism]] $h:F \to K$, there is a [[ring homomorphism]] $\mathcal{C}(h):\mathcal{C}(F) \to \mathcal{C}(K)$ which preserves identity ring homomorphisms and composition of ring homomorphisms. 
\end{theorem}

\begin{proof}
...
\end{proof}

\begin{corollary}
The function $F \mapsto \mathcal{C}(F)$ is an [[endofunctor]] in the [[category]] of [[Archimedean ordered fields]] and [[ring homomorphisms]]. 
\end{corollary}

\begin{proof}
By definition of endofunctor. 
\end{proof}

\begin{theorem}
Let $F$ be an [[algebra of the endofunctor]] $F \mapsto \mathcal{C}(F)$. Then $F$ is isomorphic to $\mathcal{C}(F)$. 
\end{theorem}

\begin{proof}
The category of [[Archimedean ordered fields]] and [[ring homomorphisms]] is a [[preorder]], since any [[ring homomorphism]] which exists between two Archimedean ordered fields is [[unique]]. This means that every morphism is a [[monomorphism]] and the [[Cantor-Schroeder-Bernstein theorem]] holds in the category. As a result, it suffices for there to be ring homomorphisms in both directions between $F$ and $\mathcal{C}(F)$: there is always a ring homomorphism from $F$ to $\mathcal{C}(F)$ via the equivalence classes of constant sequences in $F$, and there is a ring homomorphism from $\mathcal{C}(F)$ to $F$ by definition of [[algebra of an endofunctor]]. Thus, $F$ is isomorphic to $\mathcal{C}(F)$. 
\end{proof}

\begin{corollary}
Every algebra for the endofunctor $F \mapsto \mathcal{C}(F)$ is [[sequentially Cauchy complete]]. 
\end{corollary}

\begin{theorem}
The [[terminal object|terminal]] [[Archimedean ordered field]] $\mathbb{R}$ is an algebra for the endofunctor $F \mapsto \mathcal{C}(F)$. 
\end{theorem}

\begin{proof}
By definition of terminal object, there is a ring homomorphism from $\mathcal{C}(\mathbb{R})$ to $\mathbb{R}$. Thus, $\mathbb{R}$ is an algebra for the endofunctor $F \mapsto \mathcal{C}(F)$. 
\end{proof}

\begin{corollary}
The [[terminal object|terminal]] [[Archimedean ordered field]] $\mathbb{R}$ is [[sequentially Cauchy complete]]. 
\end{corollary}

\begin{theorem}
Assuming [[excluded middle]] or [[countable choice]], the endofunctor $F \mapsto \mathcal{C}(F)$ is [[idempotent]] up to [[isomorphism]]. 
\end{theorem}

\begin{proof}
...
\end{proof}

## Related concepts

* [[Cauchy sequence]]

* [[Cauchy real numbers]]

## References

Some of the proofs are adapted from proofs for the special case of the [[rational numbers]] to construct the [[Cauchy real numbers]]: 

* {#Murray22} [[Zachary Murray]], *Constructive Analysis in the Agda Proof Assistant* &lbrack;[arXiv:2205.08354](https://arxiv.org/abs/2205.08354), [github](https://github.com/z-murray/honours-project-constructive-analysis-in-agda)&rbrack;

[[!redirects Cauchy quotient]]

[[!redirects Cauchy quotient functor]]
[[!redirects Cauchy quotient functors]]

[[!redirects Cauchy quotient endofunctor]]
[[!redirects Cauchy quotient endofunctors]]
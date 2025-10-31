
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of  **minimal objects** generalizes the notion of minimal elements of [[preorders]]. Intuitively, minimal elements are ones that don't have anything below them, even though they might not be _the minimum_. A 'minimum object' would be instead an [[initial object]].

Minimal objects have been first defined in [(Adámek et al. '12)](#ABHKMS) in the context of [[coalgebra]] theory, relative to an [[orthogonal factorization system]]. Trivializing the [[factorization system]] gives a general notion of minimality and maximality, though these are quite a bit stronger in more general [[categories]].

## Definition
### In preorders
\begin{definition}
In a [[preorder]] $(C, \leq)$, a minimal element $m \in C$ is one such that if $a \leq m$, then $m \leq a$. Dually, a maximal element is one such that $m \leq a$ implies $a \leq m$, i.e. which is minimal in $C^{op}$.
\end{definition}

\begin{remark}
If $C$ is [[bounded lattice|bounded below]], meaning there  is an element $\bot \in C$ such that $\bot \leq a$ for all $a \in C$ ($\bot$ is [[initial object|initial]]), then $\bot$ is the only minimal element in $C$.
Hence in many cases (chiefly, when $C$ is the preorder of [[ideals]] of a ring), one speaks of minimality in $C\setminus\{\bot\}$, that is, one defines a minimal element to be one for which $a \leq m$ implies $a=m$ _or $a=\bot$.

This is not the definition we take here!
\end{remark}

### In categories
Let $(\mathcal{E}, \mathcal{M})$ be an [[orthogonal factorization system]] on a [[category]] $\mathcal{C}$. This means:

0. $\mathcal{E}$ and $\mathcal{M}$ are [[wide subcategories]] of $\mathcal{C}$ closed under composition and each containing all isomorphisms of $\mathcal{C}$.
1. Every morphism in $\mathcal{C}$ factors uniquely as a morphism in $\mathcal{E}$ followed by one in $\mathcal{M}$:
\[
  a \overset{f}\to b = a \overset{e_f}\twoheadrightarrow \mathrm{im}(f) \overset{m_f}\rightarrowtail b.
\]
2. The morphisms in $\mathcal{E}$ are exactly the ones having the [[left lifting property]] against the morphisms in $\mathcal{M}$, and the morphisms in $\mathcal{M}$ are exactly the ones having the [[right lifting property]] against the morphisms in $\mathcal{E}$.
3. The lifts are unique.

Here we'll tend to denote morphisms in $\mathcal{E}$ with $\twoheadrightarrow$ and morphisms in $\mathcal{M}$ with $\rightarrowtail$. In fact, a common source of examples for these factorization systems is given by the systems of [[strong epimorphism|strongly epic]] and [[monic|monomorphism]] arrows.

\begin{definition}
An **$\mathcal{M}$-minimal object** is an object $M:\mathcal{C}$ such that every morphism $h : A \rightarrowtail M$ in $\mathcal{M}$ is an isomorphism.
\end{definition}

\begin{definition}
An **$\mathcal{E}$-minimal object** is an object $M:\mathcal{C}$ such that every morphism $h : M \twoheadrightarrow A$ in $\mathcal{E}$ is an isomorphism.
\end{definition}

Clearly the two definitions above are dual to each other, since $\mathcal{C}^{op}$ is equipped with the orthogonal factorization system $(\mathcal{M}^{op}, \mathcal{E}^{op})$. Indeed, one might call $\mathcal{E}$-minimal objects **$\mathcal{M}$-maximal**.

\begin{remark}
Instantiating this definition for the trivial factorization systems gives us a general definition of minimal and maximal objects in a category:

- In fact, every category $\mathcal{C}$ admits a trivial orthogonal factorization systems, namely $(Iso, All)$. In this instance, every object is $Iso$-minimal (since every isomorphism to it is already an iso) but an $Iso$-maximal object is one such that every morphism out of it is invertible.
We call these simply **maximal objects**.

- Every category $\mathcal{C}$ also admits $(All, Iso)$ as a trivial orthogonal factorization system. In this case, $All$-minimal objects are the ones for which every morphism into them is invertible, whereas every object is trivially $All$-maximal. We call these simply **minimal objects**.

These notions recover the order-theoretic ones when $\mathcal{C}$ is a preorder.
\end{remark}

\begin{proposition}
The following are equivalent:

1. An object $M : \mathcal{C}$ is $\mathcal{M}$-minimal
2. Every morphism $h:A \to M$ is in $\mathcal{E}$.
3. (if $\mathcal{E}$=epimorphisms and $\mathcal{C}$ has [[weak equalizers]]) All parallel pairs of arrows $A \rightrightarrows M$ are equal.

\end{proposition}

\begin{corollary}

Dually, the following are equivalent:

1. An object $M : \mathcal{C}$ is $\mathcal{M}$-maximal
2. Every morphism $h:M \to A$ is in $\mathcal{M}$.
3. (if $\mathcal{M}$=monomorphisms and $\mathcal{C}$ has [[weak coequalizers]]) All parallel pairs of arrows $M \rightrightarrows A$ are equal (i.e. $M$ is [[subterminal]])

\end{corollary}

## Relation with initial objects

Like for preorders, the only minimal objects in a category having initial objects are the latter (up to isomorphism, of course). In fact, suppose $\mathcal{C}$ has initial object $0$ and suppose $M : \mathcal{C}$ is minimal. Then the initial map $?_M : 0 \to M$ has to be an isomorphism, so that $M \cong 0$.

However, unlike in preorders, not all initial objects are minimal! Notice, in fact, that the argument above shows $0$ is minimal under the assumption a minimal object already exists, but this doesn't have to be true.
A **minimal initial object** is known as [[strict initial object]].

Everything just said dualizes: every maximal object in a category with terminal object is terminal, but not every terminal object is maximal. A **maximal terminal object** is known as [[strict terminal object]].

## Minimization
Let $\mathcal{C}$ be a category equipped with an $(\mathcal{E}, \mathcal{M})$-factorization system.

\begin{definition}
An **$\mathcal{M}$-minimization** of $A: \mathcal{C}$ is a morphism $m:M \to A$ in $\mathcal{M}$ where $M:\mathcal{C}$ is $\mathcal{M}$-minimal.
Dually, an **$\mathcal{E}$-minimization** of $A: \mathcal{C}$ is a morphism $e:A \to E$ in $\mathcal{E}$ where $E:\mathcal{C}$ is $\mathcal{E}$-minimal.
\end{definition}

With abuse of notation, we call 'minimization of $A$' both the morphism and the minimal object.

## Examples

1. Let $\mathcal{C} = \mathbf{Coalg}_*(F)$ is the category of [[pointed object|pointed]] [[coalgebras]] for some endofunctor $F:\mathbf{Set} \to \mathbf{Set}$. This category inherits the epi-mono factorization system from $\mathbf{Set}$. Then a mono-minimal object in $\mathbf{Coalg}_*(F)$ is a _reachable coalgebra_, that is, one that has no non-trivial pointed subcoalgebra. Intuitively, this means every state of a reachable coalgebra is reachable in finitely many transitions from its distinguished point (playing the role of 'initial state').

2. In $\mathcal{C} = \mathbf{Coalg}(F)$, an epi-maximal object is a _simple coalgebra_, that is, one that has no non-trivial quotient. Intuitively, this means that there are no states in the coalgebra with the same behaviour.

3. In the same setting as (2), when $F$ preserves monos, then a quotient $m : S \to S'$ where $S'$ is epi-maximal is called a _minimization_ for $S$. Concretely, it exhibits a way to reduce the automaton $S$ to a smaller automaton $S'$ in which no states are duplicated (where we consider duplicated states with the same behaviour).

## Properties
\begin{proposition}
In a category $\mathcal{C}$ with products, minimal objects, if they exists, are unique up to isomorphism.
\end{proposition}
\begin{proof}
Let $M,M'$ be minimal in $\mathcal{C}$. Then $\pi_M : M \times M' \to M$ and $\pi_{M'} : M \times M' \to M'$ are both invertible, proving $M \cong M \times M' \cong M'$.
\end{proof}

\begin{proposition}
Let $\mathcal{C}$ be a category with finite products.
Then if $M$ is minimal it is weakly initial.
\end{proposition}
\begin{proof}
Let $M:\mathcal{C}$ be such minimal object. Let $A$ be any other object in $\mathcal{C}$. Then, by hypothesis on $M$, the projection $\pi_M : M \times A \to M$ is invertible. Therefore $M$ admits a morphism into every object of $\mathcal{C}$, given by $w_A := M \overset{\pi^{-1}_M}\to M \times A \overset{\pi_A}\to A$.
\end{proof}

Notice we can't say anything about the uniqueness of these morphisms $w_A : M \to A$. In general, they are not even functorially chosen.

## Related concepts

* [[minimal ideal]], [[maximal ideal]]
* [[strict initial object]],  [[strict terminal object]]
* [[simple coalgebra]]
* [[reachability]]

## References

* {#ABHKMS} [[Jiri Adamek|J. Adámek]], [[Filippo Bonchi|F. Bonchi]], M. Hülsbusch, B. König, S. Milius, and [[Alexandra Silva|A. Silva]], _A coalgebraic perspective on minimization and determinization_, in Proceedings of the 15th international conference on Foundations of Software Science and Computational Structures, 2012, pp. 58–73.

* {#Weissmann22} Thorsten Weissmann, _Minimality Notions via Factorization Systems and Examples_ Logical Methods in Computer Science **18** (2022) &lbrack;<a href="https://doi.org/10.46298/lmcs-18(3:31)2022">doi:10.46298/lmcs-18(3:31)2022</a>&rbrack;

* {#BKP} Nick Bezhanishvili, Clemens Kupke, [[Prakash Panangaden]], *Minimization via Duality*, in: *Logic, Language, Information and Computation. WoLLIC 2012*, Lecture Notes in Computer Science **7456**, Springer (2012) &lbrack;[doi:10.1007/978-3-642-32621-9_14](https://doi.org/10.1007/978-3-642-32621-9_14), [pdf](https://staff.science.uva.nl/n.bezhanishvili/Papers/Wollic.pdf)&rbrack;

[[!redirects minimal objects]]
[[!redirects maximal object]]
[[!redirects maximal objects]]
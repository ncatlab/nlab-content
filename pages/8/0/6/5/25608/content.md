
# Contents
* table of contents
{:toc}


## Idea

An implicative algebra is an [[implicative structure]] equipped with a [[filter]]-like subset called a *separator*.

Recall an implicative structure is a generalized [[complete Heyting algebra]] in which the implication $\to$ is only required to be right continuous and not necessarily right adjoint to the meet.

The separator is defined in such a way as to induce a quotient which makes the implicative structure into a bona-fide Heyting algebra. It is in this sense that a separator is like a (ultra)filter, whose primary purpose is to be used to define quotients which usually restore some property.

Given the completeness result in [(Miquel'20b)](#Miquel20b), we can say implicative algebras are to ($\mathbf{Set}$-)triposes what [[complete Heyting algebra|complete Heyting algebras]] (equivalently, [[locale|locales]]) are to [[Grothendieck topos|Grothendieck toposes]].

## Definition

Let $(\mathcal{A}, \leq, \to)$ be an [[implicative structure]].

\begin{definition}
A **separator** of $\mathcal{A}$ is a subset $S \subseteq \mathcal{A}$ such that

1. $S$ is upwards closed: for all $a \leq b \in \mathcal{A}$, $a \in S$ implies $b \in S$.
2. $S$ is closed under 'modus ponens': for all $a, b \in \mathcal{A}$, $a \in S$ and $a \to b \in S$ implies $b \in S$.
3. $S$ contains the following elements:
\[
K = \bigwedge_{a,b \in \mathcal{A}} (a \to b \to a),
\]
\[
S = \bigwedge_{a,b,c \in \mathcal{A}} (a \to b \to c) \to b \to a \to c)
\]

\end{definition}

\begin{remark}
In the case $\mathcal{A}$ is actually an [[Heyting algebra]], separators coincide with filters.
\end{remark}

\begin{proposition}
Let $S$ be a separator of $\mathcal{A}$. Then we can define a relation on $\mathcal{A}$:
\[
a \vdash_S b \quad \text{iff}\quad (a \to b) \in S.
\]
This relation is a [[preorder]], and its [[posetal reflection]] is an Heyting algebra with implication given by:
\[
[a] \Rightarrow [b] := [a \to b].
\]
\end{proposition}
\begin{proof}
This is Proposition 3.2.1 in [(Miquel'20)](#Miquel20).
\end{proof}

The Heyting algebra obtained from an implicative algebra is called its **induced Heyting algebra**, denoted $(\mathcal{A}/S, \leq_S)$. It is proven in [(Miquel'20)](#Miquel20) that this operation is functorial .

\begin{remark}
When $\mathcal{A}$ is an Heyting algebra to begin with, $(\mathcal{A}/S, \leq_S)$ is the quotient induced by $S$, seen as a filter.
\end{remark}

## See also

* [[filter]]
* [[complete Heyting algebra]]
* [[realizability]]
* [[forcing]]
* [[tripos]], in particular [[implicative tripos]]

## References
* {#Miquel20} Alexandre Miquel, _Implicative algebras: a new foundation for realizability and forcing_, Mathematical Structures in Computer Science 30 (5): 458–510. [(doi)](https://doi.org/10.1017/S0960129520000079).

* {#Miquel20b} Alexandre Miquel. 2020. _Implicative Algebras II: Completeness w.r.t. Set-Based Triposes_. arXiv. https://doi.org/10.48550/arXiv.2011.09085.
 [(arxiv)](https://arxiv.org/abs/2011.09085)


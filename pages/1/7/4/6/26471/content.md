
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[strict total order]] which is not a [[connected relation]]. 

## Definition

A **strict weak order** is a [[strict preorder]] which is also a [[cotransitive relation]]. 

Strict weak orders are used in models of the real numbers which have [[infinitesimals]], such as in the smooth real numbers in [[synthetic differential geometry]], and thus where not every real number not greater than or less than zero is equal to zero. 

## Properties

\begin{theorem}
Strict weak orders are [[asymmetric relations]].
\end{theorem}

\begin{proof}
Transitivity of $\lt$ says that for all $x \in S$ and $y \in S$, $x \lt y$ and $y \lt x$ implies $x \lt x$. However, irreflexivity says that for all $x$, $x \leq x$ is always false. This implies that for all $x$ and $y$, $x \lt y$ and $y \lt x$ is always false, which is precisely the condition of asymmetry. 
\end{proof}

\begin{theorem}
Connected strict weak orders are [[pseudo-orders]].
\end{theorem}

\begin{proof}
The proof is the same as above, except both relevant orders are [[connected relations]]. 
\end{proof}

### Preorder of a strict weak order

An important part of a strict weak order is that it is a preorder. 

\begin{theorem}
The negation of a strict weak order is transitive. 
\end{theorem}

\begin{proof}
The [[contrapositive]] of cotransitivity says that 

> for all $x$, $y$, and $z$, if $x \lt y$ or $y \lt z$ is false, then $x \lt z$ is false. 

By one of [[de Morgan's laws]], that $x \lt y$ or $y \lt z$ is false is logically to equivalent to that $\neg(x \lt y)$ and $\neg(y \lt z)$, and substituting this into the original statement results in 

> if $\neg(x \lt y)$ and $\neg(y \lt z)$, then $\neg(x \lt z)$

which is precisely transitivity for the negation of the strict weak order. 
\end{proof}

\begin{theorem}
The negation of a strict weak order is reflexive.
\end{theorem}

\begin{proof}
Irreflexivity states that $\neg (x \lt x)$ is true, which is precisely reflexivity for the negation of the strict weak order. 
\end{proof}

\begin{theorem}
The negation of a strict weak order is a preorder. 
\end{theorem}

\begin{corollary}
The incomparability relation of a strict weak order, $\neg (x \lt y) \wedge \neg (y \lt x)$, is an [[equivalence relation]]
\end{corollary}

\begin{proof}
For every preorder, $(x \leq y) \wedge (y \leq x)$ is an [[equivalence relation]]. Since $\neg (x \lt y)$ is a [[preorder]], $\neg (x \lt y) \wedge \neg (y \lt x)$ is an equivalence relation. 
\end{proof}

## See also

* [[total preorder]]

* [[weak order]]

* [[pseudo-order]]

* [[strictly weakly ordered ring]]

* [[ordered local ring]]

* [[ordered Kock field]]

* [[irreflexive comparison]]

## References

* Wikipedia, [Weak order](https://en.wikipedia.org/wiki/Weak_order)

Strict weak orders are used in defining the smooth real numbers in:

* [[David Jaz Myers]], *Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory* ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))

[[!redirects strict weak order]]
[[!redirects strict weak orders]]
[[!redirects strict weak ordering]]
[[!redirects strict weak orderings]]

[[!redirects strict weakly ordered]]
[[!redirects strict weakly ordered set]]
[[!redirects strict weakly ordered sets]]

[[!redirects strictly weakly ordered]]
[[!redirects strictly weakly ordered set]]
[[!redirects strictly weakly ordered sets]]
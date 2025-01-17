# Irreflexive comparison
* table of contents
{: toc}

## Idea

Just as [[preorders]] generalise [[equivalence relations]] and [[total orders]], _irreflexive comparisons_ should generalise [[apartness relations]] and [[strict total orders]]

## Definitions

An **irreflexive comparison** on a set $S$ is a (binary) [[relation]] $\lt$ on $S$ that is both [[irreflexive relation|irreflexive]] and a [[comparison]].  That is:

* $x \lt x$ is always false;
* If $x \lt z$, then $x \lt y$ or $y \lt z$

## Properties

A [[set]] $S$ equipped with an irreflexive comparison is a [[category]] (with $S$ as the set of [[objects]]) [[enriched category|enriched]] over the [[cartesian monoidal category]] $TV^\op$, that is the [[opposite category|opposite]] of the [[partial order|poset]] of [[truth value|truth values]], made into a [[monoidal category]] using [[disjunction]]. $TV^\op$ is a [[co-Heyting algebra]]. 

### Preorder of an irreflexive comparison

An important part of an irreflexive comparison is that it is a preorder. 

\begin{theorem}
The negation of an irreflexive comparison is transitive. 
\end{theorem}

\begin{proof}
The [[contrapositive]] of comparison says that 

> for all $x$, $y$, and $z$, if $x \lt y$ or $y \lt z$ is false, then $x \lt z$ is false. 

By one of [[de Morgan's laws]], that $x \lt y$ or $y \lt z$ is false is logically to equivalent to that $\neg(x \lt y)$ and $\neg(y \lt z)$, and substituting this into the original statement results in 

> if $\neg(x \lt y)$ and $\neg(y \lt z)$, then $\neg(x \lt z)$

which is precisely transitivity for the negation of the irreflexive comparison. 
\end{proof}

\begin{theorem}
The negation of an irreflexive comparison is reflexive.
\end{theorem}

\begin{proof}
Irreflexivity states that $\neg (x \lt x)$ is true, which is precisely reflexivity for the negation of the strict weak order. 
\end{proof}

\begin{theorem}
The negation of an irreflexive comparison is a preorder. 
\end{theorem}

\begin{corollary}
The incomparability relation of a strict weak order, $\neg (x \lt y) \wedge \neg (y \lt x)$, is an [[equivalence relation]]
\end{corollary}

\begin{proof}
For every preorder, $(x \leq y) \wedge (y \leq x)$ is an [[equivalence relation]]. Since $\neg (x \lt y)$ is a [[preorder]], $\neg (x \lt y) \wedge \neg (y \lt x)$ is an equivalence relation. 
\end{proof}

\begin{theorem}
If the irreflexive comparison is a [[connected relation]], then its negation is a [[partial order]].
\end{theorem}

\begin{proof}
The connectedness condition states that $\neg (x \lt y) \wedge \neg (y \lt x)$ implies equality, which is precisely the antisymmetry condition for the negation of the strict weak order, implying that its negation is a [[partial order]]. 
\end{proof}

\begin{theorem}
If the irreflexive comparison is an [[apartness relation]], then its negation is an [[equivalence relation]].
\end{theorem}

\begin{proof}
The symmetry condition of the apartness relation states that $x \lt y$ implies $y \lt x$ for all $x$ and $y$. It's contrapositive states that $\neg(y \lt x)$ implies $\neg(x \lt y)$ for all $x$ and $y$, which is the symmetry condition for the negation of $\lt$. A [[symmetric preorder]] is the same thing as an equivalence relation, which means that the negation of $\lt$ is an equivalence relation. 
\end{proof}

\begin{theorem}
If the irreflexive comparison is a [[tight apartness relation]], then its negation is the [[equality relation]].
\end{theorem}

\begin{proof}
This follows from the previous two theorems. 
\end{proof}

## Examples

* If an irreflexive comparison satisfies symmetry (if $x \lt y$ then $y \lt x$ then it is an [[apartness relation]]. 

* If an irreflexive comparison is asymmetric (if $x \lt y$, then $\neg(y \lt x)$) or transitive (if $x \lt y$ and $y \lt z$, then $x \lt z$), then it is a [[strict weak order]]. 

* Connected versions of the above result in [[tight apartness relations]] and [[strict total orders]]. 

### Connected irreflexive comparisons

* An irreflexive comparison that is also a [[connected relation]] (if $x \lt y$ is false and $y \lt x$ is false, then $x = y$) is a __connected irreflexive comparison__. 

* If the set has a [[tight apartness relation]] $\neq$, then an irreflexive comparison is __strongly connected__ if $x \neq y$ implies $x \lt y$ or $y \lt x$.

## Related concepts

* [[apartness relation]]

* [[tight apartness relation]]

* [[strict total order]]

* [[strict weak order]]

* [[preorder]]

* [[partial order]]

* [[strict preorder]]


[[!redirects irreflexive comparisons]]
[[!redirects connected irreflexive comparison]]
[[!redirects connected irreflexive comparisons]]
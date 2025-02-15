
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### (0,1)-categoty theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In ordinary [[set theory]] one says:

\begin{definition}
A (binary) [[relation]] $\sim$ on a [[set]] $A$ is __transitive__ if in every chain of $3$ pairwise related elements, the first and last elements are also related:
\[
  \label{transitivity}
  \underset{
    (x, y, z \colon A)
  }
  \forall  
  \; 
  \big(
  (x \sim y) 
  \;\wedge\; 
  (y \sim z) 
  \big)
  \;\Rightarrow\; 
  (x \sim z)
  \,.
\]
\end{definition}
\begin{remark}
If (eq:transitivity) holds this way for 3 elements, then the analogue holds for any [[finite number|finite]] [[positive number]] of elements.
\end{remark}

\begin{remark}
In terms of [[category theory]], a transitive relation may be understood as a [[semicategory]] or [[magmoid]] $A$ such that for all [[objects]] $a$ and $b$ in $A$, there is no more than one [[morphism]] with [[domain]] $a$ and [[codomain]] $b$. Equivalently, a transitive relation is a semicategory or magmoid [[enriched category|enriched]] in [[truth values]]. 

Compare at *[[preorder]] -- [as a category](preorder#AsACategory)*.


In the language of the [[2-poset]] [[Rel]] of sets and relations, a relation $R \colon A \to A$ is _transitive_ if it contains its composite with itself:
$$R^2 \subseteq R$$
from which it follows that $R^n \subseteq R$ for any positive [[natural number]] $n$.  To include the case where $n = 0$, we must explicitly state that the relation is [[reflexive relation|reflexive]].
\end{remark}

\begin{remark}
Transitive relations might be understood as the most rudimentary notion of *[[orders]]*, but rarely are without further requirements. (Some discussion to this effect is at [math.SE:a/2210713](https://math.stackexchange.com/a/2210713/58526).)
\end{remark}


[[!redirects transitive relation]]
[[!redirects transitive relations]]

[[!redirects transitivity]]


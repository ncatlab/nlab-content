
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


# Reflection of limits
* table of contents
{: toc}

## Idea

A [[functor]] is said to _reflect_ [[limits]] ([[colimits]]) of a given shape if a [[cone]] ([[cocone]]) is (co-)limiting whenever its image under $F$ is.

## Definition

\begin{definition}
  \label{ReflectedLimit}
  Let $F\colon C\to D$ be a [[functor]] and $J\colon I\to C$ a [[diagram]].  We say that $F$ **reflects** [[limits]] of $J$ if whenever we have a [[cone]] $\eta\colon const^I_x \to J$ over $J$ in $C$ such that $F\cdot \eta$ is a [[limit]] of $F\circ J$ in $D$, then $\eta$ was already a limit of $J$ in $C$.
\end{definition}

Of course, a functor $F$ reflects a colimit if $F^{op}$ reflects the corresponding limit.

If $F$ reflects all limits or colimits of a given type (i.e. over a given category $I$), we simply say that $F$ reflects that sort of limit (e.g. $F$ reflects products, $F$ reflects equalizers, etc.).

## Properties

Reflection of limits is distinct from [[preservation of limits]], although there are relationships, e.g prop. \ref{ConservativeFunctors}.

\begin{proposition}
  \label{vacuous}
  If there exists at least one cone $\eta$ for $J$ such that $F \cdot \eta$ is a limit for $F \circ J$, and $F$ reflects limits of $J$, then $F$ __[[preservation of limits|preserves]]__ limits of $J$.
\end{proposition}

\begin{proof}
  Reflection implies $\eta$ is a limit for $J$ that is preserved by $F$. By [[preserved limit#vacuous|this remark]], $F$ necessarily preserves all limits of $J$.
\end{proof}

Thus, reflection of limits for a given diagram $J$ either holds vacuously, or holds together with preservation of limits for $J$.

\begin{remark}
  A functor which both reflects *and* lifts limits is said to [[created limit|create]] them.
\end{remark}

Let $F_i \colon C \to D_i$ be a family of functors, and $J \colon I \to C$ a diagram. We say that these functors **collectively reflect limits of $J$** if and only if a cone $(x, \eta)$ for $J$ that is mapped to a limit cone under all $F_i$ is a limit cone in $C$.

Given such a family, we can consider their "product" $F \colon C \to \prod_i D_i$. We have that:

\begin{proposition}
  \label{productReflectsIffCollectiveReflects}
  $F \colon C \to \prod_i D_i$ reflects limits of $J$ if and only if the functors $\pi_i \circ F \coloneqq F_i \colon C \to D_i$ collectively reflect limits of $J$.
\end{proposition}

\begin{proof}
  For the forwards direction, take a cone $(x, \eta)$ for $J$, and suppose that $(F_i(x), F_i \cdot \eta)$ is a limit cone in $D_i$ for all $i$. Then, by inspection of the universal property, $(F(x), F \cdot \eta)$ is a limit cone in $\prod_i D_i$. Thus, since $F$ reflects limits of $J$, we conclude that $(x, \eta)$ is a limit cone.

For the reverse direction, we exploit [[limit#limitProductCategoryComponentwise|limits in product categories are computed componentwise]]. Take a cone $(x, \eta)$ for $J$, and suppose it is mapped to a limit cone $(F(x), F \cdot \eta)$ for $F \circ J$ in $\prod_i D_i$. This means that $(F_i(x), F_i \cdot \eta)$ is a limit cone for $F_i \circ J$ in each $D_i$. Since the $F_i$ collectively reflect limits, this implies $(x, \eta)$ is a limit cone, as required.
\end{proof}

In the following, let $J \colon I \to C$ be a diagram, and $F \colon C \to D, G \colon D \to E$ be functors.

\begin{proposition}
  \label{compositeOfReflectingIsReflecting}
  If $F$ reflects limits of $J$ and $G$ reflects limits of $F \circ J$, then $G \circ F$ reflects limits of $J$.
\end{proposition}

\begin{proof}
  Take a cone $(x, \eta)$ for $J$ such that $((G \circ F)(x), (G \circ F) \cdot \eta)$ is a limit for $(G \circ F) \circ J$. Since $G$ reflects limits of $F \circ J$ we have that $(F(x), F \cdot \eta)$ is a limit for $F \circ J$, and then since $F$ reflects limits of $J$ we conclude $(x, \eta)$ is a limit cone, as required.
\end{proof}

\begin{proposition}
  \label{compositeReflectsSecondPreservesImpliesFirstReflects}
  If $G \circ F$ reflects limits of $J$ and $G$ preserves limits of $F \circ J$, then $F$ reflects limits of $J$.
\end{proposition}

\begin{proof}
  Take a cone $(x, \eta)$ for $J$ such that $(F(x), F \cdot \eta)$ is a limit for $F \circ J$. Since $G$ preserves this, $((G \circ F)(x), (G \circ F) \cdot \eta)$ is a limit for $(G \circ F) \circ J$. Then, since $G \circ F$ reflects this, $(x, \eta)$ is a limit for $J$, as required.
\end{proof}

Thus, if $G$ both preserves and reflects limits of $F \circ J$, then $F$ reflects limits of $J$ if and only if $G \circ F$ does.

## Examples
 {#Examples}

\begin{proposition}
  A [[faithful functor]] reflects [[epimorphisms]] and [[monomorphisms]].
\end{proposition}

The simple proof is spelled out [here](epimorphism#EpimorphismsAreReflectedByFaithfulFunctors) at _[[epimorphism]]_.


\begin{example}
  \label{FullSubcategoryInclusionReflectCoLimits}
  A [[fully faithful functor]] (hence a [[full subcategory]] inclusion) reflects all limits and colimits.
\end{example}

This is evident from inspection of the defining [[universal property]].

\begin{proposition}
  \label{ConservativeFunctors}
  A [[conservative functor]] reflects any limits which exist in its domain and that it [[preserved limit|preserves]].
\end{proposition}

\begin{proof}
  If $J$ in def. \ref{ReflectedLimit} has some limit $\theta$ which is preserved by $F$, then there is a unique induced map $\eta\to\theta$ by the universal property of a limit, which becomes an isomorphism in $D$ since $F \cdot \eta$ and $F\cdot \theta$ are both limits of $F\circ J$; hence if $F$ is conservative then it must already have been an isomorphism in $C$, and so $\eta$ was already also a limit of $J$.
\end{proof}

## Related pages

* [[preserved limit]]

* **reflected limit**

* [[created limit]]

* [[lifted limit]]

## References

* [[Emily Riehl]], §3.3 in: *[[Category Theory in Context]]*, Dover Publications (2017) &lbrack;[pdf](https://emilyriehl.github.io/files/context.pdf), [book website](http://www.math.jhu.edu/~eriehl/context/)&rbrack;
  


[[!redirects reflection of limits]]
[[!redirects reflected limits]]
[[!redirects reflected colimit]]
[[!redirects reflected colimits]]
[[!redirects reflection of colimits]]

[[!redirects reflects]]
[[!redirects reflected]]


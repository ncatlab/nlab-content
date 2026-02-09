
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

\begin{definition}
  \label{LiftedLimit}
  Let $J\colon I \to C$ be a [[diagram]] and $F\colon C \to D$ be a [[functor]]. Let $(d, \eta)$ with $\eta \colon \text{const}_d^I \to F \circ J$ be a [[limit]] for $F \circ J$. $F$ is said to _lift_ this [[limit]] if there exists a limiting [[cone]] $(c, \alpha)$ with $\alpha \colon \text{const}_c^I \to J$ such that $(F c, F \cdot \alpha)$ is isomorphic to $(d, \eta)$ in the category of cones over $F \circ J$. $F$ is said to _lift limits for_ $J$ if it lifts every limiting cone of $F \circ J$.
\end{definition}

Alternatively, this says that, if $F \circ J$ has a [[limit]], then $J$ also has a limit and that limit is [[preserved limit|preserved]] by $F$. This implies $(F c, F \cdot \alpha)$ is a limiting cone, thus a terminal object in the [[cone]] category, and thus (uniquely) isomorphic to $(d, \eta)$.

Of course, all the above applies dually to [[colimits]] - $F$ lifts colimits for $J$ if and only if $F^{op} \colon C^{op} \to D^{op}$ lifts limits for the corresponding diagram $J^{op} \colon I^{op} \to C^{op}$.

## Properties

\begin{remark}
  \label{vacuous}
  If $F$ lifts a limit $(d, \eta)$ for $F \circ J$ to $(c, \alpha)$, then it necessarily lifts any limit for $F \circ J$.
\end{remark}

\begin{proof}
  Any other limit $(d', \eta')$ for $F \circ J$ is (uniquely) isomorphic to $(d, \eta)$, and thus isomorphic to $(F c, F \cdot \alpha)$. Hence, it is lifted by $F$.
\end{proof}

Hence, lifting of limits for $J$ by $F$ either holds vacuously, or holds for all limits of $F \circ J$.

\begin{proposition}
  \label{productLiftsLimitsIffComponentsDo}
  Let $F_i \colon C \to D_i$ be a family of functors, and $J \colon I \to C$ a diagram. Then their product $F \colon C \to \prod_i D_i$ lifts limits for $J$ if and only if the components $F_i$ *collectively* lift limits for $J$, meaning a family of limit cones $(L_i, \lambda_{i, j})$ for $F_i \circ J$ can be simultaneously lifted to a limit cone for $J$.
\end{proposition}

\begin{proof}
  We exploit [[limit#limitProductCategoryComponentwise|limits in product categories are computed componentwise]]. So, limits for $F \circ J$ correspond to families of limits for $F_i \circ J$. By unfolding definitions, $F$ lifts limits for $J$ precisely if the $F_i$ collectively lift limits for $J$.
\end{proof}

In the following, $J \colon I \to C$ is a diagram and $F \colon C \to D, G \colon D \to E$ are functors.

\begin{proposition}
  \label{compositeOfLiftingsLifts}
  Suppose $F$ lifts limits for $J$ and $G$ lifts limits for $F \circ J$. Then $G \circ F$ lifts limits for $J$.
\end{proposition}

\begin{proof}
  Take a limit cone over $(G \circ F) \circ J$. Since $G$ lifts limits for $F \circ J$, this can be lifted to a limit cone for $F \circ J$ that $G$ preserves. And then, since $F$ lifts limits for $J$, this can be lifted to a limit cone for $J$ that $F$ preserves, which implies $G \circ F$ also preserves it, as requires.
\end{proof}

\begin{proposition}
  \label{compositeLiftsFirstPreservesSecondLifts}
  Suppose $G \circ F$ lifts limits for $J$ and $F$ preserves limits of $J$. Then $G$ lifts limits for $F \circ J$.
\end{proposition}

\begin{proof}
  Take a limit cone $(z, \alpha)$ for $(G \circ F) \circ J$. Then since $G \circ F$ lifts this, we obtain a limit cone $(x, \mu)$ for $J$ that $G \circ F$ preserves. This implies $(F(x), F \cdot \mu)$ is a limit cone for $F \circ J$ which $G$ preserves, as required.
\end{proof}

\begin{proposition}
  \label{compositeLiftsSecondPreservesReflectsFirstLifts}
  Suppose $G \circ F$ lifts limits for $J$ and $G$ preserves and reflects limits of $F \circ J$. Then $F$ lifts limits for $J$.
\end{proposition}

\begin{proof}
  Take a limit cone $(y, \mu)$ for $F \circ J$. Since $G$ preserves this, $(G(y), G \cdot \mu)$ is a limit for $(G \circ F) \circ J$. Then, since $G \circ F$ lifts this, there is a limit cone $(x, \eta)$ for $J$ preserved by $F \circ G$. Finally, since $G$ additionally reflects limits for $F \circ J$, we conclude that $F$ preserves $(x, \eta)$ too, as required.
\end{proof}

The propositions above show that:

* If $F$ preserves limits of $J$ and lifts limits for $J$, then $G$ lifts limits for $F \circ J$ if and only if $G \circ F$ lifts limits for $J$.
* If $G$ preserves and reflects limits of $F \circ J$, and lifts limits for $F \circ J$, then $F$ lifts limits of $J$ if and only if $G \circ F$ does.

## Strictness

\begin{definition}
  \label{strict}
  $F$ is said to lift limits for $J$ __strictly__ if it lifts limits for $J$ and moreover, in the notation of \ref{LiftedLimit}, $(F c, F \cdot \alpha) = (d, \eta)$.
\end{definition}

This is often how the definition is phrased in textbooks, but it is not invariant under [[equivalence of categories]]. However, in practice many functors that lift limits do so strictly.

\begin{definition}
  \label{unique}
  $F$ is said to lift limits for $J$ __uniquely__ if it strictly lifts limits for $J$ and moreover, in the notation of \ref{LiftedLimit}, there is a unique limiting cone $(c, \alpha)$ with $(Fc, F \cdot \alpha) = (d, \eta)$.
\end{definition}

Again, this is too strict to be invariant under equivalence of categories. If we relax strictness, then this actually holds automatically - any other limiting cone $(c', \alpha')$ with $(F c', F \cdot \alpha') \cong (d, \eta)$ is in particular a limit for $J$, and so (uniquely) isomorphic to $(c, \alpha)$.

## Relation to preservation and reflection

\begin{remark}
  \label{vacuousPreserve}
  If $F$ lifts limits for $J$, and there exists at least one limiting cone $(d, \eta)$ for $F \circ J$, then $F$ __[[preservation of limits|preserves]]__ limits of $J$.
\end{remark}

\begin{proof}
  This is because, in the notation of \ref{LiftedLimit}, the lift $(c, \alpha)$ is preserved by $F$, which by [[preserved limit#vacuous|this remark]] implies all limits for $J$ are preserved by $F$.
\end{proof}

Thus, lifting of limits either holds vacuously, or holds together with preservation of limits.

In general, [[reflection of limits]] neither implies nor is implied by lifting:

* If $F$ reflects limits for $J$, then any cone in $C$ whose image under $F$ is limiting must have already been limiting - but since this requires us to start with a cone in $C$, this cannot be used to lift a limit for $F \circ J$.

* Conversely, if $F$ lifts limits for $J$, and $(c, \alpha)$ is a cone in $C$ such that $(F c, F \cdot \alpha)$ is limiting, then there exists a limiting cone $(c', \alpha')$ for $J$ in $C$ preserved by $F$. This gives a canonical morphism $c \to c'$ induced by the universal property, but in general this may not be an isomorphism. So we cannot conclude that $(c, \alpha)$ is limiting.

## Examples

* The [[forgetful functor]] $Top \to Set$ lifts limits and colimits of all small diagrams (and hence preserves them, since $Set$ is a [[bicomplete category]]). However, it does not reflect them - in general there are many possible lifts for a diagram, even strictly, by choosing coarser/finer topologies as appropriate, and not all of these can be limits/colimits.

* Any functor that [[created limit|creates limits]] necessarily lifts them. In particular, [[monadic functor|monadic functors]] lift limits, often strictly.

## Terminological remarks

Lifting limits is closely related to [[created limits|creating them]].  The relationships between these notions were the subject of a post by Aleks Kissinger at the categories mailing list, [here](https://raw.githubusercontent.com/punkdit/categories/26b751bbcbe6765fe447e805629ff6416f4c38b1/gmane/science/mathematics/categories/6644), but there is [some dispute](https://nforum.ncatlab.org/discussion/7024/lifted-limit/?Focus=56765#Comment_56765) about its correctness.

## Related concepts

* [[preserved limit]]

* [[reflected limit]]

* [[created limit]]

* [[topological concrete category]] 

* **lifted limit** 

[[!redirects lifted limits]]

## References

See Definition 13.17 in [[Adamek]], [[Herrlich]], [[Strecker]]: [Abstract and Concrete Categories](http://katmat.math.uni-bremen.de/acc/acc.pdf).  Remark 13.38 provides a useful diagram of relations between reflected/created/lifted limits.

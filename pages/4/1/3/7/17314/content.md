
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

\begin{remark}
  \label{vacuous}
  If $F$ lifts a limit $(d, \eta)$ for $F \circ J$ to $(c, \alpha)$, then it necessarily lifts any limit for $F \circ J$.
\end{remark}

\begin{proof}
  Any other limit $(d', \eta')$ for $F \circ J$ is (uniquely) isomorphic to $(d, \eta)$, and thus isomorphic to $(F c, F \cdot \alpha)$. Hence, it is lifted by $F$.
\end{proof}

Hence, lifting of limits for $J$ by $F$ either holds vacuously, or holds for all limits of $F \circ J$.

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

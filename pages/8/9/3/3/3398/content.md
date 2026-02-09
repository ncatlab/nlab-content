

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



# Preservation of limits
* table of contents
{: toc}


## Idea

If $J\colon I \to C$ is a [[diagram]] and $x$ is a [[limit]] of it in $C$, then we may na&#239;vely say that this limit is _preserved_ by a [[functor]] $F\colon C \to D$ if $F(x)$ is a limit of the [[composite]] diagram $I \overset{J}\to C \overset{F}\to D$.  However, it is not enough to state this at the level of objects; we also need to impose some coherence conditions, preserving the entire universal [[cone]].  Furthermore, we can use a trick involving the [[Yoneda embedding]] to get a meaningful condition even if $J$ has no limit in $C$ at all.


## Definitions

\begin{definition}
Let $F\colon C \to D$ be a [[functor]], $J\colon I \to C$ a [[diagram]], and $\eta \colon const^I_x \to J$ be a [[cone]] over $J$. Suppose $(x, \eta)$ is a [[limit]] for $J$. The functor $F$ __preserves__ this limit if $(F(x), F \cdot \eta)$ is a limit of $F \circ J$.
\end{definition}

Here, $F\cdot\eta\colon \const^I_{F(x)} \to F \circ J$ is a [[whiskering]].

Dually, $F$ __preserves__ a [[colimit]] of $J$ if $F^\op\colon C^\op \to D^\op$ preserves it as a limit of $J^\op\colon I^\op \to C^\op$.

For instance:

* Let $I$ be the [[empty category]], so that a limit of the unique functor $J\colon I \to C$ is a [[terminal object]] $1$.  Then $F$ preserves this terminal object if and only if $F(1)$ is a terminal object of $D$.

* Let $I$ be the [[discrete category]] $\mathbf{2}$, so that $J$ picks out two objects $a$ and $b$ of $C$ and the limit of $J$ is a [[product]] $a \times b$ of $a$ and $b$.  Note that this product comes equipped with product projections $\pi\colon a \times b \to a$ and $\rho\colon a \times b \to b$.  Then $F$ preserves this product if and only if $F(a \times b)$ is a product of $F(a)$ and $F(b)$ and furthermore the product projections are $F(\pi)$ and $F(\rho)$.

\begin{definition}
  If $F$ preserves all limits/colimits for a specified diagram $J\colon I \to C$, we say that $F$ preserves limits of $J$.
\end{definition}

If $F$ preserves all limits or colimits of a given type (i.e. over a given category $I$), we simply say that $F$ preserves that sort of limit (e.g. $F$ preserves [[products]], $F$ preserves [[equalizers]], etc.).

\begin{definition}
  A functor that preserves all small limits in $C$ that exist is called a __[[continuous functor]]__.
\end{definition}

Usually this term is only used when $C$ has all small limits, i.e. is a [[complete category]].

## Properties

\begin{proposition}
  \label{vacuous}
  If there exists at least one limit $(x, \eta)$ for $J$ that is preserved by $F$, then every limit for $J$ is preserved by $F$.
\end{proposition}

\begin{proof}
  Any other limit $(y, \mu)$ is uniquely isomorphic to $(x, \eta)$, and $F$ preserves this isomorphism (as all functors do). This implies $(F(y), F \cdot \mu)$ is a limit for $F \circ J$.
\end{proof}

Thus, for a specified diagram $J\colon I \to C$, preservation of limits either holds vacuously (if $J$ has no limit in $C$), or holds for all limit cones over $J$.

\begin{proposition}
  \label{comparisonMap}
  Suppose $(x, \eta)$ is a limit for $J$ and $(y, \mu)$ is a limit for $F \circ J$. Since $(F(x), F \cdot \eta)$ is a cone over $F \circ J$, there is a canonical comparision map $f \colon F(x) \to y$ with $(F \cdot \eta)_j = \mu_j \circ f$ for each $j \in I$. Then $F$ preserves $(x, \eta)$ if and only if this comparision map is an isomorphism.
\end{proposition}

\begin{proof}
  $F$ preserves $(x, \eta)$ if and only if $(F(x), F \cdot \eta)$ is a limit for $F \circ J$. Since $(y, \mu)$ is already a limit for $F \circ J$, that is if and only if $(F(x), F \cdot \eta)$ is isomorphic to $(y, \mu)$ in the category of cones over $F \circ J$. And since $(y, \mu)$ is terminal in this category, that's if and only if the comparison map, between the unique morphism $(F(x), F \cdot \eta) \to (y, \mu)$ in the cone category, is an isomorphism.
\end{proof}

\begin{proposition}
  \label{productPreservesIffComponentsPreserve}
  Let $F_i \colon C \to D_i$ be a family of functors, and $J \colon I \to C$ a diagram. Then every $F_i$ preserves limits of $J$ if and only if their product $F \colon C \to \prod_i D_i$ preserves limits of $J$.
\end{proposition}

\begin{proof}
  We exploit [[limit#limitProductCategoryComponentwise|limits in product categories are computed componentwise]]. If every $F_i$ preserves a limit $(x, \eta)$ of $J$, then the $(F_i(x), F_i \cdot \eta)$ collectively determine a limit $(F(x), F \cdot \eta)$, so that $F$ preserves this. Conversely, if $F$ preserves the limit, then limits being computed componentwise implies each $F_i$ preserves the limit.
\end{proof}

For the following properties, we have $J \colon I \to C$ a diagram, and $F \colon C \to D, G \colon D \to E$ functors.

\begin{proposition}
  \label{compositionsOfLimitPreservingAreLimitPreserving}
  If $F$ preserves limits of $J$ and $G$ preserves limits of $F \circ J$, we have that $G \circ F$ preserves limits of $J$.
\end{proposition}

\begin{proof}
  Take a limit $(x, \eta)$ for $J$. Then $(F(x), F \cdot \eta)$ is a limit for $F \circ J$ since $F$ preserves this limit, and then $((G \circ F)(x), (G \circ F) \cdot \eta)$ is a limit for $(G \circ F) \circ J$ since $G$ preserves this limit, as required.
\end{proof}

\begin{proposition}
  \label{compositePreservesAndSecondReflectsImpliesFirstPreserves}
  If $G \circ F$ preserves limits of $J$ and $G$ [[reflected limit|reflects]] limits of $F \circ J$, we have that $F$ preserves limits of $J$.
\end{proposition}

\begin{proof}
  Take a limit $(x, \eta)$ for $J$. We want to show $(F(x), F \cdot \eta)$ is a limit for $F \circ J$. Since $G$ reflects limits of $F \circ J$, it suffices to show $((G \circ F)(x), (G \circ F) \cdot \eta)$ is a limit for $(G \circ F) \circ J$. But this follows since $G \circ F$ preserves limits of $J$.
\end{proof}

\begin{proposition}
  \label{compositePreservesAndFirstLiftsImpliesSecondPreserves}
  If $G \circ F$ preserves limits of $J$ and $F$ [[lifted limit|lifts]] limits for $J$, we have that $G$ preserves limits of $F \circ J$.
\end{proposition}

\begin{proof}
  Take a limit $(y, \mu)$ for $F \circ J$. We want to show $(G(y), G \cdot \mu)$ is a limit for $(G \circ F) \circ J$. Since $F$ lifts limits for $J$, there is some limit cone $(x, \eta)$ over $J$ with $(F(x), F \cdot \eta) \cong (y, \mu)$ in the category of cones over $F \circ J$. Thus, $((G \circ F)(x), (G \circ F) \cdot \eta) \cong (G(y), G \cdot \mu)$ in the category of cones over $(G \circ F) \circ J$. But the former is a limit for $(G \circ F) \circ J$ since $G \circ F$ preserves limits of $J$, implying the latter is too.
\end{proof}

The propositions above taken together imply the following:

* If $G$ preserves and reflects limits of $F \circ J$, then $F$ preserves limits of $J$ if and only if $G \circ F$ does.
* If $F$ preserves and lifts limits of $J$, then $G$ preserves limits of $F \circ J$ if and only if $G \circ F$ preserves limits of $J$.

## Examples
  {#Examples}

* [[limits preserve limits]]

* [[hom-functors preserve limits]]

* [[adjoints preserve (co-)limits]]

* {#ExampleYonedaEmbedding} the [[Yoneda embedding]] preserves limits (see [there](Yoneda+embedding#PreservesLimits))


## Preservation of weighted limits

Analogously, an [[enriched functor]] between [[enriched categories]] may preserve [[weighted limits]].  Are there any tricky points that we should mention?


## Preservation of limits that don\'t exist

Sometimes we want to say that a functor $F\colon C \to D$ preserves a limit that does not actually exist in $C$.  For instance, a __finitely continuous functor__ is usually defined as one that preserves all finite limits.  If $C$ is a [[finitely complete category]], then this is fine; such a functor is called __[[left exact functor|left exact]]__.  But what if $C$ does not have all finite limits?

If $C$ and $D$ are [[locally small category|locally small]], then we can use the [[Yoneda lemma]] to turn the question into one involving categories that *do* have the required limits (and in fact have all limits), the [[presheaf categories]] $[C^op,Set]$ and $[D^op,Set]$.  (For colimits, use $[C,Set]$ and $[D,Set]$; for $V$-enriched categories, use $[C^op,V]$ and $[D^op,V]$, which will work if $V$ is complete.)

The left [[Kan extension]] of the composite $C \overset{F}\to D \overset{Yon}\hookrightarrow [D^\op,Set]$ along the [[Yoneda embedding]] $C \overset{Yon}\hookrightarrow [C^\op,Set]$ (which always exists) is a functor from $[C^op,Set]$ to $[D^op,Set]$, which may be written as $- \otimes F$ (alluding to the [[bimodule]] nature of [[profunctors]]).  A diagram $J\colon I \to C$ becomes a diagram $I \overset{J}\to C \overset{Yon}\hookrightarrow [C^op,Set]$ in $[C^op,Set]$, where it has a limit.  If $- \otimes F$ preserves this limit, then we say that $F$ __preserves__ the hypothetical limit of $J$.

Since the Yoneda embedding preserves and [[reflected limit|reflects]] all limits, if $J$ has a limit in $C$, then this condition is equivalent to the condition that $F$ preserve it in the ordinary sense, but in general it is stronger than requiring that $F$ preserve the limit only if it exists in $C$.

Finishing the motivating example, a __[[flat functor]]__ may be defined as one that preserves all finite limits, whether or not they exist.

## Related concepts

* ([[cocontinuous functor|co]])[[continuous functor]]

* [[reflected limit]]

* [[created limit]]

* [[lifted limit]]

## References

* [[Saunders MacLane]], §V.4 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (1971, second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;


* [[Francis Borceux]], §2.4 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory* &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;

* [[Emily Riehl]], §3.3 in: *[[Category Theory in Context]]*, Dover Publications (2017) &lbrack;[pdf](https://emilyriehl.github.io/files/context.pdf), [book website](http://www.math.jhu.edu/~eriehl/context/)&rbrack;


[[!redirects preserved limit]]
[[!redirects preserved limits]]
[[!redirects preserves limits]]
[[!redirects preservation of limits]]
[[!redirects preserved colimit]]
[[!redirects preserved colimits]]
[[!redirects preserves colimits]]
[[!redirects preservation of colimits]]

[[!redirects preserves]]
[[!redirects preserved]]

[[!redirects preserves colimits]]
[[!redirects preserve colimits]]
[[!redirects preserving colimits]]


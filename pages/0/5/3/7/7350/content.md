
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



# $L$-finite categories
* table of contents
{: toc}

## Definition
 {#Definition}

\begin{proposition}\label{CharacterizationsOfLFiniteLimits}
**(characterizations of L-finite limits)** \linebreak
A [[category]] $C$ is **$L$-finite** if the following equivalent conditions hold, which are all equivalent:

* The [[terminal object]] of the [[functor category]] $[C,Set]$ to [[Set]] is ($\omega$-)[[compact object|compact]].

* $C$-[[limits]] [[commutativity of limits and colimits|commute]] with [[filtered colimits]] in [[Set]].

* $C$ has an [[initial functor|initial]] [[finitely generated category|finitely generated]] [[subcategory]].

* $C$ admits an [[initial functor]] from a [[finite category]].[^1]

* $C$-limits lie in the [[saturated class of limits|saturation]] of the class of [[finite limits]].

\end{proposition}
([Paré 1990, p. 740 (10 of 16), around Prop. 7](#Pare90))

\begin{remark}\label{RelationTkKFiniteness}
**(relation to K-finite sets)** \linebreak
The notion of L-finite category (Def. \ref{CharacterizationsOfLFiniteLimits}) is a sort of [[vertical categorification|categorification]] of the notion of [[K-finite set]]:

* A set $X$ is $K$-finite if the [[top element]] $1 \in \Omega^X$ belongs to the closure of the [[singletons]] under finite [[unions]].

* A category $C$ is $L$-finite if the terminal object $1\in Set^C$ belongs to the closure of the [[representable functor|representables]] under [[finite colimits]].

\end{remark}

In [Paré 1990, p. 741 (11 0f 16)](#Pare90) this observation is attributed to [[Richard Wood]]. 

## Examples

\begin{example}\label{CategoriesWithInitialObjectAreLFinite}
**(categories with initial objects are L-final)** \linebreak
  Any category $\mathcal{C}$ with an [[initial object]] $\varnothing \,\in\, \mathcal{C}$ is L-finite, with the inclusion of the [[terminal category]] mapping to this initial object
$\{\varnothing\} \xhookrightarrow{\;} \mathcal{C}$
being an [[initial functor]] (by [this exp.](final+functor#InclusionOfATerminalObjectIsFinal)) as required by Def. \ref{CharacterizationsOfLFiniteLimits}.
\end{example}

## Related concepts

* [[finite category]]

* [[filtered colimit]]

* [[sound doctrine]]

## References

* {#Pare90} [[Robert Paré]], Section 3 of: *Simply connected limits*.  Can. J. Math., Vol. XLH, No. 4, 1990, pp. 731-746 ([doi:10.4153/CJM-1990-038-6](https://doi.org/10.4153/CJM-1990-038-6))
 

[^1]: There is a typo in [Paré Prop. 7](#Pare90) in the statement of this equivalence: it says "[[final functor|final]]" instead of "[[initial functor|initial]]".


[[!redirects L-finite category]]
[[!redirects L-finite categories]]
[[!redirects L-finite limit]]
[[!redirects L-finite limits]]
[[!redirects L-finite colimit]]
[[!redirects L-finite colimits]]

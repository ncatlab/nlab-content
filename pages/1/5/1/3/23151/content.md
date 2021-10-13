
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

Given a [[category]] $\mathcal{C}$, its *free coproduct completion* (or *free sum completion*) is [[generalized the|the]] category $PSh_{\sqcup}(\mathcal{C})$ (often denoted $Fam(\mathcal{C})$, for *[[families]]* in $\mathcal{C}$) obtained by [[free construction|freely]] adjoining [[coproducts]] of all [[objects]] of $\mathcal{C}$. 

(The following description is pretty immediate, but see also [Hu & Tholen 1995, p. 281, 286](#HuTholen95).)

An explicit description of $PSh_{\sqcup}(\mathcal{C})$ is: 

* Its [[objects]] are [[pairs]] consisting of 

  1. an index [[set]] $I \in $ [[Set]] 

  1. an $I$-[[indexed set]] $\big( X_i  \in \mathcal{C} \big)_{i \in I}$ of [[objects]] of $\mathcal{C}$.

* Its [[morphisms]] $\big( X_i \big)_{i \in I} \xrightarrow{ \; ( \phi_i )_{i \in I} \; } \big( Y_j \big)_{j \in J} $ [[pairs]] consisting of 

  * a [[function]] of index sets $f \,\colon\, I \xrightarrow J$.

  * an $I$-[[indexed set]] of [[morphisms]] $\phi_i \,\colon\, X_i \xrightarrow{\;} Y_{f(j)}$ in $\mathcal{C}$.


* The [[composition]]-law and [[identity morphisms]] are the evident ones.

Slightly more abstractly, this is [[equivalence of categories|equivalently]] the [[full subcategory]] 

$$
  PSh_{\sqcup}(\mathcal{C})
  \xhookrightarrow{\;}
  PSh(\mathcal{C})
$$

of the [[category of presheaves]] over $\mathcal{C}$ on those which are [[coproducts]] of [[representables]]. The latter is the [[free cocompletion]] of $\mathcal{C}$ under *all* [[small colimit|small]] [[colimits]].

The [[Yoneda embedding]] hence factors through the free coproduct completion

$$
  y
  \;\colon\;
  \mathcal{C}
  \xhookrightarrow{\;}
  PSh_{\sqcup}(\mathcal{C})
  \xhookrightarrow{\;}
  PSh(\mathcal{C})
$$

Notice that the first inclusion here does *not* [[preserved colimit|preserve]] [[coproducts]] (coproducts are freely adjoined irrespective of whether $\mathcal{C}$ already had some coproducts), but the second does. Both inclusions [[preserved limit|preserve]] those [[limits]] that exist.

## Properties

Fairly immediate from the explicit definition above is:

\begin{proposition}\label{CategoriesOfCoproductsOfConnectedObjects}
  A [[category]] $\mathcal{B}$ is [[equivalence of categories|equivalent]] to a [[free coproduct completion]] $PSh_{\sqcup}(\mathcal{C})$ for a [[small category]] $\mathcal{C}$ if 

1. $\mathcal{C} \xhookrightarrow{\;} \mathcal{B}$ is a [[full subcategory]] of [[connected objects]], 

   i.e. $X \,\in\, \mathcal{C} \hookrightarrow \mathcal{B}$ means that the [[hom-functor]] $\mathcal{B}(X,-) \,\colon\, \mathcal{B} \to Set$ [[preserved colimit|preserves]] [[coproducts]]

   (which when $\mathcal{C}$ is [[extensive category|extensive]] means equivalently that if $X$ is a coproduct, then one of the summands is [[initial object|initial]], by [this Prop.](InExtensiveCategoryCOnnectedObjectsArePrimitiveUnderCoproduct));

1. each object of $\mathcal{B}$ is a [[coproduct]] of objects in $\mathcal{C} \hookrightarrow \mathcal{B}$.

\end{proposition}
([Carboni & Vitale 1998, Lem. 42](#CarboniVitale98))

\begin{prop}
  Any free coproduct completion is an [[extensive category]].
\end{prop}
(e.g. [Carboni, Lack & Walters 1993](#CarboniLackWalters93))


## Examples
 {#Examples}

The following examples follow as special cases of Prop. \ref{CategoriesOfCoproductsOfConnectedObjects}.

\begin{example}
The category [[Set]] is the [[free coproduct completion]] of the [[terminal category]].
\end{example}

\begin{example}\label{GActionsAndGOrbits}
**([[G-set|$G$-sets]] are the [[free coproduct completion]] of [[orbit category|$G$-orbits]])**
\linebreak
  Let $G \,\in\, Grp(Set)$ be a [[discrete group]]. Write

* [[G-set|$G Set$]] for its category of [[group actions]] on [[sets]], 

* $G Orbt \xhookrightarrow{\;} G Set$ for its [[orbit category]], the [[full subcategory]] on the [[transitive actions]], hence the [[coset space|sets of cosets]] $G/H$, for [[subgroups]] $H \subset G$.

Since every [[G-set]] $X$ decomposes as a [[disjoint union]] of [[transitive actions]], namely of [[orbits]] of [[elements]] of $X$, this inclusion exhibits $G Set$ as the [[free coproduct completion]] of [[orbit category|G Orbt]].
\end{example}



## Related concepts

* [[free cocompletion]], [[idempotent completion]], [[Cauchy completion]]

* [[free cartesian category]]

## References


On [[limits]] in free coproduct completions:

* {#HuTholen95} Hongde Hu, [[Walter Tholen]], *Limits in  free  coproduct completions*, Journal of  Pure  and  Applied  Algebra 105 (1995) 277-291 (<a href="https://doi.org/10.1016/0022-4049(94)00153-7">doi:10.1016/0022-4049(94)00153-7</a>, [pdf](https://core.ac.uk/download/pdf/82604415.pdf))

In the context of [[regular and exact completions]]:

* {#CarboniVitale98} [[Aurelio Carboni]], [[Enrico Vitale]], *Regular and exact completions*, Journal of Pure and Applied Algebra **125** 1–3  (1998) 79-116 (<a href="https://doi.org/10.1016/S0022-4049(96)00115-6">doi:10.1016/S0022-4049(96)00115-6</a>)

In the general context of [[extensive categories]]:

* {#CarboniLackWalters93} [[Aurelio Carboni]], [[Stephen Lack]], [[Bob Walters|R. F. C. Walters]], _Introduction to extensive and distributive categories_, JPAA **84** (1993) pp. 145-158 (<a href="https://doi.org/10.1016/0022-4049(93)90035-R">doi:10.1016/0022-4049(93)90035-R</a>)


[[!redirects free coproduct completions]]

[[!redirects free coproduct cocompletion]]
[[!redirects free coproduct cocompletions]]

[[!redirects free coproduct-cocompletion]]
[[!redirects free coproduct-cocompletions]]

[[!redirects free sum completion]]
[[!redirects free sum completions]]


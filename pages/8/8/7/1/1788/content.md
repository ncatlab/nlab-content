
\begin{definition}
Given 

* $k$ be a separably closed field,

* $\kappa$ be an uncountable [[strong limit cardinal]]

write

* $Sch^{\leq \kappa}_{/Spec(k)}$ for the category of $\kappa$-small [[schemes]] over $Spec(k)$, 

* $Sch^{\leq \kappa}_{/_{pet} Spec(k)}$ for its [[full subcategory]] of those that are [[pro-étale morphism of schemes|pro-étale]] over $Spec(k)$, 

  [[equivalence of categories|equivalently]] this is the category of $\kappa$-small [[profinite sets]],

both regarded as [[sites]] via the [[pro-étale site|pro-étale topology]] and write

\[
  \label{TheGeometricMorphism}
  Sh\big( Sch^{\leq \kappa}_{/Spec(k)}\big) 
  \underoverset{\underset{i_\ast}{\longrightarrow}}{\overset{i^\ast}{\longleftarrow}}{\;\; \bot \;\;} 
  Sh\big( Sch^{\leq \kappa}_{/Spec(k)}\big) 
\]

for the canonical [[geometric morphism]].
\end{definition}

\begin{remark}
\label{TerminologyOfCondensedSets}
  The [[base topos]] in (eq:TheGeometricMorphism) is equivalently called the category of $\kappa$-*[[condensed sets]]*.
\end{remark}

The following seems to be claimed:
\begin{prop}
  The geometric morphism (eq:TheGeometricMorphism) has the following properties:

* $i^\ast$ is [[fully faithful functor|fully faithful]];

* $i_\ast$ is a [[left adjoint]]

and

* $i^\ast$ is a [[right adjoint]].

\end{prop}
The first two claims are fairly standard, the last one would make the topos of pro-étale schemes be [[locally connected topos|locally connected]] and hence *almost* [[cohesive topos|cohesive]] over $\kappa$-[[condensed sets]] (by Rem. \ref{TerminologyOfCondensedSets}).




+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _finite intersection property_ on a set of [[subsets]] says that every [[finite number]] of them has [[inhabited set|non-empty]] [[intersection]] (def. \ref{FiniteIntersectionProperty} below).

This property is typically used in order to re-formulate the condition on [[topological space]] to be [[compact topological space|compact]] in terms of [[closed subsets]] (prop. \ref{CompactnessInTermsOfFiniteIntersectionProperty} below).

The formulation of compactness in terms of the finite intersection property is useful for proving the [[Tychonoff theorem]] as well as for proving that [[compact spaces equivalently have converging subnet of every net|compact spaces are equivalently those for which every net has a converging subnet]].

## Statement

+-- {: .num_defn #FiniteIntersectionProperty}
###### Definition
**(finite intersection property)**

Let $X$ be a [[set]]. Then a set of [[subsets]] $\{S_i \subset X\}_{i \in I}$ is said to satify the _finite intersection property_ if for every [[finite set|finite subset]] $J \subset I$ the corresponding intersection is [[inhabited]]: $\underset{i \in J \subset I}{\cap} S_i \neq \emptyset$.

=--

## Relation to compact topological spaces

+-- {: .num_prop #CompactnessInTermsOfFiniteIntersectionProperty}
###### Proposition

Let $(X,\tau)$ be a [[topological space]]. 

Assuming [[excluded middle]], then:

The following are equivalent.

1. $(X, \tau)$ is a [[compact topological space]] in the sense that for every [[open cover]] $\{U_i \subset X\}_{i \in I}$ there is a [[finite set|finite]] [[subset]] $J \subset I$ such that $\{U_i \subset X\}_{i \in J \subset I}$ is still a cover.


1. Every set of [[closed subsets]] $\{C_i \subset X\}_{i \in I}$ which satisfies the finite intersection property (def. \ref{FiniteIntersectionProperty}) has even [[inhabited set|non-empty]] total intersection $\underset{i \in I}{\cap} C_i \neq \emptyset$.

=--

+-- {: .proof}
###### Proof

In one direction, assume that $(X,\tau)$ is compact, and that $\{C_i \subset X\}_{i \in I}$ satisfies the finite intersection property. We need to show that then $\underset{i \in I}{\cap} C_i \neq \emptyset$.

Assume that this were not the case, hence assume that $\underset{i \in I}{\cap} C_i = \emptyset$. This would imply that the open [[complements]] $U_i \coloneqq X \backslash C_i$ were an [[open cover]] of $X$, because (using [[de Morgan's law]])

$$
  \begin{aligned}
    \underset{i \in I}{\cup} U_i
    & \coloneqq
    \underset{i \in I}{\cup} X \backslash C_i
    \\
    & = X \backslash \left( \underset{i \in I}{\cap}C_i \right)
    \\
    & X \backslash \emptyset
    \\
    & = X
  \end{aligned}
  \,.
$$

But then by compactness of $(X,\tau)$ there were a finite subset $J \subset I$ such that $\{ U_i \subset X\}_{i \in J \subset I}$ were still an open cover, hence that $\underset{i \in J \subset I}{\cup} U_i = X $. Translating this back through the [[de Morgan's law]] again this would mean that

$$
  \begin{aligned}
    \emptyset 
       & = 
    X \backslash 
    \left( 
      \underset{i \in J \subset I}{\cup} U_i
    \right)
    \\
    & \coloneqq
    X \backslash 
    \left( 
      \underset{i \in J \subset I}{\cup} X \backslash C_i
    \right) 
    \\
    & = \underset{i \in J \subset I}{\cap} X \backslash \left( X \backslash C_i\right)
    \\
    & =
    \underset{i \in J \subset I}{\cap}  C_i
    \,.
  \end{aligned}
$$

This would be in contradiction with the finite intersection property of $\{C_i \subset X\}_{i \in I}$, and hence we have [[proof by contradiction]].

Conversely, assume that every set of closed subsets in $X$ with the finite intersection property has non-empty total intersection. We need to show that the every open cover $\{U_i \subset X\}_{i \in I}$ of $X$ has a finite subcover.

Write $C_i \coloneqq X \backslash U_i$ for the closed complements of these open subsets. 

Assume that there were no finite subset $J \subset I$ such that $\underset{i \in J \subset I}{\cup} U_i = X$. By [[de Morgan's law]] this means equivalently that there were no finite subset $J$ such that $\underset{i \in J \subset I}{\cap} C_i = \emptyset$, hence it would mean that $\{C_i \subset X\}_{i \in I }$ satisfied the finite intersection property. 

But by assumption this would then imply that $\underset{i \in I}{\cap} C_i \neq \emptyset$, which, again by de Morgan, would mean that $\underset{i \in I}{\cup} U_i \neq X$. But this contradicts the assumption that the $\{U_i \subset X\}_{i \in I}$ are a cover. Hence we have a [[proof by contradiction]].


=--


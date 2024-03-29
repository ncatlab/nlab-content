
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



+-- {: .num_theorem} 
###### Theorem 

For any $a \lt b \in \mathbb{R}$ the [[closed interval]]

$$
  [a,b] \subset \mathbb{R}
$$

regarded with its [[topological subspace|subspace topology]]
of [[Euclidean space]] with its [[metric topology]] is
a [[compact topological space]]. 
=-- 


+-- {: .proof}
###### Proof

Since all the closed intervals are [[homeomorphism|homeomorphic]]
it is sufficient to show the statement for $[0,1]$. Hence let $\{U_i \subset [0,1]\}_{i \in I}$ be an [[open cover]]. We need to show that it has an [open subcover](/nlab/show/compact+space#OpenCover).

Say that an element $x \in [0,1]$ is _admissible_ if the closed sub-interval $[0,x]$ is covered by
finitely many of the $U_i$. In this terminology, what we need to show is that $1$ is admissible.

Observe from the definition that

1. 0 is admissible,

1. if $y \lt x \in [0,1]$ and $x$ is admissible, then also $y$ is admissible.

This means that the set of admissible $x$ forms either

1. an [[open interval]] $[0,g)$

1. or a [[closed interval]] $[0,g]$,

for some $g \in [0,1]$. We need to show that the latter is true, and for $g = 1$. We do so by observing that the alternatives lead to [[contradictions]]:

1. Assume that the set of admissible values were an open interval $[0,g)$. Pick an $i_0 \in I$ such that $g \in U_{i_0}$ (this exists because of the covering property). Since such $U_{i_0}$ is an open neighbourhood of $g$, there is a positive real number $\epsilon$ such that the open ball $B^\circ_g(\epsilon) \subset U_{i_0}$ is still contained in the patch. It follows that there is an element $x \in B^\circ_g(\epsilon) \cap [0,g) \subset U_{i_0} \cap [0,g)$ and such that there is a finite subset $J \subset I$ with $\{U_i \subset [0,1]\}_{i \in J \subset I}$ a finite open cover of $[0,x)$. It follows that $\{U_i \subset [0,1]\}_{i \in J \subset I} \sqcup \{U_{i_0}\}$ were a finite open cover of $[0,g]$, hence that $g$ itself were still admissible, in contradiction to the assumption. 

1. Assume that the set of admissible values were a closed interval $[0,g]$ for $g \lt 1$.
   By assumption there would then be a finite set $J \subset I$ such that $\{U_i \subset [0,1]\}_{i \in J \subset I}$
   were a finite cover of $[0,g]$. Hence there would be an index $i_g \in J$ such that $g \in U_{i_g}$.
   But then by the nature of open subsets in the Euclidean space $\mathbb{R}$, this $U_{i_g}$ would also
   contain an open ball $B^\circ_g(\epsilon) = (g-\epsilon, g + \epsilon)$. This would mean that
   the set of admissible values includes the open interval $[0,g+ \epsilon)$, contradicting the assumption.

This gives a [[proof by contradiction]].

=--


[[!redirects closed intervals are compact]]



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

Loosely speaking, the **boundary** of a subset $S$ of topological space $X$ consists of those points in $X$ that are neither 'fully in' $S$ nor are 'fully not in' $S$.

## Definition

### Of a subset of a topological space

For $S \subset X$ a [[subset]] of a [[topological space]] $X$, the **boundary** or **frontier** $\partial S$ of $S$ is its [[closure]] $\bar S$ minus its [[interior]] $S^\circ$:

$$
  \partial S = \bar S \backslash S^\circ
$$

Letting $\neg$ denote set-theoretic complementation, $\partial S = \neg (S^\circ \cup (\neg S)^\circ)$. It is a closed set. If we consider $\partial$ restricted to closed sets as an operation on closed sets, then it becomes a special case of the boundary operator on a [[co-Heyting algebra]]; see there for further properties. 

### Of a manifold

In a [[manifold with boundary]] of [[dimension]] $n$ the boundary is the collection of points which do not have a [[neighborhood]] diffeomorphic to an [[open n-ball]], but do have a neighborhood homeomorphic to a half-ball, that is, an open ball intersected with closed half-space.

## Properties 

One reason behind the notation $\partial$ may be this (cf. [[co-Heyting boundary]]): 

+-- {: .num_prop #Leibniz} 
###### Proposition 
Let $X, Y$ be topological spaces. Then for closed subsets $A \subseteq X$ and $B \subseteq Y$, the [[Leibniz rule]] $\partial (A \times B) = (\partial A \times B) \cup (A \times \partial B)$ holds. 
=-- 

Notice the conclusion *must* fail if $A$, $B$ are *not* closed, since in this case $(\partial A \times B) \cup (A \times \partial B)$ is not closed (it doesn't include $\partial A \times \partial B$). 

+-- {: .proof} 
###### Proof 
The interior operation preserves intersections, so $(A \times B)^\circ = ((A \times Y) \cap (X \times B))^\circ = (A^\circ \times Y) \cap (X \times B^\circ)$. Its complement is $(\neg A^\circ \times Y) \cup (X \times \neg B^\circ)$, whose intersection with $\widebar{A \times B} = A \times B$ is $(\partial A \times B) \cup (A \times \partial B)$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
If $A, B$ are [[connected space|connected]] open subsets of $X$ and $A \cap B$ is [[inhabited set|inhabited]], then $\partial A = \partial B$ implies $A = B$. 
=-- 

+-- {: .proof} 
###### Proof 
Since $B$ is open, we have 

$$B \subseteq \neg \partial B = \neg \partial A = A^\circ \cup (\neg A)^\circ,$$ 

where the right side is a disjoint union of open sets. $B$ is connected, so $B \subseteq A^\circ$ or $B \subseteq (\neg A)^\circ \subseteq \neg A$. The latter cannot occur since $A \cap B$ is inhabited. So $B \subseteq A^\circ \subseteq A$; by symmetry $A \subseteq B$. 
=-- 

## Some ramifications

The [Leibniz rule](#Leibniz) shows that the boundary operator is better behaved when restricted to the lattice of [[closed subspace|closed subsets]]. Since this lattice forms a [[co-Heyting algebra]], one is led to study algebraic operators axiomatizing properties of $\partial$ ([Zarycki 1927](#Zar27)) on these, the so called [[co-Heyting boundary]] operators.

Since the [[lattice of subtoposes]] of a given [[topos]] carries a co-Heyting algebra structure, it becomes possible to define (co-Heyting) boundaries of subtoposes and thereby even boundaries of the [[geometric theory|geometric theories]] that the subtoposes correspond to! Intuitively, such a boundary $\partial T$ of a theory $T$ consists of those geometric sequents that neither 'fully follow' from $T$ nor 'fully contradict' $T$.

The interior $Int(\mathcal{E}_j)$ of a subtopos $\mathcal{E}_j$ of a [[Grothendieck topos]] is defined in an exercise of [SGA4](#SGA4) as the smallest [[open subtopos]] contained in $\mathcal{E}_j$. The boundary $\partial\mathcal{E}_j$ is then defined as the subtopos complementary to the (open) join of the [[dense subtopos|exterior subtopos]] $Ext(\mathcal{E}_j)$ and $Int(\mathcal{E}_j)$ in the [[lattice of subtoposes]].

The co-Heyting algebra perspective and the accompanying _mereo-logic of theories_ was proposed by [[William Lawvere]]. See the references at [[co-Heyting boundary]] for further pointers!

## Squaring things with algebraic topology

[[!include chains and cochains - table]]

## Related entries

* [[interior]]

* [[co-Heyting boundary]]

* [[mereology]]

* [[boundary of a simplex]]

* [[corner]]


## References

* [[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (expos&#233; IV, exercise 9.4.8, pp.461-462) {#SGA4}

* {#Zar27} M. Zarycki, _Quelque notions fondamentales de l'Analysis Situs au point de vue de l'Alg&#232;bre de la Logique_ , Fund. Math. **IX** (1927) pp.3-15. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm9/fm912.pdf))

[[!redirects boundary]]
[[!redirects boundaries]]

[[!redirects frontier]]
[[!redirects frontiers]]

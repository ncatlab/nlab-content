
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

## Definition

Given a [[topological space]] (or [[locale]]) $X$, a [[subspace]] $A$ of $X$ is __dense__ if its [[closed subspace|closure]] is all of $X$: $cl(A)=X$.

Since $cl(A)$ is the set of all points $x$ such that every open neighborhood of $x$ intersects $A$, this can equivalently be written as "every open neighborhood of every point intersects $A$", or equivalently "every [[inhabited set|inhabited]] open set intersects $A$", i.e. $A\cap U$ is inhabited for all inhabited open sets $U$.

Contraposing this, we obtain another equivalent definition "the only open subset not intersecting $A$ is the empty set", or "if $A\cap U=\emptyset$ for some open set $U$, then $U=\emptyset$".  This is the definition usually given when $X$ is a [[locale]]: a [[nucleus]] $j$ is dense if $j(0)=0$ (since $j(0)$ is the union of all opens whose "intersection with $j$" is $0$).


## Properties

* If $A \subseteq X$ is a dense subset of a topological space $X$ and $f: X \to Y$ is an [[epimorphism]], then the [[image]] $f(A)$ is dense in $Y$. 

* If i: $A \hookrightarrow X$ and $j: X \hookrightarrow B$ are dense subspace inclusions, then so is the composite $j \circ i: A \to B$. 

* If $A\subseteq X$ is a dense subset of topological space $X$ and $A$ is connected, so is $X$.

* In point-set topology, a space is [[separable space|separable]] if and only if it has a dense subspace with [[countable set|countably]] many points.

* In [[locale]] theory, we have the curious property that any [[intersection]] of dense subspaces is still dense.  (This of course fails rather badly for [[topological spaces]], where the intersection of all dense topological subspaces is the space of [[isolated point]]s.)  One consequence is that every locale has a smallest dense sublocale, the [[double negation sublocale]].

## In constructive mathematics

In [[constructive mathematics]], the law of contraposition is not an equivalence, so we obtain two inequivalent notions of density:

* $A\subseteq X$ is **strongly dense** if $A\cap U$ is inhabited for all inhabited open sets $U\subseteq X$.
* $A\subseteq X$ is **weakly dense** if $A\cap U = \emptyset$ for some open $U\subseteq X$ implies $U=\emptyset$.

Of course, strong density implies weak density, since emptiness is non-inhabitation (whereas inhabitation is stronger than non-emptiness).  The two notions of density are related dually to the corresponding notions of [[closed subspace]]: $A$ is strongly dense iff its weak closure is all of $X$, and weakly dense iff its strong closure is all of $X$.

Note that the usual notion of density for [[sublocales]] $j(0)=0$ is an analogue of *weak* density, and could be called such.  There is also a notion of *strong* density for sublocales.  Since strong density refers to inhabited sets, one might expect strong density for sublocales to refer to [[positive elements]], and thus only be sensible for [[overt locales]]; but in fact it can be reformulated to make sense in all cases.

+--{: .un_defn}
###### Definition
A [[nucleus]] $j$ on a locale $X$ is **strongly dense** if $j(\hat{P})=\hat{P}$ for any [[truth value]] $P$, where $\hat{P} = \bigvee \{ X \mid P \}$.
=--

With classical logic, every truth value is either $\top$ or $\bot$, and we have $\hat{\top}=X$ (and any nucleus satisfies $j(X)=X$) while $\hat{\bot}=0$.  Thus classically strong and weak density coincide.  To see that this is really a notion of strong density, we prove:

+--{: .un_theorem}
###### Theorem
If $i:A\subseteq X$ is a sublocale such that $A$ and $X$ are both [[overt]], then $A$ is strongly dense if and only if for any positive open $U\in O(X)$, the intersection $A\cap U = i^*U \in O(A)$ is also positive.
=--
+--{: .proof}
###### Proof
First suppose $A$ is strongly dense, and let $U\in O(X)$ be positive.  Let $P$ be the truth value of the statement "$i^*U \in O(A)$ is positive".  We want to show that $P$ is true, for which it suffices to show that $\hat{P} = \bigvee \{ X \mid P \}$ is positive, since then its covering $\{ X \mid P \}$ would be inhabited and thus $P$ would be true.  And since $U$ is positive, it suffices to show $U \subseteq \hat{P}$.

Now since $A$ is strongly dense, $j_A(\hat{P}) = \hat{P}$, which is to say that $\hat{P} = i_*(i^*\hat{P})$.  By adjointness, therefore, to show $U \subseteq \hat{P}$ it suffices to show $i^*U \subseteq i^*\hat{P} = \bigvee \{ A \mid P\}$.  Now since $A$ is overt, $i^*U$ can be covered by positive opens, so it suffices to show that for any positive $V\subseteq i^*U$ we have $V\subseteq \bigvee \{ A \mid P\}$.  But if $V\subseteq i^*U$ is positive, then $i^*U$ is also positive, i.e. $P$ is true, and thus $\bigvee \{ A \mid P\} = A$, which contains $V$.

Now suppose conversely that for any positive $U\in O(X)$, $i^*U$ is also positive, and let $P$ be any truth value; we must show $i_* i^*\hat{P} \subseteq \hat{P}$.  Since $X$ is overt, $i_* i^*\hat{P}$ can be covered by positive opens, so it suffices to show that for any positive $U\subseteq i_* i^*\hat{P}$ we have $U\subseteq \hat{P}$.  But by adjointness, $U\subseteq i_* i^*\hat{P}$ is equivalent to $i^*U \subseteq i^*\hat{P}$, and by assumption $i^*U$ is also positive.  Thus, $i^*\hat{P} = \bigvee \{ A \mid P\}$ is positive, which means that $P$ is true, and hence $\hat{P} = X$ and so $U\subseteq \hat{P}$.
=--

Since spatial locales are overt, and their positivity predicate coincides with inhabitedness, we have in particular:

+--{: .un_cor}
###### Corollary
If $i:A\subseteq X$ is a subspace of a topological space, then $A$ is strongly dense as a topological subspace if and only if it is strongly dense as a sublocale.
=--

Strong density for sublocales gives rise to a corresponding notion of [[weakly closed sublocale]].  It is also the specialization of the notion of [[fiberwise dense sublocale]] to the case of locale maps $X\to 1$.


## Related concepts

* [[dense subalgebra]]

* [[dense subtopos]]

* [[closed subspace]]

* [[nowhere dense set]]

## References

Strongly dense sublocales are discussed in 

* [[Sketches of an Elephant]], C1.1 and C1.2

* [[Peter Johnstone]], *A constructive 'closed subgroup theorem' for localic groups and groupoids*, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques (1989),  Volume: 30, Issue: 1, page 3-23 [link](https://eudml.org/doc/91430)

* M. Jibladze and [[Peter Johnstone]], *The frame of fibrewise closed nuclei*, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques (1991), Volume: 32, Issue: 2, page 99-112, [link](https://eudml.org/doc/91478)

* [[Peter Johnstone]], *Fiberwise separation axioms for locales*

[[!redirects dense subspace]]
[[!redirects dense subspaces]]
[[!redirects dense subset]]
[[!redirects dense subsets]]
[[!redirects dense set]]
[[!redirects dense sets]]
[[!redirects dense topological subspace]]
[[!redirects dense topological subspaces]]

[[!redirects strongly dense subspace]]
[[!redirects strongly dense subspaces]]
[[!redirects strongly dense subset]]
[[!redirects strongly dense subsets]]
[[!redirects strongly dense set]]
[[!redirects strongly dense sets]]
[[!redirects strongly dense topological subspace]]
[[!redirects strongly dense topological subspaces]]

[[!redirects weakly dense subspace]]
[[!redirects weakly dense subspaces]]
[[!redirects weakly dense subset]]
[[!redirects weakly dense subsets]]
[[!redirects weakly dense set]]
[[!redirects weakly dense sets]]
[[!redirects weakly dense topological subspace]]
[[!redirects weakly dense topological subspaces]]

[[!redirects dense sublocale]]
[[!redirects dense sublocales]]
[[!redirects dense nucleus]]
[[!redirects dense nuclei]]

[[!redirects strongly dense sublocale]]
[[!redirects strongly dense sublocales]]
[[!redirects strongly dense nucleus]]
[[!redirects strongly dense nuclei]]

[[!redirects weakly dense sublocale]]
[[!redirects weakly dense sublocales]]
[[!redirects weakly dense nucleus]]
[[!redirects weakly dense nuclei]]

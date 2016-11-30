
> This entry is about [[closed subsets]] of a [[topological space]]. For other notions of "closed space" see for instance _[[closed manifold]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

A subset $C$ of a [[topological space]] (or more generally a [[convergence space]]) $X$ is _closed_ if its [[complement]] is an [[open subset]], or equivalently if it contains all its [[limit points]]. When equipped with the [[subspace topology]], we may call $C$ (or its inclusion $C \hookrightarrow X$) a *closed subspace*. More abstractly, a [[subspace]] $A$ of a [[space]] $X$ is __closed__ if the [[inclusion function|inclusion map]] $A \hookrightarrow X$ is a [[closed map]]. 

The collection of closed subsets of a space $X$ is closed under arbitrary intersections. If $A \subseteq X$, then the intersection of all closed subsets containing $A$ is the smallest closed subset that contains $A$, called the _[[closure]]_ of $A$, and variously denoted $Cl(A)$, $Cl_X(A)$, $\bar{A}$, $\overline{A}$, etc. It follows that $A \subseteq B$ implies $Cl(A) \subseteq Cl(B)$ and $Cl(Cl(A)) = Cl(A)$, so that $A \mapsto Cl(A)$ forms a [[Moore closure]] operator on the power set $P(X)$. 

Since closed subsets are closed with respect to finite unions, we have $Cl(A \cup B) = Cl(A) \cup Cl(B)$. 

A _topological closure operator_ is a Moore closure operator $Cl: P(X) \to P(X)$ that preserves finite unions ($Cl(0) = 0$ and $Cl(A \cup B) = Cl(A) \cup Cl(B)$). It is easy to see that all such closure operators come from a topology whose closed sets are the fixed points of $Cl$. 

(There is a lot more to say, about [[convergence spaces]], [[smooth spaces]], [[schemes]], etc.)


## Properties

#### Kuratowski's closure-complement problem 

This mildly amusing curiosity asks how many set-theoretic operations on a topological space $X$ are derivable from closure $C$ and [[complementation]] $\neg$ and applying finite composition. The answer is that at most 14 operations are so derivable (and there are examples showing this number is achievable). As the proofs below indicate, this bare fact has little to do with topology; it has more to do with general Moore closures and how they interact with complements. 

Let $P(X)$ denote the [[power set]] (ordered by [[subset|inclusion]]) and $M$ the [[monoid]] of [[endofunctions]] $P(X) \to P(X)$ with order defined pointwise. Then $C^2 = C$ and $\neg^2 = 1$ in $M$, with $C$ order-preserving and $\neg$ order-reversing. Also 

* $I \coloneqq \neg C \neg$ is the [[interior]] operation, with $I \leq Id$. 

+-- {: .num_prop} 
###### Proposition 
$C \neg C \neg$ is [[idempotent element|idempotent]]. 
=-- 

+-- {: .proof} 
###### Proof 
$I (C \neg C) \leq (C \neg C)$, i.e., $\neg C \neg C \neg C \leq C \neg C$. Applying the order-preserving operation $C$ to both sides together with the fact that $C^2 = C$, this gives 

$$C\neg C \neg C \neg C \leq C C \neg C = C \neg C.$$ 

Since $I C \leq C$, we have also $\neg C \neg C \leq C$. Applying the order-reversing operation $C \neg C$ to both sides, we obtain 

$$C \neg C = C \neg C C \leq C \neg C (\neg C \neg C).$$ 

Combining the two displayed inequalities gives $C \neg C = C \neg C \neg C \neg C$, and then multiplying this on the right by $\neg$, the proposition follows. 
=-- 

+-- {: .num_prop} 
###### Proposition 
Let $K$ be the monoid presented by two generators $C, \neg$ and subject to the relations $C^2 = C$, $\neg^2 = 1$, and $C \neg C \neg C \neg C = C \neg C$. Then $K$, called the _Kuratowski monoid_, has at most 14 elements. 
=-- 

+-- {: .proof} 
###### Proof 
We may apply an obvious reduction algorithm on the set of words in two letters $C, \neg$, in which a word is reduced by replacing any substring $C C$ by $C$ and any substring $\neg\neg$ by an empty substring, so that any word which cannot be further reduced must be alternating in $C, \neg$. This leads to a list of 14 words 

$$1, \qquad \neg, \qquad C, \qquad \neg C, \qquad C \neg, \qquad \neg C \neg, \qquad C \neg C, $$ 

$$\,$$ 

$$\neg C \neg C, \qquad C \neg C \neg, \qquad \neg C \neg C \neg, \qquad C \neg C \neg C, \qquad \neg C \neg C \neg C, \qquad C \neg C \neg C \neg, \qquad \neg C \neg C \neg C \neg $$ 

with any further alternating words reducible by replacing a substring $C \neg C \neg C \neg C$ by $C \neg C$. Thus each element in the monoid $K$ is represented by one of these 14 words. 
=-- 

These 14 words actually name distinct set-theoretic operations $P(X) \to P(X)$ for a judicious choice of space $X$; as a corollary, the Kuratowski monoid $K$ has exactly 14 elements. For instance (courtesy of Wikipedia), taking $X = \mathbb{R}$ with its standard topology, the orbit of the element $(0, 1) \cup (1, 2) \cup \{3\} \cup ([4, 5] \cap \mathbb{Q})$ under the monoid action consists of 14 distinct elements. 

+-- {: .num_remark} 
###### Remark 
At most 7 operations are possible with interior and closure, corresponding to the covariant Kuratowski operations. Thus there is a 7-element submonoid $K_{cov} \hookrightarrow K$. Spaces $X$ for which the topological action $K_{cov} \to Set(P(X), P(X))$ is *not* injective are of some structural interest; for instance, the spaces for which $C I C = I C$ are the [[extremally disconnected spaces]], whereas spaces for which $I C = C$ are those where the open sets are equivalence classes for some equivalence relation (partition spaces). Those for which $I = C$ are [[discrete spaces]]. 
=-- 

+-- {: .num_remark} 
###### Remark 
A more manifestly topological consideration is what happens when we throw [[joins]] (or [[meets]]) into the $I, C$ mix. Briefly, at most 13 subsets can be obtained by starting with a subset $A \in P(X)$ and generating new subsets by taking closures, interiors, and unions; the order structure of these 13 subsets coincides with the free cocompletion of the finite ordered monoid $K_{cov}$ with respect to nonempty joins. Here we must use distributivity of $C$ over joins. 
=-- 

For some details on these remarks (and quite a bit more), see [Gardner and Jackson, 2008](http://nzjm.math.auckland.ac.nz/images/6/63/The_Kuratowski_Closure-Complement_Theorem.pdf) and [Sherman 2004](http://people.virginia.edu/~des5e/papers/14-sets.pdf). 


## Generalizations

### Locales

In [[locale]] theory, every open $U$ in a locale $X$ defines a closed [[sublocale]] $\mathsf{C} U$ which is given by the __closed [[nucleus]]__
$$ j_{\mathsf{C} U}\colon V \mapsto U \cup V .$$
The idea is that $\mathsf{C}U$ is the part of $X$ which does not involve $U$ (hence the notation $\mathsf{C}U$, or any other notation for a [[complement]]), and we may identify $V$ with $U \cup V$ when we are looking only away from $U$.

The sublocale $\mathsf{C}U$ is literally a complement of $U$ in the lattice of sublocales of $X$, i.e. $U\cap \mathsf{C}U = \emptyset$ and $U\cup \mathsf{C}U = X$ as sublocales.  Moreover, if $X$ is a ([[sober space|sober]]) topological space regarded as a locale, then the locale $U$ is also spatial, and so is $\mathsf{C}U$, corresponding exactly to the topological closed set $X\setminus U$.  (The fixed points of $j_{\mathsf{C}U}$ can be identified with the open sets containing $U$, which are bijectively related to the open subsets of $X\setminus U$.)  Thus there is really only one notion of "closed subspace" whether we regard $X$ as a space or as a locale (at least as long as $X$ is sober).

### Constructive mathematics

In [[constructive mathematics]], however, there are many possible *inequivalent* definitions of a closed subspace, including:

1. A subspace $C\subset X$ is closed if it is the complement of an open subspace, i.e. if $C = X\setminus U$ for some open subspace $U$;
1. A subspace $C\subset X$ is closed if its complement $X\setminus C$ is open;
1. A subspace $C\subset X$ is closed if it contains all its [[limit points]], i.e. if for any $x\in X$ such that $U\cap C$ is [[inhabited set|inhabited]] for all [[neighborhoods]] $U$ of $x$, we have $x\in C$.
1. Finally, we can also consider closed sublocales of the locale corresponding to $X$.

Definition (1) coincides with definition (2) or (3) only if excluded middle holds, since under (2) or (3) every subspace of a [[discrete space]] is closed, while under (1) the only closed subspaces are those that are complements, and if every proposition is a negation then the [[law of double negation]] follows.

Note also that definition (2) is the classical contrapositive of definition (3): $X\setminus C$ is open if for any $x\notin C$ there exists a neighborhood $U$ of $x$ such that $U\cap C = \emptyset$.  This makes it seem unlikely that they are constructively equivalent, but I do not have a specific example.

Of the first three "topological" definitions, the closest to the localic one is definition (1), since both are defined as a "complement" of some open subspace.  However, in definition (1) we may not have $X = U \cup (X\setminus U)$ even as sets, whereas it remains true constructively that $X = U \cup \mathsf{C}U$ in the lattice of sublocales.  In fact, we have the following:

+-- {: .un_theorem}
###### Theorem
The following are equivalent:

1. The law of [[excluded middle]].
1. Every closed sublocale of a spatial locale is spatial.
1. Every closed sublocale of a [[discrete locale]] is spatial.
=--
+-- {: .proof}
###### Proof
We remarked above that (1)$\Rightarrow$(2), and of course (2)$\Rightarrow$(3).  So assume (3).  Every spatial sublocale is a union of its points, and in a discrete space points are open; thus if closed sublocales are spatial, they are also open.  Since $X = U \cup \mathsf{C}U$ is constructively true, it follows that every open set is complemented in the open-set lattice of any discrete locale, which is to say that all powersets are [[Boolean algebras]], i.e. excluded middle holds.
=--

This constructive variety of notions of closed subspace gives rise to a corresponding variety of notions of [[Hausdorff space]] when applied to the diagonal subspace.


## Related concepts

* [[open subset]]

* [[clopen subset]]

* [[locally closed set]]

* [[dense subspace]]

* [[limit point]]

* [[closed cover]]

* [[Moore closure]]

* [[closed subtopos]]

* [[co-Heyting boundary]]

* [[closed morphism]], [[proper morphism]]

## References

* C. Kuratowski, _Sur l'op&#233;ration $\bar{A}$ de l'analysis situs_ , Fund. Math. **III** (1922) pp.192-195. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm3/fm3121.pdf))



[[!redirects closed subspace]]
[[!redirects closed subspaces]]
[[!redirects closed subset]]
[[!redirects closed subsets]]
[[!redirects closed set]]
[[!redirects closed sets]]

[[!redirects topological closure]]
[[!redirects topological closures]]

[[!redirects closed sublocale]]
[[!redirects closed sublocales]]
[[!redirects closed nucleus]]
[[!redirects closed nuclei]]

[[!redirects closed space]]
[[!redirects closed spaces]]
[[!redirects closed topological space]]
[[!redirects closed topological spaces]]

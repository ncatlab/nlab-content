
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

## Definition

A [[subspace]] $A$ of a [[space]] $X$ is __closed__ if the [[inclusion function|inclusion map]] $A \hookrightarrow X$ is a [[closed map]].

The __closure__ of any subspace $A$ is the smallest closed subspace that contains $A$, that is the [[intersection]] of all open subspaces of $A$.  The closure of $A$ is variously denoted $Cl(A)$, $Cl_X(A)$, $\bar{A}$, $\overline{A}$, etc. Since closed subsets are closed with respect to finite unions, we in fact have $Cl(A \cup B) = Cl(A) \cup Cl(B)$. 


(There is a lot more to say, about [[convergence spaces]], [[smooth spaces]], [[schemes]], etc.)


### Topological spaces

For a point-based notion of space such as a [[topological space]], a closed subspace is the same thing as a __closed subset__.

A subset is closed precisely if

* it contains all its [[limit points]] (in either sense). 

A topological closure operator is a [[Moore closure]] operator $Cl: P(X) \to P(X)$ that preserves finite unions ($Cl(0) = 0$ and $Cl(A \cup B) = Cl(A) \cup Cl(B)$), and in fact it is easy to see that all such closure operators come from a topology whose closed sets are the fixed points of $Cl$. 

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
At most 7 operations are possible with interior and closure, corresponding to the covariant Kuratowski operations. Thus there is a 7-element submonoid $K_{cov} \hookrightarrow K$. Spaces $X$ for which the topological action $K_{cov} \to Set(P(X), P(X)$ is *not* injective are of some structural interest; for instance, the spaces for which $C I C = I C$ are the [[extremally disconnected spaces]], whereas spaces for which $I C = C$ are those where the open sets are equivalence classes for some equivalence relation (partition spaces). Those for which $I = C$ are [[discrete spaces]]. 
=-- 

+-- {: .num_remark} 
###### Remark 
A more manifestly topological consideration is what happens when we throw [[joins]] (or [[meets]]) into the $I, C$ mix. Briefly, at most 13 subsets can be obtained by starting with a subset $A \in P(X)$ and generating new subsets by taking closures, interiors, and unions; the order structure of these 13 subsets coincides with the free cocompletion of the finite ordered monoid $K_{cov}$ with respect to nonempty joins. Here we must use distributivity of $C$ over joins. 
=-- 

For some details on these remarks (and quite a bit more), see [Gardner and Jackson, 2008](http://nzjm.math.auckland.ac.nz/images/6/63/The_Kuratowski_Closure-Complement_Theorem.pdf) and [Sherman 2004](http://people.virginia.edu/~des5e/papers/14-sets.pdf). 


### Locales

In [[locale]] theory, every open $U$ in the locale defines a closed subspace which is given by the __closed [[nucleus]]__
$$ j_{U'}\colon V \mapsto U \cup V .$$
The idea is that this subspace is the part of $X$ which does not involve $U$ (hence the notation $U'$, or any other notation for a [[complement]]), and we may identify $V$ with $U \cup V$ when we are looking only away from $U$.


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

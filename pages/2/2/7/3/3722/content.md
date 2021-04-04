
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

## Idea

A [[subset]] $C$ of a [[topological space]] (or more generally a [[convergence space]]) $X$ is _closed_ if its [[complement]] is an [[open subset]], or equivalently if it contains all its [[limit points]]. When equipped with the [[subspace topology]], we may call $C$ (or its inclusion $C \hookrightarrow X$) a *closed subspace*. More abstractly, a [[subspace]] $A$ of a [[space]] $X$ is __closed__ if the [[inclusion function|inclusion map]] $A \hookrightarrow X$ is a [[closed map]]. 

The collection of closed subsets of a space $X$ is closed under arbitrary [[intersections]]. If $A \subseteq X$, then the intersection of all closed subsets containing $A$ is the smallest closed subset that contains $A$, called the _[[topological closure]]_ of $A$, and variously denoted $Cl(A)$, $Cl_X(A)$, $\bar{A}$, $\overline{A}$, etc. It follows that $A \subseteq B$ implies $Cl(A) \subseteq Cl(B)$ and $Cl(Cl(A)) = Cl(A)$, so that $A \mapsto Cl(A)$ forms a [[Moore closure]] operator on the power set $P(X)$. 

Since closed subsets are closed with respect to finite unions, we have $Cl(A \cup B) = Cl(A) \cup Cl(B)$. 

A _topological closure operator_ is a Moore closure operator $Cl: P(X) \to P(X)$ that preserves finite unions ($Cl(0) = 0$ and $Cl(A \cup B) = Cl(A) \cup Cl(B)$). It is easy to see that all such closure operators come from a topology whose closed sets are the fixed points of $Cl$. 

(There is a lot more to say, about [[convergence spaces]], [[smooth spaces]], [[schemes]], etc.)

## Definition

+-- {: .num_defn #ClosedSubset}
###### Definition
**([[closed subsets]])**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ClosedAndOpenSubsets.png" width="300">
</div>

Let $(X,\tau)$ be a [[topological space]].


1. A [[subset]] $S \subset X$ is called a _closed subset_ if its [[complement]] $X \setminus S$ is an  _[[open subset]]_:

   $$
     \left(
       S \subset X\,\, \text{is closed}
     \right)
     \phantom{AA}
       \Leftrightarrow
     \phantom{AA}
     \left(
       X\setminus S \, \subset X \,\, \text{is open}
     \right)
     \,.
   $$

   > graphics grabbed from [Vickers 89](#Vickers89)

1. If a [[singleton]] subset $\{x\} \subset X$ is closed, one says that $x$ is a _[[closed point]]_ of $X$.

1. Given any subset $S \subset X$, then its _topological closure_ $Cl(S)$ is the smallest closed subset containing $S$:

   $$
     Cl(S)
       \;\coloneqq\;
     \underset{ {C \subset X\, \text{closed}  }   \atop {S \subset C }  }{\cap} \left( C \right)
     \,.
   $$

1. A subset $S \subset X$ such that $Cl(S) = X$ is called a _[[dense subset]]_ of $(X,\tau)$.

=--



## Properties


### Basic properties

+-- {: .num_prop }
###### Proposition

[[subsets are closed in a closed subspace precisely if they are closed in the ambient space]]

=--


+-- {: .num_lemma #UnionOfOpensGivesClosure}
###### Lemma
**(alternative characterization of topological closures)**

Let $(X,\tau)$ be a [[topological space]] and let $S \subset X$ be a [[subset]] of its underlying
set. Then a point $x \in X$ is contained in the topological closure $Cl(S)$ (def. \ref{ClosedSubset})
precisely if every [[open neighbourhood]] $U_x \subset X$ of $x$ [[intersection|intersects]] $S$:

$$
  \left(
     x \in Cl(S)
  \right)
   \phantom{AA}
     \Leftrightarrow
   \phantom{AA}
   \not\left(
     \underset{ {U \subset X \setminus S}  \atop  { U \subset X \, \text{open}  } }{\exists}
      \left(
        x \in U
      \right)
   \right)
   \,.
$$

=--

+-- {: .proof}
###### Proof

Due to [[de Morgan duality]] we may rephrase the definition of the [[topological closure]]
as follows:

$$
  \begin{aligned}
    Cl(S)
    & \coloneqq
    \underset{ {S \subset C }  \atop { C \subset X\,\text{closed} } }{\cap}
    \left(C \right)
    \\
    & =
    \underset{ { U \subset X \setminus S } \atop {U \subset X\, \text{open}}  }{\cap} \left( X \setminus U \right)
    \\
    & = X \setminus
    \left(
       \underset{ {U \subset X \setminus S} \atop { U \subset X\, \text{open} }}{\cup} U
    \right)
  \end{aligned}
  \,.
$$



=--

+-- {: .num_prop #ClosureOfAFiniteUnionIsUnionOfTheClosures}
###### Proposition
**(closure of a finite union is the union of the closures)**

For $I$ a [[finite set]] and $\{U_i \subset X\}_{i \in I}$ a finite set of subsets of a topological space, we have

$$
  Cl(\underset{i \in I}{\cup}U_i)
  =
  \underset{i \in I}{\cup} Cl(U_i)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{UnionOfOpensGivesClosure} we use that a point is in the closure of a set precisely if every open neighbourhood of the point intersects the set.

Hence in one direction

$$
  \underset{i \in I}{\cup} Cl(U_i)
  \subset
  Cl(\underset{i \in I}{\cup}U_i)
$$

because if every neighbourhood of a point intersects some $U_i$, then every neighbourhood intersects their union.

The other direction

$$
  Cl(\underset{i \in I}{\cup}U_i)
  \subset
  \underset{i \in I}{\cup} Cl(U_i)
$$

is equivalent by [[de Morgan duality]] to

$$
  X \setminus 
  \underset{i \in I}{\cup} Cl(U_i)
  \subset
  X \setminus
  Cl(\underset{i \in I}{\cup}U_i)
$$

On left now we have the point for which there exists for each $i \in I$ a neighbourhood $U_{x,i}$ which does not intersect $U_i$. Since $I$ is finite, the intersection $\underset{i \in I}{\cap} U_{x,i}$ is still an open neighbourhood of $x$, and such that it intersects none of the $U_i$, hence such that it does not intersect their union. This implis that the given point is contained in the set on the right.

=--



### In metric spaces
 {#InMetricSpaces}

+-- {: .num_prop #ConvergenceInClosedSubspace}
###### Proposition

Using [[classical logic]] then:

Let $(X,d)$ be a [[metric space]], regarded as a [[topological space]] via its [[metric topology]],
and let $V \subset X$ be a [[subset]]. Then the following are equivalent:

1. $V \subset X$ is a [[closed subspace]].

1. For every [[sequence]] $x_i \in V \subset X$ with elements in $V$, which [[convergence|converges]] as a sequence in $X$ it also converges in $V$.

=--

+-- {: .proof}
###### Proof

First assume that $V \subset X$ is closed and that $x_i \overset{i \to \infty}{\longrightarrow} x_{\infty}$ for some
$x_\infty \in X$. We need to show that then $x_\infty \in V$. Suppose it were not, then 
$x_\infty \in X\backslash V$. Since by definition this [[complement]] $X \backslash V$ is an [[open subset]], 
it follows that there exists a [[real number]] $\epsilon \gt 0$ such that the [[open ball]] 
around $x$ of radius $\epsilon$ is still contained in the complement: $B^\circ_x(\epsilon) \subset X \backslash V$.
But since the sequence is assumed to converge in $X$, this means that there exists $N_\epsilon$ such that all 
$x_{i \gt N_{\epsilon}}$ are in $B^\circ_x(\epsilon)$, hence in $X\backslash V$. This contradicts the assumption that
all $x_i$ are in $V$, and hence we have [[proof by contradiction|proved by contradiction]] that $x_\infty \in V$.

Conversely, assume that for all sequences in $V$ that converge to some $x_\infty \in X$ then $x_\infty \in V \subset W$.
We need to show that then $V$ is closed, hence that $X \backslash V \subset X$ is an open subset, hence that for every
$x \in X \backslash V$ we may find a real number $\epsilon \gt 0$ such that the [[open ball]] $B^\circ_x(\epsilon)$ around $x$ 
of radius $\epsilon$ is still contained in
$X \backslash V$. Suppose on the contrary that such $\epsilon$ did not exist. This would mean that for each $k \in \mathbb{N}$
with $k \geq 1$ then the [[intersection]] $B^\circ_x(1/k) \cap V$ is [[inhabited|non-empty]]. Hence then we could choose
points $x_k \in B^\circ_x(1/k) \cap V$ in these intersections. These would form a sequence which clearly converges to   
the original $x$, and so by assumption we would conclude that $x \in V$, which violates the assumption that $x \in X \backslash V$.
Hence we [[proof by contradiction|proved by contradiction]] $X \backslash V$ is in fact open.

=--


### Relation to interior subspaces

+-- {: .num_lemma #RelationClAndInt}
###### Lemma

Let $(X,\tau)$ be a [[topological space]] and let $S \subset X$ be a [[subset]].
Then the [[topological interior]] $Int(S)$ of $S$  equals the [[complement]] of the
[[topological closure]] $Cl(X\backslash S)$ of the complement of $S$:

$$
  Int(S) 
    = 
  X \backslash Cl\left(
    X \backslash S
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By taking [[complements]] once more, the statement is equivalent to

$$
  X \backslash Int(S)
  =
  Cl( X \backslash S )
  \,.
$$

Now we compute:

$$
  \begin{aligned}
    X \backslash Int(S)
    & =
    X \backslash \left(  \underset{{U \, open} \atop {U \subset S}}{\cup}U \right)
    \\
    & = \underset{U \subset S}{\cap} X \backslash U
    \\
    & = \underset{{C\, closed} \atop {C \supset X \backslash S}}{\cap} C
    \\
    & = Cl(X \backslash S)
  \end{aligned}
$$

=--



### Relation to compact subspaces

The relation of closed subspaces to [[compact subspaces]] is expressed by the following statements

* [[Heine-Borel theorem]]

* [[closed subsets of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]



### Kuratowski's closure-complement problem 

This mildly amusing curiosity asks how many set-theoretic operations on a topological space $X$ are derivable from closure $C$ and [[complementation]] $\neg$ and applying finite composition. The answer is that at most 14 operations are so derivable (and there are examples showing this number is achievable). As the proofs below indicate, this bare fact has little to do with topology; it has more to do with general Moore closures and how they interact with complements (using [[classical logic]]). 

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

For some details on these remarks (and quite a bit more), see [Gardner and Jackson, 2008](http://nzjm.math.auckland.ac.nz/images/6/63/The_Kuratowski_Closure-Complement_Theorem.pdf) and [Sherman 2004](http://people.virginia.edu/~des5e/papers/14-sets.pdf). An example of a non-topological Moore closure where the 14 operations are all distinct is given [here](http://math.stackexchange.com/a/1912101/43208). 


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

Definition (1) coincides with definition (2) or (3) only if excluded middle holds, since under (2) or (3) every subspace of a [[discrete space]] is closed, while under (1) the only closed subspaces are those that are complements, and if every proposition is a negation then the [[law of double negation]] follows.  On the other hand, Definition (2) is clearly too strong, because even [[closed intervals]] $[a,b]$ in the [[real numbers]] can't be proved constructively to satisfy it (though they do satisfy definitions (1) and (3)).  Note also that Definition (1) always implies Definition (3), since if $C = X\setminus U$ and every open neighborhood of $x$ intersects $C$, then $x\notin U$ and thus $x\in C$.  Thus it is not unreasonable (see also below) to define:

* $C\subset X$ is **strongly closed** if it is the complement of an open subspace.
* $C\subset X$ is **weakly closed** if it contains all its [[limit points]].

This constructive variety of notions of closed subspace gives rise to a corresponding variety of notions of [[Hausdorff space]] when applied to the diagonal subspace.

Note also that neither of the sensible constructive definitions behaves quite like closed subspaces do classically.  In particular, neither of them is apparently stable under finite unions (though the too-strong Definition (2) is).  The situation is better for locales; see below.

### Locales in constructive mathematics

Of the "topological" definitions of closed subspace above, it is "strongly closed" (and the too-strong Definition (2)) that seem closest to the localic one.  However, in the topological definitions we may not have $X = U \cup (X\setminus U)$ or $X = (X\setminus C) \cup C$ even as sets, whereas it remains true constructively that $X = U \cup \mathsf{C}U$ in the lattice of sublocales.  In fact, we have the following:

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

On the other hand, there is a localic notion of *weakly closed sublocale* that is closely related to topologically weakly closed subspaces (so that the above notion of "closed sublocale" --- the formal complement of an open sublocale --- could also be called *strongly closed*).  It is the specialization of the notion of [[fiberwise closed sublocale]] to locale maps $X\to 1$ into the terminal object.

+--{: .un_defn}
###### Definition
A sublocale $C\subseteq X$ is **weakly closed** if it is not [[strongly dense sublocale|strongly dense]] in any larger sublocale of $X$.  That is, if whenever $D$ is a sublocale of $X$ such that $C\subseteq D$ by a strongly dense inclusion, then $C=D$.
=--

Since strong and weak denseness coincide classically, so do strong and weak closedness.  And as we expect, strong closedness implies weak closedness, since strong density implies weak density.  Moreover, both of them are better-behaved than the corresponding topological notions.  For instance, strongly and weakly closed sublocales are both stable under finite unions (in the lattice of sublocales), even constructively.

Both strongly and weakly closed sublocales are "correct" notions; they are simply different.  Some classical theorems about closed sublocales are constructively about strongly closed ones, while others (such as the theorem that any [[subgroup]] of a [[localic group]] is closed) are about weakly closed ones.

However, as we saw above, not every strongly closed sublocale (hence not every weakly closed sublocale either) can be spatial.  But it is shown at [[strongly dense sublocale]] that a subspace of a space is localically strongly dense if and only if it is topologically strongly dense.  This leads us to guess:

+--{: .un_theorem}
###### Conjecture
A subspace $C\subseteq X$ of a (sober) topological space $X$ is topologically weakly closed if and only if it is the spatial coreflection of a weakly closed sublocale.
=--

In one direction this is easy: suppose $C$ is topologically weakly closed, and let $D$ be its localic weak closure.  This is, by definition, the largest sublocale of $X$ in which $C$ is localically strongly dense.  Now let $E$ be the spatial coreflection of $D$; since $C$ is spatial we have $C\subseteq E$, and since $C$ is localically strongly dense in $D$, it is also so in $E$, and hence topologically strongly dense.  But $C$ is also topologically weakly closed, hence $C=E$ and is the spatial coreflection of the weakly closed sublocale $D$.

The other direction is harder.


## Related concepts

* [[closed point]]

* [[irreducible closed subspace]]

* [[open subset]]

* [[clopen subset]]

* [[locally closed set]]

* [[dense subspace]]

* [[limit point]]

* [[closed cover]]

* [[Moore closure]]

* [[closed subtopos]]

* [[co-Heyting boundary]]

* [[closed morphism]]

* [[proper morphism]]

## References

* [[Kazimierz Kuratowski|C. Kuratowski]], _Sur l'op&#233;ration_ $\bar{A}$ _de l'analysis situs_ , Fund. Math. **III** (1922) pp.192-195. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm3/fm3121.pdf))

Weakly closed sublocales are discussed in 

* [[Sketches of an Elephant]], C1.1 and C1.2

* [[Peter Johnstone]], *A constructive 'closed subgroup theorem' for localic groups and groupoids*, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques (1989),  Volume: 30, Issue: 1, page 3-23 [link](https://eudml.org/doc/91430)

* M. Jibladze and [[Peter Johnstone]], *The frame of fibrewise closed nuclei*, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques (1991), Volume: 32, Issue: 2, page 99-112, [link](https://eudml.org/doc/91478)

* [[Peter Johnstone]], *Fiberwise separation axioms for locales*


[[!redirects closed subspace]]
[[!redirects closed subspaces]]
[[!redirects closed subset]]
[[!redirects closed subsets]]
[[!redirects closed set]]
[[!redirects closed sets]]

[[!redirects weakly closed subspace]]
[[!redirects weakly closed subspaces]]
[[!redirects weakly closed subset]]
[[!redirects weakly closed subsets]]
[[!redirects weakly closed set]]
[[!redirects weakly closed sets]]

[[!redirects strongly closed subspace]]
[[!redirects strongly closed subspaces]]
[[!redirects strongly closed subset]]
[[!redirects strongly closed subsets]]
[[!redirects strongly closed set]]
[[!redirects strongly closed sets]]

[[!redirects topological closure]]
[[!redirects topological closures]]

[[!redirects closed sublocale]]
[[!redirects closed sublocales]]
[[!redirects closed nucleus]]
[[!redirects closed nuclei]]

[[!redirects strongly closed sublocale]]
[[!redirects strongly closed sublocales]]
[[!redirects strongly closed nucleus]]
[[!redirects strongly closed nuclei]]

[[!redirects weakly closed sublocale]]
[[!redirects weakly closed sublocales]]
[[!redirects weakly closed nucleus]]
[[!redirects weakly closed nuclei]]

[[!redirects weakly closed]]

[[!redirects closed space]]
[[!redirects closed spaces]]
[[!redirects closed topological space]]
[[!redirects closed topological spaces]]

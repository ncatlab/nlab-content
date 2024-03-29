
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

## Statement

+-- {: .num_lemma #LocallyCompactAndSigmaCompactImpliesGoodNestedCover}
###### Lemma

Let $X$ be a [[topological space]] which is

1. [[locally compact topological space|locally compact]] 

   in the sense that for every open neighbourhood $U$ there exists a smaller open neighbourhood whose topological closure is compact and still contained in $U$;

1. [[sigma-compact topological space|sigma-compact]].

Then there exists a [[countable open cover]] $\{U_i \subset X\}_{i \in \mathbb{N}}$ of $X$ such that for each $i \in I$

1. the [[topological closure]] $Cl(U_i)$ is a [[compact topological space|compact]] [[subspace]] 

1. $Cl(U_i) \subset U_{i +1}$.

=--

+-- {: .proof}
###### Proof

By [[sigma-compact topological space|sigma-compactness]] of $X$ there exists a [[countable cover]] $\{K_i \subset X\}_{i \in \mathbb{N}}$ of [[compact topological space|compact]] [[subspaces]]. We use these to construct the required cover by [[induction]].

For $i = 0$ set

$$
  U_0 \coloneqq \emptyset
  \,.
$$

Then assume that for $n \in \mathbb{N}$ we have constructed a set $\{U_i \subset X\}_{i \in \{1, \cdots, n\}}$ with the required properties.

In particular this implies that 

$$
  Q_n \coloneqq Cl(U_n) \cup K_{n-1} \;\subset X
$$

is a compact subspace. We now construct an open neighbourhood $U_{n+1}$ of this union as follows:

Let $\{U_x \subset X\}_{x \in Q_n}$ be a set of open neighbourhood around each of the points in $Q_n$. By [[locally compact topological space|local compactness]] of $X$, for each $x$ there is a smaller open neighbourhood $V_x$ with 

$$
  \{x\} \subset V_x \subset \underset{\text{compact}}{\Cl(V_x)} \subset U_x
  \,.
$$

So $\{V_x \subset X\}_{x \in Q_n}$ is still an open cover of $Q_n$. By compactness of $Q_n$,  there exists a [[finite set]] $J_n \subset Q_n$ such that $\{V_x \subset X\}_{x \in J_n}$ is a [[finite open cover]]. The union

$$
  U_{n + 1} \coloneqq \underset{x \in J}{\cup} V_x
$$

is an open neighbourhood of $Q_n$, hence in particular of $Cl(U_n)$. Moreover,  since finite unions of compact spaces are compact ([this prop.](compact+space#UnionsAndIntersectionOfCompactSubspaces)) and since the closure of a finite union is the union of the closures ([this prop.](closed+subspace#ClosureOfAFiniteUnionIsUnionOfTheClosures)), the closure of $U_{n+1}$ is compact:

$$
  \begin{aligned}
    Cl(U_{n+1})
    &= 
    Cl\left(  \underset{x\in J_n}{\cup} V_x \right)
    \\
    & = 
    \underset{x \in J_n}{\cup} \underset{\text{compact}}{Cl( V_x )}
  \end{aligned}
  \,.
$$

This produces by [[induction]] a set $\{U_i \subset X\}_{i \in \mathbb{N}}$ with $Cl(U_i)$ compact and $Cl(U_i) \subset U_{i+1}$ for all $i \in \mathbb{N}$. It remains to see that this is a cover. This follows since by construction each $U_{i+1}$ is an open neighbourhood not just of $Cl(U_{i})$ but in fact of $Q_i$, hence in particular of $K_i$, and since the $K_i$ form a cover:

$$
  \underset{i \in \mathbb{N}}{\cup} U_i
  \supset
  \underset{i \in \mathbb{N}}{\cup} K_i
   = 
  X
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition
**(locally compact and sigma-compact spaces are paracompact)**

Let $X$ be a [[topological space]] which is

1. [[locally compact topological space|locally compact]];

1. [[sigma-compact topological space|sigma-compact]].

Then $X$ is also [[paracompact topological space|paracompact]].

=--

+-- {: .proof}
###### Proof

Let $\{U_i \subset X\}_{i \in I}$ be an open cover of $X$. We need to show that this has a refinement by a [[locally finite cover]].

By lemma \ref{LocallyCompactAndSigmaCompactImpliesGoodNestedCover} there exists a countable open cover $\{V_n \subset X\}_{n \in \mathbb{N}}$ of $X$ such that for all $n \in \mathbb{N}$

1. $Cl(V_n)$ is compact;

1. $Cl(V_n) \subset V_{n+1}$.

Notice that the [[complement]] $Cl(V_{n+1}) \setminus V_n$ is compact, since $Cl(V_{n+1})$ is compact and $V_n$ is open (by [this lemma](compact+space#IntersectionCompactWithOpen)).

By this compactness, the cover $\{U_i \subset X\}_{i \in I}$ regarded as a cover of the [[subspace]] $Cl(V_{n+1})\setminus V_n$ has a finite subcover $\{U_i \subset X\}_{i \in J_n}$ indexed by a finite set $J_n \subset I$, for each $n \in \mathbb{N}$.

We consider the sets of intersections

$$
  \mathcal{U}_n 
    \coloneqq
  \{ U_i \cap ( V_{n+2} \setminus Cl(V_{n-1}) )  \}
  \,.
$$

Since $V_{n+2} \setminus Cl(V_{n-1})$ is open, and since $Cl(V_{n+1}) \subset V_{n+2}$ by construction, this is still an open cover of $Cl(V_{n+1})\setminus V_n$. We claim now that 

$$
  \mathcal{U} \coloneqq \underset{n\in \mathbb{N}}{\cup} \mathcal{U}_n
$$

is a locally finite refinement of the original cover, as required: 

1. $\mathcal{U}$ is a refinement, since by construction each element in $\mathcal{U}_n$ is contained in one of the $U_i$;

1. $\mathcal{U}$ is still a covering because by construction it covers $Cl(V_{n+1}) \setminus V_n$ for all $n \in \mathbb{N}$, and since by the nested nature of the cover $\{V_n \subset X\}_{n \in \mathbb{N}}$ also  $\{Cl(V_{n+1}) \setminus V_n\}_{n \in \mathbb{N}}$ is a cover of $X$.

1. $\mathcal{U}$ is locally finite because each point $x \in X$ has an open neighbourhood of the form $V_{n+2} \setminus Cl(V_{n-1})$ (since these also form an open cover, by the nestedness) and since by construction this has trivial intersection with $\mathcal{U}_{\geq n+3}$ and since all $\mathcal{U}_n$ are finite, so that also $\underset{k \lt n+3}{\cup} \mathcal{U}_k$ is finite.


=--


## Related concepts

* [[second-countable regular spaces are paracompact]]

## References

* [[Akhil Mathew]], _[Paracompactness](https://amathew.wordpress.com/2010/08/17/paracompactness/)_

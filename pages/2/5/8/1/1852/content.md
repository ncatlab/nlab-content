# Normal spaces
* table of contents
{: toc}

## Idea

A normal space is a space (typically a [[topological space]]) which satsifies one of the stronger [[separation axioms]].

[[!include main separation axioms -- table]]



## Definitions

A [[topological space]] $X$ is __normal__ if it satisfies:

*  $T_4$: for every two [[closed subspace|closed]] [[disjoint subsets]] $A,B \subset X$ there are (optionally [[open subspace|open]]) [[neighborhoods]] $U \supset A$, $V \supset B$ such that $U \cap V$ is [[empty set|empty]].

By [[Urysohn's lemma]] this is equivalent to the condition

* for every two [[closed subspace|closed]] [[disjoint subsets]] $A,B \subset X$ there exists an [[Urysohn function]] that separates them.

Often one adds the requirement

*  $T_1$: every [[point]] in $X$ is closed.

(Unlike with [[regular spaces]], $T_0$ is not sufficient here.)

One may also see terminology where a __normal space__ is any space that satsifies $T_4$, while a __$T_4$-space__ must satisfy both.  This has the benefit that a $T_4$-space is always also a $T_3$-space while still having a term available for the weaker notion.  On the other hand, the reverse might make more sense, since you would expect any space that satisfies $T_4$ to be a $T_4$-space; this convention is also seen.

If instead of $T_1$, you add only

*  $R_0$: if $x$ is in the closure of $\{y\}$, then $y$ is in the [[topological closure|closure]] of $\{x\}$,

then the result may be called an __$R_3$-space__.

Any space that satisfies both $T_4$ and $T_1$ must be [[Hausdorff space|Hausdorff]], and every Hausdorff space satisfies $T_1$, so one may call such a space a __normal Hausdorff space__; this terminology should be clear to any reader.

Any space that satisfies both $T_4$ and $R_0$ must be [[regular space|regular]] (in the weaker sense of that term), and every regular space satisfies $R_0$, so one may call such a space a __normal regular space__; however, those who interpret 'normal' to include $T_1$ usually also interpret 'regular' to include $T_1$, so this term can be ambiguous.

It can be useful to rephrase $T_4$ in terms of only open sets instead of also closed ones:

*  $T_4$: if $G,H \subset X$ are [[open subspace|open]] and $G \cup H = X$, then there exist open sets $U,V$ such that $U \cup G$ and $V \cup H$ are still $X$ but $U \cap V$ is empty.

This definition is suitable for generalisation to [[locales]] and also for use in [[constructive mathematics]] (where it is not equivalent to the usual one).

To spell out the localic case, a __normal locale__ is a [[frame]] $L$ such that

*  $T_4$: if $G,H \in L$ are opens and $G \vee H = \top$, then there exist opens $U,V$ such that $U \vee G$ and $V \vee H$ are still $\top$ but $U \wedge V = \bot$.



## Examples
 {#Examples}

Every [[metric space]] is normal Hausdorff. 

+-- {: .num_example}
###### Example

Let $(X,d)$ be a [[metric space]] regarded as a [[topological space]]
via its [[metric topology]]. Then this is a [[normal Hausdorff space]], in particular hence a regular Hausdorff space.

=--

+-- {: .proof}
###### Proof

We need to show is that given two [[disjoint subsets|disjoint]] [[closed subsets]] $C_1, C_2 \subset X$
then their exists [[disjoint subset|disjoint]] [[open neighbourhoods]] $U_{C_1} \subset C_1$
and $U_{C_2} \supset C_2$.

Consider the function

$$
  d(S,-) \colon X \to \mathbb{R}
$$


which computes [[distances]] from a subset $S \subset X$, by forming the [[infimum]] of the distances to all its points:

$$
  d(S,x) \coloneqq inf\left\{ d(s,x) \vert s \in S \right\}
  \,.
$$

Then the
[[unions]] of [[open balls]]

$$
  U_{C_1}
    \coloneqq
  \underset{x_1 \in C_1}{\cup} B^\circ_{x_1}( d(C_2,x_1) )
$$

and

$$
  U_{C_2}
    \coloneqq
  \underset{x_2 \in C_2}{\cup} B^\circ_{x_2}( d(C_1,x_2) )
  \,.
$$

have the required properties.

=--


+-- {: .num_example }
###### Counter-Example

The [[real numbers]] equipped with their [[K-topology]] $\mathbb{R}_K$ are a [[Hausdorff topological space]] which is not a [[regular Hausdorff space]] (hence in particular not a [[normal Hausdorff space]]).

=--

+-- {: .proof}
###### Proof

By construction the K-topology is [[finer topology|finer]] than the usual [[Euclidean space|euclidean]] [[metric topology]]. Since the latter is Hausdorff, so is $\mathbb{R}_K$. It remains to see that $\mathbb{R}_K$ contains a point and a [[disjoint subset|disjoint]] closed subset such that do not have dijoint [[open neighbourhoods]].

But this is the case essentially by construction: Observe that 

$$
  \mathbb{R} \backslash K
  \;=\;
  (-\infty,-1/2)
    \cup
  \left( 
    (-1,1) \backslash K
  \right)
    \cup
  (1/2, \infty)
$$

is an open subset in $\mathbb{R}_K$, whence

$$
  K = \mathbb{R} \backslash ( \mathbb{R} \backslash K  )
$$

is a [[closed subset]] of $\mathbb{R}_K$. 


But every [[open neighbourhood]] of $\{0\}$ contains at least $(-\epsilon, \epsilon) \backslash K$ for some positive real number $\epsilon$. There exists then $n \in \mathbb{N}_{\geq 0}$ with $1/n \lt \epsilon$ and $1/n \in K$. An open neighbourhood of $K$ needs to contain an open interval around $1/n$, and hence will have non-trivial intersection with $(-\epsilon, \epsilon)$. Therefore $\{0\}$ and $K$ may not be separated by disjoint open neighbourhoods, and so $\mathbb{R}_K$ is not normal.



=-- 






* Every normal Hausdorff space is an [[Urysohn space]], a fortiori regular and a fortiori Hausdorff. 

* Every regular [[second countable space]] is normal. Every [[paracompact space|paracompact]] Hausdorff space is normal (Dieudonn&#233;'s theorem). See at [[compact Hausdorff spaces are normal]]

* The [[Tietze extension theorem]] applies to normal spaces.




## References

The class of normal spaces was introduced by Tietze (1923) and Aleksandrov--Uryson (1924). 

* Ryszard Engelking, __General topology__, (Monographie Matematyczne, tom 60) Warszawa 1977; expanded Russian edition Mir 1986.


[[!redirects normal space]]
[[!redirects normal spaces]]
[[!redirects Normal space]]
[[!redirects Normal spaces]]

[[!redirects normal topological space]]
[[!redirects normal topological spaces]]


[[!redirects T4 space]]
[[!redirects T4 spaces]]
[[!redirects T4-space]]
[[!redirects T4-spaces]]
[[!redirects T-4 space]]
[[!redirects T-4 spaces]]
[[!redirects T-4-space]]
[[!redirects T-4-spaces]]

[[!redirects normal Hausdorff space]]
[[!redirects normal Hausdorff spaces]]
[[!redirects normal Hausdorff topological space]]
[[!redirects normal Hausdorff topological spaces]]

[[!redirects R3 space]]
[[!redirects R3 spaces]]
[[!redirects R3-space]]
[[!redirects R3-spaces]]
[[!redirects R-3 space]]
[[!redirects R-3 spaces]]
[[!redirects R-3-space]]
[[!redirects R-3-spaces]]

[[!redirects normal regular space]]
[[!redirects normal regular spaces]]


[[!redirects normal locale]]
[[!redirects normal locales]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Normal spaces
* table of contents
{: toc}

## Idea

A normal space is a space (typically a [[topological space]]) which satisfies one of the stronger [[separation axioms]].

[[!include main separation axioms -- table]]



## Definitions

A [[topological space]] $X$ is __normal__ if it satisfies:

*  $T_4$: for every two [[closed subspace|closed]] [[disjoint subsets]] $A,B \subset X$ there are (optionally [[open subspace|open]]) [[neighborhoods]] $U \supset A$, $V \supset B$ such that their [[intersection]] $U \cap V$ is [[empty set|empty]].

By [[Urysohn's lemma]] this is equivalent to the condition

* for every two [[closed subspace|closed]] [[disjoint subsets]] $A,B \subset X$ there exists an [[Urysohn function]] that separates them.

Often one adds the requirement

*  $T_1$: every [[point]] in $X$ is closed.

(Unlike with [[regular spaces]], $T_0$ is not sufficient here.)

One may also see terminology where a __normal space__ is any space that satisfies $T_4$, while a __$T_4$-space__ must satisfy both $T_4$ and $T_1$.  This has the benefit that a $T_4$-space is always also a $T_3$-space while still having a term available for the weaker notion.  On the other hand, the reverse might make more sense, since you would expect any space that satisfies $T_4$ to be a $T_4$-space; this convention is also seen.

If instead of $T_1$, one requires

*  $R_0$: if $x$ is in the [[topological closure|closure]] of $\{y\}$, then $y$ is in the [[topological closure|closure]] of $\{x\}$,

then the result may be called an __$R_3$-space__.

Any space that satisfies both $T_4$ and $T_1$ must be [[Hausdorff space|Hausdorff]], and every Hausdorff space satisfies $T_1$, so one may call such a space a __normal Hausdorff space__; this terminology should be clear to any reader.

Any space that satisfies both $T_4$ and $R_0$ must be [[regular space|regular]] (in the weaker sense of that term), and every regular space satisfies $R_0$, so one may call such a space a __normal regular space__; however, those who interpret 'normal' to include $T_1$ usually also interpret 'regular' to include $T_1$, so this term can be ambiguous.

Every normal Hausdorff space is an [[Urysohn space]], a fortiori regular and a fortiori Hausdorff. 

It can be useful to rephrase $T_4$ in terms of only open sets instead of also closed ones:

*  $T_4$: if $G,H \subset X$ are [[open subspace|open]] and $G \cup H = X$, then there exist open sets $U,V$ such that $U \cup G$ and $V \cup H$ are still $X$ but $U \cap V$ is empty.

This definition is suitable for generalisation to [[locales]] and also for use in [[constructive mathematics]] (where it is not equivalent to the usual one).

To spell out the localic case, a __normal locale__ is a [[frame]] $L$ such that

*  $T_4$: if $G,H \in L$ are opens and $G \vee H = \top$, then there exist opens $U,V$ such that $U \vee G$ and $V \vee H$ are still $\top$ but $U \wedge V = \bot$.



## Examples
 {#Examples}


+-- {: .num_example}
###### Example

Let $(X,d)$ be a [[metric space]] regarded as a [[topological space]]
via its [[metric topology]]. Then this is a normal Hausdorff space.

=--

+-- {: .proof}
###### Proof

We need to show that given two [[disjoint subsets|disjoint]] [[closed subsets]] $C_1, C_2 \subset X$, there exist [[disjoint subset|disjoint]] [[open neighbourhoods]] $U_{C_1} \supset C_1$
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

If $S$ is closed and $x \notin S$, then $d(S, x) \gt 0$. Then the
[[unions]] of [[open balls]]

$$
  U_{C_1}
    \coloneqq
  \underset{x_1 \in C_1}{\bigcup} B^\circ_{x_1}( \frac1{2}d(C_2,x_1) )
$$

and

$$
  U_{C_2}
    \coloneqq
  \underset{x_2 \in C_2}{\bigcup} B^\circ_{x_2}( \frac1{2}d(C_1,x_2) )
  \,.
$$

have the required properties. For if there exist $x_1 \in C_1, x_2 \in C_2$ and $y \in B^\circ_{x_1}( \frac1{2}d(C_2,x_1) ) \cap B^\circ_{x_2}( \frac1{2}d(C_1,x_2) )$, then 

$$d(x_1, x_2) \leq d(x_1, y) + d(y, x_2) \lt \frac1{2} (d(C_2, x_1) + d(C_1, x_2)) \leq \max\{d(C_2, x_1), d(C_1, x_2)\}$$ 

and if $d(C_1, x_2) \leq d(C_2, x_1)$ say, then $d(x_2, x_1) = d(x_1, x_2) \lt d(C_2, x_1)$, contradicting the definition of $d(C_2, x_1)$. 

=--

+-- {: .num_prop}
###### Proposition

Every [[regular space|regular]] [[second countable space]] is normal. 

=-- 

See [[Urysohn metrization theorem]] for details. 

+-- {: .num_prop}
###### Proposition
**(Dieudonn&#233;'s theorem)**

Every [[paracompact Hausdorff space]], in particular every [[compact Hausdorff space]], is normal.

=--

See _[[paracompact Hausdorff spaces are normal]]_ for details.


+-- {: .num_example }
###### Nonexample

The [[real numbers]] equipped with their [[K-topology]] $\mathbb{R}_K$ are a [[Hausdorff topological space]] which is not a [[regular Hausdorff space]] (hence in particular not a normal Hausdorff space).

=--

+-- {: .proof}
###### Proof

By construction the K-topology is [[finer topology|finer]] than the usual [[Euclidean space|euclidean]] [[metric topology]]. Since the latter is Hausdorff, so is $\mathbb{R}_K$. It remains to see that $\mathbb{R}_K$ contains a point and a [[disjoint subset|disjoint]] closed subset such that they do not have disjoint [[open neighbourhoods]].

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

+-- {: .num_example #Morse} 
###### Counter-Example 

If $\omega_1$ is the first un-[[countable ordinal]] with the [[order topology]], and $\widebar{\omega_1}$ its [[one-point compactification]], then $X = \omega_1 \times \widebar{\omega_1}$ with the [[product topology]] is not normal. 

Indeed, let $\infty \in \widebar{\omega_1}$ be the unique point in the [[complement]] of $\omega_1 \hookrightarrow \widebar{\omega_1}$; then it may be shown that every open set $U$ in $X$ that includes the closed set $A = \{(x, x): x \neq \infty\}$ in $X$ must somewhere intersect the closed set $\omega_1 \times \{\infty\}$ which is disjoint from $A$. For if that were false, then we could define an increasing sequence $x_n \in \omega_1$ by recursion, letting $x_0 = 0$ and letting $x_{n+1} \in \omega_1$ be the least element that is greater than $x_n$ and such that $(x_n, x_{n+1}) \notin U$. Then, letting $b \in \omega_1$ be the [[supremum]] of this increasing sequence, the sequence $(x_n, x_{n+1})$ converges to $(b, b)$, and yet the neighborhood $U$ of $(b, b)$ contains none of the points of this sequence, which is a contradiction. 
=-- 

This example also shows that general subspaces of normal spaces need not be normal, since $\omega_1 \times \widebar{\omega_1}$ is an open subspace of the compact Hausdorff space $\widebar{\omega_1} \times \widebar{\omega_1}$, which is itself normal. 

+-- {: .num_example} 
###### Counter-Example 
An uncountable product of infinite discrete spaces $X$ is not normal. More generally, a product of $T_1$ spaces $X_i$ uncountably many of which are not [[limit point compact space|limit point compact]] is not normal. 

Indeed, by a simple application of Remark \ref{retracts} below and the fact that closed subspaces of normal Hausdorff spaces are normal Hausdorff, it suffices to see that the archetypal example $\mathbb{N}^{\omega_1}$ is not normal. For a readable and not overly long account of this result, see [Dan Ma's blog](https://dantopology.wordpress.com/2009/10/13/the-uncountable-product-of-the-countable-discrete-space-is-not-normal/). 
=-- 


+-- {: .num_example}
###### Example

A [[Dowker space]] is an example of a normal space which is not [[countably paracompact topological space|countably paracompact]].

=--

## Properties

### Basic properties

+-- {: .num_prop #T4InTermsOfTopologicalClosures}
###### Proposition
**(normality in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is normal Hausdorff, precisely if all points are closed and for all [[closed subsets]] $C \subset X$ with [[open neighbourhood]] $U \supset C$ there exists a smaller open neighbourhood $V \supset C$ whose [[topological closure]] $Cl(V)$ is still contained in $U$:

$$
  C \subset V \subset Cl(V) \subset U
  \,.
$$

=--

+-- {: .proof}
###### Proof

In one direction, assume that $(X,\tau)$ is normal, and consider

$$
  C \subset U
  \,.
$$

It follows that the [[complement]] of the open subset $U$ is closed and disjoint from $C$:

$$
  C \cap X \setminus U = \emptyset
  \,.
$$

Therefore by assumption of normality of $(X,\tau)$, there exist open neighbourhoods  with

$$

  V \supset C
  \,, \phantom{AA}
  W \supset X \setminus U
  \phantom{AA}
    \text{with}
  \phantom{AA}
  V \cap W = \emptyset
  \,.
$$

But this means that

$$
  V \subset X \setminus W
$$

and since the [[complement]] $X \setminus W$ of the open set $W$ is closed, it still contains the closure of $V$, so that we have

$$
  C \subset V \subset Cl(V) \subset X \setminus W \subset U
$$

as required.

In the other direction, assume that for every open neighbourhood $U \supset C$ of a closed subset $C$ there exists a smaller open neighbourhood $V$ with

$$
  C \subset V \subset Cl(V) \subset U
  \,.
$$

Consider disjoint closed subsets

$$
  C_1, C_2 \subset X
  \,,
  \phantom{AAA}
  C_1 \cap C_2 = \emptyset
  \,.
$$

We need to produce disjoint open neighbourhoods for them.

From their disjointness it follows that

$$
  X \setminus C_2 \supset C_1
$$

is an open neighbourhood. Hence by assumption there is an open neighbourhood $V$ with

$$
  C_1 \subset V \subset Cl(V) \subset X \setminus C_2
  \,.
$$

Thus

$$
  V \supset C_1
    \,, \phantom{AAAA}
  X \setminus Cl(V) \supset C_2
$$

are two disjoint open neighbourhoods, as required.

=--






[[!include main separation axioms -- as lifting properties]]







### Tietze extension and lifting property
 {#TietzeEtensionAndLiftingProperty}

The [[Tietze extension theorem]] applies to normal spaces.

In fact the Tietze extension theorem can serve as a basis of a [[category theory|category theoretic]] characterization of normal spaces: a (Hausdorff) space $X$ is normal if and only if every function $f \colon A \to \mathbb{R}$ from a [[closed subspace]] $A \subset X$ admits an [[extension]] $\tilde{f}: X \to \mathbb{R}$, or what is the same, every [[regular monomorphism]] into $X$ in $Haus$ has the [[left lifting property]] with respect to the map $\mathbb{R} \to 1$. (See _[[separation axioms in terms of lifting properties]]_ ([Gavrilovich 14](#Gavrilovich14)) for further categorical characterizations of various topological properties in terms of lifting problems.)  


### The category of normal spaces
 {#CategoryOfNormalSpaces}

Although normal (Hausdorff) spaces are "[[nice topological spaces]]" (being for example [[Tychonoff spaces]], by [[Urysohn's lemma]]), the [[category]] of normal topological spaces with [[continuous maps]] between them seems not to be very well-behaved. (Cf. the rule of thumb expressed in [[dichotomy between nice objects and nice categories]].) It admits [[equalizers]] of pairs of maps $f, g: X \rightrightarrows Y$ (computed as in $Top$ or $Haus$; one uses the easy fact that closed subspaces of normal spaces are normal). However it curiously does not have [[products]] -- or at least it is not closed under products in $Top$, as shown by Counter-Example \ref{Morse}. It follows that this category is not a [[reflective subcategory]] of $Top$, as $Haus$ is. 

+-- {: .num_remark #retracts} 
###### Remark 
A small saving grace is that the category of normal spaces is [[Cauchy complete category|Cauchy complete]], in fact is closed under retracts in $Top$. This is so whether or not the Hausdorff condition is included. (If $r: Y \to X$ retracts $i: X \to Y$, then $r$ is a quotient map and $i$ is a subspace inclusion. If $A, B$ are closed and disjoint in $X$, then $r^{-1}(A), r^{-1}(B)$ are closed and disjoint in $Y$. Separate them by disjoint open sets $U \supseteq r^{-1}(A), V \supseteq r^{-1}(B)$ in $Y$; then $i^{-1}(U), i^{-1}(V)$ are disjoint open sets separating $i^{-1} r^{-1}(A) = A, i^{-1} r^{-1}(B) = B$ in $X$.) 
=--

More at the page _[[colimits of normal spaces]]_. 


## References

The class of normal spaces was introduced by Tietze (1923) and Aleksandrov--Uryson (1924). 

* Ryszard Engelking, _General topology_, (Monographie Matematyczne, tom 60) Warszawa 1977; expanded Russian edition Mir 1986.


Discussion of [[separation axioms in terms of lifting properties]] is due to:

* {#Gavrilovich14} [[Misha Gavrilovich]], *Point set topology as diagram chasing computations*, ([arXiv:1408.6710](https://arxiv.org/abs/1408.6710)). 



[[!redirects normal space]]
[[!redirects normal spaces]]
[[!redirects Normal space]]
[[!redirects Normal spaces]]

[[!redirects normal topological space]]
[[!redirects normal topological spaces]]

[[!redirects T4]]

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

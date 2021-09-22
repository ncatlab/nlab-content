
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Regular spaces
* table of contents
{: toc}

## Idea

A _regular space_ is a [[topological space]] (or variation, such as a [[locale]]) that has, in a certain sense, enough [[regular open subspaces]].  The condition of regularity is one of the [[separation axioms]] satsified by every [[metric space]] (and in this case, by every pseudometric space).


## Definitions

Fix a [[topological space]] $X$.

The classical definition is this: that if a point and a closed set are disjoint, then they are separated by neighbourhoods.  In detail, this means:
+-- {: .num_defn #classical}
###### Definition
Given any point $a$ and closed set $F$, if $a \notin F$, then there exist a neighbourhood $V$ of $a$ and a neighbourhood $G$ of $F$ such that $V \cap G$ is empty.
=--

In many contexts, it is more helpful to change perspective, from a closed set that $a$ does *not* belong to, to an open set that $a$ *does* belong to.  Then the definition reads:
+-- {: .num_defn #constructive}
###### Definition
Given any point $a$ and neighbourhood $U$ of $a$, there exist a neighbourhood $V$ of $a$ and an open set $G$ such that $V \cap G = \empty$ but $U \cup G = X$.
=--
You can think of $V$ as being half the size of $U$, with $G$ the exterior of $V$.  (In a [[metric space]], or even in a [[uniform space]], this can be made into a proof.)

If we apply the regularity condition twice, then we get what at first might appear to be a stronger result:
+-- {: .num_defn #closed}
###### Definition
Given any point $a$ and neighbourhood $U$ of $a$, there exist a neighbourhood $W$ of $a$ and an open set $G$ such that $Cl(W) \cap Cl(G) = \empty$ but $U \cup G = X$ (where $Cl$ indicates topological closure).
=--
+-- {: .proof}
###### Proof of equivalence
Find $V$ and $G$ as above.  Now apply the regularity axiom to $a$ and the interior $Int(V)$ of $V$ to get $W$ (and $H$).
=--
In terms of the classical language of separation axioms, this says that $a$ and $F$ are separated by *closed* neighbourhoods.

Sometimes one includes in the definition that a regular space must be $T_0$:
+-- {: .un_defn #T0}
###### Definition (of T&#x2080;)
A space is $T_0$ if, given any two points, if each neighbourhood of either is a neighbourhood of the other, then they are equal.
=--
Other authors use the weaker definition above but call a regular $T_0$ space a __$T_3$ space__, but then that term is also used for a (merely) regular space.  An unambiguous term for the weaker condition is an __$R_2$ space__, but hardly anybody uses that.

We have
+-- {: .num_theorem #T3isHausdorff}
###### Theorem
Every $T_3$ space is [[Hausdorff space|Hausdorff]].
=--
+-- {: .proof}
###### Proof
Suppose every neighbourhood of $a$ meets every neighbourhood of $b$; by $T_0$ (and symmetry), it\'s enough to show that each neighbourhood $U$ of $a$ is a neighbourhood of $b$.  Use regularity to get $V$ and $G$.  Then $G$ cannot be a neighbourhood of $b$, so $U$ is.
=--
Since every Hausdorff space is $T_0$, a less ambiguous term for a $T_3$ space is a __regular Hausdorff space__.

It is possible to describe the regularity condition fairly simply entirely in terms of the algebra of open sets.  First notice the relevance above of the condition that $Cl(V) \subset U$; we write $V \subset\!\!\!\!\subset U$ in that case and say that $V$ is __well inside__ $U$.  We now rewrite this condition in terms of open sets and regularity in terms of this condition.
+-- {: .num_defn #locale}
###### Definition
Given sets $U, V$, then $V \subset\!\!\!\!\subset U$ iff there exists an open set $G$ such that $V \cap G = \empty$ but $U \cup G = X$.  Then $X$ is regular iff, given any open set $U$, $U$ is the union of all of the open sets that are well inside $U$.
=--
This definition is suitable for [[locales]].  As the definition of a Hausdroff locale is rather more complicated, one often speaks of compact regular locales where classically one would have spoken of [[compact Hausdorff space|compact Hausdorff spaces]]. (The theorem that compact regular $T_0$ spaces and compact Hausdorff spaces are the same works also for locales, and every locale is $T_0$, so compact regular locales and compact Hausdorff locales are the same.)

The condition that a space $X$ be regular is related to the _[[regular open sets]]_ in $X$, that is those open sets $G$ such that $G$ is the interior of its own closure.  (In the [[Heyting algebra]] of open subsets of $X$, this means precisely that $G$ is its own [[double negation]]; this immediately generalises the concept to locales.)  Basically, we start with a neighbourhood $U$ of $x$ and reduce that to a closed neighbourhood $Cl(V)$ of $x$.  Then $Int(Cl(V))$ is a regular open neighbourhood of $x$.

This gives us another way to characterise regular spaces, as follows:
+-- {: .num_defn #closed_basis}
###### Definition
Given a neighbourhood $U$ of $x$,
there is a closed neighbourhood of $x$ that is contained in $U$.
(Equivalently, $x$ has a regular open neighbourhood, or indeed any neighbourhood, well inside $U$.)
In other words, the closed neighbourhoods of $x$
form a local base (a base of the [[neighbourhood filter]]) at $x$.
=--

\begin{remark}\label{regularOpenWarning}
**(Warning)**
\linebreak
It is *not* sufficient that the regular open neighbourhoods themselves form a local base of each point; see Counterexample \ref{dppesFriendCounterexample}. It\'s the *closures* of the regular open neighbourhoods (which are arbitrary closed neighbourhoods) that form the basis. But compare semiregular spaces [below](#semiregular).
\end{remark}

In [[constructive mathematics]], Definition \ref{constructive} is good; then everything else follows without change, except for the equivalence with \ref{classical}. Even then, the classical separation axioms hold for a regular space; they just are not sufficient.


## Variations

Following up on Definition \ref{closed_basis}, we have:
+-- {: .num_cor #regular_basis}
###### Corollary
For any regular space $X$,
the regular open sets form a basis for the topology of $X$.
=--
+-- {: .proof}
###### Proof
For any closed neighbourhood $V$ of $x \in X$,
the interior $Int(V)$ is a regular open neighbourhood of $x$.
Using Definition \ref{closed_basis} finishes the proof.
=--
This suggests a slightly weaker condition, that of a __semiregular space__:
+-- {: .un_defn #semiregular}
###### Definition (of semiregular)
The regular open sets form a basis for the topology of $X$.
=--

As we\'ve seen above, a regular $T_0$ space ($T_3$) is [[Hausdorff space|Hausdorff]] ($T_2$); we can also remove the $T_0$ condition from the latter to get $R_1$:
+-- {: .un_defn #R1}
###### Definition (of R&#x2081;)
Given points $a$ and $b$, if every neighbourhood of $a$ meets every neighbourhood of $b$, then every neighbourhood of $a$ is a neighbourhood of $b$.
=--
It is immediate that $T_2 \equiv R_1 \wedge T_0$, and the proof above that $T_3 \Rightarrow T_2$ becomes a proof that $R_2 \Rightarrow R_1$; that is, every regular space is $R_1$.  An $R_1$ space is also called _preregular_ (in _[[HAF]]_) or _reciprocal_ (in [[convergence space]] theory).


A bit stronger than regularity is _complete regularity_; a bit stronger than $T_3$ is $T_{3\frac{1}{2}}$.  The difference here is that for a [[completely regular space]] we require that $a$ and $F$ be separated *by a function*, that is by a continuous real-valued function.  See [[Tychonoff space]] for more. This strengthening implies (Tychonoff Embedding Theorem) that the space embeds into a product of [[metric space]]s.

For locales, there is also a weaker notion called [[weakly regular locale|weak regularity]], which uses the notion of [[fiberwise closed sublocale]] instead of ordinary closed [[sublocales]].


## Examples 
 {#Examples}

+-- {: .num_example #metricSpaceExample}
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

\begin{example}\label{KtopCounterexample}
**(counter example)**
\linebreak
The [[real numbers]] equipped with their [[K-topology]] $\mathbb{R}_K$ are a [[Hausdorff topological space]] which is not a [[regular Hausdorff space]] (hence in particular not a [[normal Hausdorff space]]).
\end{example}

\begin{proof}
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
\end{proof}

\begin{example}\label{dppesFriendCounterexample}
**(counter example)**
\linebreak
Let $\bigl((0, 1)\times(0, 1)\bigr)\cup\{0\}$ be equipped with the Euclidean topology on $(0, 1)\times(0,1)$ and have the sets of the form $(0, 1/2)\times(0, \varepsilon)\cup\{0\}$ (for $\varepsilon \in (0, 1)$) as a basis of open neighbourhoods for the point $0$.

* This space is not regular since we cannot separate $0$ from $[1/2, 1)\times(0,1)$
* Every point $p = (p_1, p_2) \neq 0$ has the euclidean balls of centre $p$ and radius $\varepsilon \in (0, p_1)$ as regular neighbourhood basis.
* The provided basis for the neighbourhoods of $0$ already is a system of regular open sets.

Therefore, this space has the property that every point has a neighbourhood basis of regular open sets (and consequently, the space is semiregular, an even weaker property), but $0$ does not have a neighbourhood basis of closed sets (and consequently, the space is *not* regular).  The problem is that, while every basic neighbourhood of $0$ (and therefore every neighbourhood of $0$ whatsoever) contains a regular open neighbourhood of $0$, none of these basic neighbourhoods contains the closure of any of these regular open neighbourhoods (or any other closed neighbourhood of $0$).
\end{example}



\begin{example}\label{LocallyCompactHausdorffSpacesAreCompletelyRegular}
  [[locally compact Hausdorff space|Locally compact Hausdorff spaces]] are completely regular.
\end{example}
(e.g. [Engelking 1989, Thm. 3.3.1](#Engelking89))
\begin{remark}
  Example \ref{LocallyCompactHausdorffSpacesAreCompletelyRegular} plays a key role in discussion of [[slice theorem|slice theorems]], see there for more.
\end{remark}


## Properties

* [[second-countable regular spaces are paracompact]]

* [[paracompact Hausdorff spaces are normal|paracompact Hausdorff spaces are regular]]



## Related concepts

[[!include main separation axioms -- table]]

A [[uniform space]] is automatically regular and even completely regular, at least in [[classical mathematics]].  In [[constructive mathematics]] this may not be true, and there is an intermediate notion of interest called [[uniform regularity]].

Every regular space comes with a naturally defined (point-point) [[apartness relation]]: we say $x # y$ if there is an open set containing $x$ but not $y$.  This can be defined for any topological space and is obviously irreflexive, but in a regular space it is symmetric and a [[comparison]], hence an apartness.  For symmetry, if $x\in U$ and $y\notin U$, let $V$ be an open set containing $x$ and $G$ an open set such that $V\cap G = \emptyset$ and $G\cup U = X$; then $y\in G$ (since $y\notin U$) while $x\notin G$ (since $x\in V$).  With the same notation, to prove comparison, for any $z$ we have either $z\in G$, in which case $z # x$, or $z\in U$, in which case $z # y$.  Note that this argument is valid constructively; indeed, classically, the much weaker $R_0$ [[separation axiom]] is enough to make this relation symmetric, and it is a comparison on any topological space whatsoever.

Note that if a space is [[Hausdorff space|localically strongly Hausdorff]] (a weaker condition than regularity), then it has an apartness relation defined by $x \# y$ if there are disjoint open sets containing $x$ and $y$.  If $X$ is regular, then this coincides with the above-defined apartness.


## References

Textbook accounts:

* {#Engelking89} Ryszard Engelking, *General Topology*, Sigma series in pure mathematics **6**, Heldermann 1989 ([ ISBN 388538-006-4](https://www.heldermann.de/SSPM/SSPM06/sspm06.htm))

[[!redirects completely regular]]
[[!redirects completely regular space]]

[[!redirects regular space]]
[[!redirects regular spaces]]
[[!redirects R2 space]]
[[!redirects R2 spaces]]
[[!redirects T3 space]]
[[!redirects T3 spaces]]

[[!redirects regular Hausdorff space]]
[[!redirects regular Hausdorff spaces]]
[[!redirects regular Hausdorff topological space]]
[[!redirects regular Hausdorff topological spaces]]

[[!redirects regular topological space]]
[[!redirects regular topological spaces]]
[[!redirects regular topology]]
[[!redirects regular topologies]]
[[!redirects R2 topology]]
[[!redirects R2 topologies]]
[[!redirects T3 topology]]
[[!redirects T3 topologies]]
[[!redirects T3 axiom]]

[[!redirects regular locale]]
[[!redirects regular locales]]


[[!redirects semiregular space]]
[[!redirects semiregular spaces]]

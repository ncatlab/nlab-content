
{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}
{:myrmk: .un_remark style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;font-size:90%;"}
{:goal: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Schedules
* table of contents
{: toc}

## Idea
{#idea}

Let $X$ be a [[topological space]] and $\mathcal{U}$ an [[open cover]] thereof.  A ([[continuous function|continuous]]) path $\gamma \colon I \to X$ can pass through many of the elements of $\mathcal{U}$ as it winds its way around $X$.  We can decompose that path into segments such that each segment lies wholly inside one of the [[open sets]] in $\mathcal{U}$.  The **Schedule Theorem** says that this can be done continuously over all paths in $X$.

This was proved by [Dyer and Eilenberg](#DyerEilenberg) and applied to the question of fibrations over numerable spaces.

## Schedules
{#schedules}

The idea of a schedule is that it is a way of decomposing a length into pieces and then assigning a label to each piece.  This clearly fits with the stated purpose of these things since we wish to decompose a path into pieces and assign an open set to each piece.

To make this precise, we start with a set of labels.  Following Dyer and Eilenberg, let us write this as $A$.  Lengths are positive [[real numbers]] and so we also need the set of such, Dyer and Eilenberg denote this by $T$; thus $T \coloneqq \mathbb{R}_{\ge 0}$.

+-- {: mynumdef #schmon}
###### Definition
The **schedule monoid** of $A$ is the [[free monoid]] on the [[set]] $A \times T$.  It is written $S A$.  Its elements are **schedules** in $A$.
=--

A schedule in $A$ is thus a finite [[order|ordered]] list of pairs $(a,t)$ where $a \in A$ and $t \in T$.

There are two notions of *length* for a schedule.  There is the *word length* which simply counts the number of pairs.  Then there is the function $l \colon S A \to T$ defined by $l((a_1,t_1) \cdots (a_k,t_k)) = t_1 + \cdots + t_k$.  There is also a right action of $T$ on $S A$ which simply multiplies all of the lengths: $((a_1,t_1) \cdots (a_k,t_k)) \cdot t = ((a_1,t_1 t) \cdots (a_k,t_k t))$.  Then $l(s t) = l(s) t$.

+-- {: mynumdef #reduced}
###### Definition
A schedule is said to be **reduced** if all of its terms, $(a,t)$, have non-zero length, i.e. $t \gt 0$.  The set of reduced schedules forms a submonoid of $S A$ which is written $R S A$.
=--

The empty schedule is reduced.

There is a [[retraction]] map $\rho \colon S A \to R S A$ defined by removing all terms with zero length part.

The schedule monoid is given a [[topology]] so that the labels are discrete and the lengths topologised as usual.  More concretely, given a word $a_1 a_2 \dots a_k$ of elements in $A$, the set of schedules of the form $(a_1,t_1) (a_2,t_2) \cdots (a_k,t_k)$ is in bijection with $T^k$ and we make that bijection a homeomorphism.  Then $S A$ is topologised by taking the coproduct over the set of words in $A$.  The reduced schedule monoid is topologised as the quotient of this.

## Paths
{#paths}

Let $X$ be a [[topological space]].  Let $P X$ denotes its [[Moore path space]].  Suppose that we have a family $\mathcal{U}$ of subsets of $X$ indexed by some set $A$.  Then we consider a schedule in $A$ as giving an ordered list of these subsets together with the times to be spent in each.  For a path in $X$, and a schedule of the appropriate length, then we can ask whether or not the path *fits* (or obeys) the schedule.  We make that precise as follows.

+-- {: mynumdef #fits}
###### Definition
Suppose that we have $\alpha \in P X$ and $s \in S A$, and suppose that $s = (a_1, t_1) \cdots (a_k,t_k)$.  Then we say that $\alpha$ **fits the schedule** s, written $\alpha \Vert s$, if the following conditions hold:

1. $l(\alpha) = l(s)$
2. We can split $\alpha$ into subpaths according to the times $\{t_i\}$.  Let $\alpha_i$ be the $i$th segment.  Then $\alpha_i \in P U_{a_i}$.
=--

Here, $l \colon P X \to T$ is the function that assigns to a Moore path its length.  The schedule designates a decomposition of $[0,l]$ into subintervals with $t_i$ being the length of the $i$th subinterval.  Then saying that $\alpha$ fits the schedule $s$ means that $\alpha$ spends the $i$th subinterval in the open set $U_{a_i}$.


## Schedule Theorem
{#secschthm}

We can now state the main theorem.

+-- {: .num_theorem #schthm}
###### Theorem
Let $X$ be a [[topological space]].  Let $\mathcal{U}$ be a [[locally finite cover|locally finite]] [[open covering]] of $X$ by [[numerable]] open sets with indexing set $A$.  Then there is a covering $\mathcal{F}$ of $P X$ by [[closed sets]] and a family of [[continuous functions]] $f \colon F \to S A$, indexed by $F \in \mathcal{F}$ such that:

1. for each $\alpha \in P X$, there some finite subfamily $\{F_1, \dots, F_k\} \subseteq \mathcal{F}$ such that $\alpha$ is in the interior of $\bigcup F_j$,
1. for each $\alpha \in F$, $\alpha \Vert f_F(\alpha)$, and
2. for each $\alpha \in F \cap F'$, $\rho(f_F(\alpha)) = \rho(f_{F'}(\alpha))$
=--

The first condition is purely about the covering.  Dyer and Eilenberg use the term *local covering* for a covering by closed sets with this property.

+-- {: .num_corollary #schcor}
###### Corollary
There exists a [[continuous function]] $h \colon P X \to R S A$ such that $\alpha \Vert h(\alpha)$ if $l(\alpha) \gt 0$ and $h(\alpha) = \Lambda$ if $l(\alpha) = 0$.
=--

Here, $\Lambda \in R S A$ is the empty word.

## Globalisation Theorem
{#secglobal}

The original motivation for the notion of *schedules* was to prove the *globalisation theorem* for (Hurewicz) [[Hurewicz fibration|fibrations]].

+-- {: .num_theorem #global}
###### Theorem
Let $p \colon Y \to B$ be a continuous function.  Suppose that $\mathcal{U}$ is a locally finite covering of $B$ by numerable open sets with the property that for each $U \in \mathcal{U}$ then the restriction $p_U \colon Y_U \to U$ is a fibration.  Then $p$ is a fibration.
=--

The link between the globalisation theorem and the schedule theorem is the characterisation of Hurewicz fibrations in terms of [[Hurewicz connections]].

## Proof of the Schedule Theorem
{#secproof}

Let $X$ be a topological space.  Let $\mathcal{U}$ be a locally finite open covering of $X$ by numerable open sets and indexing set $A$.

Let us write $A^*$ for the free monoid on $A$.  Then there is a function $A^* \times T \to S A$ which takes $(a_1 a_2 \cdots a_k, t)$ to the schedule $(a_1,t/k)(a_2,t/k)\cdots (a_k,t/k)$.  We say that a path $\alpha \in P X$ *evenly fits* $s \in A^*$, and write this as $\alpha \Vert_e s$, if it fits the schedule corresponding to $(s,l(\alpha))$.

We need an initial technical result.

+-- {: .num_lemma #even}
###### Lemma
There is a locally finite covering $\mathcal{W} = \{W_s \mid s \in A^*\}$ of $P X$ by numerable open sets such that for $\alpha \in W_s$ then $\alpha$ evenly fits the word $s$.
=--

+-- {: myrmk}
###### Remark
Let us explain why this is a reasonable result.  Consider a path, $\alpha$, of length $l$.  We pull back the cover $\mathcal{U}$ to a cover of $[0,l]$.  Using compactness of $[0,l]$ we can replace the pull-back cover by a finite family of open subintervals of $[0,l]$ which cover $[0,l]$.  Each subinterval is labelled by an element of $\mathcal{U}$ (though a label might be reused).  As the family is finite, the intersections are finite and therefore have a minimum length.  Choose $n$ big enough so that $l/n$ is less than this minimum length.  Then consider the subdivision of $[0,l]$ given by $\{0,1/n,\dots,l/n\}$.  Our conditions on $n$ guarantee that every intersection of subintervals contains at least one of these division points.  We can therefore assign to each subinterval of the form $[k/n, (k+1)/n]$ one of the original family of subintervals that contains it.  Then we can assign the corresponding element of $\mathcal{U}$.  Thus $\alpha$ fits evenly the corresponding word.

Thus the sets $Y_s \coloneqq \{\alpha : \alpha \|_e s\}$ cover $P X$.  That they are open follows from the fact that the condition for membership depends on certain compact sets lying in certain open sets and we use the [[compact-open topology]] on $P X$.

What is more complicated is reducing the family to a locally finite one.
=--

As $\mathcal{W}$ is locally finite and its elements are numerable, we can choose a numeration that is also a partition of unity.  That is, we can choose continuous functions $q_s \colon X \to [0,1]$ with the property that $q_s^{-1}((0,1]) = W_s$ and $\sum_s q_s = 1$.

Let $\mathcal{B}$ be the set of finite subsets of $A^* \setminus \Lambda$ (where $\Lambda$ is the empty word).  For $b \in \mathcal{B}$ we define

$$
\begin{aligned}
D_b &\coloneqq \{\alpha \in P X \mid \sum_{s \in b} q_s(\alpha) = 1 \} \\
&=\{ \alpha \in P X \mid q_s(\alpha) = 0 \; \text{for all}\; s \notin b\}
\end{aligned}
$$



This is a covering of $P X$ by closed sets.  As $\mathcal{W}$ is locally finite, for $\alpha \in P X$ there is some neighbourhood $V$ which meets only a finite number of the $\mathcal{W}$.  These are indexed by elements of $A^*$, indeed of $A^* \setminus \Lambda$, and so the set of indices is an element, say $b$, of$ \mathcal{B}$.  Then for $s \notin b$, $q_s \mid V = 0$ and so for $\beta \in V$, $\sum_{s \in b} q_s(\beta) = 1$, whence $V \subseteq D_b$.  Thus each $\alpha$ is contained in the interior of some $D_b$.

Now let us put a [[total ordering]] on $A^*$.  This induces a total ordering on each $b \in \mathcal{B}$ and thus allows us to define the partial sums of the summation $\sum_{s \in b} q_s$.  Write these as $Q_i$, with $Q_0$ as the zero function.

Fix $b \in \mathcal{B}$ and write it as $b = \{s_1,s_2,\dots,s_k\}$ in the inherited ordering.  Let $e = (l_1,r_1,\dots,l_k,r_k)$ be a list of integers with the property that $1 \le l_i \le r_i \le \#s_i$ where $\#s_i$ is the word length of $s_i$.  Define:

$$
D_{(b,e)} = \left\{ \alpha \in D_b \mid \frac{l_i -1}{\# s_i} \le Q_{i - 1}(\alpha) \le \frac{l_i}{\# s_i} \; \text{and} \; \frac{r_i - 1}{\# s_i} \le Q_i(\alpha) \le \frac{r_i}{\# s_i} \right\}.
$$

This is closed in $D_b$ and the collection $\{D_{(b,e)}\}$ is a finite cover of $D_b$.
The family $\{D_{(b,e)}\}$ ranging over all $b \in \mathcal{B}$ and suitable $e$ is the family $\mathcal{F}$ that we are looking for.  It has the required covering property since the interiors of the $D_b$ cover $P X$.

Define $f_{(b,e)} \colon D_{(b,e)} \to S A$ as follows:

$$
f_{(b,e)}(\alpha) = \sigma_1 \cdots \sigma_k l(\alpha)
$$

where $\sigma_i$ is the schedule with $\# \sigma_i = r_i - l_i + 1$ and $l(\sigma_i) = q_{s_i}(\alpha)$, and if $s_i = a_1 \cdots a_n$ then if $l_i \lt r_i$ we have

$$
\sigma_i = \left( a_{l_1}, \frac{l_i}{n} - Q_{i - 1}(\alpha)\right) \left(a_{l_i+1}, \frac{1}{n} \right) \cdots \left(a_{r_i - 1}, \frac{1}{n} \right) \left( a_{r_i}, Q_i(\alpha) - \frac{r_i - 1}{n} \right)
$$

otherwise, $\sigma_i = (a_{l_i}, Q_i(\alpha) - Q_{i-1}(\alpha))$.

This is continuous and for $\alpha \in D_{(b,e)}$ then $\alpha$ fits $f_{(b,e)}(\alpha)$.  Moreover, for $\alpha \in D_{(b,e)} \cap D_{(b',e')}$ then $\rho f_{(b,e)}(\alpha) = \rho f_{(b',e')}(\alpha)$.

## References
{#refs}

* {#MR0963792} Dyer, E. and E., Samuel. (1988). Globalizing fibrations by schedules. _Fund. Math._, _130_, 125&#8211;136. [MR0963792](http://www.ams.org/mathscinet-getitem?mr=963792)

* Dyer, Eilenberg, MR0963792
 {#DyerEilenberg}

[[!redirects schedules]]

[[!redirects schedule theorem]]

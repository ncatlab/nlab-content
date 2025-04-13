
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


# The locale of real numbers
* table of contents
{: toc}

## Summary

This page gives an elementary description of the [[locale]] of [[real numbers]], that is the localic [[real line]]. The development is manifestly [[constructive mathematics|constructive]] and even [[predicative mathematics|predicative]] over the [[natural numbers]] (although we are somewhat careless with the language and do not always point out when a set may predicatively be a [[proper class]]).  Ideally, we will show that our construction satisfies the seven 'headline properties' of the real line described by [Bauer & Taylor](http://www.paultaylor.eu/ASD/dedras/intro) (although so far we cover only the [[Heine–Borel theorem]]).

The exposition here is pretty much [[Toby Bartels]]\'s own work, although of course the basic ideas are well known to many.  In particular, the Zigzag Lemma \ref{zigzaglemma} is Bartels\'s as far as they know (but it\'s not very deep, just bookkeeping).  The version of [[Cousin's theorem|Cousin's Theorem]] that appears here may also be original.


## Idea
{#idea}

To describe the locale of the real numbers, we need first of all to describe what an _open_ (in the axiomatic sense, equivalent to an [[open sublocale]]) in the real line is.  The key insight is that an open subspace is determined by the [[open intervals]] of [[rational numbers]] that it contains.  This is analogous to the key insight of [[Richard Dedekind]]\'s [definition of real number](real+number#Dedekind): that a point in the real line is determined by which open intervals of [[rational numbers]] that it belongs to.  (Once one is talking about rational numbers, things are manageable.)


## Opens

An __open__ in the real line is a [[binary relation]] ${\sim}$ on the [[rational numbers]] that satisfies the four properties listed below.  Intuitively, we have $a \sim b$ iff the open [[interval]] $(a,b)$ is contained in the corresponding [[open subspace|open set]].

1. If $a \geq b$, then $a \sim b$.

2. If $a \geq b \sim c \geq d$, then $a \sim d$.

3. If $a \sim b \gt c \sim d$, then $a \sim d$.

4. If $b \sim c$ whenever $a \lt b$ and $c \lt d$, then $a \sim d$.

In practice, rather than using relation-like symbols for opens, we mimic the set-theoretic notation and terminology from [[point-set topology]].  So if $G$ is an open in the real line, then we write $(a,b) \subseteq G$ to mean that $a$ is related to $b$ through $G$ and say that $G$ __contains__ the interval from $a$ to $b$ and that this interval is __contained in__ $G$.

In this notation, and writing $(a, b) \subseteq (c, d)$ for $c \leq a$ and $b \leq d$, and $(a, b) \Subset (c, d)$ for $c \lt a$ and $b \lt d$, these requirements say:

1. If $a \geq b$, then $(a, b) \subseteq G$.

2. If $(a, d) \subseteq (b, c)$ and $(b, c) \subseteq G$, then $(a, d) \subseteq G$.

3. If $c \lt b$ and $(a, b), (c, d) \subseteq G$, then $(a, d) \subseteq G$.

4. If $(b, c) \subseteq G$ for all $(b, c) \Subset (a, d)$, then $(a, d) \subseteq G$.

Property (1) is motivated because $(a,b)$ is [[empty subset|empty]] whenever $a \geq b$. Property (2) is motivated because inclusion is [[transitive relation|transitive]]. Property (3) is motivated because if $c \lt b$, then $(a, d) = (a, b) \cup (c, d)$. Property (4) is motivated because $\bigcup_{(b, c) \Subset (a, d)} (b, c) = (a, d)$.

The really interesting property is property (3). It immediately generalizes as follows:

* If
  \[
     a_1 \sim b_1 \gt a_2 \sim b_2 \gt \cdots \gt a_n \sim b_n
  ,\]
  then $a_1 \sim b_n$.

We call the combined hypothesis of this property a __zigzag__; each hypothesis $a_i \sim b_i$ is a __zig__, and each hypothesis $b_i \gt a_{i+}$ is a __zag__.  To indicate the length of a zigzag, we will count the zigs; the zigzag above has $n$ zigs (and $n - 1$ zags).  A typical nondegenerate zigzag with $3$ zigs is shown below; it consists of $3$ overlapping open intervals, each of which belongs to a given open set; we are motivated to conclude that the entire interval from $a_1$ to $b_3$ belongs to that open set.

+-- {: style="text-align:center"}
[[!include zigzag of real numbers - SVG]]
=--

Thus the zigzag property for $n = 2$ is property (3), the zigzag property for $n = 1$ is trivial (if $a \sim b$, then $a \sim b$), and the zigzag property for $n \gt 2$ may be proved by [[induction]].

We can incorporate property (2) into this by saying:

* If
  \[
     a \geq a_1 \sim b_1 \gt a_2 \sim b_2 \gt \cdots \gt a_n \sim b_n \geq b
  ,\]
  then $a \sim b$.

Then you can think of property (1) as the zigzag property for $n = 0$.  Alternatively, we can incorporate property (4) by saying:

* If, whenever $a \lt a_1$ and $b_n \lt b$, there is a zigzag
  \[
     a_1 \sim b_1 \gt a_2 \sim b_2 \gt \cdots \gt a_n \sim b_n
  ,\]
  then $a \sim b$.

Or by making both modifications, we can stuff the entire definition into a single statement.


## The Zigzag Lemma

A zigzag may not look like the picture above; instead of an orderly progression, the zigs and zags may be wild swings that are undone by other zags and zigs.  It is sometimes convenient to replace a zigzag by a more orderly one.  Of course, this is easy if all of the zigs belong to a single open, since (by property (3) of the definition of an open), the whole zigzag can be replaced by a single zig.  But we\'ll also want to consider zigzags where the zigs are taken from different opens.  The following definitions make precise what kind of zigzag we\'ll want, and then there will be a lemma that we can indeed have this.

+-- {: .num_defn #zigzagdefn}
###### Definitions

Given rational numbers $a$ and $b$ and a positive natural number $n$, a $2n$-tuple $(a_1,b_1,\ldots,a_n,b_n)$ of rational numbers forms a __zigzag of length $n$ from $a$ to $b$__ if we have:

* $a = a_1$, $b = b_n$, and
* $b_i \gt a_{i+}$ for $i = 1, \ldots, n - 1$.

A zigzag of positive length is __orderly__ if we additionally have:

* $a_i \lt a_{i+}$ for $i = 1, \ldots, n - 1$,
* $a_i \lt b_i$ for $i = 1, \ldots, n$, and
* $b_i \lt b_{i+}$ for $i = 1, \ldots, n - 1$.

As a technicality, if $a \geq b$, then we also count the empty $0$-tuple as an __orderly zigzag of length $0$__ from $a$ to $b$.  (Notice that no zigzag of positive length can be orderly from $a$ to $b$ when $a \geq b$.)

Given additionally a collection $\mathcal{U}$ of opens, a zigzag (orderly or not) has __zigs from $\mathcal{U}$__ if every pair $(a_i,b_i)$ is contained in at least one member of $\mathcal{U}$.
=--

Now we can replace any zigzag with an orderly zigzag with zigs from the same opens:

+-- {: .num_lemma #zigzaglemma}
###### Lemma
(Zigzag Lemma)

Given rational numbers $a$ and $b$, a natural number $n$, a collection $\mathcal{U}$ of opens, and a zigzag from $a$ to $b$ of length $n$ with zigs from $\mathcal{U}$, there exists an orderly zigzag from $a$ to $b$ of length at most $n$ with zigs from $\mathcal{U}$.
=--

+-- {: .proof}
###### Proof

If $a \geq b$, then we use a zigzag of length $0$.  Otherwise, we assume that $a \lt b$ and prove the lemma by induction on $n$.  If $n = 1$, then the original zigzag is orderly since $a \lt b$.

Now assume (as an inductive hypothesis) that the lemma holds for zigzags of length $k$ for some $k \geq 1$.  A zigzag of length $k+$ consists of a zig $(a,b_1)$ from some open in $\mathcal{U}$, a zag $b_1 \gt a_2$, and a zigzag of length $k$ from $a_2$ to $b$ with zigs from $\mathcal{U}$.  Using the inductive hypothesis, replace the zigzag of length $k$ with an orderly zigzag of length $l \leq k$ from $a_2$ to $b = b_{l+}$ with zigs from $\mathcal{U}$.  We now have a zigzag of length $l+ \leq k+$ from $a$ to $b$ with zigs from $\mathcal{U}$.

If $a \lt a_2$ and $b_1 \lt b_2$, then also $a \lt a_2 \lt b_1$, so this zigzag of length $l+$ from $a$ to $b$ is orderly.

Next suppose that $a \lt a_2$ but $b_1 \geq b_2$.  In this case, consider the largest value of $i \geq 2$ such that $b_1 \geq b_i$; if $i = l+$, then we can use the orderly zigzag of length $1$ from $a$ to $b$, which is contained in the same open as $(a,b_1)$ was, since $b_1 \geq b_i = b$.  If $i \leq l$ instead, then take the orderly zigzag from $a_{i+}$ to $b$, and precede it with the zig $(a,b_i)$, to get a zigzag of length $l - i + 2 \leq k$ from $a$ to $b$.  This zigzag is orderly, because $a \lt a_2 \lt a_{i+}$, and its zigs are from $\mathcal{U}$ since $(a,b_i)$ is contained in the same open as $(a,b_1)$ was (since $b_1 \geq b_i$).  So either way, we have an orderly zigzag of length at most $k$ from $a$ to $b$ with zigs from $\mathcal{U}$.

Finally, suppose that $a \geq a_2$.  In this case, consider the largest value of $i \geq 2$ such that $a \geq a_i$, take the orderly zigzag from $a_i$ to $b$, and change $a_i$ to $a$ to get a zigzag from $a$ to $b$.  If $i \leq l$, then this is orderly since $a \lt a_{i+} \lt b_i$; if $i = l+$, then this is orderly since $a \lt b = b_i$.  Either way, $(a,b_i)$ belongs to the same open as $(a_i,b_i)$ did (since $a \geq a_i$), so this orderly zigzag of length $l - i + 2 \leq k$ from $a$ to $b$ still has zigs from $\mathcal{U}$.

In any case, we have a zigzag of length at most $k+$ from $a$ to $b$ with zigs from $\mathcal{U}$, and the induction is complete.
=--

This lemma is used in the proofs of the infinite distributivity law and some results related to measure.


## The frame of opens

The opens form a [[subobject|sub]]-[[poset]] of the [[power set]] $\mathcal{P}(\mathbb{Q} \times \mathbb{Q})$.  This poset is in fact a [[frame]], as we will now show.  (It is *not* a subframe of the power set, since the [[joins]] are different.  It *is* a sub-[[inflattice]] of the power set, although this seems to be a red herring at least for infinitary [[meets]], since those are not part of the frame structure that we need.)

The [[top element|top]] open, denoted $\mathbb{R}$, is the binary relation which is always true.  Given two opens $G$ and $H$, their [[meet]] in the poset of opens, denoted $G \cap H$, is simply their [[logical conjunction|conjunction]], that is their [[intersection]] as [[subsets]] of $\mathbb{Q} \times \mathbb{Q}$.  (In fact, given any collection of opens, their meet is their conjunction.)  It is straightforward to check that $\mathbb{R}$ and $G \cap H$ are opens and to prove that these are the desired meets.  Intuitively, this all works because an open interval will be contained in the intersection of a family of open sets if and only if it is contained in each individual open set.

The [[bottom element|bottom]] open, denoted $\empty$, is the binary relation $\geq$.  That is, $(a,b) \subseteq \empty$ iff $a \geq b$.  It is easy to check that this is an open; it precedes every open by property (1).  Intuitively, this corresponds to the [[empty subset]] of the real line; $(a,b)$ is empty if and only if $a \geq b$.  However, note that $\empty$ is *not* the empty subset of $\mathbb{Q} \times \mathbb{Q}$; the notation follows our topological intuition rather than the [[relation theory|algebra of relations]].

Given two opens $G$ and $H$, their [[join]] in the poset of opens, denoted $G \cup H$, is defined as follows:  $(a,b) \subseteq G \cup H$ if, whenever $a \lt a_1$ and $b_n \lt b$, there exists a zigzag from $a_1$ to $b_n$ with zigs from $G$ and $H$.  It is immediate that this is an open in which $G$ and $H$ are both contained.  Conversely, any open in which $G$ and $H$ are contained must contain this open $G \cup H$, by properties (3) and (4).

More generally, given any collection $\mathcal{U}$ (or family $(G_k)_k$) of opens, their [[join]] in the poset of opens, denoted $\bigcup \mathcal{U}$ (or $\bigcup_k G_k$), is defined as follows:  $(a,b) \subseteq \bigcup \mathcal{U}$ if and only if, whenever $a \lt a_1$ and $b_n \lt b$, there exists a zigzag from $a_1$ to $b_n$ with zigs from $\mathcal{U}$.  (Notice that $a \geq b$ counts even when $\mathcal{U}$ is empty, using zigzags of length $0$.)  The same argument applies as before.  Note that each individual zigzag has finitely many zigs, and therefore involves finitely many of the opens $G_k$, even when taking the join of an infinite collection.

Finally, we must check the distributive law $G \cap \bigcup_k H_k \subseteq \bigcup_k (G \cap H_k)$.  That is, if $a \sim b$ directly through $G$ and $a_1 \sim b_n$ through a zigzag of $H$s for $(a_1,b_n) \Subset (a,b)$, then we need that $a_1 \sim b_n$ through a zigzag in which each zig is related both through $G$ and through some $H$.  To prove this, start with the zigzag of $H$s, and apply the Zigzag Lemma \ref{zigzaglemma} to get an orderly zigzag of $H$s, so that each zig is bounded by $a$ and $b$.  Then these zigs hold for $G$ as well, by property (2).  Therefore, we may interpret each zig using $G \cap H_k$ for some $k$, proving the desired result.

This frame of opens, interpreted as a [[locale]], is __the locale of real numbers__.  As usual, we denote this locale with the same symbol as the top element of its frame, in this case $\mathbb{R}$.  (Of course, the true etymology of the symbols runs in the other order.)


## Open intervals as opens

Given rational numbers $a$ and $b$, the open interval $(a,b)$ may itself be interpreted as an open in the real line, also denoted $(a,b)$, as follows: let $(c,d) \subseteq (a,b)$ hold if every rational number strictly between $c$ and $d$ (in that order) is also strictly between $a$ and $b$ (in that order).  In other words, we interpret '${\subseteq}$' literally as comparing subsets of $\mathbb{Q}$.  It is straightforward to check that this condition does indeed define an open.  There is now a third way to interpret '$(c,d) \subseteq (a,b)$'; interpreting both intervals as opens in the real line, this states that the first is contained in the second.  But again, it is easy to check that this is equivalent; $(c,d) \subseteq (a,b)$ (in the set-theoretic sense) if and only if $(e,f) \subseteq (a,b)$ whenever $(e,f) \subseteq (c,d)$.  Notice that $(a,b) = \empty$ whenever $a \geq b$.

We can actually generalize this somewhat.  Given any set $L$ of rational numbers and any set $U$ of rational numbers, we may define the open $(\inf U, \sup L)$ as follows: let $(a,b) \subseteq (\inf U, \sup L)$ hold if every rational number strictly between $a$ and $b$ (in that order) is greater than some element of $U$ and less than some element of $L$.  If the [[infimum]] of $U$ and the [[supremum]] of $L$ exist in the usual sense as rational numbers, then this agrees with the previous paragraph.  If instead $U$ or $L$ is the set of all rational numbers, then we write $-\infty$ for $\inf U$ or $\infty$ for $\sup L$.  In general, we may interpret $\inf U$ as an [[extended real number|extended]] [[upper real number|upper real]] and $\sup L$ as an extended [[lower real number|lower real]].  Classically, every extended upper or lower real is either a real number, $-\infty$, or $\infty$; only the converse holds constructively.  Notice that $(-\infty,\infty) = \mathbb{R}$.

Since we will refer to them below, we will state for the record the complete definitions of $(-\infty,a)$ and $(a,\infty)$ for a rational number $a$.  We have $(b,c) \subseteq (-\infty,a)$ iff every rational number strictly between $b$ and $c$ is less than $a$, that is iff $b \geq c$ or $c \leq a$.  Similarly, we have $(b,c) \subseteq (a,\infty)$ iff every rational number strictly between $b$ and $c$ is greater than $a$, that is iff $b \geq c$ or $b \geq a$.  A fortiori, $(b,c) \subseteq (-\infty,0)$ if $c = 0$, and $(b,c) \subseteq (1, \infty)$ if $b = 1$.


## Open sets, closed sets, and points

We think of each open as defining an [[open subspace|open subset]] of the real line, but we can equally well think of it as defining a [[closed subspace|closed subset]].  The difference between these perspectives is reflected in [[complement]]ary criteria for when a real number belongs to the set.  So to make sense of this, we must identify the [[point|points]] of the real line.

Recall that a [[real number]] may be defined as a pair $(L,U)$ of [[inhabited set|inhabited]] [[subsets]] of $\mathbb{Q}$ satisfying the following properties:

1. If $a \in L$, then $a \lt b$ for some $b \in L$.
2. If $b \in U$, then $a \lt b$ for some $a \in U$.
3. If $a \in L$ and $b \in U$, then $a \lt b$.
4. If $a \lt b$, then $a \in L$ or $b \in U$.

We define a __point__ of the real line to be a real number in this sense.  Given such a point $x = (L,U)$ and a rational number $a$, we write $a \lt x$ to mean that $a \in L$ and $a \gt x$ to mean that $a \in U$.  If we wish to refer to $L$ and $U$ directly, we may call $L$ the __lower set__ of $x$ and $U$ the __upper set__.

Given a point $x$ and an open $G$, we say that $x$ __belongs__ to $G$, written $x \in G$, if $(a,b) \subseteq G$ for some $a \lt x$ and $b \gt x$; that is, $G$ contains an interval from some element of the lower set to some element of the upper set of $x$.  We have $x \in \mathbb{R}$ since its lower and upper sets are inhabited.  If $x \in G$ and $x \in H$, with $(a,b) \subseteq G$ and $(c,d) \subseteq H$, then $\big(\max(a,c), \min(b,d)\big) \subseteq G \cap H$, so $x \in G \cap H$; note that this argument fails for infinitary intersections.  (The converse, that $x \in G$ and $x \in H$ if $x \in G \cap H$, is immediate.)  Dually, suppose that $x \in \bigcup_k G_k$, as shown by some zigzag (since $a \geq b$ is impossible when $a \lt x$ and $b \gt x$, by 3).  Applying condition (4) of the definition of real number to each zag, we have $a_{i+} \lt x$ or $b_i \gt x$, for each $i \lt n$.  Checking all $2^{n-1}$ possibilities, and knowing that $a_1 \lt x$ and $b_n \gt x$ in any case, we must have $a_i \lt x$ and $b_i \gt x$ for some $i$.  Then we have $x \in G_k$ for some $k$, whichever corresponds to the $i$th zig.  (The converse, that $x \in \bigcup_k G_k$ if $x \in G_k$ for some $k$, is immediate.)

Therefore, each point defines a [[completely prime filter]] on the frame of all opens, which is the definition of a [[point of a locale|point]] in general locale theory.  Conversely, given such a completely prime filter $P$, let $L$ be the set of all rational numbers $a$ such that the open interval $(a, \infty)$ (when interpreted as an open in the real line as defined above) is in $P$, and symmetrically let $U$ be the set of all $a$ such that $(-\infty, a) \in P$.

Given a point $x$ and an open $G$, we say that $x$ __co-belongs__ to $G$, written $x \notin G$, if we never have $a \lt x$, $b \gt x$, and $(a,b) \subseteq G$, which is precisely the [[negation]] of the property that $x \in G$.  We think of this condition as defining a *[[closed subspace|closed]]* set to which $x$ *does* belong.  Notice that $x \notin \bigcup_k G_k$ if and only if $x \notin G_k$ for each $k$, giving the desired behaviour for an arbitrary intersection of closed sets (which corresponds to union of open sets under [[de Morgan duality]]).  We also have that $x \notin \mathbb{R}$ always fails, and $x \notin G \cap H$ if $x \notin G$ or $x \notin H$.  To prove that $x \notin G$ or $x \notin H$ whenever $x \notin G \cap H$, however, we must use [[excluded middle]]; constructively, closed sets don\'t behave well under union.

A related question is whether we can reconstruct $G$ from the set of points which belong to it.  This should be equivalent to the [[fan theorem]], which is classically true and also accepted by [[Jan Brouwer|Brouwer]]\'s school of intuitionism, but refuted in the Russian school in which all real numbers are assumed to be [[computable number|computable]].  (I should check this.)  Arguably, the real lesson of these logical technicalities is that we should remember that opens, not points, are the fundamental concept in a locale.


## The Heine--Borel theorem

The classical [[Heine-Borel theorem|Heine--Borel theorem]], as a statement about sets of real numbers, may fail constructively; this is related to the comments above about the [[fan theorem]].  But the beauty of the localic approach is that Heine--Borel necessarily holds when interpreted as a statement about opens in the locale of real numbers.  To state the theorem, we must define what it means for a collection of opens to [[cover]] the [[unit interval]].  We will give an ad-hoc definition, but this may also be derived from the general theory of [[closed sublocale]]s which allows us to interpret the unit interval as a [[compact space|compact]] locale in its own right.

+-- {: .num_defn}
###### Definition

An __[[open cover]] of the unit interval__ is a collection $\mathcal{C}$ of opens in the real line such that $\mathbb{R}$ is the join of $(-\infty,0)$, $(1,\infty)$, and the members of $\mathcal{C}$.
=--

+-- {: .num_theorem #HeineBorel}
###### Theorem
(Heine--Borel)

Every open cover of the unit interval has a finite subcover.
=--

The proof is almost embarrassingly simple.  The key point is that the construction of joins in terms of zigzags involves only finite zigzags, even for an infinitary join.

+-- {: .proof}
###### Proof

Let $J$ be the join of $(-\infty,0)$, $(1,\infty)$, and the members of $\mathcal{C}$.  Since this equals $\mathbb{R}$, then in particular $(-2,3) \subseteq J$, and since $(-1,2) \Subset (-2,3)$, we get a corresponding zigzag $\zeta$ involving finitely many zigs using finitely many of the members of $\mathcal{C}$.  Let $\mathcal{D}$ be the collection of these members of $\mathcal{C}$, and let $K$ be the join of $(-\infty,0)$, $(1,\infty)$, and $\mathcal{D}$.  Now if $(a,b)$ is any pair of rational numbers, we construct a zigzag showing directly that $(a,b) \subseteq K$ as follows: the zig $(a,0) \subseteq (-\infty,0)$, the zag $0 \gt -1$, the zigzag $\zeta$ from $-1$ to $2$, the zag $2 \gt 1$, and the zig $(1,b) \subseteq (1,\infty)$.  This is always a valid zigzag, so $K = \mathbb{R}$.  Therefore, the finite collection $\mathcal{D}$ covers the unit interval.
=--

This proof generalizes to any closed interval $[a,b]$, for $a$ any upper real and $b$ any lower real.  But note that we do not say 'extended' here; we need to find some rational number (analogous to $-1$ in the proof above) smaller than $a$ and some rational number (analogous to $2$ above) larger than $b$.  So the Heine--Borel theorem applies only to *bounded* closed intervals.

Another generalization is [[Cousin's lemma|Cousin's Theorem]]:
+-- {: .num_theorem #Cousin}
###### Theorem
**(Cousin\'s)**

Given any open cover $\mathcal{C}$ of the unit interval, there is a partition $0 = a_0 \leq a_1 \leq \cdots \leq a_n = 1$ such that each subinterval $[a_i, a_{i+}]$ is covered by a single member $U$ of $\mathcal{C}$ (in that $(-\infty,a_i) \cup U \cup (a_{i+},\infty) = \mathbb{R}$).
=--

+-- {: .proof}
###### Proof

As in the previous proof, construct a zigzag $\zeta$ from $-1$ to $2$ with zigs from $\mathcal{C}$.  Using the Zigzag Lemma \ref{zigzaglemma}, replace this with an orderly zigzag.  Let $a_0$ be $0$, let $a_1$ be the smallest left endpoint of a zig from $\zeta$ satisfying $0 \lt a_1 \lt 1$, let $a_2$ be smallest left endpoint satisfying $a_1 \lt a_2 \lt 1$, and so on until none are left, and then finish with $a_n \coloneqq 1$.
=--

A corollary of this theorem, when the open cover is given by a function $\delta\colon [0,1] \to (0,\infty)$ (so that $\mathcal{C} \coloneqq \big\{\big(x - \delta(x), x + \delta(x)\big) \;|\; x \in [0,1]\big\}$), is used (classically) to prove the uniqueness (indeed, non-vacuity) of the [[Henstock–Kurzweil integral]], which could be used to define [[Lebesgue measure]] (see below).


## A result on measure

The set of [[computable real numbers]] has [[null set|measure zero]] in the sense that, given any [[positive number]] $\epsilon$, there\'s a collection $\mathcal{I}$ of open intervals (even with rational endpoints), such that every computable real number belongs to at least one member of $\mathcal{I}$, and the sum of the lengths of any finite list of distinct members of $\mathcal{I}$ is less than $\epsilon$.  (We can do this by enumerating [[Turing machines]].)  This is a problem for a theory of [[Lebesgue measure]] in [[Russian constructivism]], where every real number is computable.

From a localic perspective, however, while $\mathcal{I}$ might cover all the *points* of the real line, it cannot cover all of the pointless parts (which need not be empty).  Indeed, we have this result ruling out such shenanigans:
+-- {: .num_prop #not-null}
###### Proposition

Given any open interval $I = (a,b)$ with rational endpoints and any collection $\mathcal{J}$ of such intervals, if $I \subseteq \bigcup \mathcal{J}$, then for any length $L \lt b - a$, there must be a [[finite subset|finite]] (in the strictest sense) subcollection $\{K_1, \ldots, K_n\}$ of $\mathcal{J}$ such that
$$ L \leq \sum_{i=1}^n \len K_i .$$
=--
In other words, any cover of $I$ by intervals must have a total length (defined as the [[supremum]] of the lengths of finite subcollections) at least the length of $I$.

+-- {: .proof}
###### Proof

Let $(c,d) \Subset (a,b)$ with $d - c \geq L$ (say with $c \coloneqq (a + b - L)/2$ and $d \coloneqq (a + b + L)/2$).  Then there is a zigzag from $c$ to $d$ with zigs from $\mathcal{J}$; by the Zigzag Lemma \ref{zigzaglemma}, we may take this zigzag to be orderly, say of length $n$.  Each zig is from one of the intervals in $\mathcal{J}$, say $K_1, \ldots, K_n$.  If these intervals are all distinct (which we can decide, since the endpoints are rational), then we\'re done, since
$$ \sum_{i=1}^n \len K_i \geq \sum_{i=1}^n (b_i - a_i) = \sum_{i=1}^{n-1} (b_i - a_i) + (b_n - a_n) \geq \sum_{i=1}^{n-1} (a_{i+} - a_i) + (b_n - a_n) = b_n - a_1 = d - c \geq L ,$$
or $ 0 \geq L $ if $n = 0$.  If they\'re not distinct, then we instead use the smallest $a_i$ and largest $b_i$ that appears in a given interval, and the argument still works (possibly even with some overlap now).
=--

This result can be strengthened to intervals without necessarily rational endpoints, by using the rational intervals that they contain, but this is not the most general statement either, and I think that what we really need to do is to develop a theory of measures of open subspaces (or perhaps even more general subspaces) and state a result about that.


## As a classifying locale

The locale of real numbers is the [[classifying locale]] of the [[geometric theory]] of [[Dedekind real numbers]]. 


## Defining functions in the locale of real numbers

There are two general ways to define functions on the locale of real numbers, via the [[rational numbers]] and via the [[Dedekind real numbers]].


### Using the rational numbers

The first approach uses existing functions already defined on the [[rational numbers]] $\mathbb{Q}$. Suppose that one has a locally uniformly continuous function $f:\mathbb{Q} \to \mathbb{Q}$. Then one could extend $f$ to a continuous map $\widetilde{f}:\mathbb{R} \to \mathbb{R}$ on the locale of real numbers. 


### Using the Dedekind real numbers

The other approach is via using existing functions defined on the [[Dedekind real numbers]] $\mathbb{R}$. In particular, given any well-defined continuous function $x \mapsto f(x)$ on the [[Dedekind real numbers]], and a [[geometric morphism]] $F:\mathrm{Set} \to \mathrm{Sh}(\mathbb{R}_D)$ from [[Set]] to the [[sheaf topos]] $\mathrm{Sh}(\mathbb{R}_D)$, if for all Dedekind real numbers $x \in \mathbb{R}_D$, $f(F^*(x)) = F^*(f(x))$, then the function $x \mapsto f(x)$ lifts to a function $x \mapsto \widetilde{f}(x)$ on the locale of real numbers. 

This allows us to first define real-valued functions normally on the set of [[Dedekind real numbers]], and then lift them up to a real-valued function on the locale of real numbers, thus allowing us to define functions such as the [[exponential function]], the [[sine]], and the [[cosine]] which can\'t be directly defined using functions on the rational numbers. 


### Arithmetic

Significantly, since the [[field]] operations on the discrete locale of [[rational numbers]] are all locally uniformly continuous on the $\mathbb{Q}$, and the field operations are well-defined and continuous on the Dedekind real numbers $\mathbb{R}_D$, the field operations in both cases lift up to a field structure on the locale of real numbers, allowing one to do basic [[arithmetic]] on $\mathbb{R}$. 


## References

* [[Simon Henry]], *Localic Metric spaces and the localic Gelfand duality*, ([arXiv:1411.0898](https://arxiv.org/abs/1411.0898))

* Guillaume Raynaud, *Fibred Contextual Quantum Physics* ([etheses:1685](https://etheses.bham.ac.uk/id/eprint/1685/), [pdf](https://etheses.bham.ac.uk//id/eprint/1685/1/Raynaud14PhD.pdf))

The locale of real numbers as the [[classifying locale]] of the [[geometric theory]] of [[two-sided Dedekind cuts]]:

* [[Ingo Blechschmidt]], section 2.2 of: *Generalized spaces for constructive algebra*, ([arXiv:2012.13850](https://arxiv.org/abs/2012.13850))

An (impredicative) construction of the locale of real numbers can be found in section 5.3 of:

* Graham Manuell, *Uniform locales and their constructive aspects*, ([arXiv:2106.00678](https://arxiv.org/abs/2106.00678))

On lifting functions from the [[Dedekind real numbers]] to the locale of real numbers, see:

* [[Madeleine Birchfield]], [[Simon Henry]], *The field structure on the locale of real numbers* (2022) &lbrack;[MO:q/434706](https://mathoverflow.net/q/434706/381)&rbrack;

* [[Valery Isaev]], [[Simon Henry]], *Localic maps given by series* ([MathOverflow](https://mathoverflow.net/q/426682/))


[[!redirects the locale of real numbers]]
[[!redirects locale of real numbers]]
[[!redirects localic real numbers]]
[[!redirects localic real number]]
[[!redirects the localic real line]]
[[!redirects localic real line]]

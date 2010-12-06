
# The locale of real numbers
* table of contents
{: toc}

## Summary

This page gives an elementary description of the [[locale]] of [[real numbers]], that is the localic [[real line]].  The development is manifestly [[constructive mathematics|constructive]] and even [[predicative mathematics|predicative]] over the [[natural numbers]] (although we are somewhat careless with the language and do not always point out when a set may predicatively be a [[proper class]]).  Ideally, we will show that our construction satisfies the seven 'headline properties' of the real line described by [Bauer & Taylor](http://www.paultaylor.eu/ASD/dedras/intro) (although so far we cover only the Heine--Borel theorem).

The exposition here is pretty much [[Toby Bartels|my]] own work, although of course the basic ideas are well known to many.  In particular, the technical zigzag lemma is mine (but it is not a very deep result!).


## Idea
{#idea}

To describe the local of the real numbers, we need first of all to describe what an open in the real line is.  The key insight is that an open set is determined by the open intervals of [[rational numbers]] that it contains.  This is analogous to the key insight of [[Richard Dedekind]]\'s definition of [[real number]]: that a point in the real line is determined by which open intervals of rational numbers that it belongs to.  (Once you\'re talking about rational numbers, things are manageable.)


## Opens

An __open__ in the real line is a [[binary relation]] ${\sim}$ on the [[rational numbers]] that satisfies the three properties listed below.  Intuitively, we have $a \sim b$ iff the open [[interval]] $(a,b)$ is contained in the corresponding [[open subspace|open set]].

1. If $a \geq b$, then $a \sim b$.
2. If $a \geq b \sim c \geq d$, then $a \sim d$.
3. If $a \sim b \gt c \sim d$, then $a \sim d$.
4. If $b \sim c$ whenever $a \lt b$ and $c \lt d$, then $a \sim d$.

Property (1) is motivated because $(a,b)$ is [[empty subset|empty]] whenever $a \geq b$.  Property (2) is motivated because $(a,d) \subseteq (b,c)$ whenever $a \geq b$ and $c \geq d$.  Property (4) is somewhat technical; it keeps $\{(a,b) \;|\; a \lt b \;\Rightarrow\; 0 \lt a \lt b \lt 1\}$ from being an open, while $\{(a,b) \;|\; a \lt b \Rightarrow 0 \leq a \lt b \leq 1}$ is allowed.

The really interesting property is property (3).  It in fact generalises as follows:

* If
  \[ \label{zigzag}
     a_1 \sim b_1 \gt a_2 \sim b_2 \gt \cdots \gt a_n \sim b_n
  , \]
  then $a_1 \sim b_n$.

We call the combined hypothesis of this property a __zigzag__; each hypothesis $a_i \sim b_i$ is a __zig__, and each hypothesis $b_i \gt a_{i^+}$ is a __zag__.  To indicate the length of a zigzag, we will count the zigs; the zigzag (eq:zigzag) has $n$ zigs (and $n - 1$ zags).  A typical nondegenerate zigzag with $3$ zigs is shown below; it consists of $3$ overlapping open intervals, each of which belongs to a given open set; we are motivated to conclude that the entire interval from $a_1$ to $b_3$ belongs to that open set.

+-- {: style="text-align:center"}
[[!include zigzag of real numbers - SVG]]
=--

Thus the zigzag property for $n = 2$ is property (3), the zigzag property for $n = 1$ is trivial (if $a \sim b$, then $a \sim b$), and the zigzag property for $n \gt 2$ may be proved by [[induction]].  (There is also a sense in which the zigzag property for $n = 0$ is property (1), but I haven\'t quite got my head around that.)

If $G$ is an open in the real line, then we write $(a,b) \subseteq G$ to mean that $a$ is related to $b$ through $G$ and say that $G$ __contains__ the interval from $a$ to $b$.


## The zigzag lemma

We will often have occasion to consider a zigzag as in (eq:zigzag), but where the various zigs are taken relative to different opens.  Nevertheless, we will usually want to say something about the relationship of $a_1$ to $b_n$, and it will often be convenient to assume, for all $i$, that $a_1 \leq a_i$ and $b_i \leq b_n$.  We may do so without loss of generality as follows: consider the smallest value of $i$ such that $b_i \geq b_n$, truncate the zigzag so that it now has only $i$ zigs, and change the new endpoint $b_i$ to the old endpoint $b_n$.  The final zig $(a_i,b_i) \subseteq G_i$ becomes $(a_i,b_n) \subseteq G_i$, which will hold by property (2) since $b_i \geq b_n$.  Now consider the largest value of $j \leq i$ such that $a_1 \geq a_j$, and truncate similarly on the other side.  We now have a zigzag with $i - j + 1$ zigs that never falls below $a_1$ on a zag nor rises above $b_n$ on a zig.

To be precise:
+-- {: .un_lemma}
###### Zigzag lemma

Given a collection $\mathcal{C}$ of opens and a zigzag in which each zig holds relative to some open in $\mathcal{C}$, there exists a zigzag (eq:zigzag) in which each zig holds relative to some open in $\mathcal{C}$, $a_1 \leq a_i$ for each $i$, and $b_i \leq b_n$ for each $i$.

(Since each $b_i \gt a_{i^+}$, it follows further that $a_i \lt b_n$ for each $i \gt 1$ and $a_1 \lt b_i$ for each $i \lt n$, although this corollary doesn\'t seem to be particularly useful.)
=--

At the moment, this lemma is used only in the proof of the infinite distributivity law.


## The frame of opens

The opens form a [[subobject|sub]]-[[poset]] of the [[power set]] $\mathcal{P}(\mathbb{Q} \times \mathbb{Q})$.  This poset is in fact a [[frame]], as we will now show.  (It is *not* a subframe of the power set, since the [[joins]] are different.  It *is* a sub-[[inflattice]] of the power set, although this seems to be a red herring at least for infinitary [[meets]], since those are not part of the frame structure that we need.)

The [[top element|top]] open, denoted $\mathbb{R}$, is the binary relation which is always true.  Given two opens $G$ and $H$, their [[meet]] in the poset of opens, denoted $G \cap H$, is simply their [[logical conjunction|conjunction]], that is their [[intersection]] as [[subsets]] of $\mathbb{Q} \times \mathbb{Q}$.  (In fact, given any collection of opens, their meet is their conjunction.)  It is straightforward to check that $\mathbb{R}$ and $G \cap H$ are opens and to prove that these are the desired meets.  Intuitively, this all works because an open interval will be contained in the intersection of a family of open sets if and only if it is contained in each individual open set.

The [[bottom element|bottom]] open, denoted $\empty$, is the binary relation $\geq$.  That is, $(a,b) \subseteq \empty$ iff $a \geq b$.  It is easy to check that this is an open; it precedes every open by property (1).  Intuitively, this corresponds to the [[empty subset]] of the real line; $(a,b)$ is empty if and only if $a \geq b$.  However, note that $\empty$ is *not* the empty subset of $\mathbb{Q} \times \mathbb{Q}$; the notation follows our topological intuition rather than the [[relation theory|algebra of relations]].

Given two opens $G$ and $H$, their [[join]] in the poset of opens, denoted $G \cup H$, is defined as follows:  $(a,b) \subseteq G \cup H$ if and only if there exists a zigzag (eq:zigzag) with $a = a_1$ and $b = b_n$ in which each zig is of the form $(a_i,b_i) \subseteq G$ or $(a_i,b_i) \subseteq H$.  It is immediate that this is an open in which $G$ and $H$ are both contained.  Conversely, any open in which $G$ and $H$ are contained must contain this open $G \cup H$, by property (3).

More generally, given any family $(G_k)_k$ of opens, their [[join]] in the poset of opens, denoted $\bigcup_k G_k$, is defined as follows:  $(a,b) \subseteq \bigcup_k G_k$ if and only if $a \geq b$ or there exists a zigzag (eq:zigzag) with $a = a_1$ and $b = b_n$ in which each zig is of the form $(a_i,b_i) \subseteq G_k$ for some $k$.  (We can leave out the $a \geq b$ clause if the family is [[inhabited set|inhabited]].)  The same argument applies as before.  Note that each individual zigzag has finitely many zigs, and therefore involves finitely many of the opens $G_k$, even when taking the join of an infinite family.

Finally, we must check the distributive law $G \cap \bigcup_k H_k \subseteq \bigcup_k (G \cap H_k)$.  That is, if $a \sim b$ directly through $G$ and $a \sim b$ through a zigzag of $H$s (or $a \geq b$), then we need that $a \sim b$ through a zigzag in which each zig is related both through $G$ and through some $H$ (or $a \geq b$).  To prove this (ignoring the trivial case where $a \geq b$), start with the zigzag of $H$s, and apply the zigzag lemma to get a zigzag of $H$s in which each zig involves values bounded by $a$ and $b$.  Then these zigs hold for $G$ as well, by property (2).  Therefore, we may interpret each zig using $G \cap H_k$ for some $k$, proving the desired result.

This frame of opens, interpreted as a [[locale]], is __the locale of real numbers__.  As usual, we denote this locale with the same symbol as the top element of its frame, in this case $\mathbb{R}$.  (Of course, the true etymology of the symbols runs in the other order.)


## Open intervals as opens

Given rational numbers $a$ and $b$, the open interval $(a,b)$ may itself be interpreted as an open in the real line, also denoted $(a,b)$, as follows: let $(c,d) \subseteq (a,b)$ hold if every rational number strictly between $c$ and $d$ (in that order) is also strictly between $a$ and $b$ (in that order).  In other words, we interpret '${\subseteq}$' literally as comparing subsets of $\mathbb{Q}$.  It is straightforward to check that this condition does indeed define an open.  There is now a third way to interpret '$(c,d) \subseteq (a,b)$'; interpreting both intervals as opens in the real line, this states that the first is contained in the second.  But again, it is easy to check that this is equivalent; $(c,d) \subseteq (a,b)$ (in the set-theoretic sense) if and only if $(e,f) \subseteq (a,b)$ whenever $(e,f) \subseteq (c,d)$.  Notice that $(a,b) = \empty$ whenever $a \geq b$.

We can actually generalise this somewhat.  Given any set $L$ of rational numbers and any set $U$ of rational numbers, we may define the open $(\inf U, \sup L)$ as follows: let $(a,b) \subseteq (\inf U, \sup L)$ hold if every rational number strictly between $a$ and $b$ (in that order) is greater than some element of $U$ and less than some element of $L$.  If the [[infimum]] of $U$ and the [[supremum]] of $L$ exist in the usual sense as rational numbers, then this agrees with the previous paragraph.  If instead $U$ or $L$ is the set of all rational numbers, then we write $-\infty$ for $\inf U$ or $\infty$ for $\sup L$.  In general, we may interpret $\inf U$ as an [[extended real number|extended]] [[upper real number|upper real]] and $\sup L$ as an extended [[lower real number|lower real]].  Classically, every extended upper or lower real is either a real number, $-\infty$, or $\infty$; only the converse holds constructively.  Notice that $(-\infty,\infty) = \mathbb{R}$.

Since we will refer to them below, we will state for the record the complete definitions of $(-\infty,a)$ and $(a,\infty)$ for a rational number $a$.  We have $(b,c) \subseteq (-\infty,a)$ iff every rational number strictly between $b$ and $c$ is less than $a$, that is iff $b \geq c$ or $c \leq a$.  Similarly, we have $(b,c) \subseteq (a,\infty)$ iff every rational number strictly between $b$ and $c$ is greater than $a$, that is iff $b \geq c$ or $b \geq a$.  A fortiori, $(b,c) \subseteq (-\infty,0)$ if $c = 0$, and $(b,c) \subseteq (1, \infty)$ if $b = 1$.


## Open sets, closed sets, and points

We think of each open as defining an [[open subspace|open subset]] of the real line, but we can equally well think of it as defining a [[closed subspace|closed subset]].  The difference between these perspectives is reflected in [[complement]]ary criteria for when a real number belongs to the set.  So to make sense of this, we must identify the [[point|points]] of the real line.

Recall that a [[real number]] may be defined as a pair $(L,U)$ of [[inhabited set|inhabited]] [[subsets]] of $\mathbb{Q}$ satisfying the following properties:

1. If $a \in L$, then $a \lt b$ for some $b \in L$.
2. If $b \in U$, then $a \lt b$ for some $a \in U$.
3. If $a \in L$ and $b \in U$, then $a \lt b$.
4. If $a \lt b$, then $a \in L$ or $b \in U$.

We define a __point__ of the real line to be a real number in this sense.  Given such a point $x = (L,U)$ and a rational number $a$, we write $a \lt x$ to mean that $a \in L$ and $a \gt x$ to mean that $a \in U$.  If we wish to refer to $L$ and $U$ directly, we may call $L$ the __lower set__ of $x$ and $U$ the __upper set__.

Given a point $x$ and an open $G$, we say that $x$ __belongs__ to $G$, written $x \in G$, if $(a,b) \subseteq G$ for some $a \lt x$ and $b \gt x$; that is, $G$ contains an interval from some element of the lower set to some element of the upper set of $x$.  We have $x \in \mathbb{R}$ since its lower and upper sets are inhabited.  If $x \in G$ and $x \in H$, with $(a,b) \subseteq G$ and $(c,d) \subseteq H$, then $\big(\max(a,c), \min(b,d)\big) \subseteq G \cap H$, so $x \in G \cap H$; note that this argument fails for infinitary intersections.  (The converse, that $x \in G$ and $x \in H$ if $x \in G \cap H$, is immediate.)  Dually, suppose that $x \in \bigcup_k G_k$, as shown by some zigzag (since $a \geq b$ is impossible when $a \lt x$ and $b \gt x$, by 3).  Applying condition (4) of the definition of real number to each zag, we have $a_{i^+} \lt x$ or $b_i \gt x$, for each $i \lt n$.  Checking all $2^{n-1}$ possibilities, and knowing that $a_1 \lt x$ and $b_n \gt x$ in any case, we must have $a_i \lt x$ and $b_i \gt x$ for some $i$.  Then we have $x \in G_k$ for some $k$, whichever corresponds to the $i$th zig.  (The converse, that $x \in \bigcup_k G_k$ if $x \in G_k$ for some $k$, is immediate.)

Therefore, each point defines a [[completely prime filter]] on the frame of all opens, which is the definition of a [[point of a locale|point]] in general locale theory.  Conversely, given such a completely prime filter $P$, let $L$ be the set of all rational numbers $a$ such that the open interval $(a, \infty)$ (when interpreted as an open in the real line as defined above) is in $P$, and symmetrically let $U$ be the set of all $a$ such that $(-\infty, a) \in P$.

Given a point $x$ and an open $G$, we say that $x$ __co-belongs__ to $G$, written $x \notin G$, if we never have $a \lt x$, $b \gt x$, and $(a,b) \subseteq G$, which is precisely the [[negation]] of the property that $x \in G$.  We think of this condition as defining a *[[closed subspace|closed]]* set to which $x$ *does* belong.  Notice that $x \notin \bigcup_k G_k$ if and only if $x \notin G_k$ for each $k$, giving the desired behaviour for an arbitrary intersection of closed sets (which corresponds to union of open sets under [[de Morgan duality]]).  We also have that $x \notin \mathbb{R}$ always fails, and $x \notin G \cap H$ if $x \notin G$ or $x \notin H$.  To prove that $x \notin G$ or $x \notin H$ whenever $x \notin G \cap H$, however, we must use [[excluded middle]]; constructively, closed sets don\'t behave well under union.

A related question is whether we can reconstruct $G$ from the set of points which belong to it.  This should be equivalent to the [[fan theorem]], which is classically true and also accepted by [[Jan Brouwer|Brouwer]]\'s school of intuitionism, but refuted in the Russian school in which all real numbers are assumed to be [[computable number|computable]].  (I should check this.)  Arguably, the real lesson of these logical technicalities is that we should remember that opens, not points, are the fundamental concept in a locale.


## The Heine--Borel theorem

The classical [[Heine-Borel theorem|Heine–Borel theorem]], as a statement about sets of real numbers, may fail constructively; this is related to the comments above about the [[fan theorem]].  But the beauty of the localic approach is that Heine--Borel necessarily holds when interpreted as a statement about opens in the locale of real numbers.  To state the theorem, we must define what it means for a collection of opens to [[cover]] the [[unit interval]].  We will give an ad-hoc definition, but this may also be derived from the general theory of [[closed sublocale]]s which allows us to interpret the unit interval as a [[compact space|compact]] locale in its own right.

+-- {: .un_defn}
###### Definition

An __[[open cover]] of the unit interval__ is a collection $\mathcal{C}$ of opens in the real line such that $\mathbb{R}$ is the join of $(-\infty,0)$, $(1,\infty)$, and the elements of $\mathcal{C}$.
=--

+-- {: .un_theorem}
###### Theorem
(Heine--Borel)

Every open cover of the unit interval has a finite subcover.
=--

+-- {: .proof}
###### Proof

The proof is almost embarrassingly simple.  The key point is that the construction of joins in terms of zigzags involves only finite zigzags, even for an infinitary join.

Let $J$ be the join of $(-\infty,0)$, $(1,\infty)$, and the elements of $\mathcal{C}$.  If this equals $\mathbb{R}$, then in particular $(-1,2) \subseteq J$, a fact which is given by some zigzag $\zeta$.  This zigzag involves only finitely many of the elements of $\mathcal{C}$; let $\mathcal{D}$ be the collection of these, and let $K$ be the join of $(-\infty,0)$, $(1,\infty)$, and $\mathcal{D}$.  Now if $(a,b)$ is any pair of rational numbers, we construct a zigzag showing that $(a,b) \subseteq K$ as follows: the zig $(a,0) \subseteq (-\infty,0)$, the zag $0 \gt -1$, the zigzag $\zeta$ from $-1$ to $2$, the zag $2 \gt 1$, and the zig $(1,b) \subseteq (1,\infty)$.  This is always a valid zigzag, so $K = \mathbb{R}$.  Therefore, the finite collection $\mathcal{D}$ covers the unit interval.
=--

This proof generalises immediately to any closed interval $[a,b]$, for $a$ any upper real and $b$ any lower real.  But note that we do not say 'extended' here; we need to find some rational number (analogous to $-1$ in the proof above) smaller than $a$ and some rational number (analogous to $2$ above) larger than $b$.  So the Heine--Borel theorem applies only to *bounded* closed intervals.


[[!redirects the locale of real numbers]]
[[!redirects locale of real numbers]]
[[!redirects localic real numbers]]
[[!redirects localic real number]]
[[!redirects the localic real line]]
[[!redirects localic real line]]

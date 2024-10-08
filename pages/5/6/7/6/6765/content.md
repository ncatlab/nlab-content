
# Cheng spaces
* table of contents
{: toc}

## Idea

A Cheng space is a version of a [[measurable space]] developed by [[Henry Cheng]] for [[constructive mathematics]].  Even in [[classical mathematics]], however, Cheng spaces are more general than standard measure spaces.  On the other hand, if we equip a measurable space with a $\sigma$-[[sigma-ideal|ideal]] of [[null subsets]] (or a $\delta$-filter of [[full subsets]]), there is no essential difference classically.

Some of the [[abstract nonsense]] below is original research (by [[Toby Bartels]] and [[Todd Trimble]]), but based heavily on Cheng\'s work as described in [Bishop & Bridges](#BishopBridges).


## Motivation

From a [[constructive mathematics|constructive]] perspective, there are a couple of related problems with the classical theory of measurable spaces.  One is that the notion of $\sigma$-[[sigma-algebra|algebra]] is highly suspicious, because it relies on an operation, [[complement]]ation, that behaves very differently in [[intuitionistic logic]].  The other is that, even you accept the definition of $\sigma$-algebra (after all, the Lebesgue-measurable sets on the real line do still form one), there may be very few measurable functions.  (It is possible in constructive mathematics that every function from the [[real line]] to itself, regardless of measurability, is [[continuous function|continuous]].)

Indeed, if we set aside the general theory of measurable spaces and simply do Lebesgue measure ad hoc in a constructive (even predicative) way, we find that instead of measurable [[functions]] we really want measurable [[partial functions]] whose domain of definition is a [[full subset]], the [[almost functions]].  This suggests that if we want to define the concept of measurable function, then we have to know what the full sets are, so we need a measurable space equipped with such a notion.  But since this is usually defined relative to a measure, well *after* the structure of the measurable space has been given, we are at an impasse.

There is a way out, due to [[Henry Cheng]], for both of these problems at once.  Instead of dealing with individual subsets, we will deal with pairs of [[disjoint subsets]].  The intuition is that we use disjoint pairs $(A,B)$ such that $A \cup B$ is full ---with $(A,\neg{A})$ being the motivating example in the classical theory---, but we let the Cheng measurability structure itself tell us which pairs those are.  Once we fix a particular measure, we may find additional pairs whose union is full, somewhat like finding additional measurable sets when taking the completion in the classical theory (although taking the completion is a separate phenomenon here), but that\'s all right; the important thing is that each pair chosen really is full in any measure used (much as each set in a classical $\sigma$-algebra must actually be measurable by any measure used).


## Definitions

Let $X$ be a [[set]].  We'll define the structure of a Cheng space on $X$ in several steps.

### The Boolean semi-algebra of disjoint pairs

A __[[disjoint subsets|disjoint pair]]__ in $X$ is a pair $(A,B)$ of [[subsets]] of $X$ such that the [[intersection]] $A \cap B$ is [[empty subset|empty]].  Every set $A$ defines a disjoint pair $[A] = (A,\neg{A})$, but many disjoint pairs are not of this form; the extreme counterexample (unless $X$ is empty) is $(\empty,\empty)$.  We order disjoint pairs by the usual order on the first component and the opposite on the second:
$$ (A,B) \subseteq (C,D) \;\Leftrightarrow\; A \subseteq C \;\wedge\; B \supseteq D .$$
Similarly, we make the usual operations on sets into operations on disjoint pairs by applying formal [[de Morgan duality]] to the second component:

*  $ \empty = [\empty] = (\empty, X) $;
*  $ X = [X] = (X, \empty) $;
*  $ (A,B) \cup (C,D) = (A \cup C, B \cap D) $;
*  $ (A,B) \cap (C,D) = (A \cap C, B \cup D) $;
*  $ \bigcup_i (A_i,B_i) = (\bigcup_i A_i, \bigcap_i B_i) $;
*  $ \bigcap_i (A_i,B_i) = (\bigcap_i A_i, \bigcup_i B_i) $.

(Note that we do not write $[A]$ as $A$ except when $A$ is given as $\empty$ or $X$, because for example, $[A \cap B] = [A] \cap [B]$, while classically valid, may fail constructively.)

These operations form the disjoint pairs into a [[lattice]]; in fact, it is both a [[complete lattice]] and a [[distributive lattice]], but it is not constructively completely distributive in either direction.  (Compare the fact that a [[power set]] is, constructively, completely distributive only in one direction, making it a [[frame]]; here the directions are mixed by the formal duality and so neither works.  On the other hand, that the power set is a frame is used to show that the infinitary operations do define disjoint pairs.)

Finally, we define the [[complement]] of $(A,B)$, not using the complements of $A$ and $B$ (which usually are not even disjoint) but instead simply by reversing them:
$$ \neg(A,B) = (B,A) .$$
Then an actual [[de Morgan duality]] holds for these operations:

*  $ \neg\bigcup_i (A_i,B_i) = \bigcap_i \neg(A_i,B_i) $;
*  $ \neg\bigcap_i (A_i,B_i) = \bigcup_i \neg(A_i,B_i) $;
*  $ \neg\neg(A,B) = (A,B) $, the famous [[double negation]] law.

We can go on to define the relative complement $(A,B) \setminus (C,D)$ and symmetric difference $(A,B) \uplus (C,D)$ in terms of complements, intersections, and unions as usual, and they obey many of the usual classical laws.  (For instance, $\uplus$ is ---through a fairly lengthy calculation--- associative, which is not constructively true of [[symmetric difference]] on a power set.)

At this point, the reader could be forgiven for thinking that we have cleverly pulled a [[Boolean algebra]] out of a mere [[Heyting algebra]], but this is not true; aside from the give-away that this lattice is not constructively completely distributive, it is not even classically a Boolean algebra.  This is because $(A,B) \cup \neg(A,B) = (A \cup B, \empty)$ (and similarly for intersection) and there is no requirement that $A \cup B = X$.  What we have instead is a complete Boolean [[rig]], aka semi-ring with unit; to keep consistent with the usual terminology of measure theory, I\'ll call such a thing a __Boolean semi-algebra__.

This is all a special case of the [[Chu construction]]; the poset of disjoint pairs in $X$ is $Chu_{TV}(P X, \empty)$, where $TV$ is the [[enriched category|enriching]] category of [[truth values]].


### The $\sigma$-semi-algebra of complemented pairs

Given a set $X$, a __$\sigma$-semi-algebra__ on $X$ is a collection $\mathcal{M}$ of disjoint pairs in $X$, called __complemented pairs__, such that:
1.  $[\empty] = (\empty,X)$ is a complemented pair;
2.  If $(A,B)$ is a complemented pair, then so is its complement $(B,A)$;
3.  If $(A_1,B_1), (A_2,B_2), (A_3,B_3), \ldots$ are complemented pairs, then so is their union $(\bigcup_i A_i, \bigcap_i B_i)$.

The arguments above that $\mathcal{M}$ is closed under countable intersections, relative complements, and symmetric differences goes through.  (We can also define analogous notions of semi-algebra, $\delta$-semi-ring, and other variations of $\sigma$-[[sigma-algebra|algebra]].)

Finally, a __Cheng measurable space__ or simply a __Cheng space__ is a set equipped with a $\sigma$-semi-algebra.

(Incidentally, the reason why we do not use the term 'measurable pair' is that $A$ and $B$ may easily both be measurable in some sense yet without having $(A,B)$ as a complemented pair.  In particular, $(\empty,\empty)$ is rarely a complemented pair ---although that is not forbidden either---, yet it is hard to call it non-measurable.)


### Measurable sets and functions

A [[subset]] $A$ of a Cheng space $X$ is __[[measurable subset|measurable]]__ if there is some complemented pair $(A,B)$.  A subset $S$ is __[[full subset|full]]__ if, for some complemented pair $(A,B)$, $S$ contains the [[union]] $A \cup B$.  Conversely, $S$ is __[[null subset|null]]__ if, for some such $(A,B)$, $S$ is disjoint from $A \cup B$.

Given two Cheng measurable spaces $X$ and $Y$, an __[[almost function]]__ from $X$ to $Y$ is a [[partial function]] from $X$ to $Y$ such that the [[domain]] of $f$ is full.  An almost function is __[[measurable function|measurable]]__ if, given any complemented pair $(C,D)$ in $Y$, there is a complemented pair $(A,B)$ such that $\{p\colon X \;|\; p \in A \iff f(p) \in C\}$ and $\{p\colon X \;|\; p \in B \iff f(p) \in D)$ are both full.

Two (measurable) functions are __[[almost equal]]__ if their [[equaliser]] is full.

Cheng spaces, measurable almost functions between them, and almost equality between them form a [[category]] $Cheng Sp$.


## Completion

A Cheng space is __[[complete measure space|complete]]__ if, whenever $(A,B)$ is a complemented pair and $A \Leftrightarrow C$ and $B \Leftrightarrow D$ are full, then $(C,D)$ is a complemented pair.  In particular, every full set and every null set is measurable.

Given any Cheng space $(X,\mathcal{M})$, its __completion__ $(X,\bar{\mathcal{M}})$ has the same [[underlying set]] $X$ but a disjoint pair $(C,D)$ is $\bar{\mathcal{M}}$-complemented iff, for some $\mathcal{M}$-complemented pair $(A,B)$, both $A \Leftrightarrow C$ and $B \Leftrightarrow D$ are $\mathcal{M}$-full.

A Cheng space is complete iff it is its own completion; the completion of any Cheng space is complete.  The [[identity function]] on $X$ is measurable in either direction between $(X,\mathcal{M})$ and $(X,\bar{\mathcal{M}})$, so they are [[isomorphic]] in $Cheng Sp$.  Accordingly, the [[full subcategory]] of $Cheng Sp$ on the complete spaces is [[equivalence of categories|equivalent]] to $Cheng Sp$ itself (via its [[inclusion functor]]).

When restricted to complete spaces, the definition of measurable function is simpler: any partial function under which the [[preimage]] of any complemented pair is complemented.


## Measures on Cheng spaces

We will define the notion of a [[positive measure]] on a Cheng space; it's straightforward to generalise to other sorts of measures as described at [[measure]].

Given a Cheng space $(X,\mathcal{M})$, a __positive measure__ on $(X,\mathcal{M})$ is a [[function]] $\mu$ from $\mathcal{M}$ to $[0,\infty]$ such that:

*  [[absolutely continuous measure|absolute continuity]]: $\mu(A,B) = 0$ if $B$ is full;
*  [[inclusion-exclusion]]: $\mu(A \cap C, B \cup D) + \mu(A \cup C, B \cap D) = \mu(A,B) + \mu(C,D)$;
*  [[subadditive function|subadditivity]]: $\mu(\bigcup_i A_i, \bigcap_i B_i) \leq \sum_i \mu(A_i,B_i)$ for an [[infinite sequence]] of complemented pairs.

We think of $\mu(A,B)$ as the measure of $A$; thanks to absolute continuity, either $A$ or $B$ alone is enough to determine $\mu(A,B)$.

## References

* {#BishopBridges} [[Errett Bishop]], [[Douglas Bridges]]: *[[Constructive Analysis]]*, Grundlehren der mathematischen Wissenschaften **279**, Springer (1985) &lbrack;[doi:10.1007/978-3-642-61667-9](https://doi.org/10.1007/978-3-642-61667-9)&rbrack;

* {#BishopCheng} [[Errett Bishop]], [[Henry Cheng]]. *Constructive Measure Theory*, American Mathematical Society (1972). &lbrack;ISBN:978-0821818169&rbrack;

[[!redirects Cheng space]]
[[!redirects Cheng spaces]]
[[!redirects Cheng measurable space]]
[[!redirects Cheng measurable spaces]]

[[!redirects boolean semialgebra]]
[[!redirects boolean semialgebras]]
[[!redirects boolean semi-algebra]]
[[!redirects boolean semi-algebras]]
[[!redirects Boolean semialgebra]]
[[!redirects Boolean semialgebras]]
[[!redirects Boolean semi-algebra]]
[[!redirects Boolean semi-algebras]]

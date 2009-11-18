# Measurable spaces #
* tic
{: toc}


##Idea##

Measurable spaces are a necessary prelude to the general theory of measure and [[integration]].  Basically, a measure is a recipe for computing the size --- e.g. length, area, volume --- of subsets of a given set $X$.  The structure of a 'measurable space' picks out those subsets of $X$ for which the size is well-defined.   These subsets are called 'measurable'.   A 'measure' on $X$ is then a recipe that assigns a number to each measurable subset saying how big it is.  

In short: you get a [[measure space]] by placing a measure on a measurable space.

Ideally, all subsets would be measurable, but this contradicts the [[axiom of choice]] for the basic example of [[Lebesgue measure]] on the [[real line]].  Although it is possible to use nonstandard [[foundations]] of mathematics in which all subsets of the real line are Lebesgue measurable, any general theory that includes that example and is more general than those foundations requires some notion of measurable space.

In any case, measurable spaces are of some interest in their own right, even without a measure on them.


## Definitions ##

We assume the law of [[excluded middle]] throughout; see below for the constructive theory.


### Short version ###

Given a [[set]] $X$, a __$\sigma$-algebra__ is a collection of subsets of $X$ that is closed under [[complement|complementation]], [[countable set|countable]] [[unions]], and countable [[intersections]].  A __measurable space__, by the usual modern defintion, is a set $X$ equipped with a $\sigma$-algebra $\Sigma$.  The elements of $\Sigma$ are called the __measurable subsets__ of $X$ (or more properly, the measurable sets of $(X,\Sigma)$).

Notice that the [[power set]] $P X$ of $X$ is a [[Boolean algebra]] under the operations of [[finite set|finitary]] union, intersection, and complementation.  Actually, it is a [[complete lattice|complete]] Boolean algebra, since we can also take arbitrary unions and intersections.  A $\sigma$-algebra is an intermediate notion, since (in addition to being closed under complementation) we only require that it be closed under *countable* unions and intersections.


### Long version ###

Given a [[set]] $X$ and a collection $\Sigma$ of [[subset]]s $S \subseteq X$, we will always use the term 'measurable' to describe an element of $\Sigma$.  There are really several kinds of collections that $\Sigma$ could be:

*  A __ring__ on $X$ is a collection $\Sigma$ which is closed under [[finite set|finitary]] [[union]] and under [[relative complement]]ation.  That is:

   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ and $T$ are measurable, then so is their union $S \cup T$.
   1.  If $S$ and $T$ are measurable, then so is their relative complement $T \setminus S$.

   It follows that $\Sigma$ is closed under [[inhabited set|inhabited]] finitary intersection and under finitary [[symmetric difference]]:
   *  If $S$ and $T$ are measurable, then so is their intersection $S \cap T = T \setminus (T \setminus S)$.
   *  If $S$ and $T$ are measurable, then so is their symmetric difference $S \uplus T = (T \setminus S) \cup (S \setminus T)$.

   We can actually use the latter as an alternative to (2), since $S \cup T = (S \uplus T) \uplus (S \cap T)$.  Or we can use the pair as an alternative to (2,3), since $T \setminus S = (S \cap T) \uplus T$.  For that matter, we can weaken (1) to simply say that *some* set $S$ is measurable; then $\empty = S \setminus S$.

   While the nullary union and nullary symmetric difference (both the empty set) belong to $\Sigma$, the nullary intersection (which is $S$ itself) might not.  The term 'ring' dates from the days when a [[ring]] in algebra was not assumed to be unital; so a ring on $X$ is simply a subring (in this sense) of the [[Boolean ring]] $P X$.


*  A __$\delta$-ring__ on $X$ is a ring $\Sigma$ which is closed under countable infinitary intersection.  That is:
   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ and $T$ are measurable, then so is their union $S \cup T$.
   1.  If $S$ and $T$ are measurable, then so is their relative complement $T \setminus S$.
   1.  If $S_1, S_2, S_3, \ldots$ are measurable, then so is their intersection $\bigcap_i S_i$.

   Of course, every $\delta$-ring is a ring, but not conversely.  Actually, if you want to define the concept of $\delta$-ring directly, it\'s quicker if you use the symmetric difference; then (2,3) follow by the reasoning above and the [[idempotent|idempotence]] of intersection (so that $S \cap T = S \cap T \cap T \cap T \cap \cdots$).

   The symbol '$\delta$' here is from German 'Durchschnitt', meaning intersection; it may be used in many contexts to refer to countable intersections.


*  A __$\sigma$-ring__ on $X$ is a ring $\Sigma$ which is closed under countable infintary union.  That is:
   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ and $T$ are measurable, then so is their union $S \cup T$.
   1.  If $S$ and $T$ are measurable, then so is their relative complement $T \setminus S$.
   1.  If $S_1, S_2, S_3, \ldots$ are measurable, then so is their union $\bigcup_i S_i$.

   Now (2) is simply redundant; $S \cup T = S \cup T \cup T \cup T \cup \cdots$.  A $\sigma$-ring is obviously a ring, but in fact it is also a $\delta$-ring; $\bigcap_i S_i = \bigcup_i S_i \setminus \bigcup_j (\bigcup_i S_i \setminus S_j)$.

   The symbol '$\sigma$' here is from German 'Summe', meaning union; it may be used in many contexts to refer to countable unions.


*  An __algebra__ or __field__ on $X$ is a ring $\Sigma$ to which $X$ itself belongs.  That is:
   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ and $T$ are measurable, then so is their union $S \cup T$.
   1.  If $S$ and $T$ are measurable, then so is their relative complement $T \setminus S$.
   1.  $X$ is measurable.

   Actually, (2) is now redundant again; $S \cup T = X \setminus ((X \setminus T) \setminus S)$.  But perhaps more importantly, $\Sigma$ is closed under *absolute* complementation (that is, complementation relative to the entire ambient set $X$); that is:

   *  If $S$ is measurable, then so is its complement $\neg{S}$.

   In light of this, the most common definition of algebra is probably to use this fact together with (1,2); then (3) follows because $T \setminus S = \neg(S \cup \neg{T})$ and (4) follows because $X = \neg\empty$.  On the other hand, one could equally well use intersection instead of union; absolute complements allow the full use of [[de Morgan duality]].

   Warning: the term 'field' here is even more archaic that the term 'ring' above; indeed the only field in this sense which is a [[field]] (in the usual sense) under symmetric difference and intersection is the field $\{\empty, X\}$ for an [[inhabited set]] $X$.


*  Finally, a __$\sigma$-algebra__ or __$\sigma$-field__ on $X$ is a ring $\Sigma$ that is both an algebra and a $\sigma$-ring.  That is:
   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ and $T$ are measurable, then so is their union $S \cup T$.
   1.  If $S$ and $T$ are measurable, then so is their relative complement $T \setminus S$.
   1.  $X$ is measurable.
   1.  If $S_1, S_2, S_3, \ldots$ are measurable, then so is their union $\bigcup_i S_i$.

   As with $\sigma$-rings, (2) is redundant; as with algebras, it\'s probably most common to use the absolute complement in place of (3,4).  Thus the usual definition of a $\sigma$-algebra states:
   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ is measurable, then so is its complement $\neg{S}$.
   1.  If $S_1, S_2, S_3, \ldots$ are measurable, then so is their union $\bigcup_i S_i$.

   And again we could again just as easily use intersection as union, even in the infinite case.  That is, a $\delta$-algebra is automatically a $\sigma$-algebra, because $\bigcup_i S_i = \neg\bigcap_i \neg{S_i}$.


Any and all of the above notions have been used by various authors in the definition of measurable space; for example, Kolmogorov used algebras (at least at first), and Halmos used $\sigma$-rings.  Of course, the finitary notions (ring and algebra) aren\'t strong enough to describe the interesting features of Lebesgue measure; they are usually used to study very different examples (finitely additive measures).  On the other hand, ($\delta$&#8209; or $\sigma$&#8209;) rings may be more convenient than ($\sigma$)-algebras for some purposes; for example, vector-valued measures on $\delta$-rings make good sense even when the absolute measure of the whole space is infinite.

Note that the collection of measurable sets with finite measure (in a given [[measure space]]) is a ($\delta$)-ring, while the collection of measurable sets with $\sigma$-finite measure is a $\sigma$-ring.


### Measurable sets and functions

A __measurable set__, as before, is simply any set that belongs to $\Sigma$.  If $\Sigma$ is one of the weaker notions (not necessarily a $\sigma$-algebra), then we also want some subsidiary notions: $S$ is __relatively measurable__ if $S \cap T$ is measurable whenever $T$ is, and $S$ is __$\sigma$-measurable__ if it is a countable union of measurable sets.  Notice that every relatively measurable set is measurable iff $S$ is at least an algebra; in any case, the relatively measurable sets form a ($\sigma$)-algebra if $\Sigma$ is at least a ($\delta$)-ring.  Similary, every $\sigma$-measurable set is measurable iff $S$ is at least a $\sigma$-ring; in any case, the $\sigma$-measurable sets form a $\sigma$-ring if $\Sigma$ is at least a $\delta$-ring.

> The terms 'relatively measurable' and '$\sigma$-measurable' are [[Toby Bartels|my own]]; I cannot find them in Halmos.  Since Halmos uses $\sigma$-rings, he has no need to speak of $\sigma$-measurable sets; but that\'s the case where the best terminology is obvious.  He does use relatively measurable sets, but he doesn\'t seem to give them a name.

Given measurable spaces $X$ and $Y$, a __measurable function__ from $X$ to $Y$ is a [[function]] $f: X \to Y$ such that the [[preimage]] $f^*(T)$ is measurable in $X$ whenever $T$ is measurable in $Y$.  Measurable spaces and measurable functions form a [[category]] $Measble$, which is [[topological concrete category|topological]] over [[Set]].

In classical measure theory, it is usually assumed that $Y$ is the [[real line]] (or a variation such as the extended real line or the complex plane) equipped with the [[Borel set]]s (see the examples below).  Then $f$ is measurable if and only if $f^{-1}(I)$ is measurable whenever $I \subseteq Y$ is an interval.

In measure theory based on ($\delta$&#8209; or $\sigma$&#8209;) rings instead of on ($\sigma$)-algebras, it is necessary to allow [[partial function]]s whose domain is a relatively measurable set.  Classically (when $Y$ is the real line), one achieves (for purposes of [[integration]]) essentially the same result by requiring only that $f^{-1}(I)$ be measurable whenever $I \subseteq Y$ is an interval that does not contain $0$; in other words, one effectively assumes that $f$ is zero wherever it would otherwise be undefined.


### Generating $\sigma$-algebras

As a $\sigma$-algebra is a collection of subsets, we might hope to develop a theory of bases and subbases of $\sigma$-algebras, such as is done for [[topological space|topologies]] and [[uniform space|uniformities]].  However, things do not work out as nicely.  (It *is* quite easy to generate rings or algebras, but generating $\delta$-rings and $\sigma$-rings is just as tricky as generating $\sigma$-algebras.)

We do get something by [[general abstract nonsense]], of course.  It\'s easy to see that the [[intersection]] of any collection of $\sigma$-algebras is itself a $\sigma$-algebra; that is, we have a [[Moore closure]].  So given any collection $B$ of sets whatsoever, the intersection of all $\sigma$-algebras containing $B$ is a $\sigma$-algebra, the $\sigma$-algebra __generated__ by $B$.  (We can similarly define the $\delta$-ring generated by $B$ and similar concepts for all of the other notions defined above.)

What is missing is a simple description of the $\sigma$-algebra generated by $B$.  (For a mere algebra, this is easy; any $B$ can be taken as a _subbase_ of an algebra, the finitary symmetric unions of elements of $B$ form a _base_ of the algebra, and the finitary intersections of elements of the base form an algebra.  For a ring, the only difference is to use only non-nullary intersections.  But for anything from a $\delta$-ring to a $\sigma$-algebra, nothing like this will work.)

In fact, the question of how to generate a $\sigma$-algebra is the beginning of an entire field of mathematics, [[descriptive set theory]].  For our purposes, we need this much:
*  Start with a collection $\Sigma_0$ (our collection $B$ above), and let $\Pi_0$ be the collection of the complements of the members of $\Sigma_0$.
*  Let $\Sigma_1$ be the collection of countably infinitary unions of sets in $\Pi_0$, and let $\Pi_1$ be the collection of their complements (the countably infinitary intersections of sets in $\Sigma_0$); even $\Sigma_1 \cup \Pi_1$ is not in general a $\sigma$-algebra.
*  Continue, defining $\Sigma_n$ for all [[natural number]]s $n$.
*  Let $\Sigma_\omega$ be the union of the various $\Sigma_n$; although this is closed under complement, it is still not in general a $\sigma$-algebra.
*  Continue, defining $\Sigma_\alpha$ for all countable [[ordinal number]]s $\alpha$.
*  Let $\Sigma$ be the union of the various $\Sigma_\alpha$; this is finally a $\sigma$-algebra.

So we need an uncountable number of steps, not just two.

(This is only the beginning of descriptive set theory; our $\Sigma_\alpha$ are their $\Sigma^0_\alpha$ ---except that for some reason they start with $\Sigma^0_1$ instead of $\Sigma^0_0$---, and the subject continues to higher values of the superscript.)

Note that [[countable choice]] is essential here and elsewhere in measure theory, to show that a countable union of a countable union is a countable union.  But the full [[axiom of choice]] is not; in fact, much of descriptive set theory (although this is irrelevant to the small portion above) works better with the [[axiom of determinacy]] instead.


## Examples

*  Of course, the [[power set]] of $X$ is closed under all operations, so it is a $\sigma$-algebra.


*  If $X$ is a [[topological space]], the $\sigma$-algebra generated by the open sets (or equivalently, by the closed sets) in $X$ is the __Borel $\sigma$-algebra__; its elements are called the __[[Borel set]]s__ of $X$. In particular, the Borel sets of [[real number]]s are the Borel sets in the [[real line]] with its usual topology.  (Note that even the $\delta$-ring generated by a topology is in fact a $\sigma$-algebra.)

   When measure theory is based on $\delta$-rings or $\sigma$-rings instead of on $\sigma$-algebras, a somewhat different notion of Borel set is sometimes used, which agrees with the above on the real line and its usual variations.  Specifically, define the __Borel $\delta$-ring__ and the __Borel $\sigma$-ring__ to be the $\delta$-ring or $\sigma$-ring generated by the [[compact space|compact]] subsets of $X$.  When $X$ is a [[compact Hausdorff space]] (such as the extended real line), then these both agree with the Borel $\sigma$-algebra above; when $X$ is [[locally compact space|locally compact]], $\sigma$-compact (a countable union of compact subsets), and [[Hausdorff space|Hausdorff]] (such as the real line or the complex plane), then the Borel $\sigma$-ring still agrees with the Borel $\sigma$-algebra.  If $X$ is not locally compact Hausdorff, then the relation is much more complicated, but the classical applications of Borel sets are to locally compact Hausdorff spaces anyway.

   When $X$ is a topological space, the hierarchy described above in generating a $\sigma$-algebra is called the __[[Borel hierarchy]]__.  In particular, starting with $\Sigma_0$ as the open sets or __$G$ sets__, then $\Pi_0$ consists of the closed sets or __$F$ sets__, $\Sigma_1$ the __$F_\sigma$ sets__, $\Pi_1$ the __$G_\delta$ sets__, $\Sigma_2$ the __$G_{\delta\sigma}$ sets__, etc.  (To remember these symbols, you need to know two languages: French and German.  The '$F$' comes from French 'ferm&#233;' for 'closed', while '$G$' is simply the next letter; the '$\sigma$' and '$\delta$' are from German 'Summe' and 'Durchschnitt' as remarked earlier.)


*  If a measurable space $(X,\Sigma)$ is equipped with a measure $\mu$, making it into a [[measure space]], then the sets of measure zero form a $\sigma$-[[sigma-ideal|ideal]] of $\Sigma$ (that is an [[ideal]] that is also a sub-$\sigma$-ring).  Let a __null set__ be *any* set (measurable or not) contained in a set of measure zero; then the null sets form a $\sigma$-ideal in the [[power set]] of $X$.  Call a set __$\mu$-measurable__ if it is the union of a measurable set and a null set; then the $\mu$-measurable sets form a $\sigma$-algebra called the __completion__ of $\Sigma$ under $\mu$.  (Even if $\Sigma$ is only a $\delta$-ring, still the null sets will form a $\sigma$-ring; in any case, we get as completion the same kind of structure as we began with.)

*  In particular, the __Lebesgue-measurable__ sets in the real line are the elements of the completion of the Borel $\sigma$-algebra under [[Lebesgue measure]].


## In alternative foundations

While Lebesgue measure on $\mathbb{R}^n$ can be done in very weak [[foundations]], a general theory of measure and measurable spaces seems to require powerful [[set theory|set-theoretic]] machinery.  Indeed, not much seems to be possible in [[predicative mathematics|predicative]] contexts, and the (nonpredicative) [[constructive mathematics|constructive]] theory is noticeably more complicated than the classical theory.  On the other hand, the classical theory has its own complications, with nonmeasurable sets and functions that can be proved to exist but which seem to never arise in practice.  Instead, there are classically false but apparently consistent foundations in which measure theory is extremely simple.


### Predicative theory

The main problem for measure theory in [[predicative mathematics]] is getting your hands on a $\sigma$-algebra.  Once you\'ve got that, you\'ve got a measurable space (obviously) and go on to [[measure space]], where there are no new difficulties.  However, what is (say) a Borel set in the real line?  This is difficult, if not impossible, to explain predicatively.  (In the case of [[Lebesgue measure]], there *are* ways to describe the Lebesgue-measurable sets predicatively, but these do not seem to generalise to a broader theory.)

Note that there is no real problem in describing what, say, an open set is.  Not only can this be done for the real line in the usual $\epsilon$-$\delta$ way, but it is easy to take *any* collection of subsets of any set $X$, call that collection a subbase, and describe which sets are the open sets in the topology generated by that subbase.  The reason is that there are only two steps in moving from a subbase to a topology, and while the latter step is too impredicative to allow one to speak of the *set* of all open sets, it\'s OK if you only want to talk about *individual* open sets.  (To be explicit: given a collection $B$ to be used as subbase, a set $G$ is _open_ if, for every point $x$, if $x \in G$, then there exist a [[natural number]] $n$ and elements $A_1, \ldots, A_n$ of $B$ such that $x \in A_i$ for each $i$ and, for every point $y$, if $y \in A_i$ for each $i$, then $y \in G$.  Since we quantify only over points and natural numbers, not over sets or functions, this is a predicative definition, and it\'s easy to prove that the open sets satisfy the axioms of a topology.)

This cannot be done with $\sigma$-algebras, since we need uncountably many sets.  To be sure, each individual step is predicative, and we can freely talk about $G_\delta$ sets and the like, but to define a Borel set we need to quantify over all countable ordinals.  While it is possible to hypothesise the existence of an uncountable ordinal $\omega_1$ and be predicative 'over' $\omega_1$ (and after all, everything else in this section is only predicative over the first infinite ordinal $\omega_0$, which we only have if we accept an [[axiom of infinity]]), this cannot be constructed predicatively.  (The immediate definition of $\omega_1$ as the [[Hartog's number]] of $\omega_0$ uses [[power set]]s; while the construction of an uncountable ordinal by applying the [[well-ordering theorem]] to the [[function set]] $\mathbf{N}^{\mathbf{N}}$ doesn\'t seem to use reasoning that requires the existence of power sets as long as you don\'t also throw in [[excluded middle]], it does use reasoning that is not accepted by any predicative school that I know.)

So as far as I ([[Toby Bartels]]) can tell, there is no general predicative theory of measurable spaces, only an ad hoc theory of Lebsegue measurability.  I would be delighted to learn otherwise!


### Constructive theory

From a constructive perspective, there are a couple of related problems with the classical theory.  One is that the notion of $\sigma$-algebra is highly suspicious, because it relies on an operation, [[complement]]ation, that behaves very differently in the [[intuitionistic logic]] that [[constructive mathematics]] uses.  The other is that, even you acept the definition of $\sigma$-algebra anyway (after all, the Lebesgue-measurable sets on the real line do still form one), there may be very few measurable functions.

Indeed, if we set aside the general theory of measurable spaces and simply do Lebesgue measure ad hoc in a constructive (even predicative) way, we find that instead of measurable [[function]]s we really want measurable [[partial function]]s whose domain of definition is a full set.  (A full set is a measurable set whose intersection with any set of measure $x$ also has measure $x$; classically, a set is full if and only if its complement is a null set.)  This suggests that if we want to define the concept of measurable function, then we have to know what the full sets are, which requires knowing at least something about the measure ---and yet we\'re only supposed to be talking about a measure*able* space!

There is a way out, due to Henry Cheng, for both of these problems at once.  Instead of dealing with individual sets, we will deal with pairs of [[disjoint set]]s.  The intuition is that we use disjoint pairs $(A,B)$ such that $A \cup B$ is full ---with $(A,\neg{A})$ being the motivating example in the classical theory---, but we let the $\sigma$-algebra itself tell us which pairs those are.  Once we fix a particular measure, we may find additional pairs whose union is full, somewhat like finding additional measurable sets when taking the completion in the classical theory (although taking the completion is a separate phenomenon here), but that\'s all right; the important thing is that each pair chosen really is full in any measure used (much as each set in a classical $\sigma$-algebra must actually be measurable by any measure used).

+-- {: .standout}
Some of the [[abstract nonsense]] below is original research, but based heavily on Cheng\'s example.
=--


#### The Boolean semi-algebra of disjoint pairs

Given a set $X$, a __disjoint pair__ in $X$ is a pair $(A,B)$ of [[subset]]s of $X$ such that $A \cap B$ is [[empty set|empty]].  Every set $A$ defines a disjoint pair $[A] = (A,\neg{A})$, but many disjoint pairs are not of this form; the extreme counterexample is $(\empty,\empty)$.  We order disjoint pairs by the usual order on the first component and the opposite on the second:
$$ (A,B) \subseteq (C,D) \;\Leftrightarrow\; A \subseteq C \;\wedge\; B \supseteq D .$$
Similarly, we make the usual operations on sets into operations on disjoint pairs by applying formal [[de Morgan duality]] to the second component:

*  $ \empty = [\empty] = (\empty, X) $;
*  $ X = [X] = (X, \empty) $;
*  $ (A,B) \cup (C,D) = (A \cup C, B \cap D) $;
*  $ (A,B) \cap (C,D) = (A \cap C, B \cup D) $;
*  $ \bigcup_i (A_i,B_i) = (\bigcup_i A_i, \bigcap_i B_i) $;
*  $ \bigcap_i (A_i,B_i) = (\bigcap_i A_i, \bigcup_i B_i) $.

(Note that we do not write $[A]$ as $A$ except when $A$ is given as $\empty$ or $X$, because for example, $[A \cap B] = [A] \cap [B]$, while classically valid, may fail constructively.)

These operations form the disjoint pairs into a [[lattice]]; in fact, it is both a [[complete lattice]] and a [[distributive lattice]], but it is not constructively completely distributive in either direction.  (Compare the fact that a power set is, constructively, completely distributive only in one direction, making it a [[frame]]; here the directions are mixed by the formal duality and so neither works.  On the other hand, that the power set is a frame is used to show that the infinitary operations do define disjoint pairs.)

Finally, we define the complement of $(A,B)$, not using the complements of $A$ and $B$ (which may not even be disjoint) but instead simply by reversing them:
$$ \neg(A,B) = (B,A) .$$
Then an actual [[de Morgan duality]] holds for these operations:

*  $ \neg\bigcup_i (A_i,B_i) = \bigcap_i \neg(A_i,B_i) $;
*  $ \neg\bigcap_i (A_i,B_i) = \bigcup_i \neg(A_i,B_i) $;
*  $ \neg\neg(A,B) = (A,B) $, the famous [[double negation]] law.

We can go on to define relative complement $(A,B) \setminus (C,D)$ and symmetric difference $(A,B) \uplus (C,D)$ in terms of complement, intersection, and union as usual, and they obey many of the usual classical laws.  (For instance, $\uplus$ is ---through a fairly lengthy calculation--- associative, which is not constructively true of [[symmetric difference]] on a power set.)

At this point, the reader could be forgiven for thinking that we have cleverly pulled a [[Boolean algebra]] out of a mere [[Heyting algebra]], but this is not true; aside from the give-away that this lattice is not constructively completely distributive, it is not even classically a Boolean algebra.  This is because $(A,B) \cup \neg(A,B) = (A \cup B, \empty)$ (and similarly for intersection) and there is no requirement that $A \cup B = X$.  What we have instead is a complete Boolean [[rig]], aka semi-ring with unit; to keep consistent with previous terminology, I\'ll call such a thing a _Boolean semi-algebra_.

As Todd pointed out, this is a special case of the [[Chu construction]]; the poset of disjoint pairs in $X$ is $Chu_{TV}(P X, \empty)$, where $TV$ is the [[enriched category|enriching]] category of [[truth value]]s.

+--{.query} 
_Todd_: This is interesting; it smells like a decategorified version of the [[Chu construction]], which takes a pair $(C, d)$ consisting of a symmetric monoidal category $C$ and an object $d$ therein, and produces a [[*-autonomous category]] whose objects are triples $(a, b, f: a \otimes b \to d)$, and whose dualizing object is $(d, I, d \otimes I \cong d)$ where $I$ is the monoidal unit. But I should think about it a bit more. 

_Toby_:  Ah, so $C$ is the power set of $X$, $d$ is the empty set, and $\otimes$ is intersection, so we have $(A, B, A \cap B \subseteq \empty)$.  And (even constructively) $C$ is even a bi-complete closed monoidal category, that is (in this decategorified, truth-value enriched case) a complete Heyting algebra.  So we really are looking at $Chu(P X, \empty)$ here.  And let\'s see ... the internal hom $(A,B) \multimap (C,D)$ comes out to $((A \Rightarrow C) \cap (D \Rightarrow B), A \cap D) = ((A \cup D) \Rightarrow (B \cup C)), A \cap D)$, which comes with tensor tensor product $(A,B) \otimes (C,D) = (A \cap C, (A \Rightarrow D) \cap (C \Rightarrow B)) = (A \cap C, (A \cup C) \Rightarrow (B \cup D))$.

Too bad that these operations don\'t seem to be relevant; if they\'d been $\setminus$ or $\uplus$ instead, then I\'d have been pretty pleased.  Still, $(A,B) \multimap [\empty] = (B,A) = \neg(A,B)$, so everything can be nicely described with that structure if we want.

I was worried for a bit, since $Chu(P X, \empty)$ isn\'t constructively cartesian closed (although it is classically).  But intersection is not the relevant monoidal structure anymore.
=--


#### The $\sigma$-semi-algebra of complemented pairs

Given a set $X$, a __$\sigma$-semi-algebra__ on $X$ is a collection $\Sigma$ of disjoint pairs in $X$, called the __complemented pairs__ of $\Sigma$, such that:
1.  $[\empty] = (\empty,X)$ is a complemented pair;
1.  If $(A,B)$ is a complemented pair, then so is its complement $(B,A)$;
1.  If $(A_1,B_1), (A_2,B_2), (A_3,B_3), \ldots$ are complemented pairs, then so is their union $(\bigcup_i A_i, \bigcap_i B_i)$.

The arguments above that $\Sigma$ is closed under countable intersections, relative complements, and symmetric differences goes through.  (We can also define analogous notions of semi-algebra, $\delta$-semi-ring, and the rest.)

Of course, a __Cheng measurable space__ (we don\'t really want 'semi-' here) is a set equipped with a $\sigma$-semi-algebra.

Incidentally, the reason why we do not use the term 'measurable pair' is that $A$ and $B$ may easily both be measurable in some sense yet without having $(A,B)$ as a complemented pair.  In particular, $(\empty,\empty)$ is rarely a complemented pair (although that is not forbidden either), yet it is hard to call it non-measurable.


#### Measurable functions

Given two Cheng measurable spaces $X$ and $Y$, an __almost function__ from $X$ to $Y$ is a [[partial function]] from $X$ to $Y$ such that, for some complemented pair $(A,B)$, the domain of $f$ contains $A \cup B$.  A __measurable function__ from $X$ to $Y$ is a partial function from $X$ to $Y$ such that, given any complemented pair $(C,D)$ in $Y$, the pair $(f^*(C),f^*(D))$ of [[preimage]]s is a complemented pair.  (By trying $(C,D) = (X,\empty)$, we see that a measurable function is an almost function, but the converse need not hold.)

Cheng measurable spaces and measurable functions between them form a [[topological concrete category]]. 

### In dream universes

While measure theory only gets more complicated in constructive mathematics, it becomes much easier in [[dream universe|dream mathematics]].

... more coming ...


## References

For Cheng\'s theory of measure spaces, see the 1985 edition of Bishop & Bridges, _Constructive Analysis_.  (And the references therein, obviously, but I haven\'t read those.)


[[!redirects measurable set]]
[[!redirects measurable subset]]
[[!redirects measurable function]]
[[!redirects sigma-algebra]]
[[!redirects delta-algebra]]
[[!redirects sigma-field]]
[[!redirects delta-field]]
[[!redirects sigma-ring]]
[[!redirects delta-ring]]
[[!redirects ∞-algebra]]
[[!redirects ∞-algebra]]
[[!redirects ∞-field]]
[[!redirects ∞-field]]
[[!redirects ∞-ring]]
[[!redirects ∞-ring]]
[[!redirects ∞-algebra]]
[[!redirects ∞-algebra]]
[[!redirects ∞-field]]
[[!redirects ∞-field]]
[[!redirects ∞-ring]]
[[!redirects ∞-ring]]
[[!redirects Cheng measurable space]]
[[!redirects measurable spaces]]
[[!redirects measurable sets]]
[[!redirects measurable subsets]]
[[!redirects measurable functions]]
[[!redirects sigma-algebras]]
[[!redirects delta-algebras]]
[[!redirects sigma-fields]]
[[!redirects delta-fields]]
[[!redirects sigma-rings]]
[[!redirects delta-rings]]
[[!redirects ∞-algebras]]
[[!redirects ∞-algebras]]
[[!redirects ∞-fields]]
[[!redirects ∞-fields]]
[[!redirects ∞-rings]]
[[!redirects ∞-rings]]
[[!redirects ∞-algebras]]
[[!redirects ∞-algebras]]
[[!redirects ∞-fields]]
[[!redirects ∞-fields]]
[[!redirects ∞-rings]]
[[!redirects ∞-rings]]
[[!redirects Cheng measurable spaces]]
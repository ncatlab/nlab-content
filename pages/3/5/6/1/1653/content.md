Measurable spaces are a necessary prelude to the general to the general theory of measure and integration.  Basically, a measurable space picks out those sets of a [[measure space]] that are 'measurable', regardless of what their actual measure is.  (Thus you get a measure space by placing a measure on a measurable space.)

Ideally, all subsets would be measurable, but this contradicts the [[axiom of choice]] for the basic example of [[Lebesgue measure]] on the [[real line]].  Although it is possible to use nonstandard [[foundations]] of mathematics in which all subsets of the real line are Lebesgue measurable, any general theory that includes that example and is more general than those foundations requires some notion of measurable space.

In any case, measurable spaces are of some interest in their own right, even without a measure on them.


## Definitions ##

We assume the law of [[excluded middle]] throughout; see below for the constructive theory.


### Short version ###

Given a [[set]] $X$, the [[power set]] $P X$ of $X$ is a [[Boolean algebra]] under the operations of [[finite set|finitary]] [[union]], [[intersection]], and [[complement]]ation.  Actually, it is a [[complete lattice|complete]] Boolean algebra, since we can also take arbitrary unions and intersections.  A $\sigma$-algebra is an intermediate notion where we require (in addition to complements) [[countable set|countable]] unions and intersections.

A __measurable space__, by the usual modern defintion, is simply a set $X$ equipped with a $\sigma$-algebra $\Sigma$.  The elements of $\Sigma$ are the __measurable sets__ in $X$ (or properly, in $(X,\Sigma)$).

If you are happy with this, then feel free to skip the long version below.


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


*  A __$\sigma$-ring__ on $X$ is a ring $\Sigma$ which is closed under countable infintary union.  That is:
   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ and $T$ are measurable, then so is their union $S \cup T$.
   1.  If $S$ and $T$ are measurable, then so is their relative complement $T \setminus S$.
   1.  If $S_1, S_2, S_3, \ldots$ are measurable, then so is their union $\bigcup_i S_i$.

   Now (2) is simply redundant; $S \cup T = S \cup T \cup T \cup T \cup \cdots$.  A $\sigma$-ring is obviously a ring, but in fact it is also a $\delta$-ring; $\bigcap_i S_i = \bigcup_i S_i \setminus \bigcup_j (\bigcup_i S_i \setminus S_j)$.


*  An __algebra__ or __field__ on $X$ is a ring $\Sigma$ to which $X$ itself belongs.  That is:
   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ and $T$ are measurable, then so is their union $S \cup T$.
   1.  If $S$ and $T$ are measurable, then so is their relative complement $T \setminus S$.
   1.  $X$ is measurable.

   Actually, (2) is now redundant again; $S \cup T = X \setminus ((X \setminus T) \setminus S)$.  But perhaps more importantly, $\Sigma$ is closed under *absolute* complementation (that is, complementation relative to the entire ambient set $X$); that is:

   *  If $S$ is measurable, then so is its complement $X \setminus S$.

   In light of this, the most common definition of algebra is probably to use this fact together with (1,2); then (3) follows because $T \setminus S = X \setminus (S \cup (X \setminus T))$ and (4) follows because $X = X \setminus \empty$.  On the other hand, one could equally well use intersection instead of union; absolute complements allow the full use of [[de Morgan duality]].

   Warning: the term 'field' here is even more archaic that the term 'ring' above; indeed the only field in this sense which is a [[field]] (in the usual sense) under symmetric difference and intersection is the field $\{\empty, X\}$ for an [[inhabited set]] $X$.


*  Finally, a __$\sigma$-algebra__ or __$\sigma$-field__ on $X$ is a ring $\Sigma$ that is both an algebra and a $\sigma$-ring.  That is:
   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ and $T$ are measurable, then so is their union $S \cup T$.
   1.  If $S$ and $T$ are measurable, then so is their relative complement $T \setminus S$.
   1.  $X$ is measurable.
   1.  If $S_1, S_2, S_3, \ldots$ are measurable, then so is their union $\bigcup_i S_i$.

   As with $\sigma$-rings, (2) is redundant; as with algebras, it\'s probably most common to use the absolute complement in place of (3,4).  Thus the usual definition of a $\sigma$-algebra states:
   1.  The [[empty set]] $\empty$ is measurable.
   1.  If $S$ is measurable, then so is its complement $X \setminus S$.
   1.  If $S_1, S_2, S_3, \ldots$ are measurable, then so is their union $\bigcup_i S_i$.

   And again we could again just as easily use intersection as union, even in the infinite case.  That is, a $\delta$-algebra is automatically a $\sigma$-algebra, because $\bigcup_i S_i = X \setminus \bigcap_i (X \setminus S_i)$.


Any and all of the above notions have been used by various authors in the definition of measurable space.  Of course, the finitary notions (ring and algebra) aren\'t strong enough to describe the interesting features of Lebesgue measure; they are used to study very different examples.  On the other hand, $\delta$-rings and $\sigma$-rings may be more convenient than $\sigma$-algebras for some purposes; in particular, the collection of measurable sets with finite measure (in a given [[measure space]]) is a $\delta$-ring, and the collection of measurable sets with $\sigma$-finite measure is a $\sigma$-ring.


### Measurable functions

Given measurable spaces $X$ and $Y$, a __measurable function__ from $X$ to $Y$ is a [[function]] $f: X \to Y$ such that the [[preimage]] $f^*(T)$ is measurable in $X$ whenever $T$ is measurable in $Y$.

Measurable spaces and measurable functions form a [[category]] $Measble$, which is [[topological concrete category|topological]] over [[Set]].


### Generating $\sigma$-algebras

As a $\sigma$-algebra is a collection of subsets, we might hope to develop a theory of bases and subbases of $\sigma$-algebras, such as is done for [[topological space|topologies]] and [[uniform space|uniformities]].  However, things do not work out as nicely.

We do get something by [[general abstract nonsense]], of course.  It\'s easy to see that the [[intersection]] of any collection of $\sigma$-algebras is itself a $\sigma$-algebra; that is, we have a [[Moore closure]].  So given any collection $B$ of sets whatsoever, the intersection of all $\sigma$-algebras containing $B$ is a $\sigma$-algebra, the $\sigma$-algebra __generated__ by $B$.  (We can similarly define the $\delta$-ring generated by $B$ and similar concepts for all of the other notions defined above.)

What is missing is a simple description of the $\sigma$-algebra generated by $B$.  (For a mere algebra, this is easy; any $B$ can be taken as a _subbase_ of an algebra, the finitary symmetric unions of elements of $B$ form a _base_ of the algebra, and the finitary intersections of elements of the base form an algebra.  For a ring, the only difference is to use only non-nullary intersections.  But for anything from a $\delta$-ring to a $\sigma$-algebra, nothing like this will work.)

In fact, the question of how to generate a $\sigma$-algebra is the beginning of an entire field of mathematics, [[descriptive set theory]].  For our purposes, we need this much:
*  Start with a collection $\Sigma_0$ (our collection $B$ above), and let $\Pi_0$ be the collection of the complements of the members of $\Sigma_0$.
*  Let $\Sigma_1$ be the collection of countably infinitary unions of sets in $\Pi_0$, and let $\Pi_1$ be the collection of their complements (the countably infinitary intersections of sets in $\Sigma_0$); even $\Sigma_1 \cup \Pi_1$ is not in general a $\sigma$-algebra.
*  Continue, defining $\Sigma_n$ for all [[natural number]]s $n$.
*  Let $\Sigma_\omega$ be the union of the various $\Sigma_n$; although this is closed under complement, it is still not in general a $\sigma$-algebra.
*  Continue, defining $\Sigma_\alpha$ for all countable [[ordinal number]]s $\alpha$.
*  Let $\Sigma_\Omega$ be the union of the various $\Sigma_\alpha$; this is finally a $\sigma$-algebra.

So we need an uncountable number of steps, not just two.

(This is only the beginning of descriptive set theory; our $\Sigma_\alpha$ are their $\Sigma^0_\alpha$ ---except that for some reason they start with $\Sigma^0_1$ instead of $\Sigma^0_0$---, and the subject continues to higher values of the superscript.)


## Examples

If $X$ is a [[topological space]], the intersection of all $\sigma$-algebras which contain the open sets on $X$ is again a $\sigma$-algebra, whose elements are called the __Borel sets__ of $X$. In particular, the Borel sets of [[real number]]s are the Borel sets in the [[real line]] with its usual topology.

If $X$ is any measurable space, then a _measurable function_ from $X$ to $\mathbb{R}$ is generally taken to refer to Borel sets in $\mathbb{R}$; then $f$ is measurable if and only if $f^{-1}(U)$ is measurable whenever $U \subseteq \mathbb{R}$ is open. The convention is similar if $\mathbb{R}$ is replaced by the space of extended reals $[-\infty, \infty]$, or by the space of complex numbers $\mathbb{C}$.


## In alternative foundations

While Lebesgue measure on $\mathbb{R}^n$ can be done in very weak [[foundations]], a general theory of measure and measurable spaces seems to require powerful [[set theory|set-theoretic]] machinery.  Indeed, not much seems to be possible in [[predicative mathematics|predicative]] contexts, and the (nonpredicative) [[constructive mathematics|constructive]] theory is noticeably more complicated than the classical theory.  On the other hand, the classical theory has its own complications, with nonmeasurable sets and functions that can be proved to exist but which seem to never arise in practice.  Instead, there are classically false but apparently consistent foundations in which measure theory is extremely simple.


### Predicative theory

...


### Constructive theory

...


### In dream universes

...


... coming ...


[[!redirects measurable set]]
[[!redirects measurable function]]
[[!redirects sigma-algebra]]
[[!redirects delta-algebra]]
[[!redirects sigma-field]]
[[!redirects delta-field]]
[[!redirects sigma-ring]]
[[!redirects delta-ring]]
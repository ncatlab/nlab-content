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
   *  If $S$ and $T$ are measurable, then so is their symmetric difference $S \ocup T = (T \setminus S) \cup (S \setminus T)$.

   We can actually use the latter as an alternative to (2), since $S \cup T = (S \ocup T) \ocup (S \cap T)$.  Or we can use the pair as an alternative to (2,3), since $T \setminus S = (S \cap T) \ocup T$.  For that matter, we can weaken (1) to simply say that *some* set $S$ is measurable; then $\empty = S \setminus S$.

   While the nullary union and nullary symmetric difference (both the empty set) belong to $\Sigma$, the nullary intersection (which is $S$ itself) might not.  The term 'ring' dates from the days when a [[ring]] in algebra was not assumed to be unital; so a ring on $X$ is simply a Boolean subring (in this sense) of the [[Boolean ring]] $P X$.


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

Measurable spaces and measurable functions form a [[category]] $Measble$.


## Examples

If $X$ is a [[topological space]], the intersection of all $\sigma$-algebras which contain the open sets on $X$ is again a $\sigma$-algebra, whose elements are called the __Borel sets__ of $X$. In particular, the Borel sets of [[real number]]s are the Borel sets in the [[real line]] with its usual topology.

If $X$ is any measurable space, then a _measurable function_ from $X$ to $\mathbb{R}$ is generally taken to refer to Borel sets in $\mathbb{R}$; then $f$ is measurable if and only if $f^{-1}(U)$ is measurable whenever $U \subseteq \mathbb{R}$ is open. The convention is similar if $\mathbb{R}$ is replaced by the space of extended reals $[-\infty, \infty]$, or by the space of complex numbers $\mathbb{C}$.


## In alternative fondations

... coming ...
The _Hartog\'s number_ of a [[cardinal number]] $\kappa$ is the number of ways to [[well-order]] a set of cardinality at most $\kappa$.  Assuming the [[axiom of choice]], it is the smallest [[ordinal number]] whose cardinality is greater than $\kappa$ and therefore the [[successor]] of $\kappa$ as a cardinal number.  But even without the axiom of choice, it makes sense and is often an effective substitute for such a successor.


## Definition

We will define the Hartog\'s number as a [[functor]]ial operation from [[set]]s to [[well-ordered set]]s.  The operation on numbers is just a round-about way of talking about the same thing.

So let $S$ be a set.  Without the axiom of choice (or more precisely, the [[well-ordering theorem]]), it may not be possible to well-order $S$ itself, but we can certainly well-order some [[subset]]s of $S$.  On the other hand, if we can well-order $S$ (or a subset), then there may be many different ways to do so, even non[[isomorphism|isomorphic]] ways.  So to begin with, let us form the collection of all well-ordered subsets of $S$, that is the subset of
$$ \coprod_{A: \mathcal{P}S} \mathcal{P}(A \times A) ,$$
where $\coprod$ indicates [[disjoint union]] and $\mathcal{P}$ indicates [[power set]], consisting of those pairs $(A,R)$ such that $R$ is a well-ordering.  Then form a [[quotient set]] by identifying all well-ordered subsets that are isomorphic as well-ordered sets.  This gives a set of well-order types, or [[ordinal number]]s, which can itself be well-orderd by the general theory of ordinal numbers.

The __Hartog\'s number__ of $S$ is this well-ordered set, the set of all order types of well-ordered subsets of $S$.  If $\kappa$ is the cardinality of $S$, then let $\kappa^+$ be the cardinality or ordinal rank (as desired) of the Hartog\'s number of $S$; this is called the __Hartog\'s number__ of $\kappa$.


## Properties

There is no [[injection]] to $S$ from the Hartog\'s number of $S$; this theorem is to [[Cantor's theorem]] as Burali-Forti\'s paradox is to Russell\'s paradox.  That is, using the usual ordering of cardinal numbers, $\kappa^+ \nleq \kappa$.  So if this $\leq$ is a [[total order]] (a statement equivalent to the [[axiom of choice]]), we can say that $\kappa^+ \gt \kappa$.

Even without choice, however, we can say this:  If $\alpha$ is an ordinal number such that $|\alpha| \nleq \kappa$, then $\kappa^+ \leq \alpha$.  (Notice that we\'ve shifted our thinking of the Hartog\'s number from a cardinal to an ordinal.)  That is, $\kappa^+$ is the smallest ordinal number whose cardinal number is not at most $\kappa$.  This doesn\'t use any form of choice except for [[excluded middle]]; we only need choice to conclude that $|\kappa^+| \gt \kappa$.

The axiom of choice also implies the well-ordering theorem, that any set can be well-ordered.  Thus with choice, $\kappa^+$ is (now as a cardinal again) the smallest cardinal number greater than $\kappa$; this explains the notation $\kappa^+$.


## Examples

For $n$ a [[natural number]] regarded as the cardinal number of a [[finite set]], $n^+$ is the usual [[successor]] $n + 1$.  This result uses excluded middle; else we get the _plump_ successor of $n$, which may be rather larger.

For $\aleph_0$ the cardinality of the set of all [[natural number]]s, the Hartog\'s number $\aleph_0^+ = \omega_1$ is the smallest [[uncountable set|uncountable]] ordinal.  Assuming the axiom of choice ([[countable choice]] and excluded middle are enough), we have $\aleph_0^+ = \aleph_1$ as a cardinal.

In general, we get a sequence $\omega_\alpha$ of infinite cardinalities of well-orderable sets; assuming excluded middle, every infinite well-orderable cardinality shows up in this sequence.  Assuming the axiom of choice, every infinite cardinal shows up, and we have $|\omega_\alpha| = \aleph_\alpha$.  (Actually, there\'s no real need to begin with infinite cardinals; if we started with $\omega_0 = 0$ instead of $\omega_0 = \mathbf{N}$ and $\aleph_0 = 0$ instead of $\aleph_0 = |\mathbf{N}|$, then absolutely *every* cardinality or well-orderable cardinality would appear.)
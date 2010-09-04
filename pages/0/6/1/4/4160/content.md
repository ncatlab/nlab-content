**Under Construction**


##Idea

The _Lebesgue measure_ is the usual [[measure]] on the [[real line]] (or on any [[Cartesian space]]).  It may be characterised as the [[Radon measure]] which is translation invariant and assigns measure $1$ to the [[unit interval]] (or unit cube).  It generalises to [[Haar measure]] on any [[locally compact space|locally compact]] [[topological group]].



The Lebesgue measure's origins can be traced to the broader theory of Lebesgue integration.  The original purpose of the latter, in broad terms, was to expand the class of integrable functions in order to give meaning to functions that are _not_ Riemann integrable.  In order to accomplish this, the basic properties of the concept of the _length_ of an interval must be understood.  This then leads to the need to fully define the concept of _measure_, particularly in relation to sets.  We begin with a lemma and a corollary.

**Lemma:** _Let I be an interval, $I=I_{1} \cup I_{2} \cup \cdots$ where $I_{1}, _{2}, \ldots$ are disjoint intervals.  Then ${|I|}=\sum_{j=1}^{\infty}{|I_{j}|}$ (interpreted to mean that if one side $+\infty$, then so is the other, where $\sum_{j=1}^{\infty}{|I_{j}|}$ can be $+\infty$, either because one of the summands is $+\infty$ or because the series diverges).

**Corollary:** _If I is any interval, then_

$$
  {|I|}=inf\left\{\sum_{j=1}^{\infty}{|I_{j}|}:I \subseteq \bigcup_{j=1}^{\infty} I_{j}\right\}
$$

_where_ $\{I_{j}\}$ _is any countable covering of I by intervals._ $\}$.

Now suppose _B_ is an arbitrary set.  In order for _B_ to be measurable, we must have ${|B|} \le \sum_{j=1}^{\infty}{|I_{j}|}$ where $\bigcup_{j=1}^{\infty} I_{j}$ is any countable covering of _B_ by intervals.  We must also have ${|B|}\le \bigcup_{j=1}^{\infty} {|I_{j}|}$ where the infinum is taken over all countable coverings of _B_ by intervals.

##Definition

We may define the Lebesgue measure as being

$$
  {|B|}=inf\left\{\sum_{j=1}^{\infty}{|I_{j}|}:B \subseteq \bigcup_{j=1}^{\infty} I_{j}\right\}.
$$

Note that once the Lebesgue measure is known for open sets, the outer regularity property allows us to find it for all Borel sets.

##References

* [Wikipedia](http://en.wikipedia.org/wiki/Lebesgue_measure).
* [nForum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=1385&Focus=11747#Comment_11747)

For a very intuitive and readable derivation, see:

* R. Strichartz, _The Way of Analysis_, Jones & Bartlett, 2000.
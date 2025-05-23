
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Lebesgue measure
* table of contents
{: toc}

## Idea

The _Lebesgue measure_ is the usual [[measure]] on the [[real line]] (or on any [[Cartesian space]]).  It may be characterised as the [[Radon measure]] which is translation invariant and assigns measure $1$ to the [[unit interval]] (or unit cube).  It generalises (up to a scalar constant) to [[Haar measure]] on any [[locally compact space|locally compact]] [[topological group]].


## History

The Lebesgue measure's origins can be traced to the broader theory of [[Lebesgue integral|Lebesgue integration]].  The original purpose of the latter, in broad terms, was to expand the class of integrable functions in order to give meaning to functions that are _not_ [[Riemann integral|Riemann integrable]].  In order to accomplish this, the basic properties of the concept of the _length_ of an interval must be understood.  This then leads to the need to fully define the concept of _measure_, particularly in relation to sets.  We begin with a lemma and a corollary.

+-- {: .num_lemma}
###### Lemma

Let I be an interval, $I = I_{1} \cup I_{2} \cup \cdots$ where $I_{1}, I_{2}, \ldots$ are disjoint intervals.  Then ${|I|} = \sum_{j=1}^{\infty} {|I_{j}|}$ (interpreted so that $\sum_{j=1}^{\infty} {|I_{j}|}$ can be $+\infty$, either because one of the summands is $+\infty$ or because the series diverges).
=--

+-- {: .num_corollary}
###### Corollary

If I is any interval, then
$$
  {|I|} = inf \left\{\sum_{j=1}^{\infty} {|I_{j}|} : I \subseteq \bigcup_{j=1}^{\infty} I_{j}\right\}
$$
where $\{I_{j}\}$ is any countable covering of I by intervals.
=--

Now suppose $B$ is an arbitrary set of real numbers.  In order for $B$ to be measurable, we must have ${|B|} \leq \sum_{j=1}^{\infty} {|I_{j}|}$ where $\bigcup_{j=1}^{\infty} I_{j}$ is any countable covering of $B$ by intervals.  We must also have ${|B|} \leq \bigcup_{j=1}^{\infty} {|I_{j}|}$ where the infinum is taken over all countable coverings of $B$ by intervals.


## Definition

We define the __Lebesgue [[outer measure]]__ as follows:
$$
  {|B|} = inf \left\{\sum_{j=1}^{\infty} {|I_{j}|} : B \subseteq \bigcup_{j=1}^{\infty} I_{j}\right\}.
$$

The set $B$ is __Lebesgue measurable__ if
$$ {|A|} = {|A \cap B|} + {|A \setminus B|} $$
holds for every set $A$.  Restricting to these sets, Lebesgue outer measure becomes an honest [[measure]].

Note that once the Lebesgue measure is known for open sets, the outer regularity property allows us to find it for all [[Borel set]]s (but also rather more sets).

## See also

* [[Jordan content]]

## References

Named after [[Henri Lebesgue]].

See also

* [Wikipedia](http://en.wikipedia.org/wiki/Lebesgue_measure).
* [nForum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=1385)

For a very intuitive and readable derivation, see:

* R. Strichartz, _The Way of Analysis_, Jones & Bartlett, 2000.

For a [[polynomial function]] whose Lesbegue measurability is independent of [[ZFC]], see:

* [[James E. Hanson]], *Any function I can actually write down is measurable, right?* ([arXiv:2501.02693](https://arxiv.org/abs/2501.02693))

[[!redirects Lebesgue measure]]
[[!redirects Lebesgue measures]]

[[!redirects Lebesgue-measurable set]]
[[!redirects Lebesgue-measurable sets]]
[[!redirects Lebesgue measurable set]]
[[!redirects Lebesgue measurable sets]]
[[!redirects Lebesgue-measurable subset]]
[[!redirects Lebesgue-measurable subsets]]
[[!redirects Lebesgue measurable subset]]
[[!redirects Lebesgue measurable subsets]]

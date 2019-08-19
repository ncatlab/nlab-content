
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Countable sets
* table of contents
{: toc}

## Idea

Let $S$ be any [[set]], and let $\mathbf{N}$ be the [[set]] of [[natural number]]s.  Let $|S|$ be the [[cardinality]] of $S$, and let $\aleph_0$ be the cardinality of $\mathbf{N}$.

Then $S$ is:

*  __denumerable__ if ${|S|} = \aleph_0$,
*  __countable__ if ${|S|} \leq \aleph_0$, and
*  __uncountable__ if ${|S|} \gt \aleph_0$.

Note that the first two terms are not entirely standardised; some authors use them interchangeably for one or the other concept.


## Definitions

If you accept the [[axiom of choice]], then there is really nothing more to say than what was above.  In weaker [[foundations]], more care may be needed.  The following seem to be the usual definitions in [[constructive mathematics]]:

*  $S$ is __denumerable__ if there exists a [[bijection]] from $\mathbf{N}$ to $S$.
*  $S$ is __countable__ if there exists a [[surjection]] from a [[detachable subset|detachable]] [[lower subset]] of $\mathbf{N}$ to $S$.
*  $S$ is __uncountable__ if, given any [[function]] $f$ from a detachable subset of $\mathbf{N}$ to $S$, the function is strongly non-surjective in the sense that there exists an element of $S$ that is not in the [[image]] of $f$.

Of course, the terms are even less standardised here.

Following the usage of terms for different senses of [[finite sets]], we can add 'sub' to the front of any of these words to mean a [[subset]] of such a set; classically, this would make 'subdenumerable', 'subcountable', and 'countable' all synonyms; but constructively, none of these are the same.  In fact, in [[Russian constructivism]], the set of [[real numbers]] is subcountable (because the set of [[computable numbers]] definitely is).  Indeed, one possible axiom for Russian constructivism is that *every* set is subcountable.

We can also change the suffix 'able' to 'ably indexed' to mean a [[quotient set]]; this manifestly makes no difference to 'countable', and even constructively, a denumerably indexed set (which is at least sometimes called an _enumerable set_) is the same thing as an [[inhabited set|inhabited]] countable set.  To use this terminology systematically, it would probably make more sense to define a set to be _countable_ if it has a *bijection* from a detachable lower subset.  One reason for using 'countable' to mean countably indexed is that this is about the most general term that definitely does *not* hold of the set of real numbers.


## Examples and Properties

The set of [[real numbers]] is uncountable.  (Arguably, [[set theory]] as such begins with [[Georg Cantor]]\'s [[proof]] of this statement.)

Given any [[infinite set]], its [[power set]] is uncountable by [[Cantor's theorem]].

The [[empty set]] is countable. 

Any uncountable set must be [[inhabited set|inhabited]].  

Any (Kuratowski)-[[finite set]] is countable.

Any uncountable set must be [[infinite set|infinite]].  

A [[denumerable set]] is precisely an [[infinite set|infinite]] countable set; sometimes this is written as a _countably infinite set_.

In [[classical mathematics]], [[countable unions of countable sets are countable]].

In [[classical mathematics]] a countable set is either [[finite set|finite]] or [[denumerable set|denumerable]]. This need not hold in [[constructive mathematics]].  We do have, however, that a countable set is either empty or inhabited, which is classically trivial but need not hold constructively for every set.

In some forms of [[constructive mathematics]], especially in the Russian school, it is assumed (or provable from other assumptions) that *every* set is a [[subset]] of a countable set.  The fact the the set of real numbers is uncountable still applies, however, as the inclusion map of the subset need not [[split monomorphism|split]].  In particular, the set of [[computable number]]s is a subset of a countable set, but to prove that it is itself countable requires [[excluded middle]].


## Related concepts

* [[countable ordinal]]

* [[countable cover]]


[[!redirects countable set]]
[[!redirects countable sets]]
[[!redirects countably infinite set]]
[[!redirects countably infinite sets]]
[[!redirects denumerable set]]
[[!redirects denumerable sets]]

[[!redirects uncountable set]]
[[!redirects uncountable sets]]

[[!redirects countable family]]
[[!redirects countable families]]

[[!redirects numerable]]
[[!redirects numerable set]]
[[!redirects numerable sets]]

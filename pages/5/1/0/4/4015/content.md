
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# The fan theorem
* table of contents
{: toc}

## Introduction

The fan theorem is one of the basic principles of [[intuitionism]] that make it more specific (even in [[mathematics|mathematical]] practice, independent of any [[philosophy|philosophical]] issues) than garden-variety [[constructive mathematics]].  Its main use is to justify pointwise [[analysis]]; without it, one really needs [[locale theory]] for [[point-free topology]] instead.  In [[classical mathematics]], the fan theorem is [[true]].


## Statement

Consider the [[list|finite]] and [[infinite sequence|infinite]] sequences of [[binary digits]].  Given an infinite sequence $\alpha$ and a [[natural number]] $n$, let $\bar \alpha n$ be the finite sequence consisting of the first $n$ [[elements]] of $\alpha$.

Let $B$ be a collection of [[finite set|finite]] sequences of bits (or _bitlists_), that is a [[subset]] of the [[free monoid]] on the [[boolean domain]].  Given an infinite sequence $\alpha$ and a natural number $n$, we say that $\alpha$ _$n$-bars_ $B$ if $\bar \alpha n \in B$; given only $\alpha$, we say that $\alpha$ _bars_ $B$ if $\alpha$ $n$-bars $B$ for some $n$.

We are interested in these three properties of $B$:

*  $B$ is _[[decidable subset|decidable]]_:  For every finite sequence $u$, either $u \in B$ or $u \notin B$.  (This is trivial in [[classical logic]] but will hold constructively only for some subsets $B$.)
*  $B$ is _barred_:  For every infinite sequence $\alpha$, $\alpha$ bars $B$.
*  $B$ is _uniform_:  For some natural number $M$, for every infinite sequence $\alpha$, if $\alpha$ bars $B$ at all, then $\alpha$ $n$-bars $B$ for some $n \leq M$.

A __bar__ is a barred subset $B$.

+-- {.un_theorem}
###### Decidable Fan Theorem

Every decidable bar is uniform.
(In other words, if a collection of bitlists is decidable and barred, then it is also uniform.)
=--

+-- {.un_theorem}
###### (Full) Fan Theorem
Every bar is uniform. (In other words, if a collection of bitlists is decidable and barred, then it is also uniform.)
=--

Although the fan theorem is about bars, it is different from the [[bar theorem]], also known as "bar induction", which is related but stronger. The fan theorem discusses bars on lists of elements of $\mathbb{B}$; the bar theorem discusses bars on lists of elements of $\mathbb{N}$.

Bar induction has three forms; decidable bar induction, monotone bar induction, and full bar induction (each stronger than the previous). The decidable fan theorem follows from decidable bar induction; the full fan theorem follows from monotone bar induction. Full bar induction, the strongest of the three, is a classical theorem; however, full bar induction implies Bishop's limited [[principle of omniscience]]. [[function realizability|Kleene's second realizability model]] provides a model of monotone bar induction plus Brouwer's continuity principle.

### Obfuscation

Let $\mathbb{B}$ be the set $\{0,1\}$ of binary digits (bits) and $\mathbb{N}$ the set $\{0,1,2,\ldots\}$ of natural numbers (numbers).  Given a [[set]] $A$, let $A^*$ be the set of finite sequences of elements of $A$, let $A^{\mathbb{N}}$ be the set of infinite sequences of elements of $A$, and let $\mathcal{P}_{\Delta}A$ be the set of decidable subsets of $A$.  Then the fan theorem is about (elements of) $\mathbb{B}^*$, $\mathbb{B}^{\mathbb{N}}$, and $\mathcal{P}_{\Delta}\mathbb{B}^*$.

However, the sets $\mathbb{N}$, $\mathbb{B}^*$, and $\mathbb{N}^*$ are all isomorphic.  Similarly, the sets $\mathbb{B}^{\mathbb{N}}$, $\mathcal{P}_{\Delta}\mathbb{N}$, $\mathcal{P}_{\Delta}\mathbb{B}^*$, and $\mathcal{P}_{\Delta}\mathbb{N}^*$ are all isomorphic.  In much of the literature on bars, one tacitly uses all of these isomorphisms, taking $\mathbb{N}$ and $\mathbb{B}^{\mathbb{N}}$ as chosen representatives of their isomorphism classes.  Thus, everything in sight is either a natural number or an infinite sequence of bits.

The fan theorem is hard enough to understand when $\alpha$ is an infinite sequence of bits and $\bar \alpha n$ is a finite sequence of bits; it is even harder to understand when $\bar \alpha n$ is a natural number that bears no immediate relationship to the digits in the sequence $\alpha$.


## Use in analysis

In [[classical mathematics]], the fan theorem is simply true.

In [[constructive mathematics]], the full fan theorem is equivalent to any and all of the following statements:

*  As a [[locale]], [[Cantor space]] has enough points (is [[topological locale|topological]]).
*  As a [[topological space]], Cantor space is [[compact space|compact]].

Assuming some amount of countable/dependent choice (probably pretty weak: haven't checked myself though), the full fan theorem is equivalent to each of the following statements:

*  As a topological space, the (located Dedekind) [[unit interval]] is [[compact space|compact]] (the [[Heine-Borel theorem|Heine–Borel theorem]]).
*  As a topological space, the (located Dedekind) [[real line]] is [[locally compact space|locally compact]].
*  There exists a class of "kontinuous" [[partial functions]] from the set $\mathbb{R}$ of (located Dedekind) [[real numbers]] to itself (see Waaldijk) such that
   *  the [[restriction]] of a kontinuous function to any smaller domain is kontinuous;
   *  the [[identity function]] on $\mathbb{R}$ is kontinuous;
   *  the [[composite]] of two kontinuous functions is kontinuous;
   *  a function whose domain is the unit interval is kontinuous *if and only if* it is uniformly continuous (in the usual metric-space sense); and
   *  the function $(x \mapsto 1/x)$ defined on $\dot{\mathbb{R}}^+$ is kontinuous.

However, some of these equivalences fail in the absence of countable choice. See

*  Moerdijk, Ieke. “Heine-Borel Does Not Imply the Fan Theorem.” Journal of Symbolic Logic, vol. 49, no. 2, 1984, pp. 514–519., doi:10.2307/2274182

which shows that the compactness of $[0, 1]$ does not necessarily imply the fan theorem constructively if one does not have some amount of countable choice available.

The decidable fan theorem (assuming some amount of countable/dependent choice) is equivalent to any of the following statements:

*  Every [[uniformly continuous map|uniformly continuous]] function from Cantor space to the [[metric space]] $\dot{\mathbb{R}}^+$ of positive real numbers has a positive lower bound.
*  Every [[uniformly continuous map|uniformly continuous]] function from the unit interval to $\dot{\mathbb{R}}^+$ has a positive lower bound.

For the above equivalences with the decidable fan theorem, see

*  Julian, W., &amp; Richman, F. (1984). A uniformly continuous function on [0,1] that is everywhere different from its infimum. Pacific Journal of Mathematics, 111(2), 333–340. https://doi.org/10.2140/pjm.1984.111.333 

The above paper unfortunately uses different terminology than this article; for example, using "branch-bounded" and "bounded" in place of "barred" and "uniform". The above paper also proves that, assuming all functions $\mathbb{N} \to \mathbb{N}$ are computable, there exists a decidable bar which is not uniform (and, as the title suggests, a uniformly continuous function $[0, 1] \to (0, \infty)$ whose range has an infimum of zero).

Some form of the fan theorem follows from any of these statements (some work needs to be done to verify these and get citations):

*  The [[bar theorem]] holds (see above)
*  As a locale, [[Baire space of irrational numbers|Baire space]] has enough points.
*  Every pointwise-continuous function on Cantor space is uniformly continuous.
*  Every pointwise-continuous function on the unit interval is uniformly continuous.
*  Every [[uniformity]] (or indeed any [[metric]]) compatible with the usual topology of Cantor space is [[totally bounded space|totally bounded]].
*  The property of being "complete and totally bounded", i.e. [[Bishop-compact]], is invariant under topological homemorphism between uniform (or metric) spaces.

I need to figure out how it relates to the various versions of [[Konig's lemma|König's Lemma]], as well as these statements (which are mutually equivalent):

*  As a locale, the unit interval has enough points.
*  As a locale, the [[real line]] (the [[locale of real numbers]]) has enough points.

Some of the results above may use [[countable choice]], but probably no more than $AC_{0,0}$ (which is choice for relations between $\mathbb{N}$ and itself).


### Analysis without the fan theorem

Point-wise real analysis without the fan theorem is very difficult, as shown by the example above from Waaldijk regarding "kontinuous" functions: without the fan theorem there isn't really even a good notion of continuity!  This was [[L.E.J. Brouwer|Brouwer]]\'s motivation for introducing the fan theorem.

However, the fan theorem (and bar theorem) can be avoided by instead using [[locales]] or another [[point-free topology|point-free]] approach to analysis.


### Sheaf models
[Fourman and Hyland](#FourmanHyland) provide a sheaf model not satisfying the fan theorem.


## Proofs

I should write down the classical proof (which uses [[excluded middle]]), as well as Brouwer\'s argument.

Ideally, a page on [[bar induction]] would be added. This page would contain the classical proof of full bar induction, as well as Brouwer's reasoning for why bar induction should hold. We would then provide constructive proofs here that monotone bar induction implies the full fan theorem, and that decidable bar induction implies the decidable fan theorem.

## References

*  Thanks to Giovanni Curi on [constructive news](http://groups.google.com/group/constructivenews/browse_thread/thread/9d57fa99e67e8782).

*  [Frank Waaldijk](http://www.fwaaldijk.nl/mathematics.html) pointed out exactly why point-wise analysis needs the fan theorem.

I need to read the relevant parts here:

*  [[Mike Fourman]], R. Grayson, _Formal Spaces_. In: The L.E.J. Brouwer Centenary Symposium,  A.S. Troelstra and D. van Dalen, eds. North Holland (1982), pp. 107--122.

More links that I need to keep in mind:

*  <http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html>
*  <http://www.jaist.ac.jp/is/labs/ishihara-lab/wcalm2010/berger.pdf>
*  <http://www.cairn.info/revue-internationale-de-philosophie-2004-4-page-483.htm>

Also:

* [[Mike Fourman]], [[Martin Hyland]], _Sheaf models for analysis_. [PDF](https://www.dpmms.cam.ac.uk/~martin/Research/Oldpapers/analysis79.pdf)
  {#FourmanHyland}


[[!redirects fan theorem]]
[[!redirects Fan theorem]]

[[!redirects classical fan theorem]]

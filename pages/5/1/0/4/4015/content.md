
# The fan theorem
* table of contents
{: toc}

## Introduction

The fan theorem is one of the basic principles of [[intuitionism]] that make it more specific (even in mathematical practice, independent of any philosophical issues) than garden-variety [[constructive mathematics]].  Its main use is to justify pointwise [[analysis]]; without it, one really needs [[locale theory]] instead.  In [[classical mathematics]], the fan theorem is true.


## Statement

Consider the [[list|finite]] and [[infinite sequence|infinite]] sequences of [[binary digit]]s.  Given an infinite sequence $\alpha$ and a [[natural number]] $n$, let $\bar \alpha n$ be the finite sequence consisting of the first $n$ elements of $\alpha$.

Let $B$ be a collection of finite sequences of bits (or _bitlists_), that is a [[subset]] of the [[free monoid]] on the [[boolean domain]].  Given an infinite sequence $\alpha$ and a natural number $n$, we say that $\alpha$ _$n$-bars_ $B$ if $\bar \alpha n \in B$; given only $\alpha$, we say that $\alpha$ _bars_ $B$ if $\alpha$ $n$-bars $B$ for some $n$.

We are interested in these three properties of $B$:

*  $B$ is _[[decidable subset|decidable]]_:  For every finite sequence $u$, either $u \in B$ or $u \notin B$.  (This is trivial in [[classical logic]] but will hold constructively only for some subsets $B$.)
*  $B$ is _barred_:  For every infinite sequence $\alpha$, $\alpha$ bars $B$.
*  $B$ is _uniform_:  For some natural number $M$, for every infinite sequence $\alpha$, if $\alpha$ bars $B$ at all, then $\alpha$ $n$-bars $B$ for some $n \leq M$.

A __bar__ is a barred subset $B$.

+-- {.un_theorem}
###### Fan Theorem

Every decidable bar is uniform.
(In other words, if a collection of bitlists is decidable and barred, then it is also uniform.)
=--

Although the fan theorem is about bars, it is different from the [[bar theorem]], which is related but stronger.


### Obfuscation

Let $\mathbb{B}$ be the set $\{0,1\}$ of binary digits (bits) and $\mathbb{N}$ the set $\{0,1,2,\ldots\}$ of natural numbers (numbers).  Given a [[set]] $A$, let $A^*$ be the set of finite sequences of elements of $A$, let $A^{\mathbb{N}}$ be the set of infinite sequences of elements of $A$, and let $\mathcal{P}_{\Delta}A$ be the set of decidable subsets of $A$.  Then the fan theorem is about (elements of) $\mathbb{B}^*$, $\mathbb{B}^{\mathbb{N}}$, and $\mathcal{P}_{\Delta}\mathbb{B}^*$.

However, the sets $\mathbb{N}$, $\mathbb{B}^*$, and $\mathbb{N}^*$ are all isomorphic.  Similarly, the sets $\mathbb{B}^{\mathbb{N}}$, $\mathcal{P}_{\Delta}\mathbb{N}$, $\mathcal{P}_{\Delta}\mathbb{B}^*$, and $\mathcal{P}_{\Delta}\mathbb{N}^*$ are all isomorphic.  In much of the literature on bars, one tacitly uses all of these isomorphisms, taking $\mathbb{N}$ and $\mathbb{B}^{\mathbb{N}}$ as chosen representatives of their isomorphism classes.  Thus, everything in sight is either a natural number or an infinite sequence of bits.

The fan theorem is hard enough to understand when $\alpha$ is an infinite sequence of bits and $\bar \alpha n$ is a finite sequence of bits; it is even harder to understand when $\bar \alpha n$ is a natural number that bears no immediate relationship to the digits in the sequence $\alpha$.


### Variations

The fan theorem may be stated about *all* bars, not just the decidable ones: all bars are uniform (which is true in classical mathematics).  Brouwer himself at one point claimed this, but later Kleene showed that this contradicted Brouwer\'s [[continuity theorem]].

Since decidability is classically trivial, we may call this the __classical fan theorem__.


## Use in analysis

In classical mathematics, the fan theorem is simply true.

In constructive mathematics, the fan theorem is equivalent to any and all of the following statements:

*  As a [[locale]], [[Cantor space]] has enough points (is [[topological locale|topological]]).
*  As a [[topological space]], Cantor space is [[compact space|compact]].
*  As a topological space, the (located Dedekind) [[unit interval]] is [[compact space|compact]] (the [[Heine-Borel theorem|Heine–Borel theorem]]).
*  As a topological space, the (located Dedekind) [[real line]] is [[locally compact space|locally compact]].
*  Every [[uniformly continuous map|uniformly continuous]] function from Cantor space to the [[metric space]] $\dot{\mathbb{R}}^+$ of positive real numbers has a positive lower bound.
*  Every [[uniformly continuous map|uniformly continuous]] function from the unit interval to $\dot{\mathbb{R}}^+$ has a positive lower bound.
*  There exists a class of "kontinuous" [[partial functions]] from the set $\mathbb{R}$ of (located Dedekind) [[real numbers]] to itself (see Waaldijk) such that
   *  the [[restriction]] of a kontinuous function to any smaller domain is kontinuous;
   *  the [[identity function]] on $\mathbb{R}$ is kontinuous;
   *  the [[composite]] of two kontinuous functions is kontinuous;
   *  a function whose domain is the unit interval is kontinuous *if and only if* it is uniformly continuous (in the usual metric-space sense); and
   *  the function $(x \mapsto 1/x)$ defined on $\dot{\mathbb{R}}^+$ is kontinuous.

It follows from any of these statements:

*  The [[bar theorem]] holds.
*  As a locale, [[Baire space of irrational numbers|Baire space]] has enough points.
*  Every pointwise-continuous function on Cantor space is uniformly continuous.
*  Every pointwise-continuous function on the unit interval is uniformly continuous.
*  Every [[uniformity]] (or indeed any [[metric]]) compatible with the usual topology of Cantor space is [[totally bounded space|totally bounded]].
*  The property of being "complete and totally bounded", i.e. [[Bishop-compact]], is invariant under topological homemorphism between uniform (or metric) spaces.

I need to figure out how it relates to the various versions of [[Konig's lemma|König's Lemma]], as well as these statements (which are mutually equivalent):

*  As a locale, the unit interval has enough points.
*  As a locale, the [[real line]] (the [[locale of real numbers]]) has enough points.

Some of the results above may use [[countable choice]], but probably no more than $AC_{0,0}$ (which is choice for relations between $\mathbb{N}$ and itself).


### Uselessness in analysis

Point-wise real analysis without the fan theorem is very difficult, as the example from Waaldijk shows.  This was Brouwer\'s motivation for introducing the fan theorem.  But if you use [[locales]] (or other pointless approaches), then you don\'t need the fan theorem (or bar theorem).


### Sheaf models
[Fourman and Hyland](#FourmanHyland) provide a sheaf model not satisfying the fan theorem.


## Proofs

I should write down the classical proof (which uses [[excluded middle]] and some form of [[dependent choice]]), as well as Brouwer\'s argument.


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

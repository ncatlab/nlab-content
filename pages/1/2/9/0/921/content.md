
#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

A **real number** is something that may be approximated by [[rational numbers]].  The real numbers form the **real line** $\mathbb{R}$, also known as the **continuum**, which is the corresponding completion of the set $\mathbb{Q}$ of rational numbers.

Here we are using the usual [[order|ordering]] of rational numbers; other ordings will give the $p$-[[adic number|adic numbers]] instead.

Together with its cartesian powers -- the [[cartesian spaces]] $\mathbb{R}^n$ -- the continuum encodes one basic idea of of _continuous space_.  The notion of (especially smooth) [[manifold]] is modeled on this notion.  It provides one of the basic models of [[space]], notably the standard model for _physical space_ and _time_ (see [[spacetime]]), at least in [[classical physics]].


### History of formalisations

The original idea of a real number came from [[geometry]]; one thinks of a real number as specifying a _point on a line_ , with _line_ understood as the abstract idea of the object that a pencil and a ruler draw on a piece of paper.  

(More precisely, given two distinct points on the line, called $0$ and $1$, you get a [[bijection]] between the points and the real numbers.)  [[Euclid]] (citing [[Eudoxus]]) dealt with ratios of geometric magnitudes, which give positive real numbers; an arbitrary real number is then a difference of ratios of magnitudes.  (But the Greeks did not think of such ratios as numbers.)

A big project of the 19th century (at least in hindsight) was the 'arithmetisation of analysis': showing how real numbers could be defined completely in terms of rational numbers (and the desired classes of functions on them could be defined in terms of the general point-set notion of [[function]]).  Two successful approaches were developed in 1972, [[Richard Dedekind]]\'s definition of real numbers as certain sets of rational numbers (called _Dedekind cuts_) and [[Georg Cantor]]\'s definition as certain sequences of rational numbers (called _Cauchy sequences_).

A more modern approach is instead to characterise the properties that the set of real numbers must have and to prove that this is [[generalized the|categorical]] (unique up to a unique bijection preserving those properties).  Then the important result of the 19th century programme is simply that this is consistent (that there exists at least one such set).  One can even use Hilbert\'s or Tarski\'s axioms for geometry to do this characterisation, coming full circle back to geometry.

Exactly how to define or characterise real numbers is still important in [[constructive mathematics]] and [[topos]] theory with its [[internal logic]] of every topos. For more on this see the examples below.


## Definitions and characterizations

There are two basic approaches possible: to define what a __real number__ is, as an general object, or to define the __real line__ is as a specific object in some previously known [[category]].


### Dedekind cuts

In 1872, [[Richard Dedekind]] published _Stetigkeit und irrationale Zahlen_ (Continuity and irrational numbers), in which he pointed out that a real number may be uniquely determined its order relationships with rational numbers.  That is, the real number $x$ is determined by its __lower set__ $L_x$ and its __upper set__ $U_x$:
\[ \label{cuts} \begin {split}
   L_x \coloneqq \{ a\colon \mathbb{Q} \;|\; a \lt x \} \\
   U_x \coloneqq \{ b\colon \mathbb{Q} \;|\; b \gt x \}
   .\end {split} \]
Dedekind had found great success understanding the 'ideal numbers' of [[ring theory]] as certain sets, which are what we now understand as [[ideal of a ring|ideals]].  So he defined a 'real number' as a pair of sets of rational numbers, the lower and upper sets shown above.

Such a pair of sets of rational numbers is a __Dedekind cut__.  But which pairs of sets of rational numbers can appear this way?  The simplest definition may be *any* pair $(L,U)$ of [[inhabited sets]] of rational numbers satisfying two conditions:

1.  If $a \lt b$ are rational numbers, then $a \in L$ or $b \in U$.
2.  If $a \in L$ and $b \in U$, then $a \lt b$.

The second condition simply guarantees the [[transitive relation|transitivity]] rule that $a \lt x \lt b$ implies $a \lt b$ (where $x$ is the real number in question).  The point of the first condition (1) is that we can estimate $x$ as closely as we like by choosing appropriate rational numbers.

This is entirely [[constructive mathematics|constructive]].  We have $a_0 \in L$ and $b_0 \in U$ (because these sets are known to be inhabited), so if we wish to estimate $x$ to within a positive rational number $\epsilon$, then we simply let $n$ be $\lceil{2/\epsilon}\rceil$ and apply (1) to each of the finitely many ($\lceil{n(b_0-a_0)}\rceil$) rational numbers with denominator $n$ that lie between $a_0$ and $b_0$.  This will eventually give us a numerator $i$ such that $(i-1)/n \lt x \lt (i+1)/n$, so we have estimated $x$ within $2/n \leq \epsilon$.  Alternatively, to estimate $x$ to $n$ digits after a decimal point (with an uncertainty of $1$ in the last digit), apply (1) to each of the $\lceil{(b_0-a_0) \times 10^n}\rceil$ numbers between $a_0$ and $b_0$ that have $n$ digits after the decimal point.

If we define a real number to be *any* such pair $(L,U)$, then there is a slight redundancy.  We can either define $(L,U)$ and $(L',U')$ to be equal as real numbers if, for any rational numbers $a \lt b$, $a \in L$ or $b \in U'$ and $a \in L'$ or $b \in U$.  (More generally, we have $(L,U) \leq (L',U')$ if we always have $a \in L$ or $b \in U'$.)  Alternatively, we can pick a representative pair by adding two more requirements:

3.  If $a \in L$, then $b \in L$ for some $b \gt a$.
4.  If $b \in U$, then $a \in U$ for some $a \lt b$.

Every real number has a unique representative Dedekind cut satisfying all four conditions, and in that case the sets $L$ and $U$ are the sets $L_x$ and $U_x$ in (eq:cuts).


#### One-sided cuts

...


#### Unbounded cuts

...


### The complete ordered field

...


### The locale of real numbers

A [[constructive mathematics|constructive]] construction of the real line is discussed at 

* [[locale of real numbers]].


### $\mathbb{R}$ as a terminal coalgebra

The real line $\mathbb{R}$, or at least the positive real line $\mathbb{R}^+$, may be characterized as the [[terminal object|terminal]] [[coalgebra for an endofunctor]]

Let [[Pos]] be the [[category]] of [[poset]]s. Consider the endofunctor

$$
  F_1 : Pos \to Pos
$$

that acts by [[ordinal product]] with $\omega$

$$
  F_1 : X \mapsto X \cdot \omega
  \,.
$$

+-- {: .un_prop}
###### Proposition

The terminal coalgebra of $F_1$ is order isomorphic to the non-negative real line $\mathbb{R}^+$, with its standard order.
=--

+-- {: .proof}
###### Proof

This is theorem 5.1 in

* D. Pavlovic, [[Vaughan Pratt]], _On coalgebra of real numbers_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.47.5204))
=--

> There are more and similar characterizations along these lines. Hopefully we can eventually fill them in here.


[[!redirects real number]]
[[!redirects real numbers]]
[[!redirects real line]]
[[!redirects real number line]]
[[!redirects continuum]]

[[!redirects Dedekind cut]]

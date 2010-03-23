
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

A big project of the 19th century (at least in hindsight) was the 'arithmetisation of analysis': showing how real numbers could be defined completely in terms of rational numbers (and the desired classes of functions on them could be defined in terms of the general point-set notion of [[function]]).  Two successful approaches were developed in 1872, [[Richard Dedekind]]\'s definition of real numbers as certain sets of rational numbers (called _[[Dedekind cuts]]_) and [[Georg Cantor]]\'s definition as certain sequences of rational numbers (called _[[Cauchy sequences]]_).

A more modern approach is instead to characterise the properties that the set of real numbers must have and to prove that this is [[generalized the|categorical]] (unique up to a unique bijection preserving those properties).  Then the important result of the 19th century programme is simply that this is consistent (that there exists at least one such set).  One can even use Hilbert\'s or Tarski\'s axioms for geometry to do this characterisation, coming full circle back to geometry.

Exactly how to define or characterise real numbers is still important in [[constructive mathematics]] and [[topos]] theory with its [[internal logic]] of every topos. For more on this see the examples below.


## Definitions and characterizations

There are two basic approaches possible: to define what a __real number__ is, as an general object, or to define the __real line__ is as a specific object in some previously known [[category]].


### Dedekind cuts

See [[Dedekind cut]].


### Cauchy sequences

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

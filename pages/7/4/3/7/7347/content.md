
# Maximal elements
* table of contents
{: toc}

## Idea

An element of a [[poset]] (or [[proset]]) is __maximal__ if no other (inequivalent) element is greater.  A [[top element|maximum]] must be maximal, and a maximal element of a [[toset]] must be a maximum.  However, it's easy to find posets with maximal elements that aren\'t maxima, or even with a unique maximal element that isn\'t a maximum.  The existence of a maximal element is often given by [[Zorn's lemma]].


## Definition

Let $P$ be a [[preordered set]] and $x$ an element of $P$.  Then $x$ is __maximal__ in $P$ if, whenever $x \leq y$ in $P$, we have $y \leq x$.  Dually, $x$ is __minimal__ in $P$ if, whenever $y \leq x$ in $P$, we have $x \leq y$.


## Properties

### Elementary properties

If $P$ has a [[top element]], then this is the unique (up to equivalence) maximal element of $P$.

Suppose that $P$ is [[totally ordered set|totally ordered]].  Then a maximal element of $P$ is the same as a [[top element]] of $P$.

Suppose that $P$ is [[finite set|finite]] and has a unique maximal element $x$.  Then $x$ is a top element of $P$.


### Deep properties

According to [[Zorn's Lemma]], if every [[totally ordered set|totally ordered]] [[subset]] of $P$ has an [[upper bound]] in $P$, then $P$ has a maximal element.


## Examples

Let $P$ be $\{a,b,c\}$ with $a \leq b$, $a \leq c$, and no other nontrivial ordering.  Then $b$ and $c$ are both maximal in $P$ (but of course not tops).

Let $P$ be the [[disjoint union]] of $\mathbb{N}$ (the poset of [[natural numbers]]) and a [[singleton]] \{a\}.  Then $a$ is the unique maximal element of $P$ but still not a top.


[[!redirects maximal element]]
[[!redirects maximal elements]]
[[!redirects minimal element]]
[[!redirects minimal elements]]

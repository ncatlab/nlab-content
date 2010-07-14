# Positive elements
* table of contents
{: toc}

## Idea

At least in [[classical mathematics]], an element of a [[poset]] is positive if and only if it not a [[bottom element]].

A more subtle definition is needed in [[constructive mathematics]]; compare the notion of [[inhabited set]].  In [[predicative mathematics|predicative]] constructive mathematics, positivity can be axiomatised but not defined.


## Definitions

There are two definitions, one of which is useful predicatively but not constructively, and one of which is useful constructively but not predicatively.

*  Let $L$ be a [[preordered set]], and let $x$ be an element of $L$.  Then $x$ is __positive__ if $x$ is there exists an element $y$ such that $x \leq y$ is false.

*  Let $L$ be a [[preordered set]], and let $x$ be an element of $L$.  There may be many ways to write $x$ as a [[join]] of some [[subset]] $A$ of $L$.  If in every such way, $A$ is [[inhabited subset|inhabited]], then $x$ is __positive__.

Classically, these two definitions are equivalent.


## In weak foundations

There does not seem to be any way to define the notion of positive element in a predicative way that matches the constructive definition.  However, one can consider a poset $L$ equipped with a __positivity predicate__ satisfying these conditions:

*  Whenever $x$ is positive and $x$ is the join of $A$, then some element of $A$ is positive;
*  If $x$ is the join of $A$ on the assumption that $x$ is positive, then $x$ really is the join of $A$.

Then one can prove, predicatively but not constructively, that every poset has a unique positivity predicate, which must match the first definition above; and one prove, constructively but not predicatively, that every poset has a unique positivity predicate, which must match the second definition above.


[[!redirects positive element]]
[[!redirects positive elements]]
[[!redirects positivity predicate]]
[[!redirects positivity predicates]]

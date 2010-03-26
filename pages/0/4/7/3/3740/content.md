# One-sided real numbers
* table of contents
{: toc}


## Summary

There are really two notions of one-sided real number: lower reals and upper reals.  But there is a perfect symmetry between them.

These are really concepts in [[constructive mathematics]].  Using [[excluded middle]], a one-sided real number is simply a [[real number]], but constructively they are more general (and less well behaved).

Actually, there is a small technicality: most naturally, a lower real may (classically) be either a real number or $\infty$, while an upper real may be either a real number or $-\infty$.  You can restrict to _bounded_ lower/upper reals to avoid that, or alternatively genralise to _extended_ lower/upper reals if you want to include both $\pm\infty$ at once.

Lower and upper reals don\'t interact well together; for a system that naturally includes both (and, constructively, much more), use the [[MacNeille real number]]s.


## Idea

A __lower real number__ is the [[supremum]] of an [[inhabited set|inhabited]] set of [[real numbers]], or equivalently of an inhabited set of [[rational numbers]].  A __bounded lower real__ is the supremum of an inhabited set of numbers that has a finite upper bound.  An __extended lower real__ is the supremum of an arbitrary set of  real numbers.

An __upper real number__ is the [[infimum]] of an inhabited set of numbers.  A __bounded upper real__ is the infimum of an inhabited set of numbers that has a finite upper bound.  An __extended lower real__ is the supremum of an arbitrary set of numbers.

We cannot generalise further by taking more infima or suprema.  Explicitly, the supremum of any inhabited set of lower reals is a lower real and the infimum of any inhabited set of upper reals is an upper real.  Similar results obtain if we manipulate 'bounded' and 'extended' to include or exclude $\pm\infty$, or to allow for infima and suprema of the [[empty subset|empty set]].


## Definitions

There are some choices as to how exactly to represent one-sided real numbers; we will define them here as certain [[subsets]] of the set $\mathbb{Q}$ of [[rational numbers]].


### Lower reals

An __extended lower real number__ is any subset $L$ of $\mathbb{Q}$ such that

*  if $a \in L$, then $a \lt b$ for some $b \in L$; and
*  if $a \lt b$ and $b \in L$, then $a \in L$.

We can actually combine these into a single rule:

*  $a \in L$ if and only if $a \lt b$ for some $b \in L$.

A __lower real number__ is an extended lower real $L$ such that:

*  some $a \in L$.

A __bounded lower real number__ is a lower real $L$ such that

*  some $b \notin L$.

When treated explicitly as a subset of $\mathbb{Q}$, we call $L$ a __lower set__.  When we interpret $L$ as a number $x$, we write $a \lt x$ to mean that $a \in L$.  Conversely, we can interpret any rational number, or even any real number, $x$ as a bounded lower real, specifically as the set of all rational numbers less than $x$.  We interpret $\infty$ as the lower real whose lower set is all of $\mathbb{Q}$; we interpret $-\infty$ as the extended lower real whose lower set is empty.

A bounded lower real is __located__ if it is the lower real obtained in this way from a real number.


### Upper reals

An __extended upper real number__ is any subset $U$ of $\mathbb{Q}$ such that

*  if $b \in U$, then $a \lt b$ for some $a \in U$; and
*  if $a \lt b$ and $a \in U$, then $b \in U$.

We can actually combine these into a single rule:

*  $b \in U$ if and only if $a \lt b$ for some $a \in U$.

An __upper real number__ is an extended upper real $U$ such that:

*  some $b \in U$.

A __bounded upper real number__ is an upper real $U$ such that

*  some $a \notin U$.

When treated explicitly as a subset of $\mathbb{Q}$, we call $U$ an __upper set__.  When we interpret $U$ as a number $x$, we write $x \lt b$ to mean that $b \in U$.  Conversely, we can interpret any rational number, or even any real number, $x$ as a bounded upper real, specifically as the set of all rational numbers greater than $x$.  We interpret $-\infty$ as the upper real whose upper set is all of $\mathbb{Q}$; we interpret $\infty$ as the extended upper real whose upper set is empty.

A bounded upper real is __located__ if it is the upper real obtained in this way from a real number.


## Order relations

We define [[order]] relations between extended lower reals $x$ and $y$ as follows:

*  $x \lt y$ if and only if there exists a rational number $a$ such that $a \lt y$ but not $a \lt x$;
*  $x \leq y$ if and only if $a \lt y$ for every rational number $a$ such that $a \lt x$.

In other words, $\leq$ is $\subseteq$ on lower sets, and $\lt$ is $\subsetneq$ (in an appropriate sense).

We define order relations between extended upper reals $x$ and $y$ as follows:

*  $x \lt y$ if and only if there exists a rational number $b$ such that $x \lt b$ but not $y \lt b$;
*  $x \leq y$ if and only if $x \lt b$ for every rational number $b$ such that $y \lt b$.

In other words, $\leq$ is $\supseteq$ on upper sets, and $\lt$ is $\supsetneq$.

We now have multiple meanings for $x \lt y$ or $x \leq y$ if one or both of these is already a rational number or a real number, but it is a theorem that the meanings are all consistent.  We also have $-\infty \leq x \leq \infty$ for every extended number $x$, and $-\infty \lt x \lt \infty$ for every bounded number $x$.  Finally, $x \leq y$ if $x \lt y$.

Each version of $\leq$ is a [[partial order]] and each version of $\lt$ is a [[quasiorder]].  By [[excluded middle]], $\leq$ is a [[total order]] and $\lt$ is the corresponding [[linear order]], but neither of these results holds constructively.  In particular, the [[comparison]] law for $\lt$ is invalid, which is why one-sided reals are not as well behaved as ordinary (located Dedekind) [[real numbers]].


## Suprema and infima

Given any collection of extended lower reals, their __supremum__ is an extended lower real which is found by taking the [[union]] of lower sets.  The supremum of an inhabited set of lower reals is a lower real, and the supremum of an inhabited set of bounded lower reals is bounded iff the set has a bounded lower real as an upper bound.  In any case, this supremum really is the [[supremum]] under $\leq$.  This agrees with the notion of supremum of real numbers in the real number system, when that exists.  Every extended lower real is also the supremum in this sense of its corresponding lower set, interpreted as a set of lower reals that happen to all be rational numbers.

Given any collection of extended upper reals, their __infimum__ is an extended upper real which is found by taking the union of upper sets.  The infimum of an inhabited set of upper reals is an upper real, and the infimum of an inhabited set of bounded upper reals is bounded iff the set has a bounded upper real as a lower bound.  In any case, this infimum really is the [[infimum]] under $\leq$.  This agrees with the notion of infimum of real numbers in the real number system, when that exists.  Every extended upper real is also the infimum in this sense of its corresponding upper set, interpreted as a set of upper reals that happen to all be rational numbers.

Constructively, we cannot necessarily take the infimum of a set of lower reals, nor the supremum of a set of upper reals.  We can, however, interpret such a supremum or infimum as a [[MacNeille real number]].


## Arithmetic

In general, you can extend order-preserving functions of rational numbers to lower reals and to upper reals; you simply take the [[image]] of the lower or upper set and close it downward or upwards, as appropriate.  If you have an order-reversing function of rational numbers, then you can apply it to a lower real to get an upper real and conversely; this is about the only interaction that I know of between the two kinds of one-sided real.

Since addition is order-preserving, it works nicely, at least to make a [[monoid]]; but subtraction doesn\'t work in general.  Multiplication has trouble with negative numbers but produces good results if you restrict to $[0,\infty]$.  Notice that we get $0 \cdot \infty = 0$ with lower reals but $0 \cdot \infty = \infty$ with upper reals; thus, $[0,\infty)$ is a [[rig]] for either lower or upper reals, while $[0,\infty]$ is a rig only for lower reals.  We can also use [[logarithm]]s to translate between addition and multiplication.

If you really want to do arbitrary arithmetic operations on upper or lower reals, then again you need their common generalisation, the [[MacNeille real number|MacNeille reals]].


[[!redirects one-sided real]]
[[!redirects one-sided reals]]
[[!redirects one-sided real number]]
[[!redirects one-sided real numbers]]

[[!redirects lower real]]
[[!redirects lower reals]]
[[!redirects lower real number]]
[[!redirects lower real numbers]]
[[!redirects bounded lower real]]
[[!redirects bounded lower reals]]
[[!redirects bounded lower real number]]
[[!redirects bounded lower real numbers]]
[[!redirects extended lower real]]
[[!redirects extended lower reals]]
[[!redirects extended lower real number]]
[[!redirects extended lower real numbers]]

[[!redirects upper real]]
[[!redirects upper reals]]
[[!redirects upper real number]]
[[!redirects upper real numbers]]
[[!redirects bounded upper real]]
[[!redirects bounded upper reals]]
[[!redirects bounded upper real number]]
[[!redirects bounded upper real numbers]]
[[!redirects extended upper real]]
[[!redirects extended upper reals]]
[[!redirects extended upper real number]]
[[!redirects extended upper real numbers]]

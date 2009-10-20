A _structure type_ is a categorified generating function.  Whereas a generating function assigns a number to each natural, a structure type assigns a groupoid.

If we think of the term $Z^n$ as "the set with $n$ elements", then the coefficient is the groupoid of ways for the set to be enowed with the given structure.  For example, the structure type "being a finite set" is
\[E^Z := \frac{1}{\overline{0!}} + \frac{1}{\overline{1!}}Z + \frac{1}{\overline{2!}}Z^2 + \cdots + \frac{1}{\overline{n!}}Z^n + \cdots,\]
where $+$ is disjoint union, $//$ is the weak quotient, $n!$ is the permutation group $S_n$, and $1$ is the one-element set (since there's only one way to be finite).

The structure type "being a totally ordered even set" is
\[\frac{1}{(1-Z)^2} := \frac{0!}{\overline{0!}} + 0Z + \frac{2!}{\overline{2!}}Z^2 + 0Z^3 + \cdots,\]
since there are $n!$ ways to order a set with $n$ elements and $0$ ways for an odd set to be even.

Structure types generalize to [[stuff types]].

See [Baez](John+Baez)'s Fall 2003 to Spring 2004 [quantum gravity notes](http://math.ucr.edu/home/baez/qg-fall2003/).
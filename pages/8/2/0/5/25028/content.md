
# Line segments
* table of contents
{: toc}

## Idea

A line segment is a fundamental feature of [[geometry]], going back to [[Euclid]] (and probably much earlier), and particularly relevant in [[convex spaces]].  In general, a line segment is that which lies between two [[points]].


## Definitions

In [[synthetic geometry]], a __line segment__ may be regarded as an [[unordered pair]] $\{p,q\}$ of [[points]], called the __endpoints__ of the line segment. A __directed line segment__ is given by an *[[ordered pair|ordered]]* pair of points; so we speak of the directed line segment *from* $p$ *to* $q$ instead of the (undirected) line segment *between* $p$ *and* $q$. Generally, the endpoints are required to be distinct; otherwise the line segment is __degenerate__.

In [[analytic geometry]], where geometric figures are conceived of as sets of points, the __closed line segment__ between $p$ and $q$ consists of $p$, $q$, and every point in between, while the __open line segment__ consists of the points strictly between $p$ and $q$ but not the endpoints themselves. (One can also consider half-open/half-closed versions.) Then a *directed* line segment from $p$ to $q$ (with the same open/closed variations) is a line segment between $p$ and $q$ equipped with an [[orientation]].

In axiomatic approaches to geometry, the concept of 'between' from the previous paragraph is undefined, so that line segments are a fundamental concept.  But in a [[convex space]] (including [[Cartesian spaces]] and other [[topological vector spaces]]), where we can form linear combinations of points (as long as the coefficients are positive and have unit sum) we may say that $r$ is __[[betweenness|between]]__ $p$ and $q$ if $r = t p + (1 - t) q$ for some $t \in [0,1]$ and __strictly between__ if this is so for some $t \in (0,1)$.  Now the closed and open line segments are fully defined (in terms of the operation of taking convex-linear combinations).  In other words, the closed line segment between $p$ and $q$ is the [[convex hull]] of the set $\{p,q\}$.

A line segment should be distinguished from a __line__ (vastly generalized at [[line]]), which has no endpoints but continues to [[infinity]].  (There is also a __ray__, which has one endpoint but continues infinitely in the other direction.)  In classical [[Euclidean geometry]], lines are prominent, but they are treated as being only *potentially* infinite.  So a line at any stage of construction is always a line segment, but one of the basic constructions is to extend such a line segment to a larger one, considered to still be the same line.  In this way, a line can be thought of as an [[equivalence class]] of line segments, so equivalently as an equivalence class of pairs of (distinct) points.

+-- {: .un_remark}
###### Notation

The line segment between $p$ and $q$ is traditionally denoted $\overline{p q}$.  The directed line segment from $p$ to $q$ may be denoted $\overrightarrow{p q}$, but this is also used for other things, including the ray from $p$ through $q$ (and then a double-headed arrow is used for the line through $p$ and $q$).  Another way to write a directed line segment is $[p,q]$ (borrowing from notation for [[intervals]]), and sometimes this is even used for the undirected line segment, since it allows one to distinguish the closed line segment (as above) from the open line segment $(p,q)$.
=--


[[!redirects line segment]]
[[!redirects line segments]]

[[!redirects degenerate line segment]]
[[!redirects degenerate line segments]]
[[!redirects closed line segment]]
[[!redirects closed line segments]]
[[!redirects open line segment]]
[[!redirects open line segments]]

[[!redirects directed line segment]]
[[!redirects directed line segments]]

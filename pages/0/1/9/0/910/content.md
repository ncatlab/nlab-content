# Idea #

A [[topological space]] is _compactly generated_ if (in a certain sense) the continuous images in it of all [[compact Hausdorff space]]s tell you everything about its topology.

Compactly generated spaces form a [[convenient category of topological spaces]].

# Definitions #

A map $f:X\to Y$ of topological spaces is __$k$-continuous__
if $f \circ t:C \to Y$ is continuous for all compact Hausdorff spaces $C$ and continuous functions $t: C \to X$.

The following conditions on a space $X$ are equivalent:

1. For all spaces $Y$ and all functions $f:X \to Y$, $f$ is
continuous if and only if $f$ is $k$-continuous.
1. There is a set $S$ of compact Hausdorff spaces such that the previous condition holds for all $C \in S$.
1. $X$ is an [[identification space]] of a [[disjoint union]] of compact Hausdorff spaces.
1. A subset $U\subseteq X$ is open if and only if $t^{-1}(U)$ is open for any compact Hausdorff space $C$ and continuous $t:C\to X$.

A space $X$ is a __$k$-space__ if any (hence all) of the above conditions hold.  Some authors also say that a $k$-space is __compactly generated__, while others reserve that term for a $k$-space which is also _weak Hausdorff_, meaning that the image of any $t:C\to X$ is closed (when $C$ is compact Hausdorff).

# Cartesian closure #

The category $k\Top$ of topological spaces and $k$-continuous maps is [[cartesian closed category|cartesian closed]]. In fact the exponential map 
$$k\Top(X \times Y, Z) \to kTop(X,k\Top(Y,Z))$$
is a homeomorphism (not just a $k$-homeomorphism). 

The topology on $k\Top(X,Y)$ that is used here is the test-open
topology, which has the subbase of sets $M(t,U)$ for a given $t: C
\to X$ and $U$ open in $Y$ of all $k$-continuous functions $f:X \to
Y$ such that $f(t(C))\subseteq U$.

It follows that the category of $k$-spaces and continuous maps is also cartesian closed.  This remains true if we also impose the weak Hausdorff condition.

# Local cartesian closure #

Unfortunately neither of the above categories is [[locally
cartesian closed category|locally
cartesian closed]]. There is still a lot of work on fibred exponential
laws and their applications. One reason for the success and
difficulties is that it is easy to give a topology on the space of
closed subsets of a space $X$ by regarding this as the space of maps
to the [[Sierpinski space]] (the set $\{0,1\}$ of [[truth value]]s in which $\{1\}$
is closed but not open). From this one can get an exponential law for
spaces over $B$ if $B$ is $T_0$, so that all fibres of spaces over
$B$ are closed in their total space.  Note that weak Hausdorff implies $T_0$.

+--{: .query}
[[Mike Shulman]]: What precisely does "get an exponential law" mean?  Do you mean that $k Top/B$ is cartesian closed if $B$ is $T_0$?
=--


# References #

* R. Brown, _Topology and groupoids_, Booksurge 2006, section 5.9. 

* Booth, Peter I.; Heath, Philip R.; Piccinini, Renzo A.
Fibre preserving maps and functional spaces. Algebraic topology (Proc. Conf., Univ. British Columbia, Vancouver, B.C., 1977), pp. 158--167, Lecture Notes in Math., 673, Springer, Berlin, 1978.

* J. P. May, _A Concise Course in Algebraic Topology_, Chapter 5 (I think)

[[!redirects compactly generated spaces]]
[[!redirects k-space]]
[[!redirects k-spaces]]

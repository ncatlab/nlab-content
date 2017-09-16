# Idea #

A [[topological space]] is _compactly generated_ if (in a certain sense) the continuous images in it of all compact Hausdorff spaces tell you everything about its topology.

Compactly generated spaces form a [[convenient category of topological spaces]].

The following conditions on a space $X$ are equivalent.

1. For all spaces $Y$ and all functions $f:X \to Y$, $f$ is
continuous if and only if $ft:C \to Y$ is continuous for all compact
Hausdorff spaces $C$ and continuous functions $t:C \to X$.

1. There is a set $S$ of compact Hausdorff spaces such that the
previous condition holds for all $C \in S$.

1. $X$ is an identification space of a disjoint union of compact
Hausdorff spaces.

## Definition ## 

A space $X$ is a $k$-space, or is compactly generated,
if any of the above conditions hold.

## Definition ## 

A map $f:X\to Y$ of topological spaces is $k$-continuous
if $ft:C \to Y$ is continuous for all compact Hausdorff spaces $C$ and
continuous maps $t: C \to X$.

## Proposition ## 

The category $k$Top of topological spaces and $k$-continuous maps is cartesian closed.

## Note ## 

The topology on $Top(X,Y)$ that is used here is the test-open
topology, which has the subbase of sets $M(t,U)$ for a given $t: C
\to X$ and $U$ open in $Y$ of all $k$-continuous functions $f:X \to
Y$ such that $ft(C)\subseteq U$.

## Corollary ## 

The category of compactly generated spaces and continuous maps is cartesian closed.

## Remark ## 

Unfortunately neither of the above categories is locally
cartesian closed. There is still a lot of work on fibred exponential
laws and their applications. One reason for the success and
difficulties is that it is easy to give a topology on the space of
closed subsets of a space $X$ by regarding this as the space of maps
to the Sierpinski space $\{0,1\}$ in which the set consisting of 1
is closed but not open. From this one can get an exponential law for
spaces over $B$ if $B$ is $T_0$, so that all fibres of spaces over
$B$ are closed in their total space.


## References ##

* R. Brown, _Topology and groupoids_, Booksurge 2006, section 5.9. 

* Booth, Peter I.; Heath, Philip R.; Piccinini, Renzo A.
Fibre preserving maps and functional spaces. Algebraic topology (Proc. Conf., Univ. British Columbia, Vancouver, B.C., 1977), pp. 158--167, 
Lecture Notes in Math., 673, Springer, Berlin, 1978.
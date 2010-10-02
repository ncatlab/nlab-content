
# Bridge number
* table of contents
{: toc}

## Definitions

A __bridge__ in a [[knot diagram]] is an arc that is the overpass in at least one crossing.

The __bridge number__, $b(K)$ of a [[knot]] $K$ is the minimum number of bridges occuring in a diagram of the knot.

By convention the [[unknot]] has bridge number equal to $1$.

+-- {: .query}
Why not $0$?  (I don\'t see any bridges in the obvious diagram.)  Are there numerical operations on bridge numbers that only work for the unknot if its bridge number is $1$?  Can we motivate the existence of a bridge in the unknot by proper application of [[negative thinking]]?
=--


## Example

The usual picture of the trefoil knot, which we will write as $T_{2,3}$,






 has three bridges, but the trefoil knot actually has bridge number 2. 

The first drawing corresponds to the picture as a (2,3)-[[torus knot]]. The knot thus can be represented on the surface of a solid torus $S^1\times D^2$ in $S^3$. The 3-sphere can be represented as the union of two solid tori with, in this case, the second one being $D^2\times S^1$, where the boundary of the $D^2$ in each case is the corresponding $S^1$ of the other case. Thinking of the trefoil on this other solid torus it is a $(3,2)$-torus knot .... (the second picture) and this has just two bridges, so $b(T_{2,3})\leq 2$.

How does one know that the trefoil does not have $b(K) = 1$.  For that we use
+-- {: .un_proposition}
###### Proposition

A knot $K$ has $b(K) = 1$ if and only if $K$ is the unknot.
=--

To complete the proof one needs to show or know that the trefoil is a non-trivial knot. That is most simply done using some invariant such as 3-[[n-colorability|colorability]].


[[!redirects bridge number]]
[[!redirects bridge numbers]]

Given a [[semi-free differential graded algebra]] $\Omega^\bullet A$ over $k$-algebra $A$, a __connection__ in $A$-module $M$ is a $k$-linear map 

$$
\nabla : M\otimes_A\Omega^\bullet A \to M\otimes_A\Omega^{\bullet+1} A
$$

such that for any homogenous element $\omega\in\Omega^k A$ and an element $\chi\in\Omega A$ 

$$
\nabla (\omega\chi) = \nabla(\omega)\chi + (-1)^k\omega\nabla(\chi)
$$

The curvature $F_\nabla$ of the connection $\nabla$ is the restriction of the connection squared to $M$:

$$\nabla\circ\nabla|_M : M\to M\otimes_A\Omega^2 A. $$ 

A connection is __flat__ (or integrable) iff its curvature vanishes. 

See also [[connection in noncommutative geometry]] as some versions are close to this approach. A past query on history of the notion of connection for a dga is archived [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=3107&Focus=25779#Comment_25779).

[[!redirects connection for a dga]]
[[!redirects connections for a differential graded algebra]]